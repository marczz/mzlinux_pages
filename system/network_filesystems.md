---
title: Network File Systems
---

See also the companion pages on
{{< iref "filesystems" "Filesystems" >}},
{{< iref "encrypted_filesystems" "Encrypted Filesystems" >}},
{{< iref "webdav" "WebDav" >}}.

----

# General References
-   {{< iref "filesystems#fuse" "Fuse" >}}
    allows also numerous network filesystems: _sshfs_,
    _smbNetfs_, _fusedav_, _nasfs_, ...
-   A {{< wp "storage area network" >}} (SAN)
    attach remote computer storage to servers in such a way that the devices appear as
    locally attached devices. Most storage networks use the SCSI protocol for
    communication between servers and disk drive devices. They use technology such:
    -   {{< wp "Fibre Channel" >}}
        a gigabit-speed network technology.
    -   {{< wp "ISCSI" >}} or scsi over IP.
        -   [Open-iSCSI](http://www.open-iscsi.org/) (GPL)
            is an implementation of iSCSI protocol for linux.
        -   [iSCSI Target](http://iscsitarget.sourceforge.net/) (GPL)
            iSCSI target for linux.
    -   {{< wp "ATA over Ethernet" >}} (AoE)
        is an ethernet protocol (on the same layer than IP) to access ATA
        devices. AoE is simpler and cheaper than ISCSI, being independant
        from IP it is not routable.
-   {{< wp "Network Attached Storage" >}} (NAS)
    are servers that provide file system storage on the network,at the level of the file
    system, in contrast to SAN that work at the block level. NAS use protocol like NFS,
    SMB (aka CIFS), Upnp ...
-   {{< iref "webdav" "WebDav section" >}}
    has the references to the DAV oriented virtual file systems like
    davfs2, gvfs-dav, fusedav ...
-   [Container storage for dummies
    ](https://www.redhat.com/en/resources/container-storage-dummies)
    a free ebook from RedHat.

# Mounting Network Filesystems
-   [Chapter 18. Mounting file systems on demand - Red Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/managing_file_systems/mounting-file-systems-on-demand_managing-file-systems)
    uses autofs which is also packaged in Debian.
-   [Mount Remote Filesystems Using sshfs and systemd
    ](https://www.buggycoder.com/mount-remote-fs-sshfs-systemd/)
-   [Automount filesystems with systemd | Hetzner Community
    ](https://community.hetzner.com/tutorials/automount-filesystems-with-systemd)
-   [Automatic mounts with systemd · Blog | Tomáš Tomeček
    ](https://blog.tomecek.net/post/automount-with-systemd/)
-   [fstab Automount with systemd - ArchWiki
    ](https://wiki.archlinux.org/title/Fstab#Automount_with_systemd)
-   [Automounting SSHFS - ArchWiki](https://wiki.archlinux.org/title/SSHFS#Automounting)

# SSHFS {#sshfs}

[sshfs](http://fuse.sourceforge.net/sshfs.html) is the _fuse_ access to ssh file
systems.
-  [Ubuntu: sshfs](https://help.ubuntu.com/community/SSHFS)
   explains the usage, including mounting from fstab.
-  [ArchWiki: sshfs](https://wiki.archlinux.org/index.php/Sshfs)
-  [Gentoo Wiki: SSHFS](https://wiki.gentoo.org/wiki/SSHFS)

# NFS {#nfs}
The references to use of a disc-less Linux workstation with root
filesystems via NFS. are in the {{< iref "IP#dhcp" "Dhcp protocol section" >}}.

-   Wikipedia: {{< wp "Network File System" >}}
    gives the history of the different versions of NFS.
-   The
    [Linux NFS-HOWTO](http://nfs.sourceforge.net/nfs-howto/)
    by Christopher Smith _2006_,  describe NFS v3
    principle, use and optimization.
-   The [NFS FAQ](http://nfs.sourceforge.net/) explains
    [the main new features in version 4 of the NFS protocol
    ](http://nfs.sourceforge.net/#faq_a6)
-   [NFSV4 wiki](http://wiki.linux-nfs.org/) deal with NFSV3
    and [NFSV4
    ](http://wiki.linux-nfs.org/wiki/index.php/NFSv4_Introduction);
    there is a page on
    [NFSv4 ACLs](http://wiki.linux-nfs.org/wiki/index.php/ACLs).
-   Ietf [Network File System Version 4 (nfsv4) workgroup page
    ](http://www.ietf.org/dyn/wg/charter/nfsv4-charter.html)
    gives all the ietf documents, rfc and draft for nfs v4.
-   [ArchWiki: NFS](https://wiki.archlinux.org/index.php/NFS),
    [ArchWiki: NFS Troubleshooting
    ](https://wiki.archlinux.org/index.php/NFS/Troubleshooting)
-   [gentoo Wiki: NFS](https://wiki.gentoo.org/wiki/NFS)
-   [Ubuntu: Setting Up NFS HowTo
    ](https://help.ubuntu.com/community/SettingUpNFSHowTo), and
    [Ubuntu: nfsv4](https://help.ubuntu.com/community/NFSv4Howto)
    explain the NFS v4 configuration
-   Van Emery: [NFSv3 mini-HOWTO
    ](http://www.vanemery.com/Linux/NFS-Van.html).
    [Learning NFSv4 with Fedora Core 2
    ](http://www.vanemery.com/Linux/NFSv4/NFSv4-no-rpcsec.html) is a
    tutorial by Van Emery, not Fedora specific.  -
-   [Nfs Ganesha](https://github.com/nfs-ganesha/nfs-ganesha/wiki) (LGPL)
    is a user-mode file server for NFS (v3, 4.0, 4.1, 4.1 pNFS, 4.2).
    It is in Debian.

-   {{< man "exports(5)" >}} references the exports
    option used by the server nfs daemon.
  - We can use
    {{< man "showmount(8)" >}} to examine exports of a
    server

           showmount [-adehv] [--all] [--directories] [--exports]\
               [--no-headers] [--help] [--version] [host]

-   You should run the command `exportfs -ra to` force nfsd to
    re-read the /etc/exports file
    ({{< man "exportfs(8)" >}})
    If you can't find the exportfs command, then you can kill nfsd with
    the `-HUP` flag
-   `hard,intr` is recommended on all fs, it means the program
    accessing a file on NFS will hang when the server crashes and when
    the NFS server is back online the program will continue undisturbed
    from where it was. But because of intr you can kill the program.
-   I did some benchmark for access of a nfsv3 server from my linksys
    router to evaluate the effects of buffer size:
    -   performance with default buffers or 32k buffer is 1.7 MBytes/s
        = 14 Mbits/s write, read is twice quicker i.e 3,4MBytes/s = 28
        Mbits/s
    -   with 16k buffer it lower down to 12Mbits/s write, 19Mbits/s
        read
    -   with 8k buffer 10Mbits/s write, 15Mbits/s read


To forward nfs v3 through NAT is not trivial because the number of
services used and the use of portmapped ports. To view the ports
used on some machine you can use
{{< man "rpcinfo(8)" >}} it can be necessary to
secure your firewall rules to tie down the ports of the nfs
services to fixed values.

The following table gives the services and ports used for nfs


<table width="700"  cellspacing="1" cellpadding="1" border="1" align="left" summary="table of nfs services ports">
    <thead>
        <tr>
            <th>service </th>
            <th>used port </th>
            <th>fixed to </th>
            <th>conf </th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>portmap</td>
            <td>111</td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>nfs</td>
            <td>2049 <br />
            </td>
            <td>&nbsp;</td>
            <td><br />
            </td>
        </tr>
        <tr>
            <td>rquotad</td>
            <td>4003 <br />
            </td>
            <td>&nbsp;</td>
            <td>&nbsp;</td>
        </tr>
        <tr>
            <td>mountd</td>
            <td>random</td>
            <td>4005<br />
            </td>
            <td>fix the port via -p option<br />
            </td>
        </tr>
        <tr>
            <td>statd (status)
            </td>
            <td>random
            </td>
            <td>4001 (listen)<br />
                4002 (outgoing)
            </td>
            <td>fix the port with -p (listen) and -o (outgoing)
            </td>
        </tr>
        <tr>
            <td>lockd (nlockmanager)</td>
            <td>random</td>
            <td>4004
            </td>
            <td>change with sysctl:&nbsp; fs.nfs.nlm_tcpport fs.nfs.nlm_udpport</td>
        </tr>
    </tbody>
</table>
<br/>

On gentoo system you can give the ports in `/etc/conf.d/nfs` the
debian/ubuntu user will use `/etc/default/nfs-common` and
`/etc/default/nfs-kernel-server`

The nfsv4 allow tcp connection and don't use rpc so crossing firewall
is easier.


# CIFS, Samba {#samba}

<!-- [[file:../../../../content-org/notes/system_notes/filesystems_notes.org::#samba][Samba Notes]] -->

## CIFS references
{{< wp "Samba_(software)"  "Wikipedia: Samba" >}} and {{< wp "Server_Message_Block"  "SMB/CIFS" >}}.

-   [Samba Home](http://www.samba.org/) and [Samba Wiki](http://wiki.samba.org/index.php)
-   [Samba Documentation](https://www.samba.org/samba/docs/) is mainly on the in
    [Samba Wiki User Documentation](https://wiki.samba.org/index.php/User_Documentation).
-   [Samba man pages](https://www.samba.org/samba/docs/current/man-html/)
-   [ArchLinux: Samba](https://wiki.archlinux.org/index.php/Samba) is
    a new complete howto.
-   Debian Wiki: [Samba Main page and subpages index](https://wiki.debian.org/Samba),
    [Samba/ServerSimple](https://wiki.debian.org/Samba/ServerSimple),
-   [Gentoo Wiki: Samba](https://wiki.gentoo.org/wiki/Samba),
    [Samba/Samba 4 Migration](https://wiki.gentoo.org/wiki/Samba/Samba_4_Migration),
-   [The Unofficial Samba HOWTO](http://www.oregontechsupport.com/samba/) _2013_
-   [SMB HOWTO](https://tldp.org/HOWTO/SMB-HOWTO.html) is old _2000_.
-   [CIFS Explained](http://www.codefx.com/CIFS_Explained.htm)
-   [KSMBD - SMB3 Kernel Server](https://docs.kernel.org//filesystems/cifs/ksmbd.html)
    is a linux kernel server which implements SMB3 protocol in kernel space.
    It is in Debian. KSMBD doesn't aim to be as comprehensive as well known Samba for
    CIFS/SMB support in user-space but is focused on the performance.


## Samba tools
-   [Samba.org: List of Samba Gui tools](http://www.samba.org/samba/GUI/)
    is obsolete.
-   [smbclient](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)
    is a ftp-like samba client from the samba distribution.
-   [Samba Commander (SMBC)](http://sourceforge.net/projects/smbc/) (GPL)
    is a text mode SMB network commander that allows to browse the local network,
    search for files, download/upload files and directories and create them both
    locally and remotely. The last release is in 2005 and it is no longer packaged in
    Debian.
-   [smb2www · Debian packaging GitLab](https://salsa.debian.org/debian/smb2www)
     is a perl CGI extension to smbclient, the upstream package is dead since 1998, but
     it is still maintained in Debian.
-   [SMBNetFS](http://sourceforge.net/projects/smbnetfs/)
    (GPL) is a fuse filesystem that allows you to use samba/microsoft
    network in the same manner as the network eighbourhood in
    Windoze. It is in Debian.
    -   [ArchWiki: samba - smbnetfs
        ](https://wiki.archlinux.org/index.php/samba#smbnetfs)
    -   [Gentoo Wiki: smbnetfs](https://wiki.gentoo.org/wiki/Smbnetfs)
    -   [smbnetfs - ubuntu-fr Wiki](https://doc.ubuntu-fr.org/smbnetfs)
    -   [SMBNetFS - Git repository
        ](https://sourceforge.net/p/smbnetfs/git/ci/master/tree/).
   <!-- [[file:../../../../content-org/notes/system_notes/filesystems_notes.org::#smbnetfs][smbnetfs notes]]  -->
-   [Fusesmb](http://www.ricardis.tudelft.nl/~vincent/fusesmb/) is an
    older implementation of samba under fuse that allows you to create
    a folder that displays the available shares on a network. SMBNetFS
    and Fusesmb uses the same library _libsmbclient_ _gvfs_ has also a
    backend for Samba. It is in Debian.

    [FuseSmb - Ubuntu Help](https://help.ubuntu.com/community/FuseSmb)
    warns that:
    >> Note that "fusesmb" has several outstanding bug reports from people who find that
    >> it leaves an empty directory with no contents, and that its "fusesmb.cache" file
    >> never gets written.

### Netbios tools

-   [NetBIOS Name Service (nmbd) tutorial
    ](https://www.halolinux.us/network-servers/netbios-name-service.html)

-   [nmblookup](https://www.samba.org/samba/docs/current/man-html/nmblookup.1.html)
    is the basic tool in the smbclient suite to lookup NetBIOS names.
-   [smbmap](https://github.com/ShawnDEvans/smbmap) (GPL 3.0)
     allows users to enumerate samba share drives across an entire domain. List share
     drives, drive permissions, share contents, upload/download functionality, file name
     auto-download pattern matching, and even execute remote commands.
     _smbmap_ is in Debian.
-   [wsdd](https://github.com/christgau/wsdd) (MIT License)
    is a python program which implements a Web Service Discovery host daemon. This
    enables (Samba) hosts to be found by Web Service Discovery Clients like Windows.

    It also implements the client side of the discovery protocol which allows to search
    for Windows machines and other devices.

    wsdd is in Debian.
-  {wsdd2](https://github.com/Netgear/wsdd2) (GPL 3.0)
   is a Netgear daemon which advertises and responds to probe requests from Windows clients
   looking for File Shares. It is in Debian.

## Samba tips

-   The most basic way to test your installation is with
    [smbclient
    ](http://www.samba.org/samba/docs/man/manpages-3/smbclient.1.html)
-   The configuration directories mentioned in all man pages and particularly in
    [smb.conf(5)
    ](http://www.samba.org/samba/docs/man/manpages-3/smb.conf.5.html)
    is seen with the command [smbd
    ](http://www.samba.org/samba/docs/man/manpages-3/smbd.8.html):

        smbd -b

-   The stored accounts are listed by root with the
    [pdbedit utility
    ](http://www.samba.org/samba/docs/man/manpages-3/pdbedit.8.html)
    as `pdbedit --list`, the details of an account is seen with

        pdbedit --verbose --list <account>

-   The [pdbedit utility
    ](http://www.samba.org/samba/docs/man/manpages-3/pdbedit.8.html)
    can also be used to add or delete accounts, see the
    [pdbedit(8) man page
    ](http://www.samba.org/samba/docs/man/manpages-3/pdbedit.8.html)
    or [Samba HowTo: account databases
    ](http://www.samba.org/samba/docs/man/Samba-HOWTO-Collection/passdb.html)
-   The master browser is returned by
     [nmblookup](http://www.samba.org/samba/docs/man/manpages-3/nmblookup.1.html):

        nmblookup -M -- -

-   To do a unicast query to some host use something like:

        nmblookup -U 192.168.1.1 -R 'WORKGROUP#1E'

-    A Reverse query is done with:

        nmblookup  -A 192.168.1.2

-   You can also use the program [NBTScan
    ](http://inetcat.org/software/nbtscan.html)
    to do a network scanning using it as:

        sudo nbtscan -r 192.168.1.0/24

# High Availability
See also {{< iref "clouds" "Cloud Storage" >}}.

-   [ClusterLabs Home](http://clusterlabs.org/)
    an open source high availability cluster stack grouping
    [Corosync](http://clusterlabs.org/corosync.html),
    [Pacemaker](http://clusterlabs.org/pacemaker/),
    [DRBD](https://linbit.com/), [ScanCore](https://www.alteeve.com/w/ScanCore).
-   Gentoo Wiki: [Corosync](https://wiki.gentoo.org/wiki/Corosync),
    [Heartbeat](https://wiki.gentoo.org/wiki/Heartbeat),
    [Pacemaker](https://wiki.gentoo.org/wiki/Pacemaker).

# Distributed filesystems {#distributed_filesystems}

See also {{< iref "clouds" "Cloud Storage" >}}.

-   Wikipedia:
    {{< wp "Clustered file system" >}},
    {{< wp "List_of_file_systems#Distributed_file_systems" "Distributed file systems" >}},
    {{< wp "Comparison_of_distributed_file_systems" "Comparison of distributed file systems">}},
    {{ wp "Filesystem_in_Userspace#Remote/distributed_file_system_clients" "Fuse Remote/distributed file system clients" >}}.
-   [awesome-sysadmin] - Distributed Filesystem]i
    (https://github.com/awesome-foss/awesome-sysadmin#distributed-filesystems)
-   [awesome distributed systems
    ](https://github.com/theanalyst/awesome-distributed-systems).
-   Wikipedia: {{< wp " Comparison of distributed file systems" >}}
-   [ArchWiki: list of distributed filesystems
    ](https://wiki.archlinux.org/index.php/List_of_applications#Distributed_file_systems).
-   {{< wp "Ceph (software)"  "Ceph" >}} is a distributed object store and filesystem.
    -   [Gentoo Wiki: ceph](https://wiki.gentoo.org/wiki/Ceph)
    -   [ArchWiki: ceph](https://wiki.archlinux.org/index.php/Ceph).
    -   [Ceph Home](https://ceph.com/)
    -   [Ceph cluster on Raspberry Pi
        ](http://bryanapperson.com/blog/the-definitive-guide-ceph-cluster-on-raspberry-pi/)
-   __cLVM__ or Cluster Logical Volume Manager,  extend LVM to support transparent
    management of volume groups across a cluster.
    -   [Suse SLE: CLVM
        ](https://www.suse.com/documentation/sle-ha-12/book_sleha/data/cha_ha_clvm.html).
    -   [Red Hat  LVM Administration : Creating LVM Volumes in a Cluster
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/logical_volume_manager_administration/LVM_administration#cluster_setup),
        [Creating a Mirrored LVM Logical Volume in a Cluster
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/6/html/logical_volume_manager_administration/mirvol_create_ex).

## DRBD {#drbd}
{{< wp "DRBD" >}} (Distributed Replicated Block Device) (GPLv2) is a distributed
storage system normally used on high availability (HA) clusters.
It implements a network RAID1 storage.
[DRBD Home](http://www.drbd.org/home/) is hosted by LINBIT.<br />
There are packages for main distributions,
including a kernel module and a user space software.
Since Lenny DRDB is part of Debian.

-   [Linbit Docs – DRDB User Guide 9.0
    ](https://docs.linbit.com/docs/users-guide-9.0/),
    [DRDB User Guide 8.4](https://docs.linbit.com/docs/users-guide-8.4/)
-   [Suse High Availability Guide: DRDB
    ](https://www.suse.com/documentation/sle_ha/singlehtml/book_sleha/book_sleha.html#sec.ha.drbd)
    also available in [Suse Administration Guide - DRDB
    ](https://www.suse.com/documentation/sle-ha-12/book_sleha/data/cha_ha_drbd.html).
-   [Suse SLE: Highly Available NFS Storage with DRBD and Pacemaker
    ](https://www.suse.com/documentation/sle-ha-12/singlehtml/book_sleha_techguides/book_sleha_techguides.html).
-   [Debian Wiki - DrBd](https://wiki.debian.org/DrBd)
-   [Ubuntu Help - DRBD](https://help.ubuntu.com/lts/serverguide/drbd.html)
-   [Thomas Krenn - HA Cluster with Heartbeat, Pacemaker, DRBD and LXC
    ](https://www.thomas-krenn.com/en/wiki/HA_Cluster_with_Linux_Containers_based_on_Heartbeat,_Pacemaker,_DRBD_and_LXC).
-   [HowToForge - High Availability NFS With DRBD + Heartbeat
    ](https://www.howtoforge.com/high-availability-nfs-with-drbd-plus-heartbeat)
-   [Manual HA Cluster with Linux Containers, DRBD and Btrfs
    ](https://petrovs.info/2014/11/28/ha-cluster-with-linux-containers/)
    by Blagovest Petrov.
-   [How to Setup MariaDB High Availability with Heartbeat and DRBD on Ubuntu
    ](https://www.howtoforge.com/tutorial/ubuntu-drbd-heartbeat-high-availability/)
-   [Gentoo Wiki - DRBD with OCFS2](https://wiki.gentoo.org/wiki/DRBD_with_OCFS2)
-   [Atlantic.Net - How to: DRBD Replication and Configuration
    ](https://www.atlantic.net/cloud-hosting/how-to-drbd-replication-configuration/)
-   [SUPINFO - Installation et configuration de DRBD
    ](https://www.supinfo.com/articles/single/2140-installation-configuration-drbd),
    [Mise en place d'un SAN ISCSI sous linux avec DRBD
    ](https://www.supinfo.com/articles/single/3921-mise-place-san-iscsi-linux-avec-drbd)

## Glusterfs {#glusterfs}
{{< wp "GlusterFS" >}} (GPL and LGPL)
is a clustered file-system. It aggregates various storage bricks over Infiniband RDMA or
TCP/IP.

-   [GlusterFS Documentation](https://docs.gluster.org/en/latest/)
-   [Red Hat Gluster Storage
    ](https://access.redhat.com/documentation/en-us/red_hat_gluster_storage/)
-   [GlusterFS Storage Cluster on CentOS 7
    ](https://wiki.centos.org/HowTos/GlusterFSonCentOS)
-   [BTRFS as a GlusterFS storage back-end
    ](https://www.spinics.net/lists/linux-btrfs/msg64541.html).
-   [GlusterFS – IT Tips and Tricks](https://tipstricks.itmatrix.eu/category/glusterfs/)
-   [GlusterFS Tips](https://tipstricks.itmatrix.eu/category/glusterfs/)
    from Michel Bisson.
-   [GlusterFS sur Ubuntu/Debian
    ](https://linuxfr.org/wiki/glusterfs-sur-ubuntu-debian).

## GarageHQ
[GarageHQ](https://garagehq.deuxfleurs.fr/) (AGPL v3)
is a geo-distributed data store that implements the Amazon S3 object storage protocol.

Note that the access to Garage is a pure S3 object storage protocol, it does not provide
posix compatibility.

-   [Deuxfleurs/garage Git repository](https://git.deuxfleurs.fr/Deuxfleurs/garage)

## GFS2 {#gfs2}
{{< wp "Global File System 2" >}} (GFS2)  (GPL)
is a  is a {{< wp "shared-disk file system" >}} available for Linux computer
clusters. It requires all nodes to have direct concurrent access to
the same shared block storage and has no disconnected operating
mode like other {{< wp "shared-disk file systems" >}} like {{< wp "OCFS2" >}}, {{< wp "Lustre" >}},
{{< wp "Lizardfs" >}}.

In contrast {{< wp "distributed file systems" >}} like GlusterFS, Ceph, BeeGFS do not
share block level access to the same storage but use a network protocol and can have a
disconnected operating mode.

It uses Fibre Channel, iSCSI, AoE or DRDB in primary/primary mode devices as
storage.

_Not to be confused with {{< wp "Google File System" >}} a proprietary distributed
fs also known by the acronym GFS or GoogleFS._


## JuiceFs {#juicefs}
[JuiceFs](https://juicefs.com/en/) (Apache2 License)
is a GoLang distributed POSIX file system built on top of Redis (or another database)
and S3 compatible object storage.

JuiceFS comes in two versions: a Community Edition and an Enterprise Edition. The
Enterprise Edition uses a proprietary metadata engine.

-   [JuiceFs - GitHub](https://github.com/juicedata/juicefs).

### JuiceFs documentation

-   [JuiceFS documentation (community edition)
    ](https://juicefs.com/docs/community/introduction/)
-   [Distributed filesystem comparison - JuiceFS Blog
    ](https://juicefs.com/en/blog/engineering/distributed-filesystem-comparison)
-   [Comparing with others
    ](https://juicefs.com/docs/community/comparison/juicefs_vs_alluxio/)
    contains a detailled comparison with
    Alluxio, Ceph, GlusterFs, S3FS, S3QL, Seaweedfs.
-   [6 Essential Tips for JuiceFS Users - JuiceFS Blog
    ](https://juicefs.com/en/blog/usage-tips/juicefs-user-tips-distributed-file-storage-system)
-   [Guidance on selecting metadata engine in JuiceFS - JuiceFS Blog
    ](https://juicefs.com/en/blog/usage-tips/juicefs-metadata-engine-selection-guide)
-   [How to Set Up Metadata Engine
    ](https://juicefs.com/docs/community/databases_for_metadata)
    present the setup for each choice of metadata engine.
-   [PostgreSQL Best Practices
    ](https://juicefs.com/docs/community/postgresql_best_practices)
-   [Metadata Backup & Recovery](https://juicefs.com/docs/community/metadata_dump_load/)
-   [How to Set Up Object Storage](https://juicefs.com/docs/community/reference/how_to_set_up_object_storage)

-   [Deploy WebDAV Server](https://juicefs.com/docs/community/deployment/webdav/)
-   [Create Samba Shares](https://juicefs.com/docs/community/deployment/samba)
-   [How to create a WebDAV share on JuiceFS? - JuiceFS Blog
    ](https://juicefs.com/en/blog/usage-tips/setting-up-webdav-on-juicefs)
-   [Create Samba Shares](https://juicefs.com/docs/community/deployment/samba)
-   [Create NFS Shares](https://juicefs.com/docs/community/deployment/nfs)
-   [Configuring Samba and NFS on JuiceFS - JuiceFS Blog
    ](https://juicefs.com/en/blog/usage-tips/scalable-cloud-storage-samba-nfs-shares-juicefs)

## Minio {#minio}
{{< wp "Minio" >}} (AGPLv3) is a cloud storage server written in golang
compatible with Amazon S3.

Minio provide storage optimizations through erasure coding and POSIX/Filesystem
compatibility.

deb, rpm packages and docker image are provided.

*Note: We put Minio in this section, because it is a s3compatible cloud storage,
but Minio lack the "distributed" feature.*

-  [MinIO Home](https://min.io/)
-  [Minio - GitHub](https://github.com/minio/minio).
-  [Minio Documentation](https://docs.min.io/).
-  In the clouds section you find the S3 API clients including the
   {{< iref "clouds#miniocli" "minio client *mc*" >}}.

## NBD {#nbd}
{{< wp "Network_block_device"  "NBD (Network block device)" >}}
([nbd home](http://nbd.sourceforge.net/) )
kernel module, allows remote servers to be used as local block
devices

## OpenDedup – SDFS {#opendedup}
[OpenDedup – SDFS](https://opendedup.org/odd/) (GPL)
is a POSIX compliant filesystem hat performs inline deduplication to local disk or
cloud object storage. It works natively with the applications such as backup, when
you do copy data, it dedupes, compresses, encrypts, and saves your data on disk or
in the cloud. It can perform file level snapshots, and replication; with
replication, only unique blocks  that are not shared between the two SDFS volumes
are replicated.

-   SDFS works with AWS S3, AWS Glacier, Azure, Google, and most S3 compliant backends.
-   SDFS uses strong AES-CBC 256 bit encrytion, either when using local block
    storage _in this case metadata is not encrypted_, or when data is sent to the
    cloud all data, metadata, and hash table entries are encrypted before the data
    is sent.
-   [SDFS works with Backblaze B2
    ](https://opendedup.org/odd/2018/04/04/backblaze-b2-enabled/)
-   [Administration Guide – OpenDedup
    ](https://opendedup.org/odd/administration-guide/)

## SeaweedFs {#seaweedfs}
[SeaweedFs](https://github.com/seaweedfs/seaweedfs) (Apache2 License)
is a GoLang distributed file storage systems.

The system consists of three components:

-    The volume servers, which store files in the underlying layer (filesystem or S3
     compatible object storage).
-    The master servers, which manage the cluster
-    The Filer, which provides the filesystem by using the metadata which is stored
     separately in a database, like JuiceFs.


-   [SeawedFS wiki](https://github.com/seaweedfs/seaweedfs/wiki/) contains the SeaweedFs
    documentation.

## S3FS {#s3fs}
<a name="s3fs"></a>[s3fs](https://github.com/s3fs-fuse/s3fs-fuse) (GPL)
is a C++ software which allows Linux and macOS to mount an S3 bucket via FUSE. s3fs
preserves the native object format for files. It is also compatible with Google
Cloud Storage, and other S3-based object stores. _S3Fs_ is packaged in Debian.

See also the alternatives {{< iref "#yas3fs" "YAS3FS" >}} and
{{< iref "#goofys" "goofys" >}}.

-   {{< iref "python_libraries#pyfilesystem" "PyFilesystem" >}} is a Python module
    that provides a simplified common interface to many types of filesystem, like
    FTPfs, WebdavFs, tarFs, ZipFs,... including
    [support for f3fs](https://www.pyfilesystem.org/page/s3fs/).
-   <a name="yas3fs"></a>[YAS3FS](https://github.com/danilop/yas3fs) (MIT Licence)
    (Yet Another S3-backed File System) is a Filesystem in Userspace (FUSE) interface
    to Amazon S3. It is a rewritting in python of {{< iref "#s3fs" "s3fs" >}} which
    adds a distributed cache
    synchronized by Amazon SNS notifications. A web console is provided to easily
    monitor the nodes of a cluster.
-   <a name="goofys"></a>[goofys](https://github.com/kahing/goofys) (Apache License)
    similar to {{< iref "#s3fs" "s3fs" >}} but written in go. It features better
    performance, and less POSIX compliance than {{< iref "#s3fs" "s3fs" >}}.

    It works with Ceph (ex: Digital Ocean Spaces, DreamObjects, gridscale), EMC
    Atmos Google Cloud Storage, OpenStack Swift, {{< iref "#s3proxy" "S3Proxy" >}},
    {{< iref "network_filesystems#Minio" "Minio" >}} (limited), Wasabi,Scaleway, Azure.

    Prebuilt binaries are available in the GitHub release page.

## S3Backer
[s3backer](https://github.com/archiecobbs/s3backer) (GPL)
is a filesystem that contains a single file backed by Amazon S3. The blocks of the file
are stored as S3 objects. It provides a single normal file having a fixed size which is
used to mount a loopback device then *s3backer* acts a virtual hard disk device.
_S3backer_ is packaged in Debian.

## S3QL {#s3ql}
[S3QL](https://github.com/s3ql/s3ql/) (GPL3.0)
is a file system that stores all its data online using storage services like Google
Storage, Amazon S3 and S3 compatible, OpenStack, Blackblaze B2, local filesystem.

S3QL is written in python and offers all posix features of a local file system, it
supports hardlinks, symlinks, standard unix permissions, extended attributes.

_S3QL_ deduplicate and compress data, it allows an optional AES encryption, It allows
Copy-on-Write/Snapshotting.

_S3QL_ is packaged in Debian.
-   [S3QL User’s Guide](http://www.rath.org/s3ql-docs/index.html)
-   [s3ql Wiki](https://github.com/s3ql/s3ql/wiki) includes an *incomplete* list of
    alternatives to S3QL.
-   [JuiceFS vs. S3QL | JuiceFS Documen
    ](https://juicefs.com/docs/community/comparison/juicefs_vs_s3ql)

## Tahoe-LAFS
{{< wp "Tahoe-LAFS" >}}
_the Least Authority File System_ is a distributed filesystem
written in python over Fuse, that features high reliability,
strong security properties, and a fine-grained sharing model.
Files are encrypted, signed, erasure-coded, then distributed over
multiple servers, such that any (configurable) subset of the
servers will be sufficient to recover the data.

There is a Tahoe-LAFS Debian Package.

-   [Tahoe-LAFS Home](https://tahoe-lafs.org/trac/tahoe-lafs)


# Cluster Management
-   [Debian-HA Clusters From Scratch - Debian Wiki
    ](https://wiki.debian.org/Debian-HA/ClustersFromScratch)
    *is tagged as obsolete*.
-   [Simple Linux Cluster - Tyler's Guides
    ](https://tylersguides.com/guides/simple-linux-cluster/)
-   [Linux High Availability _HA_](http://linux-ha.org/wiki/Main_Page).

## Pacemaker
[Pacemaker](http://clusterlabs.org/pacemaker/) (GPL)
is an open source high availability resource manager.

-   [Cluster From Scratch, HA Guide - Cluster Labs
    ](https://www.clusterlabs.org/pacemaker/doc/2.1/Clusters_from_Scratch/html/)
    uses  Pacemaker with Corosync. The documentation is based on the use of the use of
    the *AlmaLinux* opensource RH compatible distribution.

    Cluster Labs is the home of Pacemaker.
    -   [ClusterLabs > Ubuntu Quickstart
        ](https://www.clusterlabs.org/quickstart-ubuntu.html)
    -   [ClusterLabs Wiki](https://projects.clusterlabs.org/w/)
-   [pacemaker - GitHub](https://github.com/ClusterLabs/pacemaker) (GPL 2)
-   [corosync: The Corosync Cluster Engine] - GitHub
    ](https://github.com/corosync/corosync) (BSD License)

Documentation is also available at RedHat and Suse as the two companies developed
pacemaker and corosync.

-   [Configuring and managing high availability clusters Red Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/configuring_and_managing_high_availability_clusters/index)
    -   [Chapter 1. High Availability Add-On overview](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/configuring_and_managing_high_availability_clusters/assembly_overview-of-high-availability-configuring-and-managing-high-availability-clusters)
        is the introductory chapter, the following chapters present the pacemaker usage.
-   [Suse SLE HA 15 SP4 | Pacemaker Remote Quick Start
    ](https://documentation.suse.com/sle-ha/15-SP4/single-html/SLE-HA-pacemaker-remote/index.html)
-   [Suse SLE HA 15 SP5 | Highly Available NFS Storage with DRBD and Pacemaker
    ](https://documentation.suse.com/sle-ha/15-SP5/html/SLE-HA-all/article-nfs-storage.html)
-   [Suse SLE HA 15 SP5 | Administration Guide | Corosync QDevice and QNetd
    ](https://documentation.suse.com/sle-ha/15-SP5/html/SLE-HA-all/cha-ha-qdevice.html)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
