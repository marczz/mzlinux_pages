<!--
.. description:
.. date: 2010-01-19
.. slug: markdown
.. tags:
.. link:
.. book: mzlinux
.. title: MarkDown
-->

[TOC]

# [w:Markdown]

-   [Markdown](http://daringfireball.net/projects/markdown/)
    (BSD style license) is a text-to-HTML conversion tool originaly
    written in perl, but that has also implementations in C, python, php,
    haskell, lua. Markdown can be used in many CMS _often thru plugins_
    Instiki Wiki (ruby powered wiki), ikiwiki. dokuwiki,
    [Moinmoin](http://moinmo.in/), [WolfCms](http://www.wolfcms.org/),
    [Gollum](/node/116/#gollum "internal reference").
    It is widely used in Django
    powered applications _using the python implementation_.

    It is the most usual syntax for
    [Static site generators](node/static_site/ "internal reference")
    and used in
    [Awestruct](/node/static_site/#awestruct "internal reference"),
    [BlackSmith](/node/static_site/#blacksmith "internal reference"),
    [Bonsai](/node/static_site/#bonsai "internal reference"),
    [Docpad](node/static_site/#docpad "internal reference")
    [Chisel](/node/static_site/#chisel "internal reference"),
    [Codex](/node/static_site/#codex "internal reference"),
    [elyse](/node/static_site/#elyse "internal reference"),
    [Growl](/node/static_site/#growl "internal reference"),
    [Gollum-site](/node/static_site/#gollumsite "internal reference"),
    [Jekyll](/node/static_site/#jekyll "internal reference"),
    [Hakyll](/node/static_site/#hakyl "internal reference"),
    [Hyde](/node/static_site#hyde "internal reference"),
    [liquidluck](/node/static_site/#liquidluck "internal reference"),
    [MarkDoc](node/static_site/#markdoc "internal reference"),
    [MarkWiki](/node/static_site/#markwiki "internal reference"),
    [Middleman](/node/static_site/#middleman "internal reference"),
    [Mynt](/node/static_site/#mynt "internal reference"),
    [nanoc](/node/static_site/#nanoc "internal reference"),
    [Nib](/node/static_site/#nib  "internal reference"),
    [Nikola](/node/static_site/#nikola  "internal reference"),
    [Pelican](/node/static_site/#pelican "internal reference"),
    [poole](/node/static_site/#poole "internal reference"),
    [Ruho](/node/static_site/#ruhoh "internal reference"),
    [simple-static](/node/static_site/#simple_static "internal reference"),
    [sw](/node/static_site/#sw "internal reference"),
    [werc](/node/static_site/#werc  "internal reference")
    [Wintersmith](/node/static_site/#wintersmith "internal reference"),
    [Wok](/node/static_site/#wok "internal reference").

-   [markdown mailing list at Gmame
    ](http://dir.gmane.org/gmane.text.markdown.general)
-   A detailed references page [XBeta Wiki: Markdown
    ](http://xbeta.org/wiki/show/Markdown)
-   [DropPages](http://droppages.com/) is a site that allows to put a static site
    written in markdown in your DropBox.
-   [tpl4md](https://github.com/dloureiro/tpl4md) (AGPL)
    by David Loureiro is a set of markdown templates for widely used
    documents like letters, invoices, orders, slides.

# Markdown Editing
[Emacs Markdown Mode](http://jblevins.org/projects/markdown-mode/)
by Jason Blevinsis the standard major mode for editing Markdown
formatted text with Emacs.

Markdown Mode can export the buffer to html and preview it (key
`C-c C-c v`). Live Export (`C-c C-c l`) turn on
markdown-live-preview-mode to view the exported output side-by-side
with the source Markdown. By default the preview is done in Emacs eww
mode.

There are also packages to preview the saved buffer like
[Markdown preview mode
](https://github.com/ancane/markdown-preview-mode) in melpa.



[chitsaou/copy-as-markdown](https://github.com/chitsaou/copy-as-markdown)
is a firefox and Chromium extension to  make opying Link, Image and
Tab(s) as Markdown much easier.



# Markdown Syntax
The original [Markdown syntax
](http://daringfireball.net/projects/markdown/syntax)
is summarized in the
[dingus - Markdown on-line converter
](http://daringfireball.net/projects/markdown/dingus),

As the syntax of markdown was only given by informal free text
description, there are many ambiguities that are solved in a different
way by each parser, and numerous extensions.

There are many extensions to markdown such as tables, footnotes,
definition lists,  Markdown inside HTML blocks, source code
higlighting.
Most extensions are bound to one parser and their syntax is given by
the parser manual. See below for each parser. The
[Pandoc](#pandoc "internal reference") extensions are widely used,
but many are specific to Pandoc.

At least three extensions are quite widespread and many parsers try to
implement them

-   The Older one is
    [php markdown extra](#php-markdown-extra "internal reference")
    that add: Inline HTML, Markdown Inside HTML Blocks,
    Special Attributes, Fenced Code Blocks with <code>~~~</code>,
    Tables, Definition Lists,
    Footnotes, Output, Abbreviations, Emphasis, Backslash Escapes.<br />
    [Python-markdown](#python-markdown "internal reference")group the
    same features in
    [python-markdown-extra](#python-markdown-extra "internal reference");
    and add a rich set of custom extensions.
    <br />
    The other extensions use to build up on markdown extra and extend
    it.
-   [Stack Overflow MarkDown](http://stackoverflow.com/editing-help)
    is a very standard MarkDown with some additiosn whose main is
    [Syntax highlighting for code
    ](http://stackoverflow.com/editing-help#syntax-highlighting)
    that uses [Google prettify
    ](http://google-code-prettify.googlecode.com/svn/trunk/README.html)
-   [Github Flavored Markdown - GFM](https://github.github.com/gfm/)
    is a very popular extension. The main difference is in Stantard
    Markdown newline are ignored and in GFM they are significative.
    GFM disable also disble italicize parts of words, allow
    strikethrough, fenced code block with <code>&#96;&#96;&#96;</code>
    syntax higlighting with <code>&#96;&#96;&#96;python</code> like headers,
    task lists, and few GitHub specific shortcuts.
    -   [GitHub Help: Mastering markdown
        ](https://guides.github.com/features/mastering-markdown/)
        is an howto for
        [Github Flavored Markdown](https://github.github.com/gfm/).
-   [Pandoc Markdown](http://pandoc.org/MANUAL.html#pandocs-markdown)
    include a set of extensions of MarkDown:

    basic formatting
    :   _escaped line breaks_ with backslash before a newline, _auto
        identifiers_ and _implicit header references_ for headers,
        _all symbols escapable_ extend the backslash mecanism of
        standard markdown, to any punctuation or whitespace, and use
        a backslash followed by a newline to introduce a paragraph
        break, _intraword underscores_, _strikeout_, _superscript_,
        _subsript_, _small caps_,
    blocks
    :   require _a blank line before a block quote_,
        _fenced code blocks_,
        _backtick code block_,
        attach attributes to fenced, backtick and inline code block with
        _fenced code attributes_ and _inline code attributes_,
        _line block_ with a sequence of lines beginning with a vertical
        bar, _table captions_,
        _simple tables_, _multiline tables_,  _grid tables_ wich are alike
        emacs tables, _pipe tables_ like PHP markdown axtra tables,
        _pandoc title bloc_ to give bibliographic information, _yaml
        metadata blocks_.
    lists
    :   _startnum_ for ordered lists, _fancy list_ can be marked with a
        ``#``, _definition lists_,  _example lists_.

-   [Babelmark2](http://johnmacfarlane.net/babelmark2/) compare the rendering
    of various markdown formatters.
    -   [Babelmark2 FAQ](http://johnmacfarlane.net/babelmark2/faq.html)

## CommonMark
[CommonMark](http://commonmark.org/) is a formal specification of
(a flavor of) MarkDown language by John Mac Farlane.

John Mac Farlane previously produced many markdown parsers like
[pandoc](#pandoc) or [peg-markdown](#peg-markdown).

The [specification](http://spec.commonmark.org/) has its [source
on GitHub](http://spec.commonmark.org/). There is also a
[reference card](http://commonmark.org/help/) and an
[interactive tutorial)(http://commonmark.org/help/tutorial/).

You can test and convert on line your CommonMark document on the
[Dingus interactive translator](http://spec.commonmark.org/dingus/)
powered by _commonmark.js_.

John Mac Farlane also provide two implementations,
[cmark](https://github.com/jgm/cmark) written in C, and
[commonmark.js](https://github.com/jgm/commonmark.js)
in javascript.

[CommonMark-py](https://github.com/rtfd/CommonMark-py)
is a pure Python port of jgm's _commonmark.js_,

[recommonmark](http://recommonmark.readthedocs.io/en/latest/index.html) A
docutils-compatibility bridge to CommonMark which allows you to write
CommonMark inside of Docutils & Sphinx projects. recommonmark is
written in python, it uses CommonMark-py, [recommonmark source
](http://spec.commonmark.org/) is on GitHub.

Using recommonmark you can [use Markdown in Sphinx
](http://www.sphinx-doc.org/en/latest/markdown.html)

# Markdown formatters and extensions

[w3.org List of Markdown Implementations](http://www.w3.org/community/markdown/wiki/MarkdownImplementations).
## Awk
-   _md2x_ is an awk script, The  original 2006 scripitself authored by Jesus Galan (yiyus) is named
    [txt2html.awk
    ](http://newsgroups.derkeiler.com/Archive/Comp/comp.lang.awk/2007-08/msg00089.html)
    or
    [markdown.awk
    ](http://lawker.googlecode.com/svn/fridge/gawk/text/markdown.awk)
    (2009 version) or
    [md2html.awk](https://github.com/wlangstroth/simple-static/blob/master/md2html.awk).
    <a name="md2html_awk"></a>.
    it is used in [simple-static](/node/static_site/#simple_static "internal reference") and
    [sw](/node/static_site/#sw "internal reference").

## Bash

-   [markdown.bash](https://github.com/chadbraunduin/markdown.bash/)
    a Markdown interpreter using only Bash, Sed, Grep, and Cut.

## C

-   [cmark](https://github.com/jgm/cmark) by John MacFarlane is a
    [CommonMark](http://commonmark.org/) markdown implementation in
    C.
-   [Discount](http://www.pell.portland.or.us/~orc/Code/discount/)
    (BSD License) is a C library and comnand-line compiler for
    Markdown to html. Discount allow some Markdown extensions,
    smartypants-style substitutions, paragraph centering, images with
    size, definition lists, ordered lists with alphabetic labels,
    class blocks, PHP Markdown Extra-style tables, Pandoc-style
    document headers, Fenced code blocks. Discount has
    [bindings for node.js](https://github.com/visionmedia/node-discount),
    [bindings for lua](http://asbradbury.org/projects/lua-discount),
    [RDiscount binding for Ruby](https://github.com/rtomayko/rdiscount).
    A Debian package is available.
    {: #discount}
-   <a name="hoedown"></a>
    [Hoedown](https://github.com/hoedown/hoedown)(BSD like license)
    is a markdown processing library in C. it is a fork of the now frozen
    [sundown](#sundown "internal reference") with the same extensions.
    -   [Hoedown Wiki](https://github.com/hoedown/hoedown/wiki)
    -   [Hoedown bindings
        ](https://github.com/hoedown/hoedown/wiki/Bindings):
        Apache module, Elixir, Go, LuaJIT,
        [Nim](https://github.com/gradha/midnight_dynamite), Node.JS,
        Perl 5, PHP, Python ([Hoep](https://github.com/Anomareh/Hoep),
        [python-hoedown](https://github.com/hhatto/python-hoedown)),
        [Rust](http://doc.rust-lang.org/rustdoc/html/markdown/),
        Tcl.
-   <a name="lowdown">[lowdown](https://kristaps.bsd.lv/lowdown/)
    (ISC Licence) is a C markdown processor, it is a fork of [Hoedown
    ](#hoedown "internal reference"), see the home page for
    differences. A major feature additions is the troff ouput format.
    -   [GitHub - lowdown](https://github.com/kristapsdz/lowdown)
-   <a name="mdp"></a>[mdp](https://github.com/visit1985/mdp)(GPL)
    is a command-line based markdown presentation tool. It renders
    markdown as text formated with ansi escape sequences.
    _mdp is in Debian._
-   <a name="multimarkdown"></a>
    [multimarkdown](http://fletcherpenney.net/multimarkdown/)
    (GPL and MIT licenses)
    is an extension to markdown. It is written in C and extend
    [peg-markdown](#peg-markdown) to work with complete documents and
    convert them into other formats, including complete XHTML
    documents, LaTeX, PDF, OpenDocument. It allows like php-markdown
    tables and definition list and add metadata, header and footer,
    footnotes, MathJax, attributes to links and images,
    cross-references.
    -   [peg-multimarkdown GitHub Repository](https://github.com/fletcher/peg-multimarkdown)
    -   [Multimarkdown manual (pdf)](http://fletcher.github.com/peg-multimarkdown/mmd-manual.pdf)
    -   [MultiMarkdown CMS](http://fletcherpenney.net/multimarkdown/cms/)
        [MultiMarkdown CMS GitHub repository](https://github.com/fletcher/MultiMarkdown-CMS)
        is a CMS for markdown by Fletcher T. Penney.
        -   Wikipedia [w:multimarkdown]
-   <a name="peg-markdown"></a>
    [peg-markdown](https://github.com/jgm/peg-markdown)
    (GPL) by  John MacFarlane _author of pandoc_
    is an implementation of markdown in C, using a PEG grammar.
    John MacFarlane has also written an haskell version
    [markdown-peg](https://github.com/jgm/markdown-peg).
-   <a name="sundown"></a>
    [Sundown](https://github.com/vmg/sundown) (BSD like license)
    by [Vicent Martí (vmg)](https://github.com/vmg/)
    is a markdown processing library in C. It has bindings for many languages.
     -   [Misaka](https://github.com/FSX/misaka)) (BSD like license)
         by [Frank Smit (FSX)](https://github.com/FSX)
         provides the python bindings for sundown.
         Misaka is written in Cython and C.
         The source of [Misaka Manual](http://misaka.61924.nl/)
         are in the
         [docs directory of Misaka
         ](https://github.com/FSX/misaka/tree/master/docs).
     -   Sundown is frozen since 2012 the development continue on a
         fork named [hoedown](#hoedown "internal reference).

## Clojure

-   [markdown-clj](https://github.com/yogthos/markdown-clj)
    is a Markdown parser in Clojure that compiles to both Clojure
    and ClojureScript.

## Haskell
-   <a name="pandoc"></a> [Pandoc](http://pandoc.org/) (GPL v2)
    is a Haskell library and a command-line tool for converting from
    one markup format to another. It can convert many formats
    (reStructuredText, textile, HTML, DocBook, LaTeX, MediaWiki
    markup, TWiki markup, OPML, Emacs Org-Mode, Txt2Tags, Microsoft
    Word docx, EPUB, or Haddock markup) to plain text, Markdown,
    CommonMark, PHP Markdown Extra, GitHub-Flavored Markdown,
    MultiMarkdown, reStructuredText, XHTML, HTML5, LaTeX
    (including beamer slide shows), ConTeXt,  RTF,  OPML,  DocBook,
    OpenDocument, ODT, Word docx, GNU Texinfo, MediaWiki markup,
    DokuWiki markup, ZimWiki markup, Haddock markup,
    EPUB (v2 or v3), FictionBook2, Textile, groff man pages,
    Emacs Org mode,  AsciiDoc,  InDesign ICML,  TEI Simple, Slidy,
    Slideous, DZSlides, reveal.js, S5 HTML slide shows.
    -   The [Pandoc User’s Guide](http://pandoc.org/README.html),
        and [Pandoc examples](http://pandoc.org/demos.html)
    -   [Pandoc Markdown
        ](http://pandoc.org/MANUAL.html#pandocs-markdown)
        is a set of extensions of MarkDown, each extension can be enabled or disabled.
    -   You can try an [online pandoc converter](http://pandoc.org/try/)
    -   [Emacs pandoc mode](http://joostkremers.github.io/pandoc-mode/)
        (BSD License) by Joost Kremers is an Emacs mode for interacting with Pandoc.
    -   [panzer](https://github.com/msprev/panzer) (BSD License)
        adds styles to pandoc. Styles are combinations of templates, metadata settings,
        pandoc command line options, and instructions to run filters, scripts and
        postprocessors.  Styles simplify makefiles, bundling everything related to the
        look of the document in one place.

## Javascript
-   [Let's Make a Framework: Writing Documentation
    ](http://dailyjs.com/2011/01/13/framework-part-46/)
    tell us about converting markdown in javascript.
-   [commonmark.js](https://github.com/jgm/commonmark.js)
    by John MacFarlane is a [CommonMark](http://commonmark.org/)
    markdown implementation in javascript.  Instead of converting
    Markdown directly to HTML, as most converters do, commonmark.js
    parses Markdown to an AST (abstract syntax tree), and then renders
    this AST as HTML. This opens up the possibility of manipulating
    the AST between parsing and rendering.
-   <a name="dillinger"></a>[Dillinger](http://dillinger.io/)
    (BSD like licence) is a node.js HTML5 Markdown editor. It is abled
    to work with cloud services as Dropbox or GitHub but allow also to
    export your document in source format and html to any local
    location. It uses the
    [showdown module](#showdown "internal reference").
    -   [Dillinger GitHub repository
        ](https://github.com/joemccann/dillinger)
-   [DocToc](https://github.com/thlorenz/doctoc) is a Node.js
    application to generates table of contents for markdown files
    inside local git repository. Links are compatible with anchors
    generated by github or other sites.
-   [Docter](https://github.com/alampros/Docter) is a node application
    to render Github Flavored Markdown by using github's own
    redcarpet library. It has a big requirement list including NodeJS,
    NPM,  Ruby, Rubygems, redcarpet, pygments.rb.
    [node gfm](https://github.com/gagle/Node-GFM) (MIT License)
    by Gabriel Llamas is a Node application to render
    GitHub Flavored Markdown and allow editing them in the browser.
-   [gfms](https://github.com/ypocat/gfms) (MIT License)
    by Juraj Vitko
    is a Node application to render GitHub Flavored Markdown.
-   [Gitdown](https://github.com/gajus/gitdown) (BSD licence)
    is a markdown preprocessor in javascript for HitHub flavoured
    Markdown. It can generate a table of contents, include documents,
    use variables, generate id for sections, generate bages.
    Gitdown is designed to be run using either of the build systems,
    such as Gulp or Grunt.
-   <a name=marked></a>[marked](https://github.com/chjj/marked)
    (MIT License) by Christopher Jeffrey is
    a node.js markdown compiler, written in javascript, it is said as
    quick as the C markdown compiler and implements
    GitHub Flavored Markdown features.
-   [marked-man](https://github.com/kapouer/ronnjs) (BSD License)
    uses the javascript converter
    [marked](#marked "internal reference") to convert markdown to roff.
-   [pagedown](http://code.google.com/p/pagedown/) (MIT License)
    is the version of Attacklab's Showdown and WMD as used on Stack
    Overflow.  It includes a converter to HTML that can be used both
    in the browser, and on the server using Node.JS. , a Markdown
    editor with realtime preview of the generated HTML, and a few
    useful plugins.
-   <a name="showdown"></a>[showdown](https://github.com/coreyti/showdown)
    by  John Fraser is a javascript formatter for markdown.
    It is used by
    [wmd editor](http://wmd-editor.com/) and
    [Dillinger](#dillinger "internal reference").
    [Showdown & Highlight.js - Markdown and syntax highlighting in Javascript
    ](http://softwaremaniacs.org/playground/showdown-highlight/)
    provides  _showdown_ on-line as markdown converter.
-   <a name="remark"></a>[Remark](MIT License)
    is a markdown javascript parser and compiler.
    It is powered by the syntax tree transformer
    [unified](https://unifiedjs.github.io/)
    and uses plugins to translate markdown.
    It can process markdown to html with
    [remark-html](https://github.com/remarkjs/remark-html)
    or man pages with
    [remark-man](https://github.com/remarkjs/remark-man).
-   [unified](https://unifiedjs.github.io/)
    is a syntax tree transformer it it iused in
    -   awesome-lint to make it easier to create and maintain Awesome lists.
    -   how-to-markdown to teach markdown
    -   documentation.js to generate formatted docs
    -   [readability](https://github.com/wooorm/readability)
        measures ease of reading of text. It uses several
        formulas. Green colored texts should be readable for your target
        audience.



##  Lua
-   [lua-discount](http://asbradbury.org/projects/lua-discount)
    binding for [Discount](#discount "internal reference")
-   <a name="lunamark">[Lunamark
    ](https://github.com/jgm/lunamark) (MIT)
    is a lua library and command-line program for conversion of
    markdown to HTML, dzslides, Docbook, ConTeXt, LaTeX, and Groff
    man.
    The markdown parser is written using a PEG grammar and it is easy
    to add new writers.
-   [markdown in Lua](http://www.frykholm.se/files/markdown.lua)
    is used by Sputnik.

## Ruby
-   [word-to-markdown](https://github.com/benbalter/word-to-markdown)
    (MIT License)
    is a ruby gem to convert Microsoft Word documents to Markdown.
    It needs libreoffice, and can be used in command line. There is
    also a web service, an istance is at
    [Online Word to Markdown converter
    ](https://word-to-markdown.herokuapp.com/).

## Nim {#markdown-nim}
-   [midnight_dynamite
    ](https://github.com/gradha/midnight_dynamite)
    is a [hoedown](#hoedown "internal reference") binding for Nim.

## PHP
-   [php markdown](http://www.michelf.com/projects/php-markdown/) (BSD License) is a php PEAR
    implementation of markdown.
    The <a name="php-markdown-extra"></a> [PHP markdown extra
    ](http://michelf.com/projects/php-markdown/extra/)
    version add extra features.
    The site provides also an [on-line converter
    ](http://michelf.com/projects/php-markdown/dingus/)
    analog to the
    [original dingus](http://daringfireball.net/projects/markdown/dingus)
    but with an optional use of
    [php-markdown extra](http://michelf.com/projects/php-markdown/extra/) and
    [php-smartypants](http://michelf.com/projects/php-smartypants/).
-   [php-markdown-extra-extended
    ](https://github.com/egil/php-markdown-extra-extended)
    (MIT License) is a of  PHP Markdown Extra, extending it with
    numerous features like: generating break on newline _like Github
    Markdown_, fenced code block with language support, it also
    support generation of HTML5 with support for figure and figcaption tags.

## Python {#markdown-python}
-   [formd](https://github.com/drbunsen/formd) is a 100sloc python script
     to convert between markdown inline links and referenced links.
-   [html2text](http://www.aaronsw.com/2002/html2text/)(GPL 2.0)
    _2002_ from Aaron Swarz is a Python script that
    converts a page of HTML into markdown format. An on-line converter
    is available on the [html2text page](http://www.aaronsw.com/2002/html2text/.
-   [Grip](https://github.com/joeyespo/grip) (MIT LIcense)
    by Joe Esposito
    is a [Flask](/node/263#flask "internal reference") application
    to preview or output html of a Markdown file as it looks on GitHUb
    wikis. It has support for GitHub flavored Markdown.
-   [Hoep](https://github.com/Anomareh/Hoep)
    an [hoedown](#hoedown "internal reference") binding for Python.
-   [python-hoedown](https://github.com/hhatto/python-hoedown)
    an [hoedown](#hoedown "internal reference") binding for Python.
-   [Markdown Preprocessor](http://noswap.com/projects/markdownpp/)
    (BSD like licence)
    is a Python module designed to add a preprocessor on top of  Markdown.
    It is aimed at creating larger technical documents.
    [GitHub: markdown-pp](https://github.com/jreese/markdown-pp).
    It allows inclusions of markdown code files or url; and to expand
    latex code with
    [QuickLatex](http://www.holoborodko.com/pavel/quicklatex/)
-   [MarkLess](https://github.com/wiesmann/Markless)(BSD)
    is a small python script to render markdown as unicode text. That
    is the text decorations are rendered with unicode fonts, not with
    escape sequence as does [mdp](#mdp "internal reference").
-   [Moo](https://github.com/pyrocat101/moo)
    is an editor-agnostic markdown live previewer.
    Write markdown in any editor, and view pretty HTML output in
    your browser instantly. It supports Github-flavored markdown.
-   [Meow](https://github.com/hhatto/meow) (MIT License)
    is a fork of _Moo_ and also an editor-agnostic markdown and
    reStructuredText live previewer. It add to _Moo_ a ReStructured
    text previewer.
    Meow is built on top of
    [Bottle](/node/python_web#bottle "internal reference"),
    [Cherrypy](/node/python_web#cherrypy "internal reference") and
    can use [hoedown](#hoedown "internal reference").
-   [Parm](http://limodou.github.io/parm/README.html)
    parse markdown syntax to html, supports semantic-ui and bootstrap
    css framework, disqus, and can be used to
    [host your docs in github pages
    ](http://limodou.github.io/parm/README.html#toc13).
    It includes also a rst to markdown converter.
    -   [GiThub Par](https://github.com/limodou/par).
    -   [GiThub Parm](https://github.com/limodou/parm).

### Python-Markdown {#python-markdown}
[Python-Markdown](https://pythonhosted.org/Markdown/) (BSD+GPL)
is a python converter is, it allows many [extensions
]((https://pythonhosted.org/Markdown/extensions).

See also the [Mardown CheatSheet
](/node/markdown_cheatsheet "internal reference") for python-markdown.


There is a [Python-Markdown version 2 or markdown2
](https://github.com/trentm/python-markdown2)
also [in PyPi](https://pypi.python.org/pypi/markdown2).

-   [Python-Markdown Extra
    ](https://pythonhosted.org/Markdown/extensions/extra.html)
    or for markdown2: <a name="python-markdown-extra"></a>
    [Python Markdown2 Extra
    ](https://github.com/trentm/python-markdown2/wiki/Extras)
    regroup a set of extensions that imitate and extend
    [php-markdown extra](#php-markdown-extra "internal reference")
    by adding :

    -   [abbreviations
        ](https://pythonhosted.org/Markdown/extensions/abbreviations.html),
    -   [attribute lists
        ](https://pythonhosted.org/Markdown/extensions//attr_list.html)
        to define attributes on the various HTML elements in
        markdown’s output. It extend the
        [PHP Markdown Extra extension special attributes
        ](https://michelf.ca/projects/php-markdown/extra/#spe-attr),
        also availabe in pandoc for headers, links and fenced code.

        The python-markdown syntax extend the PHP Markdown Extra.
        While an id is written `{#id}` in PHP-Markdown, and also
        undestood as such in pandoc and python-markdown, you can
        write it `{: #id}` in Python-Markdown.
        You can also define other attibutes like
        `{: lang='french' .someclass}` You can define an id for the
        present paragraph by putting as last line `{: #attribute-list
        }`.
        {: #attribute-list }

        Note that the extension [Table of Content
        ](https://pythonhosted.org/Markdown/extensions/toc.html) and
        the now obsolete
        [headerId
        ](https://pythonhosted.org/Markdown/extensions/header_id.html)
        automatically generates id attributes for the header elements
        _(except those for which you define a specific header attribute)_.
        This is enabled by default;

        To illustrate this extension I put here a
        `[reference to attribute list](#attribute-list)`
        [reference to attribute list](#attribute-list).

    -   [definition lists
        ](https://pythonhosted.org/Markdown/extensions/attr_list.html)
        like

            definition list
            :   a type of list were the header is a work, and
                the body is the definition.

    -   [fenced code blocks
        ](https://pythonhosted.org/Markdown/extensions/fenced_code_blocks.html)
        or [fenced code blocks for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/fenced-code-blocks)
        That can delimit code blocks either with the PHP-Markdown
        syntax `~~~` or the GitHub GFM syntax <code>```</code>.  In
        addition to PHP Extra’s syntax, you can define the
        language of the code block and lines to emphasize for use
        by syntax highlighters like this:

            ```python
            if True:
                print "hi"
            ```

    -   [footnotes
        ](https://pythonhosted.org/Markdown/extensions/footnotes.html)
        or [footnotes for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/footnotes),
        example:

            Footnotes[^1] have a label[^@#$%] and the footnote's content.

            [^1]: This is a footnote content.
            [^@#$%]: A footnote on the label: "@#$%".

    -   [tables](https://pythonhosted.org/Markdown/extensions/tables.html)
        or
        [tables for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/tables)
        or [wiki-table for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/wiki-tables)
        and python-markdown third party extension
        [Markdown GridTables
        ](https://github.com/smartboyathome/Markdown-GridTables/)
        that add grid tables as seen in ReSt.
    -   [smart_strong ](https://pythonhosted.org/Markdown/extensions/smart_strong.html)
        adds smarter handling of double underscores within words.
        the default option _smart-emphasis_ do it for simple underscore.

        python-markdown2 does not have the _smart-strong_ nor the
        _smart-emphasis_ extension instead it provides
        [code-friendly
        ](https://github.com/trentm/python-markdown2/wiki/code-friendly)
        that disable all use of emphasis and strong with a simple or
        double underscore.

-   The other extensions to python-markdown are
    [listed in the doc
    ](http://pythonhosted.org/Markdown/extensions/index.html), the
    following ones are enabled by default:

    -   The [CodeHilite extension](https://pythonhosted.org/Markdown/extensions/code_hilite.html)
        adds code/syntax highlighting to standard Python-Markdown code blocks using
        [Pygments](node/311#pygments "Internal reference").
        It can be used with fenced blocks, or by using
        `:::<language>`
        as the first line of indented code blocks.

        The list of languages is in
        [Pygments language list](http://pygments.org/languages/) and
        [Pygments lexers](http://pygments.org/docs/lexers/).

    -   [headerId
        ](https://pythonhosted.org/Markdown/extensions/header_id.html)
        automatically generates id attributes for the header
        elements.
    -   [Meta-Data
        ](https://pythonhosted.org/Markdown/extensions/meta_data.html)
        adds a syntax for defining meta-data about a document.
    -   [Sane Lists
        ](https://pythonhosted.org/Markdown/extensions/sane_lists.html)
        allow the mixing of list types. In other words, an ordered
        list will not continue when an unordered list item is
        encountered and vice versa.
    -   [Table of Content
        ](https://pythonhosted.org/Markdown/extensions/toc.html)
        generates a Table of Contents from a Markdown document
        when encountering a `[TOC]` markup.
    -   [WikiLinks
        ](https://pythonhosted.org/Markdown/extensions/wikilinks.html)
        converts any [[bracketed]] word in a link.

-   There are also numerous
    [third party extensions of python-markdown
    ](https://github.com/waylan/Python-Markdown/wiki/Third-Party-Extensions).
-   [markdown2latex](http://pypi.python.org/pypi/markdown2latex/)
    by [Rufus Pollock](http://www.rufuspollock.org/)
    is an extension to python-markdown to support LaTeX
    (rather than html) output _not updated since 2009_.

## Ruby
-   [kramdown](http://kramdown.gettalong.org/)
    a pure-Ruby Markdown-superset converter.


## Rust
-   [Rust Markdown Module](http://doc.rust-lang.org/rustdoc/html/markdown/).

# Markdown documentation generators
Some markdown to slideshow converters are given in the
[html slideshow page](/node/html#slideshow "internal reference")
 landslide, markdown2deckjs, Deck.rb, keydown ...

The reference to ebook generators are in a
[section of Epub page
](node/epub##structured_to_epub "internal reference")

Some few [Static site generators](node/static_site/ "internal reference") are
either targeted to documentation, or support it easily:
   [elyse](/node/static_site/#elyse "internal reference"),
   [markdoc](/node/static_site/#markdoc "internal reference"),
   [poole](/node/static_site/#poole "internal reference"),
   [simple-static](/node/static_site/#simple_static "internal reference"),
   [sw](/node/static_site/#sw "internal reference")

-   [markdown to ebook](https://github.com/k2052/markdown-to-ebook)
    is an ebook that explain how creating ebooks using Markdown.
-   [Beautiful docs](http://beautifuldocs.com/)
    is a documentation viewer in node.js for markdown files.
-   [d](http://pypi.python.org/pypi/d) (MIT/X11)
    is a documentation generator from markdown files.
    [d documentation](http://sjl.bitbucket.org/d/)
-   [Docco](http://jashkenas.github.com/docco/) (MIT license)
    is a node.js hundred-line-long, literate-programming-style
    documentation generator.
-   [DocumentUp](http://documentup.com/)
    is a javascript generator for markdown documentation.
    [GitHub: DocumentUp](https://github.com/jeromegn/DocumentUp).
-   [mdoc](https://github.com/millermedeiros/mdoc) (MIT license)
    node.js markdown powered documentation generator
-   The [redo package](https://github.com/apenwarr/redo) *a make replacement*
    includes a python script to convert markdown to man page
    [md2man.py](https://github.com/apenwarr/redo/blob/master/Documentation/md2man.py).



<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
