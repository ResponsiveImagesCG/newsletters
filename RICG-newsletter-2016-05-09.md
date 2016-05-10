# Victory laps and deep dives

**Teaser text:** RICYMIG?

## Magick? Mitigate!

I’ll kick off with a quick PSA — if you’re using ImageMagick on a server *and* accept user uploads *and* haven’t heard about [“ImageTragick”][imagetragick], then panic, because your site is vulnerable to a zero-day exploit. Take steps!

[imagetragick]: https://imagetragick.com

## Have I mentioned that we did it?

I don’t “ICYMI” often. But when I do, it’s because [every responsive image feature is now supported by every browser][we-did-it].

The news was even better than I reported; turns out, Safari’s shipping `picture` implementation [*does* respond to viewport changes][correction-safari] and *doesn’t* double-download in the test case that I lazily linked to without actually, you know, checking. Yay!

Bruce “Strawman” Lawson (the man who first put the word “picture” between angle brackets) took a well-deserved [victory lap][bruce-victory-lap] over on the Opera blog, re-capping and reflecting on the achievement.

And our Chair, Mat Marquis, [recently appeared on the Responsive Web Design podcast][wilto-podcast] to discuss who, what, why-is-it-still-around, and what’s next for the RICG.

[we-did-it]: http://us8.campaign-archive1.com/?u=c988d9ca55d5d09e73a7dc993&id=5946649815&e=4db00bcdc4
[correction-safari]: https://github.com/ResponsiveImagesCG/newsletters/commit/351176eaa087325b9bb358b530cdfb425bf4a5d7#commitcomment-16796216
[bruce-victory-lap]: https://www.opera.com/blogs/news/2016/03/the-picture-element-saving-bandwidth-data-and-possibly-the-world/
[wilto-podcast]: http://responsivewebdesign.com/podcast/ricg/

## It’s dangerous to go alone!

 Martin Auswöger wrote a [respimg linter][respimg-linter]! “Linter” doesn’t quite capture [all of the things that this little bookmarklet does][respimg-linter-checks], though — in addition to checking for syntax errors (as the ever-helpful [HTML5 validator][valitator-nu] does), it actually loads your images across a full gamut of viewport sizes, and will raise the alarm if, say, your `sizes` is lying about the actual layout size of your image, or if it looks like you’re trying to kludge art-direction using `srcset`. I ran it across a few of my own pages, and the results were, uh, alarming. Bookmarklet bookmarked.

[valitator-nu]: https://checker.html5.org
[respimg-linter]: https://ausi.github.io/respimagelint/
[respimg-linter-checks]: https://ausi.github.io/respimagelint/docs.html

## Down ‘n nerdy with image formats

Colt McAnlis, developer advocate at Google, is writing [a book on image compression][understanding-compression] and has recently published a few articles on the subject, explaining how the [JPEG][colt-jpg-works] and [PNG][colt-png-works] compression algorithms work, and suggesting a plethora of tools and techniques for making [`.jpg`s][colt-jpg-smaller] and [`.png`s][colt-png-smaller] smaller.

If you’re game for a deep dive, these articles are well worth the effort. I’ll highlight one project that I discovered therein: the terribly-named [Butteraugli][butteraugli] image comparison tool, from Google. Buggerutley can provide not only a single number (like every other comparison metric, e.g. [PSNR][psnr] or [SSIM][ssim]), but also a *spatial map of dissimilarity* (woah?). Awesomely, Botticelli was motivated by a deep study of the biology of vision. How many engineers can casually drop references to the “frequency space inhibition of ganglion cells”?

And over on the Cloudinary blog, Jon Sneyers (creator of the new-and-exciting [FLIF image format][flif], which, hey!, he just gave [an excellent interview about][jon-interview]) takes a similarly technical tour of the JPEG compression algorithm and makes a wonderfully accessible analogy: [“JPEG is like a Photocopier”][jpeg-photocopier]. Recompression is bad; when you copy a copy of a copy, things can start to get, well, buttugli.

[understanding-compression]: http://shop.oreilly.com/product/0636920052036.do
[butteraugli]: https://github.com/google/butteraugli
[ssim]: https://en.wikipedia.org/wiki/Structural_similarity
[psnr]: https://en.wikipedia.org/wiki/Peak_signal-to-noise_ratio
[colt-png-works]: https://medium.com/@duhroach/how-png-works-f1174e3cc7b7#.7d6b3v7mz
[colt-png-smaller]: https://medium.com/@duhroach/reducing-png-file-size-8473480d0476#.rhsc7jqld
[colt-jpg-works]: https://medium.freecodecamp.com/how-jpg-works-a4dbd2316f35#.tebx1htgx
[colt-jpg-smaller]: https://medium.com/@duhroach/reducing-jpg-file-size-e5b27df3257c#.9k6ch9cis
[flif]: http://flif.info
[jon-interview]: http://dev.to/ben/interview-with-flif-creator-jon-sneyers
[jpeg-photocopier]: http://cloudinary.com/blog/why_jpeg_is_like_a_photocopier

## Grab Bag

- [Google is going to funnel all of its web platform feature development through our sister org, the WICG][google-wicg]. In other words, henceforth, when Google wants to change something about web standards, they will be doing it via a process and community that is open to anyone, everywhere, at the [click of a button][click-of-a-button].
- New-axis-of-respimg-adaptation alert! It’s time to [start thinking about color gamuts][color-gamuts].
- [Intersection Observers][intersection-observer] will power the lazyloaders of the future; the feature [just landed in Chrome 51][io-in-chrome].
- Speaking of lazy loading, my favorite lazyloader is [`lazysizes.js`][lazysizes] (because it keeps the presentation-separate-from-markup dream alive); the imgix folks just wrote about [how to use `lazysizes` in conjunction with their image hosting and resizing service][imgix-lazysizes].
- Speaking of imgix, Oliver Pattison [wrote up his strategy][imgix-jekyll] for building low-overhead respimg-equipped sites using imgix and Jekyll.
- Ever wonder [how to decorate an `object-fit` image][decorate-object-fit]?
- Neat: [Facebook is automatically authoring `alt` text on user uploads][automatic-alt] using artificial intelligence.
- [Performance matters][ft-perf].

See you in a few weeks!  
—eric

[google-wicg]: https://groups.google.com/a/chromium.org/d/msg/blink-dev/PJ_E04kcFb8/baiLN3DTBgAJ
[click-of-a-button]: https://groups.google.com/a/chromium.org/d/msg/blink-dev/PJ_E04kcFb8/qZtcSdE2AAAJ
[color-gamuts]: http://blog.iconfactory.com/2016/04/looking-at-the-future/
[intersection-observer]: https://github.com/WICG/IntersectionObserver/blob/master/explainer.md
[io-in-chrome]: https://twitter.com/ChromiumDev/status/718136230232383493
[lazysizes]: https://github.com/aFarkas/lazysizes
[lazysizes]: https://github.com/aFarkas/lazysizes
[imgix-jekyll]: https://olivermak.es/2016/05/jekyllconf-responsive-images/
[imgix-lazysizes]: https://blog.imgix.com/2016/05/02/imgix-lazysizes.html
[decorate-object-fit]: http://fvsch.com/code/object-fit-decoration/
[automatic-alt]: http://www.theverge.com/2016/4/5/11364914/facebook-automatic-alt-tags-blind-visually-impared
[ft-perf]: http://engineroom.ft.com/2016/04/04/a-faster-ft-com/
