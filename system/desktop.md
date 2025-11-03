---
title: Linux Desktops
---

The lower level is {{< iref "xorg" "Xorg and Wayland" >}}

In the {{< iref "dbus" "Dbus Section" >}} you find the
{{< iref "dbus#dbus_notification" "notification daemons" >}}.

See also the section {{< iref "file_managers" "File Managers" >}},
{{< iref "xterminals" "X Terminals" >}},
{{< iref "#desktop_components" "Desktop components" >}}.

<!-- [[file:../../../../content-org/notes/system_notes/desktop_notes.org][Desktop Notes]] -->
--------------

# Desktop environments {#desktop_environments}

A {{< wp "Desktop environment" >}} refers to a style of graphical user interface and
also to a common set of libraries ({{< wp "Widget library" >}}) used to build the
desktop components.

Presently most desktop environment use either {{< wp "Qt_(framework)"  "QT" >}} or
{{< wp "GTK+" >}}, they include various
{{< iref "#desktop_components" "desktop components" >}}, mainly
a {{< iref "#window_manager" "window manager" >}}
and a {{< iref "#file_manager" "file-manager" >}}.

Some [window manager](#window_manager "internal reference") are inseparable
from the desktop environment they use as _i3_, _fluxbox_, _awesome_
and many light window manager. You will find an entry for them in the
{{< iref "#window_manager" "window manager section" >}}

You find a nice [comparison of memory footprints of  light linux desktops
](http://l3net.wordpress.com/lightweight-linux/)  in
[layer3 networking blog](http://l3net.wordpress.com/).

Wikipedia {{< wp "Comparison of X Window System desktop environments" >}}
gives also some information on the size of each-one.

-  Archwiki:
   [Desktop environment](https://wiki.archlinux.org/title/Desktop_environment),
   [Comparison of desktop environments](https://wiki.archlinux.org/title/Comparison_of_desktop_environments)

## Main stream desktop environment

They are called _full desktop environment_
but we should call most of them _greedy_ as they eat 80% of the resources of you machines.
I don't use them so this list is brief.

-   {{< wp "KDE" >}} and {{< wp "KDE Software Compilation" >}}.
    [ArchLinux: KDE](https://wiki.archlinux.org/index.php/KDE)
-   {{< wp "GNOME" >}} there is the older Gnome2 and the newer Gnome3, look at
    {{< wp "GNOME"  "Wikipedia" >}} to learn about the differences and
    {{< wp "Controversy over GNOME 3" >}}.
    [ArchLinux: GNOME](https://wiki.archlinux.org/index.php/GNOME)
-   {{< wp "Unity" >}} is a shell interface for the GNOME desktop environment developed by
    Canonical Ltd for its Ubuntu operating system.
    [ArchLinux:Unity](https://wiki.archlinux.org/index.php/Unity)
-   {{< wp "MATE" >}} is a desktop environment forked from  GNOME 2.
    [ArchLinux: Mate](https://wiki.archlinux.org/index.php/MATE)
-   {{< wp "Cinnamon_(user_interface)"  "Cinnamon" >}}  is a fork of GNOME Shell based
    on the desktop metaphor, like GNOME 2. Cinnamon uses  as window manager _Muffin_,
    a fork of the GNOME 3 window manager _Mutter_.
    [ArchLinux: Cinnamon](https://wiki.archlinux.org/index.php/Cinnamon)

##  Xfce {#xfce}

[Xfce](http://en.wikipedia.org/wiki/Xfce "Wikipedia: Xfce") (GPL and LGPL) is a
desktop, which aims to be thinner and faster than gnome/kde, still
conforming to freedesktop platform. xfwm4 weight 6.5M resident,
xfce4-panel 8.8M, xfdesktop 8.5M, xftaskbar4 6.3M, xfce-mcs-manager
4.3M, xfce4-session 4.2M, and the file manager thunar 11M; of
course we cannot sum up these because there is shared memory, if
you add thunar on the top of a whole xfce session, you add only 5M
out of 10M because half of the resident size is truly shared (6.8
is sharable), a whole xfce session (without thunar) amount to 20M
on my computer. xfce4 is not so small than it aims to be.

-   [xfce Home](http://www.xfce.org/ "xfce.org Home") (GPL and LGPL)
-   [ArchWiki: Xfce](https://wiki.archlinux.org/index.php/Xfce)

## LXDE  {#lxde}

{{< wp "LXDE" >}} (GPL and LGPL) is a lightweight desktop environment for
Unix. It uses  the GTK+ toolkit. The components of lxde are not
strongly bound with a common library set as in KDE, Gnome or Xfce.
The standard component include the  window manager
{{< iref "#openbox" "Openbox" >}}, the session manager
{{< iref "#lxsession" "lxsession" >}}, the panel {{< iref "#lxpanel" "lxpanel" >}}
and the file manager {{< iref "file_managers#pcmanfm" "PCManFM" >}})
_but you are free to use an other one_.

Since the author of LXDE switched to LXQT, this distribution is still maintained but no
longer evolving.

-   [LXDE Home](https://lxde.github.io/)
-   [LXDE Wiki](http://wiki.lxde.org/en/Main_Page)
-   [LXDE - GitHub](https://github.com/lxde)
-   [ArchLinux: LXDE](https://wiki.archlinux.org/index.php/LXDE)
-   [LXDE - Debian Wiki](https://wiki.debian.org/LXDE)
-   [Gentoo: XDE](https://wiki.gentoo.org/wiki/LXDE)
-   [Knoppix](http://knoppix.net/) - live CD with LXDE
-   [Lxde-Openbox Guide](http://lxlinux.com/index.html)has a lot
    information on configuration of all components of lxde.
-   <a name= "lxsession"></a>[lxsession](http://wiki.lxde.org/en/LXSession) is the
    standard session manager for LXDE, it has minimal footprints 1.7M resident/1.4M
    shared. But if you want to manage yourself the session you can dispense with it and
    use a simple launcher as _fbautostart_.
-   <a name= "lxpanel"></a>[LXPanel](https://wiki.lxde.org/en/LXPanel)
    is the standard panel of LXDE, it can generate a menu from _.desktop_ files. It can
    be configured from a GUI preferences dialog, and has theming support via custom
    gtkrc file.

## LXQt {#lxqt}
LXQt was started by the author of LXDE to replace it; so all development take place on
LXQt project since 2013. It is a merge of LXDE an Razor-Qt. It is composed by many
applications written in Qt-5 and will gradually become compatible with Wayland.

-   Wikipedia: {{< wp "LXQt" >}} _look here for the application list._
-   [LXQt Home](https://lxqt-project.org/).
-   [LXQt - GitHub](https://github.com/lxqt)
-   [LXQt Wiki](https://github.com/lxqt/lxqt/wiki)
-   [LXQt - Debian Wiki](https://wiki.debian.org/LXQt)
-   {{< iref "distributions#lubuntu" "Lubuntu" >}} is the LXQT flavor of Ubuntu.
-   [LXQt - ArchWiki](https://wiki.archlinux.org/index.php/LXQt)
-   [LXQt - Gentoo Wiki](https://wiki.gentoo.org/wiki/LXQt)


LXQT is composed of many applications, the current list is on
{{< wp "LXQt" "Wikipedia" >}}. Some are independent of the desktop:
{{< iref "xterminals#qterminal" "qterminal" >}}, Falkon, sddm  _Simple Desktop Display
Manager_, lximage-qt, {{< iref "file_managers#pcmanfm-qt""pcmanfm-qt"  >}}.

LXQT is the core of {{< iref "distributions#lubuntu" "Lubuntu distribution" >}}.

# Window managers {#window_manager}

See also the the
{{< iref "#desktop_environments" "Desktop environment" >}} and
{{< iref "#desktop_components" "Desktop Components Page" >}}

-   Wikipedia {{< wp "Comparison of X window managers" >}} gives the characteristics:
    Language, License, Type (stacking/dynamic/tiling), Configurable
    titlebar buttons, Graphical configuration, Hotkeys,	ICCCM/EWMH
    compliant, Panel for window switching, Tabbed windows,
    Themeable.

    The light window managers are also compared with full environments
    in the {{< wp "Comparison of X Window System desktop environments" >}}.
-   [ArchWiki - Window manager](https://wiki.archlinux.org/index.php/Window_manager)
-   [ArchLinux list of Window Managers
    ](https://wiki.archlinux.org/index.php/Window_Manager)
-   [ArchLinux Comparison of Tiling Window Managers
    ](https://wiki.archlinux.org/index.php/Comparison_of_Tiling_Window_Managers)
-   [Matchbox](https://www.yoctoproject.org/tools-resources/projects/matchbox)
    is a base
    environment for the X Window System running on non-desktop embedded
    platforms. Matchbox is now part of the
    [Yocto Project](https://www.yoctoproject.org/) that provides tools
    to create custom Linux-based systems for embedded products.

-   {{< wp "Compiz" >}} is a {{< wp "Compositing window manager" >}} that can be used
    with gnome or KDE.
    - [Compiz Home](http://www.compiz.org/).
    - [Phoronix: The Cost Of Running Compiz](http://www.phoronix.com/scan.php?page=article&item=compiz_speed_test).
    -   [Gentoo Compiz Fusion HowTo](http://en.gentoo-wiki.com/wiki/Compiz-Fusion)
-   {{< wp "Mutter" >}} is a {{< wp "Compositing window manager" >}}
    and the standard window manager for Gnome.
    -   [Phoronix: Mutter Can Cause A Gaming/OpenGL Performance Hit Too
        ](http://www.phoronix.com/scan.php?page=article&item=mutter_composite_hit)

## EWMH {#ewmh}
The
[Extended Window Manager Hints (EWMH) specification
](http://standards.freedesktop.org/wm-spec/latest/)
is the freedesktop standard API to interact with a window manager.
This specification complete the
{{< wp "inter-Client_Communication_Conventions_Manual"  "Inter-Client Communication Conventions Manual (ICCCM)" >}},
which defines window manager interactions at a lower level.

The [wmctrl page](http://tripie.sweb.cz/utils/wmctrl/)
and the {{< wp "EWMH"  "Wikipedia EWMH page" >}} give some window managers that
implement EWMH _aewm, awsome, blackbox, bspwm, compiz, edwm,
enlightenment, evilwm, fluxbox, fvwm, i3, icewm, interfacewm, jwm,
kwin, matchbox, metacity,openbox, pekwm, penbox, sawfish, spectrwm,
waimea, wmfs, window maker, wmii, xmonad, xfce, xfwm_

Some window managers  do not implement
EWMH _ratpoison, ion, pwm, evilwm, flwm, windowlab, ctwm_. Of course
this incomplete list is subject to change with new releases.

The window managers that are EWMH compliant are also
{{< wp "inter-Client_Communication_Conventions_Manual"  "ICCCM" >}} compliant
as it is the base of EWMH. You can find on line the
[ICCCM specification](http://tronche.com/gui/x/icccm/).

See also the {{< iref "#wm_control" "WM Control" >}} subsection.


## Low resource tiling and dynamic Window Managers {#tiling_wm}
_ArchWiki_ has a [Comparison of tiling window managers
](https://wiki.archlinux.org/index.php/Comparison_of_tiling_window_managers).

A tutorial to desktop configuration with tiling wm:
[Home Sweet Home](http://blog.z3bra.org/2013/10/home-sweet-home.html)
with sections on the
[windows bars](http://blog.z3bra.org/2014/04/meeting-at-the-bar.html),
[popup notifications](http://blog.z3bra.org/2014/04/pop-it-up.html),
[colors settings](http://blog.z3bra.org/2015/06/vomiting-colors.html).

There is also a _uncomplete and not up to date_ [Tutorial index on reddit r/unixporn
](https://www.reddit.com/r/unixporn/wiki/links/external).

-   [Awesome](http://awesome.naquadah.org/)
    _active project_,
    a framework dynamic window manager which follows Freedesktop
    standards, {{< iref "#ewmh" "EWMH compiliant" >}},
    and is extensible using Lua. It is packaged in Debian.
    -   [Alberto Pettarin: awesome is awesome!
        ](http://www.albertopettarin.it/blog/2015/07/07/awesome-is-awesome.html)
-   <a name="dwm"></a>[dwm](http://dwm.suckless.org/)
    is a minimalistic window manager. It manages windows in tiling,
    monocle -i.e. stacked_ and floating modes. It is part of the
    [suckless software](http://dwm.suckless.org/) and is packaged in
    Debian.

    There is also a derivative aimed to the console terminal
    {{< iref "console#dvtm" "dvtm" >}}.
-   {{< iref "#i3_wm" "i3" >}} has its own section.
-   {{< wp "larswm" >}} _last release 2004_ a dynamic, tiling window manager
    following _9wm_ model. It is _(yet)_ packaged in Debian.
-   [RatPoison](http://www.nongnu.org/ratpoison) (GPL)
    is a simple light window manager with nographics, no window
    corations, and no mouse/touchscreen/touchpad dependence.  All
    interaction with the window manager is done through keystrokes.
    <br/>
    The screen can be split into non-overlapping frames. All
    windows are kept maximized inside their frames.
        - {{< wp "Ratpoison"  "Wikipedia Ratpoison page" >}}
        - [RatPoison manual](http://www.nongnu.org/ratpoison/doc/)
        - [ArchLinux RatPoison tutorial](http://wiki.archlinux.org/index.php/Ratpoison)
        - [Gentoo Ratpoison HowTo](http://en.gentoo-wiki.com/wiki/Ratpoison)
-   [wmii](http://wmii.suckless.org/) is a dynamic window manager for X11,
    which is highly customizable via scripts and
    usable with keyboard and mouse. It supports conventional, tabbed and tiled
    window management with low memory usage. It is the predecessor of
    {{< iref "#i3_wm" "i3" >}}

## Low resource Stacking WM

-   [aewm++](https://github.com/frankhale/aewmp) (MIT License)
    _active project packaged in Debian_ is a minimal window manager, based on aewm which
    stopped in 2007,  but written in C++.
    -   aewm++ contains desktop utilities packaged in Debian as aewm++-goodies, an
        apllication bar, a panel, and a session manager.
        It is {{< iref "#ewmh" "EWMH compliant" >}}.
-   [evilwm](http://evilwm.sourceforge.net/) (Artistic licence)
    _active project in 2022_, A minimal keyboard driven window manager. It
    supports {{< iref "#ewmh" "EWMH" >}} and is packaged in
    Debian.
    -   [evilwm git repository](https://www.6809.org.uk/git/evilwm.git/).
-   [Icewm](https://ice-wm.org/) (LGPL)
    a light {{< iref "#ewmh" "EWMH compliant" >}} wm, fully usable with keyboard, with a
    task bar, multiple workspaces and configuration tools _active in 2022_.

    It uses few libraries outside of standard X11, and its own library libice; so its
    real footprint is quite low: 6.2M resident/4.5M shared without desktop addons
    icewmtray 3M/2.3M, icewmbg 2.7M/2.2M _a background daemon is not mandatory_,
    icewm-session 1.7M/1.3M.
    -   [Gentoo IceWM HowTo](http://en.gentoo-wiki.com/wiki/IceWM)
-   [JWM (Joe's Window Manager)](https://joewing.net/projects/jwm) (GPL)
    _actively maintened in 2022_ is a low resource (half the memory footprint of Fvwm95)
    Window manager using only Xlib and (optionally) the shape extension and libXpm. It
    is said to be one of the window managers with less dependencies, and smaller
    footprints.  It supports {{< iref "#ewmh" "EWMH" >}} and is packaged in Debian.
    -   [jwm - GitHub](https://github.com/joewing/jwm/).
-  [WindowMaker](http://www.windowmaker.org/) (GPL)
    a tiny (1.3M rsz) and fully functional wm. _active in 2021_.
    -   [WidowMaker git repository](https://repo.or.cz/w/wmaker-crm.git)
    -   [dockapps.net](https://www.dockapps.net/) archive of 211 Window Maker dockapps.


## i3 {#i3_wm}

[i3](http://i3wm.org/) (BSD Licence) is a tiling window manager
written in C. It is ewmh compliant. I3 has a dynamic switching to
floating, on an individual window base.

-   [i3 documentation](http://i3wm.org/docs/):
-   [i3 doc](https://github.com/i3/i3/tree/next/docs) contain tools,
    the userguide, the refcard.
    -   [user guide](http://i3wm.org/docs/userguide.html).
-   [i3: IPC interface (interprocess communication)
    ](http://i3wm.org/docs/ipc.html)
-   <a name="i3bar"></a>[i3bar](https://i3wm.org/docs/userguide.html#_configuring_i3bar)
    is a status bar for i3, included in i3 distribution.
    -   [External workspace bars such as i3bar or dzen2](http://i3wm.org/docs/wsbar.html)
-   {{< wp "I3_(window_manager)"  "Wikipedia: I3" >}}
-   [GitHub mirror of i3](https://github.com/mgsnova/i3/)
-   [ArchLinux: I3](https://wiki.archlinux.org/index.php/I3)
-   _I3_ use [i3status](http://i3wm.org/i3status/manpage.html) to generate
     a status line for {{< iref "#i3bar" "i3bar" >}}, dzen2 or {{< iref "#xmobar" "xmobar" >}}.
-   [Lukáš Zapletal’s i3 configuration
    ](http://i3wm.org/docs/user-contributed/lzap-config.html)


The window manager alone uses 5.9M/4.8M, the {{< iref "#i3bar" "i3bar" >}} 5M/4.2M, i3status
1.6M/1.3M.


### i3 tools and scripts {#i3_tools}
-   [i3lock-color](https://github.com/Raymo111/i3lock-color) a color fork of the
    [i3lock](https://github.com/i3/i3lock) lockscreen for i3.
    -   [i3lock-solarized](https://github.com/parsiad/i3lock-solarized)
        Solarized theme for i3lock-color.
-   [GitHub: quickswitch-for-i3](https://github.com/proxypoke/quickswitch-for-i3)
    ( [WFPT Licence](http://sam.zoy.org/wtfpl/COPYING))
    is a python script using _i3-py_ that allows you to quickly switch to and locate
    windows on all your workspaces, using an interactive {{< iref "#dmenu" "dmenu" >}}
    prompt. The last commit is from 2017, there were some forks, but no recent one.
-   [GitHub: i3-wm-scripts](https://github.com/MicahChambers/i3-wm-scripts)
    is a collection of python scripts that contains:
    -   _nextmatch.py_ to jump to a window by matching a title regex.
    -   _nextfind.py_ to jump to a window choosen from a list.
    -   _mark_ to mark a window in a target list, _goto_ to jump to a
        window chhosen from the target list; _unmark_ to delete from
        the list.
-   [GitHub: i3-emacs](https://github.com/vava/i3-emacs) is an emacs
    package for i3-emacs integration. *Last commit 2020*
-   [raiseorlaunch](https://github.com/open-dynaMIX/raiseorlaunch) (MIT License)
    A run-or-raise-application-launcher for i3 window manager.

## Openbox {#openbox}

[Openbox](http://icculus.org/openbox/) is a window-manager with root menu, dock, no
taskbar (use fspanel, fbpanel, pypanel), a configuration management tool named
[obconf](http://icculus.org/openbox/obconf/ "icculus.org obconf").
Openbox is the standard window manager of {{< iref "#lxde" "Lxde" >}}
It can be used with many {{< iref "#file_managers" "file managers" >}}
most often with {{< iref "#pcmanfm" "PCManFM" >}}.

OpenBox use 10M resident memory including 5.5M shared.

-   [LXDE Openbox page](http://wiki.lxde.org/en/Openbox)
-   Gentoo
    [HOWTO Openbox](http://en.gentoo-wiki.com/wiki/Openbox).
-   [An Openbox Guide](http://urukrama.wordpress.com/openbox-guide/) and
    [Openbox Faq](http://urukrama.wordpress.com/openbox-faq/) in
    [Urukrama Web Log](http://urukrama.wordpress.com/)
-   man pages: {{< man "openbox(1)" >}}, {{< man "openbox-session(1)" >}}

## Fluxbox {#fluxbox}

[fluxbox](http://fluxbox.org/) (MIT license) is a small (5.8M resident
4.4M shared) fast and highly configurable window manager, with root
menu, dock (named slit here!), taskbar including the systray, tabbed
windows. The configuration management is integrated, there is also a
powerfull menu generating utility fluxbox-generate\_menu. Fluxbox is a
fork of [Blackbox](http://blackboxwm.sf.net/) and share with it some
[tools](http://bbtools.sourceforge.net/).

Fluxbox doesn't
depends on a specific toolkit and does not use any windowing toolkit
(no gtk/Qt binding) but can be used with any Freedesktop X11 compliant
desktop; as the main program contain everything needed for a window
manager, you have not to use any add-on like systray or panel, it
makes fluxbox one of the lighter window manager. If you need to
compare with openbox you have to add the panel, and may be the systray
if the chosen panel does not include one.

-   The configuration and use
    of fluxbox is described in the _old_
    [Fluxbox Documentation
    ](http://fluxbox.sourceforge.net/docbook/en/html/book1.html)
    and now in the fluxbox wiki.
-   In the[fluxbox wiki](http://fluxbox-wiki.org/) you can find a
    [FAQ](http://fluxbox-wiki.org/index.php?title=FAQ), and a
    [list of HowTos
    ](http://fluxbox-wiki.org/index.php?title=Category:English_howtos)
    in the wiki.
-   In the wiki you find documentation about the fluxbox
    [configurations  files
    ](http://fluxbox-wiki.org/index.php?title=Category:Configuration_howtos)
    :
    -   [init file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_init_file),
    -   [apps file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_apps_file),
    -   [Keys File
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts)
        and [Key Modes
        ](http://fluxbox-wiki.org/index.php?title=Keymodes),
    -   [Menu file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_menu),
    -   [Window Menu
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_windowmenu),
    -   [Startup file
        ](http://fluxbox-wiki.org/index.php?title=Editing_the_startup_file).
    -   [Keyboard shortcuts
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts)
        including [keychains
        ](http://fluxbox-wiki.org/index.php?title=Keyboard_shortcuts#Keychains),

-   [Gentoo: Fluxbox Configuration HOWTO
    ](http://www.gentoo.org/doc/en/fluxbox-config.xml)
-   [Ubuntu community: Fluxbox
    ](https://help.ubuntu.com/community/Fluxbox)
-   [Debian Wiki: Fluxbox](http://wiki.debian.org/FluxBox).
-   [Archwiki: Fluxbox](https://wiki.archlinux.org/index.php/Fluxbox) and
    [ArchWiki: Fluxbox Style Guide
    ](https://wiki.archlinux.org/index.php/Fluxbox_Style_Guide).
    fluxbox also supports [Key modes
    ](http://fluxbox-wiki.org/index.php?title=Keymodes)
-   [Akira's keyfile](http://darkshed.net/files/rcs/fluxbox/keys.html)
    date from 2005 but is still a very complete example.
-   Example of styles:
    [tenr fluxbox style](http://tenr.de/styles/) and
    [tenr Exemple of configuration](http://tenr.de/snippets/),
    [tenr HowTo style fluxbox
    ](http://tenr.de/howto/style_fluxbox/style_fluxbox.html)
-   The development tree is in [git.fluxbox](http://git.fluxbox.org/)
    There are instructions to
    [build fluxbox from source](http://fluxbox-wiki.org/index.php?title=Build_fluxbox_from_source).
-   [fbxdgmenu](pyhttps://bitbucket.org/confluence/fluxbox-tools) is a
    fork of *fluxbox-xdg-menu*, it is a simpler program that only deal
    with menu not the background.
-   You can complete your fluxbox desktops with some other light
    components referenced in the
    {{< iref "#desktop_components" "Desktop components sections" >}}

### Fluxbox configuration

-   local man pages:
    [fluxbox(1)](http://localhost/man/1+fluxbox),
    [fbrun(1)](//man2html.php?1+fbrun),
    [fbsetbg(1)](//man2html.php?1+fbsetbg),
    [fluxstyle(1)](http://localhost/man/1+fluxbox),
    [startfluxbox(1)](/man2/startfluxbox)
-   The config is in `~/.fluxbox/init`
-   For Fluxbox I use the development version as advised on the
    wiki and the FAQ, since the stable version is old and no longer maintained.
-   [Fluxbox: Editing the menu
   ](http://fluxbox-wiki.org/index.php/Editing_the_menu) to generate a new menu:

        fluxbox-generate_menu -h

-   there is (was?) a the script fluxbox-generate-menu is in
    `/usr/share/doc/fluxbox/fluxbox-generate_menu.gz`
-   The user menu is in `~/.fluxbox/usermenu`
-   fluxbox menu editors:
   [fluxmenu](http://sourceforge.net/projects/fluxmenu.berlios/),
   (Fluxbox Menu Editor (fme)](https://github.com/rdehouss/fme) (2009)
   [marchfluxmenu (python)](http://code.google.com/p/marchfluxmenu/) (2007)
   use desktop files found in /usr/share/applications/.
-   On Debian a  debian menu is generated by
    `/etc/menu-methods/fluxbox`,
    it lies in `/etc/X11/fluxbox/` for system and `~/.fluxbox`
     when update-menu is launched by a non-root user. There are 4 files
    `menudefs.hook` the generated menu, `system.fluxbox-menu` the system
    menu, `fluxbox-menu` the concatenation of the two previous, and `menu`
    (prototype named `/etc/X11/fluxbox/fluxbox.menu-user`) the top level
    menu that will include others.
-   I also include a first file named usermenu for the customization.
-   The __fluxbox menu__ ''(right mouse)'' allow to configure the slit.
-   [ubuntuforum:  HOWTO: get a Fluxbox menu (and customization)
    ](http://ubuntuforums.org/showthread.php?t=371144)
-   the apps file allow to customize applications and
    [to tab windows together](http://www.fluxbox.org/features/).
-   fbsetbg relies on chbg,  display, Esetroot, feh,  qiv, hsetroot,
    icewmbg,  wmsetbg, xli xsetbg, xsri,
-   fbdesk needs icons the
    [collection of gentoo bubble icons](http://bubbleicons.tuxfamily.org/)
    is appropriate.

# Wayland compositors {#wayland_compositors}

See also the {{< iref "xorg#wayland" "Wayland Section" >}},
{{< iref "xterminals#wayland_terminals" "Wayland Terminals" >}}.

-   [List of Wayland compositors - ArchWiki
    ](https://wiki.archlinux.org/index.php/Wayland#Compositors)

-   [dwl](https://github.com/djpohly/dwl) (GPL-3)
    dwm clone for Wayland based on wlroots, an hackable compositor.
-   [Enlightenment](https://en.wikipedia.org/wiki/Enlightenment_(software)) (BSD
    License) is a compositing window manager for Xorg or a  since version 20 a Wayland
    compositor.
    -   [Enlightenment Home](https://www.enlightenment.org/)
-   [Greenfield](https://github.com/udevbe/greenfield) (AGPL-3.0)
    an HTML5 Wayland compositor. a Wayland compositor written entirely in TypeScript
    while utilizing WebAssembly and WebGL for the performance critical parts. It can run
    native Wayland applications remotely, or it can run Wayland web applications
    directly in your browser.
    -   [Greenfield Documentations](https://greenfield.app/docs/)
-   <a name="mutter"></a>[Mutter](https://gitlab.gnome.org/GNOME/mutter) (GPL-2)
    A Wayland display server and X11 window manager for Gnome used by Gnome-Shell.

    When used as a Wayland display server, it runs on top of KMS and libinput. It
    implements the compositor side of the Wayland core protocol as well as various
    protocol extensions. It also has functionality related to running X11 applications
    using Xwayland.

    When used on top of Xorg it acts as a X11 window manager and compositing manager.
-   <a name="wayfire"></a>[Wayfire](https://wayfire.org/) (MIT License)
    a wayland compositor based on wlroots.
   [![packaging](https://repology.org/badge/tiny-repos/wayfire.svg?header=packages)
   ](https://repology.org/project/wayfire/versions).

    -   [Wayfire - GitHub](https://github.com/WayfireWM/wayfire)
    -   [Wayfire Wiki](https://github.com/WayfireWM/wayfire/wiki)
    -   The [WayfireWM - GitHub repository ](https://github.com/WayfireWM/)
        contains also many composants for wayfire, _wf-shell_ a GTK3-based panel for
        wayfire,  _wf-config_ a library for managing configuration files,
        _wcm_ Wayfire Config Manager, _wf-utils_ utility classes for Wayfire,
        _wf-touch_ touchscreen gesture library, _wf-osk_ on-screen keyboard using gtkmm.
    -   There are also third party plugins:
        [wstroke](https://github.com/dkondor/wstroke),
        [ammen99-plugins](https://github.com/ammen99/wayfire-plugins),
        [wf-gsettings](https://github.com/DankBSD/wf-gsettings),
        [wf-mod2key](https://github.com/DankBSD/wf-mod2key),
        [wf-wallpaper](https://github.com/DankBSD/wf-wallpaper),
        [windecor](https://gitlab.com/marcusbritanicus/wayfire-plugins)
    -   [Waysmoke](https://github.com/DankBSD/waysmoke)
        is a desktop shell for _Wayfire_. _In alpha in end 2020._
-   [weston](https://gitlab.freedesktop.org/wayland/weston)
    Weston is the reference implementation of a Wayland compositor.
    -   [Weston Gitlab repository](https://gitlab.freedesktop.org/wayland/weston)
    -   [Weston - ArchWiki](https://wiki.archlinux.org/index.php/Weston)
    -   [Building and Running Weston - Freedesktop
        ](https://wayland.freedesktop.org/building.html)
    -   [wlroots](https://github.com/swaywm/wlroots)
        A modular Wayland compositor library, on wich are based numerous compositors
        including Weston.

## Sway {#sway}
[Sway](https://swaywm.org/) (MIT License)
is a tiling Wayland compositor and a drop-in replacement for the
{{< iref "#i3_wm" "i3 X11 window manager" >}}.
It can works with your existing i3 configuration, but need some adjustement to
be fully functional
-   [Sway Wiki](https://github.com/swaywm/sway/wiki).
-   [Sway - ArchWiki](https://wiki.archlinux.org/index.php/Sway).
-   <a name="swaybar"></a>{{< man "Swaybar" >}} is the status-bar included in sway project, it
    supports a {{< man "swaybar-protocol" "similar ipc protocol"  >}} and most of the
    same features as {{< iref "#i3bar" "i3bar" >}}, and is configured in the same way.
-   [Sway IRC channel](http://webchat.freenode.net/?channels=sway&uio=d4) _#sway on
    irc.freenode.net_.
-   [dotfiles with a Nord theme for sway](https://github.com/nboughton/dotfiles)

### Tools that work in both Sway and i3. {#sway_and_i3_tools}
-   [i3status](http://i3wm.org/i3status/manpage.html) (BSD Licence)
    is a small program for generating a status bar for
    {{< iref "#i3bar" "i3bar" >}}, {{< iref "#swaybar" "swaybar" >}}, dzen2,
    {{< iref "#xmobar" "xmobar" >}} or similar programs.
-   [i3pystatus](https://github.com/enkore/i3pystatus)
    is a  collection of python 3 scripts for status output
    compatible to i3status / {{< iref "#i3bar" "i3bar" >}}.
    -   [i3pystatus documentation
        ](http://i3pystatus.readthedocs.io/en/latest/)
-   {{< iref "#j4status" "j4status" >}} below is an alternative
    to _i3-status_;
-   [i3blocks](https://github.com/vivien/i3blocks)
    status line for the i3 window manager. It handles clicks, signals
    and language-agnostic user scripts.

    We can use [i3blocks](https://github.com/vivien/i3blocks) in _{{< iref "#i3bar"
    "i3bar" >}}_ to replace _i3status_ or inside {{< iref "#swaybar" "swaybar" >}}.
    With the standard configuration which mimic i3status.

    _i3blocks_ has a memory footprint of 0.7M/0.5M to which are temporarily added the
    called programs to update status.
    -   [i3blocks wiki](https://github.com/vivien/i3blocks/wiki)
        give example of _i3blocks_ scripts, and explain how to write
        your ownmp.
-   [i3-dstatus](https://github.com/altdesktop/i3-dstatus)

statusline generator for i3wm or sway
-   [i3keys](https://github.com/RasmusLindroth/i3keys) (MIT License)
    lists all the keys that are bound to some action in _i3_ or _sway_,
    You can see the results in three ways. By opening a local web page, output the
    keyboards as text in the terminal or generate SVG files.
-   [i3ipc-python](https://github.com/altdesktop/i3ipc-python) ( BSD-3)
    is a Python library to control _i3wm_ and _sway_.
    -   [i3ipc-python Documentation](https://i3ipc-python.readthedocs.io/en/latest/).
    -   [i3ipc-python examples
        ](https://github.com/altdesktop/i3ipc-python/tree/master/examples)
-   [i3-sway-switch-window](https://github.com/johanwiden/i3-sway-switch-window)
    In i3wm, or sway, replace currently focused window with emacs buffer,
    file from emacs recentf, browser window showing URL from a browser tab,
    or another window.
    *i3-sway-switch-window* uses [brotab](https://github.com/balta2ar/brotab).

### sway tools
All wayland tools which accept _wlroots_ based compositors, work with sway, you find
them below in the {{< iref "#wayland_desktop_components" "Wayland destop components" >}}.

The {{< iref "#i3_tools" "i3 status tools" >}} like _i3status_ and alternatives like
_i3blocks_ can be used in _{{< iref "#swaybar" "swaybar" >}}_
like in _{{< iref "#i3bar" "i3bar" >}}_ and tools with text or web output
like _i3keys_.

The themes are the same than for i3 you find them in
{{< iref "#i3_themes" "I3/Sway themes" >}}.

-   [swaybg](https://github.com/swaywm/swaybg)
    is the Wallpaper tool for Wayland compositors provided by sway. It is in Debian and
    the package _sway-backgrounds_ contains the backgrounds provided with sway.
-   [swayidle](https://github.com/swaywm/swayidle) (MIT LIcense)
    Idle management daemon for Wayland. It allows to monitor user idle time and notifies
    when user activity resumes. This is useful for chat applications setting user away,
    power management features to dim screen, etc.. _In Debian._
-   [swaylock](https://github.com/swaywm/swaylock) (MIT License)
    Screen locker for Wayland. _In Debian._

## Wayland desktop components {#wayland_desktop_components}

In the {{< iref "images" "Image page" >}} you can find the
{{< iref "images#wayland_image_viewers" "wayland image viewers" >}}
and {{< iref "images#wayland-screeshot" "wayland screenshot tools" >}}

I don't list here all the GTK and QT applications that run natively under Wayland

_Sway_ has a long list of
[Useful add ons for sway](https://github.com/swaywm/sway/wiki/Useful-add-ons-for-sway).

The [wlr protocol](https://github.com/swaywm/wlr-protocols) is supported by
many wlroots-based compositors.

[awesome Wayland](https://github.com/natpen/awesome-wayland) list many wayland clients.

[Useful add ons for sway · Sway Wiki
](https://github.com/swaywm/sway/wiki/Useful-add-ons-for-sway)
is a extended list of apps and scripts for swaywm.

The Nix overlay [nixpkgs-wayland](https://github.com/colemickens/nixpkgs-wayland)
has built many wayland tools. _List in the Readme_

See also {{< iref "xorg#wayland_remote_desktop" "Wayland remote desktop" >}}
for the vnc and rdp servers and clients.

See below the {{< iref "#wayland_menus" "dmenu/rofi alternatives" >}} and above the
{{< iref "#wayland_clipboard" "Wayland clipboard tools" >}}.

-   [CuboCore](https://cubocore.gitlab.io/)
    develop _Coreapps_ alias _C suite_, a set of QT apps, which are Desktop Independent
    with Consistent Look and have minimum dependencies. The repository provides Debian
    sid packages.

    The current applications are:
    -    CoreFm - A lightweight file-manager.
    -    CoreAction - A side bar for showing widgets.
    -    CoreStats - A system resource viewer.
    -    CorePad - A document editor.
    -    CoreRenamer - A batch file renamer.
    -    CorePDF - A PDF viewer.
    -    CoreInfo - Show file informations.
    -    CorePaint - A paint app.
    -    CoreStuff - An activity viewer.  -
    -    CoreHunt - A file finder utility.
    -    CoreTime - A time related task manager.
    -    CoreTerminal - A terminal emulator.
    -    CoreShot - A screen capture utility.
    -    CorePins - A bookmarking app.
    -    CoreKeyboard - A x11 based virtual keyboard(alpha).
    -    CoreUniverse - Shows information about apps  from the CoreApps family.
    -    CoreImage - An image viewer.
    -    CoreArchiver - Archiver to create and extract archives.  -
    -    CoreGarage - A settings manager.

    _CuboCore_ also develop a desktop based on {{< iref "#wayfire" "WayFire" >}}:
    <a name="paper"></a>[Paper](https://gitlab.com/cubocore/paper)
    _still in alpha in end 2020._

-   <a name="grim"></a>[grim](https://github.com/emersion/grim) (MIT Licence)
    Grab images from a Wayland compositor. Works with slurp and with sway.
    [![packaging](https://repology.org/badge/tiny-repos/grim.svg?header=packages)
    ](https://repology.org/project/grim/versions).
-   <a name="kanshi"></a>[kanshi](https://sr.ht/~emersion/kanshi/) (MIT License)
    Dynamic display configuration for wayland compositors. Kanshi allows you to define
    output profiles that are automatically enabled and disabled on hotplug. _in Debian_
    [![packaging](https://repology.org/badge/tiny-repos/kanshi.svg?header=packages)
    ](https://repology.org/project/kanshi/versions).
-   [wshowkeys](https://git.sr.ht/~sircmpwn/wshowkeys)
     Displays keypresses on screen on supported Wayland compositors.
-   <a name="wf-recorder">[wf-recorder](https://github.com/ammen99/wf-recorder) (MIT License)
    screen recorder for wlroots based compositors. _in Debian and
    [![packaging](https://repology.org/badge/tiny-repos/wf-recorder.svg?header=packages).

    Other screencasting utilities are in
    {{< iref "video_edit#creencasting" "screncasting section" >}}.
    ](https://repology.org/project/wf-recorder/versions).
-   [wl-screenrec](https://github.com/russelltg/wl-screenrec) (Apache 2.0 License)
    High performance wlroots rust screen recording software, featuring hardware encoding,
    to use when your hardware has {{< wp "vaapi" >}} encode support.
    [![packaging](https://repology.org/badge/tiny-repos/wlscreenrec.svg?header=packages)
    ](https://repology.org/project/wlscreenrec/versions).
-   [wdisplays](https://github.com/cyclopsian/wdisplays) (GPL-3.0
    GUI display configurator for wlroots compositors. _In Debian._
    [![packaging](https://repology.org/badge/tiny-repos/wdisplays.svg?header=packages)
    ](https://repology.org/project/wdisplays/versions).
-   [wlr-randr](https://github.com/emersion/wlr-randr) (MIT License)
    An xrandr clone for wlroots compositors. _in Debian and
    [![packaging](https://repology.org/badge/tiny-repos/wlr-randr.svg?header=packages)
    ](https://repology.org/project/wlr-randr/versions).
-   [wtype](https://github.com/atx/wtype) (MIT License)
    xdotool type for wayland. _in Debian and
   [![packaging](https://repology.org/badge/tiny-repos/wtype.svg?header=packages)
   ](https://repology.org/project/wtype/versions).


# Desktop components {#desktop_components}

-   [Cursor themes - ArchWiki](https://wiki.archlinux.org/title/Cursor_themes).
-   [Icons - ArchWiki](https://wiki.archlinux.org/title/Icons).

## Panels {#panels}
The  distinction between taskbar, panel, and status bar is not clear, as some status bar
offer menus, system tray, launcher, volume-control ... On the other side panels can also
display the status. So you should also look at the
{{< iref "#status_bar" "status bar section" >}}.


Many window managers provide their own panel, some window manager other mostly the lean
ones let the user choose an external one.

-   _aewm++-fspanel_ (MIT) is a minimal panel developped with aewm++, but it
    does not depend on iT. It is in the debian package aewm++-goodies.
-   [fbpanel](https://github.com/aanatoly/fbpanel) (GPL)
    FBPanel is a spinoff of the fspanel written in C/GTK-2
    It provides a taskbar (list of all opened windows), pager, desktop switcher,
    launchbar, clock, and more through plugins is EWMH/NETWM
    compliant. Last commit 2015, but there are more recent fork _ available in Debian_
    -   [fbpanel configuration](http://aanatoly.github.io/fbpanel/docs.html)
-   _Fspanel_ (GPL)
    works with EWMH compliant WMs. _available in Debian_
-   _Hpanel_ is a fork of _fspanel_ to better handle maximized windows.
    _available in Debian_
-   [ltpanel](http://ltpanel.sourceforge.net/) (GPL)
    is a lightweight panel, looking similar to the gnome tasklist
    applet. It uses only xlib and has a very light memory footprint.
    It is based on Peter Zelzny's _fspanel_ and is available in Debian.
-   [LXPanel](http://lxde.org) is the  GTK+2 desktop panel for lxde, it
    has minimal gtk2 dependencies.
-   [lxqt-panel](https://github.com/lxqt/lxqt-panel)
    is the {{< iref "#lxqt" "LxQt" >}} panel.
-   [pypanel](http://pypanel.sourceforge.net/) (GPLv2)
    is a lightweight panel/taskbar written in Python and C
    it works with EWMH compliant WMs (Openbox, PekWM, FVWM, etc.)
    -   [ArchWiki: pypanel](https://wiki.archlinux.org/index.php/PyPanel)
-   <a name="tint2"></a>[tint2](http://code.google.com/p/tint2/)  (GPLv2)
    is a panel (made for openbox3 but without lxde dependencies)
    with taskbar,
    systray, clock and battery status and  window manager's menu.
    The mem footprints of tint2 is 6.7M resident / 5.2 shared<br />
    -   [tintwizard](http://code.google.com/p/tintwizard/) is a theme
        switcher for tint2.
    -   [ArchWiki: tint2](https://wiki.archlinux.org/index.php/Tint2)

## Status Bar {#status_bar}
Most window manager have their own status bar and a status generation
programs or scripts, like _{{< iref "#i3bar" "i3bar" >}}_ with _i3status_ or _i3blocks_.
But some alternative status are window manager independant.

-   <a name="j4status"></a>[j4status](http://j4status.j4tools.org/) (GPL)
    is an alternative to _i3-status_ but it is available on any tiling wm.  It
    provides a status line using several plugins to retrieve system information.
    -   [j4status-plugins
        ](https://j4status.j4tools.org/j4status-plugins/)
        add plugins for _alsa_, _mpris_, filesystem, cpu and memory usage, backlight
        percentage, i3 focus, _networkmanager_, and an inotify plugein to _j4status_.
-   <a name="lemonbar"></a>[lemonbar](https://github.com/LemonBoy/bar) (MIT License)
    is a lightweight bar based on XCB. It provides foreground/background color switching
    along with text alignment and colored under/overlining of text, full utf8 support
    and reduced memory footprint.
-   <a name="polybar"></a>[polybar](https://github.com/polybar/polybar) (MIT License)
    highly customizable status bar, written in c++. It has built-in functionality to
    display information about the most commonly used services.

    _polybar_ has no wayland support (except xwayland!) {{< iref "#waybar" "waybar" >}}
    and {{< iref "#yambar" "yambar" >}} are wayland bars with similar functionalities.

    _polybar_ is in Debian.
-   <a name="waybar"></a>[waybar](https://github.com/Alexays/Waybar) (MIT license)
    is a customizable Wayland bar for Sway and Wlroots based compositors. It is in Debian.
    -   [waybar wiki](https://github.com/Alexays/Waybar/wiki).
-   <a name="xmobar"</a>[xmobar](http://projects.haskell.org/xmobar/) (BSD License)
    written in haskell, is a lightweight, text-based, status.  It was originally
    designed to work with xmonad, but it's actually usable with any window-manager. It
    is in Debian.  It can be used for _conky_ or _i3status_ output.
    -   [ArchWiki xmobar](https://wiki.archlinux.org/index.php/Xmobar)
-   <a name="yabar"></a>[Yabar](https://github.com/geommer/yabar) (MIT License)
    is a lightweight status bar for X window managers. _Yabar_ is in debian.
-   [yambar](https://codeberg.org/dnkl/yambar) (MIT License)
    Modular status panel for X11 and Wayland, inspired by
    {{< iref "#polybar" "polybar" >}}.

## Menu systems {#menus_systems}
-   [List of applications  launchers - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Other#Application_launchers)

### terminal menus
-   [pdmenu](https://joeyh.name/code/pdmenu/) full screen console
    menuing sys tem for Unixs removed from Debian since 2017, but still active
    [in Joey Hess git repository](https://git.joeyh.name/index.cgi/pdmenu.git/).
-   [qmenu](https://github.com/teopost/qmenu/)
    is a terminal menu creator.
    Features include options to format the menu, bindings to function keys, possibility
    to include submenus, show help messages and launch shell sessions.  package in
    Debian.
-   [smenu](https://github.com/p-gen/smenu) (MPL-2.0 license)
    is a command-line utility that allows you to use words coming from the
    standard input to create a nice selection window just below the cursor. Your
    selection will then be sent to standard output.

### Window menus from shell
-   Root menus are menus which popup when clicking on root window they are part of most
    floating window managers, but there are some stand alone, for window managers which
    do not provide a menu such as Oroborus.
    -   [deskmenu (debian package)](https://packages.debian.org/sid/deskmenu).
-   _9menu_ from plan9,
    -   [9menu Debian package](https://packages.debian.org/testing/9menu)
-   _ratmenu_ forked from 9menu for ratpoison wm.
    -   [ratmenu Debian package](https://packages.debian.org/testing/ratmenu)
-   [Zrajm’s programs](http://zrajm.org/programs/) provide _ratmen_ a
    _ratmenu_ alternative, and _termmen_ a zsh menu.

### dmenu {#dmenu}
[dmenu](http://tools.suckless.org/dmenu/)
is a dynamic menu for X, originally designed for dwm. part of the suckless-tools package
in Debian.
-   [ArchWiki: dmenu](https://wiki.archlinux.org/index.php/dmenu).
-   [dmenu-distrotube · GitLab](https://gitlab.com/dwt1/dmenu-distrotube) (MIT License)
    Derek Taylor heavily-patched and customized build of the Suckless dmenu run launcher.
-   [Archlinux dmnenu hacking thread](https://bbs.archlinux.org/viewtopic.php?id=80145),
-   [jukil/dmenu-scripts-collection](https://github.com/jukil/dmenu-scripts-collection)
    collected from the hacking thread _until 2014, newer scripts are not here!_.
-   [tlvince/dmenu-tools](https://github.com/tlvince/dmenu-tools).
    A collection of scripts in the _dmenu_tools_ AUR package:
    dmenu_edit, dmenu_menu, dmenu_mpc, dmenu_netctl, dmenu_raise, dmenu_raise_or_run,
    dmenu_run_recent.
-  John Sagotsky [dmenu toys](http://sagotsky.github.io/2013/10/11/dmenu-toys.html)
   is a blog page from _2013_ some scripts using dmenu or {{< iref "#rofi" "rofi" >}},
   described here, and many others are available in his [dotfiles and scripts - GitHub
   ](https://github.com/sagotsky/.dotfiles/).

   Among them
   -   `cli-board` reads in a directory as its input. Selecting a file will
       either read or execute it, and copy its contents or output to the clipboard.
   -   `cheat-sheet`is similar but select a text file and allow to copy selected lines.

### Rofi {#rofi}
[Rofi](https://github.com/davatorium/rofi) (MIT License)
is a popup window switcher requiring only xlib and pango.
It was written by Sean Pringle and later expanded by [Dave Davenport
](https://github.com/DaveDavenport) alias _Qball_.

Rofi can act as a drop-in dmenu replacement and provides
extra features, like a run-dialog, ssh-launcher, ....

Rofi support wayland since version 2.0, where the
[lbonn fork of rofi](https://github.com/lbonn/rofi) which adds
[Wayland support](https://github.com/lbonn/rofi#wayland-support)
was merged with Rofi mainline.

[![packaging](https://repology.org/badge/tiny-repos/rofi.svg?header=packages)
](https://repology.org/project/rofi/versions).

-   [GitHub - davatorium/rofi](https://github.com/davatorium/rofi)
-   [Rofi Documentation](https://davatorium.github.io/rofi/)
-   [Rofi - manpage](https://github.com/davatorium/rofi/blob/master/doc/rofi.1.markdown),
-   [Rofi wiki](https://github.com/davatorium/rofi/wiki).
-   [Rofi scripts index](https://github.com/davatorium/rofi/wiki/User-scripts)
-   [Discussions · davatorium/rofi](https://github.com/davatorium/rofi/discussions)
-   [Rofi - ArchWiki](https://wiki.archlinux.org/title/Rofi).
-   [reddit - Qball tools forum](https://reddit.com/r/qtools/)
    support channels for rofi, gmpc and other tools written by Qball.
-   [Rofication](https://github.com/DaveDavenport/Rofication)
    Dave Davenport notification system.
-   [jluttine/rofi-power-menu](https://github.com/jluttine/rofi-power-menu)
    Configurable power menu mode for Rofi and dmenu.
-   [rofi-blezz](https://github.com/davatorium/rofi-blezz) is a plugin for
    {{< iref "#rofi" "rofi" >}} that emulates [blezz](https://github.com/Blezzing/blezz)
    the guided Keystroke Launcher.
-   [Derek Taylor  dmscripts](https://gitlab.com/dwt1/dmscripts) (GPL 3)
    a collection of scripts for dmenu, fzf, rofi.


### dmenu alternatives
-   You find {{< iref "#lemonbar" "lemonbar" >}} in the status bar section.
-   {{< iref "#yabar" "yabar" >}} in the status bar section.
-   [Albert](https://albertlauncher.github.io/)
    is a keyboard launcher written in C++/Qt.
    -   [Switching to Sway (Wayland) from i3 (X11)
        ](https://www.autodidacts.io/switching-to-sway-wayland-from-i3-x11-ubuntu/)
        explains how to use it in wayland by installing the proper fork. It lso warn us
        that _albert_ is very memory hungry.
-   [Kupfer](https://github.com/kupferlauncher/kupfer) (GPL-3.0)
    is a Python/GTk3 launcher .
    -   [Kupfer Manual](https://kupferlauncher.github.io/help/en/).
    -   [Kupfer Technical Documentation
        ](https://kupferlauncher.github.io/Documentation/).

### wayland dmenu/rofi alternatives {#wayland_menus}
{{< iref "#rofi" "rofi" >}} works on Wayland sinve v 2.0, but it was previously confined
to X11, an many Wayland alternatives have been developped.

See also the list in [awsome Wayland - launchers
](https://github.com/natpen/awesome-wayland#launchers).

-  <a name="bemenu"></a> [bemenu](https://github.com/Cloudef/bemenu) (GPLv3 and LGPLv3)
    is an dynamic menu library and client program inspired by dmenu.
    It has ncurses, x11, and wayland backend, provided as distinct libraries; so you
    need only the one which fit with your desktop.

    *bemenu* can be used with {{< iref "#j4-menu-desktop" "j4-menu-desktop" >}} for a
    desktop files menu.
    -   [bemenu API documentation](http://cloudef.pw/bemenu/).
-   [dmenu-wl](https://github.com/nyyManni/dmenu-wayland) (MIT License)
    dmenu for wayland (wlroots) compositors.
-   <a name="fuzzel"></a>[fuzzel](https://codeberg.org/dnkl/fuzzel) (MIT License)
    Application launcher for wlroots compositors, similar to rofi's `drun` mode.
    *Packaged in Debian.*
-  <a name="lbonn_rofi"></a> [lbonn/rofi](https://github.com/lbonn/rofi) (MIT License)
    a rofi fork with wayland support.
-  <a name="tofi"></a> [tofi](https://github.com/philj56/tofi) (MIT License)
    fast and simple dmenu / {{< iref "#rofi" "rofi" >}} replacement for wlroots-based
    Wayland compositors.  _tofi_ is in Debian.
-   <a name="wofi"></a>[wofi](https://hg.sr.ht/~scoopta/wofi) (GPL-3.0)
    a launcher/menu program for wlroots based wayland compositors such as sway.
    The documentation is in the man pages. There are packages for most distribution
    including Debian.
    -   [wofi-scripts](https://github.com/tobiaspc/wofi-scripts)
        Scripts for wofi, Window switcher and SSH session launcher.
-   [sgtk-menu](https://github.com/nwg-piotr/sgtk-menu) (GPL-3.0)
    Python GTK launchers for sway & other WMs w/ menu, dmenu, application grid and
    button bar.  There is also a C++ version
    [nwg-launchers](https://github.com/nwg-piotr/nwg-launchers) (GPL-3.0)
    which is packaged in [nixpkgs-wayland
    ](https://github.com/colemickens/nixpkgs-wayland).
-   [wlogout](https://github.com/ArtsyMacaw/wlogout)
    A wayland based logout menu in GTK+.
-   [yofi](https://github.com/l4l/yofi) (MIT License)
    is a minimalistic menu for wayland written in Rust.

### Dzen {#dzen}
[Dzen](https://github.com/robm/dzen) (MIT License)
is a notification and menuing program for X11 that requires only X11.  It is designed to
be scriptable in any language and integrate well with light window managers. A _dzen_
daemon takes only 1.5M res/1.1M shr. It is no more developed since 2013.

The debian version is a fork of dzen, to maintain it up-to-date with Debian/Ubuntu,
hosted on launchpad
[dzen2](https://git.launchpad.net/ubuntu/+source/dzen2/tree/).

-   The [Dzen Wiki](https://github.com/robm/dzen/wiki) gives many examples of using
    _dzen_ as system monitor, with simple scripts.
-   [ArchLinux: dzen](https://wiki.archlinux.org/index.php/Dzen)
-   You can [pipe the output of conky
    ](https://wiki.archlinux.org/index.php/Dzen#Dzen_.26_Conky) to dzen.
-   Or [pipe the output of i3status ](http://i3.zekjur.net/i3status/).
-   [dzen-tools](https://github.com/dgvncsz0f/dzen-tools)
    by Diego Souza has _systat2dzen_, a python script that gives hostname, date/time,
    sys statistics, meminfo, iostat, load ifo, disk status, battery status, check local
    or imap mailboxes, ethernet and wireless status; _Last commit 2013._

### Freedesktop (xdg) menus {#xdg_menus}

They can be a root menu or a popup using one of the previous bars.
The python programs use
[PyXDG
](https://pyxdg.readthedocs.org/en/latest/_modules/xdg/Menu.html).

Most often the menus are displayed by a menu launcher, the most popular being
{{< iref "#dmenu" "dmenu" >}}, {{< iref "#rofi" "rofi" >}} and all the rofi like menus
sytems such as those referred in {{< iref "#wayland_menus" "dmenu/rofi alternatives" >}}.

-   The Faq.i3wm forum [How can I use autostart .desktop files in i3?
    ](https://faq.i3wm.org/question/2155/how-can-i-use-autostart-desktop-files-in-i3/)
    teach how to use dex to test your autostart files.
-   [fluxbox-xdg-menu](http://code.google.com/p/fluxbox-xdg-menu/) (GPL)
    is a python based menu generator used to create a menu for fluxbox
    using freedesktop.org standards.
-   [Gmrun](https://sourceforge.net/projects/gmrun/)
    (Gnome Completion-Run) is an lightweight application launcher,
    with bash-like TAB completion, thet propose all the xdg desktop programs.
    -   [ArchWiki: Gmrun](https://wiki.archlinux.org/index.php/Gmrun)
-   [i3-start-menu](https://tbellembois.github.io/i3_menu.html) (GPL)
    by Thomas Bellembois.
-   <a name="jgmenu"></a>[jgmenu](https://github.com/johanmalm/jgmenu) (GPL)
    is an X11 menu, written ic C with no toolkit dependencies, designed for scripting.
    t can display the following types of menu : a jgmenu flavoured CSV format,
    XDG application menu, pipe menus, openbox XML menu.

    A Debian source package is provided in the distribution.

    _Jgmenu_ is the standard menu of
    [busenlabs distribution](https://www.bunsenlabs.org/)
    which provides a Debian package in it's apt repository.
    -   [jgmenu documentation](https://jgmenu.github.io/)
        contains the [man pages](https://jgmenu.github.io/manual.html).
    -   [jgmenututorial(7)](https://jgmenu.github.io/jgmenututorial.7.html)
        is a step-by-step tutorial to _jgmenu_.
-   <a name="j4-dmenu-desktop"></a>
    [j4-dmenu-desktop](https://github.com/enkore/j4-dmenu-desktop) (GPL)
    it is an alternative (a lot quicker) for  i3-dmenu-desktop.
    _j4-dmenu-desktop_ doesn't require i3wm and work on any desktop
    environment.
-   [MenuMaker](http://menumaker.sourceforge.net/) (BSD Licence)
    is a python menu generation utility for: Blackbox, Deskmenu, FluxBox, IceWM, Jwm,
    OpenBox, Pekwm, WindowMaker ,XFce4 it can use both of Freedesktop.org's `.desktop`
    files and Debian application entries.
-   [menutray](https://github.com/trizen/menutray) (GPL 3.0)
    is a simple GTK+ application menu tray.
-   [morc_menu](https://github.com/Boruch-Baum/morc_menu/) (GPL)
    is an categorized desktop application menu, independent of any window manager.
    it is an alternative for  i3-dmenu-desktop and
    {{< iref "#j4-dmenu-desktop" "j4-dmenu-desktop" >}}.
-   [ArchLinux xdg-menu](https://wiki.archlinux.org/index.php/Xdg-menu)
    is a perl scrip to generate menus for twm, ion3, WindowMaker, fvwm2, icewm,
    blackbox, fluxbox, openbox, awesome.
-   [xdgmenu](https://github.com/crichon/xdgmenu) (xdgMIT License)
    is a python/ncurses application to launch a xdg menu. _2016_.
-   [xdgmenumaker](https://github.com/gapan/xdgmenumaker/) (GPL)
    is a command line tool, written in python, that generates application menus using
    xdg information, by scanning *.desktop files. It can generate menus for Fluxbox,
    IceWM, jwm, pekwm, Window Maker.

## Launch Bars {#launch_bars}
Launch Bars are also named _taskbar_, _dock_ or _launchers_, but _launchers_ refers also
to launchers menus which are grouped in the previous entries.

-   [i3status](http://i3.zekjur.net/i3status/)
-   _aewm++-appbar_ (MIT) is a minimal launchbar developped with aewm++, but it does not
    depend on iT. It is in the debian package aewm++-goodies.
-   [tabble](http://www.rillion.net/tabble/) (GPL)
    is a small rectangular widget written in C/GTK2 which presents your programs in tabs
    for easy launch. It can also be launched with sudo to give an easy root access to
    some programs.The last release is 2012. It is in debian.
-   [wbar](http://code.google.com/p/wbar/source/browse/trunk/README)
    is a C++/gtk launch bar. It was initially developed for Fluxbox, then tested on
    WindowMaker, Xfce, GNOME, etc. It is in Debian
    -   _wbar-config_ is the recommended tool to customize Wbar. In debian it is in a
        separate package.
-   [lxlauncher](http://wiki.lxde.org/en/LXLauncher)
    is a launcher for application programs developed for the 7"-10.2" screens (netbooks)
    it follows freedesktop.org specs.
-   [Cairo-Dock](http://www.glx-dock.org/)
    is a highly customizable dock (_not light_) written in C. It is in debian. It can be
    controlled from a terminal or another application through the DBus interface.
    Features can be added by plug-ins or applets.
    -   [Cairo-Dock - ArchWiki](https://wiki.archlinux.org/index.php/Cairo-Dock).
-   [Launchpad: Avant Window Navigator (Awn)](https://launchpad.net/awn)
    is a dock-like bar which sits at the bottom of the screen. It is for composite
    window managers and no longer in Debian.
    -   [Avant Window Navigator - ArchWiki
        ](https://wiki.archlinux.org/index.php/Avant_Window_Navigator)

## Pin boards
Pin boards allow to create icons on your desktop and to associate some command or action
to the icon.

Some desktop include a built in pin board as _Gnome_ through its file manager
_Nautilus_.

_Pcmanfm_ also has an option to manage the desktop, and you can then use desktop
shortcuts.

You can choose to not have a pinboard on your desktop. A pinboard is easily hidden by
floating windows, and is a non-sense with tiling wm that use all the screen but to use a
menu system or a {{< iref "#launch_bars" "Launch Bar" >}}.

-   [fbdesk](http://fluxbox.sourceforge.net/fbdesk/) (3.8M) aimed at
    FluxBox/BlackBox, it is in debian.
-   [idesk](http://idesk.sourceforge.net) (9.2M)
    _last release 2005, but [still in Debian](https://tracker.debian.org/pkg/idesk) as
    far as 2023_.
-   Desklaunch from the
    [Oroborus Window Manager](http://www.oroborus.org/), which can
    be used with an other minimal wm.
    DeskLaunch is a small utility for creating desktop icons using pixmaps.
    Debian packages the three utilities *desklaunch*, *keylaunch*, *deskmenu* as three
    separates packages, but *Oroborus* and the related package are no longer pushed in
    versions after *Buster* see
    [Debian Tracker; oroborus](https://tracker.debian.org/pkg/oroborus).


## System Trays {#systrays}

The [freedesktop](http://www.freedesktop.org/) compatible application
can use a _systray_ as provided by gnome and kde.  Some light window
managers provide a _systray_ in their panel/taskbar like _fluxbox_, or
in their status-bar like _i3_
We can also use a stand alone  generic _sys-trays_.  For some I
have tried I give their memory size, this information is only
indicative as always because depending of many factors, and as some
part is shared memory, that may be yet loaded if you use the same
toolkit that your window manager, or one desktop component.

If we need to add system tray to a light wm, it should at least be
thin.

-   [trayer](https://github.com/sargon/trayer-srg) (4.4M)
    a fork of the [fbpanel](http://fbpanel.sourceforge.net/)
    systray. It is in Debian.
-   [Docker](http://icculus.org/openbox/2/docker/) comming from
    openbox dock any application into the system tray.
    It works for all NET WM compliant window managers
    It weight only 0.8M and works well. It is in debian.
    There is an alternative also in Debian
    [kdocker](https://github.com/user-none/KDocker)
    build with Qt, which has more dependencies.
-   [xfce4](http://www.xfce.org/) in xfce4-systray.
-   [stalonetray](http://stalonetray.sourceforge.net/)
    is a stand-alone system tray. It has full XEMBED support
    and minimal dependencies.
    Stalonetray works with any EWMH-compliant window manager and is in Debian.
-   [AllTray](http://alltray.trausch.us/) dock any application
    with no native tray icon into the system tray. Seems to be quite fat
    (6M), it is in debian.

Fluxbox, and i3 among the lighter wm have a systray included in the
build-in taskbar or statusbar.

## Clipboard {#clipboard}

The ICCCM (Inter-Client Communication Conventions Manual) standard
defines three _selections_, called _PRIMARY_, _SECONDARY_ and
_CLIPBOARD_. The _PRIMARY_ selection is conventionally used to
implement copying and pasting via the middle mouse button. The
_SECONDARY_ may be accessed by an alternate mouse action, it's use is
application dependent, the _CLIPBOARD_ is used by the copy/paste menu
in X applications, quite often bound to Ctl-X/Ctl-C Ctl-X/Ctl-V.

For emacs before v. 24  kill and yank commands used the primary
selection, not they use the clipboard.

-   Wikipedia: {{< wp "Clipboard manager" >}}
-   [freedesktop Specifications/ClipboardsWiki
    ](http://www.freedesktop.org/wiki/Specifications/ClipboardsWiki)
-   [Freedesktop clipboard specification
    ](http://standards.freedesktop.org/clipboards-spec/clipboards-latest.txt)
    present the use and recommendations for the three selections.
-   [ArchWiki: Clipboard](https://wiki.archlinux.org/index.php/Clipboard)
    gives a list of
    [clipboard managers](https://wiki.archlinux.org/index.php/Clipboard#Managers).

### x11 Clipboard tools

The X11 applications  provide some tools to deal
with the selections

-   {{< man "xcutsel" >}} is used to copy the current selection into a cut
    buffer and to make a selection that contains the current
    contents of the cut buffer.
    By  default,  xcutsel  will  use the selection named PRIMARY, but
    this can be changed by the option `-selection`.
-   {{< man "xclipboard" >}} in the _x11-apps_ package is an X application to
    display the CLIPBOARD selection. Memory footprints: 4M res / 2M
    shr.

    The selection displayed by _xclipboard_ is the CLIPBOARD, *not the
    PRIMARY*.

-   {{< man "xcb" >}} allows up to 8 cut buffers to be manipulated either via
    the command line, or with the mouse in a point and click
    manner. It uses 4.1M res / 3.6M shr.


Some newer command line apps to manage selection in X11:

-   [autocutsel](http://www.nongnu.org/autocutsel/).
    synchronize the three selections; _in debian_.
-   [clipmenu](https://github.com/cdown/clipmenu)  (public domain)
    is a simple clipboard manager using {{< iref "#dmenu" "dmenu" >}}
    (or {{< iref "#rofi" "rofi" >}}) and {{< iref "#xsel" "xsel" >}};
    _clipmenud_ polls the clipboard every 0.5 seconds,  changes to the
    clipboard contents is writen to a cache; clipmenu reads the cache
    directory, and call dmenu to select one.

    No support for Wayland is planed.
-   [xclip](http://sourceforge.net/projects/xclip/)
    is a command line interface to X selections. It is in Debian.
-   <a name="xsel"></a>[XSel](http://www.vergenet.net/~conrad/software/xsel/)
    is a command-line program for getting and setting the contents of
    the X selection; by default  operates on the _primary_ selection,
    but you can also specify the _secondary_ or _clipboard_.
    It is in Debian.

### Wayland Cilpboard tools{#wayland_clipboard}
-   <a nma="wl-clipboard"></a>[wl-clipboard](https://github.com/bugaevc/wl-clipboard)
     (GPL-3.0). Command-line copy/paste utilities for Wayland.
    {{< man "wl-copy" >}} and {{< man "wl-paste" >}}, copy data between the clipboard and
    pipes, sockets, files and so on.
    _wl-clipboard_ is in Debian.
-   [wl-clipboard-manager](https://github.com/maximbaz/wl-clipboard-manager) (ISC License)
    wrapper over {{< iref "#wl-clipboard" "#wl-clipboard" >}}
    that implements a clipboard manager.
-   [cliphist](https://github.com/sentriz/cliphist) (GPL-3.0)
    a Golang clipboard history “manager” for Wayland.

    The [Releases](https://github.com/sentriz/cliphist/releases) includes
    binaries for x386, amd64 and arm,there are also packages
    [![packaging](https://repology.org/badge/tiny-repos/cliphist.svg?header=packages)
    ](https://repology.org/project/cliphist/versions).

-   [clipman](https://github.com/yory8/clipman) (GPL v3.0)
    is a basic Golang clipboard manager for Wayland, with support for persisting copy
    buffers after an application exits. It is in Debian.

    _Don't confuse with xfce4 clipboard plugin also named clipman._
-   [copypasta](https://github.com/alacritty/copypasta) (MIT and Apache2 License).
    is a rust-clipboard fork. It is a library for getting and setting the
    contents of clipboard. This fork adds support for the Wayland clipboard.

Some clipboard managers in the following section have also a wayland support, but for
most of them by using Xwayland, but clipcat which has now native wayland support.

### Clipboard managers
A list is in [Archwiki Clipboard/Managers
](https://wiki.archlinux.org/title/Clipboard#Managers).


-   [clipcat](https://github.com/xrelkd/clipcat) (GPL-3.0)
    is a clipboard manager written in Rust, written with a Client-Server architecture.

    An experimental wayland support has been added beginning 2025.
-   [clipit](https://github.com/shantzu/ClipIt)
    is a lightweight GTK3 clipboard manager forked from
    {{< iref "#parcellite" "parcellite" >}}.

    _Clipit_ seat in your tray, and allow to select clipboard history.
    It can also be used from the command line.  _Clipit_ has preferences to manage
    _CLIPBOARD_ and _PRIMARY_ selections and synchronize them.
     native

    _ClipIt_ is no longer supported. and is replaced by {{< iref "#diodon" "Diodon" >}}.
-   [clipman for xfce4](https://docs.xfce.org/panel-plugins/xfce4-clipman-plugin/)
    is a clipboard manager for Xfce. It keeps the clipboard contents around while it is
    usually lost when you close an application.
-   [clipman](https://github.com/yory8/clipman) (GPL-3.0)
-   [CopyQ](https://github.com/hluk/CopyQ) (GPL-3.0)
    is a C++/QT  clipboard manager with editing, scripting and a
    command-line interface. _It is in Debian, along with a
    copyq-plugins package._

    CopyQ support wayland, but without global shortcuts, clipboard access from window
    that is not active, and pasting.  If you want these features you can use it with
    Xwayland by launching it with

        $ QT_QPA_PLATFORM=xcb copyq

-   <a name="diodon"></a>[Diodon](https://github.com/diodon-dev/diodon) (GPL-2.0)
    is a vala / GTK3 clipboard manager for Gnome/unity.

     There is no native Wayland support, you need Xwayland.

    _It is in Debian._
-   [gpaste](https://github.com/Keruspe/GPaste) (BSD-2-Clause License)
    is a GTK3 clipboard management system for Gnome. The wayland support is in the TODO
    list, it can run under Xwayland. _in Debian._
-   <a name="parcellite"></a>[Parcellite](https://github.com/rickyrockrat/parcellite)
    (GPL-3.0)
    is a lightweight, basic-features-only X11 and GTK2 clipboard manager.
    In Gnome software suite _parcellite_ is replaced by {{< iref "#diodon" "Diodon" >}}.
    _in Debian_.
-   [qlipper](https://github.com/pvanek/qlipper) (GPL-2.0)
    is a QT5 clipboard history applet.  It depends on X11 and does not support wayland.

    _It is packaged in Debian_.
-   [greenclip](https://github.com/erebe/greenclip) (BSD License)
    is an haskell clipboard manager for {{< iref "#rofi" "rofi" >}}.
    It does not support wayland, since Haskell ecosystem does not have a wayland
    package.
-   [rust-clipboard][https://github.com/aweinstock314/rust-clipboard)
    (MIT and Apache2 License) is a cross-platform library for getting and setting the
    contents of the OS-level clipboard. On Linux it uses the X11 library.

-  [redguardtoo/cliphist](https://github.com/redguardtoo/cliphist)
   is an emacs package by [Chen Bin (reguardtoo)](https://github.com/redguardtoo)
   to paste from parcellite, clipit, greenclip clipboard managers into Emacs

### Clipboard sharing {#clipboard_share}

There are also some web applications that allow sharing of a pasted
data among computers or mobile platforms like
-   [IPShare.net](http://www.ipshare.net/) for use on lan
    _source not available, confidentiality unknown_.

You can also use any {{< iref "file_sharing#pastebin" "pastebin" >}}.

-   [megahertz/clipboard-share](https://github.com/megahertz/clipboard-share)
    is a node.js server and client to share clipboard between two computers.  It works
    on Linux, Mac OS X and Windows.
-   [coralw/share-clipboard](https://github.com/coralw/share-clipboard) (MIT License)
    is a node.js server and client to share clipboard between across different
    platforms, including Mac OS X, Windows and Linux.

    The [Share Clipboard Home | Langui.net](https://langui.net/share-clipboard/)
    propose also ios application (proprietary, paid).
-   [wincent/clipper](https://github.com/wincent/clipper)
    linux daemon that provide a service exposing the local clipboard
    to local or remote processes. It is meant to be used with
    {{< iref "tmux" "tmux" >}} running both locally and remotely.
-   [pgcopy](https://github.com/nakabonne/pbgopy) (MIT License)
    lets you share data across devices like you copy and paste.
    _pbgopy_ comes with a built-in ability to encrypt/decrypt with symetric key,
    public/private key-pair or gpg. Binary are provided for linux and Mac OS, including
    a deb package.
-   [Exposing your clipboard over SSH](https://gist.github.com/dergachev/8259104)
    explains how to copy clipboard to local and remote machines with
    `netcat`, `xclip`, and a reverse ssh session. In this article the
    linux reader will remplace `pbcopy` by `xclip -sel clip`.


## Keyboard addons

-   [XbindKeys](http://www.nongnu.org/xbindkeys/)
    is a program that allows you to launch shell commands with your keyboard or your
    mouse under X Window. It links commands to keys or mouse buttons, using a
    configuration file.

    It is independant of the window manager and can capture all keyboard keys (ex:
    Power, Wake...).  XbindKeys is actively maintained and is in debian.
    -   [Xbindkeys - ArchWiki](https://wiki.archlinux.org/index.php/Xbindkeys).
-   [TrigerHappy](https://github.com/wertarbyte/triggerhappy)
    Triggerhappy is a hotkey daemon developed with small and embedded systems in
    mind. It attaches to the input device files and interprets the event data received
    and executes scripts configured in its configuration. It is in Debian.

    Unlike other hotkey daemons, it runs as a persistent, systemwide service and
    therefore can be used even outside the context of a user or X11 session It can
    handle any input device and might be useful on a headless system to use input events
    generated by a remote control (Ex. control an mpd server).
-   [Keynav](http://www.semicomplete.com/projects/keynav/)
    turns your keyboard into an fast pointer mover.
-   [Keylaunch (debian package)](https://packages.debian.org/jessie/keylaunch)
    is a small utility for binding commands to a hot key. It reads a configuration file
    in .keylaunchrc. KeyLaunch uses Ctrl, Alt and Shift as modifier keys, the hotkey is
    up to the user.

    There is a [Jerko Steiner fork of keylaunch](https://github.com/jeremija/keylaunch)
    which enables binding of Mod4 (windows) key.
-   [Synergy](http://synergy2.sourceforge.net/)
    lets you share a single mouse and keyboard between multiple computers with different
    OS, each with its own display,

## desktop background
You can use the following programs to set the X desktop backgound:

-   {{< man "xsetroot" >}}
-   {{< man "fbsetbg" >}}
-   Esetroot
-   wmsetbg
-   {{< iref "images#feh" "feh" >}}
-   hsetroot
-   chbg
-   {{< iref "images#imagemagick" "display" >}}
-   {{< iref "images#pqiv" "pqiv" >}}
-   xv
-   xsri
-   xli
-   xsetbg


{{< iref "images#feh" "feh" >}}, esetroot and wmsetbg support pseudo transparency


## Other components

-   [xgetc](http://code.google.com/p/xgetc/)
    print the pixel color (in hexadecimal notation) and position to stdout.  When a
    selection is made, xgetc will print the geometry of the selection.

# WM control {#wm_control}
These tools allow to control windows from an [EWMH](#ewmh "internal reference")
compliant manager.  They complement the basic utilities that can only give informations
on the window property like {{< man "xwininfo" >}} or {{< man "xprop" >}}.


-   [xdotool](https://github.com/jordansissel/xdotool/)
    simulate keyboard input and mouse activity, move and resize windows, etc. It is
    packaged in Debian.
    [xdotool manpage ](https://github.com/jordansissel/xdotool/blob/master/xdotool.pod)
-   [xwit](http://www.slack.com/sw/xwit-man.html)
    resize, iconify, pop, and move windows given by name or id, change an icon, title or
    name, set the screen saver going, and change individual key autorepeat settings,
    move the mouse cursor, etc. It is packaged in Debian.
-   [wmctrl](http://tripie.sweb.cz/utils/wmctrl/) (GPL)
    provides command line access to almost all the features defined in the EWMH
    specification. For example it can maximize windows, make them sticky, set them to be
    always on top. It can switch and resize desktops and perform many other
    operations. The last release is 1.07 from 2005, but EWMH specification is still in
    use unchanged and this is a usefull program which is packaged in Debian.
-   [xautomation](http://hoopajoo.net/projects/xautomation.html)
    control X from the command line, and find things on the screen The control interface
    allows mouse movement, clicking, button up/down, key up/down, etc.  The visgrep
    program find images inside of images and reports the coordinates, allowing programs
    to find buttons, etc, on the screen to click on.

    It is packaged in Debian.
-   [Devilspie2](https://www.nongnu.org/devilspie2) (GPL)
    is a a X window matching utility, allowing the user to perform scripted actions on
    windows as they are created. For example you can script a terminal program to always
    be positioned at a specific screen position, or automatically position a window on a
    specific workspace.

    Wayland is not supported by Devillspie2.

    Devilspie2 is in Debian, _active in 2025_.
    -   [Devilspie2 Home](https://www.nongnu.org/devilspie2/).
    -   [devilspie2 - GitHub](https://github.com/dsalt/devilspie2)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
