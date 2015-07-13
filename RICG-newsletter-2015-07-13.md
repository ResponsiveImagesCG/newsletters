# Big doin’s
**teaser text:** Big week

## Let’s “change the way we all write CSS,” forever!

Mat Marquis got the last couple of weeks off to a cracking start with [a big honkin’ <cite>A List Apart</cite> article][cq-ala] about <del>element</del> <ins>container</ins> queries.

Here’s the pitch: wouldn’t it be great if we could style elements based on their *own* sizes, rather than having to bake a bunch of facts about everything that surrounds an element into a ham-fisted, totally unportable media query in order to adaptively style it? Yes! It would! Mat turns that vague notion into a concrete example using an experimental prollyfill, explains why “element” queries died and why “container” queries succeeded them, and makes an impassioned plea to anyone out there with an interest in the future to take part in the exciting work of shaping it, by making [prollyfill-based demos][cq-demos] of their own. Concrete examples will allow us to identify and communicate use-cases, figure out if container queries are actually a viable way forward, and – if they’re not — figure out what comes next.

Mat weaves the RICG’s experiences with responsive images into the whole article; it ends on a particularly introspective note:

> ...the RICG isn’t a decision-maker in the world of web standards, and we don’t aim to be one. We want to be a rallying point—to provide ways for designers and developers who might not want to wade through arcane listservs and IRC channels to get involved in the standards that affect their daily work.

There would be a lot more to say about that, this week.

[cq-ala]: http://alistapart.com/article/container-queries-once-more-unto-the-breach
[cq-demos]: https://github.com/ResponsiveImagesCG/cq-demos

## Let’s “change how the web itself is built,” forever!

[The Web Platform Incubator Community Group][wicg] has launched. Before I can talk about what that means, some backstory:

Two years ago, a bunch of the most influential people in standards published the [Extensible Web Manifesto][ewm]. Their goal was to “tighten the feedback loop between the editors of web standards and web developers.” They argued that the best way to do this was to expose low-level HTML and CSS primitives in Javascript, which could be used to explain and extend the web’s functionality. This would allow work-a-day developers to ideate and iterate new high-level features themselves, rather than waiting for them to be spec'd, implemented, and delivered from on high.

In short they wanted things that looked a lot like [Picturefill][pf-docs], the aforementioned [container queries prollyfill][cq-demos], and the RICG.

But, [as Mat pointed out over on the Bocoup blog][bocoup] earlier this week, the experience of the RICG was not all moonlight and roses. We had a clear set of use cases, a large and vocal group of developers crying out for solutions, and a widely-used prototype. And yet clearing all of the technical and political hurdles that stood between us and a broadly implemented native solution has taken three and a half years of extraordinary effort from a tiny, core group of dedicated individuals. We fumbled forth into this brave new world of developer-driven standards, making mistakes and discovering enormous barriers to entry the whole way. Our experience cannot be the model if the goal is to move the web forward via frequent contributions from a broad spectrum of engaged folks who *also* have day jobs.

Enter the WICG. The RICG pledged to fight for the needs of the average developer; the WICG is an attempt to make the process of contributing easy enough that the average developer can be their own best advocate. If you can articulate an idea and click “I agree” on a form that says you won’t sue anybody who implements it, you can join a community of peers and experts who will support you as you seek to turn that idea into a reality.

I could go on about the details, but that’s the pitch. It’s time I stopped writing and started linking:

- The community group’s official page is [here][wicg].
- Marcos Caceres outlines the group’s mission and methods [on the W3C blog][wicg-blog].
- Yoav Weiss tells the story of his transformation from a guy who’d built WebKit once in 2008 to core Blink contributor/folk hero, and how this experience drove him to co-found the WICG [on his blog][yoav].
- Mat wrote an [excellent post][ricg-blog] over on the official RICG page, detailing the relationship between the RICG and WICG. For starters: the RICG will be shepherding all of our spec work through the WICG process from now on.

TL;DR the web wants *you*; [watch this space and *get involved*][wicg].

[wicg]: https://www.w3.org/community/wicg/
[ewm]: https://extensiblewebmanifesto.org/
[bocoup]: https://bocoup.com/weblog/extensible-web-manifesto/
[wicg-blog]: http://www.w3.org/blog/2015/07/wicg/
[yoav]: http://blog.yoav.ws/by_the_people/
[ricg-blog]: https://www.w3.org/community/respimg/2015/07/09/wicg/

## Grab bag

- [Picturefill 3 is in beta][pf-3b]. You’d think we’d be in the “refinement and bug fixing” part of the product cycle by now, but no, v3 is a near-complete-rewrite which brings heretofore-unthinkable levels of compatibility with native implementations and a performance boost, too. And! New, beautiful, comprehensive [documentation][pf-docs].
- It’s official: [`w` descriptor and `sizes` support are “in development” in Microsoft Edge][edge].
- Need 2x resources but don’t have 2x originals? Give this magical [upscaler][upscaler] a shot. It was made for “anime/fan” art but (in *very* limited testing) I actually had a lot of success with anything graphic (rather than photographic).
- We’ve done stickers, hoodies, and tees. [Rugs][rugs] are the final frontier of community group swag.

[pf-3b]: https://github.com/scottjehl/picturefill/releases/tag/3.0.0-beta1
[pf-docs]: https://scottjehl.github.io/picturefill
[edge]: https://github.com/MicrosoftEdge/Status/pull/241
[upscaler]: http://waifu2x.udp.jp
[rugs]: https://twitter.com/derSchepp/status/617284417107705856


See you in a couple of weeks!

—eric
