---
title: DVD and CD Recording
---


# General information
-   Wikipedia: {{< wp "Comparison of disc image software" >}};
    {{< wp "Comparison of disc authoring software" >}}
-   Debian Wiki:
    -   [CD DVD](https://wiki.debian.org/CDDVD),
    -   [CD DVD Tools](https://wiki.debian.org/CDDVDTools),
    -   [Burn CD](https://wiki.debian.org/BurnCd) is a recipe list for
        burning a CD from the command line.
-   ArchWiki:
    -   [Optical disc drive
        ](https://wiki.archlinux.org/index.php/Optical_disc_drive)
        burning, playback, ripping, troubleshooting.
    -   [DVD Backup
        ](https://wiki.archlinux.org/index.php/Dvdbackup),
    -   [Blu-ray
        ](https://wiki.archlinux.org/index.php/Blu-ray)
-   Ubuntu Help:
    -   [Cd/Dvd Burning
        ](https://help.ubuntu.com/community/CdDvd/Burning)
    -   [How do I enable restricted codecs to play DVDs?
        ](https://help.ubuntu.com/stable/ubuntu-help/video-dvd-restricted.html)
    -   [RestrictedFormats/PlayingDVDs - Community Help Wiki
        ](https://help.ubuntu.com/community/RestrictedFormats/PlayingDVDs)
-   [YoLinux Tutorial: Burning a CD or DVD
    ](http://www.yolinux.com/TUTORIALS/LinuxTutorialCDBurn.html)
-   [DVD FAQ](http://dvddemystified.com/dvdfaq.html) from
    dvddemystified.com.
-   [Blu-ray Disc/ DVD+RW/+R/ -R/-RW for Linux](http://fy.chalmers.se/~appro/linux/DVD+RW/) _2008_
-   Quite outdated: [CD-Writing-HOWTO
    ](http://en.tldp.org/HOWTO/CD-Writing-HOWTO.html) _2000_,
    [MP3-CD-Burning HOWTO](http://en.tldp.org/HOWTO/MP3-CD-Burning/index.html) _2001_
-   [Casterless - CD burning
    ](http://www.troubleshooters.com/linux/coasterless.htm) _2005_
    explains the use of
    {{< man "isoinfo" >}} to read accurately a cdrom.
-   [Twiki Md5sum after burning
    ](http://twiki.org/cgi-bin/view/Wikilearn/CdromMd5sumsAfterBurning)

# Recording tools
dvd+rw-tools
:   Is a set of tools to master the DVD media, both +RW/+R and -R[W]. The main page is
    [DVD+RW/+R/-R[W] for Linux](http://fy.chalmers.se/~appro/linux/DVD+RW/)
    and
    [dvd+rw-tools burning tips](http://crashrecovery.org/oss-dvd/HOWTO-ossdvd.html),
    [Coasterless DVD Burning](http://www.troubleshooters.com/linux/coasterless_dvd.htm)
    is a tutorial to dvd+rw-tools.

cdrdao
:   [Cdrdao](http://cdrdao.sourceforge.net/)
    records audio CD-Rs in disk-at-once (DAO) mode, based on
    a textual description of the CD contents.
:   refs [cdrdao(1)](http://man.cx/cdrdao(1))

<a name="cdrtools"></a>{{< wp "cdrtools" >}}
:   is a collection of programs for recording CDs and DVDs, created by Jörg
    Schilling. After a contreversy on the project license
    {{< iref "#cdrkit" "cdrkit" >}} was forked and Debian, Ubuntu, and Fedora opted for
    {{< iref "#cdrkit" "cdrkit" >}}.

    Cdtools works with many different brands of CD recorders, fully
    supports multi-sessions and provides human-readable error
    messages.
    The main utilities are _cdrecord_ renamed {{< man "wodim" >}} in the
    _cdrkit_ fork, _cdda2wav_ renamed {{< man "icedax" >}}, and _mkisofs_
    renamed {{< man "genisoimage" >}}.

    ArchLinux use _cdrtools_ and you fInd cdrtools recipes in
    [Optical disc drive
    ](https://wiki.archlinux.org/index.php/Optical_disc_drive)
    for burning CD/DVD, playback, ripping, troubleshooting.


    The mkisofs program is used as a pre-mastering program in _cdrtools_ suite; i.e.,
    it generates the ISO9660 filesystem. Mkisofs is used for writing
    CD-ROMs, and includes support for creating bootable El Torito
    CD-ROMs.  _mkisofs_ is renamed {{< man "genisoimage" >}} in the _cdrkit_
    fork of _cdrtools_.

<a name ="cdrkit"></A>[cdrkit](http://cdrkit.org/) (GPLv2)
:   cdrkit is a suite of command line programs for recording CDs
    and DVDs, blanking CD-RW media, creating ISO-9660 filesystem
    images, extracting audio CD data.
    cdrkit is a fork of cdrtools

    _cdrecord_ is renamed {{< man "wodim" >}}, _cdda2wav_ is renamed {{< man "icedax" >}},
    and _mkisofs_ is renamed {{< man "genisoimage" >}} in the _cdrkit_ fork.
    _cdrkit_  is compatible with the
    _cdrtools_ suite.

    {{< man "genisoimage" >}} is the name of _mkisofs_ fork, an introductionis
    in [Debian Wiki - genisoimage and xorrisofs
    ](https://wiki.debian.org/genisoimage)


tovid
:   [tovid](http://tovid.wikia.com/wiki/Tovid_Wiki) (GPL)
    is a collection of DVD authoring tools. It can convert your video files to the
    correct format, generate navigational menus, and create and burn the disc image.

    -  [tovid  GitHub repository](https://github.com/tovid-suite/tovid)

xorriso
:   [xorriso](https://dev.lovelyhq.com/libburnia/web/wikis/home)
    is a command line and dialog application, which creates, loads,
    manipulates, and writes ISO-9660 file system images with Rock
    Ridge extensions.

repair tools
:   [recoverdm](http://www.vanheusden.com/recoverdm/) help to recover
    disks with damaged sectors.
:   [ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html)
    a data recovery tool, can also be used with cdrom.

# Front Ends

Video encoding front ends (*that are also audio-ables*) are in the
section {{< iref "video_edit" "video encoders" >}}

[bashburn](https://sourceforge.net/projects/bashburn/files/bashburn/)
:   cd/dvd burning and ripping shell script.  BashBurn handles burning of multiple image
    formats, including ISO, bin/cue and nrg.

    Last release on sourceforge is 2.2 beta 2008, there is also a
    [Bashburn - GitHub](https://github.com/aelinden/BashBurn/) with few changes, mainly
    related to german language translations.

Brasero (GPL)
:   [Brasero](https://wiki.gnome.org/Apps/Brasero) uses *wodim* and
    communicate thru the dbus. Brasero is a gtk3 application with no specific gnome
    dependency. Brasero can also use cdrkit It is an active project, in Debian.

Cdlabelgen
:   _Cdlabelgen_ is a utility which generates frontcards and traycards (in
    `PostScript(TM)` format) for CD jewelcases.
:   refs: [cdlabelgen(1)](http://man.cx/cdlabelgen(1))
    [Online CD/DVD Inserts and Envelopes](http://www.aczone.com/tools/cdinsert/form.html)

[cdw](http://cdw.sourceforge.net/) (GPL-2.0)
:   Cdw  is a ncurses text front end for many cd/dvd record tools
    cdrecord/wodim, mkisofs/genisoimage, growisofs, dvd+rw-mediainfo, dvd+rw-format.

    Last release 0.8.1, in 2016, this release is in Debian, no repository with
    development code.

[K3b](https://userbase.kde.org/K3b)
:   A frontend to cdrecord, cdrdao, and growisofs. It allows to create data, audio,
    video, mixed-mode, emovix CDs, DVD-R(W) burning, CD/DVD Ripping. K3b is developed
    using KDe desktop, but has a reasonable dependency list, you need QT, and kdelibs
    but kde-base is optional. It is in Debian.

[X-CD-Roast](http://www.xcdroast.org/) (GPL)
:   X-CD-Roast is a CD-burning software that provides a GUI interface for commands
    like _cdrecord_ and _mkisofs_. There is a
    [PPA with deb packages](http://www.xcdroast.org/release/ubuntu_install.html).
