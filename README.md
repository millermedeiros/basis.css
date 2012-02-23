# basis.css - a CSS framework for rapid development #

https://github.com/millermedeiros/basis.css/



## Intro <a href="#intro" name="intro">#</a>

This main goal of this framework goal is to ease/speed up the development
process helping you to DRY. CSS zen garden is a nice concept but usually not
practical.

It is heavily inspired by the [OOCSS approach](http://www.slideshare.net/stubbornella/the-cascade-grids-headings-and-selectors-from-an-oocss-perspective-ajax-experience-2009)
of adding multiple classes to each element even if those classes aren't
semantic and using elements as building blocks. A lot of people may not agree
with this approach but it can reduce development time, file size and complexity
a lot, read [this presentation](http://www.slideshare.net/stubbornella/our-best-practices-are-killing-us)
to understand why/how.

The classes and features are mostly structural, so you won't see any sort of
rules for components like buttons or dialogs with a default visual style
(unless it's the bare-minimum to make it work) since for the kind of stuff I do
it is very uncommon to share visual styles across multiple projects. The only
elements which have a preset visual style are paragraphs and a few other basic
elements/classes used as an implementation reference and that should be edited
by the user (inside the "core" and "widgets" folders).

Depending on the kind of project it may be a good idea to [set default values
to all the elements](https://github.com/necolas/normalize.css) and just use
classes to "enhance them", in other projects the visual style is so apart from
the semantic value and/or you need so many variations that it doesn't make any
sense to have defaults, this frameworks targets the later. **Choose the best
approach based on the project.** (see [other frameworks](#other) for more info)

These files should provide a base start point but many of the properties should
be tweaked to match your needs, it **isn't** a one-size-fits-all solution.

**Be pragmatic!**



## Other Frameworks <a href="#other" name="other">#</a>

This project shares a few features, techniques and "philosophy" present on
[HTML5 Boilerplate](http://html5boilerplate.com/), [OOCSS](http://oocss.org/),
[Blueprint CSS](http://www.blueprintcss.org/),
[normalize.css](https://github.com/necolas/normalize.css) and many other CSS
frameworks... some of them are pure coincidence, others are heavily inspired or
even copied... - techniques borrowed from other people (and that aren't common
knowledge) are credited on the source code.

You can use some of the
[stubbornella/OOCSS](https://github.com/stubbornella/oocss/) files (mod.css,
space.css, media.css, table.css, ...) as a complement to basis.css features,
those rules weren't included on purpose since they are already available on
OOCSS.

If you want to use [normallize.css](https://github.com/necolas/normalize.css)
instead of a CSS reset, delete `core/reset.css` and `core/tags.css` files and
`@import url(normalize.css)` inside `master.css`, all the other things should
still work as expected.



## Folder structure <a href="#structure" name="structure">#</a>

Everything is broken into small modules to make it easier to use only the
classes you want, they are also split by kind.

```
~css/
 |+bss/             Framework code, should NOT be editted.
 |+core/            Project core structure, should be edited by user.
 |+widgets/         Componenents/Modules shared by multiple pages.
 `master.css        Loads other stylesheets.
```

Depending on the project I also create another folder called "sections" to
store styles specific to each template/section/page.


### bss <a href="#structure-bss" name="structure-bss">#</a>

Contain classes that **should not be edited or overwritten by any
circumstance** since it can lead to confusions and undesirable behavior.

Mostly classes to speed-up the development process and keeping things DRY. Most
of the classes uses `!important` to avoid conflicts with other styles.

If you don't want a certain element to behave like the `.bss-` class makes it
behave  remove the class, do **NOT** edit it! `.bss-fl` should never mean
`.bss-fr` and so on...


### core <a href="#structure-core" name="structure-core">#</a>

It is impossible to create base styles that works for all kinds of projects,
that's why these styles should be edited in almost all projects. Use them as an
implementation reference.


### widgets <a href="#structure-widgets" name="structure-widgets">#</a>

Usually elements that are shared across multiple pages and that aren't directly
related with the core structure (e.g. ui components)




## Browser Support <a href="#support" name="support">#</a>

This project targets *modern* browsers (IE 7+, FF 3+, Chrome 4+, Safari 4+,
Opera 10+).

If you need to support IE 6 search for descendant selectors `>`, if you delete
them code will probably work on IE6 as well, descendant selectors are good to
control scope of the rule (so we can have nested elements without breaking
things...)




## Important <a href="#important" name="important">#</a>

Some techniques may not be recommended on specific scenarios. Make sure you
understand how to use those classes properly and avoid using non-semantic
markup whenever possible, some of the styles should be used only on very
specific cases (.bss-fl, .bss-fr, .b, .em, .bss-hcenter, ...), use only if the
display style isn't directly related with the semantic value or if you know
it won't degrade maintainability.


### Compress/combine CSS files before deploy !!!

It is really important that you run a CSS compiler to minify and merge
`@import` calls to [reduce the number of HTTP
requests](http://developer.yahoo.com/performance/rules.html#num_http) and
increase load time performance. I've been using [RequireJS
optimizer](http://requirejs.org/docs/optimization.html#onecss) but you can use
other tools like [stylus](http://learnboost.github.com/stylus/),
[sass](http://sass-lang.com/), [less](http://lesscss.org/), since they
also merge imported style sheets. (it is not because Basis is written in plain
CSS that you can't use a pre-processor...)




## License

Released under the [WTFPL](http://sam.zoy.org/wtfpl/) license.




## Demo <a href="#demo" name="demo">#</a>

 - [demo](http://millermedeiros.github.com/basis.css/demo.html)
