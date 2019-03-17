<!--
.. description:
.. date: 2015-06-04
.. slug: source_code
.. tags:
.. link:
.. title: Source Code
-->

[TOC]

# Literate Programming {#literate_programming}

This section is about literate programming and source code
documentation, if you extract both the code and documentation from the
same piece of text, you do
literate programming. If you extract your doc from your program,
you are doing source code documentation. But there is no crisp barrier
between the two concepts.

The two main components in traditional literate programming languages
like [w:WEB] or [w:CWEB] are *tangle*, which produces compilable code
from the source texts, and *weave*, which produces nicely-formatted
documentation.

There is a related
[section on source code beautifiers](#code_beautifiers "internal reference").

-   [w:Literate_programming|Wikipedia: Literate programming]
-   [SGML/XML and Literate Programming](http://www.oasis-open.org/cover/xmlLitProg.html)
-   [www.literateprogramming.com](http://www.literateprogramming.com/)
    is an _outdated_ index of literate programming links and book reviews.
-   [antiweb](http://packages.python.org/antiweb/) (GPL)
    <a name="antiweb"></a>
    ([Pypi entry](ihttp://pypi.python.org/pypi/antiweb/))
    is an inverse literate programming tool in the [noweb](#noweb) family..
    In opposite to _web_ the documentation is weaved from syntactic correct source code.
    The result is a restructed text file, that can be used in the
    [sphinx document generator](/node/405#sphinx "internal reference").
-   [Cog](http://nedbatchelder.com/code/cog/) (MIT license.)
    <a name="cog" "Internal reference"></a>
    is a code generation tool. It is a preprocessor with all power of
    python. While __Cog__ is mainly aimed at *tangling* a source file with included python chunks,
    it can be also combined  with [Sphinx](/node/405 "internal reference")
    for documentation generation as described in
    [Producing documentation for python code in a file with reST, docutils, cog and paver
    ](http://oneau.wordpress.com/2010/05/24/documenting-python-code-with-rest-docutils-pygments-cog-and-paver/)
-   [Docco](http://jashkenas.github.io/docco/) is a documentation
    generator, written in Literate CoffeeScript. It produces an HTML
    document that displays your comments in Markdown intermingled with
    your code with syntax highlighting with
    [Highlight.js](#highlight_js "internal Reference").
-   [Doxygen](http://www.stack.nl/~dimitri/doxygen) is a documentation
    system for C++, C, Java, Objective-C, Python, IDL.
    [Doxymacs](http://doxymacs.sourceforge.net/) make using Doxygen
    from within {X}Emacs easier.
-   [FunnelWeb](http://www.ross.net/funnelweb/) a language independant
    literate programming tool which use a common source file to *tangle*
    a program and weave a latex or html documentation. .
-   [Haskell](/node/44#haskell "Internal link") has semi literate programming support.
    It can extract the source code from a _LaTeX_ source.
-   The [w:Leo_(text_editor)|Leo text editor] is an outlining editor which supports
    optional noweb and CWEB markup.
-   [w:noweb]<a name="noweb"></a> is a literate programming tool, created in 1989 by
    Norman Ramsey. It has *tangle* and *weave* components as do
    [w:WEB] or [w:CWEB] but is independent of the code language.
    [noweb Home](http://www.cs.tufts.edu/~nr/noweb/).
    -   Noweb has a python clone
        [noweb.py](https://github.com/JonathanAquino/noweb.py)
        that uses the  noweb syntax.
-   [Pnw](https://pypi.python.org/pypi/pnw/) (Apache license)
     is a text processing and literate programming tool inspired by
    [antiweb](#antiweb) and [noweb](#noweb).
-   [PyLit](https://pypi.python.org/pypi/pylit) (GPL) is a python tool that feature a
    _bidirectional text/code converter_; it can convert between the _code_ form
    and the _text_ form  the _code_  without loss of information.
    [PyLit3](https://github.com/slott56/PyLit-3) (GPL) is a fork for Python3 by Steven Lott.
-   [pyreport](http://gael-varoquaux.info/computers/pyreport/) (BSD-like license)
    runs a python script and captures its output, compiling it to a
    report in a pdf or an html file.
-   [pyWeb]( http://pywebtool.sourceforge.net/)
    is a literate programming tool written in python that combines
    the actions of _weaving_ a document with _tangling_ source files.
    It is independent of any particular document markup or source language.
    It uses a simple set of markup tags to define chunks of code and documentation.
    Steven Lott, author of PyWeb [advise now to better use Pylit
    ](http://slott-softwarearchitect.blogspot.fr/2013/10/literate-programming-and-pylit.html)
-   [Pweave](http://mpastell.com/pweave/)
    Pweave is a scientific report generator and a literate programming tool for Python
    developed after Sweave. Pweave can capture the results and plots
    from data analysis and works well with numpy, scipy and matplotlib.
    Pweave uses [noweb](#noweb) syntax, but it is also weave a python code between
    `<<>>=` and `@` blocks and include the results and capture matplotlib
    plots in the document. Pweave supports reST, Sphinx, Latex,
    and Pandoc markdown markups. <br />
    For a quick overview look at the
    [example from the documentation](http://mpastell.com/pweave/examples.html).
-   [w:Sweave] is a function in  R that enables integration of R code into LaTeX.
-   [org-babel](/node/404#babel "internal link") is a literate programming extension for
    [Org mode](/node/404 "internal link").

#  Source code beautifiers {#code_beautifiers}
-   [Wikipedia: Prettyprint](http://en.wikipedia.org/wiki/Pretty-printing)
    review code beautifiers.
-   [code-prettify](https://github.com/google/code-prettify)
    (Apache License) is  a Javascript module and CSS file that allows syntax
    highlighting of source code snippets in an html page.
    It works on a number of languages including C and friends, Java,
    Python, Bash, SQL, HTML, XML, CSS, Javascript, Makefiles, and
    Rust. Other languages are supported via extensions.
-   [Doxygen](http://www.stack.nl/~dimitri/doxygen) is a documentation
    system for C++, C, Java, Objective-C, Python, IDL.
    [Doxymacs](http://doxymacs.sourceforge.net/) make using Doxygen
    from within {X}Emacs easier _not updated since 2010_.
-   [highlight](http://www.andre-simon.de/doku/highlight/en/highlight.php)
    from André Simon is a C++ program _not to be confused with the
    javascript Highlight.js below_. It can prettify
    any language (120 programming languages) and output HTML, XHTMML,
    ansi, XSL-FO, RTF or latex.
-   [Highlight.js ](https://highlightjs.org/)
    <a name="highlight_js"></a>(BSD License)
    is a syntax highlighter written in JavaScript.
    It works in the browser as well as on the server. It works with
    [many markups
    ](http://highlightjs.readthedocs.org/en/latest/css-classes-reference.html),
    and has automatic language detection.
    -   [Highlight.js Demo](https://highlightjs.org/static/demo/).
    -   [Documentation for the API and other topics
        ](http://highlightjs.readthedocs.org/).
    -   [Highlight.js GitHub Repository
        ](https://github.com/isagalaev/highlight.js).
-   [GNU indent](http://www.gnu.org/software/indent/manual/indent.html) (GPL)
    changes the appearance of a C program by inserting or deleting whitespace,
    It can also convert from one style of writing C to another.
-   [Pygments](http://pygments.org/) <a name="pygments"></a>
    is a generic syntax highlighter. It supports a
    [wide range of common languages and markup formats](http://pygments.org/languages/)
    and can output to HTML, RTF, LaTeX and ANSI sequences.
    It has a [Command Line Interface](http://pygments.org/docs/cmdline/)
    and is often used by [Structured Text Formatters](/node/269 "Internal reference")
    like Rest, Sphinx, Markdown, MoinMoin... or webframeworks like Wordpress, Hyde ....
-   [Ostermiller syntax package](http://ostermiller.org/syntax/features.html)(GPL)
    is a java program that add syntax coloring to web pages for source
    code of C/C++, Java, HTML.
-   [GNU Source-highlight](http://www.gnu.org/software/src-highlite/)
    (GPL) is a C++ program wich uses boost library regular expression
    handling to highlight programming languages source code. Gnu
    highlight can handle: C/C++, C#, Bib, Bison, Caml, Changelog, Diff,
    Flex, Fortran, Html, Java, Javascript, Latex, Logtalk, Log files,
    Lua, ML, Pascal, Perl, PHP, Postscript, Prolog, Python, Ruby,
    Shell, Sql, Tcl, XML. It can output, HTML, XHTML, LATEX, TEXINFO,
    ANSI color escape sequences, DocBook.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
