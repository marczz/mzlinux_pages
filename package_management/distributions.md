---
title: Linux Distributions
---

{{% toc /%}}

See also the  {{< iref "lightweight_distributions" "Lightweight Linuxes" >}} section.

A full state of distributions is given in
[DistroWatch](http://distrowatch.com).


# Ubuntu

-   Richard Stallman gave an advice on
    [Ubuntu Spyware: What to Do?](http://www.gnu.org/philosophy/ubuntu-spyware.html)
    quoting this article:

    > Ubuntu,[...] has installed surveillance code. When the user searches
    >  her own local files for a string using the Ubuntu desktop, Ubuntu
    > sends that string to one of Canonical's servers.
    > ......
    > If you ever recommend or redistribute GNU/Linux,
    >  please remove Ubuntu from the distros you recommend or redistribute.

-   [Ubuntu](http://www.ubuntu.com/),
    [wiki.ubuntu](https://wiki.ubuntu.com/),
    [Documentation for Ubuntu](https://help.ubuntu.com/),
    [Xubuntu](http://www.xubuntu.org/),
    [Lubuntu](https://wiki.ubuntu.com/Lubuntu) *LXDE+Ubuntu*
     targeted at low-spec hardware, can run from 128MB RAM.
-   [Ubuntu Packages](http://packages.ubuntu.com)
-   [How to install Ubuntu on low memory systems
    ](https://help.ubuntu.com/community/Installation/LowMemorySystems).
-   [Ubuntu  Guide](http://ubuntuguide.org/) browse on all categories of software
    you may want to install on Ubuntu or any other distribution.
-   [Ubuntu Low End System Support
    ](https://help.ubuntu.com/community/LowEndSystemSupport)
-   [Documentation for latest distribution
    ](https://help.ubuntu.com/) contains
    _Ubuntu Desktop Help_,    _Ubuntu Server Guide_,   _Installing Ubuntu_.
-   [ubuntugeek](http://www.ubuntugeek.com/) site
    contains tips,howtos,tutorials and articles about Ubuntu Linux.
-   [Linux Mint](http://www.linuxmint.com/)
    is a distribution aimed at the ease of use.  It is based on Debian
    and Ubuntu and provides full multimedia support. There are many
    variants of Mint, the main one is based on Ubuntu, there is alo a
    Debian edition based on Debian, and alternate fluxbox or lxde
    desktop.
-   [Pepermint Linux OS](https://en.wikipedia.org/wiki/Peppermint_Linux_OS)
    is a cloud-centric OS based on Lubuntu, with LXDE as default user interface.  It
    creates a hybrid desktop that integrates both cloud and local application.  It
    provides {{< wp "Site-Specific Browsers" >}} or SSBs. Essentially many modern web
    applications offer much advanced functionality and SSBs allow these apps to be more
    directly integrated with the desktop. Ice now supports SSB's through four web
    browsers, Chrome, Chromium, Firefox, and Vivaldi. The
    [Ice application](https://peppermintos.com/guide/ice/) allow to create and manage
    SSBs.


# Debian derivatives
_See the also sections:
{{< iref "debian_admin" "Debian administration" >}} and
[Package management
](node/debian_admin#package_management "internal reference").

-   [Debian](http://www.debian.org/),
    [Debian FAQ](http://www.debian.org/doc/FAQ/).

-   <a name="grml"></a>[Grml](http://grml.org/)
    is a bootable live system for system administrators based on Debian.
    -   [Grml Wiki](http://wiki.grml.org/doku.php)
    -   The Grml rescue system supports [booting the Grml ISO from a hard disk
        ](http://wiki.grml.org/doku.php?id=rescueboot)
        by using the package grml-rescueboot which integrates ISO-booting into GRUB.
    -   [Boot Grml from Harddisk](http://wiki.grml.org/doku.php?id=rescueboot)
    -   [Grml-Forensic](https://grml-forensic.org/)  is a system designed for forensic
        investigations and data rescue tasks.
    -   [Use grml as a rescue system](http://wiki.grml.org/doku.php?id=rescue)
    -   [Use Grml for bios update](http://wiki.grml.org/doku.php?id=biosupdate)
    -   [use Grml to scan for virus](http://wiki.grml.org/doku.php?id=antivirus)
-   [gNewSense](http://www.gnewsense.org/) is a derivative of Debian
    (with Ubuntu ingredients) that focus on restricting to free
    software and qualify as [Free GNU/Linux distributions](http://www.gnu.org/distros/free-distros.html)
    as defined by the FSF in their
    [Guidelines for Free System Distributions
    ](http://www.gnu.org/philosophy/free-system-distribution-guidelines.html).
-   [SparkyLinux](http://sparkylinux.org/)
    is a Debian testing based Linux distribution, and Live CD
    with a set of slightly customized lightweight desktops like
    Enlightenment, OpenBox, LXDE.
-   <a name="tails">[Tails
    is a live OS, derived from Debian that you can
    start on almost any computer from a USB stick or a DVD.
    It aims at preserving your privacy and anonymity.
    It sends its traffic through
    [Tor](node/proxy#tor "internal reference")
    and contains applicrions for LUKS disk encryption, OpenPGP mail
    encryption, messaging with OTR, and securely delete your files
    with _Wipe_.

    Debian provides a package _tail-installer_ which is a
    graphical tool to install or upgrade Tails on a USB stick from an
    ISO image.

## Debian Live
[Debian Live](https://wiki.debian.org/DebianLive)
allows to create your own customized Debian Live system.
-   [Debian Live images](https://www.debian.org/CD/live/)
    for amd64 and i386.
-   [Debian Live Manual
    ](https://live-team.pages.debian.net/live-manual/html/live-manual)
    is primarily focused on helping you build a live system.
-   The index [installer images, live images, cloud images
    ](https://cdimage.debian.org/cdimage/) allow to know the packages installed on each
    standard Debian Live image.

# Gentoo
<!-- See the {{< iref "portage_notes" "Portage Notes" >}} the
    Gentoo packaging system.-->

-   [Gentoo](http://www.gentoo.org/),
    [Gentoo packages](http://packages.gentoo.org/)
-   [Gentoo FAQ](http://www.gentoo.org/doc/en/faq.xml),
-   [Gentoo Handbook](http://www.gentoo.org/doc/en/handbook/):
    [Gentoo Linux AMD64 Handbook]](https://wiki.gentoo.org/wiki/Handbook:AMD64),
-   [Gentoo Documentation Resources](http://www.gentoo.org/doc/en/ "gentoo.org /doc/en/")
-   The site [gentoo-portage](http://gentoo-portage.com/) allows to
    browse all the gentoo packages and list releases, dependencies,
    change logs, use flags.
-   [Gentoo Linux AMD64 Handbook](https://wiki.gentoo.org/wiki/Handbook:AMD64):
    the
    [chapter 3. Portage](https://wiki.gentoo.org/wiki/Handbook:AMD64#Working_with_Portage)
    describe the portage structure.
-   [Hardened Gentoo](https://wiki.gentoo.org/wiki/Project:Hardened) is a
    high security gentoo distribution.
-   Gentoo bugs tracking is done thru
    [Gentoo Bugzilla](http://bugs.gentoo.org/)
-   [Gentoo Power Management Guide](https://wiki.gentoo.org/wiki/Power_management/Guide)
    is aimed to increase battery run time on laptops.
-   [Gentoo Wiki](https://wiki.gentoo.org/wiki/Main_Page)
-   Catalyst is used to build all Gentoo releases


# Arch Linux
-   [Arch Linux](https://www.archlinux.org/) is a Linux distribution
    targeted at competent Linux users. It uses a  home-grown package
    manager_pacman_.<br />
-   Like Gentoo Arch Linux is a source based distribution.
    But Arch base system is designed to be installed as pre-built
    i686/x86_64 binary. This generally makes Arch quicker to build and
    update, but less customizable than Gentoo which also differs in
    supporting ARM, MIPS and many other architectures.<br />
    A comparaison review is given in Arch Wiki
    [Arch Compared to Other Distributions
    ](https://wiki.archlinux.org/index.php/Arch_Compared_to_Other_Distributions).
-   [Arch User Repository (AUR)
    ](https://wiki.archlinux.org/index.php/AUR_User_Guidelines)
    contains package descriptions (PKGBUILDs) that allow to compile a
    package from source with the utility makepkg and then install it
    via pacman.
-   The power of Arch Wiki is a very comprehensive
    [documentation](https://wiki.archlinux.org/index.php/Table_of_contents)
    in the [ArchWiki](https://wiki.archlinux.org/)
-   Arch Linux [supports LXDE](https://wiki.archlinux.org/index.php/LXDE)
-   [ArchBang](http://archbang.org/)
     is a minimal Arch Linux system using Openbox Window Manager. Its
     goal is to allow the user to skip the Arch post installation work
     to have a functional desktop.
-   [ArchLinux list of applications
    ](https://wiki.archlinux.org/index.php/List_of_applications).

# Fedora - Red Hat

-   [Red Hat Home](http://www.redhat.com/),
    [Red Hat Developer Connection](http://developer.redhat.com/)
-   [Fedora](https://getfedora.org/)
-   [Dag Wierrs Apt and Yum repository](http://dag.wieers.com/rpm/)

# minor dists

-   {{< wp "Solus" >}} is a desktop operating system based on the Linux kernel.
    -   [Solus Home](https://solus-project.com/)
-   [NixOs](https://nixos.org/)
    is a Linux distribution built on top of the
    [Nix package manager](https://nixos.org/nix/). NixOS currently
    runs on 32-bit and 64-bit x86 machines , and experimentally on
    ARM.
-   [OpenPKG](http://www.openpkg.org/) not a distribution, but an
    alternate packaging system.

# Site mirroring many distributions

-   [ftp.heanet.ie](http://ftp.heanet.ie/) :
    [distributions](http://ftp.heanet.ie/pub/).
-   [Linux à IBP](http://ftp.lip6.fr/pub/linux/),
    [distributions](http://ftp.lip6.fr/pub/linux/distributions/).
-   [Miroirs free.fr](http://ftp.free.fr/pub/)
    [Distributions linux](http://ftp.free.fr/pub/Distributions_Linux/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
