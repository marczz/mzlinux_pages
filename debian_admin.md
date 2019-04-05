---
title: Debian Administration
---

{{% toc /%}}

## Debian Official documentation

-   [Debian Reference](http://www.debian.org/doc/manuals/reference/)
    the true up-to-date reference for all debian tasks, begin here for any
    administration task.  Of course some services are not _(yet?)_ covered in this
    guide.
-   [Securing Debian Manual
    ](http://www.debian.org/doc/manuals/securing-debian-howto/)
    an other maintained manual focused on security aspects.
-   [Debian New Maintainers' Guide
    ](http://www.debian.org/doc/manuals/maint-guide/)
    explains how to build debian packages. It is completed by
    [Debian New Maintainers' Guide
    ](https://www.debian.org/doc/devel-manuals#debmake-doc)
    which describes the building of the Debian package using the debmake command. The
    [Debian Developer's Reference
    ](http://www.debian.org/doc/manuals/developers-reference/index.en.html)
    is only usefull if you are ore want to become an official
    package maintainer.
-   [Debian Linux Kernel Handbook
    ](http://kernel-handbook.alioth.debian.org/)
-   [Debian GNU/Linux Installation Guides
    ](http://www.debian.org/releases/stable/install):
    [Installation Guide for the am64 architecture.
    ](https://www.debian.org/releases/stable/amd64/) and
    [for the armhf achitecture
    ](https://www.debian.org/releases/stable/armhf/)
-   [Release Notes for Debian](http://www.debian.org/releases/) :
    [Release Notes for Debian stable amd64
    ](http://www.debian.org/releases/stable/amd64/release-notes/),
    [Ch 4: upgrading to stable from previous release
    ](http://www.debian.org/releases/stable/amd64/release-notes/ch-upgrading.en.html)
    [Release Notes for Debian stable armhf
    ](http://www.debian.org/releases/stable/armhf/release-notes/),
    [Ch 4: upgrading to stable from previous release
    ](http://www.debian.org/releases/stable/armhf/release-notes/ch-upgrading.en.html)
-   [Debian Policy Manual](http://www.debian.org/doc/debian-policy/)
    policy requirements for the Debian packages distribution.
-   [Debian FAQ](http://www.debian.org/doc/FAQ)
-   [Debian Bugs](http://www.debian.org/Bugs/)
    also availables in google groups
    [debian.bugs.dist
    ](http://groups.google.com/group/linux.debian.bugs.dist)
    and
    [debian.bugs.rc
    ](http://groups.google.com/group/linux.debian.bugs.rc)
-   [Debian Menu System
    ](http://www.debian.org/doc/packaging-manuals/menu.html/)
-   [Debian GNU/Linux Installation Guide](http://www.debian.org/releases/stable/amd64/)

## Unofficial documentation

-   [Debian Wiki](http://wiki.debian.org/)
-   [DebianHelp](http://www.debianhelp.co.uk/)
    is a site of articles and tips for Debian system administration.
-   [Debian Administration](http://www.debian-administration.org/)
-   Raphaël Hertzog and Roland Mas: [The Debian Administrator's Handbook
    ](https://debian-handbook.info/browse/stable/) for stable (Debian 8 -
    Jessie). It is also available as Ebook.
-   The [Aptosid](http://aptosid.com/index.php?module=wikula)
    distribution is a Debian Sid derivative, it has an
    [aptosid OS Manual](http://manual.aptosid.com/en/welcome-en.htm).
-   [Debian Wiki](http://wiki.debian.org/) Pages:
    -   [Manual-Howto](http://wiki.debian.org/Manual-Howto)
        or _How to install and configure various software on Debian_.
    -   [Debian Development](http://wiki.debian.org/DebianDevelopment).
-   [dwww at tuwien.ac.at](http://hep.itp.tuwien.ac.at/cgi-bin/dwww)
    has a web access to all [packages doc index
    ](http://hep.itp.tuwien.ac.at/cgi-bin/dwww/usr/share/doc/)
-   [GNU/Linux Desktop Survival Guide
    ](http://www.togaware.com/linux/survivor/) by Graham Williams


# Package management  {#package_management}

Debian packages are managed by  low level tools
 [dpkg](http://manpages.debian.net/cgi-bin/man.cgi?query=dpkg),
 [apt-get](http://manpages.debian.net/cgi-bin/man.cgi?query=apt-get),
 [apt-cache](http://manpages.debian.net/cgi-bin/man.cgi?query=apt-cache),
and higher level:
 [aptitude](http://manpages.debian.net/cgi-bin/man.cgi?query=aptitude),
 [aptitude reference manual](http://algebraicthunk.net/~dburrows/projects/aptitude/doc/en/),
 [synaptic](http://manpages.debian.net/cgi-bin/man.cgi?query=synaptic).

-   [Index of Debian packages: packages.debian.org](http://packages.debian.org/)
-   [Debian  Reference](http://www.debian.org/doc/manuals/debian-reference/):
    [Chapter 2 - Debian package management](http://www.debian.org/doc/manuals/debian-reference/ch02.en.html)
-   [apt-get.org index of repositories of unofficial packages](http://www.apt-get.org/)
-   [Basic package management operations (with aptitude)
    ](http://www.debian.org/doc/manuals/reference/ch02.en.html#_basic_package_management_operations)
    and [Examples of aptitude operations
    ](http://www.debian.org/doc/manuals/reference/ch02.en.html#_examples_of_aptitude_operations)
    including installing from unstable or testing.
-   [Advanced package management operations
    ](http://www.debian.org/doc/manuals/reference/ch02.en.html#_advanced_package_management_operations)
    with _dpkg_, _apt-get_,  _apt-cache_.
-   [APT HOWTO](http://www.debian.org/doc/manuals/apt-howto/)
-   [Debian wiki: Secure Apt](http://wiki.debian.org/SecureApt)
    from Joey Hess explains the principles and  use of signed packages
-   [How to manage packages on an off-line Debian system
    ](http://blog.sleeplessbeastie.eu/2014/01/30/how-to-manage-packages-on-an-off-line-debian-system/)
-   [apt-offline Home and Repository
    ](https://alioth.debian.org/projects/apt-offline/)

# Package Repositories {#package_repository}

-   [Debian Wiki](https://wiki.debian.org/):
    [Debian Repository](https://wiki.debian.org/),
    [Debian Repository Unofficial
    ](https://wiki.debian.org/DebianRepository/Unofficial)
    [Debian Repository Format
    ](https://wiki.debian.org/DebianRepository/Format),
    [Debian Repository Setup
    ](https://wiki.debian.org/DebianRepository/Format),
    [Debian Repository Setup With Minidinstal
    ](https://wiki.debian.org/DebianRepository/SetupWithMinidinstall)
    [Debian Repository Setup With Reprepro
    ](https://wiki.debian.org/DebianRepository/SetupWithReprepro),
    [Instructions to connect to a third-party repository
    ](https://wiki.debian.org/DebianRepository/UseThirdParty),
-   [Debian Multimedia](http://www.deb-multimedia.org/)

## Backports {#backports}

-   [Debian Backports](http://backports.debian.org/)
    are recompiled packages from testing (mostly) and unstable (in a
    few cases only), so they will run without new libraries (wherever
    it is possible) on a stable Debian distribution.  You just have to
    follow
    [Backports instructions
    ](http://backports.debian.org/Instructions/). You can
    [search backports for packages](http://backports.debian.org/Packages/)
-   Backports use is also described in [Debian wiki Backports
    ](http://wiki.debian.org/Backports)

# Mixing stable and unstable {#apt_pinning}
__Apt Pinning__ is described in:

-   [Apt howto:How to keep a mixed system
    ](http://www.debian.org/doc/manuals/apt-howto/ch-apt-get.en.html#s-default-version),
    the package selection by pin numbers is in
    [Apt howto: How to keep specific versions of packages installed
    ](http://www.debian.org/doc/manuals/apt-howto/ch-apt-get.en.html#s-pin)
-   [Debian Wiki: Apt Preferences
    ](https://wiki.debian.org/AptPreferences)
-   [Debian Reference: Debian package management
    ](http://www.debian.org/doc/manuals/reference/ch02.en.html):
    [tweaking candidate version
    ](http://www.debian.org/doc/manuals/reference/ch02.en.html#_tweaking_candidate_version)
-   [wiki.debian.org AptPinning
    ](http://wiki.debian.org/AptPinning)
    Last reference shows a way that you can have apt mix-and-match
    between Stable Testing, and Unstable sources.
-   [Apt-Pinning for Beginners
    ](http://jaqque.sbih.org/kplug/apt-pinning.html)
-   {{< man "apt_preferences" >}}



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
