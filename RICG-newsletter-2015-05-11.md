
## Firefox 38 with respimg support ships *tomorrow*

It’ll support everything (`srcset`, `x`, `w`, `sizes`, `picture`, `type`, and `media`) but doesn’t respond to viewport changes — yet. Those should arrive [shortly](https://bugzilla.mozilla.org/show_bug.cgi?id=1135812#c32).

Speaking of major imminent implementation news…

## `w` and `sizes` have landed in WebKit nightlies

`srcset` and `x` descriptors have been shipping in WebKit [since  forever](https://www.webkit.org/blog/2910/improved-support-for-high-resolution-displays-with-the-srcset-image-attribute/), but support for `w` descriptors and `sizes` has been conspicuously absent. Until last week! Yoav – after [a Twitter exchange](https://twitter.com/awfulben/status/595852748375068672) with WebKit engineer Benjamin Poulain – [fixed](https://bugs.webkit.org/show_bug.cgi?id=144766) [a](https://bugs.webkit.org/show_bug.cgi?id=144640) [few](https://bugs.webkit.org/show_bug.cgi?id=144739) [bugs](https://bugs.webkit.org/show_bug.cgi?id=144675), [added a boatload of tests](https://bugs.webkit.org/show_bug.cgi?id=144674), [removed a compile time flag](https://bugs.webkit.org/show_bug.cgi?id=144679) *et voilà* – WebKit nightlies now support `sizes` and the full `srcset` syntax.

Yoav’s tests are good, but testing against real-world production-code is better, so [download WebKit Nightly](http://nightly.webkit.org/), point it to your `srcset`s, and [let Yoav know](https://twitter.com/yoavweiss) about any funny business.

Next up: `picture`! And the wait for these features to trickle down through Apple’s opaque machinery into release versions of desktop and mobile Safaris.


## Picturefill 3 [comin’](https://github.com/scottjehl/picturefill/issues/492)

It will be both faster (especially on sites with huge numbers of images and/or complex DOMs) and more furious, where by “furious” I of course mean mean “spec- and test-compliant, mimicking as much native behavior as is possible”. For example: just like Chrome, if the polyfill finds a larger image than it needs from a given `srcset` available in the cache, it’ll use that, rather than downloading an entirely new, smaller image.

Oh, and the docs page should be getting [a spiffy new re-design](https://github.com/scottjehl/picturefill/issues/495).

## Grab bag

- Want respimg in the WordPress core? [Get involved in the effort!](https://twitter.com/kadamwhite/status/596707141135695873) (more detailed instructions on joining the WordPress Slack are [here](https://make.wordpress.org/chat/).

- Dave Newton speaks! Dave Newton [will speak!](https://2015.cssconf.com/#speakers) (at the CSSConf in New York on June 18th and 19th) Dave Newton [has](https://speakerdeck.com/newtron/universal-web-design-how-to-create-an-awesome-experience-for-every-user-openwest) [spoken!](https://speakerdeck.com/newtron/improving-performance-with-responsive-and-responsible-images-openwest) (on respimg and the broader goal of a universally accessible web at the OpenWest conference in Provo, Utah)

- I penned a tiny update to my A List Apart respimg article, talking about how and why my examples no longer validate. [Don’t rely on default `sizes`](http://alistapart.com/blog/post/article-update-dont-rely-on-default-sizes/)!

- Here’s a nice little implementation experience writeup: stuff.co.nz [wrote up their struggle](https://technology.fairfaxmedia.co.nz/responsive-images-using-srcset/) with an age-old Picturefill question: whether or not to include a `src`. The prose leads me to believe that after trying to cheat fate with some ill-advised `visibility:hidden;` and `<noscript>` trickery, they came down on the side of including a `src` and risking double downloads, even though a `src` is actually missing from the last example.

- Yoav [took to his blog](http://blog.yoav.ws/long_overdue/) to summarize the last eventful, productive, and respimg-filled year and a half of his life. The best part: promises of more blogging!

See you in a couple of weeks!

—eric
