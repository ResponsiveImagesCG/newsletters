# Happy New Year!

**Teaser:** WordPress, WebKit, WooHoo!

As the newsletter wakes from its long winter’s nap, let me wish everybody a very happy new year! What happened while I was away? Lots!

## WordPress 4.4 happened!

[WordPress 4.4 was released][wp-release], bringing responsive images to the biggest CMS on the planet.

Predictably, this resulted in the biggest uptake in responsive image usage, ever. A month ago, one in every 2,500 pages sampled by Chrome used `w` descriptors. Now that number is 1 in 500 and [quickly climbing][chrome-status].

So, once again, let me thank [the team behind the effort][wp-respimg-team]. To Joe McGill, Tim Evko, Jasper DeGroot, and everyone else who lent time and energy to respimg-in-WordPress: thanks for making the web a faster, better, and more responsive place.

(And for an excellent technical overview of how 4.4 actually goes about it’s responsifying, read [this post by Fränk Klein over on the WP Best Practices blog][wp-best])

## So did `picture` in WebKit (sorta)!

The [`picture` bug in WebKit][webkit-bug] is now `RESOLVED FIXED`, and WebKit are announcing that [`picture` “has landed”][webkit-tweet].

This is true! But, if you’ll allow me to over-extend the metaphor, the implementation is still taxiing towards the gate.

`picture` in WebKit (which you can test by downloading [WebKit Nightly][webkit-nightly]) currently has some issues with double-downloads, and doesn’t yet respond to viewport changes. Luckily the implementation will have plenty of time to mature, as it (probably) won’t be ported over to shipping Safaris until their next major version bumps in the fall.

But! In the Fall! Mobile and desktop Safari will (probably) ship with complete responsive images implementations! And the last gap in respimg support will be filled. Huzzah.

## 2016: Year of the Container Query?

The end of 2015 brought a lot of new thinking and tinkering on the evergreen topic of Element/Container Queries. Tommy Hodgins and Maxime Euzière have registered [elementqueries.com][eq-com]; in addition to housing their [EQCSS Javascript library][eqcss] there, they’ve used the domain to publish *loads* of [demos][eq-demos] and collected [a comprehensive list][eq-resources] of element/container query resources. Check it out!

And [over on 24 Ways][ways], Jonathan Snook gives a very nice executive summary of the what and why of container queries, surveys the current landscape of prollyfills and experimental implementations, and shows how Shopify is actually prollyfilling Container Queries in production (!).

## Grab bag

- I wrote a thing! About [automating responsive images using Cloudinary’s on-the-fly resizing  features][cloudinary].
- A couple of Performance Calendar posts went deep on topics near and dear to the RICG’s heart: [Colin Bendell on chroma-subsampling][chroma]; [Tobias Baldauf on lazy loading][lazy].
- `alt` text is vital, and a *truly* responsive image will adapt all the way down to no-image-at-all. [Chrome for Android just shipped a “no images” preference][no-images].
- [Placeholder images in spaaaaaaace][space]


See you in a few weeks!
—eric

[wp-release]: https://codex.wordpress.org/Version_4.4
[chrome-status]: https://www.chromestatus.com/metrics/feature/timeline/popularity/524
[wp-best]: http://wpbestpractices.com/wordpress-4-4-responsive-images/
[wp-respimg-team]: https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images/graphs/contributors

[webkit-bug]: https://bugs.webkit.org/show_bug.cgi?id=116963
[webkit-tweet]: https://twitter.com/webkit/status/672430609491431425
[webkit-nightly]: http://nightly.webkit.org

[eq-com]: http://elementqueries.com
[eqcss]: https://github.com/eqcss/eqcss 
[eq-demos]: http://elementqueries.com/#demos
[eq-resources]: http://elementqueries.com/#further-reading
[ways]: https://24ways.org/2015/being-responsive-to-the-small-things/

[cloudinary]: http://cloudinary.com/blog/responsive_images_with_srcset_sizes_and_cloudinary
[chroma]: http://calendar.perfplanet.com/2015/why-arent-your-images-using-chroma-subsampling/
[lazy]: http://calendar.perfplanet.com/2015/immaculate-imagery-with-lazy-pictures-bpg/
[no-images]: http://www.theverge.com/2015/12/1/9827386/google-chrome-android-data-saver-image-blocking
[space]: https://spaceholder.cc
