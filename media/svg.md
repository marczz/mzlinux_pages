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

# Software
{{<iref "images#imagemagick" "Image Magick" >}} and
{{<iref "images#exactimage" "ExactImage" >}} are in the
{{< iref "images" "Images Section" >}}.

-   [Aafigure](http://packages.python.org/aafigure/)
    is used to convert drawings in plain text documents to HTML, PDF,
    SVG,png. It can be integrated with
    {{< iref "rest#docutils" "docutils" >}},
    {{< iref "rest#sphinx" "Sphinx" >}},
    [MoinMoin](http://moinmo.in/).
-   [Autotrace](http://autotrace.sourceforge.net/) (GPL) is a bitmaps
    to vector graphics converter. It was and may be still the more
    achieved open source vectorisation program. but don't seem any
    longer developped since 2004. [potracegui](http://potracegui.sourceforge.net)
    is a gui frontend that support potrace and autotrace.
-   [Blockdiag](http://blockdiag.com/en/index.html) is a set of graph generators
    from text source similar to {{< iref "#graphviz" "graphviz" >}}’s `dot` format.
    It includes  block diagrams, sequence diagrams,  activity diagrams, and network diagrams.<br />
    In the [sphinx contribs](https://bitbucket.org/birkenfeld/sphinx-contrib)
    there is a {{< iref "rest#sphinx" "Sphinx" >}} extension for _Blockdiag_.
-   [Dia](http://live.gnome.org/Dia) (GPL) a GTK+ based diagram
    creation program that save diagrams to a custom XML format and can
    export them to EPS, SVG, XFIG, WMF and PNG, ...
-   [Ditaa](http://ditaa.sourceforge.net/)
    ([Github](https://github.com/stathissideris/ditaa))
    is a java tool that convert ascii art to bitmap diagram (or EPS
    with a plugin), _no vector graphic presently_. It can be used
    in DocuWiki, in Sphinx through the extension
    [sphinxcontrib-ditaa](https://pypi.org/project/sphinxcontrib-ditaa/),
    in Pandoc with the [imagine](https://github.com/hertogp/imagine) filter,
    and in {{< iref "org-mode" "Org Mode" >}}
    see the syntax in [Worg - Ditaa Source Code Blocks in Org Mode
    ](https://www.orgmode.org/worg/org-contrib/babel/languages/ob-doc-ditaa.html)
    and [this example](http://doc.norang.ca/org-mode.html#playingwithditaa).
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
-   [ivtools](http://www.ivtools.org/ivtools/) drawing editors for
    PostScript, TeX, and web graphics and vector graphic shell
    _no longer developed, since 2009_.
-   {{< wp "libsrvg" >}}
    is the gnome SVG rendering library  The  command-line _rsvg_
    part of the package _librsvg2-bin_ convert SVG files into
    raster images.
-   [Mscgen](http://www.mcternan.me.uk/mscgen/) is a  program that
    parses Message Sequence Chart descriptions and produces PNG, SVG, EPS
    or server side image maps (as the output.
    Mscgen integrates with _Asciidoc_, _Doxygen_, _Sphinx_, _Org Mode_, _Latex_.
-   [OpenClipArt](http://www.openclipart.org/) is a library of public domain clipart in vector format.
-   [potrace](http://potrace.sourceforge.net/) (GPL) is a vector conversion program
    that can transform bitmaps in PBM, PGM, PPM, or BMP format to vector
    graphics in EPS, PostScript, PDF, SVG, Xfig, Gimppath, and PGM.
    potrace is now embedded in inkscape, you find it in the menu
    `Path/Trace Bitmap` see also the
    [inkscape wiki](http://wiki.inkscape.org/wiki/index.php/Potrace "/wiki.inkscape.org Potrace").<br />
    [potracegui](http://potracegui.sourceforge.net) (GPL) is a gui frontend
    for potrace and autotrace.
-   [pstoedit](http://www.pstoedit.net/pstoedit "pstoedit.net")
    (GPL) translates PostScript and PDF graphics into other vector
    formats: tgif, xfig, pdf, gnuplot, dxf-cad, hpgl, wmf, pic (troff),
    latex picture, kontour, plotutils, skencil, swf, svg, ...
    [pstoedit manual](http://www.helga-glunz.homepage.t-online.de/pstoedit/pstoedit.htm)
-   [Skencil](http://www.skencil.org/) (LGPL)
    is a vector drawing program. The development of Skencil stopped in
    2010, but the sK1 team gave a new start to the project, you find
    the new 1.x release on
    [sK1 page for Skencil
    ](http://sk1project.org/viewpage.php?page_id=21).
-   [sK1](http://sk1project.org/)
    is an open source vector graphics editor similar to CorelDRAW.  It
    is a fork of Sketch/Skencil, but while Skencil is developped
    against GTK+, sK1 uses TK. It also aim to be compatible with Corel
    Draw and Adobe Illustrator. It is packaged for main distributions.
-   [tgif](http://bourbon.usc.edu:8001/tgif/) (Q public license
    *trolltech*) drawing Program for the X Window System.
-   [Uniconvertor](http://sk1project.org/modules.php?name=Products&product=uniconvertor)
    is a universal vector graphics translator.<br />
    It can convert from:
    CorelDRAW, Adobe Illustrator, Postscript, Encapsulated Postscript,
    Computer Graphics Metafile, Windows Metafile (WMF), XFIG,
    Scalable Vector Graphics, Skencil/Sketch/sK1, Acorn Draw;
    to:
    Adobe Illustrator, Postscript, Computer Graphics Metafile, Windows Metafile,
    PDF, Sketch/Skencil, sK1, SVG.<br />
    It is available in Debian as _python-uniconvertor_.
-   [VectorMagic](http://vectormagic.com "/vectormagic.com")
    (proprietary closed license), convert bitmap images in
    JPEGs, GIFs and PNGs formats to EPS, SVG, and PDF
    It is a piece software  expensive to purchase, they also propose
    a 3 month subscription to online conversion, with a free trial.
-   [Veusz](http://home.gna.org/veusz/) (GPL)
    is a scientific plotting package written in python, PyQt and NumPy.
    Veusz produces plots in PNG, PDF, Encapsulated PostScript and SVG.
-   [XFig](http://www.xfig.org/ "xfig.org") A menu-driven tool to
    draw and manipulate objects interactively in an X window, with
    output to latex graphic formats or raster files thru *transfig.*

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
