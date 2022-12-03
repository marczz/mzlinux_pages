---
title: File Managers
---

# Reference
-   Wikipedia: {{< wp "File manager" >}}, [Comparison of file managers].
-   [ArchWiki: list of file managers
    ](https://wiki.archlinux.org/index.php/List_of_applications#File_managers).
-   [File manager functionality - ArchWiki
    ](https://wiki.archlinux.org/title/File_manager_functionality).

# Console File managers {#console}
-   The ancestor of Ncurses file managers is
    [Thomas E. Dickey's ded](http://dickey.his.com/ded/ded.html) now
    superseded by Midnight Commander. The ded design dates from 1988,
    but there is still available build and even deb packages on the
    home page.
-   The {{< wp "Midnight Commander" >}} (GPL) is a console application written with
    Ncurses (or S-Lang) it is an old application still actively maintained in 2022.
    -   [Midnight Commander Development site](https://www.midnight-commander.org)
    -   [Midnight Commander's Github repository](https://github.com/MidnightCommander/mc).
    -   [Draft of documentation](https://www.midnight-commander.org/wiki/doc)
    -   [Midnight Commander FAQ](https://www.midnight-commander.org/wiki/doc/faq).
    -   [ArchWiki: Midnight Commander
        ](https://wiki.archlinux.org/index.php/Midnight_Commander)
    -   As for version 4.8.28  in 2022 mc uses 12.9M res / 7.8M shr.
-   The [emacs dired
    ](http://www.gnu.org/software/emacs/manual/html_node/emacs/Dired.html)
    is  a directory browser integrated in emacs.
-   [ranger](https://ranger.github.io/) (GPL-3.0)
    a python file manager with VI key bindings _and optional
    emacs bindings_. It provides a curses interface with a view on the
    directory hierarchy. _in debian_ .
    _ranger_ _development is active in 2022_.

    As ranger is python powered it has medium footprint, lighter than GUI file managers,
    but heavier than console file manager like mc or n³. It uses 27M res / 11M shr.
    -   Wikipedia {{< wp "Ranger_(file_manager)"  "ranger" >}}.
    -   [ArchWiki: Ranger](https://wiki.archlinux.org/index.php/Ranger).
    -   [ranger Wiki](https://github.com/ranger/ranger/wiki).
    -   [ranger User Guide](https://github.com/ranger/ranger/wiki/Official-User-Guide).
-   [nnn](https://github.com/jarun/nnn/)
    n³ a terminal file manager. _nnn_ can analyze disk usage, batch rename, launch apps
    and pick files. There are many plugins to extend the capabilities further
    e.g. preview, (un)mount disks, find & list, file/dir diff, upload files.
    _In Debian._

    n³ has very low memory footprint 4.2M res. / 3.2 M shared.
    -   [nnn Wiki](https://github.com/jarun/nnn/wiki)
    -   [nnn - ArchWiki](https://wiki.archlinux.org/index.php/Nnn)
    -   There are many [nnn plugins for neovim on GitHub
        https://github.com/topics/neovim-plugin?q=nnn).
-   [Vifm](https://vifm.info/) (GPL-2.0)
    Vifm is a file manager with curses interface, which provides Vim-like environment.
    It is packaged in Debian.
    -   [Vifm - GitHub](https://github.com/vifm/vifm).
    -   [Vifm Wiki](https://wiki.vifm.info/index.php/Main_Page).
    -   [Vifm - ArchWiki](https://wiki.archlinux.org/title/Vifm).
    -   Vifm version 0.12 _2022_ uses 8M res / 5M shared

# Graphical file managers

-   Wikipedia: {{< wp "File manager" >}}, [Comparison of file managers].
-   [ArchWiki: File manager functionality
    ](https://wiki.archlinux.org/index.php/File_manager_functionality)

-   <a name="pcmanfm"></a>[PCManFM](https://wiki.lxde.org/en/PCManFM)
    is a
    light GTK-2 file manager, it is comparable to Thunar, but have
    lower requirements, and you may prefer it if you don't have xfce.
    _PCManFM_  is part of {{< iref "desktop#lxde" "lxde" >}}
    -   _pcmanfm_ memory footprint is 14M Resident/ 10M shr for an empty
        directory but it will grow when opening directories with many
        files (and bitmaps thumbnails) and as so many applications;
        it does not garbage collect when closing.
    -   _pcmanfm_ can be used as a desktop manager daemon with the options
        `--desktop -d`, it then uses 11M resident/8.5 shared
        _before opening any folder_.

    <a name="pcmanfm-qt"></a>{{< iref "desktop#lxqt" "lxqt" >}} replaces the GTK-2 version
    by [lxqt/pcmanfm-qt](https://github.com/lxqt/pcmanfm-qt) (GPL)
    a Qt port of PCManFM and libfm. PCManFM-QT is wayland compatible as it is based on
    QT-5.

    PCManFM can also be built with GTK3, this build is used in arch-linux package
    _pcmanfm-gtk3_ and in the Nix package.

    -   Wikipedia: {{< wp "PCMan File Manager" >}}.
    -   [Archlinux: PCManFM](https://wiki.archlinux.org/index.php/PCManFM)
        contains a usefull section on [Volume handling
        ](https://wiki.archlinux.org/index.php/PCManFM#Volume_handling),
        that can be done either with _udisks/udisks2_  or _gvfs_.
    -   [Gentoo Wiki: PCManFM](https://wiki.gentoo.org/wiki/PCManFM).
-   [SpaceFM](http://ignorantguru.github.io/spacefm/) (GPL)
    is a fork of PCManFM 0.5 that has been competing with pcmanfm for years. The fork of
    PCManFM 0.5 was did by developers that did not want the gvfs bindings that were
    added to PCManFM, and rather preferred the
    [udevil](http://ignorantguru.github.io/udevil/) mount program.  SpaceFM can use
    udevil, pmount or udisks/udisks2, and if PCManFM has kept gvfs, it is no longer
    mandatory and can be replaced by udisks/udisks2.

    The memory footprints of the two products is similar and they have the same
    functionality of a tabbed File Manager and Desktop manager.

    What distinguish SpaceFM is the extended configurations options including an easy
    system of plugins, allowing easy shell plugins.

    Since march 2015 spacefm  had only a minimal maintenance, which completely stopped
    in 2018.

    There is a new fork on [thermitegod/spacefm](https://github.com/thermitegod/spacefm).
    -   [SpaceFM legacy GitHub repository](https://github.com/IgnorantGuru/spacefm)
    -   IgnorantGuru was the main developer of SpaceFM, and his
        [GitHub repositories](https://github.com/IgnorantGuru/)
        includes SpaceFM, many
        [system scripts](http://igurublog.wordpress.com/downloads/)
        and [udevil](http://ignorantguru.github.io/udevil/) (GPL)
    -   [ArchWiki: SpaceFM](https://wiki.archlinux.org/index.php/SpaceFM)
    -   <a name="udevil"></a>[udevil](http://ignorantguru.github.io/udevil/)
        is a command line Linux program which mounts and unmounts removable devices
        without a password, shows device info, and monitors device changes. It can also
        mount ISO files, nfs://, smb://, ftp://, ssh:// and WebDAV URLs, and tmpfs/ramfs
        filesystems.<br /> it includes a mounting daemon _devmon_. _udevil_ has no
        dependency on udisks, gvfs, fuse, policykit, consolekit, etc.

        _udevil_ takes 1.5M resident / 1.2M shared; devmon add 1.9M
        resident / 1.3M shared.
    -   [SpaceFM User-Contributed Plugins
        ](https://github.com/IgnorantGuru/spacefm/wiki/plugins),
-   {{< wp "Thunar" >}} (GPL) the [xfce](http://xfce.org/) window manager.
    -    [Thunar Home](http://docs.xfce.org/xfce/thunar/start)
    -    Thunar project was publishing  a _memory usage page_ (unavailable today?)
         where there is a comparison between Konqueror, ROX, Nautilus and Thunar memory
         footprints. They advocate that the data size of thunar is only 3M which is
         roughly the overhead of the application.  It is also what I experience, when I
         launch Thunar I get an Overhead of 3M. Note also that the amount of unshared
         memory is of course what is meaningfull in these comparisons, but this unshared
         memory is **not** the difference between resident and shared memory, because
         what is named _shared_ is what is potentially shared, to add a single Qt
         application on a gtk desktop is costly even if most libraries are potentially
         shared.
-   [Worker](http://www.boomerangsworld.de/cms/worker)
    (GPL) is a light c++ X11 graphical two panels file manager that has very low
    requirements (X11, no X toolkit).  It provides access to archives and remote file
    systems.  It is packaged in Debian and development is active in 2022.

    As for version 3.4.1 in 2015 it uses 12.6M resident / 9.8M shr.
-   If you install kde you can do nothing but using the heavy
    [Konqueror](http://konqueror.kde.org/)
-   A Gnome user can not avoid
    [Nautilus](https://wiki.gnome.org/action/show/Apps/Nautilus)
    now renamed {{< wp "GNOME Files" >}}.
    -   [ArchWiki: GNOME Files
        ](https://wiki.archlinux.org/index.php/GNOME_Files)
    -   Nautilus seems
        became leaner over years, I previously experienced  49M Res/25M Shr
        where now it is 27M/17M. Its dependencies are also now smaller,
        allowing to install it even if you don't use a full gnome desktop.
        _But for debian/ubuntu users take care that the recommended packages
        may add a lot of dependencies._

# Web File managers

-   [CKFinder](https://ckeditor.com/ckfinder/) is part of
    [CKEditor 5](https://ckeditor.com/ckeditor-5/) (Open Source and commercial)
-   [elfinder](https://github.com/Studio-42/elFinder) (BSD License)
    elFinder is a file manager for web, written in JavaScript using jQuery UI.  It can
    create and extract archives.

    A QuickLook function allows to preview common types of files like images, flash,
    text, audio, video and pdf.

    ElFinder integrates with
    [_CKEditor_, _Tiny MCE_, _elRTE_](https://github.com/studio-42/elFinder/wiki#howtos),
    Drupal, Django, Laravel, Roundcube, Symfony, TikiWiki, WordPress, Yii,
    [zenphoto](https://www.zenphoto.org/).
-   [File Browser](https://filebrowser.org/)
    is a GoLang web server giving users remote access to the filesystem.
    -   [File Browser GitHub](https://github.com/filebrowser/filebrowser).
-   [Pydio Cells](https://pydio.com/en/pydio-cells/overview) (AGPL and commercial)
    is a Go language content sharing platform. It requires a MySQL/MariaDB database.
    The open source [server is hosted on GitHub](https://github.com/pydio/cells)
    as well as the
    [client](https://github.com/pydio/cells-client).
-   [Tiny File Manager](https://tinyfilemanager.github.io/) (GPL-3.0)
    is a Web php based file manager in a single php file. It allows storing, uploading,
    editing and managing files and folders online via web browser, and  upports syntax
    highlighting for over 150+ languages and over 35+ themes.
    -   [Tiny File Manager - GitHub](https://github.com/prasathmani/tinyfilemanager).



<!-- Local Variables: -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
