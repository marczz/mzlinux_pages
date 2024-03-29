---
title: Linux Distributions
---

See also the  {{< iref "lightweight_distributions" "Lightweight Linuxes" >}} section.

A full state of distributions is given in [DistroWatch](http://distrowatch.com).

# Ubuntu {#ubuntu}

-   Richard Stallman gave an advice on
    [Ubuntu Spyware: What to Do?](http://www.gnu.org/philosophy/ubuntu-spyware.html)
    quoting this article:

    > Ubuntu,[...] has installed surveillance code. When the user searches
    >  her own local files for a string using the Ubuntu desktop, Ubuntu
    > sends that string to one of Canonical's servers.
    > ......
    > If you ever recommend or redistribute GNU/Linux,
    >  please remove Ubuntu from the distros you recommend or redistribute.

-   [Ubuntu](https://www.ubuntu.com/),
    [wiki.ubuntu](https://wiki.ubuntu.com/),
    [Documentation for Ubuntu](https://help.ubuntu.com/),
    [Xubuntu](https://www.xubuntu.org/),
-   <a name="lubuntu"></a>[Lubuntu](https://lubuntu.me/) *LXQT+Ubuntu*
     is the {{< iref "desktop#lxqt" "LXQT" >}} flavor of Ubuntu, it is targeted at
     low-spec hardware.
     -   [Lubuntu Wiki](https://phab.lubuntu.me/w/)
     -   [Lubuntu Manual](https://manual.lubuntu.me/stable/)
     -   Wikipedia: {{< wp "Lubuntu" >}}
-   [Ubuntu Packages](https://packages.ubuntu.com)
-   [How to install Ubuntu on low memory systems
    ](https://help.ubuntu.com/community/Installation/LowMemorySystems).
-   [Ubuntu  Guide](https://ubuntuguide.org/) browse on all categories of software
    you may want to install on Ubuntu or any other distribution.
-   [Ubuntu Low End System Support
    ](https://help.ubuntu.com/community/LowEndSystemSupport)
-   [Documentation for latest distribution
    ](https://help.ubuntu.com/) contains
    _Ubuntu Desktop Help_,    _Ubuntu Server Guide_,   _Installing Ubuntu_.
-   [ubuntugeek](https://www.ubuntugeek.com/) site
    contains tips,howtos,tutorials and articles about Ubuntu Linux.
-   [Linux Mint](https://www.linuxmint.com/)
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
_See the also sections: {{< iref "debian_admin" "Debian administration" >}} and
{{< iref "debian_admin#package_management" "Package management" >}}

-   [Debian](https://www.debian.org/),
    [Debian FAQ](https://www.debian.org/doc/FAQ/).

-   <a name="grml"></a>[Grml](https://grml.org/)
    is a bootable live system for system administrators based on Debian.
    -   [Grml Wiki](https://wiki.grml.org/doku.php)
    -   The Grml rescue system supports [booting the Grml ISO from a hard disk
        ](https://wiki.grml.org/doku.php?id=rescueboot)
        by using the package grml-rescueboot which integrates ISO-booting into GRUB.
    -   [Boot Grml from Harddisk](https://wiki.grml.org/doku.php?id=rescueboot)
    -   [Grml-Forensic](https://grml-forensic.org/)  is a system designed for forensic
        investigations and data rescue tasks.
    -   [Use grml as a rescue system](https://wiki.grml.org/doku.php?id=rescue)
    -   [Use Grml for bios update](https://wiki.grml.org/doku.php?id=biosupdate)
    -   [use Grml to scan for virus](https://wiki.grml.org/doku.php?id=antivirus)
-   [gNewSense](https://www.gnewsense.org/) is a derivative of Debian
    (with Ubuntu ingredients) that focus on restricting to free
    software and qualify as [Free GNU/Linux distributions](https://www.gnu.org/distros/free-distros.html)
    as defined by the FSF in their
    [Guidelines for Free System Distributions
    ](https://www.gnu.org/philosophy/free-system-distribution-guidelines.html).
-   [SparkyLinux](https://sparkylinux.org/)
    is a Debian testing based Linux distribution, and Live CD
    with a set of slightly customized lightweight desktops like
    Enlightenment, OpenBox, LXDE.
-   <a name="tails">[Tails](https://tails.boum.org/)
    is a live OS, derived from Debian that you can start on almost any computer from a
    USB stick or a DVD.  It aims at preserving your privacy and anonymity.  It sends its
    traffic through {{< iref "proxy#tor" "Tor" >}} and contains applications for LUKS
    disk encryption, OpenPGP mail encryption, messaging with OTR, and securely delete
    your files with _Wipe_.

    Debian provides a package _tail-installer_ which is a graphical tool to install or
    upgrade Tails on a USB stick from an ISO image

    Tail needs an usb stick with 8GB memory.

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

# Alpine Linux
{{< wp "Alpine Linux" >}},
[Alpine Linux Home](https://www.alpinelinux.org/)
is a security-oriented, lightweight Linux distribution based on musl libc and
busybox. A container requires no more than 8 MB and a minimal installation to disk
requires around 130 MB of storage.

Alpine Linux is used heavily in containers (e.g. docker images) on servers, so many
of its main packages are focused on server services.

-   [Alpine Linux Wiki](https://wiki.alpinelinux.org/wiki/Main_Page)


# Gentoo
<!-- See the {{< iref "portage_notes" "Portage Notes" >}} the
    Gentoo packaging system.-->

-   [Gentoo](https://www.gentoo.org/),
    [Gentoo packages](https://packages.gentoo.org/)
-   [Gentoo FAQ](https://www.gentoo.org/doc/en/faq.xml),
-   [Gentoo Handbook](https://www.gentoo.org/doc/en/handbook/):
    [Gentoo Linux AMD64 Handbook](https://wiki.gentoo.org/wiki/Handbook:AMD64),
-   [Gentoo Documentation Resources](https://www.gentoo.org/doc/en/)
-   The site [gentoo-portage](https://gentoo-portage.com/) allows to
    browse all the gentoo packages and list releases, dependencies,
    change logs, use flags.
-   [Gentoo Linux AMD64 Handbook](https://wiki.gentoo.org/wiki/Handbook:AMD64):
    the
    [chapter 3. Portage](https://wiki.gentoo.org/wiki/Handbook:AMD64#Working_with_Portage)
    describe the portage structure.
-   [Hardened Gentoo](https://wiki.gentoo.org/wiki/Project:Hardened) is a
    high security gentoo distribution.
-   Gentoo bugs tracking is done thru
    [Gentoo Bugzilla](https://bugs.gentoo.org/)
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
-   [ArchBang](https://archbang.org/)
     is a minimal Arch Linux system using Openbox Window Manager. Its
     goal is to allow the user to skip the Arch post installation work
     to have a functional desktop.
-   [ArchLinux list of applications
    ](https://wiki.archlinux.org/index.php/List_of_applications).

# Fedora - Red Hat

-   [Red Hat Home](https://www.redhat.com/),
    [Red Hat Developer Connection](https://developer.redhat.com/)
-   [Fedora](https://getfedora.org/)
-   [Dag Wierrs Apt and Yum repository](https://dag.wieers.com/rpm/)

# NiX
{{< wp "Nix package manager" >}} utilizes a purely functional deployment model where
software is installed into unique directories generated through cryptographic hashes, it
is also the name of the programming language.

{{< wp "NixOx" >}} is a Linux distribution built on top of the Nix package manager.

-   [NixOS - NixOS Linux](https://nixos.org/)
-   [NixOS - Learn Guides ](https://nixos.org/learn.html#learn-guides):
    -   [Install Nix](https://nixos.org/guides/install-nix.html)
    -   [Ad hoc developer environments
        ](https://nixos.org/guides/ad-hoc-developer-environments.html)
    -   [Declarative and reproducible developer environments
        ](https://nixos.org/guides/declarative-and-reproducible-developer-environments.html)
    -   [Setup a development environment
        ](https://nixos.org/guides/dev-environment.html)
    -   [Towards reproducibility: Pinning nixpkgs
        ](https://nixos.org/guides/towards-reproducibility-pinning-nixpkgs.html)
    -   [Continuous Integration with GitHub Actions
        ](https://nixos.org/guides/continuous-integration-github-actions.html)
    -   [Building and running Docker images
        ](https://nixos.org/guides/building-and-running-docker-images.html)
-   [nix.dev documentation](https://nix.dev/) provides the previous tutorials and
    -   [getting-started-nix-template](https://github.com/nix-dot-dev/getting-started-nix-template)
        Based on nix.dev tutorials, repository template to get you started with Nix.
    -   [Anti-patterns](https://nix.dev/anti-patterns/index.html),
        [Nix language](https://nix.dev/anti-patterns/language.html)
    -   [Pinning Nixpkgs](https://nix.dev/reference/pinning-nixpkgs.html)
    -   [Frequently Asked Questions](https://nix.dev/faq.html)
        ( [Nix](https://nix.dev/faq.html#nix),
        [NixOS](https://nix.dev/faq.html#nixos) )

-   [Nix manual](https://nixos.org/manual/nix/stable/)
-   [Nixpkgs Manual](https://nixos.org/manual/nixpkgs/stable)
-   [NixOS Manual](https://nixos.org/manual/nixos/stable)
-   [Nix Pills](https://nixos.org/guides/nix-pills/pr01.html)
    is a a series of blog posts written by Luca Bruno (aka Lethalman).
    It provides a tutorial introduction into Nix  and Nixpkgs package collection,
    in the form of short chapters called _pills_.
-   [nix-shorts](https://github.com/justinwoo/nix-shorts)
    A collection of short notes about Nix.
    -   [posts folder](https://github.com/justinwoo/nix-shorts/tree/master/posts)


-   [Nix - GitHub](https://github.com/NixOS/nix)
-   [NixOS Discourse - NixOS community forum](https://discourse.nixos.org/)
-   [Flakes](https://nixos.wiki/wiki/Flakes)
    Flakes allow you to specify your code's dependencies (e.g. remote Git repositories)
    in a declarative way, Flakes are meant as a replacement for channels.

-   [Cachix](https://cachix.org/)  Nix binary cache hosting, with Continuous Integration
    support.
    Hosted instance with 10 GB free storage for open source projects.
-   [Cachix docs](https://docs.cachix.org/index.html)
-   [cachix - GitHub.](https://github.com/cachix/cachix) (Apache-2.0)
    is written in haskell.

# minor dists

-   {{< wp "Solus" >}} is a desktop operating system based on the Linux kernel.
    -   [Solus Home](https://solus-project.com/)
-   [OpenPKG](https://www.openpkg.org/) not a distribution, but an
    alternate packaging system.

# Site mirroring many distributions

-   [ftp.heanet.ie](https://ftp.heanet.ie/) :
    [distributions](https://ftp.heanet.ie/pub/).
-   [Linux à IBP](https://ftp.lip6.fr/pub/linux/),
    [distributions](https://ftp.lip6.fr/pub/linux/distributions/).
-   [Miroirs free.fr](https://ftp.free.fr/pub/)
    [Distributions linux](http://ftp.free.fr/pub/Distributions_Linux/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
