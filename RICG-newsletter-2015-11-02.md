
# Build and Deploy

## Remember, remember, the 8th of December

That’s the day that responsive images will ship in WordPress core, as the marquee feature of version 4.4 (curently in [beta][wp_beta]). The team is making some [final tweaks][wp_new_size] to the platform to prepare the way, and [Joe McGill recently appeared on the WP Tavern podcast to explain how it all works][wp_tavern].

WordPress may be the web’s largest single CMS, but it’s not the only one — a new, excellent-looking [respimg plugin for Kirby][kirby_respimg] appeared the other week. And it looks like the `jekyll-picture-tag` plugin for Jekyll [will soon be boarding the `srcset`, `w`, and `sizes` bandwagon][jekyll_w].

[wp_beta]: [https://wordpress.org/news/2015/10/wordpress-4-4-beta-1/]
[wp_new_size]: https://core.trac.wordpress.org/changeset/35479
[wp_tavern]: http://wptavern.com/joe-mcgill-explains-how-responsive-images-work-in-wordpress-4-4

[kirby_respimg]: https://github.com/jancbeck/kirby-responsive-images
[jekyll_w]: https://github.com/robwierzbowski/jekyll-picture-tag/issues/68#issuecomment-152596140

## It’s hosted

All of the above plugins do two things. First, they generate and manage multiple sizes/versions of your “master” image files. Second, they generate respimg markup that’ll be used within the context of each of their respective CMSes. What if you just want the first part of that – the image-management-bit, without the markup (or the tie-in to a particular CMS)?

Never fear, The Cloud™ is here! Mike Engel [wrote a thing about pairing cloud-based image hosts with respimg markup][nobake_respimg]. I’ve been experimenting with this stuff recently and having a fully-featured, well-maintained CMS/API for just your images ... well let’s just say it has some nice benefits when compared to the the bespoke ImageMagick, Ruby, duct-tape, and wishes-based workflow that I, personally, have been using for the past couple of years. Upload a high-res file once, and use it (with a few URL parameters to handle the scaling/cropping/format-conversion) anywhere.

And the services Mike mentions are moving *fast* – Imgix [just added bleeding-edge Client Hints support][imgix_ch].

[nobake_respimg]: https://medium.com/@beardfury/no-bake-responsive-images-9e1289ceb9f7
[imgix_ch]: http://blog.imgix.com/post/131102712254/next-generation-responsive-images-with-client

## Free as in JPEG

The venerable JPEG format — a 20+ year old [“alien technology from the future”][alien] — still rules the web. It’s efficient, universal, and patent-and-DRM-free.

Bad news: the committee in charge of JPEG is [“investigating solutions that will empower end-users to protect their privacy”][jpeg_bs] AKA adding a DRM extension to the web’s primary image format. The EFF (god love ’em) attended the latest JPEG meeting to tell them [exactly why that’s such a terrible idea][eff_jpeg]. Here’s hoping their presentation didn’t fall on deaf ears.

[alien]: https://xiph.org/~xiphmont/demo/daala/update1.shtml
[jpeg_good]: http://jpeg.org
[jpeg_bs]: http://jpeg.org/items/20151023_press.html
[eff_jpeg]: https://www.eff.org/deeplinks/2015/10/theres-no-drm-jpeg-lets-keep-it-way

## NKOTB

JPEG is old; formats like WebP and JPEG-XR are shiny and new. These are even newer, as they’ve just popped up on my radar in the last few weeks:

- [FLIF][flif] features world-beating lossless compression with a progressive loading scheme that they’re thinking some [interesting thoughts about re: responsive images][flif-rwd].
- [HIMG][himg] offers JPEG-like compression on slow and/or simple hardware

Neat.

[flif]: http://flif.info
[flif-rwd]: http://flif.info/responsive.html
[himg]: https://github.com/mbitsnbites/himg

## Grab Bag

- Toot toot! What’s that sound? It’s my own horn! Because this here newsletter just passed the 1,000-subscriber mark. I owe all of you beers.
- [Yoav went to TPAC][incubate_ur_face].
- Use Node and need to automatically crop/art direct images? [smartcrop.js][autocrop_js] might be just what the doctor ordered.
- Speaking of art direction at scale — a couple of folks from Walmart Labs gave [a great presentation about how they deal with responsive hero images][walmart_heros]. I write a lot of words about respimg code, tools, and specs — this talk focuses on the much gnarlier problems of organizational process and people. Super-informative and refreshing; also includes some delightful Jason Grigsby/Rick Astley mashup gifs.

[incubate_ur_face]: http://w3cmemes.tumblr.com/post/132069160337/meanwhile-in-the-wicg-breakout
[autocrop_js]: https://github.com/jwagner/smartcrop.js/
[walmart_heros]: https://www.youtube.com/watch?v=CJ07hLitIfU

See you in a couple of weeks!

—eric
