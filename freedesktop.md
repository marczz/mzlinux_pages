<!--
.. description:
.. date: 2015-06-20
.. slug: freedesktop
.. tags:
.. link:
.. book: mzlinux
.. title: Freedesktop
-->

[TOC]

---

# References
-   [freedesktop.org](http://www.freedesktop.org/) a base platform
    (both software and standard) for desktop software.
-   [Freedesktop Software](http://freedesktop.org/wiki/Software/)
-   [freedesktop spécifications
    ](http://www.freedesktop.org/wiki/Specifications):
    -   [Menu specifications
        ](http://standards.freedesktop.org/menu-spec/latest/)
    -   [Mime Actions Specification
        ](http://standards.freedesktop.org/mime-apps-spec/latest/)
    -   [Shared Mime Info Specification
        ](http://www.freedesktop.org/wiki/Specifications/shared-mime-info-spec)
    -   [Base-Directory Specification
        ](http://standards.freedesktop.org/basedir-spec/latest/)
    -   [Desktop Entry Specification
        ](http://standards.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html):
        [the exec key
        ](http://standards.freedesktop.org/desktop-entry-spec/latest/ar01s06.html)
    -   [Recent File Specification
        ](http://www.freedesktop.org/wiki/Specifications/recent-file-spec)
    -   [Icon Themes Specification
        ](http://standards.freedesktop.org/icon-theme-spec/icon-theme-spec-latest.html)
    -   [Desktop Application Autostart Specification
        ](http://standards.freedesktop.org/autostart-spec/latest/)
-   [python-xdg](http://freedesktop.org/wiki/Software/pyxdg) is a
    python library to access freedesktop.org standards.
    -   [python-xdg documentation](http://pyxdg.readthedocs.org/en/latest/index.html)

# XDG menus
-   [XDG Menu in LXDE](http://wiki.lxde.org/en/Main_Menu)
-   [ArchLinux: xdg-menu](https://wiki.archlinux.org/index.php/Xdg-menu).
-   [xdg-utils](http://portland.freedesktop.org/)
    is a set of command line utilities for Free Desktop:  creating
    menus, opening files, setting mime types it includes the command
    [man:xdg-desktop-menu]
    which is used  for (un)installing freedesktop menu items i.e. `.desktop` files
    for freedesktop compatible environments.
-   To build the full desktop menu many distribution use a command to browse the freedesktop
    menu hierarchy `xdg-menu` is decribed in
    [Archlinux: XdgMenu](https://wiki.archlinux.org/index.php/Xdg-Menu).
-   In Debian the freedesktop menus are generated from
    [Debian Menus System
    ](http://www.debian.org/doc/packaging-manuals/menu.html/)
    by the command
    [`install-menu`
    ](http://www.debian.org/doc/packaging-manuals/menu.html/ch7.html)

    with the configuration `/etc/menu-methods/menu-xdg` from the
    package `menu-xdg` to use them with default config
    `$XDG_MENU_PREFIX` must be set to `debian-`.
-   Debian is using the alternate debian menu, with the increasing spreading
    of Free desktop menus through `.desktop` files, it becomes more difficult to
    maintain a debian menu file for each package. There was a
    [Proposal: using Desktop entries with the Debian menu system
    ]( https://wiki.debian.org/Proposals/DebianMenuUsingDesktopEntries) which
    compare Debian menus with `.xdesktop` files. An alternative is to switch
    debian packaging to freedesktop menus, it is developped in
    [Debian and application-menu policies
    ](http://lwn.net/Articles/597697/).


# XDG Default application.
The freedesktop way of opening applications is
thru `xdg-open` and the Mime type of the file,
it is explained in Freedesktop
[Desktop Entry Specification
](http://standards.freedesktop.org/desktop-entry-spec/desktop-entry-spec-latest.html),
[Mime Actions Specification
](http://standards.freedesktop.org/mime-apps-spec/latest/)
and:

-   [ArchLinux: Default applications
    ](https://wiki.archlinux.org/index.php/Default_Applications)
    _describe mime database, xdg-open, xdg-mime, ect._
    [Xdg user directories
    ](https://wiki.archlinux.org/index.php/XDG_user_directories),
    [Desktop Entries](https://wiki.archlinux.org/index.php/Desktop_entries)

Some [alternatives are available
](https://wiki.archlinux.org/index.php/Default_Applications#Utilities),
they try to provide more flexibility.

# Freedesktop Directories
The Base Directories are used when looking for for user configuration.

-   XDG Base Directories are specified in
    [Freedesktop Base-Directory Specification
    ](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html).
-   The [file-hierarchy(7) overview
    ](https://www.freedesktop.org/software/systemd/man/file-hierarchy.html)
    describe the unix file hierarchy used by freedesktop and systemd. You find ther the
    use of `XDG_RUNTIME_DIR`.
-   [ArchWiki: XDG Base Directory support
    ](https://wiki.archlinux.org/index.php/XDG_Base_Directory_support)
    catalog software using the XDG Base Directory Specification.
-   [GNOME Goal: XDG Base Directory Specification Usage
    ](https://wiki.gnome.org/Initiatives/GnomeGoals/XDGConfigFolders)
    explains why and how gnome siftware should implement XDG base
    directories, and list the present support in gnome programs.
-   [ArchWiki: XDG user directories
    ](https://wiki.archlinux.org/index.php/XDG_user_directories)


The [freedesktop base directories
](http://standards.freedesktop.org/basedir-spec/latest/)
that follow is used by all freedesktop compatible application. They
have a default that can be overrided by exporting in your environment
the variables.

-   `$XDG_DATA_HOME` default `$HOME/.local/share` contains user-specific
    data files.
-   `$XDG_CONFIG_HOME` default `$HOME/.config` contains user specific
    configuration files.
-   `$XDG_DATA_DIRS` default `/usr/local/share/:/usr/share/` are
    directories seperated with a colon ':' to search for data in
    addition of `$XDG_DATA_HOME`
-   `$XDG_CONFIG_DIRS` default `/etc/xdg` are directories seperated with
    a colon ':' to search for configuration files in addition of
    `$XDG_CONFIG_HOME`.  Configurations are searched in directory
    order, using the first match.
-   `$XDG_CACHE_HOME` default `$HOME/.cache` for temporary data.
-   `$XDG_RUNTIME_DIR` temporary runtime, his life must be the
    session, and it must be owned by the user with access mode 0700
    _see full requirement in the
    [specification
    ](http://standards.freedesktop.org/basedir-spec/latest/)_
    Usually it is set by `pam_systemd` at login and there is no need
    to change it.  You can get its value from the environment variable
    `$XDG_RUNTIME_DIR`.


The user directories are the directories under `$HOME` used by your
desktop to store your data their default set in
`$XDG_CONFIG_DIRS/user-dirs.defaults` usually
`/etc/xdg/user-dirs.defaults` it default to:

    DESKTOP=Desktop
    DOWNLOAD=Downloads
    TEMPLATES=Templates
    PUBLICSHARE=Public
    DOCUMENTS=Documents
    MUSIC=Music
    PICTURES=Pictures
    VIDEOS=Videos

These system defaults can be changed in  this file.

The program [man:xdg-user-dirs-update] is run very early in the login
phase. This program reads a configuration file, and a set of default
directories. It then creates localized versions of these directories
in the users home directory and sets up a config file in
`$(XDG_CONFIG_HOME)/user-dirs.dirs` _defaults to_ `~/.config` that
applications read to find these directories.

You can customize the values in your `~/.config/user-dirs.dirs`;
as an example if you have a non english locale and wish to force these
directories to keep their default english names run:

    $ LC_ALL=C xdg-user-dirs-update

That will create the  `~/.config/user-dirs.dirs`. It also creates an
`~/.config/user-dirs.locale` used to remember the locale used and
allowing to translate names if it changes.

An other popular alternative to avoid to create too many directories
under `$HOME` is:

    MUSIC=Documents/Music
    PICTURES=Documents/Pictures
    VIDEOS=Documents/Videos

The [Debian Wiki](https://wiki.debian.org/DotFilesList) list the
dotfiles we can find in a Debian system, their role and the programs
that use them. TMost of them are not yet following the XDG standard,
many programs may be launched with a specific environment on command
line option to make them comply with xdg satndard as explained in
[ArchWiki: XDG Base Directory support
](https://wiki.archlinux.org/index.php/XDG_Base_Directory_support).
You can also symlink many of these files or directories inside the
corresponding XDG Base directory.


# Menu specification

The reference is [Freedesktop Menu Specification
](http://www.freedesktop.org/wiki/Specifications/menu-spec)
see also the Gnome:
[Desktop Menu Specification](http://developer.gnome.org/menu-spec/).

-   `$XDG_CONFIG_DIRS/menus/${XDG_MENU_PREFIX}applications.menu`
    is a file containning the  XML definition of the main application
    menu layout, with the first match strategy you can overide the
    system wide menu with `$XDG_CONFIG_HOME/${XDG_MENU_PREFIX}applications.menu`.
-   `$XDG_CONFIG_DIRS/menus/applications-merged/` is the default merge
    directory included in the `<DefaultMergeDirs>` element of the previous file.
-   `$XDG_DATA_DIRS/applications/` contains a .desktop file for each menu item,
    desktop entries are collected from all of them, but in case of name
    conflict the first one is used.
-    `$XDG_DATA_DIRS/desktop-directories/` contains .directory file giving
    directory entries in the menu layout.

# Autostart applications
-   [ArchWiki Autostarting
    ](https://wiki.archlinux.org/index.php/Autostarting)
-   [ArchWiki Desktop entries
    ](https://wiki.archlinux.org/index.php/Desktop_entries#Autostart)

Applications referenced by a `.desktop` file in
`$XDG_CONFIG_DIRS/autostart` and `$XDG_CONFIG_HOME`
may be autostarted  by xdg compliant window managers.

In additions to generic keys, autostart  `.desktop` files may contain
additional keys:

-   `Hidden` when true, the application is ignored
-   `OnlyShowIn` and `NotShowIn` can list desktop environments
    in which the application is only (not?) started.
    These two keys are exclusives each other.
-   `TryExec`: Tha application is started only when the named exec
    exist. It can be an absolute path or a name to be looked for in `$PATH`.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
