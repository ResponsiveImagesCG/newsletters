# Optimizing for Truth

**Teaser:** The RICG meets, greets, and files a bunch of panicky test-fail issues with browser vendors.

## Meeting!

RICG members and representatives from the IE, Firefox, and Chrome teams met in Redmond last Thursday to talk about where the RICG is and where we’re all headed. The meeting was *action-packed*. I’m hoping that some of the folks who were in attendance will be able to write up recaps, but here are the things that stuck out to me from [the minutes](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T116903):

- Microsoft is planning on implementing the [full suite](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T116908) of respimg features.
- `img` [will be getting](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T116931) a readable/writeable DPR property, accessible via JavaScript.
- The venerable [respimg use-cases doc](http://usecases.responsiveimages.org) will be seeing some new [use](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T116958)-[cases](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T117039) soon.
- Tab Atkins is preparing a concrete, workable Element Queries spec [to submit to The Group](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T117125).
- Client hints are a much bigger deal than I’d previously understood them to be, and will provide [a general architecture](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T117300) for [intelligently-managed](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T117349), [opt-in](http://ircbot.responsiveimages.org/bot/log/respimg/2015-03-05#T117380) content negotiation. Yoav’s [just-landed](https://codereview.chromium.org/951303003/) implementation of the DPR, Content-DPR, and Resource Width hints in Chrome is just the first step.
- Yoav and Ilya are also working to implement a bunch of standard ways that developers can use `link`/headers to suggest that browsers do work head of time: [preconnect](https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/CM5BaP6uVvE), [preload](http://w3c.github.io/preload/), and prefetch/pre-render aka [Resource Hints](http://w3c.github.io/resource-hints/).

Phew!

## Gecko issues

Last newsletter, I [jubilantly celebrated](http://us8.campaign-archive2.com/?u=c988d9ca55d5d09e73a7dc993&id=5efd23c152&e=4db00bcdc4) the prefing-on of respimg features in Firefox Nightly, which paved the way for the features to be pushed out to millions of Firefox stable users in May. Subsequently, it was discovered that the pref-ed on implementation [failed](https://bugzilla.mozilla.org/show_bug.cgi?id=1139554) a [boatload](https://bugzilla.mozilla.org/show_bug.cgi?id=1017878) of [tests](https://bugzilla.mozilla.org/show_bug.cgi?id=1139560). A freakout ensued, but I’m happy to report a happy ending — original Gecko respimg developer John Schoenick was cajoled out of Mozilla-retirement for one last job and saved the day, identifying and fixing a handful of root parser incompatibilities.

Phew!

## Grab Bag

- Remember the microtasks Yoav was implementing in WebKit last newsletter? They’ve  [landed!](https://bugs.webkit.org/show_bug.cgi?id=137496) Action now moves to [the async image loading issue](https://bugs.webkit.org/show_bug.cgi?id=134488).
- Dave Newton published [an all-in-one Grunt respimg plugin](https://www.npmjs.com/package/grunt-respimg
) which’ll take an input image and spit out well-optimized, multiple-resolution, multiple-format versions of it, ready for inclusion in markup. The plugin packages up all of the [exhaustive research](https://github.com/nwtn/image-resize-tests) that Dave has been doing into ImageMagick settings into a Grunt-based easy button.
- Tim Evko [penned a wonderful article](http://www.smashingmagazine.com/2015/02/24/ricg-responsive-images-for-wordpress/
) over on Smashing Magazine which details the hows and whys of the Wordpress respimg plugin.
- Bruce Lawson — `picture`’s [fairy godmother](http://www.brucelawson.co.uk/2011/notes-on-adaptive-images-yet-again/) — gave what appears to have been [an excellent, whimsical, and informative respimg talk](http://brucelawson.github.io/talks/2015/awwwards/
) at the Awwwards conference in Barcelona.
- Jason Grigsby [went deep on responsive hero images](http://blog.cloudfour.com/responsive-hero-images/
) over on the Cloud Four blog, using them as a window into a much large discussion about designing with/for constraints in order to deliver useful, simple, and thoughtful design *systems* to clients. Choose your breakpoints based on where it breaks — this is as true for images and art direction as it is for layouts.

See you in a couple of weeks!

—eric
