# basis.css - a CSS framework for rapid development #


## Intro

This is a collection of patterns that repeat across different projects and base styles that I have to set across most projects. This file is as an example of how to use some of the features and also how they render by default. It is also used for testing purposes.
Philosophy

This framework is meant to be used for fast development. It is heavily inspired by the OOCSS approach of adding multiple classes to each element even if those classes aren't semantic. A lot of people may not agree with this approach but it can reduce a lot development time and also reduce file size and CSS complexity. The classes and features are exclusively structural, so you won't see any sort of rules for components like buttons or dialogs with a default visual style since for the kind of projects I work it is very uncommon to share visual styles across multiple projects. The only elements which have a preset visual style are headings, paragraphs and a few other basic elements/classes which should be edited by the user to match the project needs and are included just as a reference.


## Other Frameworks

This file shares a few features, techniques and "philosophy" present on [HTML5 Boilerplate](http://html5boilerplate.com/), [OOCSS](http://oocss.org/), [Blueprint CSS](http://www.blueprintcss.org/) and many other CSS frameworks... some of them are pure coincidence, others are heavily inspired or even copied... - techniques borrowed from other people (and that aren't common knowledge) are credited on the source code.


## Browser Support

This project targets modern browsers (IE 7+, FF 3+, Chrome 4+, Safari 4+, Opera 10+). Please note that not all features been tested on all these browsers.


##Important

**This is a work in progress.** Some techniques may not be recommended on specific scenarios. Make sure you understand how to use those classes properly and avoid using non-semantic markup whenever possible, some of the styles should be used only on very specific cases (.small, .big, .em, .b, .del, ...), use only if the display style isn't directly related with the semantic value. 

