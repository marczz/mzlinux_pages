---
title: Text Editors Notes
---

{{% toc /%}}

# VI

-   Steve Losh has many [Vim projects](http://stevelosh.com/projects/)
    Including a theme _Bad Wolf_.

## Hex editor

We may choose between:
-   dhex
-   [shed](https://packages.debian.org/sid/shed)
    in ncurses with pico style editing, do'nt load whole file in
    memory
-   [dhex](https://packages.debian.org/sid/dhex)
    in ncurses, can do hexa diff.
-   [beav](https://packages.debian.org/sid/beav)
    ncurses binary editor.
-   [ncurses-hexedit](
    https://packages.debian.org/buster/ncurses-hexedit)
-   [lfhex](https://packages.debian.org/sid/lfhex)
    for large files, QT interface.
-   [bless](https://packages.debian.org/sid/bless)
    gnome editor written in mono.
-   [jeex](https://packages.debian.org/sid/jeex)
    GTK editor.
-   [WxHexEditor](https://packages.debian.org/sid/wxhexeditor)
    interface in WxGTK.


-   Emacs with [Hexl Mode](https://www.emacswiki.org/emacs/HexlMode)
-   We can use [xxd](https://packages.debian.org/sid/xxd), it's not an
    editor, but convert files to and from hexadecimal.
-   In VI uses :`%:!xxd` to switch into hex mode,
    `:%!xxd -r` to exit from hex mode
