# Finishing touches & new foundations

**Teaser text:** `picture` in Safari is imminent, cool tools, and a container query status update

A long time ago, in a newsletter far, far away*, I reported that `picture` would be shipping in Safaris in “the fall.” Good news everybody! Apple decided to do a webdev-focused Safari point release, and [the headlining feature](https://developer.apple.com/library/prerelease/mac/releasenotes/General/WhatsNewInSafari/Articles/Safari_9_1.html) is `picture`! On desktops, 9.1 should land in OS 10.11.4 (any day now?); with any luck iOS won’t be too far behind.

*Caveat implementor*: Apple’s implementation still suffers from some fairly severe bugs. Two biggies: 1) double downloads [sometimes](http://jsbin.com/fikizogapu/1/edit?html,output), 2) it doesn’t respond to viewport changes.

## Hey! What’s up with container queries?

Tab “The Catalyst” Atkins Jr., who outlined a technical plan for how [container queries](http://alistapart.com/article/container-queries-once-more-unto-the-breach) could work at the RICG meeting a year ago in Redmond, [provided a status update in the RICG IRC](http://ircbot.responsiveimages.org/bot/log/respimg/2016-02-08#T158122). TL;DR: he wants to see this feature evolve from the ground up, rather decreeing it from the top, down. [Extensible-Web-Manifesto](https://extensiblewebmanifesto.org)-style.

So:

1. Give authors the tools to create their *own* solutions. Namely: element-level resize events, custom CSS @-rules, and (maybe) an explicit way to break out of some of the thorny [circular-dependency issues](http://www.xanthir.com/b4VG0).
2. Nudge authors to create (JavaScript-dependent) libraries and see if any of them gain traction and mature.
3. If/when a given solution wins sufficient hearts/minds and achieves a degree of maturity: pull it into the platform; make it native.

To me, this sounds more or less like the path we (eventually) took to get from `picturefill.js` to `<picture>`. (Frustratingly) slow, (reassuringly) steady, and (happily) democratic. While we wait for various foundations to be laid, I say we all spend some time thinking about how to implement CQs as a *progressive enhancement*?

For the impatient: nitty-gritty discussions (and [specifications](https://drafts.csswg.org/css-containment-3/#containment-layout)!) about those pesky circularity issues have been [kicking up again recently](https://github.com/ResponsiveImagesCG/container-queries/issues/3#issuecomment-169471593). Read up and chime in!

## Managing complexity

Efforts continue on all fronts to make the creation, management, and delivery of responsive images as easy as possible.

The coolest tool released during the newsletter’s long haitus: Cloudinary’s [responsive images breakpoint generator](http://www.responsivebreakpoints.com). A living, breathing, (and free!) answer to [Jason Grigsby’s koan](http://blog.cloudfour.com/responsive-images-101-part-9-image-breakpoints/): how many differently-sized versions of a given image do we really need, and exactly what should their resolutions be?

It seems like I’ve mentioned this in every newsletter for the last six months, but – responsive images landing in WordPress 4.4 Core was a Big Flippin’ Deal, and has made respimg deployment completely automatic for *millions* of sites. Tim Evko wrote up [a great explainer of how the implementation actually works on SmashingMag](http://www.smashingmagazine.com/2015/12/responsive-images-in-wordpress-core/).

Speaking of great explainers on SmashingMag, Jon Arne Sæterås penned [a great intro to Client Hints](https://www.smashingmagazine.com/2016/01/leaner-responsive-images-client-hints/). If you want to do more respimg heavy lifting on your server and in HTTP headers and less in markup, Client Hints are the ticket.

Finally, I wrote a little thing on the Cloudinary blog about how to use their smart-cropping features for [automatic art direction](http://cloudinary.com/blog/automatically_art_directed_responsive_images).

# Grab bag

- The excellent and under-appreciated spec intro for respimg features [now sports a few snazzy (and helpful!) illustrations](https://html.spec.whatwg.org/multipage/embedded-content.html#introduction-3), courtesy of editor Simon “Non-Normative” Pieters.
- While most of us are only just now dipping our toes into generating WebPs and JPEG-XRs, the *next* next generation of image formats continues to take shape. The FILF folks [wrote a few words](http://flif.info/lossy.html) about using their (lossless-focused) codec lossilly, and the Daala crew (whose in-development video codec [includes an innovative still image coder](https://people.xiph.org/~xiphmont/demo/daala/update1.shtml)) is getting [awfully close](https://arewecompressedyet.com/?r%5B%5D=x265_1.6_ntt-short-1&r%5B%5D=master-2016-03-16-20af6e2&s=ntt-short-1) to their stated goal of outperforming the royalty-encumbered, [world-beating](https://people.mozilla.org/~josh/lossy_compressed_image_study_july_2014/#y-ssim-data) HEVC/H.265.
- Expect the unexpected and [style your broken images](http://bitsofco.de/styling-broken-images/).

See you in a couple weeks!
—eric

\* Sorry, by the way, for the extended haitus. Turns out: quitting your job, leaving the country for three weeks, and then moving from the Mile-High City to a cabin by the sea is fairly disruptive, re: timely newslettering.

