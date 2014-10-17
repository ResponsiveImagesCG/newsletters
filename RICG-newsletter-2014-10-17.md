# NATIVE RESPONSIVE IMAGES HAVE LANDED
Teaser text: We did it. And there’s work to be done.

## Two! Browsers! Down!

[Chrome](http://www.theregister.co.uk/2014/10/15/chrome_38_first_picture_element/) [38](http://googlechromereleases.blogspot.com/2014/10/stable-channel-update.html) and [Opera 25](https://dev.opera.com/blog/opera-25/) have landed, bringing responsive image capabilities to hundreds of millions of users for the first time.

To everyone who’s given their time, attention, or money to this multi-year collaborative effort: thank you, and congratulations. We made the web better for everyone forever.


## ...three to go

Now seems like a good time to take stock of the work yet to be done. First of all: in browser engines. Armed with spec-editor Simon Pieter’s [suite of tests](http://w3c-test.org/html/semantics/embedded-content/the-img-element/), implementors march on:

**WebKit:** Yoav [has already landed basic `srcset` and `sizes` support in WebKit](https://bugs.webkit.org/show_bug.cgi?id=133620) ([the `x` descriptor bits shipped in iOS 8 and Safari 7.1!](http://caniuse.com/#search=srcset)), and is hard at work laying the [microtask](https://bugs.webkit.org/show_bug.cgi?id=137496) and [asynchronous image loading](https://bugs.webkit.org/show_bug.cgi?id=134488) foundations that WebKit needs in order to load images in response to changing media conditions (aka [all of that work that Christian Biesinger did in Blink](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2014-07-11.md#responsive-elements-in-blink--complete-picture-implementation-imminent)).

**Gecko:** John Schoenick continues to [plug](http://bugzil.la/picture-prefon) [away](http://bugzil.la/srcset-prefon) at his [various patches](https://treeherder.mozilla.org/ui/#/jobs?repo=try&revision=33010414cfab), and [is still hoping to get full respimg support on by default in FireFox 34 (or 35 by the latest)](http://ircbot.responsiveimages.org/bot/log/respimg/2014-10-08#T95391).

**IE:** Officially, the features are still “[under](https://status.modern.ie/imgsrcset) [consideration](https://status.modern.ie/pictureelement).” There are [positive signs](https://twitter.com/respimg/status/517744964223385600)!
 

## But more importantly: it’s our turn

- [`srcset` with `x`](https://www.chromestatus.com/metrics/feature/timeline/popularity/523): 0.0069% 
- [`picture`](https://www.chromestatus.com/metrics/feature/timeline/popularity/521): 0.0004%
- [`srcset` with `w`](https://www.chromestatus.com/metrics/feature/timeline/popularity/524) and  [`sizes`](https://www.chromestatus.com/metrics/feature/timeline/popularity/522): 0.0001%

Those are the percentages of Chrome pageloads that are utilizing responsive image markup right now. So: web developers! Implementors have paved (and continue to pave) the responsive image way; now it’s on us to actually walk it, one `picture` element and `srcset` attribute at a time. Go forth and mark up!


## Let the tools do the work

Or, wait, a better idea: let computers do it!

Tooling to take care of some of the tedious and error-prone bits of a responsive image implementation is already here to help.

Stephen Max has published [a Grunt plugin](https://github.com/smaxtastic/grunt-responsive-images-extender) that will auto-generate image versions and write your `scrset`s for you.

And Alexander Farkas published a truly wondrous thing, a bit of Javascript called [“lazysizes”](https://github.com/aFarkas/lazysizes) which lazily-loads images and writes your `sizes` for you, on the fly. This not only saves you from the trouble of writing `sizes` by hand — it lets you to keep your markup and presentation entirely separate!


## Keep those articles coming

The more how-to articles and personal implementation accounts, the merrier. Here’s this fortnight’s batch:

- Responsive Images: getting [bigger](https://dev.opera.com/articles/ja/native-responsive-images/) in [Japan](http://parashuto.com/rriver/responsive-web/picture-srcset-use-case) all of the time.

- Dudley Storey published [an introduction to `picture`](http://demosthenes.info/blog/936/Responsive-Images-For-Designers-The-HTML5-picture-element), and promises additional articles on `srcset` and `sizes` in the future. I can’t wait!

- Shane Prendergast wrote up [an intro to the full suite of markup and his efforts to understand it ](http://shaneprendergast.co.uk/css/srcset-picture/).

In it, Shane opines:

> One of the most confusing aspects is the fact that the widths are based on the viewport and not their containing elements. It would be cool if the browser was smart enough to know how big an image should be inside its container.

Sounds a lot like [Element Queries](http://responsiveimagescg.github.io/eq-usecases/) to me!

See you in a couple of weeks!

—eric
