# New website, new name
Teaser text: Deep and sincere apologies for all of the HORRORble puns!

## Scope creepy!

The RICG is about to tackle [Element Queries](http://responsiveimagescg.github.io/eq-usecases/). To prepare for the imminent broadening of the our scope of work, we’re doing some housekeeping:

- It’s official! We’re now the Responsive *Issues* Community Group
- We’ve got a new website, and it lives at [ricg.io](http://ricg.io)

Element Queries are a GHOULd idea! But it’s still very, very early days; to draft a use cases document, SPOOKification, and ultimately bring them to browsers we’ll need all the help we can get. ContriBOOte!


## image-spook()

A week ago Jason Grigsby [asked](http://lists.w3.org/Archives/Public/public-respimg/2014Oct/0016.html), “what ever happened to `image-set()`?” `image-set()` brings `srcset`’s functionality to CSS; Jason does a great job of explaining why we need it in a subsequent [blog post](http://blog.cloudfour.com/the-forgotten-responsive-images-spec-image-set/). `image-set()` was implemented with a prefix in WebKit [two years ago](http://blog.cloudfour.com/safari-6-and-chrome-21-add-image-set-to-support-retina-images/) (!) and then we all kind of... forgot about it.

The discussions that came out of Jason’s post were productive. `image-set()` is happening; [it’ll be specced as a part of CSS Images Level 3](http://lists.w3.org/Archives/Public/public-respimg/2014Oct/0032.html), [it’s going to have feature parity with HTML’s respimg features](http://ircbot.responsiveimages.org/bot/log/respimg/2014-10-23#T97312), and the RICG is going to push for it however we can. TERRORiffic!


## Boo!-link

Yoav’s respimg implementation in Blink is already shipping, but that doesn’t mean it’s done. Some changes made over the last couple of weeks:

[Blink now uses gemetric means to pick `srcset` sources](https://codereview.chromium.org/667763004/). What in the HELL does that mean? Blink used to pick the smallest source that supplied *at least* as many pixels as it needed; now it picks the source whose dimensions are the *closest* to what it needs. For example: before, given an option between two resources, one with 0.9x the image’s device pixel width and the other with 3x, Blink would have picked the 3x source; now it’ll compromise a little bit on sharpness and save a lot of bytes by selecting the 0.9x resource.

Different browsers are going to do different things here. With any luck, they’ll continue to experiment with, refine, and ultimately improve their `srcset` picking logic over time. Developers can’t predict which source will be chosen out of a `srcset`, and that’s a good thing. [“`srcset` is about letting go”](https://twitter.com/yoavweiss/status/524634996108427264).

Blink also now [avoids downloading smaller images if bigger ones are already available in the cache](https://codereview.chromium.org/674923004/). So, now, shrinking your browser window (or changing the orientation of your phone from landscape to portrait) won’t trigger a new request for a new resource; Blink will happily continue to scale-down the old, larger one. A clear and obvious win!

Lastly, Blink now gives developers [console warnings about bad `srcset` descriptors](https://codereview.chromium.org/649183007/). Helping you EXORCISE bugs.


## Yay! Link!

The [video from Wilto’s excellent talk at Refresh Boston](http://www.futureinsights.com/home/responsive-images-are-here-its-up-to-you-to-make-the-web-for.html) is up and it is chock full o’ Zelda references.


## Tricks and treats

There’s been no SCAREcity of miscellaneous links over the last two weeks:

- [Picturefill 2.2 hit beta](https://github.com/scottjehl/picturefill/releases/tag/2.2.0-beta). The new version brings better spec compliance, better performance, fewer bugs, and it plays nicely with Asynchronous Module Definitions.

- The NCC Group contradicted [Betteridgde’s Law of Headlines](http://en.wikipedia.org/wiki/Betteridge's_law_of_headlines) by asking, [“Is it time to start using `srcset` and the `picture` element?”](https://www.nccgroup.com/en/blog/2014/10/is-it-time-to-start-using-srcset-and-the-picture-element/)

- Eiji Kitamura published a bit of Javascript that uses [Service Workers](https://slightlyoff.github.io/ServiceWorker/spec/service_worker/) (which were just [green-lighted in Blink](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/QfxPGw0kJW8/bsIQTZu0UCkJ)) to auto-inject `srcset` markup based on a global manifest. Yoav [asks](https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/QfxPGw0kJW8/bsIQTZu0UCkJ), “who will write the tool that accomplishes the same task with a pre-processor?”

- Finally, in my favorite post this week, Brad Frost [showed us his shockingly simple responsive images strategy](http://bradfrost.com/blog/post/responsive-images/), and, in keeping with the philosophy of minimalism embodied in the markup itself, didn’t explain the rationale behind it *at all*. But one take-away is clear: respimg can be very simple; this stuff is only as complicated as we make it.

See you in a couple of weeks!

—eric
