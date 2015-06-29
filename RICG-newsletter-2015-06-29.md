# Diving into the weeds

I’ve been highlighting Jason Grigsby’s superb <cite>[Responsive Images 101](http://blog.cloudfour.com/responsive-images-101-definitions/)</cite> posts for weeks. They’re a series clear, concise posts which neatly break the new respimg features down into their component conceptual parts.

I want to lead this week with the *opposite* of that: [<cite>When Responsive Images Get Ugly</cite>, by Taylor Hunt](http://codepen.io/Tigt/blog/when-responsive-images-get-ugly). If Jason’s posts are the 101 course, this is a graduate seminar. Big, messy, in-depth, and exploratory.

The post gets into the *weeds*. Topics include: using picture to supply an `x`-descriptor fallback `srcset` to a preferred `w`-descriptor `srcset`; dealing with the lack of `h` descriptors when marking-up height-constrained images; and stuffing respimgs into inline SVGs (!?). But my favorite part is [the bit about the heretofore untapped power of the `media` attribute](http://codepen.io/Tigt/blog/when-responsive-images-get-ugly#media-aware-images). We generally think of the new responsive features as ways to adapt images to different screen sizes, pixel densities, and maybe network speeds. But media queries allow us to do much more, marking up images which tailor themselves to all sorts of contexts. One small example: replacing animated gifs with still images on e-readers and other devices whose `media="(update-frequency: slow)"`. A good and eye-opening article.

## Client hints lurch forth

After submitting [a patch implementing Content-DPR header support](https://bugs.webkit.org/show_bug.cgi?id=145380) to Webkit last month, only to see [discussions around it stall](https://lists.webkit.org/pipermail/webkit-dev/2015-May/027474.html), Yoav posted an [Intent to Ship client hints thread](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/vvX1vCQihDE/wg6JQg9utaMJ) to Blink-dev a couple of weeks ago… only to see discussions around it stall. Good thing we’re nothing if not persistent.

## Compress, automate, deliver

Yoav and a few of his Akamai chums are getting together to write a book! Based on [Guy Podjarny’s overview](https://medium.com/@guypod/high-performance-images-beautiful-shouldn-t-mean-slow-22ffc4e31663), <cite>High Performance Images</cite> will be a book-length treatment from some of the smartest minds in the business about optimal compression, delivery, and backend automation strategies.

Dave Newton just published a stellar article [explaining his optimal ImageMagick resizing/compression settings,](http://www.smashingmagazine.com/2015/06/25/efficient-image-resizing-with-imagemagick/) which concludes with links to a bunch of immediately-implementable tools for bash, Node, PHP, and Grunt. Explanatory, [actionable](https://twitter.com/brandonkelly/status/614765799782223872), excellent.

## We speak

- Speaking of Dave, he just spoke about <cite>Improving Performance With Responsive (And Responsible!) Images</cite> [at CSS Conf](https://2015.cssconf.com/#videos).

- And Jason Grigsby flew across the Atlantic to answer the question, <cite>Why Responsive Images</cite> at the final [Responsive Day Out](http://responsiveconf.com/2015/) in Brighton, England. [Notes](https://decadecity.net/blog/2015/06/19/jason-grigsby-responsive-images-have-landed) / [slides](https://speakerdeck.com/grigs/why-responsive-images) / [audio](https://huffduffer.com/adactio/243771).

## A bummer, a book, and a correction

- Firefox’s shipping respimg implentation might not respond to viewport changes [until September](https://bugzilla.mozilla.org/show_bug.cgi?id=1135812#c62). But never fear: [Picturefill’s got your back](https://twitter.com/respimg/status/614514633890791424).

- Five Simple Steps have just released [<cite>Practical Responsive Images</cite>, by Ben Seymour](http://www.fivesimplesteps.com/products/practical-responsive-images). I haven’t had a chance to check it out yet but it looks good!

- In the last newsletter I mentioned “a nifty little library that uses CSS gradients as image placeholders”. And forgot to add the link, which is:
[http://gradifycss.com/](http://gradifycss.com/). Oops!

See you in a couple of weeks!

—eric
