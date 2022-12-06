---
title: Virtualization
---

# Emulators and virtualization References

-   This section deals with virtualization platforms or
    {{< wp "Hypervisors" >}}
    that allow multiple operating systems to run on a host computer at
    the same time.
-   Wikipedia {{< wp "Comparison of platform virtualization software" >}},
    {{< wp "List of computer system emulators" >}}  lists software and
    hardware that emulates computing platforms,
    {{< wp "x86 virtualization" >}}.
-   [Ubuntu Server](https://ubuntu.com/server/):
    [Virtualization](https://ubuntu.com/server/docs/virtualization-introduction)
-   [System Virtualization - Debian Wiki](https://wiki.debian.org/SystemVirtualization)
    compare the virtualization software availables on a Debian Server.

# Chroot {#chroot}
_not a true virtualization_


-   {{< wp "chroot"  "Wikipedia: chroot" >}}
-   [Debian wiki: chroot](https://wiki.debian.org/chroot)
-   [chroot chapter of debian reference manual
    ](http://www.debian.org/doc/manuals/reference/ch09.en.html#_chroot_system)
-   [Debian/installers FAQ list of chroot refs
    ](http://linuxmafia.com/faq/Debian/installers.html#chroot)
-   [Ubuntu documentation: Basic Chroot](https://help.ubuntu.com/community/BasicChroot)
-   [ArchWiki: Chroot](https://wiki.archlinux.org/index.php/Chroot)
-   [Debian Wiki: schroot](https://wiki.debian.org/Schroot) and
    [other schroot page](https://wiki.debian.org/RichardDarst/Schroot).
-   [Debian Wiki: Debootstrap](https://wiki.debian.org/Debootstrap).
-   [Debian GNU/Linux Installation Guide
    ](https://www.debian.org/releases/stable/amd64/index.en.html) :
    [Appendix D.3. Installing Debian GNU/Linux from a Unix/Linux System
    ](https://www.debian.org/releases/stable/amd64/index.en.html)
    uses {{< man "debootstrap" >}} and a chroot.
-   [Ubuntu documentation: Debootstrap Chroot
    ](https://help.ubuntu.com/community/DebootstrapChroot)
-   [debootstick](http://drakkar-lig.github.io/debootstick/)
    Turn a chroot environment into a bootable image.
    It is in Debian.
    -   [GitHub: debootstick
        ](https://github.com/drakkar-lig/debootstick/).
    -   [debootstick Wiki
        ](https://github.com/drakkar-lig/debootstick/wiki)
-   [PRoot](https://proot-me.github.io/)
    is a user-space implementation of _chroot_, _mount --bind_, and
    _binfmt_misc_. It is in Debian
    -   [PRoot - ArchWiki](https://wiki.archlinux.org/index.php/PRoot)
-   Debian provides the packages [chrootuid
    ](http://ftp.porcupine.org/pub/security/chrootuid1.3.README)
    and _compartment_, that are used to chroot automatically servers and services.


# Dos emulators

-   [Bochs](http://bochs.sourceforge.net/)&nbsp; IA-32 (x86) PC
    emulator;
-   The
    [The FreeDOS Project](http://www.freedos.org/ "freedos.org Home")
    is an open source DOS compatible operating system most of freedos
    programs are licensed under GPL.
-   [DOSBox](http://dosbox.sourceforge.net/)a x86 emulator with DOS
-   [dosemu](http://www.dosemu.org) a _DOS box_ under linux.
    -   [The dosemu HOWTO](http://dosemu.sourceforge.net/docs/HOWTO/)
-   [bootdisk.com](http://www.bootdisk.com/)
    -   Notes:
        :   Toggle between windowed and fullscreen mode using Ctrl-Alt-F

# KVM _Kernel-based Virtual Machine_ {#KVM}
-   [KVM](http://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine) (some part GPL,
    some part LGPL) is a virtualization solution for Linux on x86 hardware containing
    virtualization extensions (Intel VT or AMD-V). It consists of a loadable kernel
    module, _kvm.ko_, and a processor specific module, _kvm-intel.ko_ or _kvm-amd.ko_
    providing {{< wp "Hardware-assisted virtualization (HVM)" >}} used to run
    {{< iref "#qemu" "QEMU" >}} _Unlike native Qemu that uses emulation_. The kernel
    component of KVM is included in mainline Linux.

    Using KVM, one can run multiple virtual machines running unmodified
    Linux or Windows images. Each virtual machine has private
    virtualized hardware: a network card, disk, graphics adapter, etc.

    KVM is the default virtualization technology in Ubuntu.

    The difference with {{< iref "#xen" "Xen" >}} is [explained in the KVM FAQ
    ](http://www.linux-kvm.org/page/FAQ#General_KVM_information). Xen is an external
    hypervisor that divides resources among guests, and can run on non-hvm x86
    processors using {{< wp "paravirtualization" >}}; On the other hand, KVM uses the
    regular Linux scheduler and memory management; it is much smaller
    and simpler and featureful. But _KVM_  does not support paravirtualization which
    limit it's use to hvm x86 processors.

    KVM can be managed via {{< iref "#libvirt" "libvirt" >}} using _virsh_ as described
    in [KVM/Virsh - Ubuntu Community Wiki](https://help.ubuntu.com/community/KVM/Virsh).

-   [KVM Home Page](https://www.linux-kvm.org/page/Main_Page)
-   [HOWTO - KVM](http://www.linux-kvm.org/page/HOWTO).
-   [Using KVM virtualization – IBM Developer
    ](https://developer.ibm.com/technologies/linux/articles/l-using-kvm)
-   [Ubuntu Help: The Kernel Virtual Machine](https://help.ubuntu.com/community/KVM)
    is an index of several pages dealing with _installation_, _networking_, _guest
    creation_, _guest management_, _guest console access_, _FAQ_.
-   [KVM - Debian Wiki](https://wiki.debian.org/KVM),
    [DebianKVMGuests - Debian Wiki](https://wiki.debian.org/DebianKVMGuests),
-   [Winapps](https://github.com/Fmstrat/winapps)
    run Windows apps such as Microsoft Office/Adobe in Linux  and
    GNOME/KDE as if they were a part of the native OS, including Nautilus integration
    for right clicking on files of specific mime types to open them.

    It works by running Windows under KVM and communicating through a RDP server.
-   [Creating a ]a Virtual Machine in KVM
    ](https://github.com/Fmstrat/winapps/blob/main/docs/KVM.md)
    is a tutorial aimed to Winapps, but can be used to set any KVM windows virtual
    machine.

# Linux-VServer / OpenVZ {#openvz}
-   Os level virtualization is provided by
   [Linux-VServer](http://en.wikipedia.org/wiki/Linux-VServer)
   (GPL v.2) or it's fork'
   [OpenVZ](http://en.wikipedia.org/wiki/OpenVZ) (GPL v.2).
   The proprietary fork of OpenVZ is named {{< wp "Virtuozzo" >}}.
-   The [Home of the vserver project linux-vserver.org](http://linux-vserver.org/)
   host the documentation and the
   [Vserver Faq](http://linux-vserver.org/Frequently_Asked_Questions).
-  [Wikipedia: OpenVz](http://en.wikipedia.org/wiki/OpenVZ),
   [Official OpenVz site](http://openvz.org/),
   [OpenVz wiki](http://wiki.openvz.org/)
-  [Markus Gattol: OpenVz](http://www.markus-gattol.name/ws/openvz.html)

# LibVirt {#libvirt}
[Libvirt](http://libvirt.org) is used to interface
with different virtualization technologies {{< iref "#KVM" "KVM" >}},
{{< iref "#xen" "Xen" >}}, {{< iref "#qemu" "Qemu" >}}, {{< iref "#openvz" "OpenVz" >}}
or Virtuozzo, {{< iref "#vmware" "VMWare ESX" >}}
{{< iref "#LXC"  "LXC" >}}, {{< iref "#virtualbox"  "VirtualBox" >}}, _BHyve_

-   [ArchWiki - LibVirt](https://wiki.archlinux.org/index.php/Libvirt).
-   [Ubuntu Server](https://ubuntu.com/server/):
    [Virtualization](https://ubuntu.com/server/docs/virtualization-introduction),
    [LibVirt](https://ubuntu.com/server/docs/virtualization-libvirt).
-   [libvirt - Debian Wiki](https://wiki.debian.org/libvirt)
-   [LibVirt LXC container driver](http://libvirt.org/drvlxc.html)
-   [An introduction to libvirt's LXC support
    ](http://openvz.org/pipermail/devel/2008-September/014314.html) by Daniel P. Berrange.
-   <a name="virsh"></a>[virsh](https://www.libvirt.org/manpages/virsh.html) (GPL) is the
    main command line tool for managing libvirt guest domains. It can be used to to list current
    domains. create, pause, and shutdown domains.
    -   [Virsh Command Reference](https://libvirt.org/virshcmdref.html).
-   <a name="virt-manager"></a>[virt-manager](https://virt-manager.org/)
    (GPL) is a front end to libvirt written in Python, while the UI is
    constructed with Glade and GTK+.

# LXC {#LXC}

{{< wp "LXC" "Linux container tools (LXC)" >}} is a virtualization method for running
multiple isolated server on a single control host. It provides a virtual environment
that has its own process and network space.  Lxc is similar to a chroot, but with much
more isolation.  Early versions of Docker used LXC as the container execution driver,
but LXC support was dropped in Docker v1.10.

-   [ArchWiki - Linux Containers
    ](https://wiki.archlinux.org/index.php/Linux_Containers).
-   [ArchWiki - Cgoups](https://wiki.archlinux.org/index.php/Cgroups).
-   [Ubuntu serverguide - cgroups
    ](https://help.ubuntu.com/lts/serverguide/cgroups.html).
-   [LXC - Ubuntu server](https://ubuntu.com/server/docs/containers-lxc)
_   [LXC - Debian Wiki](https://wiki.debian.org/LXC).
-   [LXC HOWTO](http://lxc.teegra.net) by Dwight Schauer.
-   Kernel [cgroups doc directory
    ](http://www.mjmwired.net/kernel/Documentation/cgroups/)
    with documentation on [kdoc:cgroups/cgroups.txt|cgroups]  and
    [kdoc:cgroups/devices.txt|devices].
-   [bodhizazen blog](http://blog.bodhizazen.net/) contains LXC tutorials.
-   [Markus Gattol: Linux Containers
    ]( http://www.markus-gattol.name/ws/linux_containers.html)
-   [LXD - ArchWiki](https://wiki.archlinux.org/index.php/LXD)
     is a container and virtual-machine "hypervisor" for Linux Containers.
-   [Containers - lxd - Ubuntu Server](https://ubuntu.com/server/docs/containers-lxd)
-   [Linux Containers - LXD Home](https://linuxcontainers.org/lxd/)
-   [LXD documentation](https://lxd.readthedocs.io/en/latest/)

# Qemu {#qemu}
[Qemu](http://wiki.qemu.org/) (GPL)is a generic  emulator and virtualizer.

As an emulator, QEMU can run guest OSes on an architecture different from the host.

When guest and host architecture is identical QEMU can be used as virtualizer and
achieve near native performances by executing the guest code directly on the host
CPU. When using {{< iref "#KVM" "KVM" >}}, QEMU can virtualize x86, server and embedded
PowerPC, and S390 guests.


-   [Qemu Documentation](http://wiki.qemu.org/Manual):
    [QEMU User manual](https://qemu.weilnetz.de/doc/qemu-doc.html),
    [Qemu networking](http://wiki.qemu.org/Documentation/Networking).
-   Wikipedia: {{< wp "Qemu" >}}.
-   [Qemu Wikibook](http://en.wikibooks.org/wiki/QEMU) has sections:
    [Installing QEMU](http://en.wikibooks.org/wiki/QEMU/Installing_QEMU),
    [Creating and Manipulating Images](http://en.wikibooks.org/wiki/QEMU/Images),
    [Networking](http://en.wikibooks.org/wiki/QEMU/Networking),
    [Using the Monitor](http://en.wikibooks.org/wiki/QEMU/Monitor),
    [Windows XP Guest](http://en.wikibooks.org/wiki/QEMU/Windows_XP)
    [FreeDOS Guest](http://en.wikibooks.org/wiki/QEMU/FreeDOS)
-   [Qemu - Unbutu Server](https://ubuntu.com/server/docs/virtualization-qemu)
-   [Gentoo Wiki: Qemu](https://wiki.gentoo.org/wiki/QEMU).
-   [QEMU - ArchWiki](https://wiki.archlinux.org/index.php/QEMU)
    is a tutorial with a chapter
    on _using any real partition as the single primary partition of a hard disk image_
-   [QEMU - Debian Wiki](https://wiki.debian.org/QEMU),
    [VGA Passthrough - Debian Wiki](https://wiki.debian.org/VGAPassthrough).
-   [Virtual Networking](http://people.gnome.org/~markmc/virtual-networking.html)
    by Mark McLoughlin.


# VirtualBox {#virtualbox}
-   [VirtualBox](http://www.virtualbox.org/) is another virtualization
    system, that runs on Windows, Linux and Macintosh hosts and
    supports as guests Windows,
    DOS/Windows 3.x, Linux, and OpenBSD. Packaged
    binaries are available for the main distributions.**VirtualBox**
    was initially developped by *Innotek* which was acquired by Sun
    Microsystems in February 2008 (release 1.6 and 2.0 of VirtualBox).
    VirtualBox is distributed either as a GPLed edition and a free, but
    closed source, personal use and evaluation license. The PUEL
    edition adds USB and virtual Remote Desktop support

-   [Official Virtual Box documentation
    ](https://www.virtualbox.org/wiki/Documentation):
    - [VirtualBox Manual](http://www.virtualbox.org/manual/)
      This is the same manual that we have in the vbox manager when we
      select manual under the help dropdown.
  -   [VirtualBox pdf user manual
      ](http://download.virtualbox.org/virtualbox/UserManual.pdf),
      [french](http://download.virtualbox.org/virtualbox/UserManual_fr_FR.pdf).
-   [VirtualBox user how-tos](http://www.virtualbox.org/wiki/User_HOWTOS):
        - [How to migrate existing Windows
        ](http://virtualbox.org/wiki/Migrate_Windows)
-   [ArchWiki: VirtualBox
    ](https://wiki.archlinux.org/index.php/VirtualBox).
    -   [VirtualBox Tips_and_tricks
        ](https://wiki.archlinux.org/index.php/VirtualBox/Tips_and_tricks).
-   There are several tutorials to virtual box on Ubuntu:
    -   [Ubuntu community VirtualBox documentation
        ](https://help.ubuntu.com/community/VirtualBox),
    -   [VirtualBox Installation
        ](https://help.ubuntu.com/community/VirtualBox/Installation),
    -   [VirtualBox GuestAdditions
        ](https://help.ubuntu.com/community/VirtualBox/GuestAdditions),
    -   [VirtualBox SharedFolders
        ](https://help.ubuntu.com/community/VirtualBox/SharedFolders).


# Wine
-   {{< wp "Wine (software)" >}} implementation of the Win32 API,
-   [Wine hq](http://www.winehq.com/)
-   [Wine Documentation](http://www.winehq.org/site/documentation) and
    [HowTo](http://wiki.winehq.org/HowTo)
-   [Running Windows applications on Linux using Wine](http://www.frankscorner.org/)
    ( Frank's corner)
-   [CodeWeavers](http://www.codeweavers.com/) sell a customized wine.

# Xen {#xen}
-   {{< wp "Xen" >}} is a GPL paravirtualization layer. Intermediate between
    hardware virtualization and os level virtualization,
    paravirtualization involves making the virtual server OS aware of
    the fact that it is being virtualized.

    Citrix has forked a proprietary source _citrix server_ from Xen.

-   {{< wp "Xen" "Wikipedia: Xen" >}} is a detailled page with an extensive description
    of Xen History.
-   [Xen home page](https://xenproject.org/).
-   [Xen Wiki](https://wiki.xen.org/wiki/Main_Page),
    [Category:HowTo - Xen](https://wiki.xenproject.org/wiki/Category:HowTo).
-   [Xen - Debian Wiki](https://wiki.debian.org/Xen),
    [Category:Debian - Xen Wiki](https://wiki.xen.org/wiki/Category:Debian)
-   [Xen - Gentoo Wiki](https://wiki.gentoo.org/wiki/Xen).
-   [Xen - Ubuntu Community](https://help.ubuntu.com/community/Xen)
-   {{< iref "#virt-manager" "virt-manager" >}} can be used to manage Xen hypervisor,
    as explained in
    [this page](https://wiki.xen.org/wiki/DomU_Install_with_Virt-Manager)
    of the Xen wiki, or
    [this other page](https://wiki.xenproject.org/wiki/DomU_Install_with_Virt-Install).

# Other Virtualization systems
-   [Virtual Square](http://wiki.virtualsquare.org/)
    create an unified environment that allows virtual machines,
    systems and networks to communicate and interact.
    -   The virtual networking is handled by _VDE_. A _vde2_ package is in Debian.
    -   _View-OS_ is an approach to the process/kernel interface.
        UMView is a user-mode implementation of View-OS. It is packaged in Debian.
-   <a name="vmware"></a>The harware emulation virtual machine
    [VMware](http://en.wikipedia.org/wiki/VMware) (Proprietary)
    provides a completely virtualized set of hardware to the guest
    operating system.
-   {{< wp "oVirt" >}} (Apache Licence) is a  virtualization management platform. It
    consists of two components, oVirt engine written in Java and oVirt node the frontend
    which uses Google Web Toolkit -GWT_. oVirt is built upon
    {{< iref "#libvirt" "libvirt" >}}, Gluster, PatternFly, and Ansible.
    -   [oVirt Home](http://www.ovirt.org/)
    -   [oVirt - GitHub](https://github.com/oVirt).

# deprecated projects

-   {{< wp "User-mode Linux" >}} (GPL) gives a virtual linux machine under a linux
    system.
   {{< wp "Cooperative Linux" >}}, abbreviated as coLinux allows Microsoft
    Windows and the Linux kernel to run simultaneously in parallel on the same machine.
    -   [Cooperative Linux Home](http://colinux.org/) (GPL).

# Windows images
We find on
[Windows Software Download](https://www.microsoft.com/en-us/software-download/)
([french page](https://www.microsoft.com/fr-fr/software-download/))
image for all windows version 8.1, 10 and 11, as ISO disc images,  windows 7 is no more
supported and there are [migration guidance
](https://support.microsoft.com/en-us/windows/windows-7-support-ended-on-january-14-2020-b75d4580-2cc7-895a-2c9c-1466d9a53962).

# Docker {#docker}

-   [Docker Documentation](https://docs.docker.com/)
    -   [Get started](https://docs.docker.com/get-started/)
    -   [Reference documentation](https://docs.docker.com/reference/)
-   [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
    list of Docker resources.
-   [Archwiki - Docker
    ](https://wiki.archlinux.org/index.php/Docker).
-   [Docker - Debian Wiki](https://wiki.debian.org/Docker).
-   [Create Docker Image - Debian Wiki](https://wiki.debian.org/Cloud/CreateDockerImage)
    look also to the two following items, to secure your image.
-   John Goerzen has a [GitHub repository of Debian images
    ](https://github.com/jgoerzen/docker-debian-base),

    He explains his [guideline in his blog
    ](https://changelog.complete.org/archives/9794-fixing-the-problems-with-docker-images)
    these images have  only 11MB RAM overhead and provide:
    -   A real init system, capable of running standard startup scripts,
    -   Working syslog, which can either export all logs to Docker’s logging
        infrastructure, or keep them within the container,
    -   Working real schedulers (cron, anacron, and at) and logrotate.

    and optional features:
    -   A real SMTP agent (exim4-daemon-light).
    -   SSH client and server (optionally exposed to the Internet).
    -   Automatic security patching via unattended-upgrades and needsrestart.

-   _Phusion_ has a  [GitHub repository of Ubuntu Images
    ](https://github.com/phusion/baseimage-docker). They are described in the Readme of
    the repository, and [Your Docker image might be broken
    ](http://phusion.github.io/baseimage-docker/) which teach right way to build your
    Dockerfile.

## Docker Tutorials
-   [Docker for beginners.md
    ](https://github.com/groda/big_data/blob/master/docker_for_beginners.md)
-   [The Docker Handbook](https://docker-handbook.farhan.dev/)

# Sandboxing
A a {{< wp "Sandbox_(computer_security)" "sandbox" >}} is a security mechanism for
separating running programs, usually in an effort to mitigate system failures or
software vulnerabilities from spreading.

## Security jails

-   [Security, sandboxing - ArchWiki
    ](https://wiki.archlinux.org/index.php/Security#Sandboxing_applications).
-   {{< wp "Sandbox_(computer_security)" "Wikipedia: Sandbox" >}}

-   [containerd](https://containerd.io/) (Apache License)
    container runtime with an emphasis on simplicity, robustness and portability.  It is
    available as a daemon for Linux and Windows, which can manage the complete container
    life cycle of its host system: image transfer and storage, container execution and
    supervision, low-level storage and network attachments, etc.

    Containerd is designed to be embedded into a larger system, rather than being used
    directly by developers or end-users.

    _Containerd_ is packaged in Debian.

    -   [Getting started with containerd](https://containerd.io/docs/getting-started/)
    -   [GitHub - containerd](https://github.com/containerd/containerd)
-   [Firejail](https://firejail.wordpress.com/) (GPL)
    is a SUID program that reduces the risk of security breaches by restricting
    the running environment of untrusted applications using Linux namespaces and
    {{< wp  "Secomp"  >}} filter [seccomp-bpf
    ](https://www.kernel.org/doc/html/latest/userspace-api/seccomp_filter.html).
    It is used for browsers and internet facing applications, as well as
    any servers.

    _Firejail_ is packaged in Debian, with an extra package _firejail-profiles_.
    -   [Firejail - ArchWiki](https://wiki.archlinux.org/index.php/Firejail).
    -   [Firejail - GitHub](https://github.com/netblue30/firejail).
-   [Bubblewrap](https://github.com/containers/bubblewrap) (LGPL)
    is a lightweight sandbox application developed from Flatpak.
    The readme contains a comparison with _runc_, _Firejail_ and _SandStorm_.

    _Bubblewrap_  is packaged in Debian.
    -   [Bubblewrap - ArchWiki](https://wiki.archlinux.org/index.php/Bubblewrap).
-   [runc](https://github.com/opencontainers/runc) (Apache-2.0 License)
    CLI tool for spawning and running containers according to the OCI specification
    _Open Container Project specification_.
    _runc_ is in Debian.
-   [Sandstorm](https://sandstorm.io/) (Apache License)
    is a platform for self-hosting web apps. It's implemented as a
    security-hardened web app package manager.
    -   [Sandstorm install instructions](https://sandstorm.io/install).
    -   [Sandstorm App Market](https://apps.sandstorm.io/).
    -   [Sandstorm docsumentation](https://docs.sandstorm.io/en/latest/).
    -   [GitHub - sandstorm](https://github.com/sandstorm-io/sandstorm).

## distribution independent application image
-   {{< wp "Flatpak" >}}
    is a package management system, and application virtualization for
    Linux , it provides a sandbox environment.
    -   [Flatpak Home](https://flatpak.org/)
    -   [Flatpak Wiki - GitHub](https://github.com/flatpak/flatpak/wiki)
    -   Search Flatpak packages at [FlatHub](https://flathub.org/home).
    -   [Flatpak - Debian Wiki](https://wiki.debian.org/FlatPak)
    -   [Flatpak - ArchWiki](https://wiki.archlinux.org/index.php/Flatpak)
-   {{< wp "AppImage" >}}
    An Appimage is a downloadable file for Linux that
    contains an application and everything the application needs to
    run (e.g., libraries, icons, fonts, translations, etc.)
    -   [AppImage Wiki](https://github.com/AppImage/AppImageKit/wiki).
    -   [AppImageHub](https://appimage.github.io/) references the known AppImages by
        categories, you can also look at the
    -   [full list of referenced applications](https://appimage.github.io/apps/)
        but this is a long list of 1020 apps, so an heavy download.
-   {{< wp "Snappy_(package_manager)"  "Snappy" >}}
    is a distribution agnostic software deployment and package
    management system for Linux.
    -   You can [search packages](https://snapcraft.io/store) at
        [snaptcraft.io](https://snapcraft.io/)
    -   [snapd](https://github.com/snapcore/snapd)
        is the background service that manages and maintains installed snaps.
        It is in Debian and is the application image system choosen by Ubuntu.
    -   [Snap - ArchWiki](https://wiki.archlinux.org/index.php/Snap)
-   [Linux Package Managers Compared - AppImage vs Snap vs Flatpak
    ](https://www.ostechnix.com/linux-package-managers-compared-appimage-vs-snap-vs-flatpak/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
