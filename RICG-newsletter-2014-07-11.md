## WebKit gets `sizes` – three cheers for Yoav

Yoav Weiss had a big week. First he [implemented](https://bugs.webkit.org/show_bug.cgi?id=133620) and [enabled](https://bugs.webkit.org/show_bug.cgi?id=134634) `sizes` in [WebKit Nightly](http://nightly.webkit.org/).

Apple being Apple, no one can say for certain what this means about *when* the feature will be landing in the iDevices and desktop Safaris of the world, but we can say this: it’s coming.

For those keeping count (me!), that’s three major rendering engines — [Blink](http://www.google.com/intl/en/chrome/browser/canary.html), [Gecko](http://nightly.mozilla.org), and now [WebKit](http://nightly.webkit.org/) – with completed `srcset` and `sizes` implementations, testable *now* and slated for stable-channel release. And we’re hearing [positive, unofficial noises](https://twitter.com/adrianba/status/486248562011799553) from the fourth!

Back to Yoav. He was just [added as a Blink core owner](https://codereview.chromium.org/374573003) – a title that comes with no little amount of power and responsibility. Yoav is one of only sixty-two out of the <!--FACTCHECK --> thousands <!--/FACTCHECK --> of Blink contributors to have the title, and the only one I see on [the list](https://github.com/mirrors/blink/blob/master/Source/core/OWNERS) with an email address not ending in Chromium, Intel, Samsung, or Opera.

While this newsletter spends a significant amount of time simply listing his accomplishments, now seems like a particularly nice time to offer Yoav our thanks and congratulations. Thanks, Yoav! And congrats!

## Responsive elements in Blink — complete `picture` implementation imminent

`picture` needs to react to changes in browsing conditions, post-load. If it didn’t, an art-directed layout  that relied on a certain image appearing at a certain breakpoint might break on window-resize.

Previously, while *JavaScripts* could listen for and react to environmental changes, there was no good way for plain old elements to do so. In a [set](https://codereview.chromium.org/348893004/) [of](https://codereview.chromium.org/337883003/) [recent](https://codereview.chromium.org/361003004/) [patches](https://codereview.chromium.org/287163010/), Google's Christian Biesinger has enabled Blink to define C++ listeners to environment changes, generally, and given `source` elements the ability to re-evaluate their `media` attributes in real time, specifically.

With that work done, `picture` can run its selection algorithm whenever one of its `source`’s senses a relevant change, and `picture` can switch out images *responsively*.

A fully-functioning `picture` implementation in Blink is right around the corner!

## Spreading the word

There isn’t too much else to report this week but I did want to mention an excellent talk on the new markup, delivered by Matt Steele to Omaha Coffee & Code. Your websites are fat!

See you in a couple of weeks!

—eric
