# Use cases in the streets, rebases in the sheets
Teaser: Client hints have landed, `picture` in Edge is official, and Yoav is bad at vacation.

## Client Hints have landed

After [months][intent-1] of [discussion][intent-2] over on blink-dev, Client Hints finally got the magical “LGTM”s and support for the DPR, Width and Viewport-Width hints has [landed in Blink][ch-landed]. If all goes well, they’ll ship in Chrome 46. 

Because he’s Yoav – the very same Yoav whose Blink username currently claims to be “Out of the Office until the 15th” – Yoav landed the commit [on shady wifi while on vacation][yoav-wifi]. As a great man once said,

“We shall land responsive image patches, whatever the cost may be. We shall commit on the beaches, we shall express our intent to implement in the [countryside][countryside], we shall read mailing lists in the fields and compile use cases in the streets, we shall spec in the hills; we shall never serve an [85.4MB website about sunglasses][omfg].”

God Save Yoav. And if you’re interested in pushing the complexity of managing multiple resources out of your markup and onto a server, grab a fresh [Canary][canary], brush up on the [spec][ch-spec] and give Client Hints a spin.

[intent-1]:  https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/vvX1vCQihDE/wg6JQg9utaMJ
[intent-2]: https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/ATbqmznya_k
[ch-landed]: https://codereview.chromium.org/1262253002/
[yoav-wifi]: https://twitter.com/yoavweiss/status/631505136075055105
[countryside]: https://twitter.com/yoavweiss/status/612883735864807424
[omfg]: http://hawksworx.com/blog/oakleys-monster-page-of-baubles/
[canary]: https://www.google.com/chrome/browser/canary.html
[ch-spec]: http://igrigorik.github.io/http-client-hints/

## `picture` is coming to Edge

It’s [official][its-happening]. No timeline yet (and their [status page][ms-status] hasn’t even been updated), but: `picture` is coming to Edge. Which makes Webkit the last of the three major rendering engines not to have made a public commitment to implementing the full respimg spec.

There are, of course, [positive signs][positive]. And Yoav’s [on][async] the [case][webkit-picture].

[its-happening]: https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/suggestions/6261271-picture-element?tracking_code=2bff73cbe7ab5df6de48a42bf23848f0
[ms-status]: http://dev.modern.ie/platform/status/pictureelement/?filter=f3e0000bf&search=picture
[positive]: https://twitter.com/grorgwork/status/616333173362786304
[async]: https://bugs.webkit.org/show_bug.cgi?id=134488
[webkit-picture]: https://bugs.webkit.org/show_bug.cgi?id=picture

## Grab bag

- The Financial Times [implemented responsive images][ft-implement] on a new responsive design that they’re cooking up and saw a 66% decrease in total bytes transferred, and a 40% improvement on their Speed Index. Not too shabby.

- Chris Coyier published an excellent thirty minute [screencast over on CSS Tricks][screencast] which walks through [a responsive images implementation][eg] using Picturefill, `w` descriptors, and `sizes` with a design breakpoint. Uniquely, Chris delves into how to actually export the resources we need from layout comps in both Sketch and Photoshop. [Excellent!][excellent]

[ft-implement]: https://twitter.com/patrickhamann/status/626414825279778817
[screencast]: https://css-tricks.com/video-screencasts/141-getting-the-images-and-numbers-for-responsive-images/
[eg]: http://codepen.io/chriscoyier/pen/QbVwYp
[excellent]: http://www.billandted.org/sounds/ea/eaexcellent.mp3]

See you in a couple of weeks!

—eric
