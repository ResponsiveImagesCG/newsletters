# LGTM

## Three browsers by Halloween

[Firefox Nightly](http://nightly.mozilla.org/) now includes `srcset` and `x`-descriptor support behind a flag – instructions on how to enable and test the feature are [here](http://codepen.io/RICG/pen/poKfj). The feature should be on-by-default [shortly](https://bugzilla.mozilla.org/show_bug.cgi?id=1018389) and `sizes`, `w` descriptors, and `picture` support are [right around the corner](https://bugzilla.mozilla.org/show_bug.cgi?id=picture). Nothing is certian, but if things keep progressing apace, full `picture` spec support should be shipping on-by-default in FireFox 33 on October 14th.

Over on the Blink side of things, `srcset` and `sizes` received [the three magical “LGTM”s](https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/GRfwz951FHo
) they needed to come out from behind their experimental feature flag and should be on-by-default in M38 — shipping in Chrome 38 stable on September 26th and Opera 25 around the same time.

## Webkit’s not *too* far behind

Yoav has successfully wrangled the existing WebKit `srcset` implementation into shape, [aligning it with the spec](https://bugs.webkit.org/show_bug.cgi?id=133504) and setting the stage for [`sizes` support](https://bugs.webkit.org/show_bug.cgi?id=133620).

[Rumor has it](https://twitter.com/helloanselm/status/473719818756317184) that iOS 8 even supports `x` descriptors in `srcset`. Baby steps!

## In the meantime, Picturefill...

PictureFill 2.1, which brings `srcset` parsing in-line with the spec, hit [beta](https://github.com/scottjehl/picturefill/releases/tag/2.1.0-beta).

If you haven’t given Picturefill a go yet, you really should code like it’s 2015 and give it a whirl. If you *are* using it, [let them know](https://github.com/scottjehl/picturefill/issues/258)!

## ...and boatloads of blog posts!

- [Chris Coyier wrote and video’d](http://css-tricks.com/video-screencasts/133-figuring-responsive-images/) his initial experiences with the new markup over on CSS Tricks
- Tracy Rotton posted [a great tutorial on how to use Picturefill in WordPress](http://www.taupecat.com/2014/05/picturefill-js-wordpress/)
- Matt Wilcox [wrote up his initial (cautious) thoughts](https://mattwilcox.net/archives/a-picture-perfect-problem/) ([Yoav’s response](https://github.com/ResponsiveImagesCG/newsletters/issues/17#issuecomment-43977530))
- Derek Johnson provided a [great, complete overview](http://nostrongbeliefs.com/responsive-images/) of the spec
- Mat Marquis [took to the A List Apart blog](http://alistapart.com/blog/post/testing-responsive-images), calling all interested parties to help test the in-progress implementations.
- Speaking of things Apart, the Monkey Do folks [wrote up their experience deploying Picturefill on the An Event Apart page](http://monkeydo.biz/blog/an-event-apart-and-the-picture-element) (and [I nitpicked thier post](https://github.com/ResponsiveImagesCG/newsletters/issues/22#issue-34792503))
- Martin Wolf [screencasted](http://martinwolf.org/2014/06/05/screencast-native-picture-element-implementation-in-chrome-canary/) his experience kicking the Canary tires.

## And hey! Weren’t those [t-shirts](https://dribbble.com/shots/1471972-Responsive-Images-Community-Group-IndieGogo-Campaign) great?

I got mine in the mail last week and I just want to say that they’re really terrific. Thanks again to [Geri Coady](http://www.hellogeri.com/) for the design, [United Pixelworkers](http://www.unitedpixelworkers.com/) for the printing, and RICG chair [Mat Marquis](https://twitter.com/wilto) for running logistics. And thanks most of all to all of you for buying them and [making Yoav’s tireless implementation work possible](https://www.indiegogo.com/projects/picture-element-implementation-in-blink)!

We’ve been getting a lot of questions about how to buy the shirts now that the campaign is over. We don’t have anything firm to report yet but we’re looking into our re-print options. If you missed the boat on these, keep an eye out!

See you in a couple of weeks!

—eric
