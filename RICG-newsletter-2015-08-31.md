# Steering gigantic ships
Microsoft, WordPress, and the HTML spec, oh my!

## Edge progress

`picture` is officially [“In Development”][in-dev] on Microsoft’s official status page. Even better: the latest Microsoft Edge build [now supports][sup] `w` descriptors and `sizes`! Go Redmond, go.

[in-dev]: https://dev.modern.ie/platform/status/pictureelement/?filter=f3f0000bf&search=picture
[sup]: http://www.winbeta.org/news/heres-whats-new-in-microsoft-edge-on-windows-10-build-10532

## Bringing responsive images to WordPress core

The [official responsive images plugin for WordPress][wp-ricg] currently sports “10,000+” active installs. Joe McGill recently penned [a post over on the WordPress Core blog][joe-post] about the effort to land the plugin’s functionality in Core, so that all million-bajillion of WordPress’ users will get respimg functionality *automatically*.

Joe outlines the issues left to conquer (and there are more than a few of them — WordPress’ image-handling is old, stable, and resistant to change), and calls on all interested to contribute. [Contribute!][joe-post]

[wp-ricg]: https://wordpress.org/plugins/ricg-responsive-images/
[joe-post]: https://make.wordpress.org/core/2015/08/25/responsive-image-support-update/

## 101 done

Jason Grigsby has completed his stupendous <cite>Responsive Images 101</cite> series with a pair of posts: one on [image breakpoints][ibreak], the other, a [conclusion][concl].

Jason has thought about image breakpoints more than anyone — I’m pretty sure he coined the term? — and it shows. After outlining the problem and a bunch of different ways to think about tackling it, Jason ends with a section called “Humans shouldn’t be doing this” and a plea for developers and CMSs to shield content creators from having to do the confounding, tedious work of creating and managing multiple alternate image resources.

The conclusion to the series is excellent. Jason celebrates how far responsive images have come, touches on a bunch of possible “201” topics, and implores us all to “Please share what you learn!” Hear, hear!

[ibreak]: http://blog.cloudfour.com/responsive-images-101-part-9-image-breakpoints/
[concl]: http://blog.cloudfour.com/responsive-images-part-10-conclusion/

## Specs on the move

The WHATWG HTML spec moved from its lonely SVN server [over to GitHub][html-gh] over the weekend. To date, Ian Hickson, WHATWG editor, has used a build script to pull `picture` from the [RICG’s repo][picture-gh] into the published WHATWG spec. As a result of the move, that workflow is being tossed. Henceforth, `picture` and friends [will][picture-direct-issue] [live][picture-direct-commit] in the WHATWG HTML repo, just like everything else.

Our venerable [`picture-element` repository][picture-gh] will live on for history, but all of the action is moving to the WHATWG HTML spec repo on GitHub. So if you’ve got a bug: [file it there][html-issues].

[html-gh]: https://github.com/whatwg/html
[picture-gh]: https://github.com/ResponsiveImagesCG/picture-element
[picture-direct-issue]: https://github.com/whatwg/html/issues/52
[picture-direct-commit]: https://github.com/whatwg/html/commit/d9cff6e9a6fb2928ef5d3f3d8df4e4dd18fb9b4c
[html-issues]: https://github.com/whatwg/html/issues

See you in a couple of weeks!

—eric

