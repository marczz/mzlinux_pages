---
title: Virtualization
---

{{% toc /%}}

# Emulators and virtualization References

-   This section deals with virtualization platforms or
    [Hypervisors](http://en.wikipedia.org/wiki/Hypervisor "en.wikipedia.org Hypervisor")
    that allow multiple operating systems to run on a host computer at
    the same time.
-   [Wikipedia: Comparison of virtual machines](http://en.wikipedia.org/wiki/Comparison_of_virtual_machines)


# Chroot {#chroot}
_not a true virtualization_


-   {{< wp "chroot"  "Wikipedia: chroot" >}}
-   [Debian wiki: chroot](https://wiki.debian.org/chroot)
-   [chroot chapter of debian reference manual
    ](http://www.debian.org/doc/manuals/reference/ch09.en.html#_chroot_system)

-   [Securing Debian HowTo
    ](http://www.debian.org/doc/manuals/securing-debian-howto):
    [5.10 General chroot and suid paranoia
    ](https://www.debian.org/doc/manuals/securing-debian-howto/ch-sec-services.en.html#s-chroot),
    [Chroot environment for Apache
    ](http://www.debian.org/doc/manuals/securing-debian-howto/ap-chroot-apache-env.en.html),
    [Chroot environment for SSH
    ](http://www.debian.org/doc/manuals/securing-debian-howto/ap-chroot-ssh-env.en.html).
-   [Debian/installers FAQ list of chroot refs
    ](http://linuxmafia.com/faq/Debian/installers.html#chroot)

-   [Ubuntu documentation: Basic Chroot
    ](https://help.ubuntu.com/community/BasicChroot)
-   [ArchWiki: Change root
    ](https://wiki.archlinux.org/index.php/change_root)
-   [Debian Wiki: schroot](https://wiki.debian.org/Schroot) and
    [other schroot page](https://wiki.debian.org/RichardDarst/Schroot).
-   [Debian facile: schroot avec sid sur debian stable
    ](https://debian-facile.org/utilisateurs:niqnutn:tutos:installer-sid-sur-jessie-avec-schroot)
-   [Debian Wiki: Debootstrap](https://wiki.debian.org/Debootstrap).
-   [Debian GNU/Linux Installation Guide
    ](https://www.debian.org/releases/stable/) :
    [Appendix D.3. Installing Debian GNU/Linux from a Unix/Linux System
    ](https://www.debian.org/releases/stable/amd64/apds03.html.en)
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
-   [PRoot (ArchWiki)](https://wiki.archlinux.org/index.php/PRoot)
    is a user-space implementation of chroot, mount --bind, and
    binfmt_misc. It is in Debian
-   Debian provides the packages [chrootuid
    ](http://ftp.porcupine.org/pub/security/chrootuid1.3.README),
    _compartment_, _jailer (no longer in recent distribs)_, _makejail
    (no longer in recent distribs)_ that are used to chroot
    automatically servers and services.


# CoLinux
[CoLinux](http://www.colinux.org/) Cooperative Linux is a port
of the Linux kernel that allows it to run cooperatively alongside
another operating system on a single machine. For instance, it
allows one to freely run Linux on Windows 2000/XP/vISTA/7.

# Docker
-   [Archwiki - Docker
    ](https://wiki.archlinux.org/index.php/Docker).

# Dos emulators

-   [Bochs](http://bochs.sourceforge.net/)&nbsp; IA-32 (x86) PC
    emulator,&nbsp;
-   The
    [The FreeDOS Project](http://www.freedos.org/ "freedos.org Home")
    is an open source DOS compatible operating system most of freedos
    programs are licensed under GPL.
    [FreeDos at ibiblio.org](http://www.ibiblio.org/pub/micro/pc-stuff/freedos/ "ibiblio.org: freedos"),
    [freedos boot disks](http://www.fdos.org/bootdisks/ "fdos.org bootdisks").
-   [Keyb](http://projects.freedos.net/keyb/) under dos
-   [DOSBox](http://dosbox.sourceforge.net/)a x86 emulator with DOS
-   [dave links](http://www.opus.co.tt/dave/) to various DOS software
    and other DOS related websites.
-   [dosemu](http://www.dosemu.org) a \\`DOS box' under linux.
    [The dosemu HOWTO](http://dosemu.sourceforge.net/docs/HOWTO/)
-   This
    [WPDOS - WP Under Linux](http://www.columbia.edu/%7Eem36/wpdos/linux.html)
    page is part of the
    [WordPerfect for DOS Updated](http://www.columbia.edu/%7Eem36/wpdos/)
    site at Columbia university.
    ([Corel ftp for wpdos](ftp://ftp.corel.com/pub/WordPerfect/wpdos/))
-   [bootdisk.com](http://www.bootdisk.com/)
-   [Dosemu HowTo](http://tldp.org/HOWTO/DOSEMU-HOWTO.html)
-   Notes:
    :   Toggle between windowed and fullscreen mode using Ctrl-Alt-F

# KVM (for Kernel-based Virtual Machine)
-   [KVM](http://en.wikipedia.org/wiki/Kernel-based_Virtual_Machine "en.wikipedia.org: KVM")
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

-   [Discover the Linux Kernel Virtual Machine](http://www.ibm.com/developerworks/linux/library/l-linux-kvm/ "ibm.com/developerworks l-linux-kvm")
    by M. Tim Jones at Ibm Developerworks.
-   [KVM Wiki](http://kvm.qumranet.com/kvmwiki "kvm.qumranet.com kvmwiki"),
    [KVM HowTo on U32](http://u32.net/KVM/ "u32.net KVM").
-   [Ubuntu Server Guide](https://help.ubuntu.com/9.10/serverguide/C/ "help.ubuntu.com/9.10 serverguide")
-   [Ubuntu Help: The Kernel Virtual Machine](https://help.ubuntu.com/community/KVM "help.ubuntu.com KVM").
-   [JeOS](https://help.ubuntu.com/9.10/serverguide/C/jeos-and-vmbuilder.html "help.ubuntu.com/9.10 serverguide jeos-and-vmbuilder.html")
    is an efficient variant of the Ubuntu Server operating system,
    configured specifically for virtual appliances.

# Linux-VServer / OpenVZ
-   Os level virtualization is provided by
   [Linux-VServer](http://en.wikipedia.org/wiki/Linux-VServer "en.wikipedia.org Linux-VServer")
   (GPL v.2) or its fork
   [FreeVPS](http://en.wikipedia.org/wiki/FreeVPS "en.wikipedia.org FreeVPS")
   (GPL) and [OpenVZ](http://en.wikipedia.org/wiki/OpenVZ) (GPL v.2).

-   The [Home of the vserver project linux-vserver.org](http://linux-vserver.org/ "linux-vserver.org")
   host the documentation and the
   [Vserver Faq](http://linux-vserver.org/Frequently_Asked_Questions "linux-vserver.org FAQ").
-   [Gentoo Virtual Private Server Project](http://www.gentoo.org/proj/en/vps/ "gentoo.org vps")
   maintain the projects
   [Linux-VServer](http://www.gentoo.org/proj/en/vps/vserver-howto.xml "gentoo.org vps")
   and
   [OpenVZ](http://www.gentoo.org/proj/en/vps/openvz-howto.xml "gentoo.org vps")
   on gentoo.
-   [Wikipedia: OpenVz](http://en.wikipedia.org/wiki/OpenVZ "en.wikipedia.org OpenVZ"),
   [Official OpenVz site](http://openvz.org/ "openvz.org"),
   [OpenVz wiki](http://wiki.openvz.org/ "wiki.openvz.org")
-  [Markus Gattol: OpenVz](http://www.markus-gattol.name/ws/openvz.html)

# LibVirt
[Libvirt](http://libvirt.org "libvirt.org") is used to interface
with different virtualization technologies KVM, Xen, qemu, OpenVz, LXC
LXC. Libvirt is used by the virtual machine manager
[Ovirt](http://www.ovirt.org/ "ovirt.org") (GPL), and is the used
in Ubuntu since 8.04.

-   [ArchWiki - LibVirt](https://wiki.archlinux.org/index.php/Libvirt).
-   [Ubuntu Server Guide](https://help.ubuntu.com/lts/serverguide/)
    [Virtualization](https://help.ubuntu.com/lts/serverguide/virtualization.html),
    [LibVirt](https://help.ubuntu.com/lts/serverguide/libvirt.html).
-   [LibVirt LXC container driver](http://libvirt.org/drvlxc.html)
-   [An introduction to libvirt's LXC support](http://openvz.org/pipermail/devel/2008-September/014314.html) by Daniel P. Berrange.
-   [virt-manager](http://virt-manager.et.redhat.com "virt-manager.et.redhat.com")
    (GPL) is a front end to libvirt written in Python, while the UI is
    constructed with Glade and GTK+.

# LXC

Linux container tools (LXC) is a virtualization method for running multiple isolated
server  on a single control host. It provides a virtual
environment that has its own process and network space.
e Minute Guide to Linux Containers for Debian     Lxc is similar to a chroot, but with much more isolation.

-   [ArchWiki - Linux Containers
    ](https://wiki.archlinux.org/index.php/Linux_Containers).
-   [ArchWiki - Cgoups](https://wiki.archlinux.org/index.php/Cgroups).
-   [Ubuntu serverguide - cgroups
    ](https://help.ubuntu.com/lts/serverguide/cgroups.html).
-   [Ubuntu serverguide - LXC](https://help.ubuntu.com/lts/serverguide/lxc.html)
-   [LXC HOWTO](http://lxc.teegra.net) by Dwight Schauer.
-   [Using Linux Containers with Debian Lenny
    ](http://jim.studt.net/depository/index.php/using-linux-containers-with-debian-lenny) and
    [Letting your LXC containers use virtual consoles
    ](http://jim.studt.net/depository/index.php/letting-your-lxc-containers-use-consoles)
    by Jim Studt.
-   [LXC tour and set up
    ](https://www.ibm.com/developerworks/linux/library/l-lxc-containers/)
    by Matt Helsley at IBM  developerWorks.
-   [A Five Minute Guide to Linux Containers for Debian
    ](http://nigel.mcnie.name/blog/a-five-minute-guide-to-linux-containers-for-debian)
    by Nigel McNie gives a better lxc-debian configuration and explains it's use.
-   Kernel [cgroups doc directory
    ](http://www.mjmwired.net/kernel/Documentation/cgroups/)
    with documentation on [kdoc:cgroups/cgroups.txt|cgroups]  and
    [kdoc:cgroups/devices.txt|devices].
-   [bodhizazen blog](http://blog.bodhizazen.net/) contains LXC tutorials.
-   [Markus Gattol: Linux Containers
    ]( http://www.markus-gattol.name/ws/linux_containers.html)

# Qemu
[Qemu](http://wiki.qemu.org/) (GPL)is a generic  emulator and virtualizer.

As an emulator, QEMU can run guest OSes on an architecture different from the host.

When guest and host architecture is identical QEMU van be used as virtualizer
and achieve near  native performances by executing the guest code directly
on the host CPU. When using KVM, QEMU can virtualize x86, server and embedded
PowerPC, and S390 guests.


-   [Qemu Documentation](http://wiki.qemu.org/Manual):
    [QEMU User manual](http://wiki.qemu.org/download/qemu-doc.html),
    [Qemu networking](http://wiki.qemu.org/Documentation/Networking).
-   [The qemu forum](http://qemu-forum.ipi.fi/),
-   Wikipedia: {{< wp "Qemu" >}}.
-   [Qemu Wikibook](http://en.wikibooks.org/wiki/QEMU) has sections:
    [Installing QEMU](http://en.wikibooks.org/wiki/QEMU/Installing_QEMU),
    [Creating and Manipulating Images](http://en.wikibooks.org/wiki/QEMU/Images),
    [Networking](http://en.wikibooks.org/wiki/QEMU/Networking),
    [Using the Monitor](http://en.wikibooks.org/wiki/QEMU/Monitor),
    [Windows XP Guest](http://en.wikibooks.org/wiki/QEMU/Windows_XP)
    [FreeDOS Guest](http://en.wikibooks.org/wiki/QEMU/FreeDOS)
-   [Ububtu server guide - Qemu
    ](https://help.ubuntu.com/lts/serverguide/qemu.html)
-   [Gentoo Wiki: Qemu](https://wiki.gentoo.org/wiki/QEMU).
-   [List of OSes working under qemu](http://www.claunia.com/qemu/)
-   [Arch Linux Qemu Page](http://wiki.archlinux.org/index.php/QEMU)
    is a tutorial with a chapter
    on _using any real partition as the single primary partition of a hard disk image_
-   [Mark Mc Loughlin](http://blogs.gnome.org/markmc/ "Mark McLoughlin blog"):
    [The QCOW2 Image Format](http://people.gnome.org/~markmc/qcow-image-format.html),
    [QEMU Networking](http://people.gnome.org/~markmc/qemu-networking.html),
    [Virtual Networking](http://people.gnome.org/~markmc/virtual-networking.html)
-   [Simulate complex networks with qemu](http://aplawrence.com/Girish/qemu.html)
    by Girish Venkatachalam
-   [Aboriginal Linux](http://landley.net/aboriginal/)
    is a set of tools to build custom virtual machines under QEMU.


# User Mode Linux
[User Mode Linux](http://user-mode-linux.sourceforge.net/)
gives avirtual linux machine under your (linux) system.
[HOWTO User Mode Linux](http://gentoo-wiki.com/HOWTO_User_Mode_Linux)
from the Gentoo Wiki.

# Virtual Square
[Virtual Square](http://wiki.v2.cs.unibo.it/wiki/index.php/Main_Page)
create an unified environment that allows virtual machines,
systems and networks to communicate and interact.
-   The virtual networking is handled by _VDE_. A _vde2_ package is in Debian.
-   _View-OS_ is an approach to the process/kernel interface.
    UMView is a user-mode implementation of View-OS. It is packaged in Debian.

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
-   There are numerous tutorial to virtual box on Ubuntu:
    -   [Ubuntu community VirtualBox documentation
        ](https://help.ubuntu.com/community/VirtualBox),
    -   [VirtualBox Installation
        ](https://help.ubuntu.com/community/VirtualBox/Installation),
    -   [VirtualBox GuestAdditions
        ](https://help.ubuntu.com/community/VirtualBox/GuestAdditions),
    -   [VirtualBox SharedFolders
        ](https://help.ubuntu.com/community/VirtualBox/SharedFolders).
    [Testing Iso images with VirtualBox
    ](https://wiki.ubuntu.com/Testing/VirtualBox)


# VMware
-   The harware emulation virtual machine
    [VMware](http://en.wikipedia.org/wiki/VMware "en.wikipedia.org VMware")
    provides a completely virtualized set of hardware to the guest
    operating system.

-   VMware can be
    [installed under ubuntu](https://help.ubuntu.com/community/VMware "help.ubuntu.com VMware")
    following
    [Ubuntu help: VMware/Player](https://help.ubuntu.com/community/VMware/Player "help.ubuntu.com VMware Player")
    or
    [Ubuntu help: VMware/Server](https://help.ubuntu.com/community/VMware/Server "help.ubuntu.com VMware Server").

# Wine
-   {{< wp "Wine (software)" >}} implementation of the Win32 API,
-   [Wine hq](http://www.winehq.com/)
-   [Wine Documentation](http://www.winehq.org/site/documentation) and
    [HowTo](http://wiki.winehq.org/HowTo)
-   [Running Windows applications on Linux using Wine](http://www.frankscorner.org/)
    ( Frank's corner)
-   [CodeWeavers](http://www.codeweavers.com/) sell a customized wine.

# Xen
-   Xen is a GPL paravirtualization layer. Intermediate between
    hardware virtualization and os level virtualization,
    paravirtualization involves making the virtual server OS aware of
    the fact that it is being virtualized.

-   Xen has now been acquired by citrix so the home page of Xen is now
    [citrixxenserver.com](http://www.citrixxenserver.com/ "citrixxenserver.com")
    you find there a lot of advertisements for citrix. If you use
    mainly free opensource product you may be disapointed and agree
    with the subtitle that proclame "end of virtualization is here"!
-   There is still an
    [open source home page at xen.org](http://www.xen.org/ "xen.org").
-   [Xen Wiki](http://wiki.xensource.com/xenwiki/ "wiki.xensource.com xenwiki"),
    [Xen Faqs](http://www.xensource.com/products/xen/faqs.html "xensource.com Faqs").
-   [HOWTO Xen and Gentoo](http://gentoo-wiki.com/HOWTO_Xen_and_Gentoo "gentoo-wiki.com HOWTO_Xen_and_Gentoo")
-   Ubuntu doc:
    [Xen Virtual Machine](https://help.ubuntu.com/community/XenVirtualMachine "help.ubuntu.com XenVirtualMachine")
    is subsumed by
    [Xen on Ubuntu](https://help.ubuntu.com/community/Xen "help.ubuntu.com Xen")
-   Xen can even run unmodified windows on
    [HVM Compatible Processors](http://wiki.xensource.com/xenwiki/HVM_Compatible_Processors "xensource.com/xenwiki HVM_Compatible_Processors")
    as described in
    [Xen install windows *(pdf)*](http://www.xensource.com/files/xen_install_windows.pdf "xensource.com xen_install_windows.pdf")

# Docker


-   [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
    list of Docker resources.


# Sandboxing

-   {{< wp "Flatpak" >}}
    is a package management system, and application virtualization for
    Linux , it provides a sandbox environment.
-   {{< wp "AppImage" >}}
    An Appimage is a downloadable file for Linux that
    contains an application and everything the application needs to
    run (e.g., libraries, icons, fonts, translations, etc.)
    -   [AppImage Wiki](https://github.com/AppImage/AppImageKit/wiki).
-   {{< wp "Snappy_(package_manager)"  "Snappy" >}}
    is a distribution agnostic software deployment and package
    management system for Linux.
    -   [snaptcraft.io](https://snapcraft.io/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
