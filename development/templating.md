---
title: Templating engines
---

See also {{< iref "python/python_web" "Python Web" >}}.

----

# General references

A popular category of template engine is _logic-less_ template engines
that have no control flow statements, all control are driven by data.
In this category you find {{< iref "#mustache" "Mustache" >}},
c-template, {{< iref "#handlebars" "Handlebars" >}}, {{< iref "#dustjs" "Dust.js" >}}.

An other important characteristic of templating language is template
inheritance, which is available in
{{< iref "#jinja2" "jinja2" >}},
{{< iref "#pug" "pug" >}},
{{< iref "#nunjucks" "Nunjucks" >}},
some mustache implementations implementing the
[template inheritance proposal
](https://github.com/mustache/spec/pull/75) like
{{< iref "#hogan" "Hogan" >}}, and _hxmustache_.

Template inheritance allows you to build a base “skeleton” template
that contains some blocks that child templates can override.
You find more explanation in [Flask: Template Inheritance
](https://flask.palletsprojects.com/en/1.1.x/patterns/templateinheritance/).

-   The Wikipedia page {{< wp "Template_engine_(web)"  >}}
    includes a list of templates engines, it is accompanied by a
    {{< wp "Comparison of web template engines" >}}.
-   [Comparing  node.js template engines: Jade, Mustache, Dust, Nunjucks, EJS
    ](https://developer.ibm.com/node/2014/11/11/compare-javascript-templates-jade-mustache-dust/)
    _2014_.

# Logicless templates

-   <a name="mustache"></a>[Mustache](http://mustache.github.io/)
    (MIT License)
    is a _logic-less_ template language. It is Available in Ruby,
    JavaScript, Python, Erlang, Elixir, PHP, Perl, Perl6, Objective-C,
    Java, C#/.NET, Android, C++, CFEngine, Go, Lua, ooc, ActionScript,
    ColdFusion, Scala, Clojure[Script], Fantom, CoffeeScript, D,
    Haskell, XQuery, ASP, Io, Dart, Haxe, Delphi, Racket, Rust, OCaml,
    Swift, Bash, Julia, R, Crystal, Common Lisp, Nim, Smalltalk, Tcl,
    C, ABAP, and  Elm.
    -   [Mustache Demo](http://mustache.github.io/#demo)
    -   [Mustache Manual](http://mustache.github.io/mustache.5.html)
    -   [Pystache (GitHub repo.)](https://github.com/defunkt/pystache)
        is the Python implementation of Mustache. It has support for py3k.
    -   [Mustache.el](https://github.com/Wilfred/mustache.el)
        a mustache templating library in Emacs Lisp.
    -   [mustache.js](https://github.com/janl/mustache.js) -
        templating with {{mustaches}} in JavaScript.
    -   <a name="hogan"></a>[hogan.js
        ](https://github.com/twitter/hogan.js) -
        A Node compiler for the Mustache templating language. Hogan
        compiles templates to HoganTemplate objects, which have a
        render method. Hogan also supports template inheritance.
    -   [hxmustache](https://github.com/nadako/hxmustache/)
        is an Haxe implementation of Mustache
        [supporting template inheritance
        ](https://github.com/nadako/hxmustache/blob/master/README.md#template-inheritance).
-   <a name="handlebars"></a>
    {{< wp "Mustache_%28template_system%29#Handlebars"  "Handlebars" >}} is an
    extension de {{< iref "#mustache" "Mustache" >}} writen in
    node.js.
    -   [Handlebars Home](http://handlebarsjs.com/)
    -   [Handlebars Github](https://github.com/wycats/handlebars.js)
        explain the extensions made to
        {{< iref "#mustache" "Mustache" >}}.
    -   [Handlebars helpers](http://assemble.io/helpers/)
        a list of more than 130 helpers for handlebars.
    -   [GitHub: Handlebars helpers
        ](https://github.com/assemble/handlebars-helpers)

-   <a name="dustjs"></a>[dust.js](http://www.dustjs.com/)
    is a logicless asynchronous template enginefor the browser and
    node.js..
    -   [Dust.js - GitHub] https://github.com/linkedin/dustjs)
-   {{< iref "#slim" "Slim" >}} that you find
    {{< iref "#slim" "below" >}} has a [logic-less mode
    ](http://www.rubydoc.info/gems/slim/file/doc/logic_less.md)
    inspired by Mustache.

# main logic templating engines

-   <a name="jinja2"></a>[Jinja2](https://www.palletsprojects.com/jinja/)
    (BSD license) is a Python template engine similar to the
    {{< iref "python/python_web#django" "Django" >}}
    template engine.  It can be used to generate any markup as well as
    sourcecode.
   
    -   [jinja2 documentation](https://jinja.palletsprojects.com/)
    -   [Jinja Tutorial
        ](https://ttl255.com/jinja2-tutorial-part-1-introduction-and-variable-substitution/)
        in 6 parts by Przemek Rogala.
   
    There are many jinja2/django derived processors:
    -   The web framework [Django](http://www.djangoproject.com/) (BSD
        License) includes a template language similar to
        {{< iref "#jinja2" "jinja2" >}}.
    -   [jinja2-cli](https://github.com/mattrobenolt/jinja2-cli) (BSD License)a
        is a CLI interface to Jinja2.
    -   [j2-cli](https://github.com/kolypto/j2cli)  (BSD License)
        is a command-line tool for templating in shell-scripts, leveraging the Jinja2 library.a
    -   [pongo2](https://github.com/flosch/pongo2)  (MIT License)
        is a Django-syntax like template-engine for Go. 
    -   [tera](https://github.com/Keats/tera) (MIT License)
        is a  template engine for Rust based on Jinja2/Django. 
    -   <a name="nunjucks"></a>[Nunjucks](http://mozilla.github.io/nunjucks/)
        is a javascript templating engine inspired by {{< iref "#jinja2" "Jinja2" >}}.
        Nunjucks support [template inheritance
        ](http://mozilla.github.io/nunjucks/templating.html#template-inheritance).
        -   [Nunjucks templating Doc](http://mozilla.github.io/nunjucks/templating.html)
        -   [Nunjuck GitHub](https://github.com/mozilla/nunjucks)
-   [Go text template](https://pkg.go.dev/text/template) and
    [Go html template](https://pkg.go.dev/html/template) are in the standard go library.
-   <a name="pug"></a>[Pug](https://pugjs.org/) (MIT License)
    _formerly known as Jade_ is a _node.js_, _tag-free_ template
    engine derived from Haml.  It is similar to
    {{< iref "#slim" "Slim" >}}.
    Pug support [template inheritance
    ](https://pugjs.org/language/inheritance.html).
    -   [GitHub Pug](https://github.com/pugjs/pug)
    -   [Pug official documentation
        ](https://pugjs.org/api/getting-started.html).
    -   [Interactive Jade Syntax Documentation by example
        ](http://naltatis.github.com/jade-syntax-docs/) allow to learn
        Pug and test your code.
    -   [PyPugjs (GitHub)](https://github.com/kakulukia/pypugjs)
        is the python port of Pug. _PyPugjs_ can
        convert any Pug source to Django, Jinja2, Mako or
        {{< iref "#tornado" "Tornado template" >}}.
    -   [GitHub: eknc/pug](https://github.com/eknkc/pug) (MIT License)
        is a port to Go of Pug template engine, it compiles templates to
        standard [go templates](https://golang.org/pkg/html/template/).
        _no longer developed since 2018, in this repo, but continued in
        [knaka/pug](https://github.com/knaka/pug)._
-   <a name="slim"></a>[Slim](http://slim-lang.com/) (MIT license)
    is a _tag-free_ Ruby templating language, derived from _HAML_. There are also port
    to _Python_, _javascript_ with _Coffee script_, _Clojure_. _Slim_ is similar to
    {{< iref "#pug" "Pug" >}}.  It allows to embed other generators like Markdown.  A
    plugin implement also a
    [logic-less mode](http://www.rubydoc.info/gems/slim/file/doc/logic_less.md)
    inspired by Mustache.
    -   [Skim (GitHub)](https://github.com/appjudo/skim) (MIT License)
        is the Slim templating engine with embedded CoffeeScript. It compiles to
        JavaScript templates (.jst), which can then be served by Rails
    -   [Plim (GitHub)](https://github.com/avanov/Plim) is a Python port Slim
        built on top of {{< iref "#mako" "Mako Templates" >}}
        It uses Mako's preprocessor feature to translate its syntax
        into a valid HTML/Mako markup.
    -   [Slm (GitHub)](https://github.com/slm-lang/slm) (MIT License)
        is a Node javascript implementation of _Slim_ it is among the quicker node
        templating system, with a comparable speed to ECT and Hogan.
-   <a name="twig"></a>[Twig](https://twig.symfony.com/) (BSD License)
    is a PHP template engine similar to
    {{< iref "#jinja2" "Jinja2" >}}
    -   {{< wp "Twig_(template_engine)"  "Wikipedia: Twig" >}} gives the syntax
        essentials.
    -   [Twig.js](https://github.com/twigjs/twig.js)
        javaScript implementation of Twig.
-   <a name="haml"></a>{{< wp "HAML" >}} (MIT License)
    is a ruby templating language which inpired many newer templating
    languages like _Pug_, _Nunjuck_, _jinja2_,or _Slim_.
    -   [HAML Home](http://haml.info/)
    -   [GitHub: HAML](https://github.com/haml/haml)
    -   [haml-js](https://github.com/creationix/haml-js)
        a node javascript implementation of Haml.
    -   [haml.js](https://github.com/tj/haml.js/)
        Haml JavaScript implementation for nodejs.
     -  [haml-coffee](github.com/netzpirat/haml-coffee)
         compile HAML to coffeescript.

## Javascript _only_ templating
There are many transformers in Node javascript, including templating sytems
structured text compilers, and beautifiers, each one with a
different API, [jstransformer
](https://github.com/jstransformers/jstransformer)
is a middleware that unifies them into one standardized API.
The [list of jtransformer packages
](https://www.npmjs.com/browse/keyword/jstransformer) give the list of
supported backends.

-   [doT](https://github.com/olado/doT) - The fastest + concise
    javascript template engine for nodejs and browsers.
-   [eco](https://github.com/sstephenson/eco/) - Embedded CoffeeScript
    templates.
-   [JavaScript-Templates](https://github.com/blueimp/JavaScript-Templates) -
    < 1KB lightweight, fast & powerful JavaScript templating engine
    with zero dependencies.
-   [t.js](https://github.com/jasonmoo/t.js) - A tiny javascript
    templating framework in ~400 bytes gzipped.
-   [EJS](https://github.com/mde/ejs) - Effective JavaScript
    templating.
-   [xtemplate](https://github.com/xtemplate/xtemplate) - eXtensible
    Template Engine lib for node and the browser
-   [marko](https://github.com/marko-js/marko) - A fast, lightweight,
    HTML-based templating engine for Node.js and the browser with
    async, streaming, custom tags and CommonJS modules as compiled
    output.

# Python _only_ templating
See also {{< iref "python/python_web" "Python Web" >}}.

-   [Templating in Python](http://wiki.python.org/moin/Templating)
    in the python wiki gives a list of python templating engines and
    web frameworks.

-   [Cheetah 3](http://www.cheetahtemplate.org/)  (MIT License)
    is a template engine that uses Python It is used for server-side scripting and to
    generate source code.
-   [empy](http://www.alcyone.com/software/empy/)
    (LGPL) is a templating system for Python. It is quite different
    from the more usual template syntax. EmPy can expand arbitrary
    Python expressions and statements enclosed by some special
    delimiter like `@`.
-   [Genshi](http://genshi.edgewall.org/) (BSD  like license)
    defines itself as a Python toolkit for stream-based generation of output for the
    web. It has replaced the older  {{< wp "Kid_(templating_language)"  "Kid" >}}
-   <a name="mako"></a>[Mako](http://www.makotemplates.org/) (MIT License)
    is a template library written in Python. Mako is used as a Python Server Page
    language. _Mako_ was previously named _Mighty_.  Mako is used by reddit.com and is
    the default template language for the
    {{< iref "python/python_web#pylon" "Pylons and Pyramid web frameworks" >}}.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
