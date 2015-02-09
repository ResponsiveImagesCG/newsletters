# The Hard Part

**Teaser text:** “Now we’ve got the tools. How do we use them?”

I'm going to open with a quote from Jason Grigsby, from his recent appearance on [the UIE Brain Sparks podcast](http://www.uie.com/brainsparks/2015/02/02/jason-grigsby-real-world-responsive-web-design/):

> I think even though responsive images is something that we’ve been talking about for quite some time, that really 2015 is going to be the year that web developers as a whole now are going to be, “Now we’ve got the tools. How do we use them?”

The RICG researched use cases, labeled them “responsive images,” built consensus around a solution, spec’d that solution, and implemented it in browsers. Now comes the hard part: how do we, both as individual developers working on individual projects, and as evangelists looking to respimg-ify the web as a whole, get responsive images into *webpages*?

## Trailblazers

Ethan Marcotte’s [@RWD Twitter account](https://twitter.com/rwd) asked for examples of respimg in action and [a few of his 112K followers obliged](https://twitter.com/RWD/status/560114266137985026). The replies contain a [wealth](http://www.shopify.com) of [real](http://cooking.nytimes.com/guides/how-to-make-pie-crust)-[world](https://twitter.com/ResWebDes/status/564198907341975552) [examples](http://commonreader.wustl.edu/).

A bit of “view source” shows a boatload of `picturefill`, a smattering of `picture`, mostly `x` descriptors, and nary a `w` descriptor in sight. [The](https://www.chromestatus.com/metrics/feature/timeline/popularity/524) [numbers](https://www.chromestatus.com/metrics/feature/timeline/popularity/523) [indicate](https://www.chromestatus.com/metrics/feature/timeline/popularity/521) that this is a representative sample; it seems that the Hi-DPI and art direction use cases are easier for folks to wrap their minds around than resolution-switching. Which brings us to:

## Developer education

The aforementioned Jason Grigsby is giving a respimg talk at [An Event Apart in Atlanta](http://aneventapart.com/event/atlanta-2015) next week, and [posted a flowchart](http://lists.w3.org/Archives/Public/public-respimg/2015Jan/0003.html) that he was developing for the talk to the RICG mailing list, asking for feedback. This chart was a bit of a revelation for me. So many boxes! A spaghetti of arrows! And yet as I followed each branch of the decision tree, I realized that they were all necessary.

The new markup covers a bunch of separate, yet related, use cases. I agree with Jason that presenting every use case all at once, up front, is [not](https://twitter.com/grigs/status/562738155317907456) [the](https://twitter.com/grigs/status/562738406997127169) [best](https://twitter.com/grigs/status/562738553189593088) way to teach respimg. Better to start with a single use case and build out from there. Perhaps it’s entirely natural that, at this early stage, `w` (and `sizes`) adoption is lagging behind the older, more established bits of syntax.

## WordPress follow-up

So what should the largest CMS in the world do about the new bits?

After the WordPress respimg plugin [shipped last week](http://us8.campaign-archive2.com/?u=c988d9ca55d5d09e73a7dc993&id=528f79d024&e=4db00bcdc4), conversations surrounding how to move it forward largely centered around the `sizes` attribute. Those [conversations](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/issues/34) are [fascinating](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/issues/35).

The plugin, as shipped, leaves `sizes` off of `img` elements entirely, letting the browser pick amongst the provided (and `w`-descripted) `srcset` sources using the default `sizes` value of `100vw`. But! The spec [recently changed](https://github.com/ResponsiveImagesCG/picture-element/issues/253) to *require* a `sizes` attribute whenever `w` descriptors are present. So the plugin maintainers are trying to figure out how, if, and who to expose `sizes` to. Should site maintainers have a say in this? Or should it be left to theme authors? Should it be done via a straight-up text input field, or can this functionality be abstracted in some useful way?

These are the sorts of questions that CMSes are going to have to answer over the coming months.

While we're discussing the WordPress plugin –

- If you’re using it, we’d love your [feedback](https://wordpress.org/support/view/plugin-reviews/ricg-responsive-images)!

- Here’s an article about using the plugin [in Japanese.](http://parashuto.com/rriver/responsive-web/responsive-images-wordpress-plugin)

## Housekeeping, part deux

The results from [last week’s poll](https://docs.google.com/forms/d/1c_pQqkwOhBYe3mD5gBAEXscZDeA2bQyhL_NiW-mYpC4/viewform) are in:

- 43% of you want monthly newsletters
- 43% of you want fortnightly newsletters (a.k.a. the status quo)
- 14% of you want weekly newsletters

Given that this leans slightly towards MOAR NEWSLETTERS, we’ll change nothing, and continue to send one of these things to you every couple of weeks.

## Grab bag

- Here’s a smashing [video of Yoav’s respimg talk in Whistler](http://vimeo.com/117250453)
(oh and he’s giving a whole workshop at [SmashingConf Oxford](http://smashingconf.com/workshops/yoav-weiss)).

- Printing responsive images? [Printing responsive images!](https://www.w3.org/Bugs/Public/show_bug.cgi?id=27864#c2)

- A couple of [kind words for the group from Robin Berjon](https://twitter.com/boblet/status/559222927124488192)

See you in a couple of weeks!

—eric


