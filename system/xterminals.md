---
title: Terminal emulators
---

See also {{< iref "desktop" "Desktop" >}}, {{< iref "checkpointing#tmux" "Tmux" >}}.

# Terminals emulators
-   Wikipedia has an _incomplete_ {{< wp "List of terminal emulators" >}}.
-   [ArchWiki: List of terminal emulators
    ](https://wiki.archlinux.org/index.php/List_of_applications#Terminal_emulators)
-   [Comprehensive Linux Terminal Performance Comparison | Martin Ankerl
    ](http://martin.ankerl.com/2007/09/01/comprehensive-linux-terminal-performance-comparison/)
    _2007_

The terminal with smaller footprint are built whithout the desktop rendering libraries
like GTK or KDE. They directly bind to libx11 or libwayland.

When you want support for complex scripts you need a
layout library like {{< wp "pango" >}} for GTK or libxrender1 for qt.

The new GTK3 or QT6 terminals can be used in both X11 and Wayland.


# X11 terminals
Even if we look for a simple support of unicode our choice reduce to
{{< iref "#xterm" "xterm" >}}, {{< iref "#st" "st" >}},
{{< iref "#rxvt" "rxvt-unicode" >}}, _mlterm_.

The smaller foot print are for  {{< iref "#xterm" "xterm" >}}, {{< iref "#st" "st" >}},
{{< iref "#rxvt" "rxvt" >}}.

 The footprints of _xterm_ are 9.5M resident with 5.6M shared, for _st_
it is 7.3M/6.3M. This has not changed between {{< iref "#oldtest" "old test (1)" >}}
and {{< iref "#newtest15" "new 2015 test (2)" >}}.

There are many web applications to help to configure
{{< iref "desktop#color_themes" color themes  >}} for xterm, st or other terminal
emulators that don't have a graphic interface to configure colors.

You can use
[4bit Terminal Color Scheme Designer](http://ciembor.github.io/4bit/).


## xterm {#xterm}
The standard X {{< wp "terminal emulator" >}} is
[xterm](http://invisible-island.net/xterm/xterm.html).
-   [ArchWiki: xterm](https://wiki.archlinux.org/index.php/Xterm)
-   [list of xterm control sequences
    ](http://invisible-island.net/xterm/ctlseqs/ctlseqs.html).

## St {#st}
[suckless st](http://st.suckless.org/),
is intended to serve as a lightweight replacement for {{< iref "#xterm" "xterm" >}} or
rxvt-unicode. It currently supports 256 colors, most VT10X escape sequences, UTF-8, X11
copy/paste, anti-aliased fonts (using fontconfig), fallback fonts, resizing, shortcuts
via config.h, and line drawing. The configuration is explained in
[Archwiki: st](https://wiki.archlinux.org/index.php/St).
There is also a fork for Wayland named {{< iref "#wterm" "wterm" >}}.
In Debian _st_ is packaged a _stterm_.

One benefit of _st_ over _xterm_ is the support of fontconfig and
24bits colour scheme. So it matches the
[powerline terminal requirements
](https://powerline.readthedocs.org/en/latest/usage.html#terminal-emulator-requirements).

## rxvt and friends
There are also
a lot of alternate terminals like {{< wp "rxvt" >}},
[rxvt-unicode](https://wiki.archlinux.org/index.php/Rxvt-unicode)
[eterm](http://www.eterm.org) _replaced by terminology_,
[mrxvt](http://materm.sourceforge.net/wiki/pmwiki.php) _stopped in
2008_,
_wterm_ Wterm is a fork of rxvt designed for  Window Maker, it is distinct from the
homonym Wayland terminal {{< iref "#wterm" "wterm" >}}.


[mlterm](http://mlterm.sourceforge.net/) _active in 2019_ is a
multilingual terminal with support for input-methods.


# List of  vte terminal emulators {#vte}
<a name="vte"></a> [vte](https://live.gnome.org/Apps/Terminal/VTE) is a library for
terminal emulators build upon gtk3, pango, libatk,libcairo2...

It is desktop agnostic, as it doesn't depend directly on Xorg, and is also available on
Wayland it can even be compiled against directfb. A bunch of terminal emulator use this
__libvte__ library and they add their on dependencies they all share some common
characteristics comming from __libvte__, and can use multiple tabs, some uses a single
server for multiple windows.

Most of them have support for UTF-8 , tabbing,
coloring and reordering tabs, manage tabs through keybindings,
user profile, hiding menu bar, optional toolbar.

Vte includes pango so it can display {{< wp "OpenType" >}}  fonts.

The heavier terminals usually have strong binding with a desktop like
gnome, xfce, KT some lighter terminals are also build on _vte_ but rely
only on Gtk and xfreedesktop and avoid heavy desktop bindings like:


-   [evilvte](http://www.calno.com/evilvte/) (GPL)
    a light {{< iref "#vte" "vte" >}} terminal, but you have to
    recompile it to change the configuration. _It is no more
    developped since 2013 and no more in debian_
-   <a name="gnome-terminal"></a>{{< wp "gnome terminal" >}} (GPL)  build
    upon {{< iref "#vte" "vte" >}}
    with gnome dependencies but not too heavy (no gnome specific
    daemon) since they have adopted dbus and dropped bonobbo. It has
    a detailed preference menu with full profile support. It was a
    very heavy terminal compared to others when launched, but now it
    is lighter than many. Gnome Terminal or its fork
    {{< iref "#mate" "Mate Terminal" >}}
    are a good choice for a vte terminal supporting dbus, pango and
    advanced preferences.
    33M res / 25M shr {{< iref "#newtest17" "3" >}}. _in
    Debian_.
    -   [Gnome Terminal Help
        ](https://help.gnome.org/users/gnome-terminal/stable/index.html.en)
    -   [gnome-terminal-colors-solarized
        ](https://github.com/Anthony25/gnome-terminal-colors-solarized)
        script to set the Solarized color set with Gnome Terminal.
    -   [askununtu - How can I create a “built-in” color scheme for
        GNOME Terminal?
        ](https://askubuntu.com/questions/218930/how-can-i-create-a-built-in-color-scheme-for-gnome-terminal/236229)
-   [Guake](https://github.com/Guake/guake)
    is a python based drop-down terminal,similar to Yakuaka (KDE)
    and Tilda, but programmed in python for the GNOME Desktop.
    Footprints: 49M / 32M shr {{< iref "#newtest17" "3" >}}.
    _in Debian_.
    -   [ArchWiki: Guake](https://wiki.archlinux.org/index.php/Guake)
-   [lilyterm](http://lilyterm.luna.com.tw/) (GPL)
    a terminal with easy and complete configurations options, it
    supports multiple profiles and dbus._in Debian_.
    Memory footprints:  34M / 28 M shr
    {{< iref "#newtest17" "3" >}}
-   [lxterminal](http://lxde.org) (GPL) from lxde which is quite light.
    but with a very limited configuration menu.  We can change the
    foreground and backgroun colour but I found no way of customizing
    colour scheme, it is confirmed by [Ubuntu Help
    ](https://help.ubuntu.com/community/Lubuntu/Documentation/LXTerminal/Customising)
    even if the lxde wiki page state this is a feature of lxterminal.
    23M / 19M shr {{< iref "#newtest17" "3" >}}.<br />
    The lxterminal process act as a server so whenyou launch a new
    instance you reuse the same process for a new window, but compared
    to the other dbus powered applications it seems you have no way to
    move a tab from a window to an other, or specifying from the
    command line to reuse an open window.<br />
    Compared to gnome-terminal you have lighter footprint but no
    profile preferences nor the possibility to launch new tabs through
    dbus.
-   <a name="mate-terminal"></a>__Mate Terminal__ (GPL)
    is a fork of
    {{< iref "#gnome" "Gnome Terminal" >}}
    for the [Mate Desktop](http://mate-desktop.org/) and have the same
    charecteristics, its memory footprint seems slightly lighter
    33M / 25M shr {{< iref "#newtest17" "3" >}},
-   [mt](https://github.com/mutantturkey/mt/) (GPL) is a fork of
    _sakura_,
-   [Pangoterm](http://www.leonerd.org.uk/code/pangoterm/)
    A GTK/Pango-based terminal that uses
    [libvterm](http://www.leonerd.org.uk/code/libvterm/)
    an abstract C99 library which implements a VT220 or xterm-like
    terminal emulator without using any particular graphics toolkit or
    output system. _It does not seems to be anymore developped since
    2015 but is in debian experimental_<br/>
    Memory footprints: 18M res. / 16M shared {{< iref "#newtest15" "(2)" >}}.
-   [roxterm](http://roxterm.sourceforge.net/) (GPL) heavier than
    lxterminal but easier to customize, it allows colour schemes.
    It is no more developped since 2016, and no more available in Debian.
-   [Sakura](http://www.pleyades.net/david/projects/sakura) (GPL),
    has many tabs and configurable keybindings,  a
    contextual menu with some basic options but no preference profile.
    Footprints: 24M res / 27M shr {{< iref "#newtest17" "3" >}},
    _in Debian_
    -   [Sakura launchpad page](https://launchpad.net/sakura)_
-   [terminator](http://www.tenshu.net/p/terminator.html) build upon
    _python-vte_ arrange many {{< iref "#vte" "vte" >}}
    terminals in a grid. It has advanced customizable profile options,
    you can change the size, colour, give different shapes to the
    terminal.  With the embedded python it is has large memory
    footprints, but as you probably have some python app running in
    your desktop (look under ibus the gtk ui!)  some libraries are
    probably truly shared. _in debian_ It is quite big since it embeds
    python-vte terminator 55M / 33M shr
    {{< iref "#newtest17" "3" >}}.
-   [Termit](http://github.com/nonstop/termit/wiki) (GPL)
    has many tabs and configurable keybindings, it allows switching
    encodings, sessions, and embedded Lua. _in debian_<br/>
    It has configurable colors and font by tab but no _profile_
    notion. It has no command line option to reuse a window process,
    every call from the command line open a window in a new process,
    and so you cannot move a tab from a window to an other
    window. _in Debian_<br/>
    Memory footprints: 34M/26M {{< iref "#newtest17" "3" >}}
    for 2 tabs.
-   [Termite](https://github.com/thestinger/termite)
    [Archwiki: Termite](https://wiki.archlinux.org/index.php/Termite)
    is a minimal {{< iref "#vte" "vte" >}} terminal emulator
    designed for use with tiling window managers. It has a similar
    look and feel to rxvt-unicode.
-   [Tilda](https://github.com/lanoxx/tilda) is a drop down
    terminal,  it can be pulled up and down from the top of the screen
    with a special hotkey _default F1_.
    It has a customizable colour shemes.
    There is a {{< wp "Tilda_(software)"  "Wikipedia page" >}}.
    Footprints: 44M / 29M {{< iref "#newtest17" "3" >}},
    _in Debian_
    -   [ArchWiki: Tilda](https://wiki.archlinux.org/index.php/Tilda)
-   [xfce-terminal](http://www.xfce.org/projects/terminal/) (GPL)
    _xfce dependencies_, _in debian_

A list of {{< iref "#vte" "vte" >}} terminals is on the
[evilvte Home Page](http://www.calno.com/evilvte/) along with a
comparison of dependencies and binary sizes _wich is not so much a
criteria as it is quite disconnected from the true memory footprint of
the application._.

I made some <a name="oldtest">older test (1)</a>, with terminal with
two open tabs running the bash shell; and a
<a name="newtest15">new test in 2015 (2)</a>  and
checked in <a name="newtest17">2017 (3)</a>
the new measurement report
gives for most pieces of software an increased memory footprint.

All light terminals have comparable footprints 15M resident 10M shared
{{< iref "#oldtest" "old test (1)" >}} with only one tab;
we can expect if we use a Gtk desktop that a big ratio of
the shared libraries are truly shared. Adding a new tab add only 1M
_of course without adding memory footprint of the shell you launch in
the tab!_. If we go in details for 2 tabs for the {{< iref "#oldtest" "old test (1)" >}} terminator use 40M since it
embeds python-vte; tilda, roxterm, gnome terminal use 16-18M, lilyterm
and sakura 14M lxterminal and evilvte 12M.

For the  {{< iref "#newtest15" "new test (2)" >}} or
{{< iref "#newtest17" "3" >}}:
gnome-terminal 33M res / 25M shr {{< iref "#newtest17" "3" >}},
guake 49M / 32M shr {{< iref "#newtest17" "3" >}},
lilyterm 34M / 28M shr {{< iref "#newtest17" "3" >}},
lxterminal  24M / 20M shr {{< iref "#newtest17" "3" >}},
mate-terminal 42M / 30M shr {{< iref "#newtest17" "3" >}},
pangoterm 18M res. / 16M shared.
qterminal 34M / 29M shr {{< iref "#newtest17" "3" >}},
roxterm 21M res / 14M shr {{< iref "#newtest17" "3" >}},
sakura 24M res / 27M shr {{< iref "#newtest17" "3" >}},
st 7.7M/6.7M {{< iref "#newtest17" "3" >}},
terminator 55M / 33M shr {{< iref "#newtest17" "3" >}},
terminology 27.5M/18.6M {{< iref "#newtest15" "2" >}},
termit 21M/18M {{< iref "#newtest15" "2" >}} 34M/26M
{{< iref "#newtest17" "3" >}},
tilda 44M / 29M {{< iref "#newtest17" "3" >}},
xterm 9.7M/5.8M {{< iref "#newtest17" "3" >}}.

Some terminal emulators like _Roxterm_, _gnome terminal_,
_mate terminal_, _terminator_, _guake_, _lilyterm_
have dbus support, and allow to launch a new tab or a new window in
the same process from the command line and move tabs between windows.

Other terminal emulators open a new process for each window, of course they
support multiple tabs, but it seems they need to be opened from the
window.

[tdrop](https://github.com/noctuid/tdrop/) (BSD License)
is a bash script to allow dropdown for a an independent terminal, it is also
WM-Independent. _tdrop_ is compatible with many terminal software and window managers.

# Wayland Terminals {#wayland_terminals}

See also the {{< iref "xorg#wayland" "Wayland Section" >}},
{{< iref "desktop#wayland_compositors" "Wayland Compositors" >}}.


-   [foot](https://codeberg.org/dnkl/foot) (MIT License)
    -   [foot Wiki](https://codeberg.org/dnkl/foot/wiki)
    fast, lightweight and minimalistic Wayland terminal emulator.
-   [wterm](https://github.com/majestrate/wterm) (MIT Licee)
    is an _st_ fork for wayland.

## Terminals that work on both Wayland and X11
The {{< iref "#vte" "VTE Terminals" >}} as well of all terminals based on GTK3, GTK4, QT5,
QT6 don't depend on Xorg and can run on both Xorg and Wayland.


-   [Alacritty](https://github.com/alacritty/alacritty) (Apache License)
    A Rust cross-platform, GPU-accelerated terminal emulator, with a strong focus on
    performance.  Wayland is also supported.

    Many {{<  iref "desktop#color_themes" "color themes" >}} are available for
    _Alacritty_.:

    /In 2022 Alacritty 0.8.0 crash in sway wayland./

    In 2022 there is no recent Debian package for alacritty 0.8.0 and 0.11.O crash in
    sway wayland. There is an
    [alacritty-debian repository](https://github.com/barnumbirr/alacritty-debian)
    which gives new package releases.

    -   [Alacritty features
        ](https://github.com/alacritty/alacritty/blob/master/docs/features.md)
    -   [Alacritty Ubuntu PPA](https://launchpad.net/~mmstick76/+archive/ubuntu/alacritty)
        is [not up to date with last releases
        ](https://github.com/alacritty/alacritty/pull/3983).
    -   The POP_OS fork add a [debian package configuration
        ](https://github.com/pop-os/alacritty/tree/master/debian).

-   [Kitty](https://sw.kovidgoyal.net/kitty/) (GPL)
    a scriptable OpenGL based terminal emulator with tiling capabilities, TrueColor,
    ligatures support and protocol extensions for keyboard input and image rendering.

    I tried in 2020 Kitty on Linux X11, but it let my window manager, in an
    unrecoverable state. In 2022 kitty works well in Wayland; it uses 4.5M resident /
    3.0M shared.

    The [Kitty Page](https://sw.kovidgoyal.net/kitty/) has configuration and usage
    documentation.

-   The Kde/Qt terminal is {{< wp "Konsole" >}} it has heavy KDE dependencie.

-   <a name="qterminal"></a>[qterminal](https://github.com/lxqt/qterminal/)
    is a light Qt terminal which is part
    of [lxqt](https://lxqt.org/) The Lightweight Qt Desktop Environment (previously
    _Razor-qt_) It has no dependencies but its own qtwidget library and use on
    X11 34M / 29M shr {{< iref "#newtest17" "3" >}} with 2 tabs.

    You can have multiple tabs but it does not allow to share a process
    between multiple windows

-   [Terminology](https://www.enlightenment.org/about-terminology)
    is a terminal emulator created for the Enlightenment desktop.  it allows: Multiple
    copy and paste selections, multiple tabs and split into multiple panes, inline
    display of link content, to preview thumbnails of images, videos and documents A
    unique feature is its ability to work in X11, Wayland and directly in the Linux
    framebuffer (fbcon).  It is usable out of Enlightenment desktop, but its
    installation will pull all the enlightenement libraries.
    -   [GitHub: Terminology](https://github.com/billiob/terminology)
    -   Terminology uses 27M resident memory / 17 shared.
    -   Wikipedia: {{< wp "terminology" >}}

-   [Wayst](https://github.com/91861/wayst)
    is a simple terminal emulator for Wayland and X11 with OpenGL rendering and minimal
    dependencies (OpenGL, fontconfig, freetype).


# Javascript Terminals
-   [terminal javascript Library](http://www.masswerk.at/termlib/)
    (ad-hoc open source license) provides terminal capabilities from a
    browser.
-   [xwiterm](https://code.google.com/p/xwiterm/) (GPL)
    a web terminal to login to your remote account.
    It has the possibility to execute commands that needs user interaction,
    like "sudo su", because the emulator waits for the user input.
-   [ajaxPHPterm](http://sourceforge.net/projects/ajaxphpterm/) (GPL)
    is an AJAX terminal/shell emulator for PHP, based on the PHPterm project.
    _I could not make v 1.0 work_.
-   [PHP shell terminal](http://sourceforge.net/projects/phpterm/) (GPL)
    a terminal/shell emulator for PHP.
-   [Shell Commander](http://sourceforge.net/projects/shcmd/) a PHP script,
    that allows remote execution of shell commands as the  web user.
-   [Tiny Shell](http://sourceforge.net/projects/tiny-shell/) (MIT License)
    PHP-based Ajax-terminal with a special
    [concern about security](http://www.5p.dk/tinyshell/docs/security/).
    TinyShell comes with a native MySQL command line client.
-   [Anyterm](http://anyterm.org/) (GPL) is a combination of a
    Javascript web page and a process that runs on your web server
    that provides shell access.
-   [Ajaxterm](https://github.com/antonylesuisse/qweb/tree/master/ajaxterm)
    (Public Domain parts are LGPL) is a web based terminal similar to
    _anyterm_ but the server is written in Python.
-   [web-console](http://www.web-console.org/) (GPL) is an ajax-perl web console.
-   [Gate One](http://liftoffsoftware.com/Products/GateOne) (AGPL)
    is a javascript and HTML5-powered terminal emulator and SSH
    client. It is multi-user and multi-session, emulates xterm, can be
    interrupted and restarted It supports multiple method of
    authentication, SSL and TLS encryption, logging, IPV6 prorocol.
    -   [GitHub:Gate One](https://github.com/liftoff/GateOne)

# Ansi Code support

Most terminals, both console and X support {{< wp "ANSI escape code" >}}
and characters color. While the console support 16 colors, X terminals
like eterm, gnome terminal, Konsole,  guake, nautilus terminal,
terminator, xfce4 terminal, st (called also stterm), xterm, and all
{{< iref "#vte" "vte" >}} terminals support 256 colors.

For xterm _the reference for control codes_ the color modifying control sequence are
described among the [Functions using CSI - Xterm ctlseqs)
](https://invisible-island.net/xterm/ctlseqs/ctlseqs.html#h3-Functions-using-CSI-_-ordered-by-the-final-character_s_)
they are the CSI sequences ending with `m`.

There are lists of ansi escape sequences in [ascii-table
](http://ascii-table.com/ansi-escape-sequences.php), in
[bash-hackers: terminal codes
](http://wiki.bash-hackers.org/scripting/terminalcodes)
and another in [vtansi](http://www.termsys.demon.co.uk/vtansi.htm);
and the [list of xterm control sequence (invisible-island.net)
](http://invisible-island.net/xterm/ctlseqs/ctlseqs.html).

For exemple of code and a listing of color codes look at
{{< wp "ANSI escape code"  "XWikipedia: ANSI escape code" >}}
and [Bash tips: Colors and formatting
](http://misc.flogisoft.com/bash/tip_colors_and_formatting).

The ArchWiki [Prompt customization - ANSI_escape_sequences
](https://wiki.archlinux.org/index.php/Bash/Prompt_customization#ANSI_escape_sequences)
describe also their use in shell.

In 256-color mode the color-codes are the following:
-   `0x00-0x07`:  standard colors (as in `ESC [ 30–37 m`)
-   `0x08-0x0F`:  high intensity colors (as in `ESC [ 90–97 m`)
-   `0x10-0xE7`:  6 × 6 × 6 = 216 colors: 16 + 36 × r + 6 × g + b (0 ≤ r, g, b ≤ 5)
-   `0xE8-0xFF`:  grayscale from black to white in 24 steps

## Operating System Command (OSC) {#osc}

Xterm supports also [OSC ctlseqs
](https://invisible-island.net/xterm/ctlseqs/ctlseqs.html#h3-Operating-System-Commands)

Among them the OSC 52 code allow to manipulate selection data and the clipboard, primary,
secondary, select, or cut-buffers.
It may be used to communicate between tmux or vim selection and the clipboard, or to use
a remote clipboard in ssh.

The support of OSC 52 in terminals is given in [vim oscyank Readme
](https://github.com/ojroques/vim-oscyank) in June 2022 it is:

| Terminal | OSC52 support |
|----------|:-------------:|
| [Alacritty](https://github.com/alacritty/alacritty) | **yes** |
| [foot](https://codeberg.org/dnkl/foot) | **yes** |
| [GNOME Terminal](https://github.com/GNOME/gnome-terminal) (and other VTE-based terminals) | [not yet](https://bugzilla.gnome.org/show_bug.cgi?id=795774) |
| [hterm (Chromebook)](https://chromium.googlesource.com/apps/libapps/+/master/README.md) | [**yes**](https://chromium.googlesource.com/apps/libapps/+/master/nassh/doc/FAQ.md#Is-OSC-52-aka-clipboard-operations_supported) |
| [iTerm2](https://iterm2.com/) | **yes** |
| [kitty](https://github.com/kovidgoyal/kitty) | **yes** |
| [Konsole](https://konsole.kde.org/) | [not yet](https://bugs.kde.org/show_bug.cgi?id=372116) |
| [QTerminal](https://github.com/lxqt/qterminal#readme) | [not yet](https://github.com/lxqt/qterminal/issues/839)
| [screen](https://www.gnu.org/software/screen/) | **yes** |
| [st](https://st.suckless.org/) | **yes** (but needs to be enabled, see [here](https://git.suckless.org/st/commit/a2a704492b9f4d2408d180f7aeeacf4c789a1d67.html)) |
| [Terminal.app](https://en.wikipedia.org/wiki/Terminal_(macOS)) | no, but see [workaround](https://github.com/roy2220/osc52pty) |
| [tmux](https://github.com/tmux/tmux) | **yes** |
| [Windows Terminal](https://github.com/microsoft/terminal) | **yes** |
| [rxvt](http://rxvt.sourceforge.net/) | **yes** (to be confirmed) |
| [urxvt](http://software.schmorp.de/pkg/rxvt-unicode.html) | **yes** (with a script, see [here](https://github.com/ojroques/vim-oscyank/issues/4)) |
| [xterm.js](https://xtermjs.org/) (Hyper terminal) | [not yet](https://github.com/xtermjs/xterm.js/issues/3260) |
| [wezterm](https://github.com/wez/wezterm) | [**yes**](https://wezfurlong.org/wezterm/escape-sequences.html#operating-system-command-sequences) |

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
