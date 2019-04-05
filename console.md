---
title: Console configuration
---

{{% toc /%}}

---

See also {{< iref "xorg" "Xorg section" >}},
{{< iref "checkpointing" "Checkpointing" >}}.

# References
-   Wikipedia {{< wp "Linux Console" >}},
-   [ArchWiki: console
    ](https://wiki.archlinux.org/index.php/Linux_console)
-   [The Linux keyboard and console HOWTO
    ](http://tldp.org/HOWTO/Keyboard-and-Console-HOWTO.html) _2002_
    by Andries Brouwer (
-   [Debian Wiki - Keyboard](https://wiki.debian.org/Keyboard)
-   [Text-Terminal-HOWTO
    ](http://tldp.org/HOWTO/Text-Terminal-HOWTO.html) _new release in 2013_.
-   [Loadkeys, Dumpkeys Tutorial
    ](http://www.developertutorials.com/tutorials/linux/loadkeys-dumpkeys-050518/)
    by Tony Lawrence.
-   [Linux console - ArchWiki](https://wiki.archlinux.org/index.php/Linux_console#Fonts)
-   [Linux console/Keyboard configuration - ArchWiki
    ](https://wiki.archlinux.org/index.php/Linux_console/Keyboard_configuration)
-   <a name="dvtm"></a>[dvtm](http://www.brain-dump.org/projects/dvtm/)
    ( MIT/X11 license) (dynamic virtual terminal manager) brings the concept of
    {{< iref "desktop#tiling_wm" "tiling window management" >}}
    used in {{< iref "desktop#dwm" "dwm" >}} to the console.
    It allows to work with multiple console based programs. It is in Debian.
    -   [dvtm additional documentation](http://waxandwane.org/dvtm.html)
        contains a [dvtm-commands pdf cheat sheet
        ](http://waxandwane.org/dvtm/dvtm-commands-A4.pdf).
    -   _Dtvm_ itself don't have session management but you can use
        {{< iref "checkpointing#abucco" "abucco" >}} or
        {{< iref "checkpointing#dtach" "dtach" >}}
        to provide the session management.
    -   _Dtvm_ can also be used in an X virtual console.
    -   We can also use in console a {{< iref "checkpointing#terminal_multiplexors" "Terminal multiplexor" >}}
        like screen or {{< iref "checkpointing#tmux" "tmux" >}}.

# Setting console Keyboard and Font
See also {{< iref "input_methods" "input method" >}},

-   The keyboard and font are set at startup with {{< man "setupcon" >}} from the package
    console-setup.
-   {{< man "setupcon" >}} default is to read the keyboard configuration from
    `/etc/default/keyboard` which can be overrided by `~/.keyboard`. The syntax of these
    files is given in {{< man "keyboard(5)" >}}.
-   {{< man "setupcon" >}} read the font configuration from `/etc/default/console-setup`
    overrided by ` ~/.console-setup` whose syntax is given in
    {{< man "console-setup(5)" >}}.
-   You can change `/etc/default/keyboard` by editing it or by running:

        # dpkg-reconfigure keyboard-configuration

    to activate the new setting run

        # service keyboard-setup restart

-   The same file `/etc/default/keyboard` is also used by Xorg and Wayland to set the
    keyboard.
-   Debian Wiki explains [How to set keyboard layout in initramfs
    ](https://wiki.debian.org/Keyboard#How_to_set_keyboard_layout_in_initramfs),
    and _How to enable USB keyboard in initramfs_.
-   A lower level utility to manipulate {{< man "keymaps(5)" >}} is {{< man "loadkeys" >}}.
-   A lower level utility to manipulate console fonts is {{< man "setfont(8)" >}}
-   The locale is seen by running {{< man "locale" >}} without arguments. The default are set in
    `/etc/default/locale` and can be changed by editing this file or running
    {{< man "update-locale(8)" >}}.
-   You can see all locales by running `locale -a`, the available locale are configured
    in `/etc/locale.gen` and can have to be regenerated with {{< man "locale-gen" >}} when you
    change this file.

-   [Linux Support for Funny/Functional Keys](http://rick.vanrein.org/linux/funkey).
-   [Keyboard/MultimediaKeys - Debian Wiki
    ](https://wiki.debian.org/Keyboard/MultimediaKeys).
-   [autres-clavier multimedia - Lea Linux
    ](http://lea-linux.org/documentations/Hardware-hard_autres-clavier_multimedia)

## Lower level Utilities

{{< man "showkey" >}}
:   prints to standard output either the scan codes (`-s`) or the
    keycode (`-k`) or the ascii code(`-a`) of each key pressed.
    _It can be used only on console._

{{< man "loadkeys" >}}
:   load a kernel keymap for the console.

{{< man "dumpkeys" >}}
:   writes the current contents of the keyboard drivers translation
    tables

{{< man "unicode\_start" >}}
:   Enables Unicode processing in the current console.

-   first reload the keys in unicode to produce UTF-8 encoded
    multibyte sequences, instead of single bytes >= 0x80 by
    `dumpkeys | loadkeys --unicode`
-   Tell the console output driver that the bytes arriving are
    UTF-8 encoded multibyte sequences by
    `echo -n -e               '\033%G'`
-   set the font to `$1` and optionally the map to `$2`

# Console fonts {#console_fonts}
-   [Into the Mist: How Linux Console Fonts Work
    ](http://linuxgazette.net/91/loozzr.html)
    article in linux gazette.
-   [Font-formats recognized by the Linux kbd package
    ](http://www.win.tue.nl/~aeb/linux/kbd/font-formats.html) _2001_)
    by Andries Brouwer
-   [ArchWiki: console Fonts
    ](https://wiki.archlinux.org/index.php/Linux_console#Fonts)
-   [nafe](http://nafe.sourceforge.net/)
    is a toolset to translate psf format console fonts to and from
    text files.
-   bdf2psf is a command line converter from bdf to psf
-   Dmitry Bolkhovityanov has produced the
    [Unicode VGA font
    ](http://www.inp.nsk.su/~bolkhov/files/fonts/univga/index.html)
    is a Unicode VGA font for X11 and console that covers a large part
    of unicode blocks.
-   [fonty-rg](http://nixbit.com/cat/system/console-fonts/fonty-rg/)
    is a set of fonts for the Linux console providing LatCyrGr-16.psf
    and chavo.psf to cover most of iso8859-1 and iso8859-2. _2005_
-   Mark Leisher [gbdfed Bitmap Font Editor
    ](http://www.math.nmsu.edu/~mleisher/Software/gbdfed/)
    _2010_ lets you interactively create new bitmap font files or
    modify existing ones, it can export HEX fonts and PSF2 Linux
    console fonts and import Metafont PK/GF fonts, Linux console (PSF,
    CP, and EGA/VGA) fonts, OpenType (OTF & TTF) fonts, fonts from the
    X server.  The manual is
    [gbdfed(1)
    ](http://www.math.nmsu.edu/~mleisher/Software/gbdfed/gbdfed-man.html)
-   [PSF Tools](http://www.seasip.info/Unix/PSF/index.html)
    is a psf font conversion tool.
-   [bdflib](https://github.com/peter-conalgo/bdflib)
    is a python library for working with BDF font files, see
    [BDF Fonts and Modern Linux](http://thristian.livejournal.com/90017.html).

# kmscon {#kmscon}
Kmscon is a simple terminal emulator based on linux kernel mode setting (KMS)
_but KMS is not required for Kmscon_.
It replaces the in-kernel VT implementation with a userspace
console.

It does not depend on any graphics-server, like X.org, but instead
provides a raw console layer that can be used independently.

Kmscon provides  full-internationalized keyboard handling, full UTF8
input/font support, hardware-accelerated rendering, multi-seat support
and more.

Kmscon can also run in listen-mode and replace virtual terminals. This
allows to run multiple graphics-servers (like kmscon,  X-Server,
{{< iref "xorg#wayland" "Wayland Compositors" >}}
simultaneously on all seats.

-   Wikipedia {{< wp "kmscon" >}}
-   [Freedesktop: kmscon - KMS/DRM based System Console
    ](http://www.freedesktop.org/wiki/Software/kmscon/)
-   [ArchWiki: kmscon
    ](https://wiki.archlinux.org/index.php/KMSCON).
    _kmscon is in Arch but not yet Debian.
-   [kmscon introduction
    ](https://dvdhrm.wordpress.com/2012/12/10/kmscon-introduction/)
    describe the use of _kmscon_ for {{< wp "multiseat configuration" >}}
-   _kmscon- is build upon [libstm](https://www.freedesktop.org/wiki/Software/libtsm/)
    _Terminal-emulator State Machine_ This library is very similar to libvte but without
    GTK+ bindings, it allows mainly to interpret terminal escape sequences in a Xterm
    compatible way.
-   [kmscon GitHub repository
    ](https://github.com/dvdhrm/kmscon)
-   The [kmscon repository](https://github.com/dvdhrm/kmscon)contains also the source of
    [wlterm](https://www.freedesktop.org/wiki/Software/kmscon/wlterm/)
    a native Wayland terminal build upon libstm. More explanations in this
    [post from David Herrmann](https://lwn.net/Articles/517818/).

# Framebuffer terminals {#framebuffer_terminals}

[fbterm](http://code.google.com/p/fbterm/ )(Frame buffer terminal emulator),
[Archwiki: Fbterm](https://wiki.archlinux.org/index.php/Fbterm)
is a replacement of Linux console terminal that can function outside
of Xorg. The development has stopped _there is still a Debian package_.


[fbpad (git)](http://repo.or.cz/w/fbpad.git),
[ArchWiki: fbpad](https://wiki.archlinux.org/index.php/Fbpad) is a
small framebuffer terminal that manages many terminals through single
character tags. It is exceptionally lightweight,  written in C and
using its own font format, tinyfont, which avoids xorg font
dependencies. fbpad optionally supports 256 colors, bold fonts, and
saving the framebuffer contents to memory.

[yaft](https://github.com/uobikiemukot/yaft)
is simple framebuffer terminal emulator.  yaft supports UCS2 glyphs
including wide character and 256 color.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
