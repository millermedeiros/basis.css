# basis.css - a CSS framework for rapid development #

https://github.com/millermedeiros/basis.css/



## Intro

This is a collection of patterns that repeat across different projects and base
styles that I have to set across multiple projects.

This framework is target for fast development and is heavily inspired by the
[OOCSS
approach](http://www.slideshare.net/stubbornella/the-cascade-grids-headings-and-selectors-from-an-oocss-perspective-ajax-experience-2009)
of adding multiple classes to each element even if those classes aren't
semantic and using elements as building blocks. A lot of people may not agree
with this approach but it can reduce development time, file size and complexity
a lot, read [this
presentation](http://www.slideshare.net/stubbornella/our-best-practices-are-killing-us)
to understand why/how.

The classes and features are exclusively structural, so you won't see any sort
of rules for components like buttons or dialogs with a default visual style
since for the kind of work I do it is very uncommon to share visual styles
across multiple projects. The only elements which have a preset visual style
are paragraphs and a few other basic elements/classes used as an implementation
reference and that should be edited by the user (inside the "core" and
"widgets" folders).

Depending on the kind of project it may be a good idea to [set default values
to all the elements](https://github.com/necolas/normalize.css) and just use
classes to "enhance them", in other projects the visual style is so apart from
the semantic value and/or you need so many variations that it doesn't make any
sense to have defaults, this frameworks targets the later. **Choose the best
approach based on the project.**

> These files should provide a base start point but many of the properties
> should be tweaked to match your needs, it **isn't** a one-size-fits-all
> solution.

**Be pragmatic!**



## Other Frameworks

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




## Folder structure

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


### bss

Contain classes that **should not be edited or overwritten by any
circumstance** since it can lead to confusions and undesirable behavior.

Mostly classes to speed-up the development process and keeping things DRY. Most
of the classes uses `!important` to avoid that an element with the class
`.bss-fl` behaves like `.bss-fr`.

If you don't want a certain element to behave like the `.bss-` class makes it
behave  remove the class, don't edit it! `.bss-fl` should never mean `.bss-fr`
and so on...


### core

It is impossible to create base styles that works for all kinds of projects,
that's why these styles should be edited in almost all projects. Use them as an
implementation reference.


### widgets

Usually elements that are shared across multiple pages and that aren't directly
related with the core structure (e.g. ui components)




## Browser Support

This project targets *modern* browsers (IE 7+, FF 3+, Chrome 4+, Safari 4+,
Opera 10+).

If you need to support IE 6 search for descendant selectors `>`, if you delete
them code will probably work on IE6 as well, descendant selectors are good to
control scope of the rule (so we can have nested elements without breaking
things...)




## Important

### This is a work in progress.

Some techniques may not be recommended on specific scenarios. Make sure you
understand how to use those classes properly and avoid using non-semantic
markup whenever possible, some of the styles should be used only on very
specific cases (.bss-fl, .bss-fr, .b, .em, .bss-hcenter, ...), use only if the
display style isn't directly related with the semantic value or if you are sure
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




## Demo

 - [demo](http://millermedeiros.github.com/basis.css/demo.html)
