---
title: Hard Drive
---


See also {{< iref "filesystems" "File Systems" >}}.


# References
-   Wikipedia: {{< wp "Hard_disk_drive" >}}, {{< wp "Solid-state drive" >}},
    {{< wp "Automatic acoustic management" >}}, {{< wp "S.M.A.R.T." >}},
    {{< wp "GNOME Disks" >}} _debian package: gnome-disk-utility_, {{< wp "RAID" >}}
-   [Red Hat Storage Administration Guide
    ](https://access.redhat.com/site/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Storage_Administration_Guide/index.html)
-   [Red Hat LVM Administrator Guide
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Logical_Volume_Manager_Administration/index.html)
-   [Red Hat DM Multipath Configuration and Administration
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/DM_Multipath/index.html)
    the utilities in Debian are in the package _multipath-tools_.
-   [Red Hat - Managing storage devices
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_storage_devices/index)
-   [Red Hat - Online Storage Reconfiguration Guide
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/online_storage_reconfiguration_guide/index)
    : [1.4. Removing a Storage Device
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/5/html/online_storage_reconfiguration_guide/removing_devices).
-   [Fedora - Storage Administration Guide
    ](https://docs.fedoraproject.org/en-US/Fedora/14/html/Storage_Administration_Guide/index.html)
-   [ArchWiki - Filesystems
    ](https://wiki.archlinux.org/index.php/File_systems).
-   [linux-advanced-storage (pdf)
    ](https://oss.oracle.com/~mkp/docs/linux-advanced-storage.pdf)
    describes the low level disk driver access via ATA and SCSI commands.
-   [Blackblaze: What is the Best Hard Drive?
    ](https://www.backblaze.com/blog/best-hard-drive/),
    [Hard Drive Reliability update
    ](https://www.backblaze.com/blog/hard-drive-reliability-update-september-2014/),
    [How long do disk drives last?
    ](https://www.backblaze.com/blog/how-long-do-disk-drives-last/)
-   [ArchWiki: list of Disk applications
    ](https://wiki.archlinux.org/index.php/List_of_applications/Utilities#Disks)

# Disk Interfaces
-   {{< wp "USB#USB_2.0"  "USB 2.0" >}} Max speed 280 Mbit/s (35 MB/s)
-   {{< wp "USB 3.0" >}}  5 Gbit/s (625 MB/s)
-   {{< wp "USB_3.0#3.1"  "USB 3.1" >}} Gen 1:  5 Gbit/s (625 MB/s);
    Gen 2: 10 Gbit/s (1250 MB/s)
-   {{< wp "USB_3.0#3.2"  "USB 3.2" >}} Gen 1x1:  5 Gbit/s (625 MB/s); Gen 1x2:
    10 Gbit/s (1250 MB/s) over 2 lanes; Gen 2x1: 10 Gbit/s (1250 MB/s);
    Gen 2x2: 20 Gbit/s (2500 MB/s) over 2 lanes;
-   {{< wp "Serial_ATA#SATA_revision_1.0_(1.5_Gbit/s,_150_MB/s,_Serial_ATA-150)" >}}
    1.5 Gbit/s, 150 MB/s
-   {{< wp "Serial_ATA#SATA_revision_2.0_(3_Gbit/s,_300_MB/s,_Serial_ATA-300)" >}}
    3 Gbits/s, 150MB/s.
-   {{< wp "Serial_ATA#SATA_revision_3.0_(6_Gbit/s,_600_MB/s,_Serial_ATA-600)" >}}
    6Gbits/s, 600MB/s
-   SATA revision 3.2 and 3.3: 16 Gbit/s, 1969 MB/s.

# hdparm
-   [ArchWiki: hdparm](https://wiki.archlinux.org/index.php/hdparm)
-   [Gentoo wiki: hdparm](http://wiki.gentoo.org/wiki/Hdparm)
-   [Linux Magazine: Tune Your Hard Disk with hdparm
    ](http://www.linux-magazine.com/Online/Features/Tune-Your-Hard-Disk-with-hdparm)

## hdparm memo
-   The configuration of hdparm in in /etc/hdparm.conf
-   information `sudo hdparm -I /dev/hdc`
-   Power status `sudo hdparm -C /dev/hdc`
-   put in stanby ` sudo hdparm -y dev/hdc`
-   put in sleep mode ` sudo hdparm -Y dev/hdc`

# smartmontool {#smartmontools}

[smartmontools](http://www.smartmontools.org/)(GPL)
:   contains two programs to report {{< wp "S.M.A.R.T." >}} able hard drives

-   [Smartmontools Home](http://www.smartmontools.org/)
    -   [Smartmontools Documentation
        ](http://www.smartmontools.org/wiki/TocDoc)
    -   [SMART attributes interpretation
        ](http://www.smartmontools.org/wiki/TocDoc#SMARTAttributes)
        which is more detailled in the
        [_ATA S.M.A.R.T. attributes_ section of the Wikipedia page
        ](http://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)
    -   [Bad block HOWTO for smartmontools
        ](https://www.smartmontools.org/wiki/BadBlockHowto)
    -   [Smartmontool FAQ](http://www.smartmontools.org/wiki/FAQ)
-   [ArchWiki: S.M.A.R.T.](https://wiki.archlinux.org/index.php/S.M.A.R.T.)
-   [Ubuntu Help: smartmontools
    ](https://help.ubuntu.com/community/Smartmontools)
-   [GentooWiki: smartmontools](http://wiki.gentoo.org/wiki/Smartmontools)
-   [smartctl(8)
    ](http://www.smartmontools.org/browser/trunk/smartmontools/smartctl.8.in)
    a command line utility to control the SMART system
-   [smartd(8)
    ](http://www.smartmontools.org/browser/trunk/smartmontools/smartd.8.in)
    a daemon that monitors the
    SMART system built into many ATA IDE and SCSI-3 hard drives.
-   [smartd.conf manual page
    ](http://www.smartmontools.org/browser/trunk/smartmontools/smartd.conf.5.in)
-   Linux Journal:
    [Monitoring Hard Disks with SMART](http://www.linuxjournal.com/article/6983)
-   [GSmartControl](https://gsmartcontrol.sourceforge.io/home/)
    is a GUI interface to smatmontool. It allows you to inspect the drive's SMART data
    to determine its health, as well as run various tests on it. It is in Debian.

### smartd memo
-   disk smart capacities: `sudo smartctl -c /dev/hdc`
-   Error log `sudo smartctl -l error /dev/hdc`
-   short seltestt (1mn) `sudo smartctl -t short /dev/hdc`
-   Long selftest `sudo smartctl -t long /dev/hdc`
-   results of selftest `sudo smartctl -l selftest /dev/hdc`
-   SMART Attributes `sudo smartctl -A /dev/hdc`
-   smartd take 1.8M Vsz
-   conf in /etc/smartd.conf

## SMART Attributes

See Wikipedia: [SMART Attributes
](http://en.wikipedia.org/wiki/S.M.A.R.T.#ATA_S.M.A.R.T._attributes)

The disk's firmware converts the raw value to a normalized value
ranging from 1 to 253. If this normalized value is less than or equal
to the threshold (THRESH), the Attribute is said to have failed

| attribute                   | meaning                                         |
|-----------------------------+-------------------------------------------------+
| 1 Raw_Read_Error_Rate       | read failure                                    |
| 3 Spin_Up_Time              | Average time of spindle spin up in millisec     |
| 4 Start_Stop_Count          | number of start from off or sleep               |
| 5 Reallocated_Sector_Ct     | nb of reallocated bad blocks                    |
| 7 Seek_Error_Rate           |                                                 |
| 9 Power_On_Hours            |                                                 |
| 10 Spin_Retry_Count         | retry indicates a mechanical pb.                |
| 12 Power_Cycle_Count        | full hard disk power on/off cycles              |
| 187 Reported_Uncorrectable  | no ecc corrrectable (see 195)                   |
| 189 High_Fly_Writes         | recording head flying outside its normal range  |
| 190 Airflow_Temperature_Cel |                                                 |
| 194 Temperature_Celsius     | better below 47°                                |
| 195 Hardware_ECC_Recovered  |                                                 |
| 197 Current_Pending_Sector  | waiting to be remapped, because of read errors  |
| 198 Offline_Uncorrectable   |                                                 |
| 199 UDMA_CRC_Error_Count    | errors in data transfer via the interface cable |
| 200 Multi_Zone_Error_Rate   | errors when writing a sector.                   |
| 202 TA_Increase_Count       |                                                 |

ECC = Error Correcting Code memory is a data storage code for testing
the accuracy of data passing through it.

The raw value of Hardware ECC Recovered as a decimal number represents
a sector count, not an error count. This value rolls over to 0 once
the count reaches about 250 million or low level disk format.

# GPT -  GUID Partition Table {#partition_table}
-   Wikipedia: {{< wp "Master boot record" >}}, {{< wp "GUID Partition Table" >}} (GPT):
    a more modern partitioning scheme, replacing the purpose of the MBR,
    {{< wp "Globally unique identifier" >}} (GID),
    {{< wp "Universally unique identifier" >}} (UUID),
    {{< wp "Unified Extensible Firmware Interface" >}} (UEFI)
    is meant as a replacement for the BIOS firmware interface,
-   The {{< wp "GUID Partition Table" >}} (GPT) is part of
    {{< wp "Unified Extensible Firmware Interface" >}} (UEFI).
    It has numerous advantages over {{< wp "Master boot record"  "MBR" >}} it uses
    {{< wp "Universally unique identifier"  "Universally unique identifier (UUID)" >}}
    also named {{< wp "Globally_Unique_Identifier"  "GUID" >}} for
    partition types, disk, and partitions. It allows a minimum of 128 partition table entries
    so logical and extended partitions are no longer necessary.
    It uses 64-bit LBA for storing Sector numbers  allowing up to 2 ZiB disks,
    and  disks with sectors larger than 512b  which are now common.
    It has backup and crc checksum for header and partition table.<br />
    _fdisk_ does not work with GPT, you have to use *gdisk* or *parted*.
-   [ArchWiki: GUID Partition Table
    ](https://wiki.archlinux.org/index.php/GUID_Partition_Table)
    see also the references in this ArchWiki page.
-   You need to have `CONFIG_EFI_PARTITION=y` (**not** `m`)
    in the kernel to support GPT,

# partitions managers. {#partionning}
See also {{< iref "filesystems" "File Systems" >}}
where you find {{< iref "filesystems#lvm" "LVM" >}}.

-   [ArchWiki: partitionning
    ](https://wiki.archlinux.org/index.php/Partitioning)
    : [partitionning tools
    ](https://wiki.archlinux.org/index.php/Partitioning#Partitioning_tools),
    [fstab](https://wiki.archlinux.org/index.php/Fstab),
    [swap](https://wiki.archlinux.org/index.php/Swap).
-   <a name="parted"></a>
    [Gnu Parted](https://www.gnu.org/software/parted/)
    is a program for creating and manipulating partition tables.
    It support  ext2, ext3, ext4,  fat16, fat32, hfs, hfs+, hfsx, linux-swap, NTFS
    reiserfs, ufs, btrfs
    -   [manual
        ](https://www.gnu.org/software/parted/manual/html_node/index.html)
    -   [ArchWiki: Gnu Parted
        ](https://wiki.archlinux.org/index.php/GNU_Parted)
    -   [Parted Cheat-Sheet
        ](http://www.troubleshooters.com/linux/parted_cheat.htm)
        by Steve litt.
-   <a name="gparted"></a>{{< wp "Gparted" >}} is the gnome front end for libparted. It supports
    btrfs, ext2 / ext3 / ext4, fat16 / fat32,  hfs / hfs+,  linux-swap, lvm2 pv, nilfs2,
    ntfs, reiserfs / reiser4,  udf, ufs, xfs. The detailed suported operations for each
    file system is summarized in the [feature page](https://gparted.org/features.php).
    -   [gparted Home](https://gparted.org/);
    -   [gparted manual](https://gparted.org/display-doc.php?name=help-manual)
    -   [ArchWiki: GParted
        ](https://wiki.archlinux.org/index.php/GParted)
    -   {{< iref "#gparted_live" "GParted Live" >}}
        is a small bootable GNU/Linux distribution for x86 based computers.

-   [ArchWiki: fdisk and gdisk
    ](https://wiki.archlinux.org/index.php/Fdisk)
-   [GPT fdisk Tutorial](http://www.rodsbooks.com/gdisk/),
    [An sgdisk Walkthrough
    ](http://www.rodsbooks.com/gdisk/sgdisk-walkthrough.html)
    by Rod Smith.
-   [Gnome Disk](https://wiki.gnome.org/Apps/Disks)
    or _gnome-disk-utility_
    is a tool to manage disk drives and media. It can format and
    partition drives,  resize partitions, mount and unmount partitions, query
    S.M.A.R.T. attributes. It uses _udisk2_.
    It has support for LUKS encryption.
    -   [gnome-disk-utility git repository
        )(https://git.gnome.org/browse/gnome-disk-utility/)

# Disk Cloning {#disk_cloning}
There are many ways of cloning a disk. We can clone the disk sector by sector; by doing
so the tool has no need to know about the underlying file system. It is nevertheless
possible to skip empty blocks and compress an image. This is the way to clone with
{{< iref "#dd" "dd" >}} and its variants, it can also be an alternative of some
utility when they don't know the file system.

-   Wikipedia: {{< wp "Disk cloning" >}}, {{< wp "List of disk cloning software" >}}
-   [ArchWiki: Disk cloning
    ](https://wiki.archlinux.org/index.php/Disk_cloning)
-   [Clone HOWTO](http://www.tldp.org/HOWTO/Clone-HOWTO/index.html)
    Describes a setup that allows a machine to boot Linux from
    BOOTP/TFTP, using the Grub boot loader, and save and restore disk
    and partition images to and from a TFTP server. _2002_.

## Low level disk copy
-   <a name="dd"></a>{{< wp "Dd_(Unix)"  "dd" >}} (GPL)
    is a unix command part of _coreutils_ used to copy partitions. the
    {{< wp "Dd_(Unix)"  "Wikipedia dd Page" >}} and man page have many examples of use.
    -   [coreutils manual: dd page
        ](http://www.gnu.org/software/coreutils/manual/html_node/dd-invocation.html)
    -   [ArchWiki: Cloning - using dd
        ](https://wiki.archlinux.org/index.php/Disk_cloning#Using_dd)
    I find sometime useful during a long *dd* to get progress information with:

        $ dd if=/dev/zero of=/dev/null count=10MB
        $ killall -s USR1 dd
        5221621+0 records in
        5221620+0 records out
        2673469440 bytes (2.7 GB) copied, 2.70126 s, 990 MB/s

-   <a name="dcfldd"></a>[dcfldd](http://dcfldd.sourceforge.net/) (GPL)
    is an enhanced version of GNU with hashing on-the-fly, progress report,
    wipe disks with a pattern, bit-for-bit verify of the image,
    multiple concurent outputs, split output to multiple files, piped output and logs.
    _dcfldd_ is in Debian.
    -   [dcfldd(1)](https://manpages.debian.org/testing/dcfldd/dcfldd.1.en.html)
-   <a name="dc3dd"></a>[dc3dd](https://sourceforge.net/projects/dc3dd/)
    is a patched version of Coreutil dd, with added features similar to
    {{< iref "#dcfldd" "dcfldd" >}} i.e on the fly hashing (md5, sha-1, sha-256,
    and sha-512), progress report, pattern wiping, write errors to a file,  group
    errors in the error log, split output.
    -   [dc3dd(1)](https://manpages.debian.org/stretch/dc3dd/dc3dd.1.en.html)
-   <a name="ddrescue"></a>
    [gnu ddrescue](http://www.gnu.org/software/ddrescue/ddrescue.html) (GPL)
    (GPL) by Antonio Diaz copies data from one file or block device to
    another, trying hard to rescue data in case of read errors.  The
    Debian package is *gddrescue* don't forget the initial **g** or
    you will get the Kurt Garloff *ddr_rescue*.<br /> I use _ddrescue_
    to recover partitions in this way (look at manual for options and
    many useful examples)

         # grab error-free areas
         ddrescue -f -n /dev/hda1 /dev/hdb1 logfile
         # work with direct access, retrying 3 times bad blocks
         ddrescue -d -f -r3 /dev/hda1 /dev/hdb1 logfile
         #check and correct the image partition, show progress and at end fs status
         e2fsck -v -f  -C 0 /dev/hdb1

    -   [gnu ddrescue manual
        ](http://www.gnu.org/software/ddrescue/manual/ddrescue_manual.html)
    -    [Kurt Garloff ddr_rescue
        ](http://www.garloff.de/kurt/linux/ddrescue/) (GPL)
         predate the *gnu ddrescue*. It can be assisted by
         [dd_rhelp
         ](http://www.kalysto.org/utilities/dd_rhelp/index.en.html) (GPL)
         the author explains in this last page, that in most case
         *gnu ddrescue* must be preferred.

## Partition cloning

-   <a name="clonezilla">[Clonezilla](http://sourceforge.net/projects/clonezilla/) (GPL)
    is a partition or disk clone tool with text interface, it is frontend to
    {{< iref "#partclone" "Partclone" >}} but can use also
    {{< iref "#dd" "dd" >}}, {{< iref "#partimage" "partimage" >}}
    and _ntfsclone_.
    Filesystem supported: ext2, ext3, ext4, reiserfs, xfs, jfs of
    GNU/Linux, FAT, NTFS of MS Windows, HFS+ of Mac OS, UFS of BSD,
    and VMFS of VMWare ESX, LVM2.
    -   [Clonezilla Live](https://clonezilla.org/clonezilla-live.php)
        is a small bootable GNU/Linux distribution for x86/amd64.
        based on  Debian Live. n image-file or as a duplicated copy of the data. The
        image of copy of the data  can be saved to locally attached storage device, or
        vian NFS, Samba or on an SSH server.
    -   [clonezilla Live documantation
       ](https://clonezilla.org/clonezilla-usage/general-live-use.php).
-   [e2image](https://manpages.debian.org/testing/e2fsprogs/e2image.8.en.html)
    can be used to copy ext2, ext3, and ext4 partitions efficiently by only copying the
    used blocks. Make shure to use the `-a` flag to include all data, without it e2image
    only includes fs metadata.
    {{< iref "#gparted" "gparted" >}} uses e2image to copy ext2/3/4 partitions.
-   <a name="fsarchiver"></a>[FSArchiver](http://www.fsarchiver.org/)
    is a system tool that allows you to save the contents of a
    file-system to a compressed and optionally encrypted archive
    file. It works at the file level for FAT32, btrfs, ext2, ext3,
    ext4, ReiserFS-4, HPFS, JFS, XFS and preserve all the standard
    file attributes (permissions, timestamps, symbolic-links,
    hard-links, extended-attributes, …). It checksum everything and so
    you can restore the sane part of a corrupted archive.
    _FSArchiver_ is in Debian and included in {{< iref "#sysrescd" "SystemRescueCd" >}}.
-   <a name="partclone">[Partclone](https://partclone.org/) (GPL)
    provides utilities to save and restore used blocks on a partition. It is similar to
    {{< iref "#partimage" "PartImage" >}} but has a wider file system support
    ext2, ext3, ext4, hfs+, reiserfs, reiser4, btrfs, vmfs3, vmfs5, xfs, jfs, ufs, ntfs,
    fat(12/16/32), exfat, f2fs, nilfs.
    -   [partclone utilities man pages](https://partclone.org/usage/).
    -   [partclone GitHub repository](https://github.com/Thomas-Tsai/partclone).
    -   [partclone wiki](https://github.com/Thomas-Tsai/partclone/wiki)
-   <a name="partimage"></a>{{< wp "Partimage" >}}
    is an ncurses disk cloning utility. It does not support ext4 or btrfs
    filesystems. and is now replaced by
    {{< iref "#fsarchiver" "FSArchiver" >}}. You can also consider
    {{< iref "#partclone" "Partclone" >}}.
    -   [partimage Home](http://www.partimage.org/)

# Disk and sectors rescue
-   {{< wp "Disc Rot" >}}  is the tendency of CD or DVD or other optical discs to become
    unreadable because of physical or chemical deterioration.
-   [Storage device Setup HOWTO
    ](https://github.com/trapexit/backup-and-recovery-howtos/blob/master/docs/setup_(storage_device).md)
    by _trapexit_, explains inititial checking of a new disk.
-   [badblocks - ArchWiki](https://wiki.archlinux.org/index.php/Badblocks)
-   Lvm does not support badblock the only solution proposed by
    [this answer to "Can LVM mark / avoid bad blocks?"
    ](https://unix.stackexchange.com/a/362257/266187)
    is to create a PV on the top of a device mapper device.
-   [File recovery - ArchWiki](https://wiki.archlinux.org/index.php/File_recovery).
-   {{< wp "Parchive" >}} is an erasure code system that produces par files for checksum
    verification of data integrity, with the capability to perform data recovery
    operations that can repair or regenerate corrupted or missing data.
    -   [par2cmdline](https://github.com/Parchive/par2cmdline/) (GPL)
        is a PAR 2.0 compatible file verification and repair tool.
-   [Disk Maintenance under Linux (Disk Recovery)
    ](http://www.linuxjournal.com/article/193) explains dumpe2fs, badblocks, debugfs use
    _1997_
-   <a name=testdisk"></a>[TestDisk](http://www.cgsecurity.org/wiki/TestDisk)
    TestDisk can find lost partitions for many file systems including
    DOS/Windows FAT12, FAT16, FAT32, exFat, NTFS; linux  ext2, ext3, ext4,
    btrfs, GFS2, GFS2, RAID 1/4/5/6, swap, lvm, lvm2; zfs, reiserfs
    ...
    Testdisk is included in {{< iref "#sysrescd" "System Rescue CD" >}}.
    -   [TestDisk step by step
        ](http://www.cgsecurity.org/wiki/TestDisk_Step_By_Step)


## Rescue systems {#rescue_systems}

-   [Finnix](http://www.finnix.org/)
    is a live cd of 300MiB based on debian testing. It is aimed at
    system administrators and does not include a desktop or
    productivity toolkit. It has support for lvm2, encrypted partitions,
    etc. There is x386, amd64, PPC, an ARM V7 version.
-   <a name="gparted_live"></a>[GParted Live](https://gparted.org/livecd.php)
    is a small bootable GNU/Linux distribution for x86/amd64 based computers.
    In addition to {{< iref "#gparted" "GParted" >}} and
    {{< iref "#parted" "Gnu Parted" >}} it contains
    {{< iref "#clonezilla" "Clonezilla" >}},   doClone,
    {{< iref "#fsarchiver" "FSArchiver" >}},   G4L,   g4u,
    {{< iref "#partimage" "PartImage" >}},
    {{< iref "#partclone" "Partclone" >}},
    {{< iref "#testdisk" "TestDisk" >}}.
    -   [Gparted Live manual
        ](https://gparted.org/display-doc.php?name=gparted-live-manual)
-   [Super Grub2 Disk](http://www.supergrubdisk.org/wiki/SuperGRUB2Disk)
    is an image to be burned on a cdrom, or installed on an usb key.
    It is used to boot a filesystem with damaged boot loader, and
    restore an unusable grub configuration.
-   <a name="sysrescd"></a>
    [SystemRescueCd](http://www.sysresccd.org/)
    is a rescue system for x86 and amd64 on CD or USB stick. It is based on Gentoo and
    provides many tools: fdisk, GRUB, Syslinux
    {{< iref "#parted" "Gnu Parted" >}},
    {{< iref "#gparted" "GParted" >}},
    {{< iref "#partimage" "PartImage" >}},
    {{< iref "#fsarchiver" "FSArchiver" >}},
    {{< iref "#ddrescue" "ddrescue" >}},
    {{< iref "#testdisk" "TestDisk" >}},
    borgbackup, rsnapshot, iozone,
    lvm2, Ntfs3g, samba,
    fstools, grub2, lilo, rsync, rdiff-backup,  Xorg or
    Xvesa with an xfce4 desktop, network tools .....<br />
    _SystemRescueCd_ has kernel images for 32 bits and 64 bits
    architecture, it allow to setup a PXE boot server, which allow you
    to rescue systems without CD drive, but with PXE boot option.
    -   [SystemRescueCD Documentation
        ](http://www.sysresccd.org/Online-Manual-EN)
        the chapter on Grub, lvm, partitioning are easy tutorials on
        these subjects.
    -   Wikipedia: {{< wp "SystemRescueCD" >}}

# Hard Disk spindown {#hd_spindown}


-   [spin down USB Hard disk
    ](http://www.nslu2-linux.org/wiki/FAQ/SpinDownUSBHarddisks)
    in [nslu2 wiki](http://www.nslu2-linux.org/wiki/) and the special
    [AutoSpinDown on Seagate FreeAgent
    ](http://www.nslu2-linux.org/wiki/FAQ/DealWithAutoSpinDownOnSeagateFreeAgent)

The number of spinup cycles for a disk is reported by `smartctl -A
<device>`.  A disk is able to spin up/down 30000-50000 times in its
lifetime. It means that if your disk spin up every 10 mn, it will last
no more than one year.

The disk standby or spindown time can be controled with
[hdparm](http://man.cx/hdparm(8) "man.cx hdparm(8)"). You can change
the value by issuing `hdparm -S <n>` where `<n>` means _n_ units of 5s
if _n <= 240_ or _(n-240)*30 minutes_ otherwise.

Then it is carreful to check how much your standby cycle increase with
smartmontool, and you can automate your setting by putting it in
`/etc/hdparm.conf`
~~~~~~~
/dev/sda {
spindown_time = 120
}
~~~~~~~
for a spindown time of 10mn.

It is very often difficult to let your disk spin down. It is kept busy
by daemons, `crond` uses to launch tasks quite often, at least hourly.
So it is usefull to check your `/etc/cron.hourly` directory, and
`/etc/cron.d` to check if your computer truly needs a hourly disk
activity.  Some other daemons that may wake up your disk are your
logging daemon _syslogd or alternative_, network time protocol daemon,
mail transport agent.




Quoting [Lapttop Mode FAQ](http://www.samwel.tk/laptop_mode/faq)
"Desktop hard drives are usually rated for only 40,000-50,000 spinups,
and one spinup every 10 minutes will kill your 40,000-spinup HD in 277
days. So this is NOT recommended for server use, unless you increase
the spinup interval dramatically, to say once every hour or
two. Laptop hard drives are usually rated for around 300,000 spinups,
so those will last about 2083 days or 6 years if you have them powered
on 24-7."

-   [How can I tell what's spinning up my drive?
    ](http://serverfault.com/questions/44294/how-can-i-tell-whats-spinning-up-my-drive)
-   [NSLU2: HowtoIdentifyWhichProcessesAccessDisk
    ](http://www.nslu2-linux.org/wiki/FAQ/HowtoIdentifyWhichProcessesAccessDisk)
-   [Laptop Mode Faq](http://www.samwel.tk/laptop_mode/faq)
    see the section 5 spinup debugging
-   Use lm-profiler from laptop-mode-tools
-   Output of `iotop -o -b -t -qqq`
-   `sudo hdparm -C /dev/sda` to know the activity of the disk.
-   [Safely remove an USB hard drive in Linux](http://elliotli.blogspot.com/2009/01/safely-remove-usb-hard-drive-in-linux.html)
    gives [this script](https://raw.github.com/liyan/suspend-usb-device/master/suspend-usb-device)
-   [hd-idle](http://hd-idle.sourceforge.net/) is the more efficient for me
-   You can try [sdparm](http://sg.danny.cz/sg/sdparm.html)
    but as quoted from the page
    "In summary, sdparm can do very little with USB mass storage devices.
    Best to start with very low expectations."

# laptop mode {#laptop_mode}

Bart Samwel has written
[Laptop mode](http://www.samwel.tk/laptop_mode/)
which is a kernel "mode" that allows you to group write activity on your disks, so that only reads of uncached data result in a disk spinup.
It replaces it's older  _Smart Spindown_ script to allow spinning down the hard disk when it is idle and the older
__kernel laptop mode__  which is described in the
[/Documentation/laptops/laptop-mode.txt
](http://www.kernel.org/doc/Documentation/laptops/laptop-mode.txt) file
of the kernel.

You may want to read
[laptop mode faq](http://samwel.tk/laptop_mode/faq)
and learn how _spinning down too many times may kill hard drives_.

Laptop mode is provided by Debian/Ubuntu package
[laptop_mode-tools](http://samwel.tk/laptop_mode/packages/debian).

The heart of the kernel laptop\_mode is the knob
`/proc/sys/vm/laptop_mode`, when it is set to *n* as in:

    sysctl -w vm.laptop_mode=5

any physical disk I/O causes Linux to flush all dirty blocks *n*
seconds after the occurrence of disk I/O.

We can also use `/proc/sys/vm/dirty_expire_centisecs` which define
when dirty data is old enough to be eligible for writeout by the
pdflush daemons. Increasing the value minimize the disk access and
increase the possibility of losing information. But for ext3fs the
journal does not use the pdflush daemon.

The flag `/proc/sys/vm/block_dump` ask the kernel to reports all
disk read and write operations that take place, and all block
dirtying done to files. The result can be accessed in dmesg.

The
[/proc/sys/vm directory
](http://www.linuxinsight.com/proc_sys_vm_hierarchy.html )
_see also [/proc/sys/vm/ kernel.org documentation
](http://www.kernel.org/doc/Documentation/sysctl/vm.txt)_
is used to tune the operation of the virtual memory (VM) subsystem
of the Linux kernel and the writeout of dirty data to disk.

# RAID
-   {{< wp "RAID"  "Wikipedia: RAID" >}}
-   [Linux Raid kernel Wiki
    ](https://raid.wiki.kernel.org/index.php/Linux_Raid).
    [Linux SATA RAID FAQ](http://linux-ata.org/faq-sata-raid.html)


# Disk performance
-   [Benchmarking - ArchWiki](https://wiki.archlinux.org/index.php/Benchmarking)
-   [Linux Benchmark Suite Homepage](http://lbs.sourceforge.net/)
-   [Phoronix Test Suite](https://www.phoronix-test-suite.com/) (GPL)
-   [Iozone Filesystem Benchmark](http://iozone.org/)
-   [Iozone manual (pdf)](http://www.iozone.org/docs/IOzone_msword_98.pdf)
-   [Rovanion/iozone-results-comparator](https://github.com/Rovanion/iozone-results-comparator)
    is a tool for comparing outputs of iozone to each other.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
