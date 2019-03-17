<!--
.. description:
.. date: 2015-06-10
.. slug: asciidoc
.. tags:
.. link:
.. title: Asciidoc
-->

[TOC]

# References
-   [Asciidoc](http://www.methods.co.nz/asciidoc/) (GPL)
    is a text document format for writing short documents,
    articles, books, UNIX man pages, Beamer and Slidy slide shows.
    The asciidoc formatter is written in python.
    AsciiDoc files can be translated to latex, (X)HTML, HTML5,
    man-troff, epub, DocBook, and from DocBook to pdf, man, chunked
    html. Asciidoc is the documentation format used by the
    [git source code management system](/node/scm "Internal reference").
-   [AsciiDoc cheatsheet](http://powerman.name/doc/asciidoc)
    by Alex Efros. He also provides a [compact theme for asciidoc
    ](http://powerman.name/download/asciidoc/).
-   [O'Reilly atlas asciidoc guide
    ](http://chimera.labs.oreilly.com/books/1230000000065/ch04.html),
    [O'Reilly AsciiDoc Indexing Guidelines
    ](http://chimera.labs.oreilly.com/books/1234000001578/ch02.html)
-   [oreillymedia/asciidoctor-htmlbook
    ](https://github.com/oreillymedia/asciidoctor-htmlbook) is a set of
    templates for asciidoctor.
-   [opendevise/asciidoc-samples
    ](https://github.com/opendevise/asciidoc-samples/blob/master/article.adoc)
    repository contains asciidoc samples to test GitHub rendering, you
    can look at the [rendered article]
    ](https://gihub.com/opendevise/asciidoc-samples/blob/master/article.adoc).
    For a larger example look at [GitHub Guides in AsciiDoc
    ](https://github.com/opendevise/github-guides-asciidoc).
-   [Asciidoc Syntax Quick Summary
    ](http://xpt.sourceforge.net/techdocs/nix/tool/asciidoc-syn/ascs01-AsciiDocMarkupSyntaxQuickSummary/)
-   [Using DocBook toolchain
    ](http://xpt.sourceforge.net/techdocs/nix/tool/asciidoc-usg/ascu04-UsingDocBooktoolchain/)
-   [LaTeX backend for Asciidoc
    ](http://www.methods.co.nz/asciidoc/latex-backend.html)
-   [asciidoc google group
    ](https://groups.google.com/forum/#!forum/asciidoc)
-   [Asciidoctor](http://asciidoctor.org/) (MIT license)
    is an implementation of AsciiDoc in Ruby that converts
    AsciiDoc markup into HTML 5, DocBook 4.5.
    -   [Asciidoctor user manual
        ](http://asciidoctor.org/docs/user-manual).
    -   [GitHub: asciidoctor / asciidoctor
        ](https://github.com/asciidoctor/asciidoctor).
    -   [asciidoctor-htmlbook
        ](https://github.com/oreillymedia/asciidoctor-htmlbook)
        is O'Reilly set of templates for the htmlbook backend for Asciidoctor.
    -   [asciidoctor / asciidoctor.js
        ](https://github.com/asciidoctor/asciidoctor.js) (MIT license)
        uses [Opal](http://opalrb.org/) Ruby-to-JavaScript cross compiler
        to translate Asciidoctor to JavaScript, and
        bring AsciiDoc to the browser!
-   [Asciidoc compared to Markdown
    ](http://asciidoctor.org/docs/user-manual/#compared-to-markdown)
    from Asciidoctor user manual.


# Asciidoc editing.

-   For Emacs we have:
    -   [adoc-mode]( https://github.com/sensorflo/adoc-mode/wiki)
        It emphasizes on the idea that the document is highlighted so
        it pretty much looks like the final output. What must be bold
        is bold, what must be italic is italic etc.  Meta characters
        are naturally still visible, but in a faint way, so they can
        be easily ignored.
    -   [doc-mode Emacs Mode for AsciiDoc Fontlocking
        ](http://xpt.sourceforge.net/tools/doc-mode/) _2006_


-   AsciiDoctor [Editing AsciiDoc with Live Preview
    ](http://asciidoctor.org/docs/editing-asciidoc-with-live-preview/)
-   [Asciidoctor.js
    ](https://chrome.google.com/webstore/detail/asciidoctorjs-live-previe/iaalpfgpbocpdfblpnhhgllgbdbchmia)
    live preview plugin for chrome browser.
-   [AsciidocFX](https://www.asciidocfx.com/)(Apache License)
    is a javaFX8 document editor to build PDF, Epub, Mobi and HTML
    books, documents and slides from asciidoc and markdown source. It
    includes an Epub viewer.
    -   [GitHub: AsciidocFX](https://github.com/asciidocfx/AsciidocFX)
-   [Brackets
    ](https://github.com/adobe/brackets/wiki/How-to-Use-Brackets)
    is an editor with an [asciidoc preview extension
    ](https://github.com/asciidoctor/brackets-asciidoc-preview).
-   [Atom](https://atom.io)
    has many extensions for asciidoc, including a [toolset
    ](https://atom.io/packages/asciidoc-assistant), including  the
    syntax, the completion and live preview using asciidoctor.js,
    if you have a complete asciidoctor ruby installation there is an
    [asciidoctor preview package
    ](https://atom.io/packages/asciidoctor-preview), the asciidoc
    rendering can also be done with [pandoc package
    ](https://atom.io/packages/pandoc).
    The [ultra-sync package](https://atom.io/packages/ultra-sync)
    can keep your source code and preview in sync.
-   On Ios we can [Setup Textastic app to write AsciiDoc on iOS
    ](https://www.makzan.net/2015/10/07/setup-textastic-app-to-write-asciidoc-on-ios/)

# Static site generators using asciidoc:
-   [AsciiDoc Website Builder
    ](http://awb.sourceforge.net/).
-   [Hyde](/node/static_sites#hyde "internal link") written in python.
-   [AsciiDocGen](http://dbixjcl.org/jcl/asciidocgen/asciidocgen.html)
    (Artistic License) written in perl.
-   [Gollum](https://github.com/gollum/gollum/) (MIT License)
    a ruby Wiki with git  backend  _not static!_
-   [Awestruct](http://awestruct.org/) is a ruby static website
    generator, that uses Asciidoc an Markdown (+Haml) formats.

# Backends and reverse conversion
## Builtin backends
-   The [asciidoc](http://www.methods.co.nz/asciidoc/manpage.html)
    command produces DocBook XML 4.5 (with a _wordpress_ variant),
    HTML 4.01 Transitional, XHTML 1.1 markup styled with CSS2, HTML5,
    slidy, latex.
-   The [a2x](http://www.methods.co.nz/asciidoc/a2x.1.html)
    command add: chunked doc book, dvi, epub, htmlhelp, manpage, pdf,
    ps, tex, text, xhtml.
-   [epub backend - Publishing eBooks with AsciiDoc
    ](http://www.methods.co.nz/asciidoc/publishing-ebooks-with-asciidoc.html)

## Other backends
-   [asciidoc bootstrap docs backend
    ](https://github.com/mojavelinux/asciidoc-bootstrap-docs-backend)
    An AsciiDoc backend by Dan Allen that renders the AsciiDoc
    source as HTML5 in the style of the Twitter Bootstrap docs.
-   [asciidoc-odf](https://github.com/dagwieers/asciidoc-odf)
    enables to directly convert documents from AsciiDoc to
    Open Document Format.
-   [ebook-template](https://github.com/akosmasoftware/eBook-Template)
    is an asciidoc template used to generate eBooks in several formats:
    Self-contained HTML, ePub, PDF, Kindle
-   [eWEB](http://eweb.sourceforge.net/) (GPL)
    is a python+eWEB tool for literate programming in asciidoc.
-   [Flexndex](https://github.com/elextr/flexndex)
    _2012_
    is a flexible tool to generate multiple indices as document internal
    links. It is usable with most XML based document formats,
    eg xhtml, docbook or Open Document Format.
    Flexndex can be used with the xml generated by the Asciidoc tool
    in xhtml11, docbook and ODT backends.<br />
    [Flexndex Manual
    ](https://github.com/elextr/flexndex/blob/master/flexndex.asciidoc).
-   [git-scribe](https://github.com/schacon/git-scribe/)
    by Scott Chacon  is a  command line toolset to write e-books using Git, GitHub and Asciidoc.
-   [Graphviz filter for AsciiDoc
    ](http://asciidoc.org/asciidoc-graphviz-sample.html)
    allow to include graphs in _dot_ language via
    [Graphviz](/node/20#graphviz "internal reference")
-   [Publican](https://fedorahosted.org/publican/)
    is a DocBook XML publication system. Publican automates producing
    documentation in  plain text, HTML and PDF. A Publican package is
    in debian.
    [Asciidoctor can convert AsciiDoc to DocBook for use with Publican
    ](https://github.com/asciidoctor/asciidoctor/wiki/Convert-Asciidoc-to-Docbook-for-use-with-Publican).<br />
    [Publican user Guide
    ](https://jfearn.fedorapeople.org/en-US/Publican/4.1/html/Users_Guide/index.html).

## conversion to asciidoc
-   [Codiicsa](https://github.com/elextr/codiicsa/) (GPL)
    is an extendable  Python program for converting Docbook XML
    to the Asciidoc markup language. [Codiicsa Manual
    ](https://github.com/elextr/codiicsa/blob/master/codiicsa.asciidoc).
-   [docbook2asciidoc](https://github.com/oreillymedia/docbook2asciidoc)
    is a xslt stylesheet for transforming DocBook 4.5 to AsciiDoc.
    A saxon jar is also provided to power the XSLT 2.0 processor.

# Asciidoc  [html slideshows](/node/html#slideshow "internal reference")
-   Asciidoc includes a _slidy_ backend.
    Other slide backends are available through
    [plugins](http://www.methods.co.nz/asciidoc/plugins.html).
-   [slidy2 backend](http://code.google.com/p/asciidoc-slidy2-backend-plugin/)
    by Jean-Michel Inglebert; and [Additions for the slidy backend
    ](http://csrp.iut-blagnac.fr/jmiwebsite/home/index.html).
-   [asciidoc dzslides backend
    ](https://github.com/mojavelinux/asciidoc-dzslides-backend)
    by Dan Allen _(mojavelinux) has an extensive exemple in his slides
    [Asciidoc with pleasure
    ](http://mojavelinux.github.com/decks/asciidoc-with-pleasure/).
    The [slides source is in GitHub
    ](https://github.com/mojavelinux/decks/blob/master/asciidoc-with-pleasure/slides.asciidoc)
    in his [deck repository](https://github.com/mojavelinux/decks).
    In this repository you find also the sources of his presentation:
    [Discover the zen of writing (Ascii)Docs
    ](http://mojavelinux.github.io/decks/discover-zen-writing-asciidoc/cojugs201305/index.html).
-   [AsciiDoc-Deck.js](http://houqp.github.com/asciidoc-deckjs/) (GPL)
    by Qingping Hou is a Deck.js backend.



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
