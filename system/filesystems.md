---
title: File Systems
---

<!--
See also [[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/hardware/hdrive.md][Hard Drive]] ([[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/hardware/hdrive.md:: #partition_table][Partition Tables]], [[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/hardware/hdrive.md #partionning][Partitionning]]),
[[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/hardware/network_filesystems.md][network filesystems]] , [[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/hardware/encrypted_filesystems.md][encrypted Filesystems]]
-->

See also the companion pages on
{{< iref "network_filesystems" "network filesystems" >}},
{{< iref "encrypted_filesystems" "encrypted filesystems" >}}
The lower level is in the section
{{< iref "hdrive" "Hard Drive" >}}
where you find the
{{< iref "hdrive#partition_table" "partition tables" >}}
and {{< iref "hdrive#partitioning" "partitioning" >}}.

----

# General References
-   LDP HOWTOs
    -   [Filesystems HOWTO](http://ldp.tuke.sk/HOWTO/Filesystems-HOWTO.html)
        About filesystems and accessing filesystems. _2007_
    -   [Linux Filesystem Hierarchy
        ](http://www.tldp.org/LDP/Linux-Filesystem-Hierarchy/html/)
        _2004_
    -   [Linux Partition HOWTO](http://www.tldp.org/HOWTO/Partition/)
        _2005_
    -   [The Software RAID HowTo
        ](http://www.tldp.org/HOWTO/Software-RAID-HOWTO.html),
        _2010_
    -   [Quota mini-HOWTO](http://www.tldp.org/HOWTO/Quota.html)
        _2003_
-   Wikipedia:
    {{< wp "List of file systems" >}},
    {{< wp "Comparison of file systems" >}}, {{< wp "Fat" >}}, {{< wp "ext2" >}}, {{< wp "ext3" >}},
    {{< wp "ext4" >}}, {{< wp "XFS" >}}, {{< wp "Reiser4" >}}, {{< wp "ZFS" >}}, {{< wp "Btrfs" >}}, {{< wp "NTFS" >}},
    {{< wp "Network File System" >}},
    {{< wp "Andrew file system" >}},
    {{< wp "Server Message Block" >}} (SMB), {{< wp "Samba software" >}},
    [fuse](http://en.wikipedia.org/wiki/FUSE_%28Linux%29),
    {{< wp "JFFS2" >}}, {{< wp "UBIFS" >}}, {{< wp "SquashFS" >}}, {{< wp "UnionFS" >}},
    {{< wp "Sysfs" >}}, {{< wp "Procfs" >}},
    {{< wp "Redundant_array_of_independent_disks"  "RAID" >}}
-   [ArchWiki: File Systems
    ](https://wiki.archlinux.org/index.php/File_systems)
-   [Gentoo Wiki: Filesystems
    ](https://wiki.gentoo.org/wiki/Filesystem)
    has an index of filesystems.
-   [Suse SLE: Major File Systems in Linux
    ](https://www.suse.com/documentation/sles11/stor_admin/data/sec_filesystems_major.html)
-   [RAID Wiki: comparison of performance of different types of RAIDs
    ](https://raid.wiki.kernel.org/index.php/Performance)

# Disk filesystems
-   {{< wp "Ext4" >}} filesystem is the previous default filesystem on linux
    and the successor of  {{< wp "ext2" >}}and {{< wp "ext3" >}}
    -   [ArchWiki: Ext4](https://wiki.archlinux.org/index.php/Ext4)
    -   [GentooWiki: Ext4](https://wiki.gentoo.org/wiki/Ext4)
    -   [Linux kernel documentation - Ext4
        ](https://www.kernel.org/doc/html/latest/filesystems/ext4/index.html?)
        a low level description of the Ext4 fs structure.

    On an ext2/ext3 file system some default for the mount options,
    are managed by `tune2fs -o`
    ([tune2fs(8)](http://man.cx/tune2fs(8))) it includes `user_xattr,
    acl`, on an other hand some features are characteristics of the
    file system and cannot be modified dynamically at mount they are
    set or cleared by `tune2fs -O` : it includes `dir_index, filetype,
    has_journal`

    All characteristics of the ext2/3 file system are part of the
    output of [dumpe2fs(8)](http://man.cx/dumpe2fs(8)).

-   {{< wp "ReiserFS" >}} is a very fast journaled filesystem based on fast
    balanced tree (Reiser4 uses dancing trees).
-   {{< wp "ZFS" >}} ({{< wp "CDDL" >}} License) is a  file system and logical volume manager designed by Sun.
     ZFS ihas data integrity verification, support for high storage capacities,
    filesystem and volume management, snapshots and copy-on-write clones, continuous integrity checking and automatic repair, RAID-Z and native NFSv4 ACLs.
    -   A blog from Richard Hartmann:
        [Raid Suck](http://richardhartmann.de/blog/posts/2012/02/RAID-sucks/)
        propose to turn from Raid to ZFS.
    -   ZFS is the native filesystem of OpenSolaris, because of a license incompatibility
        ZFS is not proposed on Linux Kernel
        except as [ZFS-Fuse](http://zfs-fuse.net/)
        but it is used on FreeBSD systems including the new
        [Debian_GNU/kFreeBSD](http://wiki.debian.org/Debian_GNU/kFreeBSD_FAQ).
    -   There is also a [Native ZFS for Linux](http://zfsonlinux.org/) that you have
        just to download as source and build yourself to comply with the
        kernel __and__ zfs license.
    -   [OpenZFS](http://www.open-zfs.org/wiki/Main_Page)
        is the the  open source successor to the ZFS project.
    -   [ArchWiki: ZFS](https://wiki.archlinux.org/index.php/ZFS)
    -   [Gentoo Wiki: ZFS](https://wiki.gentoo.org/wiki/ZFS)
-   {{< wp "XFS" >}} is a journaling file system created by Silicon Graphics,
    It is based on allocation group which allow good performance on
    parallel input/output (I/O) operations, and  file system
    bandwidth.
    It uses  metadata journaling and supporting write barriers and
    allocate databy extents organized in a B-Tree.
    It has no provision for snapshots except through lvm, on-line
    resizing can be done only for extending the fs, XFS partitions
    cannot be shrunk in place.
    -   [RedHat entreprise storage administration - XFS
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-xfs),
        [Tuning XFS
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html-single/performance_tuning_guide/index#sect-Red_Hat_Enterprise_Linux-Performance_Tuning_Guide-Configuring_file_systems_for_performance-Tuning_XFS)

## Btrfs
{{< wp "Btrfs" >}} (GPL) is a copy-on-write file system which is an improvement of
ext3/ext4 file system. It offers numerous {{< wp "Btrfs#Features" "new features" >}}
including copy-on-write snapshots of files and subvolumes, checksums, transparent
compresssion.

-   The main site is the
    [Kernel Brtfs Wiki](https://btrfs.wiki.kernel.org)
    it holds on the Home page a [list of Guides and articles
    ](https://btrfs.wiki.kernel.org/index.php/Main_Page#Guides_and_usage_information)
    and the [Btrfs FAQ](https://btrfs.wiki.kernel.org/index.php/FAQ).
-   [Red Hat Storage Administration Guide - Chapter 6. Btrfs
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-btrfs)
-   [Suse storage administration: Btrfs filesystem
    ](https://www.suse.com/documentation/sles-12/stor_admin/data/sec_filesystems_major_btrfs.html),
    [Btrfs Error: No space is left on device
    ](https://www.suse.com/documentation/sles11/stor_admin/data/trbl_btrfs_volfull.html).
-   [Oracle Linux -  The Btrfs File System
    ](https://docs.oracle.com/cd/E37670_01/E37355/html/ol_btrfs.html)
-   [Debian Wiki: Btrfs](https://wiki.debian.org/Btrfs)
-   [ArchWiki: Btrfs](https://wiki.archlinux.org/index.php/Btrfs),
    [Btrfs - Tips and tricks
    ](https://wiki.archlinux.org/index.php/Btrfs_-_Tips_and_tricks),
-   [GentooWiki: Btrfs](https://wiki.gentoo.org/wiki/Btrfs),
    [Btrfs/System Root Guide - Gentoo Wiki
    ](https://wiki.gentoo.org/wiki/Btrfs/System_Root_Guide)
-   Manpages: {{< man "mkfs.btrfs(8)" >}}, {{< man "btrfsctl(8)" >}},
    {{< man "btrfs-show(8)" >}}, {{< man "mkfs.btrfs(8)" >}} and other in brtfs-tools.
-   [Ubuntu Community Help: Btrfs
    ](https://help.ubuntu.com/community/btrfs).
-   Marc Merlin [Btrfs overview, LinuxCon 2014
    ](http://marc.merlins.org/linux/talks/Btrfs-LC2014-JP/Btrfs.pdf)
    _(pdf)_
    and [Linux Btrfs posts](http://marc.merlins.org/perso/btrfs/)
-   [compsize](https://github.com/kilobyte/compsize) (GPL)
     takes a list of files (given as arguments) on a btrfs filesystem and measures used
     compression types and effective compression ratio.

The use of subvolumes is explained in the
[Btrfs FAQ](https://btrfs.wiki.kernel.org/index.php/FAQ) in the [Subvolume section
](https://btrfs.wiki.kernel.org/index.php/FAQ#Subvolumes) the choice bteween using btrfs
and subvolumes over a raw partition or over a LVM layer is discussed in
[Interaction with partitions, device managers and logical volumes
](https://btrfs.wiki.kernel.org/index.php/FAQ#Interaction_with_partitions.2C_device_managers_and_logical_volumes).
To summarize: a raw partition has a light performance benefit, but you can no longer
shrink or move online. Lvm allow to use pvmove.
Using subvolumes instead of LV will increase performances and avoid dupliacate data
storage, but a single subvolume can use all space.


# Flash memory and ssd filesystems
-   Wikipedia: {{< wp "Secure Digital" >}}
-   Gentoo Wiki: [SSD](https://wiki.gentoo.org/wiki/SSD) and
    [SD card](https://wiki.gentoo.org/wiki/SDCard). A precious source
    of information on these media.
-   [In-depth on how SSDs really work
    ](https://arstechnica.com/information-technology/2012/06/inside-the-ssd-revolution-how-solid-state-disks-really-work/).
-   [Wikipedia: jjfs2](http://en.wikipedia.org/wiki/JFFS2), is a file
    system for
    [memory technology device](http://www.linux-mtd.infradead.org/)
    and
    [not a block device
    ](http://www.linux-mtd.infradead.org/faq/general.html#L_mtd_what)
    nor a
    [removable flash media
    ](http://www.linux-mtd.infradead.org/faq/jffs2.html#L_stick_jffs2)
    usb key or flash card.
    -   [mtd.infradead.org jffs2 documentation](http://www.linux-mtd.infradead.org/doc/jffs2.html)
        is quite short and can be completed by the article by David
        Woodhouse
    -   [JFFS : The Journalling Flash File System](http://sources.redhat.com/jffs2/jffs2-html/)
        ( also in
        [pdf](http://linux-mtd.infradead.org/~dwmw2/jffs2.pdf))
        Look also at the previously referred
        [FAQ](http://www.linux-mtd.infradead.org/faq/general.html)
-   {{< wp "SquashFS" >}} is a compressed read-only file system, squashFS is
    capable of de-duplicating the data
    -   [SquashFS HOWTO
        ](http://www.tldp.org/HOWTO/html_single/SquashFS-HOWTO/)
        2010
    -   [Gentoo Wiki: SquashFS
        ](https://wiki.gentoo.org/wiki/SquashFS)
    -   [SquashFs Home Page at sourceforge
        ](http://squashfs.sourceforge.net/)
-   {{< wp "UBIFS" >}} is a successor to JFFS2. But while JFFS2 file system
    works on top of MTD devices, but UBIFS works on top of
    {{< wp "Unsorted Block Images" >}} (UBI) volumes, and cannot operate on top
    of {{< wp "Memory_Technology_Device"  "MTD" >}}.
    -   [linux-mtd](http://www.linux-mtd.infradead.org/)
        main reference for
        [UBIFS](http://www.linux-mtd.infradead.org/doc/ubifs.html) and
        [UBI](http://www.linux-mtd.infradead.org/doc/ubi.html).

## Bootable SD Card
-   [Gentoo Wiki SD card](https://wiki.gentoo.org/wiki/SDCard)
    explain how to format a SD card for io speed, and compare the
    speed of diferent file system.
-   When using a filesystem on a sd card, we should avoid  wearing it
    off by disabling swap, or in raspberry remove `dphys-swapfile`.
    using the `noatime` option, highly used directories such as
    `/var/tmp/` can be put in RAM _tmpfs_, putting /var/log in RAM is
    also an option, but we can no longer examine the logs after a crash.
    It is also possible to disable journaling, but any unwanted
    dismount will result in data loss. On Raspberry 3 we can
    [boot from external USB device
    ](https://www.raspberrypi.org/documentation/hardware/raspberrypi/bootmodes/msd.md)
    but this option is not available with earlier releases.
    Using a bigger sd card also augment the wear levelling capacity,
    and so increase the lifetime of sd cards.
-   [F3](http://oss.digirati.com.br/f3/) (GPL)
    is used to test sdcards.  it uses the same algorithm than
    [h2testhw](https://www.heise.de/download/product/h2testw-50539).
    that is [used to detect counterfeit flash cards
    ](https://sosfakeflash.wordpress.com/2008/09/02/h2testw-14-gold-standard-in-detecting-usb-counterfeit-drives/)
    (see also [Fighting flash fraud on Ebay
    ](https://fightflashfraud.wordpress.com/2008/11/24/h2testw-gold-standard-in-detecting-fake-capacity-flash/).

    [Armbian recommend to verify SD cards with F3
    ](https://docs.armbian.com/User-Guide_Getting-Started/#how-to-prepare-a-sd-card).
    F3 is packaged in Debian.
    -   [F3 Documentation
        ](https://fight-flash-fraud.readthedocs.io/en/latest/).
    -   [F3 github repository](https://github.com/AltraMayor/f3).
-   [Etcher](https://github.com/resin-io/etche) (Apache2 License)
    is an OS image flasher built on electron which run on any platform supported by
    Electron includinx linux, windoze, mac OS.
    It checks that every byte of data was written correctly.

    The software is provided as an app image, It also provides a Debian repository to
    install the node application.

    This tool, and _usbimager_ are [recommended by armbian
    ](https://docs.armbian.com/User-Guide_Getting-Started/#how-to-prepare-a-sd-card)
    for writing images.

    There was previously a CLI version which did not
    require the electron stuff, but it was removed _without explanation_ at version
    1.5.0 - 2019-02-16.
-   [mkusb](https://help.ubuntu.com/community/mkusb)
    is a wrapper around _dd_ to flash or clone an iso image or a compressed image file
    to a mass storage device, either an USB drive, an internal drive or an eSATA drive.
    _Mkusb_ is the recommended ubuntu tool to create a bootable drive. It exists in
    several flavors. The GUI version named _mkusb_, a text only interface _mkusb-nox_, a
    simple shell script _mkusb-min_.
    -   [mkusb PPA](https://launchpad.net/~mkusb/+archive/ubuntu/ppa)
    -   [How to make usb boot drive](https://ubuntuforums.org/showthread.php?t=1958073)
        is an ubuntu mkusb tutorial.
    -   [mkusb quick start manual (pdf)
        ](https://phillw.net/isos/linux-tools/mkusb/mkUSB-quick-start-manual-12.pdf)
    -   [How to install mkusb in Debian
        ](https://help.ubuntu.com/community/mkusb/install-to-debian).
    -   _mkusb-min_, minimal shell script can be downloaded and used following the
        [mkusb-min manual](https://help.ubuntu.com/community/mkusb/min).
-   [usbimager](https://gitlab.com/bztsrc/usbimager) (MIT Licence)
    is a GUI application that writes compressed disk images to USB drives and creates
    backups. It is lighter than _balena-etcher_. The repository provides Debian and
    Raspbian packages
-   [Ventoy](https://github.com/ventoy/Ventoy) (GPL 3.0)
    creates bootable USB drive for ISO/WIM/IMG/VHD(x)/EFI files. 86 Legacy BIOS, IA32
    UEFI, x86_64 UEFI, ARM64 UEFI and MIPS64EL UEFI with  MBR or GPT partition are
    supported.

An advice given by _mkusb_ manual is if you want to re-use a USB drive previously used
for a booting image, you should wipe the first megabyte it with dd (overwrite with
zeros), otherwise grub-install doesn't want to write into the mbr area, because it
recognizes the CD file system



# LVM {#lvm}

-   Wikipedia: {{< wp "LVM" >}}
-   [LVM2](http://sourceware.org/lvm2/) (previously at
    [RedHat - LVM2](http://sources.redhat.com/lvm2)) is an
    userspace toolset that provide logical volume management, lvm is
    build on top of the kernel module
    [Device Mapper](http://sources.redhat.com/dm/). See
    also the old
    [RedHat - Device-mapper and LVM2 Wiki
    ](http://sources.redhat.com/lvm2/wiki/).
-   [Red Hat - Configuring and managing logical volumes
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_logical_volumes/index)
-   [RedHat: Logical Volume Manager Administration Guide
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/index)
    ([PDF
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/pdf/Logical_Volume_Manager_Administration/Red_Hat_Enterprise_Linux-5-Logical_Volume_Manager_Administration-en-US.pdf)).
    is a very detailled documentation on LVM, it has chapters:

    -   1) LVM - presentation, news, Logical Volumes, LVM Architecture Overview, LVM in a
        Red Hat High Availability Cluster
    -   2) LVM Components - Physical Volumes, Volume Groups,  Logical Volumes
    -   3) LVM Administration Overview -  Logical Volume Creation,  Growing a File
            System on a Logical Volume, Logical Volume Backup, Logging, The Metadata
            Daemon (lvmetad), Displaying LVM Information with the lvm Command
    -   4) LVM Administration with CLI Commands -  Using CLI Commands, Physical Volume,
            Volume Group,  Logical Volume, Controlling LVM Device Scans with Filters,
             Online Data Relocation, . Activating Logical Volumes on Individual Nodes in
            a Cluster, Customized Reporting for LVM,
    -   5) LVM Configuration Examples - LVM Logical Volume on Three Disks,  Striped
           Logical Volume, Splitting a Volume Group, Removing a Disk from a Logical
           Volume, Creating a Mirrored LVM Logical Volume in a Cluster
    -   6)  LVM Troubleshooting
    -   A) The Device Mapper - Device Table Mappings,  The dmsetup Command, Device
        Mapper Support for the udev Device Manager.
    -   B) The LVM Configuration Files
    -   C) LVM Selection Criteria
    -   D) LVM Object Tags
    -   E) LVM Volume Group Metadata

    The RedHat LVM Guide has information on
    [thinly provisionned volumes, snapshot volumes, thinly provisionned snapshots
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/lv_overview#thinprovisioned_volumes)
    -   [Creating Thinly-Provisioned Logical Volumes
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/LV#thinly_provisioned_volume_creation).
    -   [Creating Snapshot Volumes
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/lv#snapshot_command)
    -   [Creating Thinly-Provisioned Snapshot Volumes
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/logical_volume_manager_administration/lv#thinly_provisioned_snapshot_creation).

-   [Suse Storage Administration Guide
    ](https://www.suse.com/documentation/sles-15/book_storage/data/book_storage.html)
    has an [LVM Section
    ](https://www.suse.com/documentation/sles-15/book_storage/data/part_lvm.html).
-   [Fedora Storage Administration Guide
    ](https://docs.fedoraproject.org/en-US/Fedora/14/html/Storage_Administration_Guide/index.html)
    has an [LVM Chapter
    ](https://docs.fedoraproject.org/en-US/Fedora/14/html/Storage_Administration_Guide/ch-lvm.html)
    that is mainly focused on the use of their tool
    [system-config-lvm](https://fedoraproject.org/wiki/SystemConfig/lvm), a graphical
    interface for lvm tools. _system-config-lvm_ is also available as a Debian package.
-   [tldp: LVM HOWTO](http://www.tldp.org/HOWTO/LVM-HOWTO/index.html)
    _2006_
-   [Debian Wiki: LVM](https://wiki.debian.org/LVM)
-   [Gentoo Wiki: LVM](https://wiki.gentoo.org/wiki/LVM) as a chapter on
    [Thin provisionning](https://wiki.gentoo.org/wiki/LVM#Thin_provisioning).
-   [ArchWiki: LVM](https://wiki.archlinux.org/index.php/LVM),
    [ArchWiki: Software RAID and LVM
    ](https://wiki.archlinux.org/index.php/Software_RAID_and_LVM)
-   [lvmthin(7)](https://manpages.debian.org/testing/lvm2/lvmthin.7.en.html).

# Fuse {#fuse}
-   [Fuse](http://fuse.sourceforge.net/) (GPL and LGPL) (
    [Wiki](http://sourceforge.net/p/fuse/wiki/))
    virtual filesystem in userspace.
-   __Fuse__ supports numerous filesystems
    [sourceforge fuse filesystems list
    ](http://sourceforge.net/p/fuse/wiki/FileSystems/) including
    [network file systems
    ](http://sourceforge.net/p/fuse/wiki/NetworkFileSystems/)
-   See also the list in Wikipedia: {{< wp "Filesystem in Userspace" >}}.
-   __Fuse__ can be used with {{< iref "#gvfs" "Gvfs" >}} with
    a D-bus daemon `gvfs-fuse` to access all gvfs enabled file systems
    including *sftp*, *ftp*, *dav*, dav over ssl *davs*, *smb*,
    smb-browse (with gvfs-ls), *http*, obexftp, medias (burn, cdda,
    gphoto2) and archive mounting support, for info look at my
    {{< iref "#gvfs" "Gvfs section" >}}.

-   [adbfs](http://collectskin.com/adbfs/)
    Mount an Android device filesystem.
-   {{< wp "archivemount" >}} (LGPL)
    is a FUSE file system to mount archives supported by libarchive,
    including write support. It support tar, pax, cpio, ISO9660 CD,
    zip archives, shar.  It is in Debian. You can also use the
    {{< iref "#gvfs" "GVFS archive backend" >}} to mount
    it with fuse.
    -   [archivemount Home](http://www.cybernoia.de/software/archivemount/)
    -   [Tutorial: Mounting archives with FUSE and archivemount
        ](http://archive09.linux.com/articles/132196)
-   [AVFS - A Virtual File System](http://avf.sourceforge.net/) (GPL)
    (GPL) alow to look into archives.
    it supports floppies, tar and gzip files, zip, bzip2, ar and rar
    files, ftp sessions, http, webdav, rsh/rcp, ssh/scp.
    It can be used on its own or as a fuse filesystem.
    It is an old project but still maintained,
    which is available in Debian packages.<br />
    _avfs_ is used by midnight commander (mc) for opening archives.
    -   [sourceforge AVF project page
        ](http://sourceforge.net/projects/avf).
    -   [AVFS git repository
        ](http://sourceforge.net/p/avf/git/ci/master/tree/)
    -   [AVFS README
        ](http://sourceforge.net/p/avf/git/ci/master/tree/README)
-   [bindfs](http://bindfs.org/) (GPL)
    is a FUSE filesystem for mounting a directory to another location,
    similarly to `mount --bind` but the owner and permissions inside
    the mountpoint can be altered.  *bindfs* is packaged in Debian.
-   [CurlFtpFs](http://curlftpfs.sourceforge.net/) (GPL)
    there exist other fuse filesystem quicker and better maintained
    than _CurlFtpFS_, nevertheless it is still useful for ftp. It is
    in Debian.
    -   [ArchWiki: CurlFtpFS
        ](https://wiki.archlinux.org/index.php/CurlFtpFS)
    -   {{< man "+curlftpfs(1)" >}} gives mount options.
-   {{< wp "Davfs2" >}} is a fuse module for dav file system including https
    encrypted connection.
-   [fuseiso](http://sourceforge.net/projects/fuseiso/)
    mount optical disk image formats as .iso, .nrg, .bin, .mdf and
    .img. It supports plain ISO9660 Level 1 and 2, Rock Ridge, Joliet,
    and zisofs.  Debian provide a package _fuseiso_ and also a package
    _fuseiso9660_ to mount ISO9660 file systems.
    -   [ArchWiki: fuseiso](https://wiki.archlinux.org/index.php/Fuseiso).
-   [fusedav](http://0pointer.de/lennart/projects/fusedav/)
    transparently edit and manage files from a WebDAV share on a remote server.
-   [Dave's IMAP Gmailfs](http://sr71.net/projects/gmailfs/)
    replaces the unmaintened
    [gmailfs
    ](http://richard.jones.name/google-hacks/gmail-filesystem/gmail-filesystem.html)
-   [jmtpfs](https://github.com/kiorky/jmtpfs) mount a
    [w:Media Transfer Protocol) (MTP) it uses libmtp, and is in debian.
-   [ntfs-3g
    ](http://www.tuxera.com/community/ntfs-3g-advanced/http://linux-ntfs.org/)
    is a FUSE module to mount NTFS filesystems.
-   [pytagfs](http://sourceforge.net/projects/py-tag-fs/)
    arranges media files in a virtual directory structure based
    on the file tags.
    -   [pytagfs on GitHub](https://github.com/dizel-by/pytagfs) _main
        or fork?_
    -   [sshfs](http://fuse.sourceforge.net/sshfs.html)<a name="sshfs">
        is the _fuse_ access to ssh file systems.
     -   [Ubuntu: sshfs](https://help.ubuntu.com/community/SSHFS)
       explains the usage, including mounting from fstab.
     -   [ArchWiki: sshfs](https://wiki.archlinux.org/index.php/Sshfs)
     -   [Gentoo Wiki: SSHFS](https://wiki.gentoo.org/wiki/SSHFS)
-   [tagfs](https://github.com/marook/tagfs/wiki) _≠ Tagsistant_.
    is used to organize your documents using tags.
-   [Tagasistant](http://www.tagsistant.net/) _previously tagfs_
    turns directories into tags and lets you search your files by
    tags.
    -   [Tagsistant documentation
        ](http://www.tagsistant.net/documents-about-tagsistant/)
-   [Yacufs](https://www.uitwisselplatform.nl/projects/yacufs)
    can access your music library containing .ogg, .flac and .mp3 files.


# Gvfs {#gvfs}

{{< wp "Gvfs" >}} is a userspace virtual filesystem where mount runs as a
separate processes which you talk to via D-Bus. It also contains a gio
module that seamlessly adds gvfs support to all applications using the
gio API. It also supports exposing the gvfs mounts to non-gio
applications using fuse.
The gvfs section is now in my
[unix-memo](http://unix-memo.readthedocs.org/vfs).

# Media Transport Protocol (MTP)

-   [ArchWiki: MTP](https://wiki.archlinux.org/index.php/MTP)

#  Kernel filesystems {#kernel_fs}
## Procfs {#procfs}

-   [Procfs](http://en.wikipedia.org/wiki/Procfs) is a pseudo file
    system used to access process information from the kernel. Linux
    2.6 kernel moved many of the non-process-related files to sysfs .
-   [The Proc filesystem
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html-single/Reference_Guide/#ch-proc)
    , [Top-level Files in the proc File System
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html-single/Reference_Guide/#s1-proc-topfiles)
    from [Red Hat Linux Reference Guide
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/4/html-single/Reference_Guide/)
-   [The /proc filesystem documentation](http://www.linuxinsight.com/proc_filesystem.html) is
    the main entry point to get a description of the entries of the
    proc filesystem.
-   You find it also in the [Fedora 17 System Administrator's Guide
    ](https://docs.fedoraproject.org/en-US/Fedora/17/html/System_Administrators_Guide/index.html)
    in html but also available in epub or pdf
    as
    [The /proc filesystem documentation
    ](https://docs.fedoraproject.org/en-US/Fedora/17/html/System_Administrators_Guide/ch-proc.html)
-   The man page {{< man "proc(5)" >}}
    and {{< man "procinfo(8)" >}}

### proc/sys {#sysctl}

A very interesting part of /proc is
[directory /proc/sys](http://www.linuxinsight.com/proc_sys_hierarchy.html)
that allows you to see and to change parameters within the kernel.
It is also partially documented in the
[kernel syctl documentation
](http://www.kernel.org/doc/Documentation/sysctl/).<br />

You find it also in the previous redhat or fedora guides as
[ /proc/sys/ section
](https://docs.fedoraproject.org/en-US/Fedora/17/html/System_Administrators_Guide/s2-proc-dir-sys.html)

You can use it directly as a
pseudo file system or thru the {{< man "sysctl(8)" >}} utility
and {{< man "sysctl.conf(5)" >}} .

-   [ArchWiki: Sysctl](https://wiki.archlinux.org/index.php/Sysctl)
-   `/proc/sys/net/ipv4` is for the network configuration it is documented in
    [ip-sysctl.txt](https://www.kernel.org/doc/Documentation/networking/ip-sysctl.txt)
-   [sysctl/vm.txt](https://www.kernel.org/doc/Documentation/sysctl/vm.txt)
    /proc/sys/vm is used to tune the operation of the virtual memory (VM) subsystem of
    the Linux kernel and the writeout of dirty data to disk.

## Sysfs {#sysfs}

-   [Sysfs](http://en.wikipedia.org/wiki/Sysfs)
    exports information about devices and drivers from the kernel to
    userspace.
-   a comprehensive presentation of sysfs is in
    [kernel documentation: sysfs.txt
    ](http://kernel.org/doc/Documentation/filesystems/sysfs.txt)
    found also in
    [The sysfs Filesystem (pdf)
    ](http://www.kernel.org/pub/linux/kernel/people/mochel/doc/papers/ols-2005/mochel.pdf)
    by Patrick Mochel.
-   [kernel documentation:
    rules on how to access information in the Linux kernel sysfs
    ](http://www.kernel.org/doc/Documentation/sysfs-rules.txt).
-   [kernel documentation:
    Accessing PCI device resources through sysfs
    ](https://www.kernel.org/doc/Documentation/filesystems/sysfs-pci.txt)
-   {{< man "lspci(8)" >}} uses the `/proc/bus/pci/devices` and the
    `/sys/bus/pci` key as explained in
    [Debian Wiki: HowToIdentifyADevice/PCI](http://wiki.debian.org/HowToIdentifyADevice/PCI).<br />
    Look also to {{< man "update-pciids(8)" >}} to maintain the dtabase of pci id
    `/usr/share/misc/pci.id` that you can also find at
    [The PCI ID Repository - public repository of all known ID's used in PCI devices
    ](http://pci-ids.ucw.cz/).
-   hwmon in lm-sensors > 3.0.0 has an interface  in sysfs described in
    [Kernel file /hwmon/sysfs-interface -
    Naming and data format standards for sysfs files
    ](https://www.kernel.org/doc/Documentation/hwmon/sysfs-interface)

## Tmpfs {#tmpfs}
{{< wp "tmpfs" >}} is a file system which keeps all files in virtual
memory. It uses {{< wp "swap space" >}} as backing store in case of low
memory situations.

-   [tmpfs - ArchWiki](https://wiki.archlinux.org/index.php/Tmpfs)
-   [tmpfs - Gentoo Wiki](https://wiki.gentoo.org/wiki/Tmpfs)

{{< man "systemd-tempfile(8)" >}} is a service that creates, deletes, and cleans up volatile and
temporary files and directories, based on the configuration file format and location
specified in [:man:tmpfiles.d(5)].

-   [systemd temporary files - ArchWiki
    ](https://wiki.archlinux.org/index.php/Systemd#Temporary_files).


tmpfs has three mount options for sizing:

size
:   The limit of allocated bytes. The default is half of your the RAM.
    can be given with unit __b__ _(byte)_, __k__ _(kilo)_, __m__ or __g__
nr\_blocks
:   The same as size, but in blocks of PAGE\_CACHE\_SIZE.
nr\_inodes
:   The maximum number of inodes. The default  is half  the number of  RAM pages.

The uses of _tmpfs_ differ from one distribution to an other, and in
the same distribution change from one release to an other.

_tmpfs_ is used for `/dev/shm` (or `/run/shm` in debian > 7.0
 (wheezy)), `/sys/fs/cgroup`, `/run` and some subdirs of `/run` like `/run/lock`
the directory `/run/user/`_<uid>_ wich belong to each _<uid>_ of an
active user.

_tmpfs_ may also be used for `/tmp`, archlinux do so, but in 2015
debian 8.0 seem to stick by default to keep /tmp on persistent memory, but
you can adopt it if you want.

You may configure _tmpfs_ in `/etc/default/tmpfs` in Debian.

The creation of tmpfiles by systemd is controled by
{{< man "tmpfiles.d(5)" >}} see also {{< man "systemd-tmpfiles(8)" >}}

-   [Debian: What's new in Debian 7.0 - Temporary filesystems
    ](https://www.debian.org/releases/wheezy/amd64/release-notes/ch-whats-new.en.html#tmpfs-filesystems)
    explains the location and settings in Debian.
-   [ArchWiki: Tmpfs](https://wiki.archlinux.org/index.php/Tmpfs)

## Other kernel fs

-   {{< wp "debugfs" >}}  make debug information available to user space.
    -   [Kernel documentation: debugfs.txt
        ](https://www.kernel.org/doc/Documentation/filesystems/debugfs.txt)
-   _devtmpfs_ is like _tmpfs_ but every device with a major/minor
    will provide a device node in devtmpfs.
    -   Wikipedia {{< wp "device" >}} explain the device support in the kernel
        evolution.
    -   [kernel commit creating devtmpfs
        ](http://git.kernel.org/cgit/linux/kernel/git/torvalds/linux.git/commit/?id=2b2af54a5bb6f7e80ccf78f20084b93c398c3a8b).
-   _devpts_ the `/dev/pts/*` entries are not created only in
    _devtmpfs_ but in a _devpts_ filesystem.
    -   [Kernel documentation: devpts
        ](https://www.kernel.org/doc/Documentation/filesystems/devpts.txt).
-   [ramfs](https://wiki.debian.org/ramfs) is a dynamically resizable
    ram-based filesystem, the two main uses of ramfs is the above
    {{< iref "#tmpfs" "tmpfs" >}} that in contrast to original
    ramfs is able to write to swap space and
    [initramfs](https://wiki.debian.org/initramfs) that contain a
    gzipped cpio archive attached to the kernel image.
-   [kernel documentation: ramfs, rootfs and initramfs
    ](

# Loop device

-   Wikipedia: {{< wp "Loop device" >}}
-   Loppdevice can be used to store a {{< wp "Disk image" >}}
-   Manpages: {{< man "losetup(8)" >}}


## Loop device memo
a loop device is a good way to use some part of a dumb file system
(as msdos, vfat .. ) as extfs2/3. I proceed as follow:

-   define the file to hold the loop device by

        # dd if=/dev/zero of=/path/of/myfile bs=4k count=1000000

    to define an empty 4giga file to hold the loop device
-   create the device:

        # losetup /dev/loop0  /path/of/myfile

-   format the loop device:

        # mkfs.ext2 /dev/loop0

-   mount the device

        # mount -t ext2 /dev/loop0 /mnt/loop0

-   Further mount can be done in only one command without invoking
    explicitly losetup by:

        # mount /path/of/myfile -t ext2 -o loop /mnt/loop0

-   To break the link of loop device to the pseudo file system:

        # umount /path/of/myfile
        # loosetup -d /mnt/loop0

-   One can use cryptography with

        # losetup -e aes /dev/loop0 /path/of/myfile

    where aes can be replaced by aes{128,192,256}
    {twofish,blowfish}{128,160,192,256}
    {serpent,mars,rc6-}{128,192,256} or tripleDES depending of
    encryptions available in the kernel or loaded as module. The loop
    device is formatted as usual and mounted as

        # mount /path/of/myfile -t ext2 -o loop,encryption=aes /mnt/loop0


# Stackable file systems

Stackable file systems implement {{< wp "union mount" >}}. They combine two file systems
in an unique virtual fs. The more usual policy stack file systems such the upper one
hide the lower one when there is a conflict. These file system require a special policy
for some standard file operations: when deleting a stacked entry, deleting the upper one
makes the lower one reappear; renaming a file or a directory should be an atomic
operation but it need here multiple rename of the underlying files entries, so it is
replaced by a slower copy and delete, lower level operation which involve inodes are
also difficult to implement.


Many of these filesystems implement {{< wp "Copy-on-write" >}}, allowing to mount a
writable filesystem upon a read-only one like a live CD, giving the illusion it can be
modified. This mechanism is also used by Docker

Wikipedia «The main mechanics of OverlayFS relate to the merging of directory access
when both filesystems present a directory for the same name. Otherwise, OverlayFS
presents the object, if any, yielded by one or the other, with the "upper" filesystem
taking precedence.»


## UnionFs
The older implementation was [Unionfs](http://en.wikipedia.org/wiki/Unionfs)
builds a stackable unification file system, which can appear to
merge the contents of several directories (branches), while keeping
their physical content separate. UnionFs implement
[Copy on Write](http://en.wikipedia.org/wiki/Copy-on-write)
also known by the acronym **COW**. The
[unionfs project page](http://www.filesystems.org/project-unionfs.html)
is an old page unmaintained since unionfs is merged in the kernel
[Unionfs: Bringing Filesystems Together](http://www.linuxjournal.com/article/7714)
by Charles P. Wright and Erez Zadok is an _old 2004_  presentation of the use of
UnionFs.

[unionfs-fuse](https://github.com/rpodgorny/unionfs-fuse) is an
implementation of unionfs in user space. It is available in Debian.

## AUFS


[aufs](http://aufs.sourceforge.net) is an
alternative union file system implementation. _Aufs5_ is used with kernel 5.x while
_aufs4_ is used with kernel 4.x, _aufs3_ is used with kernel 3.8, and _aufs2_ with
kernel > 2.6.16.

_Aufs_ is used by [Linux Live](http://www.linux-live.org/) which is a set of shell
scripts which allows you to create own Live Linux from your installed Linux
distribution.

Debian provides the packages _aufs-dkms_ and _aufs-tools_.
[Gentoo kernels can be compiled with aufs
](https://wiki.gentoo.org/wiki/Aufs).

The basic use of aufs is

    # mount -t aufs -o br=/tmp/rw=rw:${HOME}=ro none /tmp/aufs

you can see whole tree of your home dir through /tmp/aufs. If
you modify a file under /tmp/aufs, the one on your home directory is
not affected, instead the same named file will be newly created under
/tmp/rw. And all of your modification to a file will be applied to
the one under /tmp/rw.<br />
The man page  is
[aufs(5)](http://aufs.sourceforge.net/aufs2/man.html);
it is the reference for all _aufs-utils_ _(Debian package:
aufs-tools)_ i.e. `mount.aufs`, `umount.aufs`, `auplink` _(make
pseudo links permanent)_, `auchk` _(aufs fsck tool)_, `aubrsync`
_(synchronize files between two aufs branches)_.

A slightly longer example that stack three file systems a
read_only and two read-write is:

    # cd /tmp
    # mkdir ro rw1 rw2
    # for f in ro rw1 rw2; do echo "content of $f" > $f/file_$f; done
    # mount -t aufs -o br=/tmp/rw1=rw:/tmp/rw2=rw:/tmp/ro=ro none /tmp/aufs
    # for f in ro rw1 rw2 new; do echo "appended in file_$f">> /tmp/aufs/file_$f; done
    # cat /tmp/ro/file_ro
    content of file_ro
    # cat /tmp/aufs/file_ro
    content of file_ro
    appended in file_ro
    # cat /tmp/rw2/file_ro
    cat: /tmp/rw2/file_ro: No such file or directory
    # cat /tmp/rw1/file_ro
    content of file_ro
    appended in file_ro
    # ls /tmp/{rw1,rw2,ro,aufs}/file_new
    ls: cannot access /tmp/rw2/file_new: No such file or directory
    ls: cannot access /tmp/ro/file_new: No such file or directory
    /tmp/aufs/file_new  /tmp/rw1/file_new

The default policy of create and copy up for aufs is _top-down-parent_ which means that
aufs selects the highest writable branch where the parent dir exists.
If the parent dir does not exist on a writable branch, then  the
internal  copyup  will  happen.  The  policy  for this copyup is
always _bottom-up_.

We can find more examples in the
[aufs-utils sample directory
](http://git.c3sl.ufpr.br/gitweb?p=aufs/aufs2-util.git;a=tree;f=sample)

[Docker can use aufs as storage driver
](https://docs.docker.com/storage/storagedriver/aufs-driver/)

## OverlayFS

{{< wp "OverlayFS" >}} is a fork and improvement of UnionFS, since kernel version 3.18
it is the standard stackable file system in Linux, obsoleting UnionFS, and gradually
replacing aufs.

OverlayFS supports whiteouts files and opaque directories in the upper filesystem to
allow deletion in the lower read-only filesystem. For modification of files in a
readonly lower layer, upadating occur on a copy created in the upper layer.

OverlayFS is [implemented in the kernel since version 3.18
](https://github.com/torvalds/linux/commit/e9be9d5e76e34872f0c37d72e25bc27fe9e2c54c)
in a module named _overlay_, and since kernel 4 _overlay2_.

You can mount overlayfs with:

    mount -t overlayfs overlayfs -olowerdir=/lower,upperdir=/upper/upper,workdir=/upper/work /overlay

You can find examples of use in the answers to [How do I use OverlayFS?
}(https://askubuntu.com/questions/109413/how-do-i-use-overlayfs).
and in [OverlayFS | Programster's Blog](https://blog.programster.org/overlayfs).


The more extensive documentation on overlayfs is the [kernel overlayfs documentation
](https://www.kernel.org/doc/Documentation/filesystems/overlayfs.txt)

There is an HowTo in [Overlay filesystem - ArchWiki
](https://wiki.archlinux.org/index.php/Overlay_filesystem).

[fuse-overlayfs](https://github.com/containers/fuse-overlayfs) is a Fuse implementation
of overlayfs+shiftfs for rootless containers. _Shiftfs is a virtual filesystem for
mapping mountpoints across user namespaces._

[Docker can use OverlayFS
](https://docs.docker.com/storage/storagedriver/overlayfs-driver/) and this is the
prefered Driver on recent Linux ( kernel > 4.0 to have the _overlay2_ driver.)


## btrfs and thinly provisionned lvm

Btrfs and thinly provisionned lvm, are not stackable filesystems, but snapshotting allow
to use a pseudo file system stack.

On btrfs when you create a snapshot of a subvolume, you use only metadata, the file data
itself is shared between the source subvolume and the snapshots. With copy-on-write when
you modify the snapshot only the modified data is duplicated, and your source subvolume
stay untouched.

Docker can [use btrfs](https://docs.docker.com/storage/storagedriver/btrfs-driver/) or
[device mapper with thinly provisionned pool
](https://docs.docker.com/storage/storagedriver/device-mapper-driver/) as device driver.

## MergerFS

[MergerFS](https://github.com/trapexit/mergerfs) is a FUSE union filesystem.

In contrast to aufs and overlayfs, it does not support Copey-On-Write, so you can not
use it to make a read only file sytem appear writable; so it is not truly _stackable_.

Look at the [FAQ](https://github.com/trapexit/mergerfs#faq) for comparison with other
unionfs tools.

There are exemple of use in the
[Backup and recovery howtos](https://github.com/trapexit/backup-and-recovery-howtos)
from the _mergefs_ author _trapexit_.

## Bilibop
[Bilibop](https://un.poivron.org/~quidame/wiki/bilibop/)
helps to maintain an OS installed on an external media (USB, FireWire, Flash memory, eSATA)

When the lockfs feature is enabled filesystems in /etc/fstab are set read-only except
for those that have been whitelisted, or for the encrypted swap devices.

_Bibilop_ is packaged in Debian.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
