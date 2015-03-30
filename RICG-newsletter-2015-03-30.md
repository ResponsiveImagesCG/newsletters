# Mount up

**Teaser text:**
“You can't be any geek off the street / gotta be handy with the [images] if you know what I mean, earn your keep!”

## Educate, regulate

I took an unplanned sabbatical from the newsletter last week (*aka* flubbed a deadline) and it turns out that though the newsletter may stop, the news does not. Let’s dig right in.

Google and Udacity have teamed up to produce [an online responsive images course](https://www.udacity.com/course/ud882), and it is wonderful. There are videos. There are corny jokes. There is a gentle learning curve that starts with an introduction to the Chrome dev tools and ends with a fully-responsive blog that incorporates all of the myriad respimg use-cases. There are [interactive quizzes that you complete in-browser via the dev tools](http://udacity.github.io/responsive-images/examples/srcsetAndSizes/index-quiz1.html). To date 1,528 people have signed up for the course, and if you or anyone you know wants to learn respimg from the ground up, you should, too.

Perhaps reading’s your thing? Jason Grigsby has been publishing a series of blog posts titled [Responsive Images 101](http://blog.cloudfour.com/responsive-images-101-definitions/) which — in Jason’s clear, concise, and friendly style — introduce each piece of the respimg puzzle in perfectly [grok](http://en.wikipedia.org/wiki/Grok)-able chunks.

Hate videos *and* the written word? Never fear — Jason was just on [episode 99 of The Web Ahead podcast](http://thewebahead.net/99), talking through the history, use-cases, and implementation-nitty-gritty of respimg with host Jen Simmons.

Watch, read, listen, and most importantly, do. ’Tis the year of implementing respimg. Let’s!

([The Guardian](http://www.theguardian.co.uk) — with their 378 million monthly pageviews — [just did!](https://twitter.com/patrickhamann/status/577831047964028928))

## Implement, represent

[Picturefill](https://github.com/scottjehl/picturefill) was just updated to [version 2.3](https://github.com/scottjehl/picturefill/releases/tag/2.3.0). The new version adds support for more alternate file types and handles intrinsic densities the same way that the native implementations do — check out the [beta’s changelist](https://github.com/scottjehl/picturefill/releases/tag/2.3.0-beta) for more details.

[The Wordpress Respimg plugin](https://wordpress.org/plugins/ricg-responsive-images/) was [just updated](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/releases/tag/2.2.0) to use this new and improved Picturefill, and brings the plugin’s `srcset`/`sizes` markup in line with the spec.

Use Django? Use [this!](https://pypi.python.org/pypi/django-responsive-images)

How about Grunt, or ImageMagick? Dave Newton just published the slides from his [talk at the Toronto Web Performance Group](https://speakerdeck.com/newtron/using-imagemagick-to-resize-your-images-webperfto), wherein he details all of the research that went into his incredible and indispensable [Grunt-respimg plugin](https://www.npmjs.com/package/grunt-respimg). Favorite slide: [the `liquid-rescale` nightmare horror owl](https://speakerdeck.com/newtron/using-imagemagick-to-resize-your-images-webperfto?slide=37).

If you’re in Toronto and missed it, Dave will be presenting his ImageMagick talk again at the [GTA PHP User Group on April 7th](http://www.meetup.com/GTA-PHP-User-Group-Toronto/events/221364819/) and at [Full Stack Toronto on April 8th](http://www.meetup.com/full-stack-to/events/221499929/). And if you’re in Utah, he’ll be [talking about Responsive Images generally](http://www.openwest.org/schedule/#talk-22) at the OpenWest Conference in Provo on May 7th.

Speaking of slides, Yoav ran through his [legendary deck](http://yoavweiss.github.io/smashingconf_oxford/#/) at SmashingConf Oxford a couple of weeks ago. [Here are some sketchnotes](https://twitter.com/daigen/status/577816047383789568). [Moar sketchnotes](https://twitter.com/elisabethirg/status/577818850185605120)! Video soon, presumably.

And while we’re on the topic of Yoav, the off-main-thread, pre-parser-friendly CSS tokenizer that he wrote for `picture` and `sizes` has evolved into it’s final form as [the new CSS parser for all of Blink](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/r9bthijsX3A/mlJ9xc8yJCQJ). It brings an enormous 25% (!) layout-performance improvement to Blink users everywhere. I try not to trot this out very often, but: [not bad for a community group](http://w3cmemes.tumblr.com/post/23122022271).

See you in a couple of weeks!

—eric
