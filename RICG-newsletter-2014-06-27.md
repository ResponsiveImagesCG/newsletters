# Spec’d!

<header><small>
`picture` has landed in the W3C and WHATWG HTML specifications; validators and best-practice guides have been updated with the new markup; implementations march on.
</small></header>

## Spec’d…

The `picture` spec has landed in both the WHATWG and W3C specs.

- [WHATWG `picture`](http://www.whatwg.org/specs/web-apps/current-work/multipage/edits.html#the-picture-element)
- [WHATWG `srcset`](http://www.whatwg.org/specs/web-apps/current-work/multipage/edits.html#attr-img-srcset)
- [WHATWG `sizes`](http://www.whatwg.org/specs/web-apps/current-work/multipage/edits.html#attr-img-sizes)
- [W3C `picture`](http://www.w3.org/html/wg/drafts/html/master/embedded-content.html#the-picture-element)
- [W3C `srcset`](http://www.w3.org/html/wg/drafts/html/master/embedded-content.html#attr-img-srcset)
- [W3C `sizes`](http://www.w3.org/html/wg/drafts/html/master/embedded-content.html#attr-img-sizes)

Simon Pieters, [hero](https://twitter.com/zcorpan/status/478960023234945024), took on responsibility for all of the image-related bits of the WHATWG spec in order to make this happen. Simon included a nice, “non-normative” (aka “informal” also known as “readable”) [introduction to the new markup](http://www.whatwg.org/specs/web-apps/current-work/multipage/edits.html#introduction-0) along with all of the technical bits.

And, hey! Look who popped into the W3C HTML spec’s [list of editors](http://www.w3.org/html/wg/drafts/html/master/Overview.html#specification-editors)!

Not bad for a [Community Group](http://w3cmemes.tumblr.com/post/23122022271).

## …correct…

Mike Smith, who maintains the [W3C HTML Validator](http://validator.w3.org/nu/) is [adding](https://github.com/validator/syntax/commits/picture) `picture` spec support; it should land within a [fortnight](http://ircbot.responsiveimages.org/bot/log/respimg/2014-06-26#T79559). The under-development `picture` branch is up and running [here](http://qa-dev.w3.org:8888/), armed with [boatloatds of useful error messages](https://gist.github.com/sideshowbarker/8284404#file-messages-json) – go test your code!

[Can I Use](http://caniuse.com/) has begun tracking [`picture` support](http://caniuse.com/picture).

And Google’s new and wonderful [Web Fundamentals](https://developers.google.com/web/fundamentals/) guide now features the new markup in its [section on content images](https://developers.google.com/web/fundamentals/media/images/images-in-markup).

## …and in effect

Firefox Nightly has included `srcset` and `sizes` support for a few weeks – yesterday, John Schoenick (hero) [landed `picture` support](http://bugzil.la/picture), too. It’s currently disabled by default (behind the `dom.image.picture` flag), but that should [change](http://bugzil.la/picture-prefon) [soon](http://bugzil.la/srcset-prefon). John is still aiming for on-by-default support in Firefox 33 (which, [you may recall](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2014-06-13.md#three-browsers-by-halloween), ships on October 14th!).

Over on the Blink side of things, Yoav Weiss (who is *definitely* a hero) took `sizes` and `w` descriptors [out from behind their Experimental flag](https://codereview.chromium.org/356833007/). Meaning that the features are on-by-default in [Canary](http://www.google.com/intl/en/chrome/browser/canary.html) *now*, and will almost certainly be enabled for millions of Chrome users when version 38 ships on September 26th.

Heros, all of you.

See you in a couple of weeks!

—eric
