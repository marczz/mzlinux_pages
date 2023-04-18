---
title: Text Editors
---

{{< iref "emacs" "Emacs has its own section" >}}
where you find also {{< iref "emacs#terminal_editors_emacslike" "emacs compatible editors" >}}.

# List of text editors
-   Wikipedia {{< wp "Comparison of text editors" >}}.
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


## misc terminal editors
-   {{< wp "ne (text editor)"  "ne" >}} (GPL)
    is a small curses editor. ne supports UTF-8, syntax highlighting,
    regular expressions, configurable menus and keybindings and autocomplete.
    -   [ne Home page](http://ne.di.unimi.it/),
    -   [ne’s manual](http://ne.di.unimi.it/docs/index.html),
    -   [Unix: ne Editor - Help & Support - The University of North Carolina
        ](http://help.unc.edu/help/unix-ne-editor/)
    -   _ne_ footprints as for v 2.5 2015 are 2.9M res / 2.6M shr
-   [cream](http://cream.sourceforge.net/)
    is a configuration of  Vim, aimed to simplify it's use for vim
    beginners and implementing a {{< wp "IBM Common User Access"  "CUA" >}}
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
