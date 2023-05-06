---
title: Man Pages
---

<!--

-->

# Man pages format

-   {{< wp "Man page" >}} are written using {{< wp "Troff" >}} and {{< wp "Troff macros" >}}
    or the Gnu {{< wp "Groff_(software)" "Groff" >}} with macro packages.  Groff is used
    in Linux and FreeBSD, and OpenBSD replaced groff with {{< wp "mandoc" >}}.
-   [Linux Man Page Howto
    ](http://www.tldp.org/HOWTO/Man-Page/index.html) an old HOWTO
    _2002_, but still usefull, as man page format is very stable.
    The section [How should a formatted man page look?
    ](http://www.tldp.org/HOWTO/Man-Page/q3.html)
    is a good basic example of man page.
-   [troff.org](http://www.troff.org/)
-   [Gnu Groff](https://www.gnu.org/software/groff/groff.html)
    is the gnu implementation of troff. {{< man "groff"  "groff(1) man page" >}}.
-   [Richard Stevens](http://www.kohala.com/start/):
    [Troff Resources](http://www.kohala.com/start/troff/troff.html)..
-   [mandoc](https://mdocml.bsd.lv/) (BSD License)
    is the BSD manpage compiler toolset for *mdoc*, the BSD roff macro language for BSD
    manual pages, and *man*, the language for UNIX manuals. *mandoc* since march 2017
    includes a new formatter `-mdoc -Tmarkdown` which output markdown. This formatter
    work only with *mdoc* input and not with *man* input.
-   [Guide for writing UNIX manuals in the mdoc language
    ](http://manpages.bsd.lv/mdoc.html)
-   Manual pages {{< man "man" >}},
    [mdoc(7)](https://mdocml.bsd.lv/man/mdoc.7.html),
    [mdoc extended documentation](https://mdocml.bsd.lv/mdoc/),
    [mandoc(1)](http://man.openbsd.org/mandoc.1)
-   [WritingManPages - HerzbubeWiki
    ](https://wiki.herzbube.ch/index.php/WritingManPages)
-   [PolyglotMan i.e. rman](http://polyglotman.sourceforge.net/)
    PolyglotMan is a *reverse man*. It takes man pages sources in [tn]roff source and
    produce ASCII, section headers-only, HTML, LaTeX2e, RTF, Perl 5 POD. It is in
    Debian.

    *See also above {{< iref "#mandoc" "mandoc" >}} which can output markdown from
    mdoc.*
    -   [rman manual](http://polyglotman.sourceforge.net/rman.html)
-   [debiman](https://github.com/Debian/debiman)
    generates a static manpage HTML repository out of a Debian archive
-   [doclifter](https://gitlab.com/esr/doclifter) (BSD license)
    translates documents written in troff macros to DocBook, it support *man*, *mdoc*
    and *troff*.  The script *manlifter* convert an entire manual-page tree to
    XML-Docbook.  While the docbook output workd well with xml tools, the use of
    generated docbook with *pandoc* to convert a man page to restructured text, has not
    the expected result.
    -   [doclifter manual
        ](http://www.catb.org/~esr/doclifter/doclifter.html)
    -   [manlifter manual
        ](http://www.catb.org/~esr/doclifter/manlifter.html)
-   [man-to-md](https://github.com/mle86/man-to-md/)
    convert nroff files to markdown but even if it works on samples from test/samples/
    directory, when trying to convert any standard man page from my linux system (like
    man.1 or ls.1) give an error.
-   Free desktop has a [Help Specification
    ](https://www.freedesktop.org/wiki/Specifications/help-spec/).
-   [Gnome help system
    ](https://help.gnome.org/admin/system-admin-guide/2.32/help-1.html.en)
    uses [Yelp](https://wiki.gnome.org/Apps/Yelp) with
    {{< wp "docbook" >}} or {{< wp "Mallard_(documentation)"  "Mallard" >}}.
-   QT use [QT Help](http://doc.qt.io/qt-4.8/qthelp-framework.html).


# The standard sections of man pages
Taken from the  [Guide for writing UNIX manuals in the mdoc language
    ](http://manpages.bsd.lv/mdoc.html)
where you can find more explanations.

NAME
:   Name of all documented components and a collective description.

SYNOPSIS
:   Calling syntax of the components.

    A few conventions are used, particularly in the Commands section. Underlined words
    are considered literals. Square brackets ([]) around an argument indicate that the
    argument is optional. An argument given as name refers to a file name. Ellipses
    ... are used to show that the previous argument-prototype may be repeated.  An
    argument beginning with a minus sign - is often taken to mean some sort of flag
    argument even if it appears in a position where a file name could appear.

DESCRIPTION
:   Description of all components. This constitutes the bulk of the manual.

IMPLEMENTATION NOTES
:   Specific notes on the implementation of a generic (e.g., standardised) component.

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
:w
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

Only the NAME and DESCRIPTION sections are required in the document body, although a
SYNOPSIS should appear for most manuals as well.

Other sections may be necessary depending on the category. For example, RETURN VALUES is
found for most category 3 and 2 manuals; while EXIT STATUS is found for most category 1,
6, and 8 manuals.

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
    is a tool to translate UNIX manual pages written with LaTeX into man pages.
-   [pod2man](http://perldoc.perl.org/pod2man.html)
    generate *roff* input from POD source.
-   DocBook XML can be processed to man pages with an xml processor. We can use the
    *xmlto* front-end. See the {{< iref "data_exchange#xml" "Xml Section" >}}.


## Markdown {#man_from_markdown}
-   {{< iref "markdown#lowdown" "lowdown" >}}
    ISC Licence) is a C markdown processor that process markdown to troff.
-   [go-md2man](https://github.com/cpuguy83/go-md2man)
    is a go language using *blackfriday* to process markdown into man pages. It is in
    Debian.
-   {{< iref "markdown#lunamark" "lunamark" >}} is a lua converter to many
    formats including groff.
-   [marked-man](https://github.com/kapouer/ronnjs) (BSD License)
    uses the javascript converter {{< iref "markdown#marked" "marked" >}}
    to convert markdown to roff.
    The Debian package is *node-marked-man*.
-   {{< iref "markdown#pandoc" "pandoc" >}} allow to convert fromall the input formats
    (Markdown, CommonMark, Textile, reStructuredText, HTML, (subset of) LaTeX,
    MediaWiki, TWiki, Haddock, OPML, Org-mode, DocBook, txt2tags, Word docx) to troff
    man format.
    -   [Write Your Own Man Pages | g.p. Anders
        ](https://gpanders.com/blog/write-your-own-man-pages/)
        uses pandoc in a script.
-   [remark-man](https://github.com/remarkjs/remark-man)
    compile markdown to man using the javascript translator
    {{< iref "markdown#remark" "remark" >}}.
-   [ronn](https://github.com/apjanke/ronn-ng) (MIT License)
    is a ruby application to build a man page from markdown source.

    The accepted syntax is defined in [ronn-format(7)
    ](https://manpages.debian.org/unstable/ruby-ronn/ronn-format.7.en.html)
    it includes basic markdown, a non standard variant of definition list, but
    no table. The _ronn-format_  manpage also give a last of commonly used sections
    in man pages.
-   [Ronn](https://github.com/rtomayko/ronn) (MIT License)
    is a ruby application that uses a markdown and
    [additional man pages constructs](http://rtomayko.github.io/ronn/ronn-format.7.html)
    to generate man pages and html.


## ReST
See also the {{< iref "rest" "ReST page" >}}

-   [rst2man](http://docutils.sourceforge.net/sandbox/manpage-writer/rst2man.txt)
    is the standard [ReST tool](https://docutils.sourceforge.io/docs/user/tools.htm)
    to produce manpages.
-   {{< iref "rest#sphinx" "Sphinx" >}}
    has a manual page builder.

## Asciidoc
See also the {{< iref "asciidoc" "Asciidoc page" >}}

{{< iref "asciidoc" "Asciidoc" >}}
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

# Linux man pages
-   [GitHub - mkerrisk/man-pages](https://github.com/mkerrisk/man-pages),
    source of all linux man pages.
-   [Debian Manpages](https://manpages.debian.org/) processed by
    [DebiMan](https://github.com/Debian/debiman/).

# Cheat sheets

-   [awesome cheatsheet](https://github.com/detailyang/awesome-cheatsheetp)
    list of cheatsheet resources.
-   [Github topic cheatsheet](https://github.com/topics/cheatsheets)
-   <a name="tdlr"></a>The [TLDR pages](https://tldr.sh/) are a community effort to
    simplify the man pages with practical examples.
    -   [GitHub - tldr-pages/tldr](https://github.com/tldr-pages/tldr).
    -   There are [many clients](https://github.com/tldr-pages/tldr/wiki/TLDR-clients)
        in numerous programming languages, mainly console clients, but also web clients,
        and android and ios clients.
-   [bro pages](http://bropages.org/) is a web site with community driven
    concise examples for command line programs. There is a ruby CLI
    [bro](https://github.com/hubsmoke/bro).
-   [GitHub - chubin/cheat.sh](https://github.com/chubin/cheat.sh) (MIT License)
    is a repository of cheat sheets that can be queried on the command line with curl or
    with a provided client. It covers 56 programming languages, several DBMSes, and more
    than 1000 most important UNIX/Linux commands. It has integration [with emacs
    ](https://github.com/chubin/cheat.sh#emacs) and [within vim
    ](https://github.com/chubin/cheat.sh#vim).

    In addition of its own [cheatsheets repository
    ](https://github.com/chubin/cheat.sheets)
    it can access many big style sheet repositories like {{< iref "#tdlr" "TDLR" >}},
    {{< iref "#chrisallenlane_cheat" "Chris Allen Lane cheat" >}},
    {{< iref "#learnxinyminutes" "learnxinyminutes" >}} and  stackoverflow.
    -   [cheat.sh web interface](https://cheat.sh/)
    -   [cheat.sh command line client](https://github.com/chubin/cheat.sh#installation)
    -   Use with curl without installing a client:
        ``` console
        curl cheat.sh/tar
        curl cht.sh/curl
        curl https://cheat.sh/rsync
        curl https://cht.sh/tr
        ```
    -   [Rico Sta. Cruz](https://github.com/rstacruz) has written
    more than 380 cheat sheets that you can find on [devhints.io](https://devhints.io/).

    They are written in markdown, with a
    [complex css style](https://devhints.io/cheatsheet-styles) used in his
    [sheet publishing system
    ](https://github.com/rstacruz/cheatsheets/blob/master/CONTRIBUTING.md)

    The [source is on GitHub](https://github.com/rstacruz/cheatsheets).
-   [DennyZhang CheatSheets
    ](https://github.com/dennyzhang/cheatsheet.dennyzhang.com)
    is a collection of Cheat sheets. They are written in org with export to PDF.
    Some are very rudimentary, and don't give much information, other more complete.
-    <a name="learnxinyminutes">[learnxinyminutes-docs
    ](https://github.com/adambard/learnxinyminutes-docs)
    _Learn X in Y minutes_ are codes examples for numerous languages.
-   [Commande line Fu API](https://www.commandlinefu.com/site/api)
    allow to download the text of the command pages.
-   [Dan’s Cheat Sheets](https://cheat.readthedocs.io/en/latest/index.html)
    is a collection of Cheatsheets published as a Sphinx document from Dan Poirier.
    the RST source is in [poirier/cheat](https://github.com/poirier/cheat) GitHub
    repository.
-   [Lecoupa/awesome cheatsheets](https://github.com/LeCoupa/awesome-cheatsheets)
    _not an awesome list_ but a repository of cheatsheets for popular programming
    languages, frameworks and development tools.

## CheatSheet software
-   [alhassy/CheatSheet](https://github.com/alhassy/CheatSheet)
    is an org mode library for creating cheat sheets in pdf, they can be multicolumn.
    They support source code colouring, equational support, unicode characters support.
-   [pbellon/cheat](https://github.com/pbellon/cheat) (GPL)
    is an Emacs package to register and open cheatsheets.
-   <a name="chrisallenlane_cheat">[GitHub - cheat/cheat](https://github.com/cheat/cheat)
    by Chris Allen Lane is a go program _which was previously written in python_ to
    create and view interactive cheatsheets on the command-line.
    -   [communauty cheatsheets](https://github.com/cheat/cheatsheets)
    -   [Related Projects](https://github.com/cheat/cheat/wiki/Related-Projects)
    -   implementatations in other languages:
        [lucaswerkmeister/cheats](https://github.com/lucaswerkmeister/cheats) and
        [jahendrie/cheat](https://github.com/jahendrie/cheat) in bash,
        [weakish/cheat](https://github.com/weakish/cheat) in sh store the cheat sheets
        in a git repo, [dufferzafar/cheat](https://github.com/dufferzafar/cheat) in go,
        [srsudar/eg](https://github.com/srsudar/eg) in python, with pre-loaded examples
        and a way to modify them.

# Dash Docsets {#dash_docsets}
[Dash](https://kapeli.com/dash) is an offline documentation browser created and maintained by
[Kapeli (Bogdan Popescu)](https://github.com/Kapeli). _Dash_ use
documentation in the _Docset format_ which is  just a folder containing the HTML
documentation and a SQLite database that indexes the files.
More information in the [Docset Generation Guide
](https://kapeli.com/docsets), the _docset_ format is specified in [this section
](https://kapeli.com/docsets#dashDocset), you find there also how to generate them, and
improve them to conform to the policy of _Dash_, and other compatible readers.

Dash is a software available only on Mac. But there is some docset readers for Linux.

-   [Zeal](https://zealdocs.org/) is a Qt docset browser. It can be shown with a
    customisable Hotkey, and it
    [integrates with emacs and vim](https://zealdocs.org/usage.html).
-   the github repository [dash-docs-el](https://github.com/dash-docs-el), group emacs
    packages that allow access to the dash docsets from emacs. The two fronends are
    _helm-dash_ and _counsel-dash_, both are available in _Melpa_.
-   [dash.vim](https://github.com/rizzatti/dash.vim) search dash from vim.
-   [zeavim.vim](https://github.com/KabbAmine/zeavim.vim) (Public domain License)
    allows to use the offline documentation browser Zeal from Vim
-   [atom-dash](https://github.com/blakeembrey/atom-dash) (MIT License)
    is a _Dash_ documentation integration with _Atom_.
-   [bracket-zeal](https://github.com/anephew/brackets-zeal)
    is a Zeal integration for the open source code editor for the web
    [Bracket](http://brackets.io).


There is a set of official docset, and a set of
[contributed docset](https://github.com/Kapeli/Dash-User-Contributions). The user
contribution repository don't contain the docset itself, only metadata. The
`<docset>tar.gz` file itself is pushed to Kapeli CDN. You can browse the
[json index of the CDN
](http://sanfrancisco.kapeli.com/feeds/zzz/user_contributed/build/index.json)
Once you have that, you can get to the docset archives at the URL:
```
http://<mirror>.kapeli.com/feeds/zzz/user_contributed/build/<key name inside json>/<archive name>
```
The two icons and the json description is in the [contributed docset repository
](https://github.com/Kapeli/Dash-User-Contributions).

The _mirrors_ are the same than those in the [regular dash docset feeds
](https://github.com/Kapeli/feeds).

To facilitate the download for Zeal a prebuild repository of xml feeds is
[hashhar/dash-contrib-docset-feeds](https://github.com/hashhar/dash-contrib-docset-feeds),

The Heroku site[Zeal Contribution site](https://zealusercontributions.now.sh/)
give the url of the xml feed, and the two icons for each contributed docset,
and the site [Zeal Cheat Sheet](https://zeal-cheatsheets.herokuapp.com/)
is used for the cheat sheets.

To install a docset in Zeal after opening the _ Add feed_ dialog, paste the URL. You can
then add the two icons inside docset folder next to Contents folder and meta.json file.

Some scripts are available to automate this process, I have not tested them.
[this python script](https://gist.github.com/crmne/3fe84c05013fa87d74a8), and the node
appli [jmerle/zeal-user-contrib](https://github.com/jmerle/zeal-user-contrib).


Kapeli the dash author also propose a set of
[Dash Cheat Sheets](https://kapeli.com/cheatsheets)
the source is in the GitHub repository
[Kapeli/cheatsheet]( https://github.com/Kapeli/cheatsheets).
[cheatset](https://github.com/Kapeli/cheatset) is a ruby program to generate these
cheets.

To generate your own docset, follow the
[Docset Generation Guide](https://kapeli.com/docsets),
this guide mention many sources of docset and programs to do the generation.

-   [doc2dash](https://doc2dash.readthedocs.io/en/stable/)
    Create docsets from Sphinx, or pydoctor.
    -    [doc2dash - GitHub](https://github.com/hynek/doc2dash).
-   [html2Dash](https://github.com/selfboot/html2Dash)
    a python program to generate a docset from any HTML documentations.
-   [dashing](https://github.com/technosophos/dashing) (MIT License)
    is a Dash generator script for any HTML.
-   [mandocset](https://github.com/Yanpas/mandocset)
    is python script that generates Dash docset from man pages.
-   [cargo-docset](https://github.com/Robzz/cargo-docset) (Apache License)
    Cargo subcommand to generate a Dash/Zeal docset for your Rust packages.
-   [william8th/javadocset](https://github.com/william8th/javadocset)
    is a golang program to generate a Dash/Zeal docset from javadoc.
    It is a port of
    [Kapeli's javadocset](https://github.com/Kapeli/javadocset) in Golang.


<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
