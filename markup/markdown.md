---
title: MarkDown
---

{{% toc /%}}

# {{< wp "Markdown" >}}

-   [Markdown](http://daringfireball.net/projects/markdown/)
    (BSD style license) is a text-to-HTML conversion tool originaly
    written in perl, but that has also implementations in C, python, php,
    haskell, lua. Markdown can be used in many CMS _often through plugins_
    Instiki Wiki (ruby powered wiki), ikiwiki. dokuwiki,
    [Moinmoin](http://moinmo.in/), [WolfCms](http://www.wolfcms.org/),
    {{< iref  "content_management#gollum" "Gollum" >}}.
    It is widely used in Django
    powered applications _using the python implementation_.

    It is the most usual syntax for
    {{< iref  "static_sites" "Static site generators" >}}

-   There is two lists of _Awesome Markdown_ references:
    [GitHub - mundimark/awesome-markdown](https://github.com/mundimark/awesome-markdown)
    seems the more complete and up to date, and
    [GitHub - BubuAnabelas/awesome-markdown
    ](https://github.com/BubuAnabelas/awesome-markdown).
-   [markdown mailing list at Gmame
    ](http://dir.gmane.org/gmane.text.markdown.general)
-   A detailed references page [XBeta Wiki: Markdown
    ](http://xbeta.org/wiki/show/Markdown)
-   [DropPages](http://droppages.com/) is a site that allows to put a static site
    written in markdown in your DropBox.
-   [tpl4md](https://github.com/dloureiro/tpl4md) (AGPL)
    by David Loureiro is a set of markdown templates for widely used
    documents like letters, invoices, orders, slides. _2013_

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

Some browser extensions allow to capture markdown from a displayed page in the browser:

-   [chitsaou/copy-as-markdown](https://github.com/chitsaou/copy-as-markdown)
    is a firefox and Chromium extension to  make opying Link, Image and
    Tab(s) as Markdown much easier. _in 2019 no longer referenced as a Firefox
    extension_.
-   [0x6b/copy-selection-as-markdown](https://github.com/0x6b/copy-selection-as-markdown)
    is a firefox extension to copy selection as markdown, copy title and url as markdown
    and copy link as markdown. The markdown style is configurable, and a shortcut key
    can be assigned (default `Ctrl + Shift + E` but as it is yet used I prefer
    `Alt + Shift + W`).




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
{{< iref "#pandoc" "Pandoc" >}} extensions are widely used,
but many are specific to Pandoc.

At least three extensions are quite widespread and many parsers try to
implement them

-   The Older one is
    {{< iref "#php" "php markdown extra" >}}
    that add: Inline HTML, Markdown Inside HTML Blocks,
    Special Attributes, Fenced Code Blocks with <code>~~~</code>,
    Tables, Definition Lists,
    Footnotes, Output, Abbreviations, Emphasis, Backslash Escapes.<br />
    {{< iref "#python" "Python-markdown" >}}group the
    same features in
    {{< iref "#python" "python-markdown-extra" >}};
    and add a rich set of custom extensions.
    <br />
    The other extensions use to build up on markdown extra and extend
    it.
-   [Stack Overflow MarkDown](http://stackoverflow.com/editing-help)
    is a very standard MarkDown with some additions whose main is
    [Syntax highlighting for code
    ](http://stackoverflow.com/editing-help#syntax-highlighting)
    that uses [Google prettify
    ](http://google-code-prettify.googlecode.com/svn/trunk/README.html)
-   <a name=gfm"></a>[Github Flavored Markdown - GFM](https://github.github.com/gfm/)
    is a very popular extension. The main difference is that in Standard
    Markdown newline are ignored and in GFM they are significative.
    GFM disable also disable italicize parts of words, allow
    strikethrough, fenced code block with <code>&#96;&#96;&#96;</code>
    syntax higlighting with <code>&#96;&#96;&#96;python</code> like headers.

    It also add a definition list and a
    [table extension](https://github.github.com/gfm/#tables-extension-),
    task lists, and few GitHub specific shortcuts.

    -   [GitHub Help: Mastering markdown
        ](https://guides.github.com/features/mastering-markdown/)
        is an howto for
        [Github Flavored Markdown](https://github.github.com/gfm/).

-   {{< iref "#pandoc_markdown" "Pandoc Markdown" >}}
    include a set of extensions for MarkDown.
-   [Babelmark2](http://johnmacfarlane.net/babelmark2/) compare the rendering
    of various markdown formatters.
    -   [Babelmark2 FAQ](http://johnmacfarlane.net/babelmark2/faq.html)

## CommonMark {#commonmark}
[CommonMark](http://commonmark.org/) is a formal specification of
(a flavor of) MarkDown language by John Mac Farlane.

John Mac Farlane previously produced many markdown parsers like
{{< iref "#pandoc" "pandoc" >}} or {{< iref "#peg" "peg-markdown" >}}.

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

[w3.org List of Markdown Implementations
](http://www.w3.org/community/markdown/wiki/MarkdownImplementations).

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
    it is used in {{< iref "static_sites#simple_static" "simple-static" >}} and
    {{< iref "static_sites#sw" "sw" >}}.

## Bash

-   [markdown.bash](https://github.com/chadbraunduin/markdown.bash/)
    a Markdown interpreter using only Bash, Sed, Grep, and Cut.

## C

-   [cmark](https://github.com/jgm/cmark) by John MacFarlane is a
    {{< iref "#Commonmark" "CommonMark" >}} markdown implementation in C.
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
    {{< iref "#sundown" "sundown" >}} with the same extensions.

    It is nearly compatible with {{< iref "gfm" "GitHub Flavored Markdown" >}}
    with only
    [small differences](https://github.com/hoedown/hoedown/wiki/Spec-differences)

    -   [Hoedown Wiki](https://github.com/hoedown/hoedown/wiki)
    -   [Hoedown bindings
        ](https://github.com/hoedown/hoedown/wiki/Bindings):
        Apache module, Elixir, Go, LuaJIT,
        [Midnight Dynamite](https://github.com/gradha/midnight_dynamite) _(NIM)_,
        Node.JS, Perl 5, PHP, ([Hoep](https://github.com/Anomareh/Hoep) _( Python)_,
        [python-hoedown](https://github.com/hhatto/python-hoedown)),
        [Misaka](https://github.com/FSX/misaka) _(Python)_,
        [Rust](http://doc.rust-lang.org/rustdoc/html/markdown/),
        Tcl {{< iref "markdown#redcarpet" "Redcarpet" >}} _(Ruby)_.
    -   [Hoextdown](https://github.com/jasharpe/hoextdown) (MIT License)
         is an extension to Hoedown adding Special Attributes, Task Lists,
         Line Continue, Header ID, Fenced Script, Script Tags, Meta Block.

-   <a name="lowdown">[lowdown](https://kristaps.bsd.lv/lowdown/) (ISC Licence)
    is a C markdown processor, it is a fork of {{< iref "#hoedown" "Hoedown" >}}, see
    the home page for differences. A major feature additions is the troff ouput format.
    -   [GitHub - lowdown](https://github.com/kristapsdz/lowdown)
-   <a name="mdp"></a>[mdp](https://github.com/visit1985/mdp)(GPL)
    is a command-line based markdown presentation tool. It renders
    markdown as text formated with ansi escape sequences.
    _mdp is in Debian._
-   <a name="multimarkdown"></a>
    [multimarkdown](http://fletcherpenney.net/multimarkdown/)
    (GPL and MIT licenses)
    is an extension to markdown. It is written in C and extend
    {{< iref "#peg" "peg-markdown" >}} to work with complete documents and
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
        -   Wikipedia {{< wp "multimarkdown" >}}
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

     -   Sundown is frozen since 2012 the development continue on a
         fork named {{< iref "#hoedown" "hoedown" >}}.

## Clojure

-   [markdown-clj](https://github.com/yogthos/markdown-clj)
    is a Markdown parser in Clojure that compiles to both Clojure
    and ClojureScript.


## Javascript
-   [Let's Make a Framework: Writing Documentation
    ](http://dailyjs.com/2011/01/13/framework-part-46/)
    tell us about converting markdown in javascript.
-   [commonmark.js](https://github.com/jgm/commonmark.js)
    by John MacFarlane is a  {{< iref "#Commonmark" "CommonMark" >}}
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
    {{< iref "#showdown" "showdown module" >}}.
    -   [Dillinger GitHub repository
        ](https://github.com/joemccann/dillinger)
-   [DocToc](https://github.com/thlorenz/doctoc) is a Node.js
    application to generates table of contents for markdown files
    inside local git repository. Links are compatible with anchors
    generated by github or other sites.
-   [Docter](https://github.com/alampros/Docter) is a node application
    to render Github Flavored Markdown by using github's own
    {{< iref "#redcarpet" "Redcarpet" >}} library. It has a big requirement list
    including NodeJS, NPM, Ruby, Rubygems, {{< iref "#redcarpet" "Redcarpet" >}},
    pygments.rb.
-   <a name="node_gfm"></a>[node gfm](https://github.com/gagle/Node-GFM) (MIT License)
    by Gabriel Llamas is a Node application to render
    GitHub Flavored Markdown and allow editing them in the browser.
-   <a name="gfms"></a>[gfms](https://github.com/ypocat/gfms) (MIT License)
    by Juraj Vitko  is a Node application to render GitHub Flavored Markdown.
-   <a name="gitdown"></a>[Gitdown](https://github.com/gajus/gitdown) (BSD licence)
    is a markdown preprocessor in javascript for GitHub flavoured
    Markdown. It can generate a table of contents, include documents,
    use variables, generate id for sections, generate bages.
    Gitdown is designed to be run using either of the build systems,
    such as Gulp or Grunt.
-   <a name=marked></a>[marked](https://github.com/chjj/marked)
    (MIT License) by Christopher Jeffrey is
    a node.js markdown compiler, written in javascript, it is said as
    quick as the C markdown compiler and implements
    {{< iref "#commonmark" "CommonMark" >}} and
    {{< iref "#gfm" "GitHub Flavored Markdown" >}} features.
-   [marked-man](https://github.com/kapouer/ronnjs) (BSD License)
    uses the javascript converter
    {{< iref "#marked" "marked" >}} to convert markdown to roff.
-   [pagedown](http://code.google.com/p/pagedown/) (MIT License)
    is the version of Attacklab's Showdown and WMD as used on Stack
    Overflow.  It includes a converter to HTML that can be used both
    in the browser, and on the server using Node.js. , a Markdown
    editor with realtime preview of the generated HTML, and a few
    useful plugins.
-   <a name="showdown"></a>[showdown](https://github.com/coreyti/showdown)
    by  John Fraser is a javascript formatter for markdown.
    It is used by
    [wmd editor](http://wmd-editor.com/) and
    {{< iref "#dillinger" "Dillinger" >}}.
    [Showdown & Highlight.js - Markdown and syntax highlighting in Javascript
    ](http://softwaremaniacs.org/playground/showdown-highlight/)
    provides  _showdown_ on-line as markdown converter.
-   <a name="remark"></a>[Remark](https://github.com/remarkjs/remark) (MIT License)
    is a markdown javascript parser and compiler.
    It is powered by the syntax tree transformer
    [unified](https://unifiedjs.github.io/)
    and uses plugins to translate markdown.
    It can process markdown to html with
    [remark-html](https://github.com/remarkjs/remark-html)
    or man pages with
    [remark-man](https://github.com/remarkjs/remark-man).
-   [unified](https://unifiedjs.github.io/)
    is a syntax tree transformer it is used in
    -   awesome-lint to make it easier to create and maintain Awesome lists.
    -   how-to-markdown to teach markdown
    -   documentation.js to generate formatted docs
    -   [readability](https://github.com/wooorm/readability)
        measures ease of reading of text. It uses several
        formulas. Green colored texts should be readable for your target
        audience.

## Haskell

See {{< iref "#pandoc" "Pandoc" >}} below.


##  Lua
-   [lua-discount](http://asbradbury.org/projects/lua-discount)
    binding for {{< iref "#discount" "Discount" >}}
-   <a name="lunamark">[Lunamark
    ](https://github.com/jgm/lunamark) (MIT)
    is a lua library and command-line program for conversion of
    markdown to HTML, dzslides, Docbook, ConTeXt, LaTeX, and Groff
    man.
    The markdown parser is written using a PEG grammar and it is easy
    to add new writers.
-   [markdown in Lua](http://www.frykholm.se/files/markdown.lua)
    is used by Sputnik.

## Nim {#markdown-nim}
-   [midnight_dynamite
    ](https://github.com/gradha/midnight_dynamite)
    is a {{< iref "#hoedown" "hoedown" >}} binding for Nim.

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
    numerous features like: generating break on newline _like
    {{< iref "#gfm" "Github Markdown" >}}_, fenced code block with language support, it
    also support generation of HTML5 with support for figure and figcaption tags.

## Python {#markdown-python}


-   [formd](https://github.com/drbunsen/formd) is a 100sloc python script
     to convert between markdown inline links and referenced links.
-   [html2text](http://www.aaronsw.com/2002/html2text/)(GPL 2.0)
    _2002_ from Aaron Swarz is a Python script that
    converts a page of HTML into markdown format. An on-line converter
    is available on the [html2text page](http://www.aaronsw.com/2002/html2text/.
-   [Grip](https://github.com/joeyespo/grip) (MIT LIcense)
    by Joe Esposito
    is a {{< iref "python_web#flask" "Flask" >}} application
    to preview or output html of a Markdown file as it looks on GitHUb
    wikis. It has support for GitHub flavored Markdown.
-   [Hoep](https://github.com/Anomareh/Hoep)
    an {{< iref "#hoedown" "hoedown" >}} binding for Python.
-   [python-hoedown](https://github.com/hhatto/python-hoedown)
    an {{< iref "#hoedown" "hoedown" >}} binding for Python.
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
    escape sequence as does {{< iref "#mdp" "mdp" >}}.
-   < a name="misaka"><a>[Misaka](https://github.com/FSX/misaka)) (BSD like license)
    by [Frank Smit (FSX)](https://github.com/FSX) provides the python bindings for
    {{< iref "#sundown" "Sundown" >}}.
    Misaka is written in Cython and C.  The source of
    [Misaka Manual](http://misaka.61924.nl/) are in the
    [docs directory of Misaka](https://github.com/FSX/misaka/tree/master/docs).
-   [Moo](https://github.com/pyrocat101/moo)
    is an editor-agnostic markdown live previewer.
    Write markdown in any editor, and view pretty HTML output in
    your browser instantly. It supports Github-flavored markdown.
-   [Meow](https://github.com/hhatto/meow) (MIT License)
    is a fork of _Moo_ and also an editor-agnostic markdown and
    reStructuredText live previewer. It add to _Moo_ a ReStructured
    text previewer.
    Meow is built on top of
    {{< iref "python_web#bottle" "Bottle" >}},
    {{< iref "python_web#cherrypy" "Cherrypy" >}} and
    can use {{< iref "#hoedown" "hoedown" >}}.
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
](https://pythonhosted.org/Markdown/extensions).

See also the {{< iref "markdown_cheatsheet" "Mardown CheatSheet" >}} for python-markdown.


There is a [Python-Markdown version 2 or markdown2
](https://github.com/trentm/python-markdown2)
also [in PyPi](https://pypi.python.org/pypi/markdown2).

-   [Python-Markdown Extra
    ](https://pythonhosted.org/Markdown/extensions/extra.html)
    or for markdown2: <a name="python-markdown-extra"></a>
    [Python Markdown2 Extra
    ](https://github.com/trentm/python-markdown2/wiki/Extras)
    regroup a set of extensions that imitate and extend
    {{< iref "#php" "php-markdown extra" >}}
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
        `{{< iref "#attribute" "reference to attribute list" >}}`
        {{< iref "#attribute" "reference to attribute list" >}}.

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
        {{< iref "source_code#pygments" "Pygments" >}}
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

## Go

-   <a name="blackfriday"></a>[Blackfriday](https://github.com/russross/blackfriday)
    (BSD License)
    started as a translation from C of {{< iref "sundown" "Sundown" >}}.
    It contain extensions, including table support, fenced code blocks,
    autolinks, strikethroughs, non-strict emphasis, etc.


    It is not completly compatible with {{< iref "#commonmark" "Commonmark" >}} and its
    lists are not compatible with GFM. It is one reason of Hugo switching to GoldMark.

    It was the default formatter for {{< iref "static_sites#hugo" "Hugo" >}} until
    version 0.60.

    -   [blackfriday-latex](https://gitlab.com/ambrevar/blackfriday-latex) (MIT License)
        is a LaTeX renderer for the Blackfriday Markdown processor (v2).

-   <a name="goldmark">[Goldmark](https://github.com/yuin/goldmark/) (MIT License)
    Goldmark is compatible with {{< iref "#commonmark" "CommonMark" >}}
    and has many built-in extensions like

    -   [GFM extensions](https://github.github.com/gfm): Strikethrough, Autolinks,
        Task list items,
        [GFM table](https://github.github.com/gfm/#tables-extension-),
    -   PHP Markdown Extra:
        [Definitions Lists](https://michelf.ca/projects/php-markdown/extra/#def-list),
        [Footnotes](https://michelf.ca/projects/php-markdown/extra/#footnotes)

    It is the default formatter for {{< iref "static_sites#hugo" "Hugo" >}}.

## Ruby
-   <a name="kramdown"></a>[kramdown](http://kramdown.gettalong.org/)
    a pure-Ruby Markdown-superset converter. It can parse
     {{< iref "gfm" "GFM" >}} extensions.
-   <a name="redcarpet"></a>[redcarpet](https://github.com/vmg/redcarpet) (MIT License)
    is a Ruby library for Markdown processing.
    It is based on {{< iref "#sundown" "sundown" >}} and accept the same extensions.
-   [word-to-markdown](https://github.com/benbalter/word-to-markdown)
    (MIT License)
    is a ruby gem to convert Microsoft Word documents to Markdown.
    It needs libreoffice, and can be used in command line. There is
    also a web service, an istance is at
    [Online Word to Markdown converter
    ](https://word-to-markdown.herokuapp.com/).

## Rust
-   [Rust Markdown Module](http://doc.rust-lang.org/rustdoc/html/markdown/).

## Pandoc {#pandoc}
[Pandoc](http://pandoc.org/) (GPL v2)
is a Haskell library and a command-line tool for converting from
one markup format to another.

It can convert from many formats:<br/>
{{< iref "#commonmark" "CommonMark" >}}, creole, docbook, docx, dokuwiki, epub, fb2,
gfm, haddock (Haddock markup), html, ipynb (Jupyter notebook), jats (JATS XML), json,
latex, markdown (Pandoc’s Markdown), markdown_mmd (MultiMarkdown), markdown_phpextra,
markdown_strict, mediawiki, man (roff man), muse, native (native Haskell), odt, opml,
org (Emacs Org mode), rst, t2t (txt2tags), textile, tikiwiki, twiki, vimwiki

To many formats:<br/>
asciidoc or asciidoctor, beamer, {{< iref "#commonmark" "CommonMark" >}}, context,
docbook or docbook4, docbook5, docx, dokuwiki, epub or epub3, epub2, fb2, gfm, haddock
(Haddock markup), html or html5, html4, icml (InDesign ICML), ipynb (Jupyter notebook),
jats (JATS XML), jira (Jira wiki markup), json, latex, man (roff man), markdown,
markdown_mmd (MultiMarkdown), markdown_phpextra, markdown_strict, mediawiki, ms (roff
ms), muse, native (native Haskell),, odt, opml, opendocument, org (Emacs Org mode),
plain (plain text),, pptx (PowerPoint slide show), rst, rtf, texinfo, textile, slideous,
slidy, dzslides, revealjs, s5, tei, xwiki, zimwiki

-   The [Pandoc User’s Guide](http://pandoc.org/README.html),
    and [Pandoc examples](http://pandoc.org/demos.html)
-   [Pandoc Markdown"](https://pandoc.org/MANUAL.html#pandocs-markdown)
    is a set of extensions of MarkDown, each extension can be enabled or disabled.
-   You can try an [online pandoc converter](http://pandoc.org/try/)
-   [Emacs pandoc mode](http://joostkremers.github.io/pandoc-mode/)
    (BSD License) by Joost Kremers is an Emacs mode for interacting with Pandoc.
-   [panzer](https://github.com/msprev/panzer) (BSD License)
    adds styles to pandoc. Styles are combinations of templates, metadata settings,
    pandoc command line options, and instructions to run filters, scripts and
    postprocessors.  Styles simplify makefiles, bundling everything related to the
    look of the document in one place.
-   [Customizing pandoc to generate beautiful pdfs from markdown
    ](https://learnbyexample.github.io/tutorial/ebook-generation/customizing-pandoc/)
-   [Élaboration et conversion de documents avec Markdown et Pandoc
    ](https://enacit1.epfl.ch/markdown-pandoc/)

Pandoc processing may use _filters_ that work on the intermediate abstract syntax
tree (AST), the reference page is the
[Pandoc Filters page on Pandoc Wiki
](https://github.com/jgm/pandoc/wiki/Pandoc-Filters). The filters can bee written in
LUA, python (with [Panflute](http://scorreia.com/software/panflute/)),
PHP, node.js, perl, groovy and ruby.The
[Filters page](https://github.com/jgm/pandoc/wiki/Pandoc-Filters)
gives a list of wrappers for each programming language, and a list of known
available filters.

# Pandoc Markdown {#pandoc_markdown}

[Pandoc Markdown](http://pandoc.org/MANUAL.html#pandocs-markdown)
include a set of extensions of MarkDown which are enabled by default, unless you use
the *markdown-strict* format:

basic formatting
:   *blank_before_headers*, *header_attributes*, *implicit_header_references*,
    *escaped_line_breaks* with backslash before a newline, *auto_identifiers* and
    *implicit_header_references* for headers, *intraword_underscores*, _strikeout_,
    _superscript_, _subsript_, *small_caps*.

    *all_symbols_escapable* extend the backslash mecanism of standard markdown, to
    any punctuation or whitespace, and use a backslash followed by a newline to
    introduce a paragraph break.

blocks
:   *blank_before_blockquote* requires a blank line before a block quote ,
    *fenced_code_blocks* , *backtick_code_block*, attach attributes to fenced,
    backtick and inline code block with *fenced_code_attributes* and
    *inline_code_attributes*, *footnotes*, *inline_notes*,
    *line_block* with a sequence of lines beginning with a
    vertical bar, *markdown_in_html_blocks*,
    *pandoc_title_bloc* to give bibliographic information, *raw_html*,
    *yaml_metadata_blocks*.

tables
:   *table_captions*, *simple_tables*, *multiline_tables*, *grid_tables* wich
    are alike emacs tables, *pipe_tables* like PHP markdown axtra tables,

lists
:   _startnum_ for ordered lists, _fancy list_ can be marked with a `#` ,
     *definition_lists*, *example_lists*.

You can enable/disable individually each extension ou limit to some predefined set of
extension by using the formats *markdown_phpextra*, *gfm*, *markdown_mmd*,
*markdown_strict*, *{{< iref "#commonmark" "commonmark" >}}*.


# Markdown documentation generators
Some markdown to slideshow converters are given in the
{{< iref "html#slideshow" "html slideshow page" >}}
landslide, markdown2deckjs, Deck.rb, keydown ...

The reference to ebook generators are in a
{{< iref "epub#structured_to_epub" "section of Epub page" >}}.

Some few {{< iref "static_sites" "Static site generators" >}} are
either targeted to documentation, or support it easily:
    {{< iref "static_sites#hugo" "Hugo" >}},
    {{< iref "static_sites#elyse" "elyse" >}},
    {{< iref "static_sites#marcdoc" "markdoc" >}},
    {{< iref "static_sites#poole" "poole" >}},
    {{< iref "static_sites#simple_static" "simple-static" >}},
    {{< iref "static_sites#sw" "sw" >}}

-   [markdown to ebook](https://github.com/k2052/markdown-to-ebook)
    is an ebook that explain how creating ebooks using Markdown.
-   Markdown is used in 0'Reilly publications as an alternative to
    {{< iref "asciidoc" >}} to produce
    [htmlbook](http://oreillymedia.github.io/HTMLBook/).
    the _Atlas environment_ hosted at _O'Reilly Media_ allow to transform markdown
    to htmlbook, but they also provide a node.js program to do this translation
    [htmlbook.js](https://github.com/oreillymedia/htmlbook.js).
-   [oreillymedia/docbook2htmlbook](https://github.com/oreillymedia/docbook2htmlbook)
    is an XSL Transform to convert Docbook XML to HTMLBook.
-   [O'Reilly Atlas - writing in Markdown
    ](http://docs.atlas.oreilly.com/writing_in_markdown.html)
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
-   [doctoc](https://github.com/thlorenz/doctoc) (MIT License)
    Generates table of contents for markdown files inside local git repository.
    Links are compatible with anchors generated by github or other sites.

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
