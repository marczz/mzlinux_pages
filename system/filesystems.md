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
    {{< wp "Comparison of file systems" >}}, {{< wp "Fat" >}}, {{< wp "ext2" >}},
    {{< wp "ext3" >}}, {{< wp "ext4" >}}, {{< wp "XFS" >}}, {{< wp "Reiser4" >}},
    {{< wp "ZFS" >}}, {{< wp "Btrfs" >}}, {{< wp "NTFS" >}},
    {{< wp "Network File System" >}}, {{< wp "Andrew file system" >}},
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
-  {{< wp "Stratis (configuration daemon)" >}} is a rust userland daemon provides ZFS/Btrfs-style features by
   integrating LVM and XFS. RedHat deprecated Btrfs in favor of Stratis.

## Btrfs
{{< wp "Btrfs" >}} (GPL) is a copy-on-write file system which is an improvement of
ext3/ext4 file system. It offers numerous {{< wp "Btrfs#Features" "new features" >}}
including copy-on-write snapshots of files and subvolumes, checksums, transparent
compresssion.

-   [BTRFS documentation](https://btrfs.readthedocs.io/en/latest/)
-   [Kernel Brtfs Wiki](https://btrfs.wiki.kernel.org)
    reference  on the Home page
    -   [list of Guides and articles
        ](https://btrfs.wiki.kernel.org/index.php/Main_Page#Guides_and_usage_information)
    -   [Btrfs FAQ](https://btrfs.wiki.kernel.org/index.php/FAQ).
    -   [SysadminGuide - btrfs Wiki
        ](https://btrfs.wiki.kernel.org/index.php/SysadminGuide)
-   [Manual pages — BTRFS documentation](https://btrfs.readthedocs.io/en/latest/man-index.html)
-   [Suse storage administration: Btrfs filesystem
    ](https://documentation.suse.com/sles/15-SP3/html/SLES-all/cha-filesystems.html#sec-filesystems-major-btrfs)
    -   [Troubleshouting filesystems
        ](https://documentation.suse.com/sles/15-SP3/html/SLES-all/cha-filesystems.html#sec-filesystems-trouble)
    -   [OpenSuse Support Data Base: BTRFS](https://en.opensuse.org/SDB:BTRFS)
        covers important diagnostic and repair steps for btrfs.
-   [Oracle Linux -  The Btrfs File System
    ](https://docs.oracle.com/cd/E37670_01/E37355/html/ol_btrfs.html)
-   [Debian Wiki: Btrfs](https://wiki.debian.org/Btrfs)
-   [ArchWiki: Btrfs](https://wiki.archlinux.org/index.php/Btrfs),
    [Btrfs - Tips and tricks
    ](https://wiki.archlinux.org/index.php/Btrfs_-_Tips_and_tricks),
-   [GentooWiki: Btrfs](https://wiki.gentoo.org/wiki/Btrfs),
    [Btrfs/System Root Guide - Gentoo Wiki
    ](https://wiki.gentoo.org/wiki/Btrfs/System_Root_Guide)
-   [Ubuntu Community Help: Btrfs
    ](https://help.ubuntu.com/community/btrfs).
-   [Btrfs Maintenance](https://github.com/kdave/btrfsmaintenance/blob/master/)
    (GPL-2.0)
    a set of scripts to automate scrub, balance, trim or defragmentation.
-   Marc Merlin [Btrfs overview, LinuxCon 2014
    ](http://marc.merlins.org/linux/talks/Btrfs-LC2014-JP/Btrfs.pdf)
    _(pdf)_
    and [Linux Btrfs posts](http://marc.merlins.org/perso/btrfs/)
-   [Btrfs: Subvolumes and snapshots [LWN.net]](https://lwn.net/Articles/579009/)
    explains quotas.
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

### Btrfs backup

We use {{< man "btrfs-send" >}} and {{< man "btrfs-receive" >}} for transferring
snapshots.

This is described in
[Incremental Backup - btrfs Wiki](https://btrfs.wiki.kernel.org/index.php/Incremental_Backup)

The wiki gives also few of the scripts created to implement an incremental backup.
The most used tool is {{< iref "#snapper" "Snapper" >}} you find in next section.

-   [btrbk](https://digint.ch/btrbk/) (GPL-3.0)
    is a single perl script, which allows creation of backups from multiple sources to
    multiple destinations at once, with ssh and configurable retention support
    (daily/weekly/monthly). _brtbk_ is packaged in Debian.
    -   [btrbk - README](https://digint.ch/btrbk/doc/readme.html)
    -   [btrbk - GitHub](https://github.com/digint/btrbk)
-   [btrfs-backup](https://github.com/bob1de/btrfs-backup) (MIT License)
    incremental atomic backups for btrfs using snapshots with local and/or remote storage.
    written in python.
-   [GitHub - nachoparker/btrfs-snp](https://github.com/nachoparker/btrfs-snp) and
    [GitHub - nachoparker/btrfs-sync](https://github.com/nachoparker/btrfs-sync)
    Automatic BTRFS snapshots and sync of BTRFS snapshots, locally or through SSH
    written in bash _active, but few commits_.
    -   [Easy sync BTRFS snapshots with btrfs-sync
        ](https://ownyourbits.com/2018/03/09/easy-sync-of-btrfs-snapshots-with-btrfs-sync/)
        by nachoparker.
    -   [Schedule BTRFS snapshots with btrfs-snp
        ](https://ownyourbits.com/2017/12/27/schedule-btrfs-snapshots-with-btrfs-snp/)
        by nachoparker.
-   [btrfs-sxbackup](https://github.com/masc3d/btrfs-sxbackup) (GPL-2.0)
    a python Btrfs snapshot backup utility with push/pull support via ssh, retention,
    email notifications, compression of transferred data, syslog logging.
-   [buttersink](https://github.com/AmesCornish/buttersink) (GPL-3.0)
    a python script to synchronize btrfs snapshots like rsync. last activity 2018.

     Sources and destinations can be local btrfs file systems, remote btrfs file systems
     over SSH, or S3 buckets.
-   [snapbtrex](https://github.com/yoshtec/snapbtrex) (BSD-2-Clause License)
    a python script which is an extended version of
    [SnapBtr](https://btrfs.wiki.kernel.org/index.php/SnapBtr)
    capable of transferring snapshots to remote systems.
-   [snap-sync ](https://github.com/wesbarnett/snap-sync) (GPL-2.0)
    a script to backup snapper snapshots to external drive;
    -   [Backup Snapper Snapshots With snap-sync - JWillikers
        ](https://www.jwillikers.com/backup-snapper-snapshots-with-snap-sync).
    -   [rzerres/dsnap-sync](https://github.com/rzerres/dsnap-sync)
        is a fork of wesbarnett/snap-sync.
-   [baksnapper](https://github.com/plattfot/baksnapper) (GPL-3.0)
    a bash script for backing up snapper snapshots on a drive or through ssh on a remote
    server, using btrfs send and receive.
-   [UrBackup - Client/Server](https://www.urbackup.org/)
    save backups as btrfs sub-volumes. Incremental backups are created using btrfs
    snapshots. Blocks which are not changed in files in incremental backups are stored
    only once using cross-device reflinks. This is also explained in the
    [UrBackup Developer Blog](https://blog.urbackup.org/) where you find
    [File Backup Storage with Btrfs Snapshots
    ](https://blog.urbackup.org/83/file-backup-storage-with-btrfs-snapshots).

    Urbackup propose binaries for windows and packages for main Linux distribution
    including [Debian](https://www.urbackup.org/download.html#server_debian).

Tutorials on how to make backup using btrfs send/receive:

-   [Marc's Blog: Doing Fast Incremental Backups With Btrfs Send and Receive
    ](http://marc.merlins.org/perso/btrfs/post_2014-03-22_Btrfs-Tips_-Doing-Fast-Incremental-Backups-With-Btrfs-Send-and-Receive.html)
    _2014_.
-   [NAS Backups, Part 2: Btrfs send / receive
    ](https://starbeamrainbowlabs.com/blog/article.php?article=posts%2F472-nas-backups-part-2-btrfs-send-recieve.html)

## Snapper {#snapper}
[Snapper](https://en.opensuse.org/Portal:Snapper) (GPL-2.0)
is the most popular btrfs backup tool.
-   [Snapper - Github](https://github.com/openSUSE/snapper) (GPL-2.0).
-   [Snapper documentation](http://snapper.io/documentation.html),
    [Snapper FAQ](http://snapper.io/faq.html)
-   [Snapper Tutorial](http://snapper.io/tutorial.html)
-   [Manpage: snapper](http://snapper.io/manpages/snapper.html)
-   [Portal:Snapper - openSUSE](https://en.opensuse.org/Portal:Snapper):gives all
    snapper related documents. It includes a tutorial, FAQ, System Recovery and Snapshot
    Management with Snapper, and the manpages.
-   [Snapper - ArchWiki](https://wiki.archlinux.org/index.php/Snapper)
-   RedHat no longer use snapper since redhat 8.

## Btrfs deduplication {#btrfs_dedupe}
Block deduplication ib btrfs is done when we use the `cp --reflink` command when doing a
snapshot. Some program may inspect files to find common block between them and
deduplicate them.

The currnt known program are listed in
[Deduplication - btrfs Wiki](https://btrfs.wiki.kernel.org/index.php/Deduplication).

Some file deduplication programs listed in the
{{< iref "#dedupe" "section below" >}} have support for btrfs, this include
{{< iref "#jdupes" "jdupes" >}} and {{< iref "#rmlint" "rmlint" >}}.


-   [Bees](https://github.com/Zygo/bees) (GPL-3.0)
    bees is a block-oriented userspace deduplication daemon agent designed for large
    btrfs filesystems. It is an offline dedupe combined with an incremental data scan
    capability .
-   [dduper](https://github.com/lakshmipathi/dduper) (GPL-2.0)
    dduper is a block-level out-of-band BTRFS dedupe tool. This works by fetching
    built-in checksum from BTRFS csum-tree, instead of reading file blocks and computing
    checksum itself. This hugely improves the performance.

    To use dduper you need to patch `btrfs-progs` with a patch included in the
    repository.
-   <a name="duperemove"></a>
    [Duperemove](http://markfasheh.github.io/duperemove/) (GPL-2.0)
    finds duplicated extents and submits them to the kernel for deduplication.
    When given a list of files it will hash their contents on a block by block basis and
    compare those hashes to each other, finding and categorizing blocks that match each
    other. When given the -d option, duperemove will submit those extents for deduplication using the Linux kernel extent-same ioctl.

    Duperemove can store the hashes it computes in a 'hashfile', then it will only
    compute hashes for those files which have changed since the last run.

    _duperemove_ is in Debian.

    -   [duperemove - Github](https://github.com/markfasheh/duperemove)
    -   [duperemove(8)](http://markfasheh.github.io/duperemove/duperemove.html)
    -   [duperemove Wiki · GitHub](https://github.com/markfasheh/duperemove/wiki)


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

# Filesystem Deduplication {#dedup}

See {{< iref "#btrfs_dedupe" "above" >}} for btrfs block deduplication.

-   Wikipedia: {{< wp "List of duplicate file finders" >}}

There are a lot of benchmarking, each software shows it is quicker than the previous
ones, we cn also take care that often these benchmarking are flawed by different way of
comparing files, either only hashsum, and here the hash algorithm mater, or hashsum and
byte to byte comparison when the hash is the same.

The functionalities differ also greatly, and are important if you want more than a list
of duplicate files, program like {{< iref "#czkwaka" "czkwaka" >}},
{{< iref "#fslint" "fslint"  >}}, {{< iref "#rmlint" "rmlint" >}} can detect a lot of
other anomalies on your filesystem like  non-stripped binaries. broken symlinks, empty
files or directories, broken user or group ID.

To summarize benchmarks on the quicker side we find _fclone_, _yadf_ (on ssd only),
_ffdf_, _rdfind_ (on hdd only).

Medium speed: _czkawka_, _rmlint_

Slower: _jdupes_, _rdupes_, _ddf_, _fdupes (C)_ _yadf_ (on hdd), _rdfind_ (on sdd)

Very slow: _fdudes-java_, _duff_, _fslint_,

I don't include in my list the basic rust duplicate finders, that have no active
development like [yadf](https://github.com/jRimbault/yadf),
[fddf](https://github.com/birkenfeld/fddf), for these type of quick basic duplicate
finders _fclone_ may be preferred.


-   <a name="czkwaka"></a>[czkawka](https://qarmin.github.io/czkawka/) (MIT license)
    is a rewrite of _fslint_ in rust. It has a GTK3 GUI and a command line
    interface.
 -  [Duff](https://github.com/elmindreda/duff)
    is a C command-line utility for quickly finding duplicates in a given set of
    files. It is no longer developed.
-   [fclones](https://github.com/pkolaczk/fclones) (MIT License) is a rust command line
    duplicate file finder and remover.  the benchmark shows it as a lot faster than
    _czkawka_, _rmlint_, _jdupes_, _fdupes_, rdfind_.
-   <a name="fslint"></a>[fslint](http://www.pixelbeat.org/fslint/)
    a python app which finds duplicate files, problematic filenames, temporary files,
    bad symlinks, empty directories. It includes a GTK+ GUI as well as a command line
    interface. _It is in Debian._
-   [fdupes](https://github.com/adrianlopezroche/fdupes) c-program
    (there is also a perl alias!) that uses md5sums and then a byte by byte comparison to
    find duplicate, it is in Debian. See also the {{<iref "#jdupes" "jdupes" >}} fork
    below. There is also a java fork
    [fdupes-java](https://github.com/cbismuth/fdupes-java), no more developed since
    2017, slower than the C version.
-   <a name="jdupes"></a>[jdupes](https://github.com/jbruchon/jdupes)
    is a fork of {{< iref "#fdupes" "fdupes" >}}.  It is not binary compatible with
    _fdupes_, it enhanced the search speed, and is seven time quicker. It include btrfs
    block-level deduplication. _jdupes_ is packaged in Debian.
-   [rdfind](https://github.com/pauldreik/rdfind) (GPL)
    is a program that finds duplicate files. The benchmark on the rdfind page, show that
    it is a lot quicker than _fdupes_ and _fslint_, but it is slower than _rmlint_.
    _rdfind_ supports btrfs filesystems. It is in debian.
-   <a name="rmlint"></a>[rmlint](https://github.com/sahib/rmlint)
    finds duplicate files & directories, nonstripped binaries, broken symlinks, empty
    files, recursive empty directories, files with broken user or group id.
    _It is packaged in Debian._

    _rmlint_ has an option `rmlint --dedupe` to deduplicate blocks on btrfs filesystems.
    you use it by first looking at duplicates with
    ``` sh
    rmlint --types="duplicates" --config=sh:handler=clone [paths...]
    ```
    the handler _clone_  free up duplicate extents, using
    {{< man "ioctl_fideduperange" >}} it is usable even with a read only
    btrfs filesystem.  if reflinking read-only snapshots, `rmlint.sh` must be run with
    -r option and with root privileges.

    According to this [post](https://unix.stackexchange.com/a/428253)
    > The handler _reflink_ creates reflinks to the original for identical files.
    > Reflink deletes the duplicate file and creates a new file in its place which
    > is a clone of the original file. The metadata of the duplicate is lost,
    > although rmlint does its best to preserve the metadata via some trickery with touch -mr.
    >
    > Clone uses the BTRFS_IOC_FILE_EXTENT_SAME ioctl (or, in the latest version,
    > the FIDEDUPERANGE ioctl) which asks the kernel to check if the files are
    > identical, if so then make them share the same data extents. They keep their
    > original metadata. It's arguably safer than reflink because it's done atomically
    > by the kernel, and because it checks that the files are still identical.

    It has [Benchmarks
    ](https://rmlint.readthedocs.io/en/latest/benchmarks.html?highlight=fast#benchmarks)
    showing it is quicker than fdupes, rdfind, dupd ... but no comparison with _jdupes_.

    -   [rmlint tutorial](https://github.com/sahib/rmlint/blob/master/docs/tutorial.rst).
    -   [rmlint documentation](https://rmlint.readthedocs.io/en/latest/)

    The [btrfs Wiki](https://btrfs.wiki.kernel.org/index.php/Deduplication)
    gives an example of deduplicating with _rmlinT_:
    ``` sh
    $ rmlint --types="duplicates" --config=sh:handler=clone [paths...]
    $ ./rmlint.sh
    ```
    `rmlint.sh` must be done as root if reflinking read-only snapshots.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
