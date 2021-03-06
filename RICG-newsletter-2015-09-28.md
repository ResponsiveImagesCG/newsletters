# Eventful

What a month. Personally, I went to Germany to speak (!) at SmashingConf (!!!). Never did I think an interest in respimg would take me to a medieval hall, half a world away, to tell hundreds of people how to do their jobs. But! It did! And I drank bier and ate würst and met heroes and made friends. It was as wonderful as it was surreal.

And I actually had a newsletter all written in the Frankfurt Flughafen, ready to fire off as soon as I got home, but by the time I got there the RICG had won a pair of [Net Awards](https://thenetawards.com), necessitating a re-write.

- [Best Collaborative Project](https://twitter.com/yoavweiss/status/644982406211063808)
- [Best New Web Technology](https://twitter.com/yoavweiss/status/644984378045673472)

Feels good, man. To the links!

## Edge implements `picture`

That was quick. Edge version 10547 [supports `picture` and `sizes`][edge_picture].

This means that (with a single, hopefully-soon-remedied [exception][safari]) every current version of every desktop browser now supports the full suite of responsive image features.

Oh, and the Edge team will [probably][edge_image-set] implement `image-set()`, too!

[edge_picture]: https://dev.modern.ie/platform/changelog/desktop/10547/
[safari]: https://bugs.webkit.org/show_bug.cgi?id=116963
[edge_image-set]: https://dev.modern.ie/platform/status/cssimageset/


## Core Competency

The energy (and consistency!) behind the respimg-in-WordPress team is a joy to behold.

They [released a new version of the official plugin last week][wp_v25], which, among other things, brings respimg support to images published before the plugin was installed, using output filters. This is one more step towards the larger goal: [bringing respimg functionality to WordPress core][joe_wp].

A very large website (anybody know who?) deployed `x` descriptors this month and [doubled the current level of usage overnight](https://www.chromestatus.com/metrics/feature/timeline/popularity/523): `x` descriptors are now used on ~1% of Chrome pageviews. That’s a very big deal, but `w`s hitting WP-Core might an order-of-magnitude bigger.

[wp_v25]: https://wordpress.org/plugins/ricg-responsive-images/changelog/
[joe_wp]: https://make.wordpress.org/core/2015/09/05/responsive-images-feature-plugin-update/


## Terriffic Tutorials

Mat, Yoav, and the good people at Akamai collaborated on a pair of whiteboard-style respimg [tutorial][mat_vid] [videos][yoav_vid]. They’re fast-paced and accessible; the visual metaphors surprise and delight. Watch!

Jake Archibald had a respimg “[epiphany][jake_ri]” recently — “I’m writing it all down before I forget everything.” His post conveys a a ton of information extremely economically, and it’s somehow personable and digestible, too. Everything that you need to know about the syntax in a pretty-short blog post. Read!

Finally — my interest in Client Hints still far outpaces my expertise, so I learned a lot from [this article][ilya_ch] by Mr. Client Hints himself, Ilya Grigorik. Automate!

[mat_vid]: https://www.youtube.com/watch?v=GJLl6MSHDr4
[yoav_vid]: https://www.youtube.com/watch?v=WwgQ0LGRnR8
[jake_ri]: https://jakearchibald.com/2015/anatomy-of-responsive-images/
[ilya_ch]: https://developers.google.com/web/updates/2015/09/automating-resource-selection-with-client-hints

## Grab Bag

- Picturefill 3 should be out of beta [imminently][pf3_rc1].
- Spec changes afoot: [the `width` attribute is now used as a fallback][width_attr] for invalidly-omitted `sizes`, and the meaning of the Client Hints `Width` header [just changed from CSS to device pixels][ch_width]. Someday I shall catalog the many definitions of the extremly-overloaded word “width” w/r/t respimg...
- Understanding and communicating how an adaptable image will adapt within a responsive design is hard. Kevin Mack and Tim Vonderloh gave [a presentation][cropping] at the Columbus Web Group explaining how they apply the concepts and language of print (where variability comes from imperfect processeses) to respimg (where the variability happens *by design*).
- Last and maybe actually least, Facebook blogged about their [cover photo optimization efforts][cover_photos]. The post doesn’t mention respimg, per-se, but it does contain a lot of insight into how Facebook actually goes about making, managing, and delivering images efficiently at Facebook-scale.

[pf3_rc1]: https://twitter.com/respimg/status/641311961171533824
[cropping]: https://twitter.com/nicetransition/status/637345391910916096
[width_attr]: https://github.com/ResponsiveImagesCG/picture-element/issues/268
[ch_width]: https://twitter.com/yoavweiss/status/647005135017758720
[cover_photos]: https://code.facebook.com/posts/991252547593574/the-technology-behind-preview-photos/

Tschüs!

—eric
