# Crazy Eights

***Teaser:** Firefox gets respimg! Drupal gets respimg! Ev-er-y-bo-dy gets a respimg!*

## 38 Special

Firefox users! Belatedly elate! Your images will soon be very lightweight.

[`picture`](https://bugzilla.mozilla.org/show_bug.cgi?id=1017875) and [`srcset`](https://bugzilla.mozilla.org/show_bug.cgi?id=1018389) have been [turned on by default in Firefox Nightly](https://twitter.com/FirefoxNightly/status/567870148763209728), and are slated for Firefox 38 — release date: [May 19th](http://release.mozilla.org/planning/2015/01/13/release-schedule.html).


What is it about version 38s? Is their greatness innate? The first responsive image implementations landed in *Chrome **38*** and Opera, uh, 25 [back in October](http://us8.campaign-archive2.com/?u=c988d9ca55d5d09e73a7dc993&id=58a0665da3&e=[UNIQID]).

The wait for Gecko respimg was a bit longer than anticipated; issue-owner John Schoenick left Mozilla for Valve back in November. But Josh Matthews picked up where John left off and succeeded this week in pushing the implementations across the finish line.

Huzzah!

## Drupal for your pupils

[Responsive image support landed in Drupal 8 this week](https://www.drupal.org/node/2260061). I’ve played with the implementation a bit and it’s fascinating to see how it differs from [WordPress’](https://wordpress.org/plugins/ricg-responsive-images/) — whereas the WordPress respimg plugin tries very hard to keep things simple and automagic, Drupal’s support is much more structured, providing developers with tremendous control (but requiring more setup).

Next up for Drupal: [a UI](https://www.drupal.org/node/2334387) to make that control accessible to people who don’t like mucking around in `.yml` files.

## WebKit, slow and steady

Don’t look now, but Yoav is persistently laying the foundations for respimg in WebKit. Exhibit A: [microtask abstractions](https://html.spec.whatwg.org/multipage/webappapis.html#microtask), which saw [a new batch of patches](https://bugs.webkit.org/show_bug.cgi?id=137496) this week. Let’s be honest: while I might be able to mumble a few vague words about how microtasks enable [asynchronous image loading](https://bugs.webkit.org/show_bug.cgi?id=134488) in response to [changing media conditions](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2014-07-11.md#responsive-elements-in-blink--complete-picture-implementation-imminent), I wouldn’t recognize a microtask abstraction if it hit me in the face. But! I trust Yoav when he tells us that microtask-in-WebKit progress is respimg progress: slow, steady, and inexorable.

## Client hints in Blink?

[Client Hints](https://github.com/igrigorik/http-client-hints) move the complexities of alternate resources, `x` descriptors, and `w` descriptors out of `srcset` attributes and into HTTP headers. Using Client Hints, markup can point to a single `src`. Browsers may send various “hints” — about their `device-pixel-ratio`, the layout width of the image, or their maximum download speed — as headers on the request for that `src`; the server can then use those hints to choose an alternate, more appropriate resource to send in response.

Yoav posted an [intent to implement thread](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/vOgv-TqefsA/o_fEsy8RFcwJ) about Client Hints over on blink-dev this week. Let’s see where it goes!

## Automatically optimal compression

Artisanal-ly “Save for Web…”-ing every image by hand is fine for bespoke websites, but automated image compression is the name of the game for anything larger. Two great, recent, developments on that front:

1. [imgmin](https://github.com/rflynn/imgmin) — the tool that lets you standardize image quality around an objective metric, rather twiddling an arbitrary and mysterious 0-100 encoder knob — has [integrated the <abbr title="structural dissimilarity">DSSIM</abbr> metric](https://github.com/rflynn/imgmin/pull/43). [Structural (dis)similarity](http://en.wikipedia.org/wiki/Structural_similarity) is [Kornel Lesiński’s favorite image quality metric](https://github.com/rflynn/imgmin/issues/30); therefore it is also mine.
2. Dave Newton is constructing a [massive set of tests](https://github.com/nwtn/image-resize-tests) for all of [ImageMagick](http://www.imagemagick.org/)’s compression and conversion options. These tests are the raw material for an upcoming [talk](http://www.meetup.com/Toronto-Web-Performance-Group/events/220287399/) and article on the subject – I can’t wait!


## Grab bag

- Matt Wilcox wrote up his [fantastically practical method](https://mattwilcox.net/web-development/keeping-srcset-and-sizes-under-control) for picking image breakpoints and authoring `srcset` and `sizes` markup a few months back; I somehow missed it. Oops! Go read it! It’s great!
- SVG savant Sara Soueidan published a great thing on [using `picture` to serve SVGs with PNG fallbacks](http://sarasoueidan.com/blog/svg-picture/).
- A bit of follow-up from last week: [Wordpress settled on a default `sizes` value](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images#51) and it’s eminently practical. That default is also [settable by theme authors](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images#30) (though they’re [still tinkering](https://github.com/ResponsiveImagesCG/newsletters/issues/154#issuecomment-75567634) with how that should work), and adjustable on an image-by-image basis via a sorta-janky/sorta-genius `data-sizes` attribute. Neat.
- The `srcset` syntax and/or `sizes` attribute [might be useful for](https://github.com/ResponsiveImagesCG/picture-element/issues/258) `video` `poster`s?
- After his [An Event Apart Atlanta talk](http://hookedoncode.com/responsive-images-are-here-now-what-by-jason-grigsby-notes-from-an-event-apart-talk/), Jason Grigsby has set about writing down a bunch of respimg implementation best practices in a series of blog posts. Here’s the [first](http://blog.cloudfour.com/responsive-images-are-here-now-what/) — an introduction, of sorts — and [here’s the second](http://blog.cloudfour.com/responsive-images-audits/), which outlines the extremely sensible, constantly-overlooked step of auditing what you have before deciding where to go, re: images on a website.
- Here are a couple of Rails respimg helpers — [`srcset` with `w`s](https://gist.github.com/mrreynolds/4fc71c8d09646567111f), [`srcset` with `x`s](https://gist.github.com/henrik/2ddcc6ab8c66e7c49305) — if you’re into that sort of thing.

See you in a couple of weeks!

—eric
