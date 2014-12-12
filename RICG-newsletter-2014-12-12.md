# Walking and talking

**Teaser text:** `<!--[if IE]><img src="http://bukk.it/thumbsup.gif" /><![endif]-->`

## IE walks the walk

[Internet Explorer is implementing `srcset` with `x` descriptors](http://blogs.msdn.com/b/ie/archive/2014/12/08/status-roadmap-update-srcset-lt-main-gt-element-and-date-inputs-in-development.aspx).

This is *huge* news; it means that `x` descriptors have or will soon come to [every major browser](http://caniuse.com/#feat=srcset).

`w` descriptors, `sizes`, `picture`, and all of the rest are still officially “under consideration” (and not “in development”), but [from the looks of it](https://twitter.com/gregwhitworth/status/542075784014204929) this represents a firmly planted first step on the path towards a full respimg implementation in IE.

(And it certainly doesn’t hurt the RICG’s unofficial [1% in 2014 campaign](https://twitter.com/zcorpan/status/542048849641340931).)

## RICG members talk at talks

[Here’s](http://www.ami.ca/AMI-tv/Pages/AMI-Inside.aspx) a video recap of [Dave Newton’s September talk](https://speakerdeck.com/newtron/using-responsive-images-responsibly-performance-and-accessibility) at Accessibility Camp Toronto. Respimg discussions start at the eight minute mark; Newtron takes center stage from 9:22–16:50. The talk and the interview are great, and hey! Nice shirt!

And apparently Yoav brought the house down at [SmashingConf Whistler this past week](http://smashingconf.com/speakers/yoav-weiss). “Responsive images are <del>coming</del> here!” Yoav’s slides are [here](http://yoavweiss.github.io/smashingconf_whistler/#/).

## Etcetera

I was pleasantly surprised by the comments on my recent [A List Apart respimg article](http://alistapart.com/article/responsive-images-in-practice). I’d braced myself for a lot of criticism and complaint, but almost every comment concerned *implementing* and *automating* all of this new markup. Myriad dev environments and CMSes are going to require myriad tutorials and implementation recaps; Aaron Gustafson has written a great one about his recent experiences [implementing respimg with ExpressionEngine](http://aaron-gustafson.com/notebook/2014/adaptive-images-in-expressionengine-with-ce-image/) on the [Nichols College site](http://www.nichols.edu/).

Ian Devlin did some walking *and* talking this week, on the subject of [providing multiple, alternate captions for art-directed images](http://www.iandevlin.com/blog/2014/12/html5/defining-multiple-captions-and-alt-text-for-responsive-images). Personally I’m a bit ambivalent about this, but Ian’s article (and [ polyfill](https://github.com/iandevlin/picturecaption)!) make a strong case.

Finally, element query talk is still rumbling along. [Minutes from a recent RICG conference call](https://docs.google.com/document/d/1NlJslYLNkmm42EYAXSiA94PIq7t4Bo7EiUA6t2tj7ps/mobilebasic?pli=1) indicate that there is some consensus within the group on how to deal with the feature’s inherent [circular dependency issues](http://www.xanthir.com/b4VG0), and that Tab is getting ready to start a syntax discussion thread on [www-style](http://lists.w3.org/Archives/Public/www-style/). That should be fun.

See you in a couple of weeks!

—eric
