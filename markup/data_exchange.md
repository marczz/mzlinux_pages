---
title: Data exchange formats
---

{{% toc /%}}

-   Wikipedia: {{< wp "Data exchange" >}}, {{< wp "serialization" >}},
    {{< wp "Comparison of data serialization formats" >}} (json, yaml, xml,
    property-lists, Comma-separated values, ...), {{< wp "Binary-to-text encoding" >}}
-   RSS and Atom formats are {{< iref "rss_readers#rss_formats" "in the rss readers section" >}}.


# Json/ Yaml

See also the related {{< iref "javascript" "Javascript Page" >}}

## Json  {#json}
-   {{< wp "Json"  "Wikipedia: Json" >}}
-   [Json Home](http://json.org/) with an introduction and a list of
    implementations in numerous languages.
-   Json format is defined in the
    [rfc4627](http://www.ietf.org/rfc/rfc4627.txt).
-   {{< wp "JsonML" >}} JSON Markup Language is  used to map between XML  and JSON.
    JsonML allows easy manipulation of the markup in JavaScript.
    [JsonML.org Home](http://jsonml.org/).<br />
-   [awesome-json](https://github.com/burningtree/awesome-json)
    and [awesome-Json-Datasets
    ](https://github.com/jdorfman/awesome-json-datasets)
    lists of json resources.
-   [rson](https://code.google.com/p/rson/)
    is a format that sits between json and yaml a Python decoder is
    available.

## Json libraries and bindings
-   {{< iref "python_libraries#serializing_modules" "Python modules for Json" >}},
    and {{< iref "python_libraries#serializing_libs" "libraries" >}},
-   [Json in javascript](http://www.json.org/js.html)
-   [libjson](http://sourceforge.net/projects/libjson/)
    (FreeBSD License)is a fast, lightweight JSON parser written in C++.
-   [Yet Another JSON Library. YAJL](http://lloyd.github.io/yajl/)
    (ISC license)
    is a small event-driven (SAX-style) JSON parser written in ANSI C,
    and a small validating JSON generator. It has binding in python,
    lua, node.js, perl, ...

## Json Tools
-   [jsonviewer.stack.hu
    ](http://jsonviewer.stack.hu/) is an Online Json viewer.
-   [online-toolz: Json Editor
    ](http://www.online-toolz.com/tools/json-editor.php)
-   [Json Editor Online
    ](http://www.jsoneditoronline.org/)
-   [Json Parser Online](http://json.parser.online.fr/)
-   [JSON Formatter
    ](http://www.freeformatter.com/json-formatter.html)

## Yaml {#yaml}
-   {{< wp "Yaml" >}} is a human-readable data serialization format designed
     to be easily mapped to  list, associative array, and scalar.<br />
    It is a superset of JSON and is more easily human readable, but
    harder to parse.
-   [Yaml Home](http://www.yaml.org/about.html)
-   [Yaml specifications](http://www.yaml.org/spec/)
    is a  comprehensive document with numerous examples.
-   [Yaml Reference Card](http://www.yaml.org/refcard.html)
-   [awesome-yaml (dreftymac)
    ](https://github.com/dreftymac/awesome-yaml) and
    [Awesome Yaml (datatxt)](https://github.com/datatxt/awseome-yaml)
    lists of YAML resources.
-   Yaml has a [binding for all main programming languages
    ](http://en.wikipedia.org/wiki/Yaml#Bindings).
-   {{< iref "python_libraries#serializing_libs" "Python Libraries for Yaml" >}}


# XML {#xml}

## Xml References
-   [The World Wide Web Consortium](http://www.w3.org/) (w3.org)
    -   [XML](http://www.w3c.org/XML/), [XSL](http://www.w3.org/Style/XSL/)
    -   [HTML Working Group](http://www.w3.org/html/wg/)
    -   [Cascading Style Sheets](http://www.w3.org/Style/CSS/)
    -   [Accessibility]( http://www.w3.org/WAI/)
-   [w3schools.com Xml Index](http://www.w3schools.com/xml/)
-   [XML FAQ](http://www.ucc.ie/xml/) (Peter Flynn)
-   [ZVON.org](http://www.zvon.org/) XML References and tutorials _up to 2007_
-   [Relax NG links][12] from James Clark.
-   [Dave Pawson]( http://www.dpawson.co.uk/):
    [Docbook Frequently Asked Questions
    ](http://www.dpawson.co.uk/docbook/) _2009_,
    [XSL Frequently Asked Questions](http://www.dpawson.co.uk/xsl/)
    _2005_,
    [Relax-ng FAQ]( http://www.dpawson.co.uk/relaxng/) _2004_
-   [xml.com](http://www.xml.com/) ressources and advertisements!
-   [Scott Hudson's blog on XML, DocBook, ....
    ](http://shudson310.blogspot.com/)

## Xml Tools
{{< iref "emacs#xml_emacs" "Xml edition with Emacs" >}}
is in {{< iref "emacs" "Emacs Section" >}}.xs

-   [Apache XML Project](http://xml.apache.org/)( Xerces: XML
    parsers in Java and C++, Xalan: XSL stylesheet processors in Java
    & C+, Cocoon: XML-based web publishing, FOP: XSL Formatting Object
    processor in Java, SOAP: Simple Object Access Protocol,)
-   [Lars Marius Garshol](http://www.garshol.priv.no/) has many xml
    links _seem outdated?_
-   [James Clark's XML resources](http://www.jclark.com/xml/)[TREX,
    XP, Expat, SP, XT ]. The nxml mode
    settings are discussed in the
    [EmacsWiki NxmlMode
    ](http://www.emacswiki.org/emacs/NxmlMode).
-   [SP](http://www.jclark.com/sp/)de James Clark
-   [IBM XML page](http://www.software.ibm.com/xml/)
-   [XML and Scheme](http://okmij.org/ftp/Scheme/xml.html) ( SSAX,
    SXML, SXPath, SXSLT ) from the
    [Scheme section](http://okmij.org/ftp/Scheme) of the
    [http://pobox.com/\~oleg/ftp/](http://okmij.org/ftp/)
-   [Expat XML Parser](http://expat.sourceforge.net) _2007_
-   [The Library LT XML](http://www.ltg.ed.ac.uk/software/xml/)
    which provides numerous utility programs as sggrep, sgmltrans,
    sgrpg, sgcount, knit, unknit, sgmltoken, sgmlseg, sgmlsb, pesis,
    xmlnorm, textonly, sgsort, nslshowddb,
-   [libxml2](http://xmlsoft.org/) is the XML C parser and toolkit
    developed for the Gnome project (but usable outside of the Gnome
    platform) [lxml](http://codespeak.net/lxml/) is a Pythonic binding
    for the libxml2 and libxslt libraries.
-   [QAML Question-Answer Xml for FAQ
    ](http://www.ascc.net/xml/en/utf-8/qaml-index.html)
-   [sgrep](http://www.cs.helsinki.fi/~jjaakkol/sgrep.html) a xml
    grep program
-   [Jaxe](http://jaxe.sourceforge.net/en/) (GPL)
    is an xml editor written in java.
-   xmlto is a front-end to an XSL toolchain. It chooses an appropriate
    stylesheet and applies it using an
    external XSLT processor (currently xsltproc) and
    performs any necessary post-processing.
    It supports conversion from docbook, xhtml1 and fo  to
    awt, fo, htmlhelp, javahelp, mif, pdf, svg, xhtml,
    dvi, html, html-nochunks, man , pcl, ps, txt, xhtml-nochunks.
    The outpu is produced with any of the supported toolchains -
    dblatex, PassiveTeX or docbook-xsl/fop.

## Docbook {#docbook}

-   [Docbook OASIS home page](http://www.oasis-open.org/docbook)
-   sourceforge [DocBook Open Repository
    ](http://docbook.sourceforge.net/)
    (downloads, wiki, faq, documentation, [xsl stylesheet
    documentation](http://docbook.sourceforge.net/release/xsl/current/doc/))
-   [DocBook XSL: The Complete
    Guide](http://www.sagehill.net/docbookxsl/) by Bob Stayton is an
    online reference book on the docbook xsl stylesheets.
-   [DocBook FAQ](http://www.dpawson.co.uk/docbook/) _2009_
-   [db2latex](http://db2latex.sourceforge.net/whatis.html "db2latex.sourceforge.net")
    docbook to latex converter superseded by dblatex.
-   [DbLatex](http://dblatex.sourceforge.net/ "dblatex.sourceforge.net")
    transforms DocBook SGML/XML documents into PDF, PostScript, and DVI
    by translating first to LaTeX. it is based on db2latex.
-   [A minimal DocBook setup on
    Unix](http://aeditor.rubyforge.org/mini_docbook.html) from Simon
    Strandgaard deal with xml catalogs for docbook.
-   [Publican](https://fedorahosted.org/publican/)
    is a DocBook XML publication system. Publican automates producing
    documentation in  plain text, HTML and PDF. A Publican package is
    in debian.
    [Asciidoctor can convert AsciiDoc to DocBook for use with Publican
    ](https://github.com/asciidoctor/asciidoctor/wiki/Convert-Asciidoc-to-Docbook-for-use-with-Publican).
-   [DocBook Doclet (dbdoclet)](http://www.dbdoclet.org/) (GPL)
    is a java program that creates DocBook XML and class diagrams
    from Javadoc comments, converts HTML to DocBook, and transfoms
    DocBook XML into various output formats.
    [Herold](http://www.dbdoclet.org/projects/herold/index.html)
    is an HTML to DocBook converter. Both dbdoclet and
    herold are in Debian.


# Office XML {#office_xml}

There are two concurent formats for representing spreadsheets, charts,
presentations and word processing documents in XML:

-   {{< wp " Office Open XML" >}} a specification originally by Microsoft and now
    the ISO ECMA-376 specification, starting with Microsoft Office
    2007, it has become the default file format of Microsoft Office.

    On Wikipedia here is a huge list of {{< wp "Office Open XML software" >}},
    allowed by the {{< wp "Microsoft_Open_Specification_Promise"  "Covenant     Not to Sue of Microsoft" >}}.

    The ISO standard comprise 6546 pages to compare with the
    OpenDocument specification wich aim at he same goals and is only
    867 pages in length.

-   {{< wp "OpenDocument" >}} (ODF) is an XML open OASIS standard. It has been
    developped by Sun Microsystems with IBM contributions.

    The leading implementation is {{< wp "OpenOffice.org" >}}, and
    its fork {{< wp " LibreOffice" >}}

-   Wikipedia a list of {{< wp "OpenDocument software" >}}

# XSL {#xsl}

-   [W3C XSL Page](http://www.w3.org/Style/XSL/):
    [XSLT 1.0](http://www.w3.org/TR/xslt),
    [XPath 1.0](http://www.w3.org/TR/xpath),
    [XSLT 2.0](http://www.w3.org/TR/xslt20/),
    [XPath 2.0](http://www.w3.org/TR/xpath20/).
-   [The SAXON XSLT Processor](http://saxon.sourceforge.net/)
-   [TUTORIAL XSL Par Alain DESEINE
    ](http://www.cabinfo.com/xsltut/xsl_tut.htm)
-   [pyxml general resources about XML](http://pyxml.sourceforge.net/topics/xml.html)
-   [XSL FAQ](http://www.dpawson.co.uk/xsl/) from Dave Pawson _2005_
-   [Jeni Tennison's XSLT Pages](http://www.jenitennison.com/xslt/)
-   [The XSLT C library](http://xmlsoft.org/XSLT/):
    [xsltproc user manual](http://xmlsoft.org/XSLT/xsltproc.html),
    [libxslt
    Tutorial](http://xmlsoft.org/XSLT/tutorial/libxslttutorial.html) by
    John Fleck.
-   [XML resources publication guidelines
    ](http://xmlsoft.org/guidelines.html)
    also contains a chapter on xml catalogs
-   [How to write an XML catalog file
    ](http://www.sagehill.net/docbookxsl/WriteCatalog.html)
    from [DocBook XSL: The Complete Guide
    ](http://www.sagehill.net/docbookxsl/)
-   [XSL Transformations (XSLT) in Mozilla
    ](http://www.mozilla.org/projects/xslt/)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
