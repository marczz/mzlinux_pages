---
title: Neovim and Vim
---

<!--
[[file:../../../../content-org/notes/text_processing_notes/neovim_notes.org][neovim_notes.org]]
-->


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
-   [lists of which programs support Vim-like keybindings
    ](https://github.com/erikw/vim-keybindings-everywhere-the-ultimate-list)
     natively, or how they can be added with extensions

# (Neo)Vim documentation
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
-   [Seven habits of effective text editing  (with vi)
    ](http://www.moolenaar.net/habits.html)
-   [Learn Vimscript the Hard Way](http://learnvimscriptthehardway.stevelosh.com/)
    by Steve Losh.
    -   [GitHub repository](https://github.com/sjl/learnvimscriptthehardway).
-   [A Vimlike Fluency: Bibliography and Next Steps – Terminally Undead
    ](https://countvajhula.com/2021/02/23/a-vimlike-fluency-bibliography-and-next-steps/).

## Vim tutorials
-   [Getting Started with Vi](http://www.linuxjournal.com/article/6542) (Linux Journal)
-   [A Slightly Advanced Introduction to Vim
    ](http://linuxgazette.net/152/srinivasan.html)
-   [Wikibook: Learning the vi editor](https://en.wikibooks.org/wiki/Learning_the_vi_Editor)
-   [Learn Vim the Smart Way](https://learnvim.irian.to/)
    comprehensive tutorial by [Igor Irianto](https://irian.to/).
    -   [How to Learn Vim in 2020](https://irian.to/blogs/how-to-learn-vim-in-2020/)
        index many [posts of Igor Irianto on dev.to](https://dev.to/iggredible/).
-   [linux.com](https://www.linux.com/?s=vim) has a lot of
    [vim tutorials](https://www.linux.com/?s=vim) *with often scarse content* :
    [vim-201-an-intermediate-guide-to-vim
    ](https://www.linux.com/training-tutorials/vim-201-intermediate-guide-vim/),
    [vim-301-getting-adept-at-vim
    ](https://www.linux.com/training-tutorials/vim-301-getting-adept-vim/),
    [vim-401-extending-vim-and-more
    ](https://www.linux.com/training-tutorials/vim-401-extending-vim-and-more/).
-   [Vim Text Objects: The Definitive Guide
    ](https://blog.carbonfive.com/vim-text-objects-the-definitive-guide/).
-   [A Vimlike Fluency: Daily Tips for Learning Vim – Terminally Undead
    ](https://countvajhula.com/2021/01/21/vim-tip-of-the-day-a-series/)
    a set of 17 tutorials.
-   [Vim - DEV Community](https://dev.to/t/vim).
-   [Neovim - DEV Community](https://dev.to/t/neovim).

## Vim cheatsheets, quick refs
-   [vim ref card by command (pdf)](http://utools.com/vimrefcard.pdf)
-   [Vim quick reference cards](http://tnerual.eriogerg.free.fr/vim.html):
        [english pdf](http://tnerual.eriogerg.free.fr/vimqrc.pdf),
        [english html](http://tnerual.eriogerg.free.fr/vimqrc.html),
        [french pdf](http://tnerual.eriogerg.free.fr/vimqrc-fr.pdf),
        [french html](http://tnerual.eriogerg.free.fr/vimqrc-fr.html)
-   [Vim Cheat Sheet - rtorr.com](https://vim.rtorr.com/).
-   [sudormrfbin/cheatsheet.nvim](https://github.com/sudormrfbin/cheatsheet.nvim)
    A cheatsheet plugin for neovim with bundled cheatsheets for the editor, multiple
    vim plugins, nerd-fonts, regex, etc. with a Telescope fuzzy finder interface.
-   [rdvm/rofi-vim](https://github.com/rdvm/rofi-vim)
    A Vim cheat sheet for Rofi.
-   [Vim Reference Guide](https://learnbyexample.github.io/vim_reference)
    by Sundeep Agarwal, the markdown source is available in
    [GitHub - learnbyexample](https://github.com/learnbyexample/vim_reference)
    like a cheatsheet with examples.

## vim plugins
-   [Vim Awesome](https://vimawesome.com/) list of vim plugins.
-   [awesome-vim](https://github.com/akrawchyk/awesome-vim)
    a Vim plugin shortlist.
-   See in {{< iref "rest" "ReStructured Text page" >}} the
    {{< iref "rest#vim_rest" "list of ReSt support plugins" >}}.
-   [vim-markdown](http://github.com/plasticboy/vim-markdown/).
-   [GitHub - nvim-orgmode Orgmode clone written in Lua
    ](https://github.com/nvim-orgmode/orgmode)
-   [tpope/vim-fugitive](https://github.com/tpope/vim-fugitive)
    A vim/neovim Git wrapper.a
-   [junegunn/fzf.vim](https://github.com/junegunn/fzf.vim)
    is not a Vim plugin, bu  is a bundle of fzf-based commands and mappings.
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

-   [Documentation - Neovim](https://neovim.io/doc/general/)
-   [neovim Wiki](https://github.com/neovim/neovim/wiki)
-   [neovim FAQ](https://github.com/neovim/neovim/wiki/FAQ)
-   [online version of neovim help with hyperlinks
    ](https://neovim.io/doc/user/index.html)
    is an index of html rendered version of all the help files distributed with neovim
    that you visualise with the `:help`command inside nvim.
-   [python-client](https://github.com/neovim/python-client)
-   [Moving to Neovim from Vim](https://jacky.wtf/weblog/moving-to-neovim/)
-   [neovim-qt](https://github.com/equalsraf/neovim-qt)
    Neovim client library and GUI, in Qt5. _in Debian_.

## Neovim lua engine

-   [Lua Everywhere - What's New in Neovim 0.7
    ](https://gpanders.com/blog/whats-new-in-neovim-0-7#lua-everywhere)
-   [Lua - Neovim docs](https://neovim.io/doc/user/lua.html)
    html formatted version of the help file lua.txt that you display in nvim with
    `:help lua`.
-   [Luaref - Neovim docs](https://neovim.io/doc/user/luaref.html)
    html formatted version of the help file luaref.txt in nvim ≥ 0.8.
-   [Lua-guide - Neovim docs](https://neovim.io/doc/user/lua-guide.html)
    html formatted version of the help file lua-guide.txt in nvim ≥ 0.9.
-   [Lua: reference manual - lua.org](https://www.lua.org/manual/)


-   [FooSoft Productions - Saying Goodbye to Vimscript
    ](https://foosoft.net/posts/saying-goodbye-to-vimscript/)
    is a tutorial to use of lua in vim configuration.

## Neovim configuration
-   [LunarVim/Neovim-from-scratch](https://github.com/LunarVim/Neovim-from-scratch)
    A Neovim config designed from scratch to be understandable.

## Neovim Plugins.

-   [list of plugins that use neovim features
    ](https://github.com/neovim/neovim/wiki/Related-projects#plugins)
-   [Why Neovim is Better than Vim
-   [rockerBOO/awesome-neovim](https://github.com/rockerBOO/awesome-neovim/)
    Collections of awesome Neovim plugins.
-   [telescope.nvim](https://github.com/nvim-telescope/telescope.nvim)
    extendable fuzzy finder over lists.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
