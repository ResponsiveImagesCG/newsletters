# RICG newsletter 2014-05-02

It's been a busy couple of weeks.

First and foremost: the Group's [IndieGoGo campaign](https://www.indiegogo.com/projects/picture-element-implementation-in-blink) to support Yoav Weiss’ implementation efforts came to a close on Thursday and we're over the moon about its success. We raised $1X,XXX: %XXX of our original $10K goal. Thus, not only will Yoav will be able to devote himself full-time to seeing the [rapidly-progressing](https://www.indiegogo.com/projects/picture-element-implementation-in-blink#activity) Blink implementation through — he'll also be able to port that implementation over to WebKit.

WebKit have given Yoav the [go-ahead](https://lists.webkit.org/pipermail/webkit-dev/2014-March/026401.html) to start coding and committing. It's important to note that they've made no promises to ship anything. But we can now say that experimental implementations have been green-lighted in Blink, [Gec](https://bugzilla.mozilla.org/show_bug.cgi?id=picture)[ko](https://bugzilla.mozilla.org/show_bug.cgi?id=srcset), WebKit, and [probably even IE](http://status.modern.ie/pictureelement). `<picture>`, `srcset`, and `sizes` are coming to every major rendering engine.

If you've been following the Group for any amount of time, you know just how amazing that is.

To everyone that contributed to the campaing: a sincere and heartfelt thank you. You helped make responsive images on the web a reality. Now it's time to start kicking the tires.

[Picturefill v2](http://scottjehl.github.io/picturefill/) hit beta this week. It provides a complete, spec-compliant pollyfill, allowing everyone to use the new markup in a fallback-and-future-friendly fashion, *right now*. It's still in beta so I wouldn't drop it into a production setting *yet*, but if you're looking to get your hands dirty with the new markup, [grab Picturefill v2](http://scottjehl.github.io/picturefill/#download) and start coding.

If you're feeling particularly adventurous, Yoav would like nothing more than to have as many people as possible using and abusing the in-progress Blink implementation. How-to:

1. Download [Chrome Canary](https://www.google.com/intl/en/chrome/browser/canary.html)
2. Go to `chrome://flags/#enable-experimental-web-platform-features`
3. Click "Enable"
4. Pause a moment, relishing life on the bleeding edge as you prepare to experience the future: native, in-browser responsive images.
6. Break things and [submit bugs](http://new.crbug.com).

As of this writing, `srcset` and `sizes` are up and running; `<picture>` and `<source>` aren't. [But they're just around the corner!](https://code.google.com/p/chromium/issues/detail?id=368830)

More huge news! [Sizer Soze](http://sizersoze.org/) is fully operational. Want to see first-hand just how wasteful your non-responsive images are? Give Sizer Soze a URL and a few window widths — it'll load your page, re-size and re-compress your images to fit the layout at those widths, and tell you what you would have saved by supplying appropriately-sized images. Hint: lots!

The server is young and loading/re-compressing boatloads of images is expensive so a little paitence and understanding might be in order... but it's worth it. There's nothing like seeing the giant potential savings on sites *you* own and maintain to really bring home the importance and potential of the new spec.

So: there is a *lot* going on. Sadly, I'm pushing up against my word limit... otherwise I'd mention that the new features are getting [Modern](https://github.com/Modernizr/Modernizr/pull/1305)[ized](https://github.com/Modernizr/Modernizr/pull/1302), [shived](https://github.com/aFarkas/html5shiv/issues/150), and [caniused](https://github.com/Fyrd/caniuse/pull/518), and point you to [Yoav's recent talk](http://vimeo.com/93347500) at the State of the Browser 2014 conference. Maybe I'd even have the space to show you [a crazy picture](https://twitter.com/AndyDavies/status/459982131562045440) of his grody jalopy of a laptop. Too bad.

See you in a couple of weeks!
