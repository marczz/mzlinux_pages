---
title: Source Code
---

# Literate Programming {#literate_programming}

This section is about literate programming and source code
documentation, if you extract both the code and documentation from the
same piece of text, you do
literate programming. If you extract your doc from your program,
you are doing source code documentation. But there is no crisp barrier
between the two concepts.

The two main components in traditional literate programming languages
like {{< wp "WEB" >}} or {{< wp "CWEB" >}} are *tangle*, which produces compilable code
from the source texts, and *weave*, which produces nicely-formatted
documentation.

There is a related
{{< iref "#code_beautifiers" "section on source code beautifiers" >}}.

-   Wikipedia: {{< wp "Literate_programming"  "Literate programming" >}},
    {{< wp "Comparison of documentation generators" >}}
-
-   [SGML/XML and Literate Programming](http://www.oasis-open.org/cover/xmlLitProg.html)
-   [www.literateprogramming.com](http://www.literateprogramming.com/)
    is an _outdated_ index of literate programming links and book reviews.
-   [antiweb](http://packages.python.org/antiweb/) (GPL)
    <a name="antiweb"></a>
    ([Pypi entry](ihttp://pypi.python.org/pypi/antiweb/))
    is an inverse literate programming tool in the {{< iref "#noweb" "noweb" >}} family..
    In opposite to _web_ the documentation is weaved from syntactic correct source code.
    The result is a restructed text file, that can be used in the
    {{< iref "rest#sphinx" "sphinx document generator" >}}.
-   <a name="cog"></a> [Cog](http://nedbatchelder.com/code/cog/) (MIT license.)
    is a code generation tool. It is a preprocessor with all power of python. While
    __Cog__ is mainly aimed at _tangling_ a source file with included python chunks, it
    can be also combined with {{< iref "rest#sphinx" "Sphinx" >}} for documentation
    generation as described in
    [Documentation for python code with reST, docutils, cog and paver
    ](http://oneau.wordpress.com/2010/05/24/documenting-python-code-with-rest-docutils-pygments-cog-and-paver/)
    _2010_.
-   [Docco](http://jashkenas.github.io/docco/) is a documentation
    generator, written in Literate CoffeeScript. It produces an HTML
    document that displays your comments written in Markdown intermingled with
    your code with syntax highlighting with
    {{< iref "#highlight_js" "Highlight.js" >}}.

    __Doco__ has many ports to various langages like
    [Rocco](http://rtomayko.github.io/rocco/rocco.html) in Ruby,
    [Shocco](http://rtomayko.github.io/shocco/) for Shell,
    [Pycco](https://github.com/pycco-docs/pycco) in Python,
    [Marginalia](http://fogus.me/fun/marginalia/) in Clojure,
    [Gocco](http://nikhilm.github.io/gocco/) in Go,
    [sourceMakeup](http://jquery-jkit.com/sourcemakeup/) in PHP,
    [Locco](http://rgieseke.github.io/locco/) in Lua,
    [Nocco](http://dontangg.github.io/nocco/) in .NET,
    [Groc](http://nevir.github.io/groc/) is a **CoffeeScript** fork with supplementary
    features.
-   [Doxygen](http://www.stack.nl/~dimitri/doxygen) is a documentation
    system for C++, C, Java, Objective-C, Python, IDL.
    [Doxymacs](http://doxymacs.sourceforge.net/) make using Doxygen
    from within {X}Emacs easier. _not updated since 2010_.
-   [FunnelWeb](http://www.ross.net/funnelweb/) a language independant
    literate programming tool which use a common source file to *tangle*
    a program and weave a latex or html documentation. .
-   {{< iref "programming_languages#haskell" "Haskell" >}}
    has semi literate programming support.  It can extract the source code from a
    _LaTeX_ source.
-   The {{< wp "Leo_(text_editor)" "Leo text editor" >}} is an outlining editor which
    supports optional noweb and CWEB markup.
-   {{< wp "noweb" >}}<a name="noweb"></a> is a literate programming tool, created in
    1989 by Norman Ramsey. It has *tangle* and *weave* components as do {{< wp "WEB" >}}
    or {{< wp "CWEB" >}} but is independent of the code language.
    -   [noweb Home](http://www.cs.tufts.edu/~nr/noweb/).
    -   Noweb has a python clone
        [noweb.py](https://github.com/JonathanAquino/noweb.py)
        that uses the  noweb syntax.
-   [Natural Docs](https://www.naturaldocs.org/) (AGPL)
    is a code documentation  supporting numerous languages. It was first written in
    Perl; then in .NET _or Mono for linux_.
-   [Pnw](https://pypi.python.org/pypi/pnw/) (Apache license)
     is a text processing and literate programming tool inspired by
    {{< iref "#antiweb" "antiweb" >}} and {{< iref "#noweb" "noweb" >}}.
-   [PyLit](https://pypi.python.org/pypi/pylit) (GPL) is a python tool that feature a
    _bidirectional text/code converter_; it can convert between the _code_ form
    and the _text_ form  the _code_  without loss of information.
    [PyLit3](https://github.com/slott56/PyLit-3) (GPL) is a fork for Python3 by Steven
    Lott, which [replace PyWeb
    ]((http://slott-softwarearchitect.blogspot.fr/2013/10/literate-programming-and-pylit.html)
    previously developped by  Steven Lott.
-   [pyreport](http://gael-varoquaux.info/computers/pyreport/) (BSD-like license)
    runs a python script and captures its output, compiling it to a
    report in a pdf or an html file.
-   [Pweave](http://mpastell.com/pweave/)
    Pweave is a scientific report generator and a literate programming tool for Python
    developed after Sweave. Pweave can capture the results and plots
    from data analysis and works well with numpy, scipy and matplotlib.
    Pweave uses {{< iref "#noweb" "noweb" >}} syntax, but it is also weave a python code between
    `<<>>=` and `@` blocks and include the results and capture matplotlib
    plots in the document. Pweave supports reST, Sphinx, Latex,
    and Pandoc markdown markups. <br />
    For a quick overview look at the
    [example from the documentation](http://mpastell.com/pweave/examples.html).
-   {{< wp "ROBODoc" >}} (GPL)
    is a documentation generator for with C, C++, Fortran, Perl, shell scripts,
    Assembler, DCL, DB/C, Tcl/Tk, Forth, Lisp, COBOL, Occam, Basic, HTML, Clarion, and
    any other language that supports comments. It is an old software, main part of the
    code from 2010 and last release 2015, it is no longer packaged with Debian. You can
    compile from source, there is also a Docker image.
    -   [ROBODoc Home](https://rfsber.home.xs4all.nl/Robo/)
-   {{< wp "Sweave" >}} is a function in  R that enables integration of R code into LaTeX.
-   {{< iref "org-mode#babel" "org-babel" >}} is a literate programming extension for
    {{< iref "org-mode" "Org mode" >}}.
-   [Literate](https://github.com/zyedidia/Literate) (MIT License)
    is a langage agnostic Markdown based literate programming tool writen in D language.
-   [mdsh](https://github.com/bashup/mdsh)
    is a bash script compiler and interpreter for markdown files. It can make markdown
    files executable, or generate bash scripts from markdown files.
-   [zshelldoc](https://github.com/zdharma/zshelldoc) (MIT and GPL)
    is a documentation generator written in zsh for Bash & Zsh, with call-trees, comment
    extraction, etc.
    It generates asciidoc documentation.
-   [shelldoc](https://github.com/charlesdaniels/shelldoc)
    A tool for generating ReST documentation from shell scripts

#  Source code beautifiers {#code_beautifiers}
_There are two different operations that might be used to prettify source code,
re-formatting, and higlighting._

-   [Wikipedia: Prettyprint](http://en.wikipedia.org/wiki/Pretty-printing)
    review code beautifiers.
-   [bat and other highlighting software feature comparison
    ](https://github.com/sharkdp/bat/blob/master/doc/alternatives.md).

-   <a name="bat"</a>[Bat](https://github.com/sharkdp/bat) (MIT/Apache License)
    is a  cat(1) clone with syntax highlighting and Git integration.
    It uses the {{ "#syntect" "Syntect" >}} library to hightlight code; and integrates
    with unix utilities like `find` or `fd`, `ripgrep`, `git --show`. _Bat is in
    Debian._

    The original bat theme is for Dark bckground console, but you can use:
    ~~~
    $ bat --themes
    ~~~
    to show all the themes with an example of code coloring.
    For light backgroundyou can choose `GitHub`, `Monokai Extended Light`,
    `OneHalfLight`, `Solarized (light)` (and also `Solarized (dark)`!), `ansi-light`,

    -   [bat-extras)(https://github.com/eth-p/bat-extras) (MIT Licence)
        are utlities to use unix commands with _bat_ output. It includes
        _batman_, _batgrep_, _batdiff_, _batwatch_, _prettybat_.
-   <a name="chroma"></a>[Chroma](https://github.com/alecthomas/chroma) (MIT License)
    is a general purpose syntax highlighter in pure Go based heavily on
    {{< iref "#pygments" "Pygments" >}}.
    _Chroma_ includes translators for Pygments lexers and styles.
    _Chroma_ formatters can output HTML, as well as terminal output in 8/256/true
    colour. Chroma has also a command line client.

    _Chroma_ can be used with the {{< iref "markdown#goldmark" "Goldmark" >}}
    Markdown renderer using the
    [syntax-highlighting for fenced code blocks extension
    ](https://github.com/yuin/goldmark-highlighting).
    The static site generator {{< iref "static_sites#hugo" "Hugo" >}} uses
    [chroma for syntax highlighting
    ](https://gohugo.io/content-management/syntax-highlighting/).

-   [code-prettify](https://github.com/google/code-prettify) (Apache License)
    is a Javascript module and CSS file that allows syntax highlighting of source code
    snippets in an html page.  It works on a number of languages including C and
    friends, Java, Python, Bash, SQL, HTML, XML, CSS, Javascript, Makefiles, and
    Rust. Other languages are supported via extensions.
-   [highlight](http://www.andre-simon.de/doku/highlight/en/highlight.php) (GPL)
    from André Simon is a C++ program _not to be confused with the javascript
    Highlight.js below_. It can prettify a [huge number of languages
    ](https://gitlab.com/saalen/highlight/-/wikis/Languages-List) (120 programming
    languages) and output HTML, XHTML, RTF, LaTeX, TeX, SVG, BBCode and ANSI terminal
    escape sequences. It can also [Integrate in Pandoc
    ](https://gitlab.com/saalen/highlight/-/wikis/Pandoc-Integration).
    -   [highlight - GitLab](https://gitlab.com/saalen/highlight)
    -   [highlight Wiki][https://gitlab.com/saalen/highlight/-/wikis)
-   <a name="highlight_js"></a>[Highlight.js ](https://highlightjs.org/) (BSD License)
    is a syntax highlighter written in JavaScript.  It works in the browser as well as
    on the server. It works with [many markups languages
    ](https://github.com/highlightjs/highlight.js/blob/master/SUPPORTED_LANGUAGES.md),
    and has automatic language detection.
    -   [Highlight.js Demo](https://highlightjs.org/static/demo/).
    -   [Documentation for the API and other topics
        ](http://highlightjs.readthedocs.org/).
    -   [Highlight.js GitHub Repository
        ](https://github.com/isagalaev/highlight.js).
    -   [hicat](https://github.com/rstacruz/hicat) (MIT License)
         a CLI to `cat` with highlight.js syntax highlighting.
-   [GNU indent](http://www.gnu.org/software/indent/manual/indent.html) (GPL)
    changes the appearance of a C program by inserting or deleting whitespace,
    It can also convert from one style of writing C to another.
-   <a name="pygments"></a>[Pygments](http://pygments.org/) (BSD-2-Clause License)
    is a generic syntax highlighter. It supports a
    [wide range of common languages and markup formats](http://pygments.org/languages/)
    and can output to HTML, RTF, LaTeX and ANSI sequences.
    It has a [Command Line Interface](http://pygments.org/docs/cmdline/)
    and is often used by {{< iref "structured_text" "Structured Text Formatters" >}}
    like Rest, Sphinx, Markdown, MoinMoin... or webframeworks like Wordpress, Hyde ....

    [pygmentize](https://pygments.org/docs/cmdline/) is the command line interface to
    pygments.

-   [Ostermiller syntax package](http://ostermiller.org/syntax/features.html) (GPL)
    is a java program that add syntax coloring to web pages for source code of C/C++,
    Java, HTML.
-   <a name="prettier">[Prettier](https://prettier.io/) (MIT License)
    is a node.js code formatter with support for:
    JavaScript, JSX, Angular, Vue, Flow, TypeScript, CSS, Less, and SCSS, HTML, JSON,
    GraphQL, Markdown _including GFM and MDX_, YAML.
    It removes all original styling* and ensures that all outputted code conforms to a
    consistent style. It disregards the original styling* by parsing it away and
    re-printing the parsed AST with its own rules that take the maximum line length into
    account, wrapping code when necessary.

    [Prettier integrates with many editors](https://prettier.io/docs/en/editors.html)
    including _emacs_ and _vim_.

    You may need to [ignore some files or some section of your code
    ](https://prettier.io/docs/en/ignore.html)
    -   [Prettier - GitHub](https://github.com/prettier/prettier).
    -   [prettierx](https://github.com/brodybits/prettierx) (MIT License)
        is a less opinionated code formatter fork of prettier.
-   [GNU Source-highlight](http://www.gnu.org/software/src-highlite/) (GPL)
    (GPL) is a C++ program wich uses boost library regular expression
    handling to highlight programming languages source code. Gnu
    highlight can handle: C/C++, C#, Bib, Bison, Caml, Changelog, Diff,
    Flex, Fortran, Html, Java, Javascript, Latex, Logtalk, Log files,
    Lua, ML, Pascal, Perl, PHP, Postscript, Prolog, Python, Ruby,
    Shell, Sql, Tcl, XML. It can output, HTML, XHTML, LATEX, TEXINFO,
    ANSI color escape sequences, DocBook.
-   <a name="synctect"></a>[Synctect](https://github.com/trishume/syntect) (MIT License)
    is a syntax highlighting library for Rust that uses
    [Sublime Text syntax definitions](http://www.sublimetext.com/docs/3/syntax.html).
    It is used by [many rust open source projects
    ](https://github.com/trishume/syntect#projects-using-syntect) including
    {{< iref "#bat"  "bat" >}}, and _crowdown_,
    {{< iref "git#delta" "Delta diff viewer" >}}.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
