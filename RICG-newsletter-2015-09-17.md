# Elastisch Bilder

Jetlagged greetings from a train in Germany; I’m on my way back to the States after speaking (!) at SmashingConf (!!!). Never did I think an interest in respimg would take me to a medieval hall, half a world away, to tell hundreds of people how to do their jobs. But! It did! And I drank bier and ate würst and met heroes and made friends. It was as wonderful as it was surreal. Video soon, [slides here][my_slides]. To the links—

[my_slides]: http://www.slideshare.net/eeeps/a-techy-stretchy-image-scrimmage

## Terriffic Tutorials

Mat, Yoav, and the good people at Akamai collaborated on a pair of whiteboard-style respimg [tutorial][mat_vid] [videos][yoav_vid]. They’re fast-paced and accessible; the visual metaphors surprise and delight. Watch!

Jake Archibald had a respimg “[epiphany][jake_ri]” recently — “I’m writing it all down before I forget everything.” His post wins the award for conveying the most information in the least amount of space. And it’s somehow personable and digestible, too. Everything that you need to know about the syntax in a pretty-short blog post. Read!

Finally — my interest in Client Hints still far outpaces my expertise, so I learned a lot from [this article][ilya_ch] by Mr. Client Hints himself, Ilya Grigorik. Automate!

[mat_vid]: https://www.youtube.com/watch?v=GJLl6MSHDr4
[yoav_vid]: https://www.youtube.com/watch?v=WwgQ0LGRnR8
[jake_ri]: https://jakearchibald.com/2015/anatomy-of-responsive-images/
[ilya_ch]: https://developers.google.com/web/updates/2015/09/automating-resource-selection-with-client-hints


## Core Competency

The energy (and consistency!) behind the effort to bring respimg to WordPress core is a joy to behold. Joe McGill published a brief update on the efforts last week, which concludes (with all too little fanfare) “we’re ready to create an initial patch candidate for core.”

A very large website (anybody know who?) deployed `x` descriptors last week and [doubled the current level of usage overnight](https://www.chromestatus.com/metrics/feature/timeline/popularity/523): `x` descriptors are now used on ~1% of Chrome pageviews. That’s a very big deal, but `w`s hitting WP-Core might an order-of-magnitude bigger.

[joe_wp]: https://make.wordpress.org/core/2015/09/05/responsive-images-feature-plugin-update/

## Grab Bag

- Edge is [officially][edge_image-set] implementing `image-set()`.
- Picturefill 3 should be out of beta [imminently][pf3_rc1].
- Understanding and communicating how an adaptable image will adapt within a responsive design is hard. Kevin Mack and Tim Vonderloh gave [a presentation][cropping] at the Columbus Web Group about re-using the concepts and language of print (where variability comes from imperfect processeses) to respimg (where the variability happens *by design*).
- Last and maybe actually least, Facebook blogged about their [cover photo optimization efforts][cover_photos]. The post doesn’t mention respimg, per-se, but it does contain a lot of insight into how Facebook actually goes about making, managing, and delivering images efficiently at Facebook-scale.

[edge_image-set]: https://dev.modern.ie/platform/status/cssimageset/
[pf3_rc1]: https://twitter.com/respimg/status/641311961171533824
[cropping]: https://twitter.com/nicetransition/status/637345391910916096
[cover_photos]: https://code.facebook.com/posts/991252547593574/the-technology-behind-preview-photos/

Tschüs!
—eric

