---
title: Javascript
---

{{% toc /%}}

# References

-   See also {{< iref "data_exchange#yaml" "Yaml/Json" >}}

-   Wikipedia: {{< wp "Ecmascript" >}},
    {{< wp "JavaScript" >}},
    {{< wp "Client-side JavaScript" >}},
    {{< wp "Server-side JavaScript" >}},
    {{< wp "JavaScript syntax" >}}
-   [JavaScript](https://github.com/sorrycc/awesome-javascript)
    *awesome list* of resources
-   Javascript libraries *awesome lists*:
    -   [Angular 2](https://github.com/AngularClass/awesome-angular)
    -   [Ember.js](https://github.com/nmec/awesome-ember)
    -   [JavaScript Learning Resources
        ](https://github.com/micromata/awesome-javascript-learning)
    -   [Koa](https://github.com/ellerbrock/awesome-koa)
    -   [Node.js](https://github.com/sindresorhus/awesome-nodejs)
    -   [npm](https://github.com/sindresorhus/awesome-npm)
    -   [React](https://github.com/enaqx/awesome-react)
    -   [Svelte](https://github.com/flagello/awesome-sveltejs)
    -   [VueJS](https://github.com/vuejs/awesome-vue)

The {{< wp "Ecmascript" >}} specification evolved since the 3rd edition
(December 1999) which is a widely adpted standard, just straightened
in Emascript V5 _ES5_ which was published in 2009, and a new standard
5.1 in 2011. The emacscript V 6
in 2015, named _ES6_ or _ES2015_ is a strong improvement it was
followed in 2016 by the V 7 and 2017 by the V 8. Presentely most modern [implementations
](https://en.wikipedia.org/wiki/ECMAScript#Implementations) follow at
least V5.1, the {{< wp "V8_(JavaScript_engine)"  "V8" >}} engine which power up
Chrome, Opera, Vivaldi, CouchBase, Electon and Node.js support ES6 and
some part of V7 and V8; while {{< wp "JavaScriptCore" >}} that power up WebKit,
Safari, Qt 5 support ES2017 and {{< wp "SpiderMonkey" >}} the engine of
Firefox, Gecko, Adobe Acrobat support 5.1 and partially ES2015 ES2016,
ES2017.


-   The original ECMAScript Language Specification, 3rd edition
    (December 1999) _«The specification is of extremely poor
    quality. It is difficult to read and very difficult to understand»
    dixit Douglas Crockford._
-   [ECMA-402 ECMAScript 2016 Internationalization API Specification
    (june 2016)
    ](http://www.ecma-international.org/publications/standards/Ecma-402.htm)
-   [ECMA-414 ECMAScript Specification Suite (December 2016) (pdf)
    ](http://www.ecma-international.org/publications/files/ECMA-ST/ECMA-414.pdf)
-   [ECMAScript 2017 (ECMA-262) Language Specification
    ](https://tc39.github.io/ecma262/)
-   [ECMAScript 6 — New Features: Overview & Comparison
    ](http://es6-features.org/)
-   [w3schools.com JavaScript index](http://www.w3schools.com/js/default.asp)
-   [developer.mozilla.org](http://developer.mozilla.org/):
    [About JavaScript](http://developer.mozilla.org/en/docs/About_JavaScript)
    includes JavaScript resources, complemented by
    [JavaScript Language Resources
    ](http://developer.mozilla.org/en/docs/JavaScript_Language_Resources)
    and the
    [Javascript main page](https://developer.mozilla.org/En/JavaScript).
    [Core JavaScript Reference](https://developer.mozilla.org/en/JavaScript/Reference),
    [Core JavaScript Guide](https://developer.mozilla.org/en/JavaScript/Guide),
    and a
    [re-introduction to JavaScript
    ](https://developer.mozilla.org/en/A_re-introduction_to_JavaScript).
-   [State Of JavaScript](http://stateofjs.com/) a survey  of current
    state of  JavaScript Flavors, front-end frameworks, full-stack
    frameworks, testing frameworks, state management, CSS Tools, build
    tools, mobile frameworks.

#  Javascript Guides and Tutorials
-   [Essential Javascript
    ](http://www.hunlock.com/blogs/Essential_Javascript_--_A_Javascript_Tutorial )
    is a javascript tutorial by Patrick Hunlock who offers many
    javascript howtos on his
    [blog](http://www.hunlock.com/blogs/).
-   [developper tutorials](http://www.developertutorials.com/):
    [Javascript tutorials](http://www.developertutorials.com/tutorials/javascript/)
-   Opera [Javascript section of Web Standards Curriculum
    ](http://dev.opera.com/articles/view/programming-the-real-basics/)
-   [Javascript References and Tutorials
    ](http://www.hunlock.com/) by Patrick Hunlock.
-   The [Javascript chapter
    ](https://runestone.academy/runestone/books/published/webfundamentals/Javascript/toctree.html)
    of [Fundamentals of Web Programming
    ](https://runestone.academy/runestone/books/published/webfundamentals/index.html)
    and [JavaScript for Python Programmers
    ](https://runestone.academy/runestone/books/published/JS4Python/index.html)
    are interactive courses from [Runestone Interactive Books
    ](https://runestone.academy/runestone/books/).
-   Douglas Crockford has written a couple of article very usefull to
    better understand the (lack of) design of javascript and its
    limitations:
    [JavaScript: The World's Most Misunderstood Programming Language
    ](http://javascript.crockford.com/javascript.html)
    and
    [The World's Most Misunderstood Programming Language Has Become the World's Most Popular Programming Language
    ](http://javascript.crockford.com/popular.html) _quite old 2001_
    he teach how to bypass the defects of Javascript in
    [The Elements of JavaScript Style One
    ](http://crockford.com/javascript/style1.html) and [two
    ](http://crockford.com/javascript/style2.html) _2005_

    His site host also
    [useful Javacript links](http://javascript.crockford.com/)

    He has written _JavaScript: The Good Parts_  This is not a
    reference book. but just contains important things  _O'Reilly 2008_.
    for learning Javascript he recommands _JavaScript: The Definitive
    Guide_ by   David Flanagan _6th edition 2011_.
    and the {{< iref "#jslint" "JSLint Home" >}} (see below).
-   {{< wp "JSDoc" >}} _(wikipedia)_ is a {{< wp "Javadoc" >}} simile for Javascript.


## Ajax

-   {{< wp "Ajax_(programming)"  "Ajax *(Wikipedia)*" >}}
    shorthand for _Asynchronous JavaScript and XML_, is a web
    development technique for creating interactive web applications.
    Ajax incorporates: standards-based presentation using XHTML and
    CSS; dynamic display and interaction using the Document Object
    Model; data interchange and manipulation using XML and XSLT;
    synchronous data retrieval using
    [XMLHttpRequest *(Wikipedia)*
    ](http://en.wikipedia.org/wiki/XMLHttpRequest)
    ; and JavaScript binding everything together.
-   An {{< wp "Ajax framework" >}} is a web application framework that  provide the
    {{< wp "Ajax (programming)"  "Ajax" >}} engine and
    associated server and client-side functions. It may be a
    {{< wp "Ajax framework#Direct_Ajax_frameworks"  "direct framework" >}}
     when it only provides the basic Ajax components or an
    {{< wp "Ajax framework#Indirect_Ajax_frameworks"  "indirect framework" >}} when the Ajax code
    is generated from the translation of an high level language.
    {{< wp "List_of_Ajax_frameworks"  "Wikipedia list of Ajax frameworks" >}}.


# Javascript tools
-   [JsDoc3 Toolkit](https://github.com/jsdoc3/jsdoc)
    is an application, written in JavaScript, for automatically
    generating template-formatted, multi-page HTML (or XML, JSON, or
    any other text-based) documentation from commented JavaScript
    source code.
-   <a name="jslint"></a>[JSLint](http://www.jslint.com/l)
    is a _lint_ code quality tool
    for javascript.  JSLint check against a strict subset of
    [Ecma-222 ECMAScript Language Specification, 3rd edition
    ](http://www.ecma-international.org/publications/standards/ECMA-262.HTM)
    and follow the recommendations found in
    [Code Conventions for the JavaScript Programming Language
    ](http://javascript.crockford.com/code.html).
    JSLint can operate on JavaScript source, HTML source, CSS source,
    or JSON  text.<br />
    The conventions are summarized in the
    [JSLint instructions page](http://www.jslint.com/lint.html);
    it is very usefull when writting Javascript to make sure you
    follow them, since Javascript makes easy to write clumsy code with
    hidden errors
-   [MozRepl](https://github.com/bard/mozrepl/wiki)
    is a Read-eval-print loop for javascript under Mozilla.
    It [integrates with emacs
    ](https://github.com/bard/mozrepl/wiki/emacs-integration/)
-   [CodeMirror](.https://github.com/marijnh/CodeMirror)
    is a  text editor implemented in JavaScript for the browser
-   [Editing JavaScript in Emacs
    ](http://edward.oconnor.cx/2005/09/editing-javascript-in-emacs)
    by [Edward 0'Connor](http://edward.oconnor.cx)
    being written in 2005 it does not mention the new packages.
    You find them in
    [EmacsWiki: JavaScriptMode](http://www.emacswiki.org/emacs/JavaScriptMode).
    The javascript mode from Karl Landstrom, enhanced by Daniel
    Colascione, _also known as expresso_ is available in emacs > 23.2
    as __js.el__.

## Other web scripting languages

-   {{< wp "CoffeeScript" >}} is a programming language  inspired by Ruby, Python and Haskell
   that compiles to JavaScript. It add features like list
   comprehension and pattern matching.
   -   [Coffeescript Home](http://coffeescript.org/).
   -   [Cofeescript GitHub repository
       ](https://github.com/jashkenas/coffeescript)
-   {{< wp "Elm" >}} is a purely functionnal language aimed at web user
    interfaces. It enforces  static type checking. Elm compiler
    generates HTML, CSS, and JavaScript
    -   [An Introduction to Elm](https://guide.elm-lang.org/)
    -   [Elm FAQ](http://faq.elm-community.org/)
-   {{< wp "Dart" >}} is a class-based, single inheritance, object-oriented language
    with C-style syntax developed by Google. It supports interfaces,
    abstract classes, reified generics, and optional typing.
-   {{< wp "Haxe" >}} (GPL) is a programming language, for creating interactive
    web applications it generates code in five targets: Adobe Flash,
    JavaScript, PHP, C++ and the Neko VM.
    [Haxe Home](http://haxe.org/)


# Javascript frameworks.
## References
-   Wikipedia: {{< wp "Comparison of JavaScript frameworks" >}} with detailed list of features,
    {{< wp "List of JavaScript libraries" >}}, {{< wp "Ajax framework" >}}, {{< wp "Ajax_(programming)"  "Ajax_programming" >}}.
-   Wikipedia: {{< wp " List of rich Internet application frameworks" >}},
    {{< wp "Multiple phone web-based application framework" >}},
-   [ToDo MVC](http://todomvc.com/) is a comparison of JavaScript MVC frameworks
    with a single example application implemented on each of them. It help to
    *decide on which to use in a sea of so many options*.
    The [source is in GitHub](https://github.com/addyosmani/todomvc).
-   [speed/validity selectors test for framework](http://mootools.net/slickspeed/)
    compare MoTools, JQuery, Prototype, YUI, Dojo.

-   {{< wp "AngularJS" >}} (MIT License) is a javascript framework by Google
    for developing {{< wp "single-page applications" >}}. It provides a
    framework for client-side {{< wp "model–view–controller" >}} (MVC) and
    {{< wp "model–view–viewmodel" >}} (MVVM) architectures.
    -   [AngularJS Home](https://angularjs.org/).
    -   [AngularJS 2.x Home](https://angular.io/).
    -   [W3school AngularJS Tutorial
        ](http://www.w3schools.com/angular/).
    -   [AngularJS vs. Backbone.js vs. Ember.js
        ](https://www.airpair.com/js/javascript-framework-comparison).
-   {{< wp "Backbone.js" >}} (MIT License) is a JavaScript library designed for
    developing {{< wp "single-page web applications" >}}. It features a RESTful
    JSON interface based on the {{< wp "model–view–presenter" >}}
    paradigm. Backbone is lightweight and depends only on
    [Underscore.js](http://underscorejs.org/).
    -   [Backbone.js Home](http://backbonejs.org/)
-   {{< wp "Ext JS" >}}  (GPL or commercial) by
    [Sencha](http://www.sencha.com/)
    is a pure JavaScript application framework interoperable with jQuery and Prototype.
    [Ext JS Home](http://www.sencha.com/products/extjs/)
-   {{< wp "Google Web Toolkit" >}} (GWT) (Apache License) allows to create and maintain
     complex JavaScript front-end applications in Java.
-   {{< wp "Midori_Javascript_Framework"  "Midori" >}} (MIT License)
-   {{< wp "Moo Tools" >}} (MIT License) is a Javascript framework using the OO model.
    [Mootol sHome](http://mootools.net/).
    -   [Mootools templated](https://github.com/darkwing/Templated)
        (MIT License) is a JavaScript template system for Mootols.

## Mobile development frameworks
-   {{< wp "PhoneGap" >}}  (Apache License) is a mobile development framework
-   {{< wp "Sencha Touch" >}} (GPLv3 or commercial)
    is a user interface JavaScript HTML5  framework, built for the Mobile Web.
    [Sencha Touch Home](http://www.sencha.com/products/touch)

# Javascript all purpose Libraries
-   Wikipedia: {{< wp "List of JavaScript libraries" >}},

## Dojo
{{< wp "Dojo_Toolkit"  "Dojo" >}} (BSD License and Academic Free Licence)
 provides asynchronous communications, and client and server storage.

-   [Dojo Toolkit Home](http://dojotoolkit.org/)
-   [Dojo resources](http://www.ibm.com/developerworks/web/tutorials/wa-dojotoolkit/resources.html)
    by Joe Lennon.
-   [Ibm Developer Work: Dojo from the ground up](http://www.ibm.com/developerworks/views/web/libraryview.jsp?contentarea_by=Web+development&search_by=dojo+ground+up)
-   [Consuming web services with the Dojo Toolkit](http://www.ibm.com/developerworks/web/library/wa-aj-consume/)
by Nathan A. Good.
-   [Build an Ajax application with the Dojo Toolkit](http://www.ibm.com/developerworks/web/tutorials/wa-dojotoolkit/wa-dojotoolkit-pdf.pdf)
bye Joe Lennon.
-   [Dojo Boilerplate](https://github.com/csnover/dojo-boilerplate):
    A Starter Kit for Dojo Development, and [Dojo Demo](https://github.com/rmurphey/dojo-demo):
    Dojo Toolkit for MVC JavaScript applications by Rebecca Murphey.


## Node.js {#node_js}
{{< wp "Node.js" >}} is a javascript library designed for writing scalable
Internet applications, notably web servers.  Node is similar in design
to Ruby's Event Machine or Python's Twisted.  Programs are written on
the server side in JavaScript, using event-driven, asynchronous I/O.

-   [Node.js Documentation](http://nodejs.org/docs/latest/api/index.html)
-   [npm -- node package manager](http://npmjs.org/) is a package
    manager for node.  [GitHub: npm](https://github.com/isaacs/npm).
-   [Ender](http://ender.no.de/) is a javascript package manager to
    search, install, manage, and compile front-end javascript packages
    and their dependencies.

## JQuery {#jquery}
### References
{{< wp "jQuery" >}} (MIT license) is a cross-browser JavaScript library extensible through
the use of [plugins](http://plugins.jquery.com/), {{< wp "jQuery UI" >}} provides widgets
and effects on the top of jQuery, {{< wp "jQuery Mobile" >}} is a a mobile framework developed by the jQuery team.

-   [jQuery Documentation Index](http://docs.jquery.com/Main_Page)
-   [Tutorials:How jQuery Works](http://docs.jquery.com/How_jQuery_Works)
-   [Tutorials:Getting Started with jQuery](http://docs.jquery.com/Tutorials:Getting_Started_with_jQuery)
-   [Using jQuery with Other Libraries](http://docs.jquery.com/Using_jQuery_with_Other_Libraries)
-   [jQuery Fundamentals](http://jqfundamentals.com/book/index.html) an ebook by Rebecca Murphey,
    it is the base of [web-learn-jquery-com](https://github.com/jquery/web-learn-jquery-com)
    and the original author now seems to switch to Dojo, see above the Dojo boilerplate.
-   [LearninJquery](http://www.learningjquery.com/)
    Tips, techniques, and tutorials for the jQuery JavaScript library.
-   [developertutorials - javascript collection
    ](http://www.developertutorials.com/tutorials/javascript/):
    -   [A Quick Introduction to JQuery – Part 1
        ](http://www.developertutorials.com/tutorials/javascript/a-quick-introduction-to-jquery-part-1-2594/),
        [Get Rolling With jQuery – Part 2
        ](http://www.developertutorials.com/tutorials/javascript/rolling-with-jquery-part-2-2604/)
        and [Part 3
        ](http://www.developertutorials.com/tutorials/javascript/get-rolling-with-jquery-part-3-2774/)
        by Larry Schoeneman.
    -   [Getting Started with AJAX in jQuery
        ](http://www.developertutorials.com/tutorials/ajax/getting-started-with-ajax-in-jquery-874/)
        by Akash Mehta
-   [Ibm Developer Work: Working with jQuery
    ](http://www.ibm.com/developerworks/views/web/libraryview.jsp?search_by=working+with+jquery:)
-   [Intro to Unintrusive JavaScript with Django
    ](http://dev.lethain.com/intro-to-unintrusive-javascript-with-django/) and
    [Custom Django Views for Happier Ajax
    ](http://dev.lethain.com/custom-django-views-for-happier-ajax/)
    by Will Larson
-   [jQuery Mobile](http://jquerymobile.com/) (MIT License)
    is an unified, touch-friendly, user interface system across all
    popular mobile device platforms, built on jQuery and jQuery UI.
    -   [jQuery Mobile Introduction
        ](http://view.jquerymobile.com/demos/intro/)
    -   [jQuery Mobile Demo site](http://view.jquerymobile.com/)
    -   [jQuery Mobile GitHub](https://github.com/jquery/jquery-mobile)
-   [Zepto](http://zeptojs.com/) (MIT License) is a minimalist
    JavaScript library for modern browsers with a largely
    jQuery-compatible API.  It is compatible with most of desktop
    __and mobile__ browsers.

### jQuery plugins
[The jQuery Plugin Registry](http://plugins.jquery.com/)
is an index of GitHub repositories that contain jQuery plugins.

I reference some JQuery plugins in the
{{< iref "#javascript_libraries" "Javascript Libraries section" >}}

# React.js {#reactjs}

{{< wp "React.js" >}}  is a JavaScript library for building user interfaces. It is
maintained by Facebook.
React can be used as a base in the development of single-page or mobile applications.

-   [React Home](https://reactjs.org/)
-   [Awesome React](https://github.com/enaqx/awesome-react)
-   [React How To](https://github.com/petehunt/react-howto)
-   <a name="jsx"></a>{{< wp "React_(web_framework)#JSX" "JSX" >}}, or JavaScript XML ,
    is an extension to the JavaScript language syntax
-   [Introducing JSX – React](https://reactjs.org/docs/introducing-jsx.html)

## Other Libraries
-   {{< wp "MochiKit" >}} was used in TurboGears and many python frameworks,
    it is no more in active development.
    -   [Mochikit Home Page on GitHub](http://mochi.github.com/mochikit/).



# Javascript libraries {#javascript_libraries}
## Libraries lists
-   [JSAN - JavaScript Archive Network](http://openjsan.org/)
    is a comprehensive resource for Open Source JavaScript libraries and software.
-   [Javascript Toolbox](http://www.javascripttoolbox.com/)
    repository of code and reusable libraries written by Matt Kruse.
-   [The jQuery Plugin Registry](http://plugins.jquery.com/)
    is an index of GitHub repositories that contain jQuery plugins.
-   [CodeMirror](http://codemirror.net/)
    is a JavaScript component that provides a code editor in the
    browser.
    [CodeMirror GitHub repository](https://github.com/marijnh/CodeMirror).

## Javascript encryption {#js_encrypt}
Read first
[Javascript Cryptography Considered Harmful
](http://www.matasano.com/articles/javascript-cryptography/)

-   [CryptoJS](http://code.google.com/p/crypto-js/)
    is a collection of cryptographic algorithms implemented in JavaScript.
    it includes  the following cyphers: AES-128, AES-192, AES-256, DES, Triple DES, Rabbit,
    RC4, RC4Drop and hashers: MD5, RIPEMD-160,
    SHA-1, SHA-256, SHA-512, SHA-3 with 224, 256, 384, or 512 bits.
    [node-cryptojs-aes](https://npmjs.org/package/node-cryptojs-aes)
     is a node.js port of _crypto-js_
-   [Gibberish AES](https://github.com/mdp/gibberish-aes)
    is a Javascript library for OpenSSL compatible AES encryption.
    It is a development of the [javascript aes library
    ](http://www.movable-type.co.uk/scripts/aes.html) by  Chris Veness.
-   [jsaes](http://point-at-infinity.org/jsaes/) (GPL) is a JavaScript
    implementation of the AES block cipher. Key lengths of 128, 192
    and 256 bits are supported.
-   [Stanford Javascript Crypto Library
    ](http://bitwiseshiftleft.github.io/sjcl/) (GPL)
    uses AES algorithm at 128, 192 or 256 bits, SHA256 hash function;
    the HMAC authentication code; the PBKDF2 password strengthener;
    and the CCM and OCB authenticated-encryption modes. The source
    is [hosted at GitHub](https://github.com/bitwiseshiftleft/sjcl).

## Tables

-   [33 JavaScript Solutions for Sorting Tables
    ](http://tympanus.net/codrops/2009/10/03/33-javascript-solutions-for-sorting-tables/)
    _article from 2009, there is now some new libraries._
-   [DataTables ](http://www.datatables.net/) (Dual GPL and BSD
    Licenses)
    a plug-in for jQuery, that add multiple filtering, and paginations
    options to tables.
-   {{< wp "Dhtmlx" >}} (GPL or commercial)
    a standalone library written in pure JavaScript and CSS
    including many UI components, data grids, spreadsheets, events calendar, or scheduler,
    navigation with treemenu or menu or tabs...
-   [js-tables](http://code.google.com/p/js-tables)
    (Apache License 2.0) provides `jquery.csv.js` to convert csv files
    into array of arrays, and `query.table.js` to show an interactive
    table with filters.
-   [stackable.js](http://johnpolacek.github.com/stacktable.js/)
    (Dual MIT & GPL licenses) is a jQuery plugin for stacking tables on
    small screens.
    [GitHub Repository](https://github.com/johnpolacek/stacktable.js/)
-   [table.js](http://www.javascripttoolbox.com/lib/table/index.php)
    (Dual MIT and GPL Licenses) add sorting ang pagination.

## Tree view
### jQuery
-   We can display a Tree View in CSS3 without any javascript as
    explained in
    [CSS3 Treeview. No JavaScript
    ](http://acidmartin.wordpress.com/2011/09/26/css3-treevew-no-javascript/)
    by Martin Ivanov.
-   [fancytree](https://github.com/mar10/fancytree)
    Tree plugin for jQuery with support for persistence, keyboard,
    checkboxes, tables (grid), drag'n'drop, and lazy loading.
-   [jsTree](http://www.jstree.com/) (MIT License)
-   [nestedSortable](https://github.com/ilikenwf/nestedSortable)
    (MIT License)
-   [jqueryui_btechco_tree
    ](https://github.com/btechco/jqueryui_btechco_tree)
    (MIT License)
    A jQuery-ui compatible tree control.
-   [Multi Level Hierarchical jQuery Menu: jQSimpleMenu
    ](https://github.com/mshahbazsaleem/jQSimpleMenu/wiki/Multi-Level-Hierarchical-jQuery-Menu:-jQSimpleMenu)
    (GPL) by Muhammad Shahbaz Saleem

### other ajax tree views
_Not Jquery_

-   [dhtmlgoodies: folder trees
    ](http://www.dhtmlgoodies.com/index.html?page=folderTree) (LGPL)
-   [Dhtmlx JavaScript Tree Menu
    ](http://www.dhtmlx.com/docs/products/dhtmlxTree/) (GPL or
    commercial)

### Images and Video
-   {{< wp "Lightbox" >}} (MIT License)
    is a JavaScript library that displays images and
    videos by filling the screen, and dimming out the rest of the web
    page.

    -   [Lightbox2 Home](http://lokeshdhakar.com/projects/lightbox2).
    -   [Slimbox 2] is a 4 KB visual clone of Lightbox2 , written
        using the jQuery javascript library. It is compatible with the
        original Lightbox. It offers added features and options
        Slimbox 2 is compatible with Firefox 2+, Internet Explorer 6+,
        Opera 9+ and Opera for Wii, Safari 3+, Camino and Google
        Chrome.


## Not yet classified
-   [MarkitUp](http://markitup.jaysalvat.com/home/)
    is a JQuery editor that can  turn any textarea into a markup editor. Html, Textile, Wiki Syntax,
    Markdown, BBcode or
    [Org-Mode with the orgitdown extension](https://github.com/gnowgi/orgitdown).
    -   MarkitUp can be   integrated in django with
        [django-markitup](https://pypi.python.org/pypi/django-markitup/)
-   [e-math calculator](https://github.com/e-math/calculator) is a Jquery
    embedable calculator.
-   {{< wp "Electron" >}} Electron is a framework for creating native
    applications with web technologies like JavaScript, HTML, and CSS.
    -   [Electron Home](https://electron.atom.io/)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
