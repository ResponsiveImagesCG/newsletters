# Twenty-four percent

**teaser:** WordPress gets respimg and Picturefill’s over the hill

The RICG aims to responsify the web’s images; I’ve always thought of that as a three-part problem. We needed to get respimg features into specs, browsers, and, most important of all, websites. That last one was always going to be a long slog, so I’m overjoyed to report some huge, wonderful news: [the RICG’s official WordPress plugin has been merged into WordPress Core][m].

[24%+ of the web][twenty], here we come!

To Joe McGill and the whole team behind the WordPress plugin: huge congrats and even bigger thanks.

[p]: https://core.trac.wordpress.org/ticket/33641#comment:9
[m]: https://core.trac.wordpress.org/changeset/34855
[twenty]: https://wordpress.org/about/features/

## This Picturefill goes to 3.0.1

A couple of weeks ago, I reported that Picturefill 3.0 — a near-complete re-write bringing spec-accurate parsing, robust tests, and fixes for niggling browser bugs in the extant implementations — was imminent. Welp, the team did me one better and released 3.0.1 last week. [Go update!][pf3]

So... what now? Picturefill was always meant to be a bridge — shepherding us all from a world without native implementations into a world with universal support. Now that almost every current shipping browser supports almost every respimg feature, Alexander Farkas (who was a driving force behind the PF3 effort) [has some ideas][farkasgist] on how Picturefill can start reducing its footprint. I find the fact that Picturefill was *designed* to slowly erase itself — to do less and less over time instead of piling on features ad infinitum — fascinating; PictureFill as a study in how to practically accelerate the progress of the web has always been fascinating to me too. I’m not close enough to the project to know if the time is right for Alexander’s ideas, but they’re definitely worth a [read-through][farkasgist].

[pf3]: https://github.com/scottjehl/picturefill/releases/tag/3.0.1
[farkasgist]: https://gist.github.com/aFarkas/dcc87311232987591a16

## Keep ’em Coming

It’s been a good fortnight for respimg articles and tutorials.

- Chen Hui Jing published [an excellent intro][jing] over at A List Apart.
- Greg Whitworth, the man behind Edge’s respimg implementation, posted [another great intro][whitworth] over on the Microsoft Edge Dev Blog.
- Video of a typo-prone, nervous nelly [presenting at SmashingConf][me-smashing] has surfaced.
- You can’t read it online yet, but I have a respimg article in the [latest Net Magazine][netmag], too.

[jing]: http://alistapart.com/article/using-responsive-images-now
[whitworth]: https://blogs.windows.com/msedgedev/2015/10/07/using-extended-srcset-and-the-picture-element-to-tailor-your-image-to-every-device-and-layout/
[me-smashing]: https://vimeo.com/140641364
[netmag]: http://www.creativebloq.com/net-magazine

## Grab bag

- Yoav has been cleaning up a couple of nasty viewport size bugs in the Chrome pre-parser. If you’ve noticed double-downloads on either [viewports that have a `width=device-width`][widthheight] or [mobile viewports that rely on the default viewport][nineeighty], fixes are on the way! And big thanks to all of the good people that have been [reporting][stack-one] [these][stack-two] [bugs][terraling].
- Tell [Responsivizr][responsivizr] little bit about your image breakpoints and it’ll chart out the range of sizes that image will occupy on the layout and spit out a markup snippet, too.
- If all goes according to plan, lazyload scripts of the future will leverage [Intersecton Observers][io].
- Finally, Brad Frost is [starting to write a little about Container Queries][frosty-cq] in his in-progress book on Atomic Design.

[widthheight]: https://code.google.com/p/chromium/issues/detail?id=526630
[nineeighty]: https://code.google.com/p/chromium/issues/detail?id=531820
[stack-one]: http://stackoverflow.com/questions/32941158/why-is-srcset-causing-images-to-download-multiple-times
[stack-two]: http://stackoverflow.com/questions/32841724/picture-tag-uses-wrong-source-on-chrome-on-android
[terraling]: http://terraling.github.io/srcset-sizes/
[responsivizr]: http://responsivizr.com
[io]: https://groups.google.com/a/chromium.org/forum/#!msg/blink-dev/eLxh8xUp3j4/m7RH4_nLBgAJ
[frosty-cq]: http://atomicdesign.bradfrost.com/chapter-3/#viewport-tools-for-flexible-patterns

See you in a couple of weeks!

—eric

