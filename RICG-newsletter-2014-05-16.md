# RICG newsletter 2014-05-16

## Implementations march on

First off, after months of work, John Schoenick [published thirteen patches for Firefox last week](https://bugzilla.mozilla.org/show_bug.cgi?id=870022#c19) which provide “basically-working” `picture`, `srcset`, and `sizes` implementations! Grab John’s “Work In Progress” builds and see for yourself [here](https://tbpl.mozilla.org/?tree=Try&rev=4a1342079d79).

Over on the Blink side of things, Yoav Weiss soldiered on, [adding `picture` support to the DOM](https://codereview.chromium.org/261823002/) and [working on preloading](https://codereview.chromium.org/265763010/). And Google developer Christian Biesinger [landed some changes](https://codereview.chromium.org/200923002/) to the basic algorithms governing image loading which pave the way for `picture`.

Christian introduced the concept of [“stable state”](http://www.whatwg.org/specs/web-apps/current-work/#await-a-stable-state). Previously, Blink would greedily load an image source as soon as it saw it; now it politely waits for processes which might switch that source out from under its nose to finish. For instance: the code Yoav is writing to pick a URL out of a `picture` element and its `source`s.

Foundational and exciting stuff!

## Spec work

Speaking of foundational and exciting stuff, work is being done to integrate picture into the HTML spec proper. WHATWG editor Ian Hickson has concerns about `picture`’s maintainability and offered to turn over responsibility for the pertinent parts of the [Living Standard](http://www.whatwg.org/specs/web-apps/current-work/) to Simon Pieters of Opera, one of `picture`’s editors. Simon accepted, and soon the Group’s [GitHub repository](https://github.com/ResponsiveImagesCG/picture-element/) will become the canonical home of the WHATWG `picture` and `img` specifications, which will be pulled from there into the WHATWG document automatically.

When we started this process we thought we’d get a responsive images solution into specifications first and browsers second. But the web, as they say, runs on rough consensus and running code. After years of work we’ve achieved both and have worked our way into the spec the other way ‘round.

## Spreading the word

Here are a few front-end-dev-centered, `picture`-related links from the past couple of weeks:

- Scott Jehl [talked about PictureFill and responsive images generally on The Big Web Show](http://www.muleradio.net/thebigwebshow/118/)
- Martin Wolf [shared his experience](http://martinwolf.org/2014/05/07/the-new-srcset-and-sizes-explained/) learning to use `srcset` and `sizes`
- Tim Kaldec [urged developers](http://timkadlec.com/2014/05/dont-wait-on-responsive-images/) to not let the perfect be the enemy of the good: use the new markup now and work to leverage other layers of the stack to make responsive images even easier, later.
- Over at Smashing Magazine, Tim Wright published an [introduction to PictureFill](http://www.smashingmagazine.com/2014/05/12/picturefill-2-0-responsive-images-and-the-perfect-polyfill/) and yours truly penned [a tour of the spec and the use-cases it was designed for](http://www.smashingmagazine.com/2014/05/14/responsive-images-done-right-guide-picture-srcset/).


## Oh and Sizer Soze is better now
If you gave [Sizer Soze](http://sizersoze.org) a spin after reading about it in the newsletter last week and found it a bit flaky, well, it’s better now. Harder better faster stronger. So go forth and measure how many bytes your non-responsive images are wasting!

See you in a couple of weeks!

—eric
