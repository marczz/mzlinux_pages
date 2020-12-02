---
title: Data exchange formats
---

RSS and Atom formats are
{{< iref "feed#rss_formats" "in the Web Feed section" >}}.

See also {{< iref "shell#awk" "Awk" >}} in the {{< iref "shell" "Shell Page" >}}.

----

# General references

-   Wikipedia: {{< wp "Data exchange" >}}, {{< wp "serialization" >}},
    {{< wp "Comparison of data serialization formats" >}} (json, yaml, xml,
    property-lists, Comma-separated values, ...), {{< wp "Binary-to-text encoding" >}}
-   [dbohdan/structured-text-tools](https://github.com/dbohdan/structured-text-tools)
    An _awesome like_ list of command line tools for manipulating structured text data.

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
    and [awesome-Json-Datasets](https://github.com/jdorfman/awesome-json-datasets)
    lists of json resources.
-   [rson](https://code.google.com/p/rson/)
    is a format that sits between json and yaml a Python decoder is
    available.

## Json libraries and bindings
-   {{< iref "python_libraries#persistence_modules" "Python modules for Json" >}},
    and {{< iref "python_libraries#persistence_libs" "Json libraries" >}},
-   [Json in javascript](http://www.json.org/js.html)
-   [libjson](http://sourceforge.net/projects/libjson/)
    (FreeBSD License)is a fast, lightweight JSON parser written in C++.
-   [Yet Another JSON Library. YAJL](http://lloyd.github.io/yajl/)
    (ISC license)
    is a small event-driven (SAX-style) JSON parser written in ANSI C,
    and a small validating JSON generator. It has binding in python,
    lua, node.js, perl, ...


## Json online Tools
-   [jsonviewer.stack.hu
    ](http://jsonviewer.stack.hu/) is an Online Json viewer.
-   [online-toolz: Json Editor
    ](http://www.online-toolz.com/tools/json-editor.php)
-   [Json Editor Online
    ](http://www.jsoneditoronline.org/)
-   [Json Parser Online](http://json.parser.online.fr/)
-   [JSON Formatter
    ](http://www.freeformatter.com/json-formatter.html)
-   [convertjson.com](http://convertjson.com/) is a web service to convert
     HTML Table, XML, YAML, and CSV and the reverse conversion. There are also JSON
     viewer, lint, Formatter and a tool to display JSON Path Names or to query using
     JSON paths.

## json cli
-   [jq](https://stedolan.github.io/jq/) (MIT license)
    is a lightweight and flexible command-line JSON processor, written in C it is like
    sed for JSON data.

    -   [jq - GitHub](https://github.com/stedolan/jq/)
    -   [jq tutorial](https://stedolan.github.io/jq/tutorial/)
    -   [manual](https://stedolan.github.io/jq/manual/)
    -   [jq questions tagged jq](https://stackoverflow.com/questions/tagged/jq)
    -   [#jq](http://irc.lc/freenode/%23jq/) channel on
        [Freenode](https://webchat.freenode.net/).
    -   [jqplay.org](https://jqplay.org) an online A playground for jq.

-   [fx](https://github.com/antonmedv/fx) (MIT license)
    _fx_ is a command-line tool and terminal JSON viewer. Written in node js.
-   [jo](https://github.com/jpmens/jo) (GPL)
    _jo_ is a C utility to create JSON objects, It
    is in Debian (but the version may be old!), and a snap package is also available.
    -   There are rewrite of jo with other programming languages:
        [jjo in Node.js](https://github.com/memoryhole/jjo),
        [rjo in Rust](https://github.com/dskkato/rjo),
        [gjo in go](https://github.com/skanehira/gjo).
    -   [jo - cli.fan](https://cli.fan/posts/jo/)    .

## YAML {#yaml}
-   {{< wp "Yaml" >}} is a human-readable data serialization format designed
     to be easily mapped to  list, associative array, and scalar.<br />
    It is a superset of JSON and is more easily human readable, but
    harder to parse.
-   [YAML Home](http://www.yaml.org/about.html)
    contains a list of binding for programming languages.
-   [YAML specifications](http://www.yaml.org/spec/) (YAZML 1.2 2009)
    is a  comprehensive document with numerous examples.
-   [YAML Reference Card](http://www.yaml.org/refcard.html)
-   [The use of aliases in YAML
    ](https://github.com/cyklo/Bukkit-OtherBlocks/wiki/Aliases-(advanced-YAML-usage))
-   [StrictYAML](https://hitchdev.com/strictyaml/features-removed/)
    is a secure subset of _YAML_. It is also the name of the python parser for this
    subset.
    Colm O'Connor [compare _strict_ YAML with other formats
    ](https://hitchdev.com/strictyaml/#why-strictyaml)
    and explains why not use JSON/init/TOML/XML/python code, ... for configuration.
-   [awesome-yaml (dreftymac)
    ](https://github.com/dreftymac/awesome-yaml) and
    [Awesome Yaml (datatxt)](https://github.com/datatxt/awseome-yaml)
    lists of YAML resources.

### Yaml tools
See the _Yaml.org_ list of [YAML projects](https://yaml.org/).
and {{< iref "python_libraries#persistence_libs" "Python Libraries for Yaml" >}}

-   [yamllint](https://github.com/adrienverge/yamllint) is a python yaml validator.
    It is in Debian.
       -   [yamllint documentation
           ](https://yamllint.readthedocs.io/en/latest/index.html)
-   Yaml online validators at [yamllint.com](http://www.yamllint.com/) and
    [codebeautify.org](https://codebeautify.org/yaml-validator).
-   Yaml has a [binding for all main programming languages
    ](http://en.wikipedia.org/wiki/Yaml#Bindings).

# ToML

{{< wp "TOML" >}} is a minimal configuration file format that's easy to read, it maps
unambiguously to a hash table.

-   [GitHub - ToML](https://github.com/toml-lang/toml) the README cobtains the manual
    and examples.
-   [ToML Wiki](https://github.com/toml-lang/toml/wiki) with a [list of projrcts using
    ToMl](https://github.com/toml-lang/toml/wiki#projects-using-toml), and a
    [list of programming language implementations
    ](/github.com/toml-lang/toml/wiki#implementations).
-   [Comparison of TOML, JSON and YAML
    ](https://gohugohq.com/howto/toml-json-yaml-comparison/).

## Recutils
{{< wp "Recfiles" "Recutils" >}} is a file format for human-editable, plain text
databases.  recfiles allow for basic relational database operations, typing,
auto-incrementing, as well as a simple join operation.

A basic set of command lines is provided for manipulating them: `csv2rec`, `rec2csv`,
`recdel`, `recfix`, `recfmt`, `recinf`, `recins`, `recsel`, `recset`.

-   [GNU Recutils Manual](https://www.gnu.org/software/recutils/manual/index.html)
-   [Relational pipes](https://relational-pipes.globalcode.info/)
    are an open data format designed for streaming structured data between two processes.
    -   [Integrating Relational pipes with GNU Recutils
        ](https://relational-pipes.globalcode.info/v_0/examples-recfile.xhtml)
    -   [Reading an Atom feed using XQuery
        ](https://relational-pipes.globalcode.info/v_0/examples-xquery-atom.xhtml)
        and convert to the recfile format.
-   [python-recutils: Python bindings for librec
    ](https://github.com/maninya/python-recutils/)
-   [aisamanra/rrecutils](https://github.com/aisamanra/rrecutils/)
    A pure Rust implementation of the GNU Recutils format

# CSV

{{< wp "Comma-separated values" >}}  is a delimited text file that uses a comma to
separate values.

The name is used more widely for any delimiter separated values where the delimiter is
any character usually non alpha-numeric.

It is a very common data exchange format used by many spreadsheet and database software.

There is a an attempt to normalize CSV in the
[RFC 4180](https://tools.ietf.org/html/rfc4180)
and also a set of documents produced by the  W3C’s CSV on the Web Working Group, that you
find in [GitHub - w3c/csvw](https://github.com/w3c/csvw). It includes recommendations
for generating  {{< wp "Resource Description Framework" "RDF" >}} and JSON from CSV.

For examples of CSV and characters escape in fields look at the
{{< wp "Comma-separated values#Basic_rules" "Wikipedia CSV basic rules" >}}.

-   [convertcsv.com](http://convertcsv.com/)
    is a web service to convert CSV/Excel to and JSON,YAML, XML,HTML,SQL,Flat File,KML,..
    and the reverse back conversion.

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


## Office XML {#office_xml}

There are two concurent formats for representing spreadsheets, charts,
presentations and word processing documents in XML:

-   {{< wp " Office Open XML" >}} a specification originally by Microsoft and now
    the ISO ECMA-376 specification, starting with Microsoft Office
    2007, it has become the default file format of Microsoft Office.

    On Wikipedia here is a huge list of {{< wp "Office Open XML software" >}},
    allowed by the
    {{< wp "Microsoft_Open_Specification_Promise"  "Covenant Not to Sue of Microsoft" >}}.

    The ISO standard comprise 6546 pages to compare with the OpenDocument specification
    wich aim at he same goals and is only 867 pages in length.

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
    [libxslt Tutorial](http://xmlsoft.org/XSLT/tutorial/libxslttutorial.html) by
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
