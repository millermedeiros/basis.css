# basis.css - a CSS framework for rapid development #

https://github.com/millermedeiros/basis.css/


## Intro

This is a collection of patterns that repeat across different projects and base 
styles that I have to set across many projects.

This framework is target for fast development. It is heavily inspired by
the [OOCSS approach](http://www.slideshare.net/stubbornella/the-cascade-grids-headings-and-selectors-from-an-oocss-perspective-ajax-experience-2009) of adding multiple classes to each element 
even if those classes aren't semantic and using elements as building blocks. 
A lot of people may not agree with this approach but it can reduce development time, 
file size and complexity a lot, read [this presentation](http://www.slideshare.net/stubbornella/our-best-practices-are-killing-us) to understand why/how.

The classes and features are exclusively structural, so you won't see any sort of 
rules for components like buttons or dialogs with a default visual style since for 
the kind of work I do it is very uncommon to share visual styles across multiple 
projects. The only elements which have a preset visual style are paragraphs 
and a few other basic elements/classes used as an implementation reference and that 
should be edited by the user.

Depending on the kind of project it may be a good idea to set default values to all the 
elements and just use classes to "enhance them", in other projects the visual style is
so apart from the semantic value and/or you need so many variations that it doesn't make 
any sense to have defaults. **Choose the best approach based on the project.**

> These files should provide a base start point but many of the properties should be
> tweaked to match your needs, it **isn't** a one-size-fits-all solution.


## Other Frameworks

This project shares a few features, techniques and "philosophy" present on 
[HTML5 Boilerplate](http://html5boilerplate.com/), [OOCSS](http://oocss.org/), 
[Blueprint CSS](http://www.blueprintcss.org/), [normalize.css](https://github.com/necolas/normalize.css)
and many other CSS frameworks... some of them are pure coincidence, others are heavily 
inspired or even copied... - techniques borrowed from other people (and that aren't 
common knowledge) are credited on the source code.

You can use some of the [stubbornella/OOCSS](https://github.com/stubbornella/oocss/) 
files (mod.css, space.css, media.css, table.css, ...) as a complement to basis.css 
features, those rules weren't included on purpose since they are already available on OOCSS.


## Browser Support

This project targets *modern* browsers (IE 7+, FF 3+, Chrome 4+, Safari 4+, Opera 10+). 
Please note that not all features been tested on all these browsers yet.


## Important

**This is a work in progress.** Some techniques may not be recommended on specific 
scenarios. Make sure you understand how to use those classes properly and avoid using
non-semantic markup whenever possible, some of the styles should be used only on very 
specific cases (.fl, .fr, .b, .em, .hcenter, ...), use only if the display style isn't 
directly related with the semantic value or if you are sure it won't degrade 
maintainability.


## License

Released under the [WTFPL](http://sam.zoy.org/wtfpl/) license.


## Examples

 - [All rules](http://millermedeiros.github.com/basis.css/tests/all.html)
