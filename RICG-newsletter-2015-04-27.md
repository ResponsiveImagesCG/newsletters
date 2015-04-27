# Trending up

**Teaser:** Usage is going up, Wordpress filesizes are going down, and you should really upgrade your dusty old Picturefill

## Put to work

All of this new markup that I prattle on about – how big of a deal is it, really? It has been a while since we last checked in with Chromium’s usage stats; so let’s (click the links for historical charts):

- [`w` descriptors](https://www.chromestatus.com/metrics/feature/timeline/popularity/524) and [`sizes`](https://www.chromestatus.com/metrics/feature/timeline/popularity/522) are both employed in one out of every 5,000 Chromium page loads.
- [`picture`](https://www.chromestatus.com/metrics/feature/timeline/popularity/521): 1 in 2,000
- [`x` descriptors](https://www.chromestatus.com/metrics/feature/timeline/popularity/523): 1 in 300

These charts raise interesting questions. Why is usage for all of these features up on the weekends and down during the work-week? Why has `x` descriptor usage fallen off slightly, after its meteoric rise? Most [recent](https://css-tricks.com/responsive-images-youre-just-changing-resolutions-use-srcset/) [articles](http://blog.cloudfour.com/dont-use-picture-most-of-the-time/) on the topic explicitly recommend using `srcset` + `w` descriptors for the most common case: images in flexible layouts that need to scale across both viewport sizes and screen resolutions. But that markup is currently dead last in the usage derby. Will it every catch up? When?

One small and interesting thing to note: `sizes` caught up with `w` descriptors *fast*, right after it was [made mandatory](https://github.com/ResponsiveImagesCG/picture-element/commit/535e96b73ea8b0e94a7819b1482cd48bff18698e), despite the fact that browsers handle `size`-less markup the same way that they always did. Three cheers for making change without breaking pages!

## Better image resizing in Wordpress

Dave Newton, wizard, [is bringing](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/commit/c71dcb37163fc3410833e92d5f2d632470948a1a) his ImageMagick magic (which he first delivered to the world [via Grunt](https://www.npmjs.com/package/grunt-respimg), before [porting it to PHP](https://github.com/nwtn/php-respimg)) to [the RICG’s WordPress plugin](https://wordpress.org/plugins/ricg-responsive-images/) (and it’s 3,000+ active installs).

His ImageMagick settings eat up a little more CPU than the WordPress defaults, so even though they produce *much* smaller images, this is going to start out as an opt-in thing. If you’re using the plugin and care about this stuff enough to subscribe to a newsletter about it, I urge you: opt in and [provide feedback](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/issues).

## Container queries have a home

“Container queries,” née “Element queries,” now have [a spec URL](http://responsiveimagescg.github.io/container-queries/). There’s little more than an abstract and some good intentions there at the moment, but from such humble beginnings, great things are born.

## PSA: upgrade your Picturefills

The [Picturefill 2.3.1 update](http://scottjehl.github.io/picturefill/#download) that I mentioned last week – which provided support for the Spartan developer preview – fixes more than just Spartan. Due to the way that the plugin used to feature-test, Picturefills ≤ 2.3.0 throw errors on WebKit Nightly, too. Which presumably means that those old Picturefills will cause errors in Mobile/Safari in the near future. So, [upgrade!](http://scottjehl.github.io/picturefill/#download).

## Grab Bag

- Yoav has formally expressed an [intent-to-implement Client Hints in WebKit](https://lists.webkit.org/pipermail/webkit-dev/2015-April/027381.html). I’d be more worried about the [stiff initial](https://lists.webkit.org/pipermail/webkit-dev/2015-April/027382.html) [resistance](https://lists.webkit.org/pipermail/webkit-dev/2015-April/027383.html) if that sort of response hadn’t characterized literally everything that Yoav has managed to do for the RICG over the last couple of years.
- Dan Matthew [wrote up his respimg implementation experiences](http://www.danmatthew.co.uk/2015/04/19/implementing-responsive-images/). The performance gains that he details (3.4 MB → 522 Kb) are particularly huge due to Dan’s simultaneous switch to lossy image compression (using JPEGs instead of PNGs for screenshots), but still! A thousand more blog posts like this, please!
- Did you know that Google provides [a free on-the-fly image re-sizer](https://carlo.zottmann.org/2013/04/14/google-image-resizer/)? I sure didn’t.

See you in a couple of weeks!

—eric
