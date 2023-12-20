---
title: Console configuration
---

The keyboard settings of the console is in
{{< iref "keyboard_input#console" "Console Keyboard Input" >}}

See also {{< iref "booting" "Booting" >}}, {{< iref "xorg" "Xorg section" >}},
{{< iref "checkpointing" "Checkpointing" >}}.

---

# References
-   Wikipedia {{< wp "Linux Console" >}},
-   [Linux console - ArchWiki](https://wiki.archlinux.org/title/Linux_console)
-   [Text-Terminal-HOWTO
    ](http://tldp.org/HOWTO/Text-Terminal-HOWTO.html) _new release in 2013_.
    by Tony Lawrence.
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

# Console message log

The Linux kernel log levels are integers from 0 to 7.

| level | name         |
|-------|--------------|
| 0     | KERN_EMERG   |
| 1     | KERN_ALERT   |
| 2     | KERN_CRIT    |
| 3     | KERN_ERR     |
| 4     | KERN_WARNING |
| 5     | KERN_NOTICE  |
| 6     | KERN_INFO    |
| 7     | KERN_DEBUG   |

You can know the loglevel with
~~~
$ cat /proc/sys/kernel/printk
4	4	1	7
~~~

or
~~~
$ sysctl kernel.printk
kernel.printk = 4	4	1	7
~~~

The four numbers are values of _console_loglevel_, _default_message_loglevel_,
_minimum_console_loglevel_, _default_console_loglevel_.

In the previous example the current level is _KERN_WARNING_ meaning that only messages
with a severity of at least _warning_ are written to the console.

You can change the console level until newt boot with:
~~~
# echo "3" > /proc/sys/kernel/printk
~~~
or
~~~
# sysctl -w kernel.printk=3
~~~

-   {{< man "printk(2)" >}}
-   {{< man "syslog(2)" >}}
-   Wikipedia: {{< wp "syslog" >}}, {{< wp "printk" >}}
-   [Introduction to the Linux kernel log levels - LinuxConfig.org
    ](https://linuxconfig.org/introduction-to-the-linux-kernel-log-levels)


The the magic SysRq key is a key combo you can hit which the kernel will respond to
regardless of whatever else it is doing, unless it is completely locked up.

You send it by pressing `ALT-SysRq-<command key>`, or `ALT-SysRq` followed by
`ALT-<command key>`.

-   [Linux Magic System Request Key Hacks — The Linux Kernel documentation
    ](https://www.kernel.org/doc/html/latest/admin-guide/sysrq.html)
-   Wikipedia: {{< wp "Magic SysRq key" >}}

# Setting console Keyboard and Font {#console_setup}
See also {{< iref "input_methods" "input method" >}},

-   The keyboard and font are set at startup with {{< man "setupcon(1)" >}} from the package
    console-setup.
-   {{< man "setupcon(1)" >}} default is to read the keyboard configuration from
    `/etc/default/keyboard` which can be overrided by `~/.keyboard`. The syntax of these
    files is given in {{< man "keyboard(5)" >}}.
-   {{< man "setupcon(1)" >}} read the font configuration from `/etc/default/console-setup`
    overrided by ` ~/.console-setup` whose syntax is given in
    {{< man "console-setup(5)" >}}.
-   You can change `/etc/default/keyboard` by editing it or by running:

        # dpkg-reconfigure keyboard-configuration

    to activate the new setting run

        # systemctl restart keyboard-setup

    But if you only want to temporarily change the console keyboard run

        $ setupcon VARIANT

    which read the configuration `/etc/default/keyboard.VARIANT`.

-   The pkg `kbd` requires either the older `console-data` or the more recent
    `console-setup`.

    The `console-data` load keymaps in `/usr/share/keymaps` with `loadkeys`.
    So there are a distinct description of the keymaps for X and for the console.

    The package `console-setup` on the other hand, use {{< man "setupcon(1)" >}}
    which call {{< man "ckbcomp(1)" >}}to compile the xkb description
    in a temporary console keymap which is loaded by {{< man "loadkeys(1)" >}}.
    No separate console keymap is necessary.

-   The same file `/etc/default/keyboard` is also used by Xorg and Wayland to set the
    keyboard.
-   Debian Wiki explains [How to set keyboard layout in initramfs
    ](https://wiki.debian.org/Keyboard#How_to_set_keyboard_layout_in_initramfs),
    and _How to enable USB keyboard in initramfs_.
-   A lower level utility to manipulate {{< man "keymaps(5)" >}} is
    {{< man "loadkeys(1)" >}}.
-   A lower level utility to manipulate console fonts is {{< man "setfont(8)" >}}
-   The locale is seen by running {{< man "locale" >}} without arguments.
    The default are set in `/etc/default/locale` and can be changed by editing this file
    or running {{< man "update-locale(8)" >}}.
-   You can see all locales by running `locale -a`, the available locale are configured
    in `/etc/locale.gen` and can have to be regenerated with {{< man "locale-gen" >}}
    when you change this file.

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
    ](https://github.com/dvdhrm/kmscon) _2014_.
-   The [kmscon repository](https://github.com/dvdhrm/kmscon)contains also the source of
    [wlterm](https://www.freedesktop.org/wiki/Software/kmscon/wlterm/)
    a native {{< iref "xterminals#wayland_terminals" "Wayland terminal" >}}
    build upon libstm. More explanations in this
    [post from David Herrmann](https://lwn.net/Articles/517818/).

# Framebuffer terminals {#framebuffer_terminals}

-   [fbterm](http://code.google.com/p/fbterm/ )(Frame buffer terminal emulator),
    is a replacement of Linux console terminal that can function outside
    of Xorg. The development has stopped _there is still a Debian package_.
    It uses X libraries to handle TTF fonts.
    -   [Archwiki: Fbterm](https://wiki.archlinux.org/index.php/Fbterm)


-   [fbpad (git)](http://repo.or.cz/w/fbpad.git),
    is a small framebuffer terminal that manages many terminals through single character
    tags. It is exceptionally lightweight, written in C and using its own font format,
    tinyfont, which avoids xorg font dependencies. fbpad optionally supports 256 colors,
    bold fonts, and saving the framebuffer contents to memory.
    -   [ArchWiki: fbpad](https://wiki.archlinux.org/index.php/Fbpad)
    -   _fbpad_ use fonts in a special _tinyfont_ format.
        The two programs *mkfn_ft* and *mkfn_stb* from the
        [fbpad_mkfn](https://repo.or.cz/fbpad_mkfn.git) repository convert ttf or stb
        truetype to The font format for fbpad _tinyfonts_.

-   [yaft](https://github.com/uobikiemukot/yaft)
    is simple framebuffer terminal emulator.  yaft supports UTF8 and UCS2 glyphs
    including wide character and 256 color. It hs its own format of fonts, that are
    created by translating BDF fonts with the provided utility *mkfont_bdf*

-   The [nosh package](https://jdebp.eu/Softwares/nosh/) is a suite of
    system-level utilities for initializing and running a BSD or Linux system, for managing
    daemons, for managing terminals, and for managing logging. All the nosh software is
    also available as Debian packages.

    [User-space virtual terminals
    ](https://jdebp.eu/Softwares/nosh/user-vt-screenshots.html)
    are one of the terminal management features of the nosh package.

    [console-terminal-emulator
    ](https://jdebp.eu/Softwares/nosh/guide/commands/console-terminal-emulator.xml)
    a userspace virtual terminal aimed at replicating Linux and FreeBSD/PC-BSD kernel
    virtual terminals.

    For more info look at the [nosh Guide](https://jdebp.eu/Softwares/nosh/guide/).

-  [Bogl Bterm](https://packages.debian.org/sid/bogl-bterm)
   an a UTF-enabled framebuffer terminal, part of Ben's Own Graphics Library, a small
   framebuffer library including basic widgets, support for text in multiple languages,
   and mouse handling. It uses its own bgf font format from fonts created with the
   _bdftobogl_ utility.


-   More references in the excellent summary of this
    [answer to: How to use /dev/fb0 as a console from userspace
    ](https://unix.stackexchange.com/questions/20458/how-to-use-dev-fb0-as-a-console-from-userspace-or-output-text-to-it#177209).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
