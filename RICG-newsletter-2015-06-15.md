# Great Taste, Less Filling

**Teaser text:** The mobile tide is turning, everybody’s still yelling about upgrading Picturefill, and hey! Shirts!

## iOS9 supports `w` & `sizes`

Yoav’s hard work – [getting `w` descriptors and `sizes` support into WebKit](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2015-05-11.md#w-and-sizes-have-landed-in-webkit-nightlies) – is paying off. Support for both features has been [confirmed in iOS 9 betas](https://twitter.com/AndyDavies/status/609028138639761408). Responsive image features are great everywhere, but they were really built for small screens. Landing resolution switching in the [most popular mobile browser in the world](https://www.netmarketshare.com/browser-market-share.aspx?qprid=1&qpcustomb=1) is a big, big deal. Both Chrome for Android and Lollipop web views [already support the features](http://caniuse.com/#feat=srcset); soon, most newish mobile devices will be fully `srcset` and `sizes` capable.

We’ve come so far since the first desktop implementations started to ship last fall. What better way to celebrate than by, oh, I dunno, buying something?

## Multi-threaded

Just get a load of [these new RICG Shirts! And hoodies!](https://cottonbureau.com/products/ricg-web-standard-mfg-corp)

Designed by [Geri](http://www.hellogeri.com/) in Nottingham.

## Wherin I continue to bang on about the importance Picturefill 2.3.1

Maybe you’ve heard? Picturefills <2.3.1 are holding back the progress of the platform. The RICG and friends are trying to make as much noise as possible about this – since I last shouted at you with a megaphone about it, both [Greg Whitworth at Microsoft](http://blogs.windows.com/msedgedev/2015/06/08/introducing-srcset-responsive-images-in-microsoft-edge/) and [Jeff Lembeck at A List Apart](http://alistapart.com/blog/post/picturefill-upgrade) have weighed in.

Greg’s post is particularly interesting, as it details the damned-if-you-do, damned-if-you-don't dilemma that the prevalence of old Picturefills put his team at Microsoft in, re: `currentSrc`.

One last note: I mentioned that the official WordPress plugin had made the jump to 2.3.1 last week, but forgot to tell you that the [Drupal responsive images module did, too](https://www.drupal.org/commitlog/commit/42538/efc4a6af36c37830079d834e1430d0003c8c36ba). Upgrade your Drupals!

## Grab bag


- Jason Grigsby has almost completed his wondrously clear and concise series, “Responsive Images 101”. [Here’s the latest](http://blog.cloudfour.com/responsive-images-101-part-8-css-images/) on responsive images in CSS aka `image-set` (but not yet).

- Most of the performance talk about images focuses on how long they take to load over the wire, but that’s just where their performance impact *begins*. Tim Kaldec gave a deep dive presentation on Mobile Image Processing, talking about how image processing actually works under the hood, and how images clog up small devices’ CPUs and memory, in addition to their internet connections. A great, technical talk with some important lessons and work-arounds: [slides](https://speakerdeck.com/tkadlec/mobile-image-processing-at-velocity-sc-2015), [video](https://www.youtube.com/watch?v=jP68rCjSSjM).

- Speaking of performance, here’s a nifty little library that uses CSS gradients as image placeholders, in order to reduce visually jarring image paints and help pages feel faster. Pairs well with [lazy](https://developers.google.com/speed/pagespeed/module/filter-lazyload-images)-[loading](https://github.com/aFarkas/lazysizes).

- The Picturefill folks have added a [gotcha section to their docs](https://github.com/scottjehl/picturefill#the-gotchas), discussing common pain points: double downloads, Firefox bugs, `vw` vs `%`, and art directing down to no image at all using transparent gifs.

- [Smashing Book 5](https://shop.smashingmagazine.com/products/smashing-book-5-real-life-responsive-web-design-ebook) with a respimg chapter by Yoav is out.

- Etsy [is using](https://twitter.com/lara_hogan/status/609371637591470080) `srcset` and `sizes` in their Seller Handbook articles. Their CMS integration appears to be [particularly impressive](https://twitter.com/lara_hogan/status/609371995617296385).

- Morten Rand-Hendriksen has been thinking deeply about how responsive images challenge some of the fundamental assumptions behind WordPress. He’s written not [one](http://mor10.com/wordpress-image-handling-in-a-responsive-images-world/), but [two](http://mor10.com/wordpress-responsive-images-and-dynamic-image-sizes/) posts on the topic.

See you in a couple of weeks!

—eric
