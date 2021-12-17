---
title: Vector Graphic software
---

The raster graphics are in the {{< iref "images" "Image Section" >}}, you find there also
the software which can deal both which raster and vector graphic.

See also the {{< iref "ps_pdf_djvu" "postscript, pdf, djvu Page" >}}.


# Documentation
-   Wikipedia: {{< wp "Scalable Vector Graphics" >}}
    an detailed review including support in browsers and software.
-   [Scalable Vector Graphics (SVG)](http://www.w3.org/Graphics/SVG/)
    from W3C
-   [Vector Markup Language (VML)
    ](http://www.w3.org/TR/1998/NOTE-VML-19980513)
    from W3C
-   [svg wiki](http://wiki.svg.org/)
-   [jan.kollhof.net svg pages](http://jan.kollhof.net/projects/svg/)

# Software {#svg_software}
{{<iref "images#imagemagick" "Image Magick" >}},
{{<iref "images#graphicsmagick" "Graphics Magick" >}} and
{{<iref "images#exactimage" "ExactImage" >}} are in the
{{< iref "images" "Images Section" >}}, they can work also with svg.

-   [Aafigure](https://pythonhosted.org/aafigure/)
    is used to convert drawings in plain text documents to HTML, PDF,
    SVG,png. It can be integrated with
    {{< iref "rest#docutils" "docutils" >}},
    {{< iref "rest#sphinx" "Sphinx" >}},
    [MoinMoin](http://moinmo.in/).

    Th Debian package is _python3-aafigure_.
-   [Autotrace](https://github.com/autotrace/) (GPL) is a bitmaps
    to vector graphics converter. It was and may be still the more
    achieved open source vectorisation program.

    The [Autotrace source forge project](http://autotrace.sourceforge.net/) is no
    longer developped since 2002 and the last version in sourceforge is 0.31.1 yer 2002.
    It was [packaged in Debian](https://tracker.debian.org/pkg/autotrace), but the last
    31.1 version has been removed since 2017. But the
    [Autotrace fork on GitHub](https://github.com/autotrace/) continued the maintenance.

    [autotrace Releases](https://github.com/autotrace/autotrace/releases) contains a deb
    package.

    -   [Online vectorizer](https://online-converting.com/autotrace/) uses autotrace and imagemagick.
-   [Blockdiag](http://blockdiag.com/en/index.html) is a set of graph generators
    from text source similar to {{< iref "#graphviz" "graphviz" >}}’s `dot` format.
    It includes  block diagrams, sequence diagrams,  activity diagrams, and network diagrams.<br />
    In the [sphinx contribs](https://bitbucket.org/birkenfeld/sphinx-contrib)
    there is a {{< iref "rest#sphinx" "Sphinx" >}} extension for _Blockdiag_.
-   [Dia](http://live.gnome.org/Dia) (GPL) a GTK+ based diagram
    creation program that save diagrams to a custom XML format and can
    export them to EPS, SVG, XFIG, WMF and PNG, ...
    Dia is packaged in Debian.
-   [Ditaa](http://ditaa.sourceforge.net/) (LGPL-3.0)
    is a command-line utility written in Java, that convert diagrams
    drawn using ascii art into bitmap graphics in _png_ format, the newer version can
    also output svg.
    -   _Ditaa_ can be used with _asciidoc_, _dokuwiki_.
    -   _Ditaa_ can be used  in Sphinx through the extension
        [sphinxcontrib-ditaa](https://pypi.org/project/sphinxcontrib-ditaa/),
    -   _Ditaa_ can be used in Pandoc with the
        [imagine](https://github.com/hertogp/imagine) filter.
    -   _Ditaa_ can be used in {{< iref "org-mode" "Org Mode" >}}
        see the syntax in [Worg - Ditaa Source Code Blocks in Org Mode
        ](https://www.orgmode.org/worg/org-contrib/babel/languages/ob-doc-ditaa.html)
        and [this example](http://doc.norang.ca/org-mode.html#playingwithditaa).
    -   [Ditaa - Github](https://github.com/stathissideris/ditaa)
 -   [Gnuplot](http://www.gnuplot.info/)
    [ad-hoc Open Source License
    ](http://gnuplot.cvs.sourceforge.net/gnuplot/gnuplot/Copyright)
    is a portable command-line driven interactive data and function plotting utility
    Gnuplot supports plots in either 2D and 3D, Gnuplot can output to many file formats
    (eps, fig, jpeg, LaTeX, metafont, pbm, pdf, png, postscript, svg, ...).
    -   [gnuplot development at sourceforge](http://gnuplot.sourceforge.net/)
         best site to find recent documentation, tutorials, demo.
    -   [gnuplot documentation](http://www.gnuplot.info/documentation.html):
        [gnuplot v4.6 manual](http://www.gnuplot.info/docs_4.6/gnuplot.pdf)
    -   [GNUPLOT 4.2 - A Brief Manual and Tutorial
        ](http://www.duke.edu/~hpgavin/gnuplot.html)
    -   [gnuplot demos](http://gnuplot.sourceforge.net/screenshots/)
-   <a name="inkscape"></a>[inkscape](http://www.inkscape.org/)
    is a SVG based generic vector-drawing program.
    -   Wikipedia {{< wp "Inskcape" >}}
    -   Documentation:
        [inskape manual
        ](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/index.php)
        by Tavmjong Bah in french or spanish
        _(Documenting Inkscape versions 0.47 and 0.48)_,
        [Inkscape User Manual
        ](http://www.angelfire.com/mi/kevincharles/inkscape/index.html)
        by Kevin Wixson,
    -   [Keys and Mouse Reference](http://www.inkscape.org/doc/keys.html),
    -   [TutorialsAndHelp
        ](http://wiki.inkscape.org/wiki/index.php/TutorialsAndHelp).
    -   When you install the _inskape package it places in the
        directory `/usr/share/inkscape` a directory of `examples` and
        `tutorials`
-   [ivtools](http://ivtools.sourceforge.net/ivtools/) (BSD-like license)
    X Windows drawing editors for
    PostScript, TeX, and web graphics and vector graphic shell

    It is packaged in Debian as the package _ivtools-bin_ which includes
    idraw, a basic vector graphics editor, graphdraw, flipbook, a vector graphics
    animation tool, a vector graphics server,

    -   [ivtools GitHub](https://github.com/vectaport/ivtools)
-   {{< wp "libsrvg" >}}
    is the gnome SVG rendering library  The  command-line _rsvg_
    part of the package _librsvg2-bin_ convert SVG files into
    raster images.
-   [Mscgen](http://www.mcternan.me.uk/mscgen/) (GPL)
    _no longer maintained since 2011_ is a  program that
    parses Message Sequence Chart descriptions and produces PNG, SVG, EPS
    or server side image maps (as the output.
    Mscgen integrates with _Asciidoc_, _Doxygen_, _Sphinx_, _Org Mode_, _Latex_.
-   [OpenClipArt](http://www.openclipart.org/) is a library of public domain clipart
    in vector format.
-   [potrace](http://potrace.sourceforge.net/) (GPL) is a vector conversion program
    that can transform bitmaps in PBM, PGM, PPM, or BMP format to vector
    graphics in EPS, PostScript, PDF, SVG, Xfig, Gimppath, and PGM.

    potrace is now embedded in inkscape, you find it in the menu
    `Path/Trace Bitmap` see also the
    [inkscape wiki](http://wiki.inkscape.org/wiki/index.php/Potrace).

    Potrace is packaged in Debian.

    -   Wikipedia {{< wp "Potrace" >}}
    -   [Online SVG Converter by Potrace](https://svg-converter.com/potrace).
    -   [Online Image Vectorizer](https://www.vectorization.org/) powered by potrace.
    -   [SVGcode—Convert](https://svgco.de/)
        (GPL-2.0)  convert raster images to SVG vector graphics with potrace.

        [SVGcode -GitHub](https://github.com/tomayac/SVGcode).
-   [pstoedit](http://www.pstoedit.net/pstoedit)
    (GPL) translates PostScript and PDF graphics into other vector
    formats: tgif, xfig, pdf, gnuplot, dxf-cad, hpgl, wmf, pic (troff),
    latex picture, kontour, plotutils, skencil, swf, svg, ...
    -   [pstoedit manual
        ](http://www.helga-glunz.homepage.t-online.de/pstoedit/pstoedit.htm)
-   [sK1](https://sk1project.net/) (GPL-3.0)
    is an open source vector graphics editor similar to CorelDRAW.  It
    is a fork of Sketch/Skencil. The development of Skencil stopped in
    2010 and the sk1 fork was launched and uses TK replacing GTK+ used by Skencil, but
    the newer version uses wxWidgets toolkit.

    Sk1 aims to be compatible with Corel Draw and Adobe Illustrator.

    The author and lead developper of Sk1 hor Novikov passed away at the age of 49 in
    March 2021, due to COVID-19.

    This application still uses only Python 2.x version.

    Packages for sk1 are available in
    [sk1 downloads](https://sk1project.net/sk1/download/).

    -   [SK1-wx - GitHub](https://github.com/sk1project/sk1-wx).
-   [tgif](http://bourbon.usc.edu:8001/tgif/) (Q public license
    *trolltech*) drawing Program for the X Window System.
    It supports PostScript formats suitable for LaTeX, as well as X11 bitmap or (version 1)
    pixmap formats. Other vector and raster image formats such as SVG and PNG can be
    handled via filters.
-   [Uniconvertor](https://sk1project.net/uc2/)  (AGPL-3.0) from the
    {{< iref "#sk1" "Sk1 project" >}}
    is a universal vector graphics translator.

    It can convert from:
    CorelDRAW, Adobe Illustrator, Postscript, Encapsulated Postscript,
    Computer Graphics Metafile, Windows Metafile (WMF), XFIG,
    Scalable Vector Graphics, Skencil/Sketch/sK1, Acorn Draw;
    to:
    Adobe Illustrator, Postscript, Computer Graphics Metafile, Windows Metafile,
    PDF, Sketch/Skencil, sK1, SVG.

    This application still uses only Python 2.x version.

    The Debian package
    [python-uniconvertor](https://tracker.debian.org/pkg/python-uniconvertor)
    was packaging the older version 1 and is removed since 2017.
    New packages can be found in [sk1 downloads
    ](https://sk1project.net/sk1/download/).

-   [Veusz](https://veusz.github.io/) (GPL-2.O)
    is a scientific plotting package written in python, PyQt and NumPy.  Veusz produces
    plots in PNG, PDF, Encapsulated PostScript and SVG.  Veusz is packaged in Debian.
    -   [Veusz -GitHub](https://github.com/veusz/veusz)
-   {{< wp "Xfig"g >}}
    A menu-driven tool to
    draw and manipulate objects interactively in an X window, with
    output to latex graphic formats or raster files thru *transfig.*
    It can also  embed images in formats
    such as GIF, JPEG, EPS (PostScript), etc.

    It export figures in the navive fig formatvector formats Postscript, EPS, PDF,
    Tex/Latex, PIC, Metafont, SVG ... and raster bitmap formats like png, gif, ppm, xbm,
    jpeg, tiff ... see the
    [list in the User Manual](http://mcj.sourceforge.net/frm_printing.html).

    Xfig is packaged in Debian.

    -   [Xfig Home and User Manual](http://mcj.sourceforge.net/).

## Online Web software
-   [draw.io](https://www.draw.io/) is an online free tool to edit
    diagrams. They can be saved in xml and exported as svg, or
    numerous raster formats.
-   [Gravit.io](http://gravit.io)
    is a web based drawing editor including Vector
    Illustration that can be exported as SVG.
-   [Inker](http://www.graphics.com/resource/inker)
    Is a free web based svg editor, that ca save in SVG and EPS.
    There is also an android app.
    -    [Inker web app](http://app.inker.co/)
-   [Vector Paint](http://vectorpaint.yaks.co.nz/)
    is an online Web SVG Editor, with svg download and optional export
    to png/speg.



# Graphviz {#graphviz}

[Graphviz](http://www.graphviz.org/) (Common Public License) is a
graph Visualization Software. It includes _dot_ for drawing directed
graphs, and _neato_ for drawing undirected graphs.

-   [An Introduction to GraphViz](http://www.linuxjournal.com/article/7275)
    by Mihalis Tsoukalos in _linux journal_.
-   [Graphviz Resources](http://www.graphviz.org/Resources.php)
-   Many python modules generate dot files and use them with
    graphviz:
    -   [python-graph](http://code.google.com/p/python-graph/)
        (MIT license) is a library for working with graphs in
        Python. It is in Debian.
    -   [GvGen](http://www.picviz.com/en/community/gvgen/gvgen.html)
        python class to produce dot language for easy scripting.
    -   [pydot](http://code.google.com/p/pydot/)(MIT License)
        allows to easily create both directed and non directed
        graphs from Python.
        It has Python 3 support.
    -   [yapgvb](http://code.google.com/p/yapgvb/) (BSD License)
        Python bindings to Graphviz,
    -   [NetworkX](http://networkx.lanl.gov/) package for the
        creation, manipulation, and study of the structure,
        dynamics, and functions of complex networks. It can output
        to Graphviz with[pygraphviz
        ](http://networkx.github.io/documentation/latest/examples/pygraphviz/)
    -   [dot2tex](https://pypi.python.org/pypi/dot2tex) (MIT
        License) by  Kjell Magne Fauske convert dot language to
        tex + PSTricks or PGF/TikZ.  [dot2tex source repository
        ](http://code.google.com/p/dot2tex/).
-   Some modules output a representaion of SQL Databases.
    -   [PostgreSQL Autodoc](http://www.rbt.ca/autodoc/index.html)
        run through PostgreSQL system tables and returns HTML, Dot,
        Dia and DocBook XML which describes the database.
    -   [SQLpp](http://www.codeproject.com/Articles/4603/A-scripted-SQL-query-generation-framework-with-IDEA)
        is a query generation framework with output to Dot.
    -   [SQLFairy](http://sqlfairy.sourceforge.net/)
        is a group of Perl modules that manipulate
        database schemas. It can convert among different dialects
        of CREATE syntax, visualizations of schemas with GraphViz
        or GD, automatic code generation, and more.
    -   [Sql2Dot](http://www.graphviz.org/Misc/sql2dot/)
        is a java parser to transform PostgreSQL sql into dot.
-   {{< iref "rest#sphinx" "Sphinx" >}}
    has the extension [sphinx.ext.graphviz
    ](http://sphinx-doc.org/ext/graphviz.html)
    to embed Graphviz graphs in Sphinx Rest.
    source.
-   [MediaWiki Extension: GraphViz
    ](http://www.mediawiki.org/wiki/GraphViz)
    uses Graphviz and Mscgen  to create and
    display graphs as inline images.
-   [Graphviz filter for AsciiDoc
    ](http://asciidoc.org/asciidoc-graphviz-sample.html)
    allow to draw graphs via graphviz in
    {{< iref "asciidoc" "Asciidoc" >}}.
-   [Worg Graphviz with Org Mode
    ](http://doc.norang.ca/org-mode.html#Graphviz),
    [Organize Your Life In Plain Text - Graphviz example
    ](http://doc.norang.ca/org-mode.html#Graphviz).
-   [gitit plugin Dot.hs
    ](https://github.com/jgm/gitit/blob/master/plugins/Dot.hs)
    allows you to include a graphviz dot diagram in a _gitit_ page.
-   [Xdot](http://code.google.com/p/jrfonseca/wiki/XDot) (LGPL) is an
    interactive viewer for Graphviz dot files written in python
    with PyGTK and Cairo.
-   [graph-easy](http://search.cpan.org/~tels/Graph-Easy/bin/graph-easy) (GPL)
    is a Perl module which can convert between many formats including
    _dot_ and render graphs.  You can use it to output to formats not
    supported by the graphviz suite, such as ASCII art.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
