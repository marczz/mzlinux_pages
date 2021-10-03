---
title: Lightweight Distributions
---

_See also the pages:
{{< iref "distributions" "Distributions" >}},
{{< iref "../network/network" "Forensic Distributions" >}},
{{< iref "firewall#firewall_distributions" "Firewall distributions" >}},
{{< iref "hdrive#rescue_systems" "Rescue Systems" >}}.

---

# Lightweight Distributions

Debian Live and GRML are in the main {{< iref "distributions" "Distributions section" >}}.

-   Wikipedia: {{< wp "Lightweight Linux distribution" >}} includes a
    comparison of lightweight Linux distributions. There is also
    a {{< wp "List of Linux distributions that run from RAM" >}}.
-   A full state of distributions is given in
    [DistroWatch](http://distrowatch.com).
-   [linuxbasis.com](http://www.linuxbasis.com/distributions.html?/distributions1.html)
    gives a review of small, embedded, iso, rescue distributions
-   [ibiblio : linux distributions](http://distro.ibiblio.org/)
-   [busybox](https://busybox.net/) combines many common UNIX
    utilities into a single small executable.
-   [uClibc -- a C library for embedded systems](http://www.uclibc.org/)

-   {{< wp "Alpine Linux" >}},
    [Alpine Linux Home](https://www.alpinelinux.org/)
    is a security-oriented, lightweight Linux distribution based on musl libc and
    busybox. A container requires no more than 8 MB and a minimal installation to disk
    requires around 130 MB of storage.

    Alpine Linux is used heavily in containers (e.g. docker images) on servers, so many
    of its main packages are focused on server services.

    -   [Alpine Linux Wiki](https://wiki.alpinelinux.org/wiki/Main_Page)
-   <a name="bunsenlabs"></a>[BunsenLabs Linux](https://www.bunsenlabs.org/)
    is the continuation of {{< wp "Crunchbang_Linux" "CrunchBang" >}} which stopped
    in 2015. It is a derivative
    of Debian with {{< iref "desktop#openbox" "Openbox window manager" >}},
    {{< iref "desktop#tint2" "tint2 panel" >}}, {{< iref "desktop#jgmenu" "Jgmenu" >}}
    and conky system monitor.
-   [Damn Small Linux](http://www.damnsmalllinux.org/) was a
    business card size (50MB) distribution, stopped since 2012.
-   [Devil Linux](http://www.devil-linux.org/) Linux on a CD that
    can be used as Firewalls / Routers or as a mail / dns / http / ftp
    server. The project was abandonned in 2018.
-   <a name="knoppix"></a>[Knoppix](http://knoppix.net/) is a Live DVD based on Debian
    [Knoppix Wiki](http://knoppix.net/wiki/Main_Page),
    [Knoppix Remastering Howto
    ](http://knoppix.net/wiki/Knoppix_Remastering_Howto)
-   {{< iref "desktop#lxde" "Lxde" >}} (GPL) is a lightweight
    desktop environment. An Lxde desktop is included in Debian,
    in Ubuntu,
    Archlinux, Slitaz, Gentoo, VectorLinux,  Knoppix and other. Look
    at {{< iref "desktop#lxde" "Lxde section" >}} and
    [Lxde Home](http://lxde.org/lxde)
    for details on how to install in your favorite distribution, and
    of included components.
-   [Puppy Linux](http://puppylinux.com/)
    is a collection of multiple Linux distributions using the same set of tools, built
    on top of a unique set of puppy specific applications and configurations. It can
    boot from usb, or cd, flash card, internal hard drive. Puppy boots into a ramdisk
    and loads into RAM.

    The Official dstributions are based on Raspian, Ubuntu, or Slackware, but you can
    build a _Puppy Linux_ image from many distributions.

    -   [puppy linux Wiki](http://wikka.puppylinux.com/HomePage)

-   [SME Server](http://wiki.contribs.org/) is a GPL derivative of
    red-hat enterprise that comes pre-configured and install a server
    with a Apache web server, firewall, Qmail SMTP, IMAP4 and POP3
    servers, samba, Dynamic DNS, ProFTPD ftp server, squid proxy, ldap
    server with an easy configuration user interface. There is also a
    [Sme server french site](http://smeserver.fr/)
-   [Vector Linux](http://vectorlinux.com/) small, fast, Linux derived from
    Slackware. Many versions based on KDE, or LXDE, or Fluxbox and JWM. _last release
    2015_.



# Nas Distributions
-   [FreeNas](http://www.freenas.org/) a FreeBSD distribution
    for NAS server dedicated to X86-64 or amd64.
-   [Openfiler](http://www.openfiler.com/) (GPLv2) is a linux
    distribution for x86_64 NAS, providing NFS, CIFS, iSCSI,
    [block level remote replication](http://www.drbd.org/) _network
    based raid-1_.

# Embedded distributions
-   Wikipedia {{< wp "Comparison of mobile operating systems" >}},
    {{< wp "Mobile operating system" >}}.
-   [Embedded Linux Wiki ](http://elinux.org/Main_Page)
-   [Ångström distribution
    ](http://en.wikipedia.org/wiki/%C3%85ngstr%C3%B6m_distribution)(GPL)
    is a Debian-based Linux distribution for embedded devices. The
    present platforms are Sharp Zaurus, HP ipaq, Nokia 770/800, HTC,
    Gumstix and Kouchuk-Bars, Hawkboard, BeagleBoard, BeagleBone and
    BeagleBone Black, PandaBoard, OpenPandora, OMAPEVM, Base for Openmoko
    distribution, Archos 5/7/101/32/28 ....
-   [FreedomBox](http://wiki.debian.org/FreedomBox)
    is a Debian project to build cheap and simple computer system that
    serves internet services and preserve Freedom.
    -   [FreedomBox TargetedHardware
        ](http://wiki.debian.org/FreedomBox/TargetedHardware)
    -   [FreedomBox Example Projects
        ](http://wiki.debian.org/FreedomBox/ExampleProjects)
    -   [FreedomBox LeavingTheCloud
        ](http://wiki.debian.org/FreedomBox/LeavingTheCloud)
        cloud related user-facing services replacement in Debian.
    -   [Nick Daly Plug-Server](https://bitbucket.org/nickdaly/plugserver)
        is a prototype of some Freedom Box services on a plug computer.
-   [Gentoo Embedded Handbook
    ](https://gentoo-handbook.lugons.org/proj/en/base/embedded/handbook/index.xml)
-   {{< wp "Maemo" >}} is a development platform, the project is abandonned by Nokia,
    but there is still an open source branch
    {{< wp "Maemo#Maemo_Leste" "Maemo Leste" >}} , {{< wp "MeeGo" >}} was a Linux project
    by Intel and Nokia that merge Moblin from Intel and Maemo from
    Nokia. Meego is now merged in {{< wp "Tizen" >}}.
    {{< wp "Mer_(software_distribution)" "Mer" >}} is a fork of MeeGo trying to recover
    a more open (source) mind.
-   {{< wp "OpenEmbedded" >}} is a tool which allows developers to create a fully usable
    Linux base for various embedded systems. It supports Ångström, KaeilOS, Openmoko,
    SHR, SlugOS, WebOS.
    -    [OpenEmbedded Home](http://www.openembedded.org/)
-   <a name= tizen"></a>{{< wp " Tizen" >}} is an open source software platform for
    smartphones, tablets, smart TVs, and more. It is the continuation of Meego by
    Samsung, Intel and als.  Tizen's main components are Linux, Enlightenment and
    WebKit.  [Tizen Homepage](https://www.tizen.org/)
-   {{< wp "Sailfish_OS"  "Sailfish" >}} is an other derivative of Meego
    opensource but with a proprietary interface. It is an active distribution in 2021.
    There are a free version of the OS and a 50$ version including updates and support.
    The supported devices a Gemini PDA, and Sony Xperia phones. There are akso community
    ports to moyorola, redmi, onepluS. More information in
    {{< wp "Sailfish_OS#Hardware_overview" "Hardware overview" >}} of Wikipedia.

## Software suites
-   [linux-to-go](http://www.linuxtogo.org/ "linuxtogo.org") is a
    community site hosting projects dealing with mobile Linux
    applications and systems, i.e. everything in the area of mobile and
    embedded Linux computing.
     Linux-to-go host the Ångström
    Distribution, GPE - G Palmtop Environment, G(PE)\\^2 - GPE Phone
    Edition, OpenZaurus Distribution, OPIE II a fork based on Qtopia
    4.2, and other projects.
    _Linux To Go now replaces [handhelds.org](http://www.handhelds.org/)_
-   [Opie](http://opie.handhelds.org/) The Open Palmtop Integrated
    Environment uses the Qt Toolkit. It is included in various embedded
    Linux distributions such as Ångström, OpenZaurus, Familiar and
    OpenSIMpad.
-   [GPE](http://gpe.linuxtogo.org/) Free Software GUI environment for
    palmtop/handheld which uses the X Window System, and the GTK+
    widget toolkit.

## Embedded Linux devices
-   [alllinuxdevices.com](http://alllinuxdevices.com/)
-   [LinuxToGo: Linux Devices](http://www.linuxtogo.org/gowiki/LinuxDevices)
-   [LinuxDevices.com](http://www.linuxdevices.com/) the embedded Linux
    portal



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
