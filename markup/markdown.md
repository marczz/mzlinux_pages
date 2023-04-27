---
title: MarkDown
---

# Markdown references


-   [Markdown](http://daringfireball.net/projects/markdown/) (BSD style license)
    is a text-to-HTML conversion tool originally
    written in perl, but that has also implementations in C, python, php,
    haskell, lua. Markdown

    It can be used in many CMS, blogg software, and Wiki _often through plugins_.

    It is widely used in Django powered applications _using the python implementation_.

    It is the most usual syntax for {{< iref  "static_sites" "Static site generators" >}}

-   Wikipedia: {{< wp "Markdown" >}}.
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
-   [Markdown Guide](https://www.markdownguide.org/getting-started/) (MIT License)
-   [tpl4md](https://github.com/dloureiro/tpl4md) (AGPL)
    by David Loureiro is a set of markdown templates for widely used
    documents like letters, invoices, orders, slides. _2013_

# Markdown Editing
[Emacs Markdown Mode](http://jblevins.org/projects/markdown-mode/) by Jason Blevins is
the standard major mode for editing Markdown formatted text with Emacs.

Markdown Mode can export the buffer to html and preview it (key `C-c C-c v`).

Live Export (`C-c C-c l`) turn on markdown-live-preview-mode to view the exported output
side-by-side with the source Markdown. By default the preview is done in Emacs eww mode.

There are also packages to preview the saved buffer like
[Markdown preview mode](https://github.com/ancane/markdown-preview-mode) in melpa.

You can nicely renders all basic CommonMark syntax with highlighted code blocks in your
terminal with [mdcat](https://github.com/lunaryorn/mdcat) (MPL-2.0) by Sebastian Wiesner
_lunaryorn_.

Some browser extensions allow to copy links as markdown or/and
to capture markdown from a displayed page in the browser:

-   [chitsaou/copy-as-markdown](https://github.com/chitsaou/copy-as-markdown)
    (MIT License)
    is a firefox and Chromium extension to  make copying Link, Image and
    Tab(s) as Markdown much easier. _in 2019 Firefox categorize it in "non recommended
    extension"._.
-   [0x6b/copy-selection-as-markdown
    ](https://github.com/0x6b/copy-selection-as-markdown)  (MIT License)
    is a firefox extension to copy selection as markdown, copy title and url as markdown
    and copy link as markdown. The markdown style is configurable
    and include {{< iref "#gfm" "GFM" >}}. A shortcut key
    can be assigned (default `Ctrl + Shift + E` but as it is yet used I prefer
    `Alt + Shift + W`).
-   [Markdown Here](https://markdown-here.com/)  (MIT License)
    is a browser extension for Chrome, Firefox, Safari, and Thunderbird to help you to
    write email, supports them. It provides an easy way of adding tables to your email
    -- a task that would otherwise require copy-pasting from another application.
    -   [Markdown Here - GitHub](https://github.com/adam-p/markdown-here/)

# Markdown Syntax
Markdown has be conceived by John Grüber, et also wrote a Perl processor for it.

The original [Markdown syntax](http://daringfireball.net/projects/markdown/syntax)
is summarized in the [dingus - Markdown on-line converter
](http://daringfireball.net/projects/markdown/dingus),
it is now referred as _Basic Markdown_ or _Vanilla Markdown_.

As the syntax of markdown was only given by informal free text description, there are
many ambiguities that are solved in a different way by each parser, and numerous
extensions.

Markdown  got a de facto standard when the {{< iref "#commonmark" "CommonMark" >}}
formal specification was published by John Mac Farlane.

{{< iref "#commonmark" "CommonMark" >}} gives the syntax for italic, emphasis (i.e
bold), and strong emphasis, hard line break (both 2 spaces and backslash),backtick code
span, ATX and Setext heading, link, image, block quote, indented, and fenced code
block, html block.

Many extensions to the basic and commonmark syntax have been defined, the first one that
predate CommonMark is {{< iref "#php-markdown-extra" "PHP Markdown Extra" >}}.

It adds : Inline HTML, Markdown Inside HTML Blocks, Special Attributes, Fenced Code Blocks
with <code>~~~</code>, Tables, Definition Lists, Footnotes, Output, Abbreviations,
Emphasis, Backslash Escapes.

From {{< iref "#php-markdown-extra" "PHP Markdown Extra" >}} extensions only emphasis,
inline html, fenced code block, backslash escape are part of
{{< iref "#commonmark" "CommonMark" >}}.

Many extensions are added by markdown parsers to {{< iref "#commonmark" "CommonMark" >}}
like tables, footnotes, definition lists, Markdown inside HTML blocks, source code
highlighting.

But the syntax of each construction is bound to one parser and only avilable in the
parser manual (at best, or the source code at worse).

{{< iref "#gfm" "GitHub Flavored  Markdown" >}} used first on GitHub, and later on on
many other popular sites is a specification of markdown which extend
{{< iref "#commonmark" "CommonMark" >}} which add a
[table extension](https://github.github.com/gfm/#tables-extension-), strikethrough,
syntax highlighting  of code,  task list.

Many processors which extend  {{< iref "#commonmark" "CommonMark" >}} use the syntax
which was used in {{< iref "#php-markdown-extra" "PHP Markdown Extra" >}}

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

The [specification](http://spec.commonmark.org/current) has its
[source on GitHub](http://spec.commonmark.org/). There is also a
[reference card](http://commonmark.org/help/) and an
[interactive tutorial)(http://commonmark.org/help/tutorial/).

You can test and convert on line your CommonMark document on the
[Dingus interactive translator](http://spec.commonmark.org/dingus/)
powered by _commonmark.js_.

John Mac Farlane also provide two implementations, [cmark](https://github.com/jgm/cmark)
written in C, and [commonmark.js](https://github.com/jgm/commonmark.js) in javascript.

[CommonMark-py](https://github.com/rtfd/CommonMark-py)
is a pure Python port of jgm's _commonmark.js_,

[recommonmark](http://recommonmark.readthedocs.io/en/latest/index.html) A
docutils-compatibility bridge to CommonMark which allows you to write CommonMark inside
of Docutils & Sphinx projects. recommonmark is written in python, it uses CommonMark-py,
[recommonmark source ](http://spec.commonmark.org/) is on GitHub.

Using recommonmark you can
[use Markdown in Sphinx](http://www.sphinx-doc.org/en/latest/markdown.html).

## GitHub Flavored Markdown {#gfm}

[Github Flavored Markdown - GFM](https://github.github.com/gfm/)
add to  {{< iref "#commonmark" "CommonMark" >}} few extensions.

One main difference is that newlines which are ignored in Standard
Markdown  are significative in GFM.

GFM disable also disable italicize parts of words, allow
strikethrough, fenced code block with <code>&#96;&#96;&#96;</code>
syntax higlighting with <code>&#96;&#96;&#96;python</code> like headers.

It also add a [table extension](https://github.github.com/gfm/#tables-extension-),
task lists, and few GitHub specific shortcuts.

-   [GitHub Help: Mastering markdown
    ](https://guides.github.com/features/mastering-markdown/)
    is an howto for
    [Github Flavored Markdown](https://github.github.com/gfm/).

-   [GitLab Flavored Markdown (GLFM)](https://docs.gitlab.com/ee/user/markdown.html)
    is the extension of CommonMark used in Gitlab.
-   [Stack Overflow MarkDown](http://stackoverflow.com/editing-help)
    is a standard MarkDown with some additions including
    [GFM pipe tables](https://github.github.com/gfm/#tables-extension-) and
    [Syntax highlighting for code
    ](http://stackoverflow.com/editing-help#syntax-highlighting)
    that uses [Google prettify
    ](http://google-code-prettify.googlecode.com/svn/trunk/README.html)

## MarkDown extensions

### Definition list

Definition list are not part of {{< iref "#commonmark" "Commonmark" >}} nor
{{< iref "#gfm" "Github Flavored Markdown" >}} but this is a common extension
which comes from {{< iref "#php-markdown-extra" "PHP Markdown Extra" >}}
with the syntax [PHP_Markdown_Extra definition list
](http://www.michelf.com/projects/php-markdown/extra/#def-list)

```markdown
definition list
:   a type of list were the header is a work, and
the body is the definition.
```

If you need to use only  {{< iref "#commonmark" "Commonmark" >}} or
{{< iref "#gfm" "Github Flavored Markdown" >}} you can include definition list as html
code with `<dl>`, `<dd>`, `<dt>` tags.

### Fenced code block
The syntax is [PHP Markdown Extra fenced code block
](http://www.michelf.com/projects/php-markdown/extra/#fenced-code-blocks) and was also
implemented in [Python Markdown fenced code blocks
](https://python-markdown.github.io/extensions/fenced_code_blocks/)
or [fenced code blocks for python markdown2
](https://github.com/trentm/python-markdown2/wiki/fenced-code-blocks).

Fenced code block are not truly _an extension_, they were not present in basic Markdown
but they are [part of CommonMark](https://spec.commonmark.org/curent/#fenced-code-blocks).


They are also
[part of GFM specification*](https://github.github.com/gfm/#fenced-code-blocks)
and described also in [Creating and highlighting code blocks - GitHub Docs
](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/creating-and-highlighting-code-blocks).

You can delimit code blocks either with
`~~~` or  <code>```</code>, instead of the four space indentation of code blocks in
basic Markdown.

Many processors allow highlighting of the code block by following the backticks or tildes
with the code language like:

```python
if True:
    print("hi")
```

The available languages and the library used to highlight the code depends on the
Markdown processor used.

GFM uses [linguist](https://github.com/github/linguist) with a huge
[list of grammar](https://github.com/github/linguist/blob/master/vendor/README.md)
and
[corresponding languages](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

Many markdown processors can render code highlight, including
{{< iref "#pandoc" "pandoc" >}},
{{< iref "#python-markdown" "Python MarkDown and python Markdown2" >}},
{{< iref "#goldmark" "goldmark" >}}, {{< iref "#blackfriday" "BlackFriday" >}},
{{< iref "#lowdown" "Lowdown" >}}, {{< iref "#cdiscount" "cdiscount" >}}
Maruku, {{< iref "#kramdown" "Kramdown" >}},
{{< iref "#markdown-it" "Markdown-It through a plugin" >}},
{{< iref "#multimarkdown" "MultiMarkdown" >}}.

### Toc  {#markdown_toc}

Automatic Table of content are not part of
[Common Mark Specification](https://spec.commonmark.org/current/)
nor [GitHub Flavored Markdown Spec](https://github.github.com/gfm/).

But many formatters can generate one.

In {{< iref "#kramdown" "Kramdown" >}} can
[generate a toc](https://kramdown.gettalong.org/converter/html.html#toc)
with the `{:toc}` construct.

{{< iref "#redcarpet" "Redcarpet" >}} README explain that *Redcarpet::Render::HTML_TOC*
generate a table of content.

In {{< iref "#markdown-python" "Python Markdown" >}}
you generate toc with
[Table of Contents extension](https://pythonhosted.org/Markdown/extensions/toc.html)
which is enabled by including:

```
[TOC]
```

{{< iref "#gitdown" "GitDown" >}} allow toc generation by including
`{"gitdown": "contents"}`

{{< iref "#pandoc" "Pandoc" >}} used with `--toc` or `--table-of-contents` generate a
table of content, you can control its depth with `--toc-depth`.

A toc can also be generated by {{< iref "#remarkable" "remarkable" >}},
{{< iref "#remark" "remark" >}}

#### Toc generators for Markdown

-   [DocToc](https://github.com/thlorenz/doctoc)  (MIT License)
    is a _node.js_ application to generates table of contents for markdown files inside
    local git repository. Links are compatible with anchors generated by github or other
    sites.
-   [gfm_toc_generator](https://github.com/gtaifu/gfm_toc_generator) (GPL)
    a Python utility to automatically generate the table of content for
    GitHub Flavored Markdown files.
-   [mdtoc](https://github.com/tallclair/mdtoc) (Apache License)
    is a go utility to generate a toc
-   <a name="markdown-content"></a>
    [markdown-contents](https://github.com/gajus/markdown-contents)  (MIT License)
    a _node.js_ application to  generate table of contents for a markdown document.
    It is used by {{< iref "#gitdown" "GitDown" >}}.
-   <a name="markdown-toc"></a>
    [markdown-toc](https://github.com/jonschlinkert/markdown-toc) (MIT Licence)
    a _node.js_ application to generate a markdown TOC
    It uses {{< iref "#remarkable" "remarkable" >}} and is also used by it to generate
    TOCs.  Also used by assemble, [verb](https://github.com/verbose/verb), and other
    projects.

    A CLI is also available.

-   {{< iref "#markedpp" "Markedpp" >}} includes a toc generator.
-   {{< iref "#markdown-pp" "Markdown-pp" >}} includes a toc generator.
-   If you use vim you can use the plugin
    [mzlogin/vim-markdown-toc](https://github.com/mzlogin/vim-markdown-toc)
    to generate table of contents n GFM link style, Redcarpet link style or
    GitLab link style for Markdown files.
-   For _Emacs_ the _elpa_ package
    [markdown-toc](https://github.com/ardumont/markdown-toc)
    generate a TOC in markdown file.



## Markdown formatters and linters

For Styling Markdown you can find some guides, which propose diverse conventions, often
incompatible. Some want ATX headers other Setext headers, some want a 2 space
indentation other 4 spaces, some accept indented code blocks, other only fenced code
block; some want a big line without soft break, others impose a 8O columns limit ....

-   [notslang/markdown-styleguide
    ](https://github.com/notslang/markdown-styleguide)
-   [Google Markdown style guide](https://google.github.io/styleguide/docguide/style.html).
-   [Ciro Santilli Markdown Style Guide](https://cirosantilli.com/markdown-style-guide/)
-   [Markdown style guide for about.gitlab
    ](https://about.gitlab.com/handbook/markdown-guide/)
    this is a style guide targeted to the use of {{< iref "#kramdown" "kramdown" >}}
    which is used for about.GitLab.com. _GitLab.com use instead the format
    [GitLab Flavored Markdown (GLFM)](https://docs.gitlab.com/ee/user/markdown.html)_

The linters or reformatters force some style convention. but often the style depends
on the underlying processor and is not even documented.

-   [shurcool/markdownfmt](https://github.com/shurcooL/markdownfmt) (MIT License)
    is a formatter for commonmark written in go. It does not support front matter
    nor commonmark extensions. It has an emacs plugin
    [emacs-markdownfmt](https://github.com/nlamirault/emacs-markdownfmt),
    and a vim pluginTh
    [vim-markdownfmt](https://github.com/moorereason/vim-markdownfmt).

    The package does not provide any specification of the rules applied,
    I just noticed that it does not allow ATX headers, and if reformat all my text in a
    long line deleting any newline inside a paragraph.
-   [Kunde21/markdownfmt](https://github.com/Kunde21/markdownfmt) (MIT License)
    is a fork in 2018 of shurcool/mdformat that switched to Goldmark instead of
    Blackfriday and support GFM, fenced code block, ATX Headers by default.
    It provide an option to allow soft line break. It enforce a non configurable two
    space indent.
-   [mdfmt](https://github.com/moorereason/mdfmt) (MIT License)
    add to shurcool markdownfmt the support of front matter.
-   [mdformat](https://github.com/executablebooks/mdformat) 5MIT License)
    is a CommonMark compliant Markdown formatter

    -   [mdformat documentation](https://mdformat.readthedocs.io/en/stable/)
-   [notslang/tidy-markdown](https://github.com/notslang/tidy-markdown)  (GPL 3.0)
    a npm package for fixing formatting mistakes and converting basic HTML &
    Unicode into their Markdown equivalents. It supports front matter.
-   [markdownlint](https://github.com/DavidAnson/markdownlint)
    a Node.js style checker and lint tool for Markdown/CommonMark files.

    -   [markdownlint-cli2](https://github.com/DavidAnson/markdownlint-cli2)
        is a command-line interface for linting Markdown/CommonMark files with the
        markdownlint library
-   [Prettier](https://github.com/prettier/prettier) (MIT License)
    a node.js formatter for javaScript, TypeScript, Flow, JSX, JSON CSS, SCSS, Less
    HTML, Vue, Angular GraphQL, Markdown, YAML. Prettier has a builtin
    [CLI](https://prettier.io/docs/en/cli.html) and can be used with the emacs packages
    [apheleia](https://github.com/radian-software/apheleia),
    [prettier.el](https://github.com/jscheid/prettier.el),


# Markdown processors

[w3.org List of Markdown Implementations
](http://www.w3.org/community/markdown/wiki/MarkdownImplementations).

## Awk
-   _md2x_ is an awk script, The  original 2006 scripitself authored by Jesus Galan (yiyus) is named
    [txt2html.awk
    ](http://newsgroups.derkeiler.com/Archive/Comp/comp.lang.awk/2007-08/msg00089.html)
    or
   cense) [markdown.awk
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

-   <a name="cmark"></a>[cmark](https://github.com/jgm/cmark) (MIT License)
    by John MacFarlane is the reference implementation of
    {{< iref "#commonmark" "CommonMark" >}}  in C.

    It is the reference implementation of cmark.
    _cmark_ is in Debian, bindings for python are in the package _python3-cmark_.
-   <a name="cmark-gfm></a>[cmark-gfm](https://github.com/github/cmark-gfm)
    is a fork of {{< iref "#cmark" "cmark" >}} which add the support for
    {{< iref "#gfm" "Github Flavored Markdown" >}}.
    It is packaged in Debian.

    TThere is a rust port {{< iref "comrak" "Comrak" >}}, and bindings for _cmark-gfm_
    in haskell, and also in python
    [cmarkgfm](https://github.com/theacodes/cmarkgfm) available in Debian under the name
    _python3-cmarkgfm_.
-   <a name="discount"></a>[Discount](http://www.pell.portland.or.us/~orc/Code/discount/)
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

    It is nearly compatible with {{< iref "#gfm" "GitHub Flavored Markdown" >}}
    with only
    [small differences](https://github.com/hoedown/hoedown/wiki/Spec-differences)

    -   [Hoedown Wiki](https://github.com/hoedown/hoedown/wiki)
    -   [Hoedown bindings
        ](https://github.com/hoedown/hoedown/wiki/Bindings):
        Apache module, Elixir, Go, LuaJIT,
        [Midnight Dynamite](https://github.com/gradha/midnight_dynamite) _(NIM)_,
        Node.JS, Perl 5, PHP, ([Hoep](https://github.com/Anomareh/Hoep) _( Python)_,
        [python-hoedown](https://github.com/hhatto/python-hoedown)),
        {{< iref "#misaka" "misaka" >}} _(Python)_,
        [Rust doc](http://doc.rust-lang.org/rustdoc/html/markdown/),
        Tcl {{< iref "markdown#redcarpet" "Redcarpet" >}} _(Ruby)_.
    -   [Hoextdown](https://github.com/jasharpe/hoextdown) (MIT License)
        is an extension to Hoedown adding Special Attributes, Task Lists,
        Line Continue, Header ID, Fenced Script, Script Tags, Meta Block.

-   <a name="lowdown">[lowdown](https://kristaps.bsd.lv/lowdown/) (ISC Licence)
    is a C markdown processor, it is a fork of {{< iref "#hoedown" "Hoedown" >}}, see
    the home page for differences. A major feature additions is the troff ouput format.

    lowdown internally converts markdown to an AST. It allows complex treatments like
    the [Diffing Engine](khttps://kristaps.bsd.lv/lowdown/diff.html) which shows the
    difference between two markdown trees in markdown.

    lowdown produces HTML5 output in XML mode with `-thtml`, LaTeX documents with
    `-tlatex`, “flat” OpenDocument XML documentx with `-tfodt`, Gemini with `-tgemini`,
    roff documents with `-tms` and `-tman1` outputs (via groff or mandoc), or directly
    on ANSI terminals with `-tterm`.

    The lowdown Markdown syntax includes extensions such as fenced code, tables,
    superscript and subscript, typographer, mathematic, definition list, task list,
    footnotes.  It is described in the man page
    [lowdown(5)](https://manpages.debian.org/unstable/lowdown/lowdown.5.en.html).

    A lowdown package is available in Debian.

    -   [GitHub - lowdown](https://github.com/kristapsdz/lowdown)
-   <a name="mdp"></a>[mdp](https://github.com/visit1985/mdp)(GPL)
    is a command-line based markdown presentation tool. It renders
    markdown as text formated with ansi escape sequences.
    _mdp is in Debian._
-   <a name="multimarkdown"></a>
    [multimarkdown](http://fletcherpenney.net/multimarkdown/) (GPL and MIT licenses)
    is an extension to markdown. It is written in C and extend {{< iref "#peg"
    "peg-markdown" >}} to work with complete documents and convert them into other
    formats, including complete XHTML documents, LaTeX, PDF, OpenDocument. It allows
    like php-markdown tables and definition list and add metadata, header and footer,
    footnotes, MathJax, attributes to links and images, cross-references.
    -   [peg-multimarkdown GitHub Repository](https://github.com/fletcher/peg-multimarkdown)
    -   [Multimarkdown manual (pdf)](http://fletcher.github.com/peg-multimarkdown/mmd-manual.pdf)
    -   [MultiMarkdown CMS](http://fletcherpenney.net/multimarkdown/cms/)
        [MultiMarkdown CMS GitHub repository](https://github.com/fletcher/MultiMarkdown-CMS)
        is a CMS for markdown by Fletcher T. Penney.
        -   Wikipedia {{< wp "multimarkdown" >}}
-   <a name="peg-markdown"></a>
    [peg-markdown](https://github.com/jgm/peg-markdown) (GPL)
    by John MacFarlane _author of pandoc_ is an implementation of markdown in C, using a
    PEG grammar.  John MacFarlane has also written an haskell version
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
    by John MacFarlane is a {{< iref "#Commonmark" "CommonMark" >}} markdown
    implementation in javascript.  Instead of converting Markdown directly to HTML, as
    most converters do, commonmark.js parses Markdown to an AST (abstract syntax tree),
    and then renders this AST as HTML. This opens up the possibility of manipulating the
    AST between parsing and rendering.
-   <a name="dillinger"></a>[Dillinger](http://dillinger.io/) (MIT License)
    (BSD like licence) is a node.js HTML5 Markdown editor. It is able to work with cloud
    services as Dropbox or GitHub but allow also to export your document in source
    format and html to any local location. It uses the
    {{< iref "#showdown" "showdown module" >}}.
    -   [Dillinger GitHub repository](https://github.com/joemccann/dillinger)
-   [Docter](https://github.com/alampros/Docter) is a _node.js_xs application
    to render Github Flavored Markdown by using github's own
    {{< iref "#redcarpet" "Redcarpet" >}} library. It has a big requirement list
    including NodeJS, NPM, Ruby, Rubygems, {{< iref "#redcarpet" "Redcarpet" >}},
    pygments.rb.
-   <a name="node_gfm"></a>[node gfm](https://github.com/gagle/Node-GFM) (MIT License)
    by Gabriel Llamas is a _node.js_ application to render
    GitHub Flavored Markdown and allow editing them in the browser.
-   <a name="gfms"></a>[gfms](https://github.com/ypocat/gfms) (MIT License)
    by Juraj Vitko  is a Node application to render GitHub Flavored Markdown.
-   <a name="gitdown"></a>[Gitdown](https://github.com/gajus/gitdown) (BSD licence)
    is a _node.js_ markdown preprocessor  for
    {{< iref "#gfm" "GitHub flavoured Markdown" >}}. It can generate a table of contents
    with {{< iref "#markdown-content" "markdown-content" >}}, include documents, use
    variables, generate id for sections, generate bages.  Gitdown is designed to be run
    using build systems such as Gulp or Grunt.
-   <a name="markdown-it"></a>[markdown-it](https://github.com/markdown-it/markdown-it)
    (MIT License)
    A _node.js_ library providing a markdown formatter.

    It supports {{< iref "#commonmark" "Commonmark" >}} and provides
    [extensions](https://github.com/markdown-it/markdown-it#syntax-extensions)
    and third party
    [plugins](https://www.npmjs.com/search?q=keywords:markdown-it-plugin)
    including {{< iref "#gfm" "GFM" >}} tables and definition lists, footnotes, task
    lists, Katex, file inclusion, mathjax, typographer ...

    _node-markdown-it_ package is in Debian.
    -   [markdown-it online demo](https://markdown-it.github.io/)
-   <a name="marked"></a>[marked](https://github.com/chjj/marked)
    (MIT License) by Christopher Jeffrey is
    a node.js markdown compiler, written in javascript, it is said as
    quick as the C markdown compiler and implements
    {{< iref "#commonmark" "CommonMark" >}} and
    {{< iref "#gfm" "GitHub Flavored Markdown" >}} features.

    _marked_ is packaged in Debian.
-   [marked-man](https://github.com/kapouer/ronnjs) (BSD License)
    uses the javascxoript converter
    {{< iref "#marked" "marked" >}} to convert markdown to roff.
-   <a name="markedpp"></a>[markedpp](https://github.com/commenthol/markedpp)
    is a preprocessor for markdown.

    It supports the following extensions:
    Generation of a "Table of Contents", automatic numbering of headings, include files,
    sorted collection of references, autonumbering of ordered lists,
    automatic update of heading identifiers

    It support  autoid for {{< iref "#marked" "Marked" >}},
    {{< iref "#markdown-it" "markdown-it"  >}},
    {{< iref "#unified" "unified" >}},
    {{< iref "#pandoc" "pandoc" >}},
    [github.com](https://github.compare), [gitlab.com](https://gitlab.com),
    [bitbucket.org](https://bitbucket.org),  [ghost.org](https://ghost.org).

    _node-marked-man_ is packaged in Debian.
-   [mdx](https://github.com/mdx-js/mdx) (MIT License)
    allow to use {{< iref "javascript#jsx" "JSX" >}} in your markdown documents. You can
    import components, like interactive charts or notifications, and export metadata.
-   [pagedown](http://code.google.com/p/pagedown/) (MIT License)
    is the version of Attacklab's Showdown and WMD as used on Stack
    Overflow.  It includes a converter to HTML that can be used both
    in the browser, and on the server using Node.js. , a Markdown
    editor with realtime preview of the generated HTML, and a few
    useful plugins.

    The GitHub repository has no documentation, for the syntax we can refer to the
    showdown project or the [StackExchange Editing help
    ](https://stackoverflow.com/editing-help).
-   <a name="remarkable"></a>[jonschlinkert/remarkable
    ](https://github.com/jonschlinkert/remarkable) (MIT License)
    a node.js parser used by Facebook, Docusaurus and  others. It support
    {{< iref "#commonmark" "Commonmark" >}} with extensions for
    {{< iref "#gfm" "GFM" >}} tables, footnotes, abbreviations ..., typographer and URL autolinking
    support.  It can to generate a table of contents with the
    [markdown-toc](https://github.com/jonschlinkert/markdown-toc) from the same author.
    {{< iref "#markdown-toc" "markdown-toc" >}}.
    Gulp and metalsmith plugins are available.
    -   [remarkable online demo](https://jonschlinkert.github.io/remarkable/demo/)
-   <a name="remark"></a>[Remark](https://github.com/remarkjs/remark) (MIT License)
    is a markdown javascript parser and compiler.
    It is powered by the syntax tree transformer
    [unified](https://unifiedjs.github.io/)
    and uses plugins to translate markdown.
    It can process markdown to html with
    [remark-html](https://github.com/remarkjs/remark-html)
    or man pages with
    [remark-man](https://github.com/remarkjs/remark-man).
    Plugins allow also to check Markdown code style, transform safely to React, add a
    table of contents.
-   <a name="showdown"></a>[showdown](https://github.com/coreyti/showdown)
    by  John Fraser is a javascript formatter for markdown.

    Showdown implement a [markdown syntax
    ](https://github.com/showdownjs/showdown/wiki/Showdown's-Markdown-syntax)
    which extend the vanilla basic syntax, including fenced code block, pipe tables.

    Showdown is compatible with vanilla John Gruber perl markdown, but it differs from
    CommonMark on some point including the list breaking.

    It is used by [wmd editor](http://wmd-editor.com/) and
    {{< iref "#dillinger" "Dillinger" >}}.

    [Showdown & Highlight.js - Markdown and syntax highlighting in Javascript
    ](http://softwaremaniacs.org/playground/showdown-highlight/)
    provides  _showdown_ on-line as markdown converter.
-   [unified](https://unifiedjs.github.io/)
    is a syntax tree transformer
    -   [awesome-unified](https://github.com/unifiedjs/awesome-unified).
    It is used in
    -   awesome-lint to make it easier to create and maintain Awesome lists.
    -   how-to-markdown to teach markdown
    -   documentation.js to generate formatted docs
    -   [readability](https://github.com/wooorm/readability)
        measures ease of reading of text. It uses several
        formulas. Green colored texts should be readable for your target
        audience.

## Go

-   <a name="blackfriday"></a>[Blackfriday](https://github.com/russross/blackfriday)
    (BSD License)
    started as a translation from C of {{< iref "#sundown" "Sundown" >}}.
    It contain extensions, including table support, definition lists, fenced code blocks,
    autolinks, strikethroughs, non-strict emphasis, etc.

    It is not completly compatible with {{< iref "#commonmark" "Commonmark" >}} and its
    lists are not compatible with GFM. It is one reason of Hugo switching to GoldMark.

    It was the default formatter for {{< iref "static_sites#hugo" "Hugo" >}} until
    version 0.60.

    -   [blackfriday-latex](https://gitlab.com/ambrevar/blackfriday-latex) (MIT License)
        is a LaTeX renderer for the Blackfriday Markdown processor (v2).
    -   [Depado/bfchroma](https://github.com/Depado/bfchroma/)
        integrates Chroma syntax highlighter as a Blackfriday renderer.

-   <a name="goldmark"></a>[Goldmark](https://github.com/yuin/goldmark/) (MIT License)
    Goldmark is compatible with {{< iref "#commonmark" "CommonMark" >}}
    and has many built-in extensions like

    -   [GFM extensions](https://github.github.com/gfm): Strikethrough, Autolinks,
        Task list items,
        [GFM table](https://github.github.com/gfm/#tables-extension-),
    -   PHP Markdown Extra:
        [Definitions Lists](https://michelf.ca/projects/php-markdown/extra/#def-list),
        [Footnotes](https://michelf.ca/projects/php-markdown/extra/#footnotes)
    -   [syntax-highlighting for fenced code blocks
        ](https://github.com/yuin/goldmark-highlighting) using the
        {{< iref "source_code#chroma" "Chroma" >}} syntax highlighting Go library.

    It is the default formatter for {{< iref "static_sites#hugo" "Hugo" >}}.

-   <a name="zmarkdown"></a>[Zmarkdown](https://github.com/zestedesavoir/zmarkdown)
    (MIT Licence)
    a javascript replacement of {{< iref "#python-zmarkdown" "Python-Zmarkdown" >}}
    the Markdown engine that was powering [Zeste de Savoir](https://zestedesavoir.com).

    It uses {{< iref "#remark" "remark" >}} and its
    [__MDAST__](https://github.com/wooorm/mdast) syntax tree,
    [__rehype__](https://github.com/rehypejs/rehype) (for HTML processing) and
    [__textr__](https://github.com/A/textr) (text transformation framework). It also
    provides LaTeX output via
    [__rebber__](https://github.com/zestedesavoir/zmarkdown/tree/master/packages/rebber#rebber--)

    [zestedesavoir/zmarkdown: Live demo](https://zestedesavoir.github.io/zmarkdown/)

-   [vmd](https://github.com/yoshuawuyts/vmd) (MIT Licence)
    Preview GFM markdown files in a separate window.
    It can be used in Emacs with
    [vmd-mode](https://github.com/blak3mill3r/vmd-mode) (MIT Licence)

## Haskell

See {{< iref "#pandoc" "Pandoc" >}} below.

-   [MMark](https://github.com/mmark-md/mmark) (BSD Licence)
    is an haskell markdown processor. It has a _strict_ behavior, i.e. it tries to
    detect and report errors. It is mostly compatibe with common mark, and allows GFM
    extensions. It exibhit nonetheless many differences, explained on the Home Page.

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
-   [parsedown](https://github.com/erusev/parsedown) (MIT License)
    a single file PHP parser without dependencies that understand GFM.
    _parsedown_ is packaged in Debian.
    -   [parsedown-extra](https://github.com/erusev/parsedown-extra)
        Markdown Extra Extension for Parsedown. Packaged in Debian.
    -   [Parsedown  Demo](https://parsedown.org/demo)

## Python {#markdown-python}


-   [Grip](https://github.com/joeyespo/grip) (MIT LIcense)
    by Joe Esposito
    is a {{< iref "python_web#flask" "Flask" >}} application
    to preview or output html of a Markdown file as it looks on GitHUb
    wikis. It has support for GitHub flavored Markdown.
-   [Hoep](https://github.com/Anomareh/Hoep)
    an {{< iref "#hoedown" "hoedown" >}} binding for Python.
-   [python-hoedown](https://github.com/hhatto/python-hoedown)
    an {{< iref "#hoedown" "hoedown" >}} binding for Python.
-   <a name="markdown-pp"></a>[Markdown Preprocessor
    ](http://noswap.com/projects/markdownpp/) (BSD like licence)
    is a Python module designed to add a preprocessor on top of  Markdown.
    It is aimed at creating larger technical documents.
    [GitHub: markdown-pp](https://github.com/jreese/markdown-pp).
    It allows inclusions of markdown code files or url, generate a table of content,
    create an index of references, and to expand
    latex code with
    [QuickLatex](http://www.holoborodko.com/pavel/quicklatex/)
-   <a name="mardown-it-py"></a>
    [markdown-it-py](https://github.com/executablebooks/markdown-it-py) (MIT License)
    is a port of {{< iref "#mardown-it" "NodeJS markdown_it" >}} to python
    It features CommonMark support, extensions, syntax plugins.

    _markdown-it-py_ is the markdown processor used in
    {{< iref "myst" "MyST" >}}.
    -   [markdown-it-py documentation](https://markdown-it-py.readthedocs.io/en/latest/)
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
-   <a name="mistletoe"></a>[mistletoe](https://github.com/miyuchina/mistletoe) (MIT License)
    A fast, extensible and spec-compliant Markdown parser in pure Python.
    Mistletoe if CommonMark compliant and provide Strikethrough and tables natively and
    plugins for toc, GitHub wiki links, Pygment renderer, Mathjax, Jira Markdown,
    scheme..

    It provides a command line client and can output HTML, Latex and AST. It is the
    fastest of fully CommonMark compliant python parser, even if mistune is three time
    quicker.  The main drawback of mistletoe is the lack of documentation.

    Debian has a _python3-mistletoe_ package.

-   [mistune](https://github.com/lepture/mistune) (BSD-3 License)
    the fastest Python Markdown parser. It provides three renderers HTML, ReST, Markdown.
    builtin plugins allow strikethrough, footnotes,, table, url, task_lists, def_list,
    abbr, mark, insert, superscript, subscript, math, ruby, spoiler.

    mistune is not fully compliant with CommonMark, which allows it to go faster but it
    cannot fully understand some complex embedded constructs. It is explained
    [by Mi Yu the mistletooe author
    ](https://github.com/miyuchina/mistletoe/blob/master/performance.md)

    It provides a command line client and is packaged in Debian.

    -   [Mistune  documentation](https://mistune.lepture.com/en/latest/)
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
    [host your docs in github pages](http://limodou.github.io/parm/README.html#toc13).
    It includes also a rst to markdown converter.
    -   [GiThub Par](https://github.com/limodou/par).
    -   [GiThub Parm](https://github.com/limodou/parm).
-   <a name="myst"></a>[MyST](https://myst-parser.readthedocs.io/en/latest/)a (MIT License)
    A Sphinx and Docutils extension to parse the _MyST_ extended Markdown for technical
    and scientific documentation.

    Mostly all docutils roles, docutils directives, Sphinx roles, or Sphinx directives
    can be used in MyST.

    _MyST_ is part of
    [The Executable Books Project](https://executablebooks.org/en/latest/)
    which provide an environment to build
    {{< iref "python_libraries#jupyter" "Jupyter" >}} books.

    The markdown parsing in MyST is done by
    {{< iref "#markdown-it-py" "markdown-it-pi" >}}.

    -   [MyST-Parser - GitHub](https://github.com/executablebooks/MyST-Parser)
    -   [RST-to-MyST](https://rst-to-myst.readthedocs.io/en/latest/)
        is a ool for converting ReStructuredText to MyST Markdown.
    -   [MySTyc - Online conversion from reStructuredText to MyST
        ](https://astrojuanlu.github.io/mystyc/)
    -   [mystjs](https://github.com/executablebooks/mystjs)
        Parser and CLI for MyST Markdown, built in Javascript.

-   <a name="python-zmarkdown"></a>
    [Python-ZMarkdown](https://github.com/zestedesavoir/Python-ZMarkdown)
    fork of Python-Markdown including somes improvements suitables for
    [Zeste de savoir](https://zestedesavoir.com/). It is now replaced by the Javascript
    package {{< iref "#zmarkdown" >}}.

### Python-Markdown {#python-markdown}
[Python-Markdown](https://python-markdown.github.io) (BSD+GPL)
is a python converter is, it allows many
[extensions](https://python-markdown.github.io/extensions).

See also the {{< iref "markdown_cheatsheet" "Mardown CheatSheet" >}} for python-markdown.


There is a [Python-Markdown version 2 or markdown2
](https://github.com/trentm/python-markdown2)
also [in PyPi](https://pypi.python.org/pypi/markdown2).

-   <a name="python-markdown-extra"></a>[Python-Markdown Extra
    ](https://python-markdown.github.io/extensions/extra/)
    or for markdown2:
    [Python Markdown2 Extra
    ](https://github.com/trentm/python-markdown2/wiki/Extras)
    regroup a set of extensions that imitate and extend
    {{< iref "#php" "php-markdown extra" >}}
    by adding :

    -   [abbreviations](https://python-markdown.github.io/extensions/abbreviations/),
    -   [attribute lists](https://python-markdown.github.io/extensions/attr_list/)
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
        ](https://python-markdown.github.io/extensions/toc/)
        automatically generates id attributes for the header elements
        _(except those for which you define a specific header attribute)_.
        This is enabled by default;

        To illustrate this extension I put here a
        `{{< iref "#attribute" "reference to attribute list" >}}`
        {{< iref "#attribute" "reference to attribute list" >}}.

    -   [definition lists
        ](https://python-markdown.github.io/extensions/definition_lists/)
        with the same syntax that [PHP_Markdown_Extrai
        ](http://www.michelf.com/projects/php-markdown/extra/#def-list)
        like

    -   [fenced code blocks
        ](https://python-markdown.github.io/extensions/fenced_code_blocks/)
        or [fenced code blocks for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/fenced-code-blocks)
        have the same syntax than [PHP Markdown Extra
        ](http://www.michelf.com/projects/php-markdown/extra/#fenced-code-blocks)
        or alternatively [GitHub Flavored Markdown
        ](https://help.github.com/en/github/writing-on-github/creating-and-highlighting-code-blocks).

        They can delimit code blocks either with the PHP-Markdown
        syntax `~~~` or the GitHub GFM syntax <code>```</code>.

    -   [footnotes](https://python-markdown.github.io/extensions/footnotes/)
        or [footnotes for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/footnotes).

        The syntax is the same than  [PHP Markdown Extra
        ](http://michelf.com/projects/php-markdown/extra/#footnotes)

        Example:

        ```markdown
        Footnotes[^1] have a label[^@#$%] and the footnote's content.

        [^1]: This is a footnote content.
        [^@#$%]: A footnote on the label: "@#$%".
        ```

    -   [tables](https://python-markdown.github.io/extensions/tables/)
        or
        [tables for markdown2
        ](https://github.com/trentm/python-markdown2/wiki/tables)
        have the same syntax than  [PHP Markdown Extra
        ](https://michelf.ca/projects/php-markdown/extra/#table).

        -   [wiki-table for markdown2
            ](https://github.com/trentm/python-markdown2/wiki/wiki-tables)
            support Google Code wiki-style tables.

        -   python-markdown third party extension
            [Markdown GridTables
            ](https://github.com/smartboyathome/Markdown-GridTables/)
            add grid tables as seen in ReSt.
    -   The [PHP Markdown Extra Emphasis
        ](https://michelf.ca/projects/php-markdown/extra/#em)
        which treat internal underscore literally is the default in Python Markdown.

        python-markdown2 add an extension
        [code-friendly](https://github.com/trentm/python-markdown2/wiki/code-friendly)
        that disable all use of emphasis and strong with a simple or double underscore.

-   The other official extensions to python-markdown are
    [listed in the doc](https://python-markdown.github.io/extensions/), the
    following ones are enabled by default:

    -   The [CodeHilite extension
        ](https://python-markdown.github.io/extensions/code_hilite/)
        adds code/syntax highlighting to standard Python-Markdown code blocks using
        {{< iref "source_code#pygments" "Pygments" >}}
        It can be used with fenced blocks, or by using
        `:::<language>`
        as the first line of indented code blocks.

        The list of languages is in
        [Pygments language list](http://pygments.org/languages/) and
        [Pygments lexers](http://pygments.org/docs/lexers/).

        Python-markdown has this separate extension to highlight fenced code blocks, in
        Python-markdown2 when you have the pygment library a fenced code block with a
        language attribute is highlighted.

    -   [Meta-Data](https://python-markdown.github.io/extensions/meta_data/)
        or [python-Markdown2 Metadata
        ](https://github.com/trentm/python-markdown2/wiki/metadata)
        adds a syntax for defining meta-data about a document.
    -   [Sane Lists
        ](https://python-markdown.github.io/extensions/sane_lists/)
        allow the mixing of list types. In other words, an ordered
        list will not continue when an unordered list item is
        encountered and vice versa.
    -   [Table of Content
        ](https://https://python-markdown.github.io/extensions/toc/)
        generates a Table of Contents from a Markdown document
        when encountering a `[TOC]` markup.
    -   [WikiLinks
        ](https://pythonhosted.org/Markdown/extensions/wikilinks.html)
        converts any [[bracketed]] word in a link.

-   There are also numerous
    [third party extensions of python-markdown
    ](https://github.com/waylan/Python-Markdown/wiki/Third-Party-Extensions),
    and a list of
    [python-marmkdown2 extensions](https://github.com/trentm/python-markdown2/wiki/)
    in the Pyhton-Markdown2 wiki.

## Ruby
-   <a name="commonmarker">[commonmarker](https://github.com/gjtorikian/commonmarker)
    (MIT license) is a ruby wrapper for Rust's {{< iref "#comrak" "comrak" >}}
    _CommonMark and GFM parser with extensions_, it is the
    processor used in Gitlab.com an implement the [GitLab Flavored Markdown
    (GLFM)](https://docs.gitlab.com/ee/user/markdown.html).

    _ruby-commonmarker_ is in Debian.
-   <a name="kramdown"></a>[kramdown](http://kramdown.gettalong.org/)
    a pure-Ruby Markdown-superset converter. It can parse
    {{< iref "#gfm" "GFM" >}} extensions. It replaces the now obsolete
    [Maruku](https://github.com/bhollis/maruku).

    Kramdown is packaged in Debian.
-   <a name="redcarpet"></a>[redcarpet](https://github.com/vmg/redcarpet) (MIT License)
    is a Ruby library for Markdown processing.
    It is based on {{< iref "#sundown" "sundown" >}} and accept the same extensions.

    _ruby-redcarpet_ is a Debian package.
-   [ronn](https://github.com/apjanke/ronn-ng) (MIT License)
    is a ruby application to build a man page from markdown source.

    The accepted syntax is defined in [ronn-format(7)
    ](https://manpages.debian.org/unstable/ruby-ronn/ronn-format.7.en.html)
    it includes basic markdown, a non standard variant of definition list, but
    no table. The _ronn-format_  manpage also give a last of commonly used sections
    in man pages.
-   [word-to-markdown](https://github.com/benbalter/word-to-markdown)
    (MIT License)
    is a ruby gem to convert Microsoft Word documents to Markdown.
    It needs libreoffice, and can be used in command line. There is
    also a web service, an istance is at
    [Online Word to Markdown converter](https://word-to-markdown.herokuapp.com/).

## Rust

-   <a name="comrak"><a>[comrak](https://github.com/kivikakk/comrak) (MIT like Licenses)
    is a port in rust of {{< iref "cmark-gfm" "cmark-gfm" >}} it supports
    {{< iref "#gfm" "Github Flavored Markdown" >}}, and add other extensions, which must
    be explicitly enabled: _Superscript_, _Header IDs_, _Footnotes_,
    _Description lists_, _Front matter_, _Shortcodes_.

    It is used by GitLab.com through the ruby bindings
    {{< irmef "#commonmarker" "Commonmarker" >}} to implement the
    [GitLab Flavored Markdown (GLFM)](https://docs.gitlab.com/ee/user/markdown.html).
-   [Rust Markdown Module](http://doc.rust-lang.org/rustdoc/html/markdown/).
-   <a name="pulldown-cmark"></a>
    [pulldown-cmark](https://github.com/raphlinus/pulldown-cmark) (MIT License)
    is a rust pulldown parser for {{< iref "#commonmark" "CommonMark" >}} with
    optional support of footnotes, Github flavored tables, task lists and strikethrough.
    It is packaged in Debian.

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

To many formats:

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
