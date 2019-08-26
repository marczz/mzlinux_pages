---
title: Network File Systems
---

{{% toc /%}}

See also the companion pages on
{{< iref "filesystems" "filesystems" >}},
{{< iref "encrypted_filesystems" "encrypted filesystems" >}}.

----

# General References
-   {{< iref "filesystems#fuse" "Fuse" >}}
    allows also numerous network filesystems: _sshfs_,
    _smbNetfs_, _fusedav_, _nasfs_, ...
-   A {{< wp "storage area network" >}} (SAN)
    attach remote computer storage to servers in such a way that the
    devices appear as locally attached devices. Most storage networks
    use the SCSI protocol for communication between servers and disk
    drive devices. They use technology such:
    -   {{< wp "Fibre Channel" >}}
        a gigabit-speed network technology.
    -   {{< wp "ISCSI" >}}
        or scsi over IP. [Open-iSCSI](http://www.open-iscsi.org/)
        GPL is an implementation of iSCSI protocol for linux. [iSCSI Target](http://iscsitarget.sourceforge.net/) is a GPL iSCSI target for linux.
    -   {{< wp "ATA over Ethernet" >}} (AoE)
        is an ethernet protocol (on the same layer than IP) to access ATA
        devices. AoE is simpler and cheaper than ISCSI, being independant
        from IP it is not routable.
-   {{< wp "Network Attached Storage" >}} (NAS)
    are servers that provide file system storage on the network,at the
    level of the file system, in contrast to SAN that work at the block
    level. NAS use protocol like NFS, SMB (aka CIFS), Upnp ...
-   [Coda](http://www.coda.cs.cmu.edu/): a distributed file system,
    it supports disconnected operation, i.e. full access to a cached
    section of the file space during voluntary or involuntary network
    or server outages.
-   {{< iref "webdav" "WebDav section" >}}
    has the references to the DAV oriented virtual file systems like
    davfs2, gvfs-dav, fusedav ...
-   [Container storage for dummies
    ](https://www.redhat.com/en/resources/container-storage-dummies)
    a free ebook from RedHat.




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

## CIFS references
{{< wp "Samba_(software)"  "Wikipedia: Samba" >}} and {{< wp "Server_Message_Block"  "SMB/CIFS" >}}.

-   [Samba Home](http://www.samba.org/) and [Samba Wiki
    ](http://wiki.samba.org/index.php)
-   [Samba Documentation](https://www.samba.org/samba/docs/) is mainly on the
    in [Samba Wiki User Documentation
    ](https://wiki.samba.org/index.php/User_Documentation).
-   [Samba man pages](https://www.samba.org/samba/docs/current/man-html/)
-   [ArchLinux: Samba](https://wiki.archlinux.org/index.php/Samba) is
    a new complete howto.
-   [Gentoo Wiki: Samba](https://wiki.gentoo.org/wiki/Samba),
    [Samba/Samba 4 Migration](https://wiki.gentoo.org/wiki/Samba/Samba_4_Migration),
-   [The Unofficial Samba HOWTO
    ](http://www.oregontechsupport.com/samba/)
-   [CIFS Explained](http://www.codefx.com/CIFS_Explained.htm)


## Samba tools
-   [Samba.org: List of Samba Gui tools](http://www.samba.org/samba/GUI/)
-   [Samba Commander (SMBC)](http://sourceforge.net/projects/smbc/) (GPL)
     is a text mode SMB network commander that
     allows to browse the local network, search for files,  download/upload files and directories
     and create them both locally and remotely.
-   [SMBNetFS](http://sourceforge.net/projects/smbnetfs/)
    (GPL) is a fuse filesystem that allows you to use samba/microsoft
    network in the same manner as the network eighbourhood in
    Windoze. It is in Debian.
    -   [ArchWiki: samba - smbnetfs
        ](https://wiki.archlinux.org/index.php/samba#smbnetfs)
    -   [Gentoo Wiki: smbnetfs
        ](https://wiki.gentoo.org/wiki/Smbnetfs)

-   [Fusesmb](http://www.ricardis.tudelft.nl/~vincent/fusesmb/) is an
    older implementation of samba under fuse that allows you to create
    a folder that displays the available shares on a network. SMBNetFS
    and Fusesmb uses the same library _libsmbclient_ _gvf_ has also a
    backend for Samba. It is in Debian.
-   [swat](http://www.samba.org) is the Samba web administration tool.
    -   [SWAT: The Samba Web Administration Tool
        ](http://www.samba.org/samba/docs/man/Samba-HOWTO-Collection/SWAT.html)
        in Samba Reference Guide.

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
-   [Linux-HA](http://linux-ha.org/wiki/Main_Page).
-   [ Red Hat - Configuring and managing high availability clusters
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8-beta/html/configuring_and_managing_high_availability_clusters/)
-   [Cluster From Scratch - pdf HA Guide
    ](http://www.clusterlabs.org/doc/Cluster_from_Scratch.pdf)
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
-   {{< wp "DRBD" >}} (Distributed Replicated Block Device) (GPLv2) is a distributed
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
-   {{< wp "GlusterFS" >}} (GPL and LGPL)
    is a clustered file-system. It aggregates various storage bricks
    over Infiniband RDMA or TCP/IP.
    -   [GlusterFS Documentation](https://docs.gluster.org/en/latest/)
    -   [Red Hat Gluster Storage: Overview, Use cases, Resources,
        Get started
        ](https://www.redhat.com/en/technologies/storage/gluster)
    -   [GlusterFS Storage Cluster on CentOS 7
        ](https://wiki.centos.org/HowTos/GlusterFSonCentOS)
    -   [BTRFS as a GlusterFS storage back-end
        ](https://www.spinics.net/lists/linux-btrfs/msg64541.html).
    -   [GlusterFS Tips
        ](https://tipstricks.itmatrix.eu/category/glusterfs/)
        from Michel Bisson.
    -   [Espace de stockage hautement disponible Partie 1
        ](https://www.supinfo.com/articles/single/1184-espace-stockage-hautement-disponible-partie-1)
        et [Partie 2
        ](https://www.supinfo.com/articles/single/1185-espace-stockage-hautement-disponible-partie-2)
        a tutorial on GlusterFs.
    -   [GlusterFS sur Ubuntu/Debian
        ](https://linuxfr.org/wiki/glusterfs-sur-ubuntu-debian).
-   {{< wp "Global File System 2" >}} (GFS2)  (GPL)
    is a  is a {{< wp "shared-disk file system" >}} available for Linux computer
    clusters. It requires all nodes to have direct concurrent access to
    the same shared block storage and has no disconnected operating
    mode like other {{< wp "shared-disk file systems" >}} like {{< wp "OCFS2" >}}, {{< wp "Lustre" >}},
    {{< wp "Lizardfs" >}}.

    In contrast  {{< wp "distributed file systems" >}} like GlusterFS, Ceph, BeeGFS  do not share
    block level access to the same storage but use a network protocol
    and can have a disconnected operating mode.
    It uses Fibre Channel, iSCSI, AoE or DRDB in primary/primary mode devices as
    storage.

    _Not to be confused with {{< wp "Google File System" >}} a proprietary distributed
    fs also known by the acronym GFS or GoogleFS._
-   {{< wp "Network_block_device"  "NBD (Network block device)" >}}
    ([nbd home](http://nbd.sourceforge.net/) )
    kernel module, allows remote servers to be used as local block
    devices
-   {{< wp "Tahoe-LAFS" >}}
    _the Least Authority File System_ is a distributed filesystem
    written in python over Fuse, that features high reliability,
    strong security properties, and a fine-grained sharing model.
    Files are encrypted, signed, erasure-coded, then distributed over
    multiple servers, such that any (configurable) subset of the
    servers will be sufficient to recover the data.<br /> There is a
    Tahoe-LAFS Debian Package.
    -   [Tahoe-LAFS Home](https://tahoe-lafs.org/trac/tahoe-lafs)


# Cluster Management

## Heartbeat and Pacemaker
__Heartbeat__ i;e; {{< wp "Linux-HA" >}} is  a high-availability clustering
solution for Linux, FreeBSD, OpenBSD, Solaris and Mac OS X.

-   [The Linux-HA User’s Guide
    ](http://www.linux-ha.org/doc/users-guide/users-guide.html)
    _2010_.


[Pacemaker](http://clusterlabs.org/pacemaker/) (GPL)
is an open source high availability resource manager.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
