---
title: Neovim and Vim
---


# vi
-   Wikipedia {{< wp "vi" >}}
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


# Vim {#vim}
-   [Vim Home Page](http://www.vim.org/)
-   [vim documentation](http://vimdoc.sourceforge.net/)
    -   [vim user manual](http://vimdoc.sourceforge.net/htmldoc/)
    -   [vim faq](http://vimdoc.sourceforge.net/htmldoc/vimfaq.html)
-   [online version of vim help with hyperlinks](http://vimhelp.appspot.com/)
    updated to the last vim.
-   [online version of neovim help with hyperlinks](https://neovim.io/doc/user/index.html)
-   [vim book in libreoffice and pdf](http://www.oualline.com/vim-book.html)
-   references for vi in the [Vi Lovers Home Page](http://www.thomer.com/vi/vi.html).
 -  [Vim Tips wiki](http://vim.wikia.com/wiki/)
    has [vim documentation](http://vim.wikia.com/wiki/Vim_documentation)
-   [Vim for humans](https://vimebook.com/en) or
    [Vim pour les humains](https://vimebook.com/fr)
    is a free vim ebooks, whose sources are
    [on GitHub.](https://github.com/vjousse/vim-for-humans-book).
    The sources are in Sphinx RST.
-   [Getting Started with Vi](http://www.linuxjournal.com/article/6542) (Linux Journal)
-   [A Slightly Advanced Introduction to Vim
    ](http://linuxgazette.net/152/srinivasan.html)
-   [Wikibook: Learning the vi editor](https://en.wikibooks.org/wiki/Learning_the_vi_Editor)
    [Seven habits of effective text editing  (with vi)
    ](http://www.moolenaar.net/habits.html)
-   [Learn Vimscript the Hard Way](http://learnvimscriptthehardway.stevelosh.com/)
    by Steve Losh.
    -   [GitHub repository](https://github.com/sjl/learnvimscriptthehardway).
-   [vim ref card by command (pdf)](http://utools.com/vimrefcard.pdf)
-   [Vim quick reference cards](http://tnerual.eriogerg.free.fr/vim.html):
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

## vim plugins
-   [Vim Awesome](https://vimawesome.com/) list of vim plugins.
-   [awesome-vim](https://github.com/akrawchyk/awesome-vim)
    a Vim plugin shortlist.
-   See in {{< iref "rest" "ReStructured Text page" >}} the
    {{< iref "rest#vim_rest" "list of ReSt support plugins" >}}.
-   [vim-markdown](http://github.com/plasticboy/vim-markdown/)
-   [SpaceVim](https://spacevim.org/) is a preconfigured configuration for Vim and
    Neovim.

## vim regular expressions {#vim_regexps}

-   __Vim documentation__:
    [Search commands and patterns](http://vimhelp.appspot.com/usr_27.txt.html),
    [pattern](http://vimhelp.appspot.com/pattern.txt.html)
    the same doc you obtain with `:help pattern`
-   __Neovim documentation__:
    [Search commands and patterns](https://neovim.io/doc/user/usr_27.html),
    [pattern](https://neovim.io/doc/user/pattern.html).
-   [vimregex](http://vimregex.com/) a page dedicated to vim re.
-   [Learn Vimscript the Hard Way](http://learnvimscriptthehardway.stevelosh.com/)
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

# Neovim {#neovim}
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
-   [Moving to Neovim from Vim](https://jacky.wtf/weblog/moving-to-neovim/)
-   [neovim-qt](https://github.com/equalsraf/neovim-qt)
    Neovim client library and GUI, in Qt5. _in Debian_.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
