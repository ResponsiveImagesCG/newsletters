# Taking stock

**Teaser text:** ’Twas two weeks after Christmas...


I signed the [last newsletter](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2014-12-12.md) “see you in a couple of weeks!” ... four weeks ago. Oops! Food, friends, festivities, and family happened, and I happily dropped off of the face of the internet for a month. After catching up on the logs, lists and repos, it seems I wasn’t the only one. The RICG as a whole seems to have collectively settled our brains for a long winter’s nap. As we re-start our engines, now seems like an excellent time to take stock of where the RICG is, and what we’re hoping to achieve in the new year.


## Browser implementations

Respimg features are under active development in every major rendering engine.

Blink is the only engine with a full, shipping, implementation of the spec. Blink supports `srcset` with both `w` and `x` descriptors, `picture`, `source media` *and* `source type`. This is not to say that Blink’s implementation is done, of course; Yoav (so lively and quick) [continues to polish](https://codereview.chromium.org/839783002/); I expect Blink’s `srcset` picking-process, especially, to get more sophisticated over the coming year, perhaps incorporating user preferences and/or bandwidth-awareness.

A full respimg implementation should be landing in Gecko soon, but after point-man John Schoenick left Mozilla for a position at Valve back in November, progress has slowed. John [isn’t yet sure](http://ircbot.responsiveimages.org/bot/log/respimg/2015-01-08#T107603) whether he’ll complete the implementation himself or hand it off to someone else; either way, the lion’s share of the work has been done, so hopefully this lands soon.

Webkit currently supports `srcset` with `x` descriptors, and Yoav is [laying](https://bugs.webkit.org/show_bug.cgi?id=137496) the [foundations](https://bugs.webkit.org/show_bug.cgi?id=134488) for a full implementation. He’s doing what he can, but patch review times have been lengthy and communication from the core WebKit team seems a bit sporadic.

Finally, [the IE team announced in December](http://blogs.msdn.com/b/ie/archive/2014/12/08/status-roadmap-update-srcset-lt-main-gt-element-and-date-inputs-in-development.aspx) that they’re actively implementing `srcset` with `x` descriptors. Better yet, they continue to wink their eyes and twist their heads re: the rest of the spec’s features (which are officially still “under consideration”) in ways that give me to know we have nothing to dread.


## Picturefill development

How to deal with all of these incomplete and in-development implementations, in the meantime? With [Picturefill](https://github.com/scottjehl/picturefill) of course! I can’t say anything about the state of the Picturefill better than [Mat did here](https://github.com/scottjehl/picturefill/issues/374) — version 2.2 provides a great polyfill that thousands of developers are relying on each and every day, but to achieve total spec compliance and optimal performance, there’s work to be done.


## Developer evangelism

The RICG continues to [make](https://twitter.com/jeremiahjmartin/status/542775285049876480) a [lot](http://aneventapart.com/event/atlanta-2015) of [clatter](http://www.futureinsights.com/home/responsive-images-are-here-its-up-to-you-to-make-the-web-for.html) about what is the matter with non-responsive images.

And it is working. I’m addicted to checking the [Chromestatus](https://www.chromestatus.com/metrics/feature/timeline/popularity/523) [usage](https://www.chromestatus.com/metrics/feature/timeline/popularity/524) [charts](https://www.chromestatus.com/metrics/feature/timeline/popularity/521), watching them go up and up. It’s uniquely gratifying to see the RICG’s work reverberate across the web in real time.

Getting respimg baked into as many CMSes as possible will probably do more than anything to push those numbers up. [Drupal](https://www.drupal.org/node/2260061) and [Wordpress](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images) are in our sights.

## Spec work

The CSS [`image-set()` spec](http://dev.w3.org/csswg/css-images-3/#image-set-notation) is but a skeleton, full of red issue boxes *aka* holes.

And, though the respimg-in-markup spec has largely settled down, there are a few [on-hold issues](https://github.com/ResponsiveImagesCG/picture-element/labels/onhold) in the repo that constitute a roadmap for future development. Once the first round of implementations stabilizes, expect more descriptors to be added to `srcset`: `h`, `type()`, and maybe `integrity()`.


## Element queries

Everything I’ve spoken of so far is mop-up. The biggest thing on the RICG’s plate in 2015 isn’t related to responsive images at all. It’s Element Queries. EQs are currently just a vision, dancing in our heads. If we’re going to make them concrete in 2015, we’re going to need all of the help we can get. Perhaps you, good webizen, have made some sort of resolution recently to become more involved in web standards, to contribute to your professional community, or to undertake more ambitious, challenging, and meaningful work? Contribute!

- Use [an experimental prollyfill](https://github.com/jonathantneal/hitch-element-queries) to get a feel for what sorts of problems Element Queries are good at solving.
- Help us codify those use cases in [a document that will guide all future work](https://github.com/ResponsiveImagesCG/eq-usecases).
- Publish neat demos in our currently-empty [demo repo](https://github.com/ResponsiveImagesCG/eq-demos).
- Or just bring your EQ questions, concerns, hopes, and dreams to the RICG [mailing list](http://lists.w3.org/Archives/Public/public-respimg/), [IRC channel](http://ircbot.responsiveimages.org/), or the [Use Cases GitHub repo](https://github.com/ResponsiveImagesCG/eq-usecases/issues).

<blockquote>
It’s 2015 and Responsive <em>Issues</em> are our game,<br />
So let me whistle and shout, and call you by name:<br />
On implementor, on spec editor, on randos and friends,<br />
On developers writing CSS, HTML, and, uh, code with parens?<br />
To the top of the porch! To the top of the wall!<br />
Let us make modular components that adapt based on their layout size a reality for all!
</blockquote>

See you in a couple of weeks! (for reals this time)

—eric
