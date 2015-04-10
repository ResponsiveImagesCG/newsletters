# Fuzzy logic

Teaser: A shaky choose-your-own-adventure analogy and a bunch of good implementation news

## Picking resources

Blink’s `srcset` selection logic [just changed](https://codereview.chromium.org/1045353002/), “due to complaints of quality issues related to the geometric-mean based resource selection.”

Uh, [come again?](http://bukk.it/hamm-wat.gif)

Let me explain – say you’re a browser. Due to the flexibility afforded by the spec, you approach every `srcset` like a tiny choose-your-own-adventure: you’re presented with a set of options, and while none of them are ever going to be wrong, per-se, some of them are definitely [worse](http://youchosewrong.tumblr.com/post/94449663144/from-choose-your-own-adventure-17-the-race).

So, let’s say that you, the browser, have been tasked with picking a resource to paint across a 900-`px`-wide piece of the layout on a 1x screen. Here are your options:

```
srcset="tiny.jpg 400w, medium.jpg 800w, enormous.jpg 1600w"
```

Which JPEG do you choose? You can either save a bunch of bytes and upscale `medium.jpg` by ~10%, or load an enormous amount of extra data only to downscale `enormous.jpg` by ~40%.

Blink’s original implementation followed an old rule-of-thumb: never upscale, because it looks [awful](http://ericportis.com/etc/updog.html).

But it’s easy to come up with examples where upscaling is the right thing to do. What if the too-small resource is only a pixel short, and the too-big resource weighs a megabyte more? There’s a line, somewhere.

Blink’s first attempt at drawing that line used something called a “[geometric mean](http://en.wikipedia.org/wiki/Geometric_mean).” In short, Blink began picking whichever resource was *closer* to the optimal size, rather than picking the *smallest resource that was bigger*.

Which meant a lot of upscaling, a lot of the time. Which upscaling front-end developers have begun to notice, and be surprised by, and [code around](https://twitter.com/PerryGStudio/status/578908993608921089), and [file bugs about](https://code.google.com/p/chromium/issues/detail?id=471337). Jason Grigsby made a strong case against the new geometric-mean-based logic [in the RICG IRC](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-30#T121658):

> I believe browsers should err on the side of never scaling up unless they can demonstrably prove they can do so without it looking terrible.
>
> This is the first time that I know of that authors have intentionally given the browser options. That’s a trust issue. Break that trust and it will be hard to get back.

A compromise was enacted: Blink will now never upscale on 1x screens, where the resulting blur is especially noticeable. But it’ll upscale freely (using the aforementioned geometric mean) on HiDPI displays. To my eyes, a 1.5x image on a 2x screen looks fine, but a 0.75x image on a 1x screen looks bad, so this seems reasonable.

Picking something that “seems reasonable” is fine for now, but browsers have an opportunity to do better. What we need is *science*. Dave Newton has [proposed a survey](https://github.com/nwtn/browser-scaling-test/blob/master/README.md) meant to determines what level of upscaling subjects find A) noticeable and B) acceptable, and Yoav Weiss has [started thinking about](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-30#T121700) how to use computable metrics like [DSSIM](http://en.wikipedia.org/wiki/Structural_similarity) in this quest. Me myself, I’m still trying to understand all of the variables that play into the problem of picking an image that’s “sharp enough,” which led me to whip up a little [visual angle calculator](http://ericportis.com/etc/visual-angle-calculator/).

If any of this sounds exciting (or, better yet, frustratingly amateur) and you’d like to point us to (or conduct!) some applicable research, please hop on the [WC3 IRC](https://www.w3.org/wiki/IRC) (channel: “respimg”), fire an email off to the RICG [mailing list](https://lists.w3.org/Archives/Public/public-respimg/), or simply hit up the [RICG Twitter](https://twitter.com/respimg).

Hm, that went a bit long, didn’t it? Let’s cram everything else into the grab bag!

## Grab bag

- Microsoft’s new Spartan browser – just released in the [Windows 10 Technical Preview](http://windows.microsoft.com/en-us/windows/preview-iso) – [implements `srcset`](http://blogs.msdn.com/b/ie/archive/2015/03/30/quot-project-spartan-quot-in-the-windows-technical-preview-build-10049.aspx)! It’s `x`-descriptors only at the moment, but you can always fill out the rest of the respimg functionality with Picturefill. The Picturefill team is getting [way out ahead of this one](https://github.com/scottjehl/picturefill/issues/478), and have pushed out v2.3.1 for the sake of Spartan support.

- Jason Grigsby’s excellent <cite>Responsive Images 101</cite> series has a new installment: [`picture`](http://blog.cloudfour.com/responsive-images-101-part-6-picture-element/).

- Dave Newton is porting his amazing, byte-saving [grunt-respimg](https://www.npmjs.com/package/grunt-respimg) optimal-image-resizing tool to [PHP](https://github.com/nwtn/php-respimg/).

- Yoav’s [asynchronous image loading patch](https://bugs.webkit.org/show_bug.cgi?id=134488) (the last brick in the lower-level foundation he needs before he can start implementing the new bits of markup in earnest) landed in WebKit ... only to be reverted a few hours later because the patch caused a few tests to go wonky.

- Yoav landed [a Blink patch](https://codereview.chromium.org/1078633003/) that’ll send [RW hints](http://igrigorik.github.io/http-client-hints/#the-rw-client-hint) to the server based on an image’s `sizes` attribute, if present. This is a vast improvement over the initial implementation, which just used the width of the viewport.

- Mark Crawford wrote up a [nice recap](http://www.iterate.ie/blog/getting-ready-responsive-images) of Yoav’s SmashingConf Oxford presentation.

- Mozilla’s respimg implementation is [shaping](https://bugzilla.mozilla.org/show_bug.cgi?id=1139560) [up](https://bugzilla.mozilla.org/show_bug.cgi?id=1064083) nicely, just in time for its version 38 debut.

See you in a couple of weeks!

—eric
