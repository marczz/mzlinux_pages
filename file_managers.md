<!--
.. description:
.. date: 2015-03-25
.. slug: file_managers
.. tags:
.. link:
.. title: File Managers
-->

[TOC]

# Reference
-   Wikipedia: [w:File manager], [Comparison of file managers].
-   [ArchWiki: list of file managers
    ](https://wiki.archlinux.org/index.php/List_of_applications#File_managers)

# Console File managers {#console}
-   The ancestor of Ncurses file managers is
    [Thomas E. Dickey's ded](http://dickey.his.com/ded/ded.html) now
    superseded by Midnight Commander. The ded design date from 1988,
    but there is still available build and even deb packages on the
    home page.
-   The [w:Midnight Commander] (GPL) is a console application written with Ncurses
(or S-Lang).
    -   The [Midnight Commander Development site
    ](https://www.midnight-commander.org)
    contains the Git development repository.
    -   [Draft of documentation](https://www.midnight-commander.org/wiki/doc)
    -   [Midnight Commander FAQ
        ](https://www.midnight-commander.org/wiki/doc/faq).
    -   [Midnight Commander GitHub repository
        ](https://github.com/MidnightCommander/mc.git)
    -   [ArchWiki: Midnight Commander
        ](https://wiki.archlinux.org/index.php/Midnight_Commander)
    -   As for version 4.8.13  in 2015 mc uses 7.9M res / 6.5M shr.
-   The [emacs dired
    ](http://www.gnu.org/software/emacs/manual/html_node/emacs/Dired.html)
    is  a directory browser integrated in emacs.
-   [Worker](http://www.boomerangsworld.de/cms/worker)
    (GPL) is a light c++ graphical two panels file manager that
    has very low requirements  (X11, nO X toolkit).
    Like MC it provides access to archives and remote file systems.
    It is packaged in Debian and development is active in 2015.<br/>
    As for version 3.4.1 in 2015 it uses 12.6M resident / 9.8M shr.
-   [ranger](http://nongnu.org/ranger/)
    a python (2 or 3) file manager with VI key bindings _and optional
    emacs bindings_. It provides a curses interface with a view on the
    directory hierarchy. _in debian_ .
    _ranger_ development is active in 2015.
    -   Wikipedia [w:Ranger_(file_manager)|ranger].
    -   [ArchWiki: Ranger](https://wiki.archlinux.org/index.php/Ranger).

# Graphical file managers

-   Wikipedia: [w:File manager], [Comparison of file managers].
-   [ArchWiki: File manager functionality
    ](https://wiki.archlinux.org/index.php/File_manager_functionality)

-   [PCManFM](http://pcmanfm.sourceforge.net/)
    <a name="pcmanfm"></a>
    is a
    light GTK-2 file manager, it is comparable to Thunar, but have
    lower requirements, and you may prefer it if you don't have xfce.
    -   _PCManFM_  is part of [lxde](/node/desktop#lxde "internal reference")
    -   _pcmanfm_ memory footprint is 14M Resident/ 10M shr for an empty
        directory but it will grow when opening directories with many
        files (and bitmaps thumbnails) and as so many applications;
        it does not garbage collect when closing.
    -   _pcmanfm_ can be used as a desktop manager daemon with the options
        `--desktop -d`, it then uses 11M resident/8.5 shared
        _before opening any folder_.
    -   Wikipedia: [w:PCMan File Manager].
    -   [Archlinux: PCManFM](https://wiki.archlinux.org/index.php/PCManFM)
        contains a usefull section on [Volume handling
        ](https://wiki.archlinux.org/index.php/PCManFM#Volume_handling),
        that can be done either with _udisks/udisks2_  or _gvfs_.
    -   [Gentoo Wiki: PCManFM](http://wiki.gentoo.org/wiki/PCManFM).
-   [SpaceFM](http://ignorantguru.github.io/spacefm/) (GPL)
    is a fork of PCManFM 0.5 that has been competing with pcmanfm for
    years, but now since march 2015 it has only a minimal maintenance.
    The fork of PCManFM 0.5 was did by developers that did not want the gvfs
    bindings that were added to PCManFM, and rather preferred
    the [udevil](http://ignorantguru.github.io/udevil/)
    <a name="udevil"></a> mount program.
    SpaceFM can use udevil, pmount or udisks/udisks2, and if PCManFM
    has kept gvfs, it is no longer mandatory and can be replaced by
    udisks/udisks2.<br />
    The memory footprints of the two products is similar and they have
    the same functionality of a tabbed File Manager and Desktop
    manager.<br />
    What distinguish SpaceFM is the extended configurations options
    including an easy system of plugins, allowing easy shell plugins.
    -   [SpaceFM GitHub repository
        ](https://github.com/IgnorantGuru/spacefm)
    -   [IgnorantGuru GitHub repositories
        ](https://github.com/IgnorantGuru/spacefm)
        [IgnorantGuru](http://igurublog.wordpress.com/)
        is the main developer of SpaceFM, and his
        [GitHub repositores
        ](https://github.com/IgnorantGuru/spacefm)
        includes SpaceFM and many
        [system scripts](http://igurublog.wordpress.com/downloads/).
    -   [udevil](http://ignorantguru.github.io/udevil/) (GPL)
    -   [ArchWiki: SpaceFM
        ](https://wiki.archlinux.org/index.php/SpaceFM)
        <a name="udevil"></a>
        is a command line Linux program which mounts and unmounts
        removable devices without a password, shows device info, and
        monitors device changes. It can also mount ISO files, nfs://,
        smb://, ftp://, ssh:// and WebDAV URLs, and tmpfs/ramfs
        filesystems.<br /> it includes a mounting daemon
        _devmon_. _udevil_ has no dependency on udisks, gvfs, fuse,
        policykit, consolekit, etc.<br />
        _udevil_ takes 1.5M resident / 1.2M shared; devmon add 1.9M
        resident / 1.3M shared.
    -   [SpaceFM User-Contributed Plugins
        ](https://github.com/IgnorantGuru/spacefm/wiki/plugins),
        [IgnorantGuru SpaceFM plugins GitHub repository
        ](https://github.com/IgnorantGuru/spacefm/wiki/plugins),
        [trile7 script directory
        ](http://code.google.com/p/bashscripts/source/browse/trunk/)
-   [w:Thunar] (GPL) the
    [xfce](http://xfce.org/) window manager.
    -    [Thunar Home](http://docs.xfce.org/xfce/thunar/start)
    -    Thunar project was publishing  a
         _memory usage page_ (unavailable today?)
         where there is a comparison between Konqueror, ROX, Nautilus and
         Thunar memory footprints. They advocate that the data size of
         thunar is only 3M which is roughly the overhead of the application.
         It is also what I experience, when I launch Thunar I get an
         Overhead of 3M. Note also that the amount of unshared memory is
         of course what is meaningfull in these comparisons, but this
         unshared memory is **not** the difference between resident and
         shared memory, because what is named _shared_ is what is potentially
         shared, to add a single Qt application on a gtk desktop is costly
         even if most libraries are potentially shared.
-   [gentoo file manager](http://www.obsession.se/gentoo/)
    Is a GTK3 2 panels, commander like, file manager, it is not
    related to the Gentoo Linux distribution. Gentoo uses the
    [w:GIO_(GNOME)|GIO] library. _Gentoo_ uses 18M resident / 12M shared.
-   [emelfm2](http://emelfm2.net/) is a two panels,
    Norton commander (or Midnight commander)
    like file manager for  Gtk3. Emlfm2 uses 16M resident memory / 12M shared.
    Emelfm2 is no longer available in main Debian,but is still under
    active development in 2014. It is [proposed in Ubuntu
    ](http://packages.ubuntu.com/search?keywords=emelfm),
    you can also find the latest
    deb package on [emlfm2 PPA](https://launchpad.net/~emelfm2).
    -   [Emelfm2 User Guide](http://emelfm2.net/wiki/UserGuide)
-   If you install kde you can do nothing but using the heavy
    [Konqueror](http://konqueror.kde.org/)
-   A Gnome user can not avoid
    [Nautilus](https://wiki.gnome.org/action/show/Apps/Nautilus)
    now renamed [w:GNOME Files].
    -   [ArchWiki: GNOME Files
        ](https://wiki.archlinux.org/index.php/GNOME_Files)
    -   Nautilus seems
        became leaner over years, I previously experienced  49M Res/25M Shr
        where now it is 27M/17M. Its dependencies are also now smaller,
        allowing to install it even if you don't use a full gnome desktop.
        _But for debian/ubuntu users take care that the recommended packages
        may add a lot of dependencies._

# Web File managers

-   [shellinbox section](/node/raspberry#shellinabox "internal reference")
-   [elfinder](http://elfinder.org/) (BSD License)
    elFinder is a file manager for web, written in JavaScript using jQuery UI.
    It can create and extract archives. A QuickLook function allows to preview
     common types of files like images, flash, text, audio, video and pdf.
    ElFinder integrates with _CKEditor_,
    _Tiny MCE_, _elRTE_,  Drupal, WordPress, web2py.
-   [eXtplorer](http://extplorer.sourceforge.net/) (GPL or MPL)
     is a web-based File Manager.
     You can use it to login to a local FTP server,
     or it can be configured to use WebDav. _last release 2011_.
-   [MCFileManager](http://www.tinymce.com/wiki.php/MCFileManager)
    (MIT and GPL licenses)
    is an online file management utility, available as PHP and
    .NET, that is integrated with
    [TinyMCE](http://www.tinymce.com/index.php) or other similar editors.
-   [KCFinder](http://kcfinder.sunhater.com/) (GPL)
    is a php/ajax web file manager which can be integrated into FCKeditor,
    CKEditor, and TinyMCE WYSIWYG web editors.

<!-- Local Variables: -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
