# Any day now

Teaser text: Chrome 38 is nigh, we have links galore and also Shakespeare for some reason.

Chrome 38 — the first browser to support native responsive image markup – is due to be pushed out to the stable channel’s [hundreds of millions of users](http://techcrunch.com/2013/05/15/googles-chrome-browser-now-has-750-million-active-users/) any day now. 

[Google’s](https://www.youtube.com/watch?v=QINlm3vjnaY) [excited](https://www.youtube.com/watch?v=Pzc5Dly_jEM).

While we wait, let’s recap a *bumper-crop* of responsive image chatter from the past couple of weeks:

> To `picture`, or not to `picture`– that is the question:

Jason Grigsby and Chris Coyier wrote a pair of [excellent](http://blog.cloudfour.com/dont-use-picture-most-of-the-time/) [articles](http://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/) that hammer home the distinction between the resolution-switching and art-direction use cases; `picture` is best reserved for the latter. When you’re not art-directing, use `srcset`!

Chris gives the friendliest technical explanation of how browsers actually use `srcset`, `sizes`, and `w` to pick a source that I’ve yet seen.

And Jason asks: why do we call it “the `picture` spec”, anyways? Maybe we shouldn’t!

> Whether tis nobler in the mind to polyfill<br />
> The `srcset`s and `sizes`, outrageously awesome

Meanwhile, over on the Filament Group blog, Scott Jehl (Picturefill author) [takes a hard look at some very hard questions](http://filamentgroup.com/lab/to-picturefill.html): why polyfill, ever? What are the benefits and what are the costs? Given the new markup’s native fallbacks, why polyfill responsive images, specifically? It’s a very thoughtful take; he comes out on the side of Picturefilling, for now.

Scott’s post came out of a discussion of whether or not to include Picturefill in Drupal 8. Drupal’s developers are blazing all kinds of trails as [they work furiously to implement the new markup](https://github.com/ResponsiveImagesCG/newsletters/issues/62). Watching them [hash out a responsive images CMS UI](https://www.drupal.org/node/2334387) has been particularly fascinating.

> Or to take arms against a sea of implementers<br />
> and by dymanic [sic] attacks, oppose them. To DIY— feature creep—

[“Thing is, canvas is PERFECT.”](https://miketaylr.com/posts/2014/09/picture-element-spec-hidden-logs.html)

> No more; and by a speech or two we end<br />
> The headache, and deliver a thousand natural talks<br />
> That flesh out how-to.

The videos from Yoav’s [responsive images](https://www.youtube.com/watch?v=GC3VgcltKKI) and [preloader](https://www.youtube.com/watch?v=i7yf_tR6kKc) talks at Velocity are up. And if the topic of preloaders fascinates (or befuddles), [Andy Davies slides from London Webstandards](http://www.slideshare.net/AndyDavies/london-web-standards-20140922-pdf) are worth a look.

Dave Newton gave a great respimg talk at Accessibility Camp Toronto; his slides are [here](https://speakerdeck.com/newtron/using-responsive-images-responsibly-performance-and-accessibility) and [here](https://github.com/nwtn/pres-respimg-perf-a11yto). The Venn diagram explaining how responsive design, performance, accessibility, and progressive enhancement are all distinct, complimentary pieces of a strategy that reaches as many people as possible is a favorite.

And last but not least, RICG Chair Mat Marquis [gave a talk at An Event Apart Austin](http://www.lukew.com/ff/entry.asp?1922) and [only threatened the audience with violence once](https://twitter.com/projekt202/status/514446031954534400).

> Tis an implementation<br />
> Devoutly to be wish’d.

I’ll say it: Microsoft is embracing an open stance towards the open web. First the Internet Explorer team [let us know what they’re working on](https://status.modern.ie); now they’ve taken things to another level entirely and are [letting us *vote* on new features](https://wpdev.uservoice.com/forums/257854-internet-explorer-platform). I think you know what to do:

- [srcset](https://wpdev.uservoice.com/forums/257854-internet-explorer-platform/suggestions/6261267-srcset-attribute-on-images)
- [picture](https://wpdev.uservoice.com/forums/257854-internet-explorer-platform/suggestions/6261271-picture-element)

Those two are currently trailing Service Workers, the Shadow DOM, auto-update, and two different suggestions that IE’s rendering engine be abandoned entirely. Old IE-hating habits die hard!

> To code— to commit. <br />
> To commit— perchance to deploy: ay, there's the rub!

Lastly, I want to point you to [Brent Lineberry’s recap](http://writings.orangegnome.com/writes/implementing-responsive-images-in-a-production-environment/) of his team’s responsive image implementation on Emory’s [Goizueta Business School site](http://goizueta.emory.edu/). The website in question is large and complex; first-hand accounts of the rubber meeting the road like this are *invaluable*. I expect to read a lot more of them in the coming months as the dev community as a whole figures out how to best leverage the new features.

See you in a couple of weeks!

—eric
