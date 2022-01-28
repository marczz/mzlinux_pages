---
title: PDF, djvu, OCR, Postscript
---

You may also be interested by the
{{< iref "images" "Image section" >}} and the
{{< iref "svg" "SVG Section" >}}.

The pieces of software that handle both SVG and postscript or PDF are
in the {{< iref "svg" "SVG section" >}} it
includes the PDF to SVG conversion programs as Autotrace, Potrace,
pstoedit.  All SVG editors have a PDF and postscript export feature.
See also the {{< iref "cups" "Cups Page" >}}.


# Postscript {#postscript}

-   {{< wp "PostScript" >}} is a {{< wp "page description language" >}},
    {{< wp "Encapsulated PostScript" >}} or eps is a self contained graphics
    file format based on postscript but that includes the
    {{< wp "Bounding Box" >}}.
-   <a name="ghostscript"></a>[Ghostscript (Home Page)](http://www.ghostscript.com/)
    (GPL)  _[Wikipedia page](http://en.wikipedia.org/wiki/Ghostscript)_
    is an interpreter and converter for Postscript. As viewer it is
    used thru the __GV__ frontend or  {{< iref "#mupdf" "mupdf" >}}.
    It is also used by the linux printing software to produce
    raster files for the printer software.

    Ghostscript provides the following utilities:

    -   [ps2pdf](http://www.ghostscript.com/doc/current/Ps2pdf.htm) :
        convert postscript to pdf. It is a wrapper around `gs` using the device
        `pdfwrite`.
    -   [ps2ps2](http://www.ghostscript.com/doc/current/Ps2ps2.htm):
        Converts Postscript Level 3 or PDF into Postscript Level 2

-   The _psutils_ package contains many perl scripts _see the README_,
    mainly to fix postscript comming from various sources and the
    following programs:

    -   psbook:          rearranges pages into signatures
    -   psselect:        selects pages and page ranges
    -   pstops:          performs general page rearrangement and selection
    -   psnup:           put multiple pages per physical sheet of paper
    -   psresize:        alter document paper size
    -   epsffit:         fits an EPSF file to a given bounding box

-   [Le GNU a2ps](http://www.infres.enst.fr/~demaille/a2ps/) from
    Akim Demaille. _a2ps_ like the
    [Gnu enscript](http://www.gnu.org/software/enscript/)
    (GPL) cannot convert UTF-8 encoded text to PostScript.
-   [paps](http://paps.sourceforge.net/) (GPL) is a  Pango to PostScript converter
    it works with a UTF-8 encoded file.
-   Some {{< iref "source_code#code_beautifiers" "source code beautifiers" >}}
    are able to generate beutified _latex_, it can be used for a two step
    géneration of pdf or ps.
-    <a name="scribus"></a>[Scribus](http://www.scribus.net/) (GPL)
    is a Page Layout program for GNU/Linux, similar to PageMaker, QuarkXPress or
    InDesign.
    - The old stable 1.3 from 2003 is outdated, be careful to get
      the new generation >= 1.4.
    - The [Official online documentation](http://wiki.scribus.net/canvas/Help:TOC)
      in the [Scribus Wiki](http://wiki.scribus.net/index.php) refer to
      the new Scribus >= 1.4

# DjVu {#djvu}
-   Wikipedia: {{< wp "DjVu" >}}
-   <a name="djvulibre"></a>[djvulibre](http://djvu.sourceforge.net/) is the open source
     implementation of djvu.
-   [djvu.org](http://djvu.org/) is the home page of {{< wp "DjVu" >}} format.
    [DjVu Tutorial](http://www.djvuzone.org/support/tutorial/index.html),
    [compression chapter
    ](www.djvuzone.org/support/tutorial/chapter-compress.html),
    [Any2DjVu Server](http://any2djvu.djvuzone.org/) allows free conversion to djvu.
-   [WikiSource Help DjVu
    ](https://en.wikisource.org/wiki/Help:DjVu_files)
    deal with images conversion to DjVu, and OCR with djvu;
    [Digitising texts and images for Wikisource
    ](https://en.wikisource.org/wiki/Help:Digitising_texts_and_images_for_Wikisource)
-   Wikipedia commons: [creating a DjVu file
    ](https://commons.wikimedia.org/wiki/Help:Creating_a_DjVu_file,
    [Help Scanning](https://commons.wikimedia.org/wiki/Help:Scanning)
-   WikiSource fr: [Créer un fichier DjVu
    ](https://fr.wikisource.org/wiki/Aide:Cr%C3%A9er_un_fichier_DjVu),
    [Créer un fichier DjVu/Linux
    ](https://fr.wikisource.org/wiki/Aide:Créer_un_fichier_DjVu/Linux),
    [Créer un fichier DjVu/Méthodes complètes
    ](https://fr.wikisource.org/wiki/Aide:Cr%C3%A9er_un_fichier_DjVu/M%C3%A9thodes_compl%C3%A8tes),
    [Créer un fichier DjVu à partir d’un pdf de Google Books
    ](https://fr.wikisource.org/wiki/Aide:Cr%C3%A9er_un_fichier_DjVu/%C3%80_partir_d%E2%80%99un_pdf_de_Google_Books).
-   [PDF, PS and DjVu - ArchWiki
    ](https://wiki.archlinux.org/index.php/PDF,_PS_and_DjVu#Create_a_PDF_from_images)
-   _Djview4_ is the standard reader for djvu, {{< iref "#evince" "Evince" >}},
    {{< iref "#atril" "Atril"  >}},  {{< iref "#okular" "Okular" >}}
    _but not epdfview_ can also display djvu.
    _Djview4_is lighter than these multipurpose viewers. I have experienced on the same
    big (10M) djvu book, {{< iref "#evince" "Evince" >}} taking 40M of resident memory
    against 20M for  _Djview4.
-   [minidjvu](http://minidjvu.sourceforge.net/): _GPL_
    is a bitonal (black & white) DjVu encoder/decoder.

# PDF {#pdf}
{{< wp "PDF" >}} or Portable Document Format is an open standard for document exchange
created by Adobe Systems.  It encapsulates a complete description of a fixed-layout flat
document, including the text, fonts, graphics, and other information needed to display
it.

{{< wp "PDF/A" >}}, an ISO-standardized version of the PDF specialized for use in the
archiving and long-term preservation of electronic documents. There are many versions
PDF/A-1 (2005) based on PDF 1.4, PDF/A-2 (2011) and PDF/A-3 (2012) based on PDF 1.7,
PDF-A4 (2020) based on PDF 2.0.

Openoffice and libreoffice can export to PDF/A-1a, in the File Menu when selecting
_export as PDF_ you are offered an option choice with the  PDF/A-1a format.

The other specialized  ISO  versions of PDF are
{{< wp "PDF/X" >}} used to facilitate graphics exchange. There are also many versions
from PDF/X-1 (2001) based on PDF 1.3 to PDF/X-1.5 (2008) based on PDF1.6, and PDF/X-6
(2020) based on PDF 2.0.
{{< wp "PDF/E" >}} specialized in the creation of documents used in geospatial,
construction and manufacturing workflows,
{{< wp "PDF/UA" >}} is focused on accessibility in PDF documents and applications,
{{< wp "PDF/VT" >}}  is optimized for variable and transactional printing.

The [PDF Association](https://www.pdfa.org/) has published introductions to these
formats in
[PDF/A in a Nutshell 2.0](https://www.pdfa.org/resource/pdfa-in-a-nutshell-2-0/),
[PDF/X in a Nutshell](https://www.pdfa.org/resource/pdfx-in-a-nutshell/),
[PDF/UA in a Nutshell](https://www.pdfa.org/resource/pdfua-in-a-nutshell/).

-   [PDF, PS and DjVu - ArchWiki
    ](https://wiki.archlinux.org/index.php/PDF,_PS_and_DjVu#Create_a_PDF_from_images)
-   {{< wp "OpenXPS" >}} is a page description format created by microsoft to
    compete with the widely used pdf format.  See the
    {{< wp "Comparison of OpenXPS and PDF" >}} in Wikipedia.
    {{< iref "#mupdf" "Mupdf" >}} and {{< iref "#okular" "Okular" >}} can read XPS files.
-   As Xps is often not available on non windows computers converting
    Xps to Pdf may be useful.  There are a lot of online services
    _google "xps pdf converter"_ you can also find a
    [tutorial to Convert XPS to PDF
    ](http://bootpolish.net/home_howto_convertxpstopdf)
    using _ghostpdl_ on linux.  Kde users can also use {{< iref "#okular" "Okular" >}}.
-   Michael Wiedmann has written a
    [Screen Presentation Tools
    ](http://me.in-berlin.de/~miwie/presentations/html/index.html)
    review that has a section on pdf representation _updated 2014_.
-   Font extraction is dealed with a detailled tutorial in the answer
    of the StackOverflow question
    [How can I extract embedded fonts from a PDF as valid font files?
    ](http://stackoverflow.com/questions/3488042/how-can-i-extract-embedded-fonts-from-a-pdf-as-valid-font-files)
    there is also a web service
    [ExtractPDF.com ](http://www.extractpdf.com/) but we have to know
    that in PDFs there are never font metric files (.pfm or .afm
    files) embedded, So the extracted font may be unusable. The
    embedded font can also be restricted as the subset used in the
    document.

# HTML to pdf and ps conversion {#html_to_pdf}
-   [htmldoc](http://www.msweet.org/projects.php?Z1) (GPL)
    converts HTML into indexed HTML, PostScript, or PDF files.
    The [htmldoc documentation
    ](http://www.msweet.org/documentation/project1/HTMLDOC.html),
    contains  the [List of special htmldoc comments
    ](http://www.msweet.org/documentation/project1/HTMLDOC.html#COMMENTS)
    that you can use to guide the translation process.
-   [html2ps](http://user.it.uu.se/~jan/html2ps.html) (GPL)
    is an HTML to PostScript converter written in Perl
-   [PDFKit](https://github.com/pdfkit/PDFKit) (MIT license)
    is a ruby program to create PDFs using plain old HTML+CSS.
    It uses {{< iref "#wkhtmltopdf" "wkhtmltopdf" >}}
    as  back-end.
-   [pdfkit-clj](https://github.com/pdfkit/pdfkit-clj)
    is  Clojure library for generating PDFs from HTML that uses
    {{< iref "#wkhtmltopdf" "wkhtmltopdf" >}}.
-   {{< wp "TCPDF" >}}
    is a PHP class for generating PDF documents with full support of UTF-8.
    -   [TCPDF Home](http://www.tcpdf.org/) (LGPL)
-   [xhtml2pdf](http://www.xhtml2pdf.com/) (Apache License) is a
    converter from HTML and CSS
    in pure Python using the ReportLab Toolkit, HTML5lib and
    {{< iref "#pypdf2" "pyPdf2" >}}.
    [GitHub xhtml2pdf repository](https://github.com/chrisglass/xhtml2pdf)
    _xhtml2pdf_ was named previously _Pisa_ and packaged in Debian as
    _python-pisa_.
-   [wkhtmltopdf](http://wkhtmltopdf.org/) (LGPLv3)
    <a name="wkhtmltopdf"></a>
    wkhtmltoimage are command line tools to render HTML into PDF
    and various image formats using the QT Webkit rendering engine.
    These run entirely "headless" and do not require a display.
    It is in Debian.
-   To convert multiple jpeg to __one__ multi page pdf

         gm convert *.jpeg myoutput.pdf

-   Some {{< iref "source_code#code_beautifiers" "source code beautifiers" >}}
    are able to generate beautified _latex_, it can be used for a two step
    géneration of pdf or ps.

# Pdf viewers

Some viewers have support for _SyncTex_ the Tex source and pdf
_live preview_ synchronization library. This include
{{< iref "#okular" "Okular" >}}, {{< iref "#evince" "Evince" >}},
{{< iref "#qpdfview" "Qpdfview" >}}, {{< iref "#zathura" "Zathura"  >}}.

-   Wikipedia {{< wp "List of PDF software" >}}
-   [ArchWiki: list of pdf and djvu software
    ](https://wiki.archlinux.org/index.php/List_of_applications/Documents#PDF_and_DjVu).
-   <a name="fbpdf">[fbpdf](http://repo.or.cz/w/fbpdf.git) (BSD license) is a
    framebuffer pdf/djvu file viewer.  It can use either
    {{< iref "#mupdf" "mupdf" >}} or
    {{< iref "#poppler" "poppler libraries" >}} for rendering
    pdf files and it uses djvulibre library for rendering djvu files.
-   <a name="pdf_js"></a>[PDF.js](https://github.com/mozilla/pdf.js)  (Apache License)
    is a javascript PDF Viewer for html5 browsers, it is embedded in Firefox to provide
    the new [Firefox built-in PDF viewer
    ](https://support.mozilla.org/en-US/kb/view-pdf-files-firefox-without-downloading-them)
    It can be [enabled/disabled in preferences
    ](https://support.mozilla.org/en-US/kb/disable-built-pdf-viewer-and-use-another-viewer).
    It is available also [in chrome web store
    ](https://chrome.google.com/webstore/detail/pdf-viewer/oemmndcbldboiebfnladdacbdfmadadm)
    and can replace *Chrome*  a built-in PDF viewer. It can also work with Opera, Edge,
    and Safari >=  9.
-   <a name="llpp"></a>[Llpp](http://repo.or.cz/w/llpp.git/)
    is  a graphical PDF pager using {{< iref "#mupdf" "mupdf library" >}}.
    lpp depends on *Ocaml*. It supports continuous page scrolling,
    bookmarking, and text search. It is not in Debian but in an
    unofficial repository [notesalexp.org](http://notesalexp.org/).
    -   [ArchWiki: Llpp](https://wiki.archlinux.org/index.php/Llpp)
-   <a name="mupdf"></a>[Mupdf](http://mupdf.com/) (GPL)
    is a C-based PDF parsing library. MuPDF has a small footprint and
    has support for all non-interactive PDF 1.7 features.
    The toolkit provides a simple API for accessing the internal structures of the
    PDF document.

    Mupdfviewer  seems to be the smallest and fastest reader available on Unix,
    see below the size size comparison and the speed test in Johnny Huang's
    [Poppler vs MuPDF](http://hzqtc.github.io/2012/04/poppler-vs-mupdf.html).
    _Mupdf_ sources and binary downloads are available in the
    [Mupdf Site](http://mupdf.com/). Debian provide two packages:
    [Mupdf](http://packages.debian.org/search?keywords=mupdf) and
    [Mupdf Tools](http://packages.debian.org/search?keywords=mupdf-tools).
    The standard _mupdf_ viewer is quick and small, it allows also reading PDF, XPS
    EPUB, XHTML and CBZ (Comic Book archive) and image formats
    such as PNG, JPEG, GIF, and TIFF.

    It does not include an outline browser as do most alternate browsers, even if the
    _mupdf_ library can read the outline, and it is rendered by the _mutool_ utility and
    other viewers using the same _mupdf_ toolkit.

    {{< iref "#llpp" "llpp" >}}  use the _mupdf_ library and
    {{< iref "#zathura" "zathura" >}} can use {{< iref "#poppler" "poppler" >}}, it is
    named in Debian _zathura-pdf-poppler_, itcan also use the _mupdf_ library, it is
    then named _zathura-pdf-mupdf_, which is not packaged in Debian but available in the
    [ppa zathura-mupdf](https://launchpad.net/~spvkgn/+archive/ubuntu/zathura-mupdf).

    These alternate viewer provide some extra features compared to the plain _mupdf_
    frontend.

    -   [PyMuPDF](https://github.com/pymupdf/PyMuPDF) (GPL)
        is a Python binding for _MuPDF_,

        For all supported document types (i.e. including images) you can decrypt the
        document,  access meta information, links and bookmarks,  render pages in raster
        formats (PNG and some others), or the vector format SVG, search for text,
        extract text and images, convert to other formats: PDF, (X)HTML, XML, JSON,
        text.

        PDF files can be created, joined or split up. Pages can be inserted, deleted,
        re-arranged, images and fonts can be extracted or inserted, PDFs can be
        reformatted to support double-sided printing, posterizing, applying logos or
        watermarks, it allows decryption and encryption.

        It can also used for PDF, as a module, from the command line.

        -   [PyMuPDF documentation](https://pymupdf.readthedocs.io/en/latest/).


-   To compare the pdf readers memory footprints I have tried some viewers with the
    same document, a 6M pdf doc. with embedded fonts. I found:
    -   acroread 53M/23M,  evince 45M/21M, apvlv 45M/13M, epdfview 36M/14M, zathura
        29M/16M,  ghostscript 26M/6,  xpdf 11M/4.3M, Mupdf 9M res/3.5 shr.
-   An other test in 2015 first with  a 6M pdf doc. with embedded
    fonts, no bookmark; then (insides parentheses) with
    _lualatex-doc.pdf_ a 14p luatex  generated pdf, 160K without image, but an index.
    -   evince 99.1M/35.6M (98M/41M), llpp 59M/12M (57M/47M the difference of shared
        memory is strange, but checked many times!), qpdfview 55.6M/41.5M (93.7M/42.3M),
        acroread 55.2M/39.9M (58M/40M), zathura 41M/26M (37.9M/25.6M), gv (gs) 28.4M/11M
        (30.5M/10.7M), xpdf 19.4M/11.5M (19.9M/10M), mupdf 9.1M/5.6M (11.1M/5.6M).
    -   All start very quickly, but _evince_ is a lot more slower, even a little slower
        than its young brother _epdfview_. _Acrobat reader_ is also a lot more slower.
    -   They all allow to follow pdf links but_mupdf_ and _gv_ don't have
        a pane showing the index,which is available in all other readers.
-   <a name="poppler"> {{< wp "Poppler_(software)"  "Poppler" >}} (GPL)
    is a software library for viewing PDF documents, stemming from a fork of Xpdf.
    There is a {{< iref "#popler-utils" "set of utilities developped with Poppler" >}}
    referenced below.

    *Poppler* is the base of many pdf viewers:

    -   [Atril](https://github.com/mate-desktop/atril) (GPL)
        is the PDF/ps/eps/djvu/XPS/ viewer of the Mat Desktop. It is a fork of
        {{< iref "#evince" "Evince" >}} and use the same libraries _poppler_ for PDF,
        _libspectre_ for ps/eps, {{< iref "#djvulibre" "DjVuLibre"  >}} for djvu,
        _libxgps_ for XPS.
    -   <a name="evince"></a>{{< wp "Evince" >}} (GPL) build with  GTK+ and *Gnome*.
        -   [Evince Gnome Home](https://wiki.gnome.org/Apps/Evince/).
        -   [Evince supported documents formats
            ](https://wiki.gnome.org/Apps/Evince/SupportedDocumentFormats)
            includes PDF using _Poppler_, PostScript using the
            [libspectre][]  backend, multi-Page TIFF, DVI, DjVu using
             {{< iref "#djvulibre" "DjVuLibre"  >}}, XPS using _libxgps_,
            OpenDocument Presentation (impress), Comics (CBR, CBZ,
            CB7).
        -   [Evince Manual](https://help.gnome.org/users/evince/stable/)
    -   <a name= "okular"></a>{{< wp "Okular" >}} (GPL) build with QT.
    -   <a name= "pdf-tools"></a>[pdf-tools](https://github.com/politza/pdf-tools) (GPL)
        is a pdfviewer and annotation tool for emacs that replace the builtin _Docview_.
        It runs in background a {{< iref "#poppler" "poppler" >}}
        program _epdfinfo_ which does all the hard work. See below for
         {{< iref "#pdf-tools_annotations" "annotations with pdf-tools" >}}.
    -   <a name="qpdfview"></a>
        [Qpdfview](https://launchpad.net/qpdfview) (GPL) is a tabbed
        PDF viewer relying on QT toolkit, It is in Debian.  The GTK
        version [Epdfview](http://trac.emma-soft.com/epdfview/) (GPL)
        is now unmaintained and no longer in Debian.  _Qpdfview_ has a
        partial support for annotation and forms. Plugins are
        available for postscript and djvu.
    -   <a name="zathura"></a> [Zathura](http://zathura.pwmt.org/projects/zathura) (GPL)
        is a pdf viewer with minimal memory footprints and focus on control thru
        keyboard interaction.  In addition of common viewer features Zathura can display
        and browse outlines and record bookmarks.  It is fully configurable, and optional
        plugins allow to display djvu, commic books, or to use
        {{< iref "#mupdf" "mupdf" >}} instead of {{< iref "#poppler" "poppler" >}}.
        It is in Debian.
    -   [apvlv](https://github.com/naihe2010/apvlv/tree/master) (GPL)
        is a {{< iref "#poppler" "poppler" >}}/GTK+ based pdf viewer, which can also
        display epub documents.  Like {{< iref "#zathura" "Zatura" >}} he is controled
        with vim like keybindings. It allows multiple tabs.  It present himself as
        *minimal* but it has huge memory footprints, that put it in the same category
        than evince.
    -   *Libreoffice*, *TeXworks* and *Inkscape* are also using
        {{< iref "#poppler" "poppler" >}} library.

-   <a name="xpdf"></a>{{< wp "Xpdf" >}} (GPL)
    is a light pdf viewer with minimal dependencies. {{< iref "#poppler" "Poppler" >}}
    was forked from _Xpdf_. _Xpdf_ is user configurable; you can even set unusal, but
    very usefull options like the paper color; and of course you can set all the key
    bindings.

    _xpdf_ is in Debian, the derived {{< iref "#popler-utils" "popler-utils" >}}
    utilities are in the package _popler-utils_  except
    {{< iref "#pdftosrc" "pdftosrc"  >}} which is in the package _texlive-binaries_.

# PDF Editing

The _pdfmark_ operator is a PostScript extension, using this operator,
many non layout-related features of a PDF file can be defined in the
original document or in the corresponding PostScript code. PdfMark is
introduced in the
[pdfmark primer](http://extras.springer.com/1998/978-3-642-72032-1/PDF/PRIMER.PDF)
available in the springer extra materials,
it is a chapter of the book _Web publishing with Acrobat/PDF_ by
Thomas Merz.

You can also refer to the tutorial
[Enhancing the Text in Text Fields using Pdfmarks
](http://www.math.uakron.edu/~dpstory/tutorial/pdfmarks/txtfield.pdf)
by D. P. Story, and his page
[Pdfmarks: Links and Forms
](http://math.uakron.edu/~dpstory/lnk_forms.html).
and to the full [Acrobat Pdfmark Reference (pdf)][pdfmark reference].

For a wider specification look in the
[Adobe Developer Connection / PDF Technology Center
](http://www.adobe.com/devnet/pdf.html), the last _ISO 32000-1:2008_  is not free
but you can get [Adobe PDF Reference, Sixth Edition, version 1.7][pdf 1.7 reference]
_November 2006 - 31M_.

-   <a name="cpdf"></a>[CPDF](https://community.coherentpdf.com/)
    ([Non-Commercial Use License
    ](https://github.com/coherentgraphics/cpdf-binaries/blob/master/LICENSE))
    _Coherent PDF Command Line Tools Community Release_
    allow you to manipulate existing PDF files in a variety of ways.
    merge, or split, encrypt and decrypt, scale, crop, rotate pages,
    read and set document info and metadata, losslessly compress PDF files.

    It can also copy, add or remove: bookmarks, stamp logos, text, dates, page numbers,
    attachments.
    - [CPDF Manual](https://www.coherentpdf.com/cpdfmanual/cpdfmanual.html)
      ([pdf](http://www.coherentpdf.com/cpdfmanual.pdf))
    -   [CPDF Examples](http://www.coherentpdf.com/usage-examples.html)
    -   [Binaries for Linux, OSX, Windows (Github)
        ](https://github.com/coherentgraphics/cpdf-binaries)
-   {{< iref "images#exactimage" "Exact Image" >}} in the Image section
    is a fast C++ image processing library. it contains some pdf
    processing tools:
    -   {{< man "hocr2pdf" >}} is an hOCR to PDF converter. It can use the
        {{< iref "#hocr" "hocr" >}} output of
        {{< iref "#tesseract" "Tesseract" >}}.
-   <a name="fpdf"></a>[FPDF](http://www.fpdf.org/)
    is a PHP class which allows to generate PDF files with pure PHP,
    that is to say without using the PDFlib library.
    It has a clone in python {{< iref "#pyfpdf" "pyfpdf" >}}
-   [gpdftext](https://github.com/codehelp/gpdftext) (GPL)
    by Neil Williams is a C/GTK+ program that
    loads a PDF file, extracts the text, reformats the paragraphs into
    single long lines and then puts the text into a standard GTK+
    editor where you can make other adjustments.<br/>
    On the ebook reader, the plain text file then has no unwanted line
    breaks and can be zoomed to whatever text size you prefer.</b>
    The manual is in docbook and provided in the package it can be
    opened with yelp. _gpdftext_ is in Debian.
-   {{< iref "#ghostscript" "Ghostscript" >}}
    The older way to edit pdf is to take advantage of the very good
    support of postscript by _Ghostscript_, and edit under postscript,
    then convert in pdf with
    [ps2pdf](http://www.ghostscript.com/doc/current/Ps2pdf.htm)
    There is a python frontend _last update 2012, unmaintained_
    [Moonshiner](http://moonshiner.sourceforge.net/).
-   [flpsed](http://flpsed.org/flpsed.html)
    (GPL) a PostScript annotator that lets you add arbitrary text
    lines to existing PostScript 1 documents. Added lines can later be
    reedited with flpsed. Using pdftops, which is part of xpdf one can
    convert PDF documents to PostScript and also add text to
    them. flpsed is useful for filling in forms, adding notes
    etc. Flpsed uses the old _fltk_ toolkit. _last stable release 2015_,
    presently minimally maintened.
-   {{< iref "images#gimp" "Gimp" >}} can be used to convert pdf
    before editing as explained in
    [How to Edit PDF Files in Linux Using GIMP
    ](http://www.wikihow.com/Edit-PDF-Files-in-Linux-Using-GIMP)
-   [gpdftext](https://github.com/codehelp/gpdftext) (GPL)
    by Neil Williams is a C/GTK+ program that loads a PDF file, extracts the text,
    reformats the paragraphs into single long lines and then puts the text into a
    standard GTK+ editor where you can make other adjustments.<br/> On the ebook reader,
    the plain text file then has no unwanted line breaks and can be zoomed to whatever
    text size you prefer.</b> The manual is in docbook and provided in the package it
    can be opened with yelp. _gpdftext_ is in Debian.
-   <a name="jbig2"></a>{{< wp "jbig2" >}} is a patent protected format from IBM and
    Mitsubishi. JBIG2 is designed for lossy or lossless encoding of
    'bilevel' (1-bit monochrome) images at moderately high resolution, and
    in particular scanned paper documents. In this domain it can be very
    efficient, offering compression ratios on the order of 100:1. JBIG2
    images can be included in PDF from version 1.4. It is very similar to
    the JB2 compression scheme used in the {{< wp "DjVu" >}} file format, but JB2
    is open source.
    -   [jbig2enc](https://github.com/agl/jbig2enc) (Apache License)
        is a _jbig2_ encoder. _Since April 2014, only maintenance fixes_
    -   [Radim Hatlapatka fork of jbig2enc
        ](https://github.com/rhatlapa/jbig2enc)
        _last commit Jul 2012_, the author has also
        [pdfjbim
        ](https://github.com/rhatlapa/pdfjbim) a java tool that
        re-compress by jbig2enc images in pdf with use of symbol
        coding. His work was in
        [google code (archived): pdfrecompressor
        ](https://code.google.com/archive/p/pdfrecompressor/)
        where you find the references of articles on this work.
        This site is also archived in [GitHub: pdfrecompressor
        ](https://github.com/rhatlapa/pdfrecompressor).
        -   [PDF Enhancements Tools for a Digital Library
            pdfJbIm and pdfsign (pdf)
            ](http://dml.cz/bitstream/handle/10338.dmlcz/702572/DML_003-2010-1_8.pdf)
            by Radim Hatlapatka and Petr Sojka.
        -   [PDF recompression using JBIG2
            ](http://www.fi.muni.cz/kd/events/cikhaj-2010-feb/slides/hatlapatka_recompression.pdf)
            by Radim Hatlapatka.
    -   [jbig2dec from ghostscript](http://www.ghostscript.com/jbig2dec.html)
        (man {{< man "jbig2dec" >}}),  can decode jbig2 to png or pbm.
    -   [PDFs: JPEG vs PNG vs JBIG2
        ](http://ssdigit.nothingisreal.com/2010/03/pdfs-jpeg-vs-png-vs-jbig.html)
        by Tristan Miller.
    -   {{< iref "images#imagemagick" "ImageMagick" >}} can read and write jbig2 images.
-   <a name="jpdftweak"></a>[jPDF Tweak](http://jpdftweak.sourceforge.net/) (AGPL)
    is a Java Swing application that can combine, split, rotate, reorder, watermark,
    encrypt, sign, add PDF bookmarks, add page transitions,  attach files to your PDF.
-   <a name="k2pdfopt"></a>[k2pdfopt](http://willus.org/k2pdfopt/) (open source)
    copying/cropping/re-sizing/OCR-ing manipulation tool using MuPDF library and
    optionally Ghostscript. It can generate native or bitmapped PDF output, with an
    optional OCR layer.  The default conversion convert all pages to bitmap, it allows
    text re-flow, so the output file size is larger than the original when the original
    was not itself bitmaps. The is also an option to use [native PDF output
    ](http://willus.org/k2pdfopt/help/native.shtml).
    -   [k2pdfopt FAQ](http://willus.org/k2pdfopt/help/faq.shtml).
    -   The [command line options](http://willus.org/k2pdfopt/help/options.shtml)
        are available by typing ? at the interactive menu or with the command-line
        option -?.
    -   [journal2ebook](https://github.com/adasilva/journal2ebook) is a python GUI for
        k2pdfopt. _last release 2014._
    -   [MobileRead forum - k2pdfopt thread
        ](https://www.mobileread.com/forums/showthread.php?t=144711)
-   [Libreoffice
    ](http://documentation.libreoffice.org/en/english-documentation/)
    can be used to edit pdf. Thanks to _libreoffice-pdfimport_ pdf
    files can be imported to libreoffice-draw, modified and
    re-exported to pdf. If the files are produced by libreoffice you
    can save them in a [PDF-Hybrid
    ](https://wiki.documentfoundation.org/Faq/Writer/PDF_Hybrid) format
    by checking _Embed OpenDocument file_ in the export menu.  It
    allows you to export libreoofice writer documents and re-edit it
    in writer. For other pdf documents you can only open them in draw.
-   {{< iref "#mupdf" "Mupdf" >}}
    provides 2 commmand line tools.

    *mutool* is multipurpose tool which replace the previous *pdfshow*
    to examine objects in a PDF file and *pdfclean* to decompress and
    pretty print streams and objects. It has with the following
    subcommands:

    -   *clean* including decompression,
        linearization;
    -   *extract* given objects;
    -   *info*
    -   *show* print the specified objects and streams to stdout,
        where the objct is given by number, but can also be the
        *xref* or the *trailer* dictionary. *show* can also list all
        the object numbers or print objects in a format suitable for
        grepping.

    *mudraw* render PDF/XPS/CBZ documents as image raster files (png or pnm).
    *mudraw* replace the older *pdfdraw*.

    These tools are in the [Debian package mupdf-tools
    ](http://packages.debian.org/search?keywords=mupdf-tools).

-   [pdf-parser](https://www.aldeid.com/wiki/Pdf-parser)
    is part of [Didier Stevens PDF Tools
    ](http://blog.didierstevens.com/programs/pdf-tools/).
    _pdf-parser.py_ is a tool which parse a PDF document to
    identify the fundamental elements used in the analyzed file.
    It can be used for detecting malicious pdf document which use some
    malicious javascript.

    The tool _pdfid.py_ will scan a file to look for certain PDF
    keywords, allowing you to identify PDF documents that contain (for
    example) JavaScript.

    -   [pdf-parser use and examples
        ](https://www.aldeid.com/wiki/Pdf-parser).
        [pdf-id  use and examples
        ](https://www.aldeid.com/wiki/Pdfid).
    -   [Didier Stevens videos to explain how to use his tools
        to detect malicious pdf
        ](http://didierstevenslabs.com/products.html).
        and also [here
        ](http://didierstevenslabs.com/free-stuff.html).
    -   In [PDF, Let Me Count the Ways…
        ](http://blog.didierstevens.com/2008/04/29/pdf-let-me-count-the-ways/)
        Didier Stevens explains how basic features of the PDF language
        can be used to generate polymorphic variants of (malicious)
        PDF documents. {{< wp "polymorphic variants" >}} are used by malicious
        programmers to produce polymorphic viruses that are not
        detected by their signature.
    -   [Malicious Documents – PDF Analysis in 5 steps
        ](http://countuponsecurity.com/2014/09/22/malicious-documents-pdf-analysis-in-5-steps/).
        is a tutorial using Didier Stevens tool suite.
    -   [Analysing a Malicious PDF Document
        ](http://www.thegreycorner.com/2010/01/analysing-malicious-pdf-document.html)
        a tutorial by  tephen Bradshaw.
    -   [Analyzing malicious documents cheatsheet (pdf)
        ](https://zeltser.com/media/docs/analyzing-malicious-document-files.pdf)

-   [PDFBeads](https://github.com/ifad/pdfbeads)
    is an utility written in Ruby which takes scanned
    page images and converts them into a single PDF file. _PFBeads_
    like DjVu separates scanned text (typically black, but indexed images with a small number of
    colors are also accepted) from halftone pictures.Each type of
    graphical data is encoded into its own layer with a specific
    compression method and resolution. It can encode B&W images using
    either CCITT Group 4 Fax or JBIG2.
    -   Tristan Miller has [experiences with pdfbeads
        ](http://ssdigit.nothingisreal.com/2012/09/experiences-with-pdfbeads.html),
        [further experiences
        ](http://ssdigit.nothingisreal.com/2012/09/further-experiences-with-pdfbeads.html).
-   [Apache PdfBox](https://pdfbox.apache.org/) (Apache Licence)
    is a Java tool for working with PDF documents, it include command line utilities.
    It can extract text, fill forms, split and merge, convert to raster image, sign,
    create pdf.
    -   [pdfindexer](https://github.com/WolfgangFahl/pdfindexer) (Apache License)
        Index and search for keywords in PDF sources (files and URLs) using Apache
        Lucene and PDFBox, it ouputs an HTML result.
-   {{< wp "pdfedit" >}} (GPL) [pdfedit sourceforge project
    ](http://sourceforge.net/projects/pdfedit)
    is a low level tool that provides access to the internal structure
    of the PDF file. There si a [user documentation
    ](http://pdfedit.petricek.net/en/user_doc.html) and a
    [Pdfedit Wiki](http://pdfedit.petricek.net/wiki/HomePage). Pdfedit
    is no more developed since _2012_, it was previously in Debian,
    but has been removed.
-   [pdfjam](http://www2.warwick.ac.uk/fac/sci/statistics/staff/academic/firth/software/pdfjam)
    is a collection of shell scripts using {{< iref "#pdfpages" "pdfpages" >}}
    to rearrange and combine pages of a PDF document.
    A  drawback of pdfjam  is that any hyperlinks in the source PDF are lost.

    The functionalities of pdfjam are similar to those of
    {{< iref "#pdfsak""pdfSAK" >}} which also uses LaTeX.

    The provided script are:

    -   _pdfjam_ is the main script. This is the core of the
        package. Other scripts are simple wrappers for calls to pdfjam.
    -   _pdfnup_, which allows one or more PDF files to be "n-upped" in
        roughly the way that psnup does for PostScript files.
    -   _pdfjoin_, which combines the pages of multiple PDF files together
        into a single file.
    -   _pdf90_, _pdf180_ and _pdf270_ which rotate the pages of one or more
        PDF files.
    -   _pdfflip_ which reflects the pages of one or more PDF files.
    -   _pdfbook_ which arranges pages into 2-up "signatures" (like psbook
        does for PostScript files), suitable for binding into a book.
    -   _pdfjam-pocketmod_ which converts 8 pages from a single PDF file
        into a pocket-sized booklet.
    -   _pdfjam-slides6up_ and _pdfjam-slides3up_ which process PDF
        presentation slides to six-per-page or three-per-page for
        handout purposes.

-   [PDFlib](http://www.pdflib.com/) (proprietary software)
    is a C/C++ pdf library, PDFlib+PDI allow to incorporate some pages
    into the PDFlib output. The PDFlib Text and Image Extraction
    Toolkit (TET) extract text, images and metatdata from PDF
    documents.<br/> The PDFlib is quite expensive: PDFLib+PPS server $
    3550, TET $ 1175. But they can be evaluated freely, PDFlib+PDI,
    and PPS display a demo stamp across all generated pages, TET will
    only process PDF documents with up to 10 pages and 1 MB size.
-   [pdfmasher](https://www.hardcoded.net/pdfmasher/) (GPL)
    is a python tool to convert PDFs to HTML, MOBI and EPUB. It is no more maintained
    since 2015.
    -   [GitHub - pdfmasher](https://github.com/hsoft/pdfmasher)
-   <a name="pdfminer"></a>[PDFMiner](http://www.unixuser.org/~euske/python/pdfminer/)
    (MIT License)
    is a python tool for extracting information such as exact location
    of text and fonts from PDF documents. It includes  a command line
    `pdf2txt.py` that extracts text from pdf and a PDF to HTML
    converter. `python-pdfminer` is in Debian.
    -   Tim Arnold [Manipulating PDFs with Python
        ](https://www.binpress.com/tutorial/manipulating-pdfs-with-python/167)
        includes a tutorial to use `pdf2txt.py`, `dumppdf.py`, and a
        pythonic use of _pdfminer_ library.
    -   [GitHub - pdfminer](https://github.com/euske/pdfminer)
    -   [pdfminer.six](https://github.com/pdfminer/pdfminer.six)
        is a port of pdfminer to Python 3 using six.
    -   [slate](https://github.com/timClicks/slate)
        is a Python package that simplifies the process of extracting
        text using PDFMiner.
-   [PDFMod](https://wiki.gnome.org/action/show/Apps/PdfMod) (GPL)
    is a gnome mono program that can rotate, extract, remove and
    reorder pages and combine documents via drag and drop.  You may
    also edit the title, subject, author and keywords of a PDF
    document. Pdfmod is in Debian.
-   <a name="pdfpage"></a>[pdfpages
    ](http://www.ctan.org/tex-archive/macros/latex/contrib/pdfpages/pdfpages.pdf)
    is a latex package for _pdflatex_, that allows inserting pages of
    external PDF documents without worrying about the print space.
    Several logical pages can be arranged onto each sheet of paper and
    the layout can be changed individually. Hyperlinks are supported,
    like links to the inserted pages, links to the original PDF
    document, threads, etc.

    -   <a name="pdflatex_bookmarks"></a>[PDF Bookmarks with PdfLaTeX
        ](http://michaelgoerz.net/notes/pdf-bookmarks-with-latex.html)
        is a tutorial by Michael Goerz to use a combination of
        _pdfpages_, _hyperref_, and _bookmark_ to add an outline to an
        existing pdf file.

-   <a name="pdfsak"></a>[pdfSAK](https://pdfsak.readthedocs.io/) (MIT License)
    previously named _pdftools_ is an utility using LaTeX.
    It allows to Merge PDF files, N-up pages, trim pages, extract pages,
    rotate pages, swap pages, delete pages, create handouts, add text (like page
    numbers), Remove owner protection which forbid to print/annotate document from PDF
    files, remove metadata from PDF file, simulate Adobe Acrobat clearscan.

    It requires a distribution of LaTeX like  TexLive or MikTex with the packages:
    pdfpages, lastpage, grffile, forloop, fancyhdr textpos, changepage.

    The functionalities of pdfsak are similar to those of
    {{< iref "#pdfjam""pdfjm" >}} which also uses LaTeX.

-   [PdfParser](https://github.com/smalot/pdfparser)
    is a standalone PHP library that provides various tools to extract
    data from a PDF file.
    -   [PdfParser documentation](http://www.pdfparser.org/documentation)
-   [pdfsam _pdf split and merge_](http://www.pdfsam.org/pdfsam-basic/)
    (GPL) an open source java utility with a GUI to splt, merge, and
    rotate pdf files. It is in Debian, there is also a private source
    commercial version. Like _pdftk_ it uses as backend {{< wp "iText" >}}.
-   [pdfsizeopt](https://github.com/pts/pdfsizeopt) is a python tool
    to optimize size of pdf files, aimed to pdf produced from TeX.
    [The installation instructions
    ](https://code.google.com/p/pdfsizeopt/wiki/InstallationInstructionLinux)
    are on the [old google code project
    ](https://code.google.com/p/pdfsizeopt/). The EuroTeX 2009 article
    [Optimizing PDF output size of TEX documents
    ](http://pdfsizeopt.googlecode.com/files/pts_pdfsizeopt2009.psom.pdf)
    by Péter Szabó the author of _pdfsizeopt_, explain what can be
    optimized, and how to use _pdfsizeopt_.
-   <a name="pdftk"></a>[pdftk - The PDF Toolkit
    ](https://www.pdflabs.com/tools/pdftk-server/) (GPL)
    is a java *compiled (with gcj)* application which uses the
    [iText library](http://en.wikipedia.org/wiki/IText)
    (LGPL). It can merge, split, rotate, encryt, decrypt, attach
    files, unpack, repair pdf documents. It allows also to fill
    PDF Forms with FDF data or XFDF data and flatten Forms.
    -   [pdfchain](http://pdfchain.sourceforge.net/)
        is a graphical user interface for the PDF Toolkit (PDFtk)
        written in GTKmm, a C++ library for GTK+.
        It can merge, split, rotate, shuffle, add backgrounds
        or stamps and add attachments.
    -   [PDFTK example](https://www.pdflabs.com/docs/pdftk-cli-examples/),
        [How to Collate Even and Odd Scanned PDF Pages
        ](https://www.pdflabs.com/blog/how-to-collate-even-odd-scanned-pages/)
        and [How to Export and Import PDF Bookmarks
        ](https://www.pdflabs.com/blog/export-and-import-pdf-bookmarks/)
        from _pdflabs_.
    -   [PDFTK tutorial (fr) - Ubuntu-fr](https://doc.ubuntu-fr.org/pdftk).
    -   There are also examples in the  [PDF, PS and DjVu - ArchWiki page
        ](https://wiki.archlinux.org/index.php/PDF,_PS_and_DjVu#Create_a_PDF_from_images).
-   <a name="pdfwritebookmarks"></a>[pdfWriteBookmarks
    ](http://github.com/goerz/pdfWriteBookmarks) (GPL)
    is a Java program by [Michael Goerz](https://github.com/goerz) and
    [Stefan Birkner](https://www.stefan-birkner.de/se/) using the
    [PDFBox](http://www.pdfbox.org/) library that reads bookmarks from a text file in a
    simple format and adds them to an exisiting PDF.
-   [PoDoFo library](http://podofo.sourceforge.net/about.html)
    (LGPL) is a portable C++ library to parse PDF files and modify
    their contents into memory.

    It includes the following tools:

    -   podofoencrypt - Encrypts any PDF and allows to set PDF
        permissions.
    -   podofoimgextract - Extracts all images from a given PDF file.
    -   podofoimpose - A powerful PDF imposition tool. It places
        pages from one or more source PDFs onto pages of a new PDF,
        applying scaling and positioning.
    -   podofomerge - Merges two PDF files into one.
    -   podofopdfinfo - Provides some basic info about a PDF -
        metadata, page details, etc.
    -   podofotxt2pdf - Converts a text file to a PDF
    -   podofotxtextract - A tool that extracts all text from a PDF
        file. Works only for simple PDFs at the moment.
    -   podofouncompress - Removes all compression filters from a PDF
        file. This is useful for debugging existing PDF files.
        You can use also PoDoFoBrowser.

    _PoDoFoBrowser_ is a Qt application distributed separatly for
    browsing the objects in a PDF file and modifying their keys
    easily.

-   <a name="popler-utils>_poppler-utils_</a> from the
    {{< iref "#poppler" "Poppler library" >}}
    contain the following command line utilities:

    -   pdfdetach -- lists or extracts embedded files (attachments)
    -   pdffonts -- font analyzer
    -   pdfimages -- image extractor
    -   pdfinfo -- document information
    -   pdfseparate -- page extraction tool
    -   pdftocairo -- PDF to PNG/JPEG/PDF/PS/EPS/SVG converter
        using Cairo
    -   pdftohtml -- generate an html page with png images of each pdf page.
    -   pdftoppm --  convert PDF to  images in PPM, PGM or PBM.
    -   pdftotext -- convert pdf to txt
    -   pdfunite --  merges several PDF

-   <a name="pypdf"></a>[pyPDF2](https://github.com/mstamy2/PyPDF2/) (BSD License)
    is the continuation of the  python librariy [pyPDF](http://pybrary.net/pyPdf/)
    by Mathieu Fenniak,  whose development stopped in 2010.
    Thew fork [pyPDF2](https://github.com/mstamy2/PyPDF2/)
    allows working on a PDF document: extracting info, splitting, merging, cropping,
    encrypting and decrypting PDF files. _PyPDF_ and  _pyPDF2_ have
    similar functionalities than {{< iref "#pdfk" "pdftk" >}}
    but are pure python with no module dependency.

    _pyPDF_ is distinct from the nearly homophone {{< iref "#pyfpdf" "pyfpdf" >}}.

    -   The [pyPDF Documentation](http://pybrary.net/pyPdf/pythondoc-pyPdf.pdf.html)
        is also usable for _pyPDF2_.
    -   [Pypi: pypdf2](https://pypi.python.org/pypi/PyPDF2).
    -    _PyPDF_ is packaged in Debian as _python3-pypdf2_.
    -   Tim Arnold [Manipulating PDFs with Python
        ](https://www.binpress.com/tutorial/manipulating-pdfs-with-python/167)
        includes a tutorial to use pypdf2 in python to merge a layer on pages of a pdf
        file, to merge the pages of two files, to append a set of pages building a new
        pdf, to delete some page, to split a pdf file, to modify metadata.

    The following scripts are wrapper around pypdf/pypdf2:

    -   [pdfsplit](http://pypi.python.org/pypi/pdfsplit) (GPL) _2008_
    -    <a name="pdfshuffler"></a>[pdfshuffler](http://pdfshuffler.sf.net)(GPL)
        allows one to merge, split, rotate, crop and rearrange their
        pages using a graphical interface. It is in debian.
    -   [pdfposter](http://pythonhosted.org/pdftools.pdfposter/)
        scale and tile PDF images/pages to print on multiple pages.
        in Debian.

-   [qpdf](http://qpdf.sourceforge.net/) (Artistic License)
    is a command-line C++ program that does structural,
    content-preserving transformations on PDF files. It can do
    transformations such as linearization , encryption, and decryption
    of PDF files.  It also has options for inspecting or checking PDF
    files. When converted in QPDF mode, pdf files can be edited with a
    text editor. It is packaged in Debian.<br />
    -   [qpdf Manual](http://qpdf.sourceforge.net/files/qpdf-manual.html),
    -   [qpdf GitHub repository](https://github.com/qpdf/qpdf).

-   [ReportLab Toolkit](http://www.reportlab.org/rl_toolkit.html)
    (BSD License) is a PDF library interfaced in Python. The Debian
    packages are _python-reportlab_ and _python-reportlab-accel_.
    [PythonPoint](http://www.reportlab.org/python_point.html)
    which is part of ReportLab Toolkit transform a simple xml language
    for describing presentation slides, in pdf slides.
-   Other graphic editors have pdf editing facilities, often after
    conversion as {{< iref "#item_scribus" "Scribus" >}}, or
    {{< iref "images#inkscape" "Inkscape" >}}.
-   [Search Pypi for pdf](http://pypi.python.org/pypi?%3Aaction=search&term=pdf&submit=search)

## PDF cropping tools {#pdf_crop}
To crop margins on a pdf document you can use some all purposes tools as
{{< iref "#pdfshuffler" "pdfshuffler" >}}  a graphical tool that
uses {{< iref "#pypdf2" "pypdf2" >}} and
{{< iref "#k2pdfopt" "k2pdfopt" >}}.

Other crop specific tools are either standalone or works as user interfaces to
{{< iref "#pdftk" "pdftk" >}}, or {{< iref "#pypdf2" "pypdf2" >}}:
{{< iref "#briss" "BRISS" >}} a java GUI,
{{< iref "#pdfcrop-python" "pdfcrop python script" >}} that
uses {{< iref "#pypdf2" "pypdf2" >}},
{{< iref "#pdfcrop-perl" "pdfcrop perl script" >}} that uses pdflatex,
{{< iref "#pdfcrop-pdftk" "pdfcrop2.sh" >}} using
{{< iref "#pdftk" "pdftk" >}}, {{< iref "#pdfcropper" "pdfcropper" >}}
python script,
{{< iref "#pdfquench" "pdf-quench" >}} a GUI that uses
{{< iref "#pypdf2" "pypdf2" >}}.

-   <a name="briss"></a>[BRISS](http://briss.sourceforge.net/) (GPL)
    is a a java cross-platform application with a GUI to crop pdf pages.
    -   |mobileread forum - BRISS thread
        ](https://www.mobileread.com/forums/showthread.php?t=83053)
-   <a name="pdfcrop-python"></a>[pdfcrop (python)](https://github.com/pboehm/pdfcrop)
    is a python script that uses _pypdf_  to crop pdf pages. _last update 2011._
-   <a name="pdfcrop-perl"></a>[pdfcrop (perl) - GitHub](https://github.com/ho-tex/pdfcrop)
    (LaTeX Project Public License) is a perl script from _texlive_ utilities that uses
    _ghostscript_ and _pdftex_ to crop pdf pages.  PDFCrop should preserve the input
    file's fonts, bookmarks and hyperlinks when generating the output file, but it may
    increase the file size during the pdf to postscript decoding/reencoding process.

    [pdfcrop source forge project](http://pdfcrop.sourceforge.net/) contains the old
    version 0.4b 2011.
-   <a name="pdfcrop-pdftk"></a>The script
    [pdfcrop2.sh](https://www.entorb.net/wickie/Modifying_PDFs#pdfcrop2.sh)
    from the
    [Torben Wiki](http://www.entorb.net/wickie/) page
    [Modifying PDFs](http://www.entorb.net/wickie/Modifying_PDFs)
    uses {{< iref "#pdftk" "pdftk" >}} to crop pdf.
    It should keep hyperlinks and not increase the size.
-   <a name="pdfcropper"></a>[pdfcropper](https://github.com/edeposit/pdfcropper) (GPL)
    is a python script to crop pages. _last update 2014._
-   <a name="pdfquench"></a>[pdf-quench](https://code.google.com/p/pdf-quench/)
    is a visual python/gtk tool for cropping pdf files. It uses
    {{< iref "#pypdf2" "PyPdf2" >}}, goocanvas, and
    {{< iref "#poppler" "python-poppler" >}}.
    It is reported that _pdfquench_ don't preserve hyperlinks.
    -    [GitHub - pdf-quench](https://github.com/linuxerwang/pdf-quench).

## PDF Outline
The PDF outline, sometime also called _Bookmarks_ is a a visual table of contents which
display the document’s structure. The Outline is defined in
[pdf 1.7 reference - section 8.2][].

You find also a description and several examples in
[pdfmark reference - bookmark(out)][].

We distinguish these Outlines with the operation of
{{< iref "#bookmarking" "bookmarking" >}} that many viewers offer, which is the object
of  {{< iref "#bookmarking" "next section" >}}.

Many software allow to modify outline, among them:
{{< iref "#pdflatex_bookmarks" "PdfLatex" >}},
{{< iref "#jpdfbookmark" "JpdfBookmark" >}},
{{< iref "#jpdftweak" "jPDFtweak" >}},
{{< iref "#pdfk" "pdftk" >}},
{{< iref "#pdfwritebookmarks" "pdfWriteBookmarks" >}},
{{< iref "#cpdf" "CPDF" >}}.

-   [bmconverter.py](https://github.com/goerz/bmconverter.py) (GPL)
    by [Michael Goerz](http://michaelgoerz.net/) _2011_
    is a python script that converts between the bookmark description
    formats used by different pdf and djvu bookmarking tools such as
    pdftk, the iText toolbox, pdfLaTeX pdfWriteBookmarks, jpdftweak,
    djvused, and the DJVU Bookmark Tool _2010_.
    -   [BmConverter Manual](http://goerz.github.io/bmconverter.py/)
    -   [User script to convert pdftk bookmarks to pdfmarks
        ](https://github.com/goerz/bmconverter.py/issues/1)
-   {{< iref "#ghostscript" "Ghostscript" >}}
    can a be used to manage bookmarks as outlined in
    [PDF bookmarks with Ghostscript
    ](http://blog.tremily.us/posts/PDF_bookmarks_with_Ghostscript/)
    where you can also find the script `pdf-merge.py` that uses `pdftk`
    and `ghostscript` to provide a bookmark-preserving version of
    pdftk's `cat`. You can take advantage from an user script
    [to convert pdftk bookmarks to pdfmarks
    ](https://github.com/goerz/bmconverter.py/issues/1)
    to use the output of {{< iref "#pdftk" "pdftk" >}}.
-   <a name="jpdfbookmark"></a>[JpdfBookmark (author page)
    ](http://flavianopetrocchi.blogspot.com/) (GPL)
    and [JpdfBookmark sourceforge project](http://sourceforge.net/projects/jpdfbookmarks/)
    is a java application that allows you to create and edit bookmarks on existing PDF files.

## PDF Bookmarking {#bookmarking}
Some viewers have support for bookmarking, we need to distinguish the
_oulines_ that are included in the document by _pdfmarks_ syntax. And
some viewer bookmarks that are proper to the editor and leave the core pdf
untouched, and store the annotations as metadata in the file.
A third bookmark type is bookmarking in an external file such method is referred in the
section {{< iref "org-mode#annotations" "Document annotation" >}}.

The bookmarks are not compatible from an application to an other one. Some application
allow to export them.

With {{< iref "#evince" "Evince" >}} you can list the bookmarks with the command:

    $ gio info -a "metadata::evince::bookmarks"  <path-of -pdf-file>

Many software have bookmarking support {{< iref "#llpp" "llpp" >}},
{{iref "#zathura" "Zathura" >}},  {{< iref "#evince" "Evince" >}},
{{< iref "#qpdfview" "Qpdfview" >}}, {{< iref "#atril" "Atril"  >}},
{{< iref "#okular" "Okular" >}} ...



## PDF Annotations {#pdf_annotations}
PDF annotations are in
[Annotation section of pdfmark reference][pdfmark reference - annotations]

There are seventeen type of annotations in PDF 1.3 and cutom annotations can be added.
The most used annotations are annotations that add an ornamentation to the pdf as the
type _square_, _circle_, _highlight_, ink_, _strikeout_, _underline_, _stamp_;
and the _Text annotations_ also known as _notes_.

All annotations appear in the pdf source as:
```
Rect [xll yll xur yur]
/Subtypename
...Optional key–value pairs...
/ANN pdfmark
```

for examples of pdf codes for annotations look at the
[pdfmark reference - annotation][pdfmark reference - annotations].

Annotations are also described in the
[8th chapter of the pdf 1.7 reference][pdf 1.7 reference - chapter 8].

Some type of annotations,like _circle_, _square_, _polygone_, _caret_, _watermark_ or
_free text_ are only visual and don't popup a text.

The most used _text annotation_ is used to associate a popup note at some document
location which appears as an icon when closed. Others types like _lines_, _rubber
stamp_, _ink_, or the text markup annotations _highlights_, _underlines_, _strikeouts_,
or _squiggly_ (jagged underlines) may have an associated note.

Other anotation can link to some other part of the document _link_, or reference an
embedded content _FileAttachment_. There is also annotations to play some media _sound_,
_movie_, _screen_.

Annotation are supported by several {{< iref "#poppler" "Poppler" >}} based software
{{< iref "#evince" "Evince" >}}, {{< iref "#qpdfview" "Qpdfview" >}} and
{{< iref "#okular" "Okular" >}}.

{{< iref "#evince" "Evince" >}} allows markup annotations of type _highlight_,
_underline_, _strikeouts_ and _squiggly_, you can choose the color and add a note.
The same hold for _text annotation_, you can also choose the icon. Unsupported
annotations type let by a software with a larger annotation support like
{{< iref "#okular" "Okular" >}} have their visual effect displayed, but cannot be
changed, you cannot display the associated note and they are not listed in the list of
annotations. It is a point where _Evince_ des not perform as well as other software in
this section.

{{< iref "#okular" "Okular" >}} allows many types of annotations _highlight_,
_underline_, _strikeouts_ and _squiggly_, _text annotation_, _ellipse_, _polygon_,
_freehand_, _highlight_, _typewriter_ and an experimental _rubber stamp_ only visible in
_Okular_.  As in  As I don't run KDE, I used Okular 1.10.1 from _flatpak_; with this
version the display of _inline_ and _typewriter_ is defective.

{{< iref "#qpdfview" "QpdfView" >}} allows only _text annotation_, and  _highlight_
but it can display allannotations set with an other tool and chage the associated note.
I has no support for displaying a list of bookmark. Other unsupported
{{< iref "#okular" "Okular" >}}
annotations can be seen, and the associated popup note displayed and changed.

<a name="pdf-tools_annotation"></a>The {{< iref "#pdf-tools" "pdf-tools" >}} package
contains a pdf annotation tool. It allows to have popup _text annotations_ at a point
that appear as a small icon, to _highlight_ or _underline_ a region and attach a textual
annotation to it.  It runs in background a {{< iref "ps_pdf_djvu#poppler" "poppler" >}}
program _epdfinfo_ which does all the hard work.


As _pdf-tools_ uses {{< iref "ps_pdf_djvu#poppler" "poppler" >}}, the annotations
are saved by _poppler_ according to the PDF specification. They can can be also
viewed or modified by other viewers following the pdf annotation specification,
like the other {{< iref "ps_pdf_djvu#poppler" "poppler" >}} based viewer and _adobe
reader_.

When an annotation type is not supported, like some annotations set with
{{< iref "#okular" "Okular" >}} they appear as visual effect and show also the note. The
note and the colour can be modified from _pdf-tool_ even if, _of course_, the shape
cannot be changed, but they don't appear in the list of annotation.

The main drawback of pdf-tools is the lack of documentation.

-   [Xournal++](https://xournalpp.github.io/) (GPL-2.0)
    is a handwriting notetaking software with PDF annotation support.
    It is written in C++ with GTK3.

    The [releases Page](https://github.com/xournalpp/xournalpp/releases/tag/nightly)
    contains a Debian package.

    -   [Xournal++ - GitHub](https://github.com/xournalpp/xournalpp)

# OCR {#ocr}

-   Wikipedia {{< wp "Comparison of optical character recognition software" >}}
-   Andreas Gohr SplitBrain: [Linux OCR Software Comparison
    ](http://www.splitbrain.org/blog/2010-06/15-linux_ocr_software_comparison)
    compare abbyyocr, cuneiform, gocr, ocrad, tesseract in 2010.
-   [Review of Linux OCR software
    ](http://www.mscs.dal.ca/~selinger/ocr-test/)
    compare in 2007 OCRAD, Tesseract, GOCR.
    The winner is Tesseract, and GOCR has poor performances.
-   [WikiSource Help:Digitising texts and images for Wikisource
    ](https://en.wikisource.org/wiki/Help:Digitising_texts_and_images_for_Wikisource)
-   [Wikimedia Help: Scanning
    ](https://commons.wikimedia.org/wiki/Help:Scanning)

-   <a name="cuneiform"></a>{{< wp "CuneiForm" >}} (BSD)  (BSD License)
    is an OCR program in C++ first developed by Cognitive Technologies then
    released as freeware in 2007.
    It recognizes any print font but not handwritten or decorative fonts .
    CuneiForm can save text formatting, and also recognizes
    complicated tables.
    -   [Cuneiform is now hosted at launchpad](https://launchpad.net/cuneiform-linux/)
        and is in Debian non-free section.
-    <a name="gocr"></a>{{< wp "GOCR" >}} is an OCR
    program (GPL). It converts scanned images of text back to text
    files.Development go at at a slow pace since 2002.
    -   [GOCR Home](http://www-e.uni-magdeburg.de/jschulen/ocr/)
-   <a name="gscan2pdf"></a>
    [gscan2pdf](http://gscan2pdf.sourceforge.net/)
    can control scanners with SANE via libsane-perl, scanimage or
    scanadf, and can scan multiple pages at once. It presents a
    thumbnail view of scanned pages, and permits simple operations
    such as cropping, rotating and deleting pages.

    The resulting document may be saved as a PDF, DjVu, multipage TIFF
    file, or single page image file.

    {{< iref "#tesseract" "Tesseract OCR" >}}
    can be used to recognise text in the scans,
    and the output embedded in the PDF or DjVu.

-   [hocr-tools](https://github.com/tmbdev/hocr-tools)
    are python tools for manipulating and evaluating the hOCR format.

    <a name=hocr"></a>hOCR is a format for representing OCR output,
    including layout information, character confidences, bounding
    boxes, and style information. It embeds this information invisibly
    in standard HTML.

    The reference for hOCR is
    [The hOCR Embedded OCR Workflow and Output Format
    ](https://docs.google.com/document/d/1QQnIQtvdAC_8n92-LhwPcjtAUFwBlzE8EWnKAxlgVf0/preview#heading=h.77bd784474e5).

    {{< iref "#cuneiform" "Cuneiform" >}},
    {{< iref "#ocropus" "OCRopus" >}},
    {{< iref "#tesseract" "Tesseract" >}}
    can use the hOCR format.

    _hocr-tools_ is in Debian and includes the following command line
    programs:

    -   hocr-check -- check the hOCR file for errors
    -   hocr-combine -- combine pages in multiple hOCR files into a single document
    -   hocr-eval -- compute number of segmentation and OCR errors
    -   hocr-eval-geom -- compute over, under, and mis-segmentations
    -   hocr-eval-lines -- compute OCR errors of hOCR output relative to text ground truth
    -   hocr-split -- split an hOCR file into individual pages
    -   hocr-merge-dc -- merge Dublin Core meta data into the hOCR HTML header


-   KDE OCR software
    [Kooka](https://techbase.kde.org/Projects/Kooka) (GPL)<a name="kooka"></a>
    was the ocr frontend for Kde until 2007, it
    support gocr, ocrad and Kadmos (commercial). Kooka can be compiled
    with mild kde dependencies (kdelibs, libksane) which make it usable
    even if you don't have a full kde desktop.<br />
    Kooka is no longer present in KDE4, Kde now use kolourpaint and
    KOffice applications also using _libksane_ or {{< iref "#skanlite" "Skanlite" >}}.
-   {{< wp "Ocrad" >}}
    <a name="ocrad"></a>is an OCR
    program which read pbm (bitmap), pgm (greyscale) or ppm
    (color) image files and produces text in byte (8-bit) or UTF-8
    formats.
    Ocrad can be used as a stand-alone command-line application,
    or as a back-end to  {{< iref "#ocrfeeder" "OCRFeeder" >}},
    {{< iref "#ocrdjvu" "ocrdjvu" >}}; it is also one backend
    of {{< iref "#weocr" "WeOCR server" >}}.
    -   [Ocrad Home](http://www.gnu.org/software/ocrad/ocrad.html) (GPL)
    -   [Ocrad Manual](http://www.gnu.org/software/ocrad/manual/ocrad_manual.html)
-   <a name="ocrdjvu"></a>
    [ocrodjvu](http://jwilk.net/software/ocrodjvu) (GPL)
    is a wrapper for OCR systems, that allows you to perform OCR on
    DjVu files.
    It can use {{< iref "#ocrad" "ocrad" >}},
    {{< iref "#gocr" "gocr" >}},
    {{< iref "#cuneiform" "cuneiform" >}},
    or {{< iref "#tesseract" "tesseract" >}}.
    It is in Debian.
-   [Ocre](http://lem.eui.upm.es/ocre.html) (GPL) <a name="ocre"></a>
    OCR program that read PGM/PBM files. Ocre seems active (2013) but
    I have found very few documentation.
-   <a name="ocrfeeder"></a>{{< wp "OCRFeeder" >}} (GPL)
    is the gnome GTK frontend to
    {{< iref "#tesseract" "tesseract" >}},
    {{< iref "#ocrad" "ocrad" >}},
    {{< iref "#gocr" "gocr" >}},
    or {{< iref "#cuneiform" "cuneiform" >}}.
    It is a pyGTK program with heavy gnome dependencies.  It can
    import data from PDF or graphic files or grab images from the
    scanner device.  The results can be saved in HTML, OpenDocument,
    plain text or PDF.
    It outline the image contents, separate graphics and text and
    perform OCR over the latter.
    The graphical interface allow to interact with the recognition
    process.
    It is in Debian.
    -   [Ocrfeeder Gnome Home](http://live.gnome.org/OCRFeeder)
-   <a name="ocrivist"></a>
    [Ocrivist](http://www.ocrivist.com/)
    is a front end to scan document and save them in DjVu or PDF
    formats. They can also be processed by
    {{< iref "#tesseract" "Tesseract" >}} and saved in
    {{< iref "#hocr" "hOCR format" >}}.
-   <a name="ocropus"></a>{{< wp "OCRopus" >}} (Apache License 2)
    is a document analysis and OCR system written previously in in
    C++, and now in Python with a [C++ text line recognizer clstm
    ](https://github.com/tmbdev/clstm). It is based on a
    high-performance handwriting recognizer developed in the mid-90 by
    the US Census bureau, and novel high-performance layout analysis
    methods.  OCRopus development is sponsored by Google and is
    initially intended for high-throughput, high-volume document
    conversion efforts.
    -   [OCRopus alias ocropy Home](https://github.com/tmbdev/ocropy)
    -   Ocropus has been completely refactored in 2011, the old 0.3
        was in debian at the time of this writing _2015_ there is
        still no package for the new version, even if 1.0 has been
        released in 2014.
-   <a name="pdfsandwich"></a>
    [pdfsandwich](http://www.tobias-elze.de/pdfsandwich/index.html)
    is a script which calls  convert _from ImageMagick_,
    {{< iref "#unpaper" "unpaper" >}}, gs, and
    {{< iref "#tesseract" "tesseract" >}}
    to generates "sandwich" OCR pdf files, i.e. pdf files which
    contain  images and text from the OCR outpu added to each page
    invisibly _behind_ the images.

    It is able to recognize the page layout even for multicolumn text.
    pdfsandwich is in debian.

-   <a name="tesseract"></a>[Tesseract](https://github.com/tesseract-ocr/tesseract)
    (Apache 2.0 License) OCR engine was originally developed at HP between 1985
    and 1995.  It was open-sourced by HP and UNLV in 2005 and Google has lead further
    development. It is probably one of the most accurate open source OCR engines
    available. The source code will read a binary, grey or color image and output
    text. It has no output formatting.  Tesseract can detect fixed pitch vs proportional
    text.

    The UI are provided by [numerous third party clients
    ](https://github.com/tesseract-ocr/tesseract/wiki/3rdParty)

    Many frontends are referenced in this page:
    {{< iref "#ocrfeeder" "ocrfeeder" >}},
    {{< iref "#gimagereader" "gimagereader" >}},
    {{< iref "#gocr" "gocr" >}},
    {{< iref "#gscan2pdf" "gsscan2pdf" >}},
    {{< iref "#pypdfocr" "PyPDFOCR" >}},
    {{< iref "#ocrdjvu" "ocrdjvu" >}},
    {{< iref "#ocrmypdf" "OCRmyPDF" >}},
    {{< iref "#ocrivist" "OCRivist" >}},
    {{< iref "#tesseractgui" "Tesseract-GUI" >}},
    {{< iref "#yagf" "Yagf" >}}.

    -   Tesseract documentation is available in the
        [Wiki](https://github.com/tesseract-ocr/tesseract/wiki).
    -   There is a wide collection of [language data
        ](https://github.com/tesseract-ocr/langdata) many _but not
        all_ are provided as an individual packages in Debian.
    -   The Debian package _tesseract-ocr_ include tesseract command line tool, the
        engine is in _libtesseract3_.
    -   <a name="gimagereader"></a>
        [gimagereader](https://github.com/manisandro/gImageReader)
        is a graphical GTK+ front end for tesseract, it
        is free from gnome overloading and is in Debian.
    -    <a name="pypdfocr"></a>[PyPDFOCR](https://github.com/virantha/pypdfocr)
        (Apache License) is a python program that Take a scanned PDF file and run
        Tesseract OCR on it, generating a searchable PDF.
    -   <a name="ocrmypdf"></a>[OCRmyPDF](https://github.com/jbarlow83/OCRmyPDF) (GPL)
        is a python program that adds an OCR text layer to scanned PDF
        files, and generates a searchable PDF/A file from a regular
        PDF, producing a searchable pdf. It uses Tesseract OCR engine,
        all the tesseract languages are availables. It can deskews
        and/or cleans the image before performing OCR.
    -   <a name="tesseractgui"></a>
        [Tesseract-GUI](http://tesseract-gui.sourceforge.net/) (GPL)
        is a GUI to prepare raster files with Imagemagick for use
        with Tesseract. It provides a Debian package. _last release 2013_.

-   [Scan Tailor](https://github.com/scantailor/scantailor) (GPL)
    is an interactive post-processing tool for scanned pages. It
    performs operations such as page splitting, deskewing,
    adding/removing borders, and others. It is used for raw scans,
    before OCR and printing or assembling into a PDF or DJVU
    file. _Scan Tailor_ is written in C++ and is available as Debian
    package.
    -   [Bindery](https://github.com/Blender3D/Bindery)
        is a PyQt4 application that takes processed images from
        Scan Tailor and binds them into a DjVu or PDF document.

-   [unpaper](https://www.flameeyes.eu/projects/unpaper) (GPL) is a
    post-processing tool for scanned sheets of paper, especially for
    book pages that have been scanned from previously created
    photocopies.  The main purpose is to make scanned book pages
    better readable on screen after conversion to PDFand enhance the
    quality of scanned pages before performing optical character
    recognition (OCR).  Input and output files can be in either .pbm ,
    .pgm or .ppm format, conversion to PDF can e.g. be achieved with
    pgm2tiff, tiffcp and tiff2pdf.  Unpaper is in debian
    -   [unpaper GitHub repository
        ](https://github.com/Flameeyes/unpaper)
-  <a name="yagf"></a>[YAGF](http://symmetrica.net/cuneiform-linux/yagf-en.html)
   is a graphical interface for
   {{< iref "#cuneiform" "cuneiform" >}}and
   {{< iref "#tesseract" "tesseract" >}}.  With YAGF you can scan
   images via XSane, import pages from PDF documents, perform images
   preprocessing and recognize texts using
   {{< iref "#cuneiform" "cuneiform" >}} or
   {{< iref "#tesseract" "tesseract" >}}.
   Yagf is in Debian.

   -   [ArchWiki:Yagf](https://wiki.archlinux.org/index.php/YAGF).

## Web based OCR
-   [WeOCR](http://weocr.ocrgrid.org/) <a name="weocr"></a>
    is a platform for Web-enabled OCR (Optical Character
    Reader/Recognition) systems that enables people to use character
    recognition over networks.
    -   The servers themselves use either
        {{< iref "#gocr" "gocr" >}},
        {{< iref "#tesseract" "tesseract" >}}, or
        {{< iref "#ocrad" "ocrad" >}}
    -   WeOCR servers can be found at
        [WeOCR Server List](http://weocr.ocrgrid.org/search.html).
    -   Other servers can be found at
        [Web-based/online OCR services and demos
        ](http://www.ocrgrid.org/online-ocr.html)

-   [Free-OCR.com](http://www.free-ocr.com/)
    is a free online OCR,
    supported file types: jpg, png, bmp, pdf, jpeg, tiff, tif, gif.
    All submitted files or inputs as well as the converted output are
    deleted automatically after half an hour.
-   [i2OCR](http://www.i2ocr.com/)
    is a free Web based OCR that can recognize 60 languages.
    It supports the images formats jpg, png, bmp, tif, pbm, pgm, ppm,
    and  can extract text from multiple columns. The uploaded images
    or output files are not shared with third party, and are deleted
    after a short period, typically one hour.

## Commercial OCR software
-   [Omnipage](http://www.nuance.com/for-individuals/by-product/omnipage/index.htm)
    is an expensive windoze and Mac commercial OCR, the same firm nuance.com
    produces the speech recognition software for windoze and Mac
    [Dragon Naturally Speakink
    ](http://www.nuance.com/for-individuals/by-product/dragon-for-pc/index.htm)
-   [VueScan](http://www.hamrick.com/) is a commercial scanning
    software with OCR for windows, MacOsX and Linux. There are free
    Linux download.
-   {{< wp "ABBY" >}} has an OCR server, with [ocr4linux: a linux client
    ](http://www.ocr4linux.com/)
    licences are a one time payment life license: 149€/12000 pages/year.


<!--------------- refs -------------------------->
[libspectre]: http://www.freedesktop.org/wiki/Software/libspectre/
[pdfmark reference]: https://www.adobe.com/content/dam/acom/en/devnet/acrobat/pdfs/pdfmark_reference.pdf
[pdfmark reference - annotations]: https://www.adobe.com/content/dam/acom/en/devnet/acrobat/pdfs/pdfmark_reference.pdf#G6.1500496
[pdfmark reference - bookmark(out)]: https://www.adobe.com/content/dam/acom/en/devnet/acrobat/pdfs/pdfmark_reference.pdf#G6.1500812
[pdf 1.7 reference]: https://www.adobe.com/content/dam/acom/en/devnet/acrobat/pdfs/pdf_reference_1-7.pdf
[pdf 1.7 reference - chapter 8]: https://www.adobe.com/content/dam/acom/en/devnet/pdf/pdf_reference_archive/pdf_reference_1-7.pdf#G13.2023455
[pdf 1.7 reference - section 8.2]: https://www.adobe.com/content/dam/acom/en/devnet/pdf/pdf_reference_archive/pdf_reference_1-7.pdf#G13.1970991

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
