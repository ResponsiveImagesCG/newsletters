# Say Yes to the Press

**Teaser text:** Adding responsive image support to WordPress, type-switching, and some housekeeping

## Responsive images in WordPress

Let’s talk about [WordPress](https://wordpress.org). According to some [websites](http://trends.builtwith.com/cms) that I just [found](https://managewp.com/14-surprising-statistics-about-wordpress-usage), the venerable pile of PHP and MySQL that we call “WordPress” serves up *1 in every 5 websites* and runs *more than half* of all websites that use a CMS at all.

So it’s high time that WordPress had proper responsive image support. Tim Evko wrote [a fine blog post](http://web-design-weekly.com/2015/01/20/ricg-responsive-images-plugin/) about the efforts that he, along with with our illustrious chair and a few members of the WordPress core team, has made to create a drop-in responsive images plugin for WordPress. The plugin can be had [here](https://wordpress.org/plugins/ricg-responsive-images/) and its source lives [here](https://github.com/ResponsiveImagesCG/wp-tevko-responsive-images). It does the hard work of creating a range of source files from a single high-resolution image, and marking them up with `srcset` and `sizes`. If you want to art-direct your WordPress-hosted images, you’ll need to use `picture`; as luck has it Rory Douglas [wrote a thing](http://terrificwebdesign.net/use-case/) about how to do *that* last week, too.

## Alternate formats

I love JPEG! [Mozilla likes it too](http://calendar.perfplanet.com/2014/mozjpeg-3-0/). The 22-year-old format recently received the strangest, highest compliment I have ever heard an engineer give when a researcher for the (awesome, exciting, in-development) Daala video standard [called it “alien technology from the future.”](https://people.xiph.org/~xiphmont/demo/daala/update1.shtml)

But, while JPEG was the first image format to dominate the web, it will not be the last. New formats are coming; new formats are already here. `picture`, `source` and the `type` attribute let us use them now while providing fallbacks for non-supporting browsers.

Jason Grigsby [posted a thing about `picture` and `type`-switching on the Cloud Four blog](http://blog.cloudfour.com/when-to-use-picture-for-resolution-switching/) this week; Zolton Dulac wrote [a *huge* article](http://www.useragentman.com/blog/2015/01/14/using-webp-jpeg2000-jpegxr-apng-now-with-picturefill-and-modernizr/) detailing the different formats currently on offer, when you should use each, and how to serve them to as many users as possible without breaking things for older browsers by using Modernizr and Picturefill. Read! Implement!


## Grab bag

A loads’o’links:

- Bruce Lawson [wrote a blog post](http://www.brucelawson.co.uk/2015/why-we-cant-do-real-responsive-images-with-css-or-javascript/) in preparation for an upcoming talk in Barcelona (next month at the [Awwwards conference](http://conference.awwwards.com)) which answers everybody’s first question about responsive images: why a markup solutuion? Why not JavaScript or CSS?
- Art direction can be a hard use-case to understand if you value content parity. [This post about adapting album art for cassettes](http://needmoredesigns.com/blog/early-responsive-design/) helped me wrap my mind around it back in the day; I recently stumbled across [an exploration into responsive logos](http://www.responsivelogos.co.uk/) that hit those same, sweet, “art direction is not only valid — it’s vital” notes for me.
- Hey did you know that [caniuse started tracking CSS image-set](http://caniuse.com/#feat=css-image-set) a month or two ago? I sure didn’t!
- [HTML5Test](https://html5test.com) – the website that tests you how well your browser supports HTML5 – [added responsive images feature tests last week](https://twitter.com/html5test/status/555747154846048256).
- Are you in Oxford, UK? Go see [Yoav talk about responsive images at SmashingConf](http://smashingconf.com/schedule#yoav-weiss)!


## Housekeeping

There was [some talk](http://ircbot.responsiveimages.org/bot/log/respimg/2015-01-12#T107999) in the RICG chat room the other day about reducing the frequency of these newsletters – maybe releasing them once a month instead of once every two weeks. We figure we should at least ask you for your opinion before making a change, so I set up [a one question survey](https://docs.google.com/forms/d/1c_pQqkwOhBYe3mD5gBAEXscZDeA2bQyhL_NiW-mYpC4/viewform?usp=send_form) which does exactly that. If you have a second, let me know — how often do you want these newsletters in your inbox?

See you in a couple of weeks!

—eric

