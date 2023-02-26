---
title: Booting
---

<!-- [[file:../../../../content-org/notes/system_notes/booting_notes.org][Booting Notes]] -->

# Boot Process
-  [Debian reference: The system initialization
   ](https://www.debian.org/doc/manuals/debian-reference/ch03.en.html#_stage_4_the_normal_debian_system)
-  the init daemon is the predecessor of systemd.
   -  [Debian Wiki: BootProcess](http://wiki.debian.org/BootProcess) describe the boot
      with SysVInit.
   -  [Debian Wiki: Init](http://wiki.debian.org/Init)
   -  [Debian Wiki: RunLevel](http://wiki.debian.org/RunLevel)
      SysVInit uses static runlevels usually five: Single-user, Multi-user without
      network, Multi-user  with network, shutdown, reboot.
      Systemd uses targets to group services.
  -  [Debian Wiki: LSBInitScripts](http://wiki.debian.org/LSBInitScripts)

# Hardware interface
-   {{< wp "Unified Extensible Firmware Interface" >}} (UEFI)
    is a replacement for the {{< wp "BIOS" >}} firmware interface,
-   {{< wp "Intelligent Platform Management Interface" >}} or _IPMI_
    provides management and monitoring capabilities independent of the
    firmware (BIOS or UEFI).
    -   [Comparison of ipmitool, ipmiutil, freeipmi, OpenIPMI
        ](http://ipmiutil.sourceforge.net/docs/ipmisw-compare.htm)
    -   [ipmiutil](http://ipmiutil.sourceforge.net/)
    -   [FreeIPMI](http://www.gnu.org/software/freeipmi/)
    -   [OpenIPMI](http://openipmi.sourceforge.net/)
-   [Archwiki: Unified Extensible Firmware Interface (UEFI)
    ](https://wiki.archlinux.org/index.php/Unified_Extensible_Firmware_Interface)
-   [UEFI - Debian Wiki](https://wiki.debian.org/UEFI)
-   [Firmware - Debian Wiki](https://wiki.debian.org/Firmware)
    describes the loading of device drivers. Firmwares are loaded from udev from
    `/lib/firmware`.
-   [CmosPwd](https://www.cgsecurity.org/wiki/CmosPwd) (GPL)
    is a  password recovery tool, which decrypts password stored in cmos used to access
    BIOS SETUP.
-   [Booting to the Boot Menu and BIOS](https://kb.wisc.edu/page.php?id=58779)
    gives the key for entering bbot menu and Bios on various systems.


# Grub
{{< wp " GNU GRUB" >}} is a Multiboot {{< wp "Booting#Boot_loader"  "boot loader" >}}.
GRUB2 has support for LVM and RAID.

The new generation of GRUB is _version 2_ The old version is now refered as _GRUB
Legacy_ and GRUB 2 is the default boot loader for distributions since 2009 (Ubuntu 9.10,
Debian Lenny) _the switch to v2 began in 2007_.

-   [GRUB manual](http://www.gnu.org/software/grub/manual/html_node/index.html)
-   [Debian Wiki: Grub2](https://wiki.debian.org/Grub2).
-   [Ubuntu Wiki: Grub2](https://help.ubuntu.com/community/Grub2/ISOBoot).
-   [ArchWiki: Grub2](http://wiki.archlinux.org/index.php/GRUB2)
    [GRUB/Tips and tricks](https://wiki.archlinux.org/title/GRUB/Tips_and_tricks).
-   [Gentoo Wiki: Grub2](http://wiki.gentoo.org/wiki/GRUB2).
-   [GRUB 2 bootloader - Full tutorial](https://www.dedoimedo.com/computers/grub-2.html).
-   [Super Grub2 Disk](http://www.supergrubdisk.org/wiki/SuperGRUB2Disk)
    is an image to be burned on a cdrom, or installed on an usb key.
    It is used to boot a filesystem with damaged boot loader, and
    restore an unusable grub configuration.

## Other bootloaders
-   Wikipedia {{< wp "Booting#Boot_loader"  "boot loader" >}}, {{< wp "Comparison of boot loaders" >}},
    {{< wp "Live USB" >}}
-   {{< wp "LILO_(boot_loader)"  "LILO" >}} was a discontinued boot loader for Linux.

### Syslinux
{{< wp "Syslinux" >}} is used for booting from FAT,or
as __isolinux__ from CD-ROM ISO 9660, or as __pxelinux__ from network using
{{< iref "../network/network#network_boot" "Pre-boot eXecution Environment (PXE)" >}},
or as __extlinux__ from ext2/3fs _but not ext4_.

-   [SysLinux Wiki](https://www.syslinux.org/wiki/)
-   [Archwiki: Syslinux](https://wiki.archlinux.org/index.php/Syslinux)
-   [Debian Wiki: Syslinux](https://wiki.debian.org/Syslinux)

## U-Boot
-   {{< wp "Das_U-Boot"  "U-Boot or Das_U-Boot" >}}
    is a boot loader for ARM, PowerPC, MIPS
-   [DENX U-Boot Home Page](http://www.denx.de/wiki/U-Boot)
-   [U-Boot Manual](http://www.denx.de/wiki/DULG/Manual)
-   [Introduction to Das U-Boot, the universal open source bootloader
    ](http://www.linuxfordevices.com/c/a/Linux-For-Devices-Articles/Introduction-to-Das-UBoot-the-universal-open-source-bootloader/)
    by Curt Brune.

# Booting from USB
-   Wikipedia : {{< wp "Live USB" >}}
-   [Debian Wiki: Boot Usb](https://wiki.debian.org/BootUsb)
-   [pendrivelinux.com: Boot and run Linux from a USB flash memory stick
    ](https://www.pendrivelinux.com/)
-   [Syslinux USB related problems
    ](https://www.syslinux.org/wiki/index.php?title=Hardware_Compatibility#USB_related_problems),
    [syslinux - usbkey](https://www.syslinux.org/doc/usbkey.txt),
    [How to Create a Bootable USB: For Linux
    ](https://www.syslinux.org/wiki/index.php?title=HowTos#How_to_Create_a_Bootable_USB:_For_Linux).

# Power Management
-   [Gentoo Power Management Guide
    ](https://wiki.gentoo.org/wiki/Power_management/Guide)
-   [Power management - ArchWiki
    ](https://wiki.archlinux.org/index.php/Power_management)
-   [Red Hat Enterprise Linux 7 Power Management Guide
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Power_Management_Guide/)
-   [Fedora 20 Power Management Guide
    ](https://docs.fedoraproject.org/en-US/Fedora/20/html/Power_Management_Guide/)
-   {{< man "rtcwake" >}} allow to suspend and wake up at a specified time
    you use it like this:

        $ rtcwake -m mem --date +30min

    to wake up in half an hour.

        $ rtcwake -m mem -t $(date +%s -d 'tomorrow 06:30')

    to wake up tomorrow at 6:30

    I a cron job run in the afternoon each day:

        $ rtcwake -m no -t $(date +%s -d 'tomorrow 06:30')

    wake up the system each day at 6:30, it does not put the system to
    sleep, you can do it manually or with an other cron task.

# Systemd

-   [freedesktop.org: systemd System and Service Manager
    ](http://www.freedesktop.org/wiki/Software/systemd),
    see the index there.
-   [systemd Frequently Asked Questions
    ](http://www.freedesktop.org/wiki/Software/systemd/FrequentlyAskedQuestions/).
-   [systemd TipsAndTricks
    ](http://www.freedesktop.org/wiki/Software/systemd/TipsAndTricks/).
-   [systemd manual pages](http://0pointer.de/public/systemd-man/)
-   [Debian Wiki: systemd](http://wiki.debian.org/systemd)
-   ArchWiki: [Systemd](https://wiki.archlinux.org/index.php/Systemd)
    -   [systemd/User](https://wiki.archlinux.org/index.php/Systemd/User)
    -   [shutdown with systemctl - ArchWiki
        ](https://wiki.archlinux.org/index.php/Allow_Users_to_Shutdown#Using_systemd-logind)
    -   [Power management - ArchWiki
        ](https://wiki.archlinux.org/index.php/Power_management)
-   [Gentoo Wiki: Systemd](http://wiki.gentoo.org/wiki/Systemd)
-   [Ubuntu Wiki: Systemd](https://wiki.ubuntu.com/systemd)
-   [systemd Documentation
    ](http://0pointer.de/blog/projects/systemd-docs.html)
-   __Systemd for Administrators__
    by [Lennart Poettering](http://0pointer.de/lennart/):
    [Part 1 - Verifying Bootup
    ](http://0pointer.de/blog/projects/systemd-for-admins-1.html),
    [Part II - Which Service Owns Which Processes?
    ](http://0pointer.de/blog/projects/systemd-for-admins-2.html),
    [Part III - How Do I Convert A SysV Init Script Into A systemd Service File?
    ](http://0pointer.de/blog/projects/systemd-for-admins-3.html),
    [Part IV - Killing Services
    ](http://0pointer.de/blog/projects/systemd-for-admins-4.html),
    [Part V - stop, disable and mask
    ](http://0pointer.de/blog/projects/three-levels-of-off.html),
    [Part VI - Changing Roots
    ](http://0pointer.net/blog/projects/changing-roots.html),
    [Part VII - systemd-analyze blame
    ](http://0pointer.net/blog/projects/blame-game.html),
    [Part VIII - The New Configuration Files
    ](http://0pointer.net/blog/projects/the-new-configuration-files.html),
    [Part IX - On /etc/sysconfig and /etc/default
    ](http://0pointer.de/blog/projects/on-etc-sysinit.html),
    [Part X - Instantiated Services
    ](http://0pointer.de/blog/projects/instances.html),
    [Part XI - Converting inetd Services
    ](http://0pointer.de/blog/projects/inetd.html),
    [Part XII - Securing Your Services
    ](http://0pointer.net/blog/projects/security.html),
    [Part> XIV - The Self-Explanatory Boot (systemctl status)
    ](http://0pointer.net/blog/projects/self-documented-boot.html),
    [Part XIII - Log and Service Status  (systemctl status)
    ](http://0pointer.net/blog/projects/systemctl-journal.html),
    [Part XV - Watchdogs
    ](http://0pointer.net/blog/projects/watchdog.html),
    [Part XVI - Gettys on Serial Consoles (and Elsewhere)
    ](http://0pointer.net/blog/projects/serial-console.html),
    [Part XVII - Using the Journal
    ](http://0pointer.net/blog/projects/journalctl.html),
    [Part XVIII - Managing Resources
    ](http://0pointer.net/blog/projects/resources.html),
    [Part XIX - Detecting Virtualization
    ](http://0pointer.net/blog/projects/detect-virt.html),
    [Part XX - Socket Activated Internet Services and OS Containers
    ](http://0pointer.net/blog/projects/socket-activated-containers.html),
    [Part XXI - Container Integration
    ](http://0pointer.net/blog/systemd-for-administrators-part-xxi.html).
-   [Understanding Systemd Units and Unit Files | DigitalOcean
    ](https://www.digitalocean.com/community/tutorials/understanding-systemd-units-and-unit-files)
-   The [Timer unit
    ](https://www.freedesktop.org/software/systemd/man/systemd.timer.html)
    allow a timer dependent service activation. The `WakeSystem=true`
    option allow to wake up the system from suspend.
    -   [cron, at and systemd timers
        ](http://yakking.branchable.com/posts/systemd-7-crontab-and-timers/)
        by Richard Maw, gives an example of systemd backup unit.
    -   Joey Hess  give an example in his
        [programmable alarm clock using systemd
        ](http://joeyh.name/blog/entry/a_programmable_alarm_clock_using_systemd/)
-   [Without Systemd](http://without-systemd.org/) is a site from
    opponents to systemd, they explain how to set up a system (like
    Debian) without using systemd.

## Manual pages

-   [fredesktop: systemd manual index
    ](http://www.freedesktop.org/software/systemd/man/)
-   [systemd
    ](http://www.freedesktop.org/software/systemd/man/systemd.html)
-   [systemctl
    ](http://www.freedesktop.org/software/systemd/man/systemctl.html)
-   [machinectl
    ](http://www.freedesktop.org/software/systemd/man/machinectl.html)
-   [logind
    ](http://www.freedesktop.org/wiki/Software/systemd/logind/)
-   [loginctl](http://www.freedesktop.org/software/systemd/man/loginctl.html)


For unit syntax [systemd.directives
](https://www.freedesktop.org/software/systemd/man/systemd.directives.html)
gives an index of alldirctives with the manual page where they are described. The main
pages for unit syntax are:

-   [systemd.service
    ](https://www.freedesktop.org/software/systemd/man/systemd.service.html)
    Service unit configuration.
-   [systemd.unit](https://www.freedesktop.org/software/systemd/man/systemd.unit.html)
    Unit configuration.
-   [systemd.exec](https://www.freedesktop.org/software/systemd/man/systemd.exec.html)
    the execution environment configuration.
-   [systemd.mount](https://www.freedesktop.org/software/systemd/man/systemd.mount.html)
    Mount unit configuration.xs

## /dev/console
-   For post booting configuration of the linux console terminal go to
    {{< iref "console" "Console configuration" >}}
-   At boot the console is set by default to `/dev/tty0` but can be
    changed by setting *optionally multiple* console device in a kernel
    boot option `console={device,options }*`.
-   To add a serial console look at
    [kernel documentation :serial-console.txt
    ](https://www.kernel.org/doc/Documentation/serial-console.txt),
    [Linux Serial Console HOWTO](http://www.vanemery.com/Linux/Serial/serial-console.html)
    by Van Emery, [Remote Serial Console HOWTO
    ](http://www.faqs.org/docs/Linux-HOWTO/Remote-Serial-Console-HOWTO.html)
    by Glen Turner _very detailled_,
    [Ubuntu Help: Serial Console Howto
    ](https://help.ubuntu.com/community/SerialConsoleHowto).
-   {{< wp "VESA_BIOS_Extensions"  "Wikipedia: VESA BIOS Extensions" >}}
    gives the defined vesa modes on a
    console. To change the boot ves mode append to the kernel command
    line `vga=xxx`, where  _&lt;xxxx&gt;_ is the linux mode number.
-   For a detailled explanation look at
    [Ubuntu Help: Console Framebuffer
    ](https://help.ubuntu.com/community/ConsoleFramebuffer).
-   The vesafb framebuffer driver is enhanced by the new
    [Uvesafb driver (Archwiki)](https://wiki.archlinux.org/index.php/Uvesafb)
-   [Gentoo Wiki: uvesafb](http://wiki.gentoo.org/wiki/Uvesafb).
-   [Kernel Documentation: uvesafb
    ](https://www.kernel.org/doc/Documentation/fb/uvesafb.txt).

## Kernel mode-setting
Kernel mode-setting (KMS) means that the kernel is responsible for setting up and
changing the display mode: resolution, frequencies and color depth, it allows to switch
resolution without reinitializing the graphics card/driver.

-   [Kernel Mode Setting - Debian](https://wiki.debian.org/KernelModesetting)
-   [Kernel mode setting - ArchWiki
    ](https://wiki.archlinux.org/index.php/Kernel_mode_setting)
-   KMS is available on the Intel GMA, nouveau cat and radeon drivers.
    Intel, Nouveau, ATI and AMDGPU enable KMS automatically, it has to be manually
    enabled for NVIDIA drivers.
    The [Gentoo Wiki: Intel GMA](http://wiki.gentoo.org/wiki/Intel),
    [Gentoo Wiki: AMD/ATI Radeon](http://wiki.gentoo.org/wiki/Radeon)
    give some hints for this brand of graphic drivers.
-   [Freedesktop: Kernel Mode-setting
    ](http://nouveau.freedesktop.org/wiki/KernelModeSetting/)
-   [Ubuntu Wiki: Kernel Mode Setting](https://wiki.ubuntu.com/X/KernelModeSetting) and
    [Debian Wiki: Kernel Mode Setting](http://wiki.debian.org/KernelModesetting)
    explain how to disable KMS and how to force a specific mode.
    Specifying a specific mode require to use the `video=` kernel option thet is detailled in
    [Freedesktop: nouveau - Kernel Mode Setting - Forcing Modes
    ](http://nouveau.freedesktop.org/wiki/KernelModeSetting#ForcingModes-1) and
    [Kernel mode setting, Forcing Modes - ArchWiki
    ](https://wiki.archlinux.org/index.php/Kernel_mode_setting#Forcing_modes).

The {{< iref "console#kmscon" "Kmscon terminal emulator" >}} is based on
KMS but don't require it.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
