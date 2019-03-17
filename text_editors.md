<!--
.. description:
.. date: 2015-07-01
.. slug: text_editors
.. tags:
.. link:
.. book: mzlinux
.. title: Text Editors
-->

[TOC]

[Emacs has its own section](/node/emacs "internal reference")
where you find also [emacs compatible editors
](/node/emacs#terminal_editors_emacslike "internal reference").

# List of text editors
-   Wikipedia [w:Comparison of text editors].
-   [ArchWiki: List of Text Editors
    ](https://wiki.archlinux.org/index.php/List_of_applications#Text_editors)

# Terminal editors {#terminal_editors}
## nano
[Nano](http://www.nano-editor.org/) (GPL) <a name="nano"></a>
is a tiny editor, that provide a superset of _pico_.

Nano is truly tiny, without loading syntax files nano 2.2 takes
on an amd64 or either on an arm server 1.3M resident with 1M  shared (with no file loaded),
with all the syntax files we get 1.6M/1.1M. Debian package a stripped build under the name
_nano-tiny_ which bind to _libslang_ instead of _libncurses_,
but it saves only 0.1M mega resident.
In 2015 I made a new test on nano 2.2.6 finding on amd64 3.7M res /
2.6M shared. while on armv7 it is 1.8M/1.2M.

-    [nano Command Manual](http://www.nano-editor.org/dist/latest/nano.html),
     [nano(1)](http://www.nano-editor.org/dist/latest/nano.1.html)
     [nanorc (5)](http://www.nano-editor.org/dist/latest/nanorc.5.html),
     [nano FAQ](http://www.nano-editor.org/dist/latest/faq.html)
-    [Nano and nanorc Tips and Tricks
     ](http://www.if-not-true-then-false.com/2009/tuning-nano-text-editor-with-nanorc/)
-    A complete set of syntax highlight rules for nano in
     [GitHub: Craig Barnes - nanorc](https://github.com/craigbarnes/nanorc)

## vi
-   Wikipedia [w:vi]
-   [neatvi](http://repo.or.cz/neatvi.git)
    is a small ex/vi editor for editing bidirectional utf-8 text.
-   [vis](https://github.com/martanne/vis)
    extends vi's modal editing with built-in support for multiple cursors/selections and
    combines it with [sam's structural regular expression
    ](https://github.com/martanne/vis/wiki/FAQ#what-are-structural-regular-expressions)
    based command language.
    -   [vis differences from vim
        ](ttps://github.com/martanne/vis/wiki/Differences-from-Vi(m))
    -   [vis(1) Manual](http://martanne.github.io/vis/man/vis.1.html)


## vim
-   [Vim Home Page](http://www.vim.org/)
-   [vim documentation
    ](http://vimdoc.sourceforge.net/)
    -   [vim user manual
        ](http://vimdoc.sourceforge.net/htmldoc/)
    -   [vim faq
        ](http://vimdoc.sourceforge.net/htmldoc/vimfaq.html)
-   [online version of vim help with hyperlinks
    ](http://vimhelp.appspot.com/) updated to the last vim
-   [online version of neovim help with hyperlinks
    ](https://neovim.io/doc/user/index.html)
-   [vim book in libreoffice and pdf
    ](http://www.oualline.com/vim-book.html)
-   references for vi in the [Vi Lovers Home Page
    ](http://www.thomer.com/vi/vi.html).
 -  [Vim Tips wiki](http://vim.wikia.com/wiki/)
    has [vim documentation
    ](http://vim.wikia.com/wiki/Vim_documentation)
-   [Vim for humans](https://vimebook.com/en) or
    [Vim pour les humains](https://vimebook.com/fr)
    is a free vim ebooks, whose sources are [on GitHub.
    ](https://github.com/vjousse/vim-for-humans-book).
    The sources are in Sphinx RST.
-   [Getting Started with Vi
    ](http://www.linuxjournal.com/article/6542) (Linux Journal)
-   [A Slightly Advanced Introduction to Vim
    ](http://linuxgazette.net/152/srinivasan.html)
-   [Wikibook: Learning the vi editor
    ](https://en.wikibooks.org/wiki/Learning_the_vi_Editor)
    [Seven habits of effective text editing  (with vi)
    ](http://www.moolenaar.net/habits.html)
-   [Learn Vimscript the Hard Way
    ](http://learnvimscriptthehardway.stevelosh.com/)
    by Steve Losh. [GitHub repository
    ](https://github.com/sjl/learnvimscriptthehardway).
-   [vim ref card by command (pdf)
    ](http://utools.com/vimrefcard.pdf)
-   [Vim quick reference cards
    ](http://tnerual.eriogerg.free.fr/vim.html):
        [english pdf](http://tnerual.eriogerg.free.fr/vimqrc.pdf),
        [english html](http://tnerual.eriogerg.free.fr/vimqrc.html),
        [french pdf](http://tnerual.eriogerg.free.fr/vimqrc-fr.pdf),
        [french html](http://tnerual.eriogerg.free.fr/vimqrc-fr.html)
-   Tutorials: [vim-201-an-intermediate-guide-to-vim
    ](http://www.linux.com/learn/tutorials/243002-vim-201-an-intermediate-guide-to-vim),
    [vim-301-getting-adept-at-vim
    ](http://www.linux.com/learn/tutorials/262147-vim-301-getting-adept-at-vim),
    [vim-401-extending-vim-and-more
    ](http://www.linux.com/learn/tutorials/264315-vim-401-extending-vim-and-more).
-   [vim-markdown](http://github.com/plasticboy/vim-markdown/)

## neovim
[neovim](https://neovim.io/) (apache license)
is an heavily refactored vim fork.

It allows  executing jobs / tasks asynchronously wich is a missing in vim.

It has an [integrated terminal emulator
](https://neovim.io/doc/user/nvim_terminal_emulator.html)
and a can communicate with external processes, lua, ruby, python.


-   [neovim FAQ](https://github.com/neovim/neovim/wiki/FAQ)
-   [online version of neovim help with hyperlinks
    ](https://neovim.io/doc/user/index.html)
-   [list of plugins that use neovim features
    ](https://github.com/neovim/neovim/wiki/Related-projects#plugins)
-   [Why Neovim is Better than Vim
    ](http://geoff.greer.fm/2015/01/15/why-neovim-is-better-than-vim/)
-   [python-client](https://github.com/neovim/python-client)
-   [Moving to Neovim from Vim
    ](https://jacky.wtf/weblog/moving-to-neovim/)

## vim regular expressions

-   __Vim documentation__: [Search commands and patterns
    ](http://vimhelp.appspot.com/usr_27.txt.html),
    [pattern
    ](http://vimhelp.appspot.com/pattern.txt.html)
    the same doc you obtain with `:help pattern`
-   __Neovim documentation__: [Search commands and patterns
    ](https://neovim.io/doc/user/usr_27.html),
    [pattern
    ](https://neovim.io/doc/user/pattern.html).
-   [vimregex](http://vimregex.com/) a page dedicated to vim re.
-   [Learn Vimscript the Hard Way
    ](http://learnvimscriptthehardway.stevelosh.com/)
    [Basic Regular Expressions chapter
    ](http://learnvimscriptthehardway.stevelosh.com/chapters/31.html)

## vim footprints

vim.basic without init takes 5.2M resident / 4.6M shared, 3.8M/3.2M on
armel with my config and plugins it takes 7.5M/4.8M.

vim.nox is compiled with support for scripts in python, perl, lua,
ruby, tcl
(as do vim.gtk) it uses 10.5M/7.3M on armel 5.9M/5M.

vim.gtk in a terminal without loading any config takes 14M resident /
12M shared (18M / 12M for gtk3), with my config and plugins it takes
18M, 12M shared.

gvim.gtk in gtk gui _most often invoked as gvim_ is 25M/20M for the
raw run (32M/23M for gtk3) and 27M/20M with the initialisation and
plugins.

vim.tiny raw is 3.7M/3.3M (2.8M/2.4M on armel) or with init 3.9M/3.4M.

neovim uses 8.8M/5.3M.

nvim-qt uses 37M/30M.

## misc terminal editors
-   [w:ne (text editor)|ne] (GPL)
    is a small curses editor. ne supports UTF-8, syntax highlighting,
    regular expressions, configurable menus and keybindings and autocomplete.
    -   [ne Home page](http://ne.di.unimi.it/),
    -   [ne’s manual](http://ne.di.unimi.it/docs/index.html),
    -   [Unix: ne Editor - Help & Support - The University of North Carolina
        ](http://help.unc.edu/help/unix-ne-editor/)
    -   _ne_ footprints as for v 2.5 2015 are 2.9M res / 2.6M shr
-   [cream](http://cream.sourceforge.net/)
    is a configuration of  Vim, aimed to simplify it's use for vim
    beginners and implementing a [w:IBM Common User Access|CUA]
    keybinding. It is in debian.

# Javascript editors
-   [Ace](https://ace.c9.io/) (BSD license)
    is an embeddable code editor written in node.js JavaScript.
-   [Atom](https://atom.io/) (MIT License)
    Atom is an extensible text editor built on [Electron
    ](https://github.com/electron/electron) javascript platform.
    It runs on OS X, Windows, or Linux, a debian package is available.
    It has a built-in package manager with numerous extensions, and
    allow a choice of themes and deep customization.
-   [Brackets
    ](http://brackets.io/)
    (MIT License)
    code editor built in HTML, CSS and JavaScript for HTML, CSS and
    JavaScript. It has [numerous extensions
    ](https://brackets-registry.aboutweb.com/),
    some syntax highlighter or preview for Asciidoc,  Liquid, Livescript, Markdown,RST,
    Textile, Markdown and syntax highlighters
    for many programming languages APL, COBOL, Common lisp, D, ECL, Erlang, Eiffel,
    Fortran, Haskell,Jade, Julia, Lua, Rust.
    It is available for Mac, Windows and Linux, and here is Debian
    package for Brackets.
    -   [Brackets Manual
        ](https://github.com/adobe/brackets/wiki/How-to-Use-Brackets)



# Graphical editors
-   [X2](http://gtk-apps.org/content/show.php?content=145463)
    is an simple text/programming editor based on gtksouceview and
    vte. _developpement stopped in 2012_ It is in debian.
-   [Yi](http://www.haskell.org/haskellwiki/Yi) is an editor written in Haskell.
-   The [list of python editors](https://wiki.python.org/moin/PythonEditors)
    includes  DrPython, SCiTe, scribes, geany ...


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
