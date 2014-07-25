**Short description:** Picture is absolutely shipping in Opera 25 and Chrome 38 and I make a number of questionable music references.

# Blink!

## The Fat Lady Sings
***Mamma don't take my code-a-Chrome-38***

With the necessary [responsive-element foundations](https://github.com/ResponsiveImagesCG/newsletters/blob/master/RICG-newsletter-2014-07-11.md#responsive-elements-in-blink--complete-picture-implementation-imminent) laid, Yoav posted an [“intent to ship” thread](https://groups.google.com/a/chromium.org/forum/#!topic/blink-dev/t3KRycUCGA8) re: the `picture` element over on the Blink-dev mailing list this week; the feature received the necessary support. Meaning that, barring any crazybugs, meteor strikes or other such unforeseen calamities, the `picture` element is finally, officially, *definitely* going to ship [un-flagged](https://codereview.chromium.org/401403003/) in Chrome 38 (in late September/early October) and Opera 25. Canary builds from here on out will support the feature by default, too.

Much implementation work remains to be done. `picture`, `srcset`, and `sizes` have been fully implemented in Gecko but are still behind flags in Firefox Nightly. The WebKit implementation has a ways to go. We’re still waiting on an official “yes, we’re implementing this” from IE. And it will take a while for these features to trickle down to mobile browsers, where they’re needed most. But! It feels great to have one foot, firmly planted.

## dev.Opera posted an excellent introductory article
***Le nozze di Figuring-out-the-new-markup-by-example-o***

Andreas Bovens posted [something great](http://dev.opera.com/articles/responsive-images/). I particularly like how he emphasizes the link between markup features and use-cases, and accompanies each example with a graphical key so that you can tell what problems the markup is trying to solve at a glance.

When [linking to the article](
http://www.brucelawson.co.uk/2014/on-the-complexity-of-the-picture-element/), Andreas’ fellow Opera employee (and [`picture` element sorta-kinda-inventor](http://www.brucelawson.co.uk/2011/notes-on-adaptive-images-yet-again/)) Bruce Lawson offered these words of encouragement:

> if my dull brain can understand it, yours can.


## Assorted tools you can use

### ...to lose those validation blues

The [W3C Validator](http://validator.w3.org/) now accepts and provides helpful advice on the new markup.

### Or perhaps you look better in red?

We’re [re-printing the RICG tees over at Cotton Bureau](https://cottonbureau.com/products/ricg). Sale ends August 5th!

### View source, up-sped

Mat Marquis wrote a Chrome extension which calls out pages using `picture` with a little badge (of approval, presumably). It’s called “[Picture in Play](https://chrome.google.com/webstore/detail/picture-in-play/mkhhihpihdlghkddhnadficgndpoigja)”. Mike Taylor quickly coded-up a [Firefox add-on  that does the same thing](https://addons.mozilla.org/en-US/firefox/addon/picture-in-play/); they both live in [this GitHub repository](https://github.com/Wilto/Picture-in-Play).


## In your “I”s
***♫ the light, the heat ♫***

Finally, as the RICG begins to look beyond responsive images into other responsive-y things – to element queries, and beyond – we realize that we need a new name. Or at least a new “I.” We’ve set up a suggestion box [here](https://docs.google.com/forms/d/1dblfSFkzsdQtdilg_xpbcufHuvSW4r761xWHEm3t8W0/viewform).

And yes, [“Insaneclownposse” has already been suggested](https://twitter.com/wilto/status/492323152303636480).

See you in a couple of weeks!

—eric
