To whit— the Blink and Gecko `picture` implementations are [all](http://bugzil.la/srcset-prefon) [but](http://bugzil.la/picture-prefon) [finished](https://codereview.chromium.org/401403003/) and IE is still [“considering”](http://status.modern.ie/imgsrcset) [things](http://status.modern.ie/pictureelement). Yoav’s WebKit work is facing some [initial technical hurdles](http://ircbot.responsiveimages.org/bot/log/respimg/2014-08-07#T85645). So it was a relatively quiet week around the RICG, but there was one bit of big news:

## [Picturefill 2.1 has landed](https://github.com/scottjehl/picturefill/releases/tag/2.1.0)

The new version of the polyfill brings it in line with many of the nittier, grittier aspects of the spec’s parsing algorithms. Edge cases and errors should all be handled as-per-spec and identically to the first implementations. All the more reason to start using `picture` and `srcset` in production, now!

Other than that, quiet week. But it wasn’t completely without incident.

## Some other stuff happened, too

Chris Ruppel [wrote a nice article on automated testing of `picture` using  CasperJS](http://fourword.fourkitchens.com/article/using-casperjs-test-picturefill). I don’t know much about CasperJS but I do know this: when developers rely less on fiddly manual window-resizing to test their responsive pages, everybody wins! Chris dosen’t get into testing `srcset` but this sort of automated testing is going to be especially helpful there; `srcset`’s functionality is essentially invisible.

Speaking of managing complexity, Rachel Andrew provided an excellent primer on [how](http://solutions.grabaperch.com/html-and-css/how-do-i-use-responsive-images-in-perch) and [why](http://grabaperch.com/blog/archive/perch-and-the-picture-element-for-responsive-images) to responsify your images in [Perch CMS](http://grabaperch.com). Hand Perch a hi-res image (or possibly a couple of crops) and, armed with a bit of template code, it will spit out all of the necessary source files and markup.

Like I always say, teach a page to `picture`, and it’ll serve users images tailored to their particular browsing environment forever. Teach a *CMS* to `picture`, and the effects will be significantly multiplied.

More of this sort of CMS integration, please!

Finally, [TAG](http://www.w3.org/2001/tag/)-alum and [#respimg](http://ircbot.responsiveimages.org/) lurker [Robin Berjon](http://berjon.com) published [a short article proposing a way forward for the HTML specification after HTML5](http://darobin.github.io/after5/). A biased TL;DR – make it work more like the RICG. Make developer-driven, feature-focused partial spec work not just easy, but the norm. Decentralize the specs and lower the barriers to entry. Sounds good to me!

See you in a couple of weeks!

—eric
