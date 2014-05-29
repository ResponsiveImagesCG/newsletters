# RICG newsletter 2014-05-30

I’ll cut right to the chase: Chrome Canary currently has a fully-operational implementation of the `picture` spec behind a experimental flag. In the words of Yoav, [“the important part now is *testing*”](https://twitter.com/yoavweiss/status/471405184741281792). So:

1. [Download Canary](http://www.google.com/intl/en/chrome/browser/canary.html)
2. [Enable “Experimental Web Platform Features”](chrome://flags/#enable-experimental-web-platform-features)
3. [File bugs](http://new.crbug.com).

Barring any unexpected opposition, outstanding bugs, last-minute spec changes, or other unforeseen circumstances, Yoav hopes to ship `sizes`, unflagged, in Chrome 37 stable — shipping in August. With any luck, on-by-default `picture` should follow in Chrome 38 in September.

It’s been a long time coming. Mark your calendars!

On the Firefox front, John Schoenick isn’t too far behind; you can grab work-in-progress builds of his latest, greatest, also fully-functional builds [here](https://tbpl.mozilla.org/?tree=Try&rev=263bdc53b84d). John’s code won’t be hitting Firefox Nightly for another week or two.

## What’s next?

[Webkit](https://twitter.com/yoavweiss/status/471573481273184256)!

## And after that?

[Element Queries](http://www.jonathantneal.com/blog/thoughts-on-media-queries-for-elements/)!

Wait, what!?

After various [chatterings](http://discourse.specifiction.org/t/element-queries/26/9) and [murmurations](https://twitter.com/wilto/status/466673241130430464), a <cite>[Use Cases and Requirements for “Element Queries”](https://github.com/ResponsiveImagesCG/eq-usecases)</cite> document appeared in the RICG GitHub the other day.

It is early, early days. But now that `picture` is on the home stretch, we find ourselves with some bandwidth to devote to other topics. An organization that’s spent the last three years bridging the gaps between everyday developers, spec editors, and browser vendors — an organization that’s succeeded in taking a major feature from ideation to implementation — seems like a terrible thing to waste, no?

We think so.

If you, like us, find yourself with ideas and/or enthusiasm for element queries, now’s the time to join the conversation on [GitHub](https://github.com/ResponsiveImagesCG/eq-usecases/issues), in the #respimg room on irc.w3.org, or on that newfangled [Discourse board](http://discourse.specifiction.org/t/element-queries/26).

See you in a couple of weeks!
