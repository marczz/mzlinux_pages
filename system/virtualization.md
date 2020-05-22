---
title: Virtualization
---

# Emulators and virtualization References

-   This section deals with virtualization platforms or
    {{< wp "Hypervisors" }}
    that allow multiple operating systems to run on a host computer at
    the same time.
-   Wikipedia {{< wp "Comparison of virtual machines" >}}.
-   [Ubuntu Server](https://ubuntu.com/server/):
    [Virtualization](https://ubuntu.com/server/docs/virtualization-introduction)

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

# KVM (for Kernel-based Virtual Machine)
-   [KVM](http://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine)
    (some part GPL, some part LGPL) is a virtualization solution for
    Linux on x86 hardware containing virtualization extensions (Intel
    VT or AMD-V). It consists of a loadable kernel module, kvm.ko, and
    a processor specific module, kvm-intel.ko or kvm-amd.ko. KVM also
    requires a modified {{< iref "#qemu" "QEMU" >}} although work is
    underway to get the required changes upstream. The kernel component
    of KVM is included in mainline Linux, as of 2.6.20 and later.

    Using KVM, one can run multiple virtual machines running unmodified
    Linux or Windows images. Each virtual machine has private
    virtualized hardware: a network card, disk, graphics adapter, etc.

    KVM is the default virtualization technology in Ubuntu.

-   [KVM Home Page](https://www.linux-kvm.org/page/Main_Page)
-   [Using KVM virtualization – IBM Developer
    ](https://developer.ibm.com/technologies/linux/articles/l-using-kvm)
-   [Ubuntu Help: The Kernel Virtual Machine](https://help.ubuntu.com/community/KVM).

# Linux-VServer / OpenVZ
-   Os level virtualization is provided by
   [Linux-VServer](http://en.wikipedia.org/wiki/Linux-VServer)
   (GPL v.2) or its fork
   [FreeVPS](http://en.wikipedia.org/wiki/FreeVPS)
   (GPL) and [OpenVZ](http://en.wikipedia.org/wiki/OpenVZ) (GPL v.2).
-   The [Home of the vserver project linux-vserver.org](http://linux-vserver.org/)
   host the documentation and the
   [Vserver Faq](http://linux-vserver.org/Frequently_Asked_Questions).
-  [Wikipedia: OpenVz](http://en.wikipedia.org/wiki/OpenVZ),
   [Official OpenVz site](http://openvz.org/ "openvz.org"),
   [OpenVz wiki](http://wiki.openvz.org/ "wiki.openvz.org")
-  [Markus Gattol: OpenVz](http://www.markus-gattol.name/ws/openvz.html)

# LibVirt
[Libvirt](http://libvirt.org) is used to interface
with different virtualization technologies KVM, Xen, qemu, OpenVz, LXC
LXC. Libvirt is used by the virtual machine manager
[Ovirt](http://www.ovirt.org/) (GPL).

-   [ArchWiki - LibVirt](https://wiki.archlinux.org/index.php/Libvirt).
-   [Ubuntu Server](https://ubuntu.com/server/):
    [Virtualization](https://ubuntu.com/server/docs/virtualization-introduction),
    [LibVirt](https://ubuntu.com/server/docs/virtualization-libvirt).
-   [LibVirt LXC container driver](http://libvirt.org/drvlxc.html)
-   [An introduction to libvirt's LXC support](http://openvz.org/pipermail/devel/2008-September/014314.html) by Daniel P. Berrange.
-   <a name="virt-manager"></a>[virt-manager](https://virt-manager.org/)
    (GPL) is a front end to libvirt written in Python, while the UI is
    constructed with Glade and GTK+.

# LXC

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

# Qemu
[Qemu](http://wiki.qemu.org/) (GPL)is a generic  emulator and virtualizer.

As an emulator, QEMU can run guest OSes on an architecture different from the host.

When guest and host architecture is identical QEMU van be used as virtualizer
and achieve near  native performances by executing the guest code directly
on the host CPU. When using KVM, QEMU can virtualize x86, server and embedded
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
-   [Virtual Networking](http://people.gnome.org/~markmc/virtual-networking.html)
    by Mark McLoughlin.


# VirtualBox
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

# Xen
-   {{< wp "Xen" >}} is a GPL paravirtualization layer. Intermediate between
    hardware virtualization and os level virtualization,
    paravirtualization involves making the virtual server OS aware of
    the fact that it is being virtualized.

    Citrix has forked a private source _citrix server_ from Xen.

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
-   {{< wp "User-mode Linux" >}}
    gives avirtual linux machine under a linux system.
-   [Virtual Square](http://wiki.virtualsquare.org/)
    create an unified environment that allows virtual machines,
    systems and networks to communicate and interact.
    -   The virtual networking is handled by _VDE_. A _vde2_ package is in Debian.
    -   _View-OS_ is an approach to the process/kernel interface.
        UMView is a user-mode implementation of View-OS. It is packaged in Debian.
-   {{< wp "Cooperative Linux" >}}, abbreviated as coLinuxxs allows Microsoft
    Windows and the Linux kernel to run simultaneously in parallel on the same machine.
    -   [Cooperative Linux Home](http://colinux.org/).
-   The harware emulation virtual machine
    [VMware](http://en.wikipedia.org/wiki/VMware)
    provides a completely virtualized set of hardware to the guest
    operating system.


# Docker

-   [Archwiki - Docker
    ](https://wiki.archlinux.org/index.php/Docker).
-   [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
    list of Docker resources.


# Sandboxing
A a {{< wp "Sandbox_(computer_security)" "sandbox" >}} is a security mechanism for
separating running programs, usually in an effort to mitigate system failures or
software vulnerabilities from spreading.

## Security jails

-   [Security, sandboxing - ArchWiki
    ](https://wiki.archlinux.org/index.php/Security#Sandboxing_applications).
-   [Firejail](https://firejail.wordpress.com/) (GPL)
    is a SUID program that reduces the risk of security breaches by restricting
    the running environment of untrusted applications using Linux namespaces and
    {{< wp  "Secomp"  >}} filter [seccomp-bpf
    ](https://www.kernel.org/doc/html/latest/userspace-api/seccomp_filter.html).
    It is used for browsers and internet facing applications, as well as
    any servers.
    -   [Firejail - ArchWiki](https://wiki.archlinux.org/index.php/Firejail).
    -   [Firejail - GitHub](https://github.com/netblue30/firejail).
-   [Bubblewrap](https://github.com/containers/bubblewrap) (LGPL)
    is a lightweight sandbox application developed from Flatpak.
    -   [Bubblewrap - ArchWiki](https://wiki.archlinux.org/index.php/Bubblewrap).

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
