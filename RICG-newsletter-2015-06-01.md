# Update! Your! Picturefills!

**Teaser**: Old Picturefills are holding the web back.

## Update! Your! Picturefills!

I know I mentioned this [last time](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2015-04-27.md#psa-upgrade-your-picturefills), but recent events have made it super-extra important – if you use Picturefill and you haven’t updated to version 2.3.1, please, drop everything and [upgrade right now](http://scottjehl.github.io/picturefill/#download).

Mat Marquis [explains why this upgrade is so critical over at CSS Tricks](https://css-tricks.com/please-update-picturefill/). Basically: old Picturefills made some assumptions about browser support that were true at the time, but aren’t any longer. Those assumptions mean Picturefill <2.3.1 tries to polyfill (and write to) [the new `currentSrc` attribute](http://www.w3.org/html/wg/drafts/html/master/semantics.html#dom-img-currentsrc) in some browsers that already support it — but when supported, `currentSrc` is read-only. Trying to write to a read-only when `use strict` is in play is bad news – giant sites [like ESPN](https://twitter.com/respimg/status/603279308866625536) that use old Picturefills were missing most of their images in Microsoft Edge previews and WebKit nightlies. So, rather than break the web, [Edge](https://twitter.com/gregwhitworth/status/603315359597244416) and [WebKit](https://bugs.webkit.org/show_bug.cgi?id=144095) have decided not to not support currentSrc until y’all upgrade your Picturefills.

Picturefill is supposed to be a bridge to the future, not an obstacle to it. So, again: [please upgrade](http://scottjehl.github.io/picturefill/#download)!

## While you’re at it: upgrade your WordPress plugins, too!

The official RICG WordPress responsive images plugin was [recently updated](https://wordpress.org/plugins/ricg-responsive-images/changelog/). The new version includes:

- the aforementioned Picturefill 2.3.1, the importance of which should already be clear
- bug fixes and performance improvements
- Dave Newton’s image-y magick, behind a flag

The last item on that list is particularly exciting. Dave’s optimal ImageMagick settings (brought previously to [Grunt](https://www.npmjs.com/package/grunt-respimg) and [PHP](https://github.com/nwtn/php-respimg)) produce *much* smaller images. But they’re new, and they eat up a little more CPU than the WordPress defaults, so this is going to start out as an opt-in thing. If you’re using the plugin and care about image performance enough to subscribe to a newsletter about it, I urge you: [opt in](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images#advanced-image-compression) and [provide feedback](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/issues).


## Super Dave

In addition to bringing huge performance gains to the WordPress plugin’s 5,000+ active installs, Dave also recently [became so frustrated](http://ircbot.responsiveimages.org/bot/log/respimg/2015-04-30#T126746) with the horrendous performance of animated gifs that he [became a core FireFox committer](https://bugzilla.mozilla.org/show_bug.cgi?id=1160200) and [registered a new IANA MIME type](https://bugzilla.mozilla.org/show_bug.cgi?id=1160200#c20) in order to be able to this:

```
<picture>
	<source type="video/vnd.mozilla.apng" srcset="cat.apng" />
	<img src="cat.gif" alt="One cool cat" />
</picture>
```

We’ll owe every [APNG](http://en.wikipedia.org/wiki/APNG) we ever use with a gif fallback to Dave. Ideas are easy, but wrangling all of the code and politics surrounding browser implementations and standards bodies necessary to implement them is very, very hard. Thanks, Dave. And, Yoav: I guess you’ve been replaced? (;


## Grab bag

- If you only click four links in this newsletter, make the first one a [Picturefill upgrade link](http://scottjehl.github.io/picturefill/#download). But these should be numbers two through four: [Jason Grigsby on `type`](http://blog.cloudfour.com/responsive-images-101-part-7-type/), [Steve Souders on hero images and measuring perceived performance](http://www.stevesouders.com/blog/2015/05/12/hero-image-custom-metrics/), and [Sara Soueidan on art-directing embedded SVGs](http://sarasoueidan.com/blog/svg-art-direction-using-viewbox/). Three great writers breaking down vital, technical subjects with clarity and style.
- It’s official (⨉3) – responsive images recently [headlined the FireFox 38 announcement post](https://hacks.mozilla.org/2015/05/trainspotting-firefox-38/), [hit the WebKit status page](https://twitter.com/yoavweiss/status/597859097074085890), and [are slated for inclusion in WordPress core](https://wordpress.org/plugins/browse/beta/).
- Speaking of Firefox support – you may remember that FireFox 38 shipped without the ability to respond to viewport changes. This is especially troublesome for pages that rely on art direction – it means that simply resizing a Firefox window can break an art-directed page’s layout. The relevant patch is still [in limbo](https://bugzilla.mozilla.org/show_bug.cgi?id=1135812#c51), but if you need resize-responding right now, Alexander Farkas has published [a quick fix](https://github.com/aFarkas/lazysizes/blob/gh-pages/plugins/static-gecko-picture/ls.static-gecko-picture.js).
- Here’s a stat that suprised me: [speculative pre-parsers initiate 43% of image loads](https://twitter.com/Souders/status/597821415354535936). The next time someone asks why we couldn’t have used CSS for responsive images, or why in the world we needed `sizes` – that’s why!
- The RICG is up for some Net Awards! It’s a bit strange to see our little red logo put in the ring against the likes of [a 24 billion dollar company with 3,700 employees](https://www.google.com/finance?q=twitter), but what the heck! [Go](https://thenetawards.com/vote/web-tech/responsive-images/) [ahead](https://thenetawards.com/vote/web-tech/element-queries/) and [vote](https://thenetawards.com/vote/collaboration/responsive-images/) [for](https://thenetawards.com/vote/developer/yoav-weiss/) [us](https://thenetawards.com/vote/team/the-responsive-issues-community-/)! 
- Yoav has [a patch in to kick off client hints work in WebKit](https://bugs.webkit.org/show_bug.cgi?id=145380). It’s getting some [push back](https://lists.webkit.org/pipermail/webkit-dev/2015-May/027471.html). Have I mentioned that the politics around browser implementations are hard?
- Bruce Lawson gave a rollicking respimg talk at DrupalJam: [slides](http://brucelawson.github.io/talks/2015/respimg/), [video](https://dev.opera.com/blog/bruce-introduction-responsive-images/).
- Joe McGill, respimg-in-WordPress implementer, will be [speaking on the subject](https://denver.wordcamp.org/2015/sessions/#wcorg-session-763) in Denver, Colorado in a couple of weeks, at WordCamp. Which is cool for me because I live in Denver, and I might get to meet him. Will you be in Denver, too? [Tweet at me](http://twitter.com/etportis) and maybe we can figure out some sort of meet up.
- Joe will probably be talking about lots of neat WordPress things, like [adding responsive images to advanced custom fields](http://responsivedesign.is/articles/adding-responsive-images-to-advanced-custom-fields-in-wordpress).
- Last and least: I will be [speaking](http://smashingconf.com/freiburg-2015/speakers/eric-portis) and [workshopping](http://smashingconf.com/freiburg-2015/workshops/eric-portis) respimg in Germany at SmashingConf in September. Gulp.

See you in a couple of weeks!

—eric
