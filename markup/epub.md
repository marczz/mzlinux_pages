---
title: Epub
---

See also the related {{< iref "html" "html section" >}}
and the {{< iref "html#css" "css section" >}}
since Epub uses css.
<!-- Other pages
[[file:../../../../content-org/weblinks/e-text.org::+hugo_front_matter_format: yaml][E-text in weblinks]],
[[file:../../../../content-org/notes/text_processing_notes/ebookreaders.org::+hugo_front_matter_format: yaml][Ebook Readers in Notes]]
-->

# Epub Format
The EPUB format Home is the {{< iref "#ipdf" "IPDF" >}}.

-   Wikipedia {{< wp "EPUB" >}}
-   [Epub Zone](http://epubzone.org/)
    all things EPUB.
-   [Kobo ePub Guidelines on Github
    ](https://github.com/kobolabs/epub-spec/)
-   [edutechwiki: epub](http://edutechwiki.unige.ch/en/EPub) has a lot
    of information on the epub format and applications to deal with
    it.

## IPDF - International Digital Publishing Forum {#ipdf}
[IPDF - International Digital Publishing Forum](http://idpf.org) Pages:
-   [EPUB Home](http://www.idpf.org/epub/)
-   EPUB2 is now considered as obsolete and was superseded by  EPUB
    3.0 in October, 2011, the last specifications are
    from year 2010: there are
    [Open Publication Structure (OPS) 2.0.1 v1.0
    ](http://www.idpf.org/epub/20/spec/OPS_2.0_latest.htm),
    [Open Packaging Format (OPF) 2.0.1 v1.0
    ](http://www.idpf.org/epub/20/spec/OPF_2.0.1_draft.htm),
    [Open Container Format (.doc)
    ](http://www.idpf.org/doc_library/epub/OCF_2.0.1_draft.doc)
-  The full list of the individual specifications comprising EPUB 3.0 is:
    -   [EPUB 3 Overview
        ](http://www.idpf.org/epub/30/spec/epub30-overview.html)
    -   [EPUB Publications 3.0
        ](http://www.idpf.org/epub/30/spec/epub30-publications.html)
    -   [EPUB Content Documents 3.0
        ](http://www.idpf.org/epub/30/spec/epub30-contentdocs.html)
    -   [EPUB Media Overlays 3.0
        ](http://www.idpf.org/epub/30/spec/epub30-mediaoverlays.html)
    -   [EPUB Open Container Format 3.0
        ](http://www.idpf.org/epub/30/spec/epub30-ocf.html)
    -   [EPUB Canonical Fragment Identifier Specification
        ](http://www.idpf.org/epub/linking/cfi/epub-cfi.html)
    -   [EPUB 3 Fixed Layout Documents](http://www.idpf.org/epub/fxl/)

-   [EPUB 3 Changes from EPUB 2.0.1
    ](http://www.idpf.org/epub/30/spec/epub30-changes.html)
-   [EPUB 3 Structural Semantics Vocabulary
    ](http://www.idpf.org/epub/vocab/structure/),
-   [EPUB Indexes 1.0](http://www.idpf.org/epub/idx/)
    [IPDF GitHub Repository](https://github.com/IDPF):
-   [EpubCheck](https://github.com/IDPF/epubcheck)
    is a tool to validate EPUB  2 and 3 files. It can detect many
    types of errors in EPUB. OCF container structure, OPF and OPS
    mark-up, and internal reference consistency are checked.
    -   [ipdf - EpubCheck as web service](http://validator.idpf.org/)
-   [Epub3 Samples](https://github.com/IDPF/epub3-samples)
-   [epub testsuite](https://github.com/IDPF/epub-testsuite)
    is a collection of EPUB documents to test EPUB  conformance
-   [epub-testsuite](https://github.com/IDPF/epub-testsuite)
    is a collection of EPUB documents to test EPUB  conformance.
-   [epub test Web
    ](https://github.com/IDPF/epubtestweb) is a Django powered site
    is used on-line in the
    [EPUB testsuite website](http://epubtest.org). You can find there
    the [Instructions for Accessibility Evaluation of Reading Systems
    ]http://epubtest.org/testsuite/).
-   [EDUPUB Samples](https://github.com/IDPF/edupub)
    project provides a collection of EPUB 3 publications
    intended to showcase features of the EDUPUB profile, and to
    provide testing materials for reading system developers.
    See the [EDUPUB Samples project page
    ](https://github.com/IDPF/edupub).

# Epub Formatters, Conversion, tools
-   <a name="calibre"></a>[Calibre](http://calibre-ebook.com/),
    the ebook platform, is a frontend that uses internal code and many
    tools to convert any ebook format to another one, including epub
    which is the reference format used by calibre. It allows also
    library Management, syncing to e-book reader devices, editing
    e-books, viewing ebook on the computer and in a built-in web
    server.
    -   [Calibre Manual](http://manual.calibre-ebook.com/).
    -   Calibre support importing and exporting to
        {{< iref "markdown" "Markdown" >}}
        using [python-markdown](https://python-markdown.github.io/), you can use
        [markdown extensions](https://python-markdown.github.io/extensions/).
-   [Booktype](https://github.com/sourcefabric/Booktype/) (AGPL)
    <a name="booktype"></a>
    is a Django, Web platform to produces books formatted in PDF
    (screen and printer), epub, mobi, xhtml.
-   [DotEPUB](https://dotepub.com)
    is a bookmarklet for javascript able browser or an extension for
    firefox or chrome to convert any webpage into an e-book.
-   [epubdiff](https://github.com/bencrowder/epubdiff)
    A Python script to diff EPUBs.
-   [EpubMaker](https://pypi.python.org/pypi/epubmaker/)
    is the python tool used for format conversion at Project
    Gutenberg. It builds EPUB2 and Kindle files from HTML and HTML4,
    EPUB2, Kindle, and PDF files from reST sources.
-   [glyphIgo](https://github.com/pettarin/glyphIgo)  MIT License
    is a tool by Alberto Pettarin aimed to deal with fonts
    in EPUB eBooks.
    It can:
    -   check whether a given font file contains all the glyphs
        needed to display an EPUB or plain text file,
    -   convert a font file from/to TTF/OTF/WOFF format,
    -   count the number of characters in an EPUB or a plain text
        UTF-8 file,
    -   list all Unicode characters used in an EPUB or a plain text
        UTF-8 file, or all Unicode glyphs present in a TTF/OTF/WOFF
        font file,
    -   lookup for information about a given Unicode character,
        including heuristic name matching,
    -   (de)obfuscate a font, with either the IDPF or the Adobe
        algorithm,
    -   subset a given font file, to the glyphs that are contained in
        a EPUB or plain text file.
-   [Grab My Books](http://www.grabmybooks.com/)
    is a Firefox or Chrome plugin that create an ePub file from a web
    sites. It can also feed its output to Calibre for conversion.
    It can be used for offline reading e.g. for Wikipedia.<br/>
    An android app is also available for 1€.
-   [Sigil](https://github.com/Sigil-Ebook/Sigil) (GPL)
    is an ebook editor. It supports EPUB2 and some features of EPUB3.
    -   [Sigil User Guide 0.7.2 (epub)
        ](https://github.com/Sigil-Ebook/Sigil/blob/master/docs/Sigil_User_Guide_0_7_2.epub).
    -   Sigil has [imported the FlightCrew code validator
        ](https://github.com/Sigil-Ebook/flightcrew) has plugin.
    -   [Sygil Plugin Index](http://www.mobileread.com/forums/showthread.php?t=247431).
    -   [Sygil Forum](https://www.mobileread.com/forums/forumdisplay.php?f=203).
-   [Standard Ebooks](https://standardebooks.org/)
    is a platform that takes ebooks from sources like Project Gutenberg,
    formats and typesets them using a style manual, proofreads and corrects them,
    and create a new edition aimed to ereader and browser technology.
    -   [Producing an Ebook, Step by Step
        ](https://standardebooks.org/contribute/producing-an-ebook-step-by-step)a
        is a Guide to  the creation of a complete Standard Ebook.It uses their Linux Toolset.
    -   [The Standard Ebooks Manual of Style](https://standardebooks.org/manual/)
    -   [standardebooks/tools](https://github.com/standardebooks/tools) (GPLv3 license)
        The Standard Ebooks python toolset for producing our ebook files.
    -   [Standard Ebooks Hints and Tricks](https://b-t-k.github.io/)
-   [Writer2ePub ](http://extensions.services.openoffice.org/en/project/Writer2ePub)
    is an OpenOffice.org extension that creates an ePub file from any
    document openable by the OOo Word Processor.

-   [Automated Ebook Builds With Pandoc and KindleGen | Puppet Labs
    ](https://puppetlabs.com/blog/automated-ebook-generation-convert-markdown-epub-mobi-pandoc-kindlegen)
    use Pandoc to convert Markdown into EPUB.

## Online services
-   [pdfpocket](http://www.pdfpocket.com/)
    online service to convert from PDF to epub
-   [Docverter](https://www.docverter.com/)
    Convert plain text documents written in HTML, Markdown, or LaTeX to
    PDF, Docx, RTF or ePub with a simple HTTP API.

# Epub libraries
-   [EbookLib]( is a Python library for managing EPUB2/EPUB3 and Kindle
    files. It's capable of reading and writing EPUB files
    programmatically.
    There is a Debian package.
    -   EbookLib is used in {{< iref "#booktype" "Booktype 2.0" >}}
    -   [EBookLib Documentation
        ](http://ebooklib.readthedocs.org/en/latest/)
-   [Exirel/Epub](https://bitbucket.org/exirel/epub)
    is a python library for Epub2, it does not seem to include an
    Epub3 support. It is in PyPi.

# Epub Readers
-   [EPUBReader](http://www.epubread.com/en/) is a Firefox addon to
    read epub in the browser.
-   [FBReader](https://fbreader.org/)
    is a linux, and android program that
    read epub, part of epub3, mobi and fb2 (2.0).. It uses
    [libunibreak](http://vimgadgets.sourceforge.net/libunibreak//).
-   [Calibre E-book Viewer](https://manual.calibre-ebook.com/viewer.html)
-   [CoolReader](http://sourceforge.net/projects/crengine/) (GPL)
    is a android and linux ebook reader. It support the following
    formats: FB2, TXT, RTF, DOC, TCR, HTML, EPUB, CHM, PDB, MOBI. , it
    is ported to e-ink devices.  On linux this is a QT package, as the
    build on sourceforge is for an old version and is not updated
    since 2012 it depends on old libraries. The git repository
    describe the requirement and process to build a newer release.
    There is a PPA on ubuntu, but it don't seem to be updated, and
    does not install on Debian Jessie.
-   [crengine git repository
    ](http://sourceforge.net/p/crengine/crengine/ci/master/tree/)
-   [Lucidor](http://lucidor.org/lucidor/)
    is a xul Epub reader, it neads either Firefox or XULRunner.
    it can also convert web feeds and web pages into e-books.
    The lucidor site provide a Debian package.
    There is also a Firefox plugin named [LuciFox
    ](http://lucidor.org/lucifox/) (GPL).

# Structured text to EPUB {#structured_to_epub}
{{< iref "rest#sphinx" "Sphinx" >}} can output to epub.

{{< iref "markdown#pandoc" "pandoc" >}} can convert
Markdown, CommonMark, Textile, reStructuredText, HTML, (subset of)
LaTeX, MediaWiki, TWiki, Haddock , OPML, Org-mode, DocBook, txt2tags,
Word docx To EPUB (v2 or v3) .

And from epub to plain text, Markdown, reStructuredText, XHTML, HTML
5, LaTeX (including beamer slide shows), ConTeXt, RTF, OPML, DocBook,
OpenDocument, ODT, Word docx, GNU Texinfo, MediaWiki, DokuWiki,
Haddock, EPUB (v2 or v3), FictionBook2, Textile, groff man pages,
Emacs Org-Mode, AsciiDoc, InDesign ICML, and Slidy, Slideous,
DZSlides, reveal.js or S5 HTML slide shows. It can also produce PDF .

{{< iref "asciidoc" "asciidoc" >}} has an
[epub backend
](http://www.methods.co.nz/asciidoc/publishing-ebooks-with-asciidoc.html)

-   [BookMarkdown](https://github.com/sjl/bookmarkdown) by Steve losh
    is a python script to build a book with markdown sources.
    He used it for his book [Learn Vim the Hardway
    ](https://github.com/sjl/learnvimscriptthehardway).
    There is a [xiyoulaoyuanjia fork
    ](https://github.com/xiyoulaoyuanjia/bookmarkdown)
-   [md2ebook](https://github.com/brunobord/md2ebook/) (MIT License)
    is a markdown to ebook converter, using Calibre or Pandoc and
    Python Markdown.
-   [md2epub](https://github.com/bencrowder/md2epub)
    Python script that takes a list of Markdown files and generates an
    EPUB out of them. It depends on python-markdown2 and smartypants.py.

    _The repository is not updated since 2011._
    -   [Initial presentation of md2epub](https://bencrowder.net/blog/2010/md2epub/).

# EPUB 3 Audio-eBooks
-   [Alberto Pettarin Pointers on Reading+Listening
    ](http://www.albertopettarin.it/blog/2015/07/25/pointers-on-reading-plus-listening.html)
-   Alberto Pettarin
    [Blog on a Python script ](http://www.albertopettarin.it/blog/2015/09/28/i-have-a-python-script.html)
    takes an ebook in EPUB 2 format and its audiobook version (ZIP of
    MP3 files), and it combines them into a reflowable EPUB 3 with
    Media Overlays.
-   [aeneas](http://www.readbeyond.it/aeneas/)
    is a Python library and a set of tools to automagically
    synchronize audio and text.
-   [A Practical Introduction To The aeneas Package
    ](http://www.albertopettarin.it/blog/2015/05/21/a-practical-introduction-to-the-aeneas-package.html)
    ,[aeneas Updates: Summer Edition
    ](http://www.albertopettarin.it/blog/2015/08/26/aeneas-updates-summer-edition.html)
-   [aeneas Web App](http://aeneasweb.org/login)
    is the web version of aenas. Users can register and run jobs for
    free. More informations in
    [aeneasweb.org Is Online Now](http://www.albertopettarin.it/blog/2015/11/09/aeneasweb-org-is-online-now.html)
-   [Alberto Pettarin Blog: A-Cute Bit
    ](http://www.albertopettarin.it/blog/),
    and [GitHub repository](https://github.com/pettarin/)


## sites with audio-ebooks

- [[http://www.readbeyond.it/][ReadBeyond]]:

[[http://www.readbeyond.it/shortstories.html][ReadBeyond  Free EPUB Audio-eBooks]]
[[http://www.readbeyond.it/menestrello/][ReadBeyond Menestrello]] is
an android/Ios app for reading+listening Audio-eBooks.
the open source version is
[Minstrel (GitHub)](https://github.com/readbeyond/minstrel) (MIT
License)

-   [[http://www.ilnarratore.com/][il Narratore audiolibri_ italian audiobooks]]
