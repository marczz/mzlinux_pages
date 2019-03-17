<!--
.. description:
.. date: 2018-02-16
.. slug: manpages
.. tags:
.. link:
.. book: mzlinux
.. title: Man Pages
-->

# Man pages format

-   [w:Man page] are written using [w:Troff] and [w:Troff macros]
    or the Gnu [w:Groff_(software)|Groff] with macro packages.
    Groff is used in Linux and FreeBSD, and OpenBSD replaced groff
    with [w:mandoc].
-   [Linux Man Page Howto
    ](http://www.tldp.org/HOWTO/Man-Page/index.html) an old HOWTO
    _2002_, but still usefull, as man page format is very stable.
    The section [How should a formatted man page look?
    ](http://www.tldp.org/HOWTO/Man-Page/q3.html)
    is a good basic example of man page.
-   [troff.org](http://www.troff.org/)
-   [Gnu Groff](https://www.gnu.org/software/groff/groff.html)
    is the gnu implementation of troff. [man:groff|groff(1) man page].
-   [Richard Stevens](http://www.kohala.com/start/)' [Troff Resources
    ](http://www.kohala.com/start/troff/troff.html).
-   [mandoc](https://mdocml.bsd.lv/) (BSD License)
    is the BSD manpage compiler toolset for *mdoc*, the BSD roff macro
    language for BSD manual pages, and *man*, the language for UNIX
    manuals. *mandoc* since march 2017 includes a new formatter
    `-mdoc -Tmarkdown` which output markdown. This formatter work only
    with *mdoc* input and not with *man* input.
-   [Guide for writing UNIX manuals in the mdoc language
    ](http://manpages.bsd.lv/mdoc.html)
-   Manual pages [man:man],
    [mdoc(7)](https://mdocml.bsd.lv/man/mdoc.7.html),
    [mdoc extended documentation](https://mdocml.bsd.lv/mdoc/),
    [mandoc(1)](http://man.openbsd.org/mandoc.1)
-   [WritingManPages - HerzbubeWiki
    ](https://wiki.herzbube.ch/index.php/WritingManPages)
-   [PolyglotMan i.e. rman](http://polyglotman.sourceforge.net/)
    PolyglotMan is a *reverse man*. It takes man pages sources in
    [tn]roff source and produce  ASCII, section
    headers-only, HTML, LaTeX2e, RTF, Perl 5 POD. It is in Debian.
    *See also above [mandoc](#mandoc "internal reference")
    which can output markdown from mdoc.*
    -   [rman manual](http://polyglotman.sourceforge.net/rman.html)
-   [debiman](https://github.com/Debian/debiman)
    generates a static manpage HTML repository out of a Debian archive
-   [doclifter](https://gitlab.com/esr/doclifter) (BSD license)
    translates documents written in troff macros to DocBook, it
    support *man*, *mdoc* and *troff*.  The
    script *manlifter* convert an entire manual-page tree to
    XML-Docbook.
    While the docbook output workd well with xml tools, the use of
    generated docbook with *pandoc* to convert a man page to
    restructured text, has not the expected result.
    -   [doclifter manual
        ](http://www.catb.org/~esr/doclifter/doclifter.html)
    -   [manlifter manual
        ](http://www.catb.org/~esr/doclifter/manlifter.html)
-   [man-to-md](https://github.com/mle86/man-to-md/)
    convert nroff files to markdown but even if it works on samples
    from test/samples/ directory, when trying to convert any standard
    man page from my linux system (like man.1 or ls.1) give an error.
-   Free desktop has a [Help Specification
    ](https://www.freedesktop.org/wiki/Specifications/help-spec/).
-   [Gnome help system
    ](https://help.gnome.org/admin/system-admin-guide/2.32/help-1.html.en)
    uses [Yelp](https://wiki.gnome.org/Apps/Yelp) with
    [w:docbook] or [w:Mallard_(documentation)|Mallard].
-   QT use [QT Help](http://doc.qt.io/qt-4.8/qthelp-framework.html).


# The standard sections of man pages
Taken from the  [Guide for writing UNIX manuals in the mdoc language
    ](http://manpages.bsd.lv/mdoc.html)
where you can find more explanations.

NAME
:   Name of all documented components and a collective description.

SYNOPSIS
:   Calling syntax of the components.

    A few conventions are used, particularly in the Commands
    section. Underlined words are considered literals. Square brackets
    ([]) around an argument indicate that the argument is optional. An
    argument given as name refers to a file name. Ellipses ... are
    used to show that the previous argument-prototype may be repeated.
    An argument beginning with a minus sign - is often taken to mean
    some sort of flag argument even if it appears in a position where
    a file name could appear.

DESCRIPTION
:   Description of all components. This constitutes the bulk of the
    manual.

IMPLEMENTATION NOTES
:   Specific notes on the implementation of a generic (e.g.,
    standardised) component.

RETURN VALUES
:   Return values, if the components are functions.

ENVIRONMENT
:   Environmental variables affecting the components' operation.

FILES
:   Files affecting the components' operation.

EXIT STATUS
:   Exit status, if the components are commands.

EXAMPLES
:   Brief examples of invocation.

DIAGNOSIS
:   Error conditions, if a command or device driver.

ERRORS
:   Error conditions, if a function or library.

SEE ALSO
:   Links to other relevant manuals or references.

STANDARDS
:   Implemented or referenced standards.

HISTORY
:   A brief history of the components.

AUTHORS
:   The authors of the components.

CAVEATS
:   Caveats regarding the components' operation.

BUGS
:   Known bugs in the components.

SECURITY CONSIDERATIONS
:   Security precautions beyond the scope of the components.

Only the NAME and DESCRIPTION sections are required in the document
body, although a SYNOPSIS should appear for most manuals as well.

Other sections may be necessary depending on the category. For
example, RETURN VALUES is found for most category 3 and 2 manuals;
while EXIT STATUS is found for most category 1, 6, and 8 manuals.

The sections are:

1.	General commands
2.	System calls
3.	Library functions
4.	Special files (usually devices, those found in /dev) and drivers
5.	File formats and conventions
6.	Games and screensavers
7.	Miscellanea
8.	System administration commands and daemons



# Generate Man Pages from structured text
-   [Latex2man
    ](http://ctan.tug.org/tex-archive/support/latex2man/latex2man.html)
    is a tool to translate UNIX manual pages written with
    LaTeX into man pages.
-   [pod2man](http://perldoc.perl.org/pod2man.html)
    generate *roff* input from POD source.
-   DocBook XML can be processed to man pages with an xml
    processor. We can use the *xmlto* front-end. See the
    [Xml Section](/node/data_exchange#xml "internal reference").


## Markdown
-   [lowdown](/node/markdown#lowdown "internal reference")
    ISC Licence) is a C markdown processor that process markdown to
    troff.
-   [go-md2man](https://github.com/cpuguy83/go-md2man)
    is a go language using *blackfriday* to process markdown into
    man pages. It is in Debian.
-   [lunamark](/node/markdown#lunamark) is a lua converter to many
    formats including groff.
-   [marked-man](https://github.com/kapouer/ronnjs) (BSD License)
    uses the javascript converter
    [marked](/node/markdown#marked "internal reference")
    to convert markdown to roff.
    The Debian package is *node-marked-man*.
-   [pandoc](/node/markdown#pandoc "internal reference") allow to
    convert fromall the input formats (Markdown, CommonMark, Textile,
    reStructuredText, HTML, (subset of) LaTeX, MediaWiki, TWiki,
    Haddock, OPML, Org-mode, DocBook, txt2tags, Word docx) to troff
    man format.
-   [remark-man](https://github.com/remarkjs/remark-man)
    compile markdown to man using the javascript translator
    [remark](/node/markdown#remark  "internal reference").
-   [Ronn](https://github.com/rtomayko/ronn) (MIT License)
    is a ruby application that uses a markdown and
    [additional man pages constructs
    ](http://rtomayko.github.io/ronn/ronn-format.7.html)
    to generate man pages and html.


## ReST
See also the [ReST page](/node/rest "internal reference")

-   [rst2man
    ](http://docutils.sourceforge.net/sandbox/manpage-writer/rst2man.txt)
    is the standard [ReST tool
    ](ttp://svn.berlios.de/viewvc/docutils/trunk/docutils/tools/)
    to produce manpages.
-   [Sphinx](/node/rest#sphinx "internal reference")
    has a manual page builder.

## Asciidoc
See also the [Asciidoc page](/node/asciidoc "internal reference")

[Asciidoc](/node/asciidoc "internal reference")
can generate man pages, there are
[examples](http://www.methods.co.nz/asciidoc/#_overview_and_examples)
in the documentation. The [asciidoc(1) manual page
](http://www.methods.co.nz/asciidoc/manpage.html)
is itself produced from an
[asciidoc source](http://www.methods.co.nz/asciidoc/manpage.txt).

All the Git manuals are written in asciidoc. You can see the source in
the [git Repository
](https://git.kernel.org/pub/scm/git/git.git/tree/Documentation?id=HEAD).

## Other formats
-   [help2man](https://www.gnu.org/software/help2man/)
    produces simple manual pages from the ‘--help’ and ‘--version’
    output of a command.

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
