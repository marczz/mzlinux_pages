---
title: reStructuredText
---

{{% toc /%}}

# ReStructured Text References
-   <a name="docutils"></a>[Docutils
    ](http://docutils.sourceforge.net/index.html)
    is a a set of tools for processing plaintext
    documentation into useful formats, such as HTML, XML, and LaTeX,
    or S5 slides. It uses [reStructuredText][rest] markup syntax. It
    is a
    [public domain software with few exceptions
    ](http://svn.berlios.de/viewvc/docutils/trunk/docutils/COPYING.txt?view=markup)
-   [reStructuredText][rest] syntax is detailed in the official
    [reStructuredText Markup Specification
    ](http://docutils.sourceforge.net/docs/ref/rst/restructuredtext.html),
    [A ReStructuredText Primer
    ](http://docutils.sourceforge.net/docs/user/rst/quickstart.html),
    [The reStructuredText Cheat Sheet
    ](http://docutils.sourceforge.net/docs/user/rst/cheatsheet.html).
-   [Docutils Configuration](http://docutils.sourceforge.net/docs/user/config.html).
-   There are also useful unofficial doc:
    [Sphinx: reStructuredText Primer
    ](http://sphinx.pocoo.org/rest.html)
    [Restructured Text (reST) and Sphinx CheatSheet
    ](http://openalea.gforge.inria.fr/doc/openalea/doc/_build/html/source/sphinx/rest_syntax.html),
    [rules, tips, and tricks for using Sphinx and reStructuredText
    ](http://docs.geoserver.org/trunk/en/docguide/sphinx.html)
    or this [Christoph Reller: restructured tutorial
    ](http://people.ee.ethz.ch/~creller/web/tricks/reST.html)

# ReSt on the web
-   ReStructuredText be used in
    [MoinMoin](http://moinmo.in/HelpOnParsers/ReStructuredText),
    [Trac Wiki](http://projects.edgewall.com/trac/wiki),
    [MediaWiki with an extension
    ](http://www.mediawiki.org/wiki/Extension%3aRstToHtml),
    the single-file personal wiki [rstwiki
    ](http://www.asynchronous.org/rstiki/).
-   It is supported by many {{< iref "static_sites" "static sites generators" >}}:
    {{< iref "static_sites#gollum-site" "Gollum-Site" >}},
    {{< iref "static_sites#handcrank" "Handcrank" >}},
    {{< iref "static_sites#hyde" "Hyde" >}},
    {{< iref "static_sites#jekyll" "Jekyll" >}},
    {{< iref "static_sites#nicola" "Nicola" >}},
    {{< iref "static_sites#pelican" "Pelican" >}},
    {{< iref "static_sites#soho" "Soho" >}},
    {{< iref "static_sites#wok" "Wok" >}},
-   [rest2web](http://www.voidspace.org.uk/python/rest2web/)
     is a web site builder from one or many
     template and content in ReStructured Text.
-   [flask-rst](https://github.com/jarus/flask-rst) create a site from rst content with
    [flask](http://flask.pocoo.org/docs/).


# ReSt tools.
-   {{< iref "emacs" >}} has a
    [reStructuredText mode](http://docutils.sourceforge.net/docs/user/emacs.html).
-   <a name="vim_rst"></a>{{< iref "text_editors#vim" "Vim" >}}
    has many plugins to support ReSt
    -   [riv.vim](https://github.com/gu-fan/riv.vim)
        is a vim plugin for taking notes with reStructuredText.
    -   [InstantRst](https://github.com/gu-fan/InstantRst) a vim plugin for instant rst
        preview in browser.
    -   [syntastic](https://github.com/vim-syntastic/syntastic)
        a syntax checking plugin for Vim, that can check a vast collection of languages
        including ReSt.
    -   [vim-rst-tables](https://github.com/nvie/vim-rst-tables)
        to create and reformat your reStructuredText tables as you change cell content.
    -   [VST - Vim reStructured Text
        ](https://www.vim.org/scripts/script.php?script_id=1334) an old _unmaintained
        since 2006_ vim plugin for ReSt.
-   [Bruce](http://pypi.python.org/pypi/bruce)
    is a presentations tool using ReSt plain text files. It allows
    xt, code, image, interative Python sessions and video.
-   [restview](https://github.com/mgedmin/restview) is a ReStructuredText viewer
    that renders documents on the fly. It is
    [in PyPI](https://pypi.org/project/restview/).

# Rest conversion

-   [Docutils](http://docutils.sourceforge.net/index.html) contains
    a basic pack of converters from ReST  in the [tool section
    ](http://svn.berlios.de/viewvc/docutils/trunk/docutils/tools/):
    [rst2html](http://docutils.sourceforge.net/docs/user/html.html) with various
    renderers, [rst2odt](http://docutils.sourceforge.net/docs/user/emacs.html),
    [rst2latex](http://docutils.sourceforge.net/docs/user/latex.html),
    rst2xetex, [rst2man](http://docutils.sourceforge.net/docs/user/manpage.html),
    rst2s5,
    [rst2odt](http://docutils.sourceforge.net/docs/user/odt.html).
-   [rst2odp](http://pypi.python.org/pypi/rst2odp)  convert from rst
    to open office impress odp format.
-   [odt2sphinx](https://bitbucket.org/cdevienne/odt2sphinx)
    (Python Software Foundation License)
    converts OpenDocument Text file(s) to one or several .rst files.
    It is [available on pypi](https://pypi.python.org/pypi/odt2sphinx/)
-   [rst2beamer](http://pypi.python.org/pypi/rst2beamer/)
     and [slides](http://pypi.python.org/pypi/slides) convert from reStructuredText
     to LaTeX beamer Presentation class.
-   [rst2slides](http://pypi.python.org/pypi/rst2slides) rst to html5 presentation,
    [rst2slides demo](http://packages.python.org/rst2slides)
-   [rst2texinfo](https://bitbucket.org/jonwaltman/rst2texinfo/)
    by  Jon Waltman adds support
    for generating Texinfo files from reStructuredText.
    A texinfo buider is now part of Sphinx since v 1.1.
-   You can convert html to rst by using the python program
    [html2rst.py](http://docutils.sourceforge.net/sandbox/cliechti/html2rst/html2rst.py)
    by Aaron Swartz and Chris Liechti,
    [xhtml2rest.py](http://docutils.sourceforge.net/sandbox/xhtml2rest/xhtml2rest.py)
    by Antonios Christofides,
    [html2rest.py](https://github.com/podados/python-html2rest)
    by Gerard Flanagan [available in pypi
    ](https://pypi.python.org/pypi/html2rest).
-   You can also use the Haskell program
    [pandoc](ttp://johnmacfarlane.net/pandoc/)
    by John MacFarlane or the web front-end
    [html2x](http://johnmacfarlane.net/pandoc/html2x.html).
    [pandoc](ttp://johnmacfarlane.net/pandoc/)
    command line use is:

        pandoc -f html -t rst input.html > output.rst

-   [db2rst](http://code.google.com/p/db2rst/) (BSD License)
    from Marcin Wojdyr  converts docbook to rst with sphinx markup.
    It has many forks  on GitHub:
    [by Kurt McKee](https://github.com/kurtmckee/db2rst),
    [by Gervase Markham](https://github.com/gerv/bzdocs),
    [by Eron Hennessey](https://github.com/EronHennessey/db2rst)
-   pandoc can be used also to
    [produce slide shows
    ](http://johnmacfarlane.net/pandoc/README.html#producing-html-slide-shows-with-pandoc)
    with {{< iref "html#slidy" "S5 or Slidy" >}}.
    (available from markdown, reStructuredText, (subsets of) HTML, and LaTeX)
-   [rst2s5](http://docutils.sourceforge.net/docs/user/slide-shows.html)
    generates S5 presentations from ReStructuredText.
-   [landslide](https://github.com/adamzap/landslide)
    is a python program that generate
    html5 slides from MarkDown or ReStructuredText.
-   [tex2_rst_html](https://github.com/ketch/tex2_rst_html)
    are python scripts for converting laTeX and Bibtex
    to ReStructured Text (.rst) and html.
-   [rst2rst](https://github.com/benoitbryon/rst2rst)
    a python utility to transform reStructuredText documents, and standardize RST syntax.
    It is in _PyPi_.
-   [rst2ansi](https://github.com/Snaipe/python-rst2ansi)
    A python utility for rendering RST in the terminal. It is in _PyPi_.

# Sphinx {#sphinx}

[Sphinx][sphinx] (BSD license) is a documentation generator that
[uses ReST](http://sphinx.pocoo.org/rest.html) to generate all the
python official documentation. It allows generation of HTML in many
formats, HtmlHelp, TexInfo, Epub, man page, LaTeX
[and more](http://sphinx.pocoo.org/latest/builders.html).

-   Documentation at [Sphinx Home][sphinx],
    [Documenting Your Project Using Sphinx
    ](http://packages.python.org/an_example_pypi_project/sphinx.html),
    and the reST documentation cited above.
-   [awesome-sphinx](https://github.com/yoloseem/awesome-sphinxdoc)
    list of extra libraries  software and resources for Sphinx.
-   Doug Hellmann explains his editorial Toolchain in
    [Writing Technical Documentation with Sphinx, Paver, and Cog
    ](https://doughellmann.com/blog/2009/02/02/writing-technical-documentation-with-sphinx-paver-and-cog/),
    he also has done a tutorial for [defining custom roles in Sphinx
    ](https://doughellmann.com/blog/2010/05/09/defining-custom-roles-in-sphinx/)
-   {{< iref "python_programming#epydoc" "Epydoc" >}} can use restructured text, it adds
    [epydoc fields](http://epydoc.sourceforge.net/manual-fields.html) and some
    [extension to rst language
    ](http://epydoc.sourceforge.net/manual-othermarkup.html#restructuredtext).
-   [Read the Doc](http://read-the-docs.readthedocs.org/en/latest/index.html)
    hosts open source documentation. It supports Sphinx,
    and can pull from your Subversion, Bazaar, Git, and Mercurial repositories.

## Sphinx extensions
-   The [manual describe Sphinx extensions and list built-in extensions
    ](http://sphinx.pocoo.org/extensions.html)
-   The [Sphinx extension contrib repository
    ](https://bitbucket.org/birkenfeld/sphinx-contrib)
    contains many Sphinx extension.
    -   multiple figure and diagram inclusions extensions including
        [Graphviz](http://sphinx-doc.org/ext/graphviz.html), aafigure, nwdiag, ...
        look at the list in the repository for more.
    -   epydoc extension to cross-reference epydoc generated documentation.
    -   Excel spreadsheets embedding
-   [sphinx-ditaa](https://github.com/baloo/sphinx-ditaa/blob/master/README.md) an extension
    for ditaa diagrams.
-   [PGF/TikZ figures extension
    ](http://people.ee.ethz.ch/~creller/web/tricks/sphinx-tikz.html)
-   [Hieroglyph](http://yergler.net/projects/hieroglyph/) (BSD license)
    is an extension for Sphinx which builds HTML slides.
-   [rst2pdf](http://rst2pdf.ralsina.com.ar/) (MIT license)
    is a pdf generator from _ReSTructured text_ based on the
    [ReportLab toolkit](http://www.reportlab.com/). It accepts  _Sphinx_
    extension and works also as a _Sphinx_ extension.
    -   [rst2pdf manual](http://rst2pdf.ralsina.com.ar/handbook.html)
    -   [rst2pdf source code](https://rst2pdf.googlecode.com/)
    -   [rst2pdf online converter](http://www.rst2pdf.net/)

## Sphinx themes
Sphinx has
[theming support](http://sphinx-doc.org/latest/theming.html)
and a collection of [builtin themes
](http://sphinx-doc.org/latest/theming.html#builtin-themes).

-   [Sphinxjp.themes.s6](http://pypi.python.org/pypi/sphinxjp.themes.s6/)
    is a sphinx theme for generate S6 presentation.
-   [sphinxjp.themes.htmlslide](http://pypi.python.org/pypi/sphinxjp.themes.htmlslide)
    is a sphinx theme for generate HTML Slide presentation.
    It shows slides on any modern javascript enabled browsers.
    The animation are owly available on
    browsers that support html5.
-   [Cloud Sphinx Theme](http://pythonhosted.org/cloud_sptheme/) (BSD License),
    [Bitbucket repository](https://bitbucket.org/ecollins/cloud_sptheme),
    [Pypi: cloud_sptheme](https://pypi.python.org/pypi/cloud_sptheme)
-   [Pylon Sphinx Theme
    ](http://docs.pylonsproject.org/projects/pyramid_tutorials/en/latest/_themes/README.html):
    [GitHub: Pylon Sphinx Theme](https://github.com/Pylons/pylons_sphinx_theme)
-   [Sphinx Bootstrap Theme
    ](https://github.com/ryan-roemer/sphinx-bootstrap-theme) (MIT
    License): [Sphinx Bootstrap Theme Demo
    ](http://ryan-roemer.github.io/sphinx-bootstrap-theme/),
    [Pypi: Sphinx Bootstrap Theme
    ](https://pypi.python.org/pypi/sphinx-bootstrap-theme/).
-   [Linfiniti Sphinx Theme
    ](https://github.com/timlinux/linfiniti-sphinx-theme) an older and
    simpler bootstrap theme for Sphinx.
-   [Sphinx theme for readthedocs.org
    ](https://github.com/snide/sphinx_rtd_theme) can also be used in
    other places. It is a mobile-friendly sphinx theme.

[rest]: http://docutils.sourceforge.net/rst.html
[sphinx]: http://sphinx.pocoo.org

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
