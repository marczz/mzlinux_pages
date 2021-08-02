---
title: Clouds
---

See also
{{< iref "network_filesystems#distributed_filesystems" "Distributed File Systems" >}},
{{< iref "backup" "Backup" >}}.

------

# Clouds references
-   Wikipedia: {{< wp "File hosting service" >}},
    {{< wp "Comparison of file hosting services" >}},
    {{< wp "Comparison of online backup services" >}}.
-   [ArchWiki: backup - cloud storage
    ](https://wiki.archlinux.org/index.php/Synchronization_and_backup_programs#Cloud_storage),
    [list of cloud storage servers
    ](https://wiki.archlinux.org/index.php/List_of_applications#Cloud_storage_servers),
    [list of cloud synchronization clients
    ](https://wiki.archlinux.org/index.php/List_of_applications#Cloud_synchronization_clients).
-   [Backup Review](http://www.backupreview.com/) review many storage plans.
-   [appappeal: Top 40 Free File Sharing Apps](http://www.appappeal.com/apps/file-sharing)
-   Richard Stallman warn us: [Cloud computing is a trap
    ](http://www.guardian.co.uk/technology/2008/sep/29/cloud.computing.richard.stallman)
-   [Search dropbox on alternativeto
    ](http://alternativeto.net/software/dropbox/?profile=linux&platform=linux&exactmatch=true)
    for more sync server solutions.
-   Rightscale pages:
    [Cloud Storage: AWS vs Azure vs Google vs SoftLayer
    ](http://www.rightscale.com/blog/cloud-management-best-practices/cloud-storage-aws-vs-azure-vs-google-vs-softlayer),
    [How to Compare AWS vs Azure vs Google vs SoftLayer
    ](http://www.rightscale.com/blog/cloud-management-best-practices/how-compare-aws-vs-azure-vs-google-vs-softlayer)


# Amazon Web Service {#aws}
-   [Amazon Web Service Home](http://aws.amazon.com)
-   [AWS Free Usage Tier](http://aws.amazon.com/free/) allow some free
    use during one year.
    -   [Hidden Charges when using Amazon AWS' Free Tier
        ](http://mhlakhani.com/blog/2011/01/hidden-charges-aws-free-tier/)
-   [AWS monthly calculator](http://calculator.s3.amazonaws.com/calc5.html)
  - [TurnKey Hub](https://hub.turnkeylinux.org/) allow to deploy server
    apps on [Amazon EC2](http://en.wikipedia.org/wiki/Amazon_Elastic_Compute_Cloud).
-   {{< wp "Amazon S3" >}} (Wikipedia),
    [S3 Home Page](http://aws.amazon.com/s3).

## S3 clients {#s3_clients}
See also below the generic {{< iref "#cloud_frontends" "Cloud Frontends" >}}
which include  {{< iref "#cloud_vfs" "Cloud  Virtual File systems" >}}.

-   [AWS Command line interface
    ](https://aws.amazon.com/cli/)
    is a unified tool to manage AWS and  {{< iref "#eucalyptus" "Eucalyptus" >}}
    services. The [file commands](http://docs.aws.amazon.com/cli/latest/reference/s3/)
    are file and directory commands ( cp, ls, mb, mv, presign, rb, rm, sync, website )
    to manage your buckets. It is packaged in Debian as _awscli_.
-   [s3tool](http://s3tools.org/) (GPL)
    provide _s3cmd_ a command line tools for Amazon S3 to uploade, retrieve and manage
    data. It .
    -   [s3tool - GitHub](https://github.com/s3tools/s3cmd).
    -   There are three howtos: [s3cmd HowTo](http://s3tools.org/s3cmd),
        [s3cmd sync HowTo](http://s3tools.org/s3cmd-sync),
        _the operation sync allow to transfer
        only files that don’t exist at the destination_;
        [s3cmd encryption HowTo](http://s3tools.org/s3cmd-encryption).
    -   _s3cmd_ is built for S3 but it is also usable with s3 compatible object storage
        with a proper configuration file, like
        {{< iref "#scaleway_object" "scaleway object storage" >}},
        {{< iref "#minio" "Minio" >}} or
        {{< iref "#eucalyptus" "Eucalyptus" >}} like explained in
        [how to use s3cmd with an eucalyptus instance
        ](https://github.com/eucalyptus/eucalyptus/wiki/HowTo-use-s3cmd-with-Eucalyptus).
    - _s3cmd_ is packaged in Debian.
-   [s4cmd](https://github.com/bloomreach/s4cmd) (Apache Licence)
    is a python alternative to _s3cmd_ tool, enhancing performance and support for large
    files, and coming with a number of additional features and fixes.
    It also supports S3 compatible storage services such as DreamHost and Cloudian.

-   [Boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
    is the Amazon Web Services (AWS) SDK for Python.
    -   [Boto3 GitHub Repository](https://github.com/boto/boto3).
    -   _Boto3_ has [many frontends in Pypi
        ](http://pypi.python.org/pypi?%3Aaction=search&term=boto3&submit=search)
        but some are not compatible with the new _Boto3_.
-   [amazon-glacier-cmd-interface
    ](https://github.com/uskudnik/amazon-glacier-cmd-interface)
    (MIT Licence) use boto _last update 2016_. An example of use is
    [Creating Long-Term Backups with Amazon Glacier on Linux
    ](http://blog.tkassembled.com/326/creating-long-term-backups-with-amazon-glacier-on-linux/)
    by TK Kocheran.
-   [s3curl](https://github.com/rtdp/s3curl) (Apache License)
    is a perl wrapper around curl to work with s3 buckets.
    -   [Amazon S3 Authentication Tool for Curl - AWS Code
        ](https://aws.amazon.com/code/amazon-s3-authentication-tool-for-curl/)
    -   It can also be used on an {{< iref "#eucalyptus" "Eucalyptus" >}} instance.
    -   s3curl is packaged in Debian.
-   [JetS3t](https://github.com/mondain/jets3t) (Apache License)
     (pronounced "jet-set") is a Java toolkit and application suite
     for Amazon S3, Amazon CloudFront, and Google Storage.
     _JetS3t_ is packaged in Debian.
-   [DragonDisk](http://www.dragondisk.com/) (proprietary software, free linux client)
    is a file manager for Amazon S3, Google Cloud Storage, and S3 compatibles cloud
    storage services. Debian packages are provided.

## Eucalyptus {#eucalyptus}

{{< wp "Eucalyptus_(software)" "Eucalyptus" >}} (MIT Like licence) is a software for
building Amazon Web Services (AWS)-compatible private and hybrid cloud computing
environments,

-   [GitHub: eucalyptus](https://github.com/eucalyptus/eucalyptus)
-   [Eucalyptus Wiki](https://github.com/eucalyptus/eucalyptus/wiki)
    is the Home of Eucalyptus.
-   [AWS Tools compatibility · eucalyptus Wiki
    ](https://github.com/eucalyptus/eucalyptus/wiki/AWS-Tools)
-   [Euca2ools](https://github.com/eucalyptus/euca2ools)
    are command line tools used to interact with Amazon Web Services (AWS) as well as
    other services that are compatible with AWS, such as Eucalyptus.
    _euca2ools_ is packaged in Debian.
    -   [euca2ools - Debian Wiki](https://wiki.debian.org/euca2ools)

## Minio {#minio}
{{< wp "Minio" >}} (Apache Licence) is a cloud storage server written in golang
compatible with Amazon S3. A docker image is provided.

-   [Minio Home](https://min.io/).
-   [Minio - GitHub](https://github.com/minio/minio).
-   [Minio Documentation](https://docs.min.io/).
-   [MinIO Client (mc)](https://github.com/minio/mc)  (Apache Licence)
    provides a modern alternative to UNIX commands like ls, cat, cp, mirror, diff, find
    etc. It supports filesystems and Amazon S3 compatible cloud storage service.  There
    is a snapcraft package for minio client, a go binary is also available on Minio
    Home.
    -   [MinIO Client Complete Guide](https://docs.min.io/docs/minio-client-complete-guide).
        and [QuickStart Guide](https://docs.min.io/docs/minio-quickstart-guide).


# Cloud virtual filesystems
# Blackblaze B2 {#b2}
{{< wp "BlackBlaze" >}} has many products available at
[Backblaze Home](http://www.backblaze.com/)
_Personal backup_ is an online backup tool using AES encryption
([more on BlackBlaze encryption
](http://blog.backblaze.com/2008/11/12/how-to-make-strong-encryption-easy-to-use/))
$60/Year by computer for unlimited data.  No linux client, and no
open api.

Backblaze _B2 Cloud Storage_ works similar to Amazon S3 or
Microsoft Azure.


It has a very appealing price of $0.005/GB a month with 10 GB storage free, uploads are
free, Download cost 0.01$/G first G/day free, _API Calls_ $0.004 per 10,000 transactions
with 2500/day free (some transactions free). _August 2020 pricing_

Previously blackblaze had a high download price, compared to some providers like OVH
openstack the storage. But they have been cut off by two. Of course some provider offer
free download until some amount, and it should be considered, depending of your needs.

The [pricing page
](https://www.backblaze.com/b2/cloud-storage-pricing.html)
includes a cost calculator, for 1000G initial data upload, 100G/month
upload, 5G/month delete, 10G/month download, it cost 98$/year three
time less than S3 or Google cloud. If you download 200G/month 121$/year still a third of
S3. For all these examples
microsoft azure and google cloud are more expansive than S3.

For 200G initial, 10G/month upload, 7G/month delete, 10G download/month 14$/year a third
of S3, Azure, or Google cloud these Three are in the same range here 57$-67$.  _August 2020 pricing_

The {{< iref "#comparison_table" "Comparison table" >}} below also add other low costs
providers like  OVH openstack, or scaleway, compared to scaleway, under 140G scaleway is
less expensive, above 140G B2 win, but scaleway has also free internal trafic, that
could give an advantage if you have a Scaleway server.

[B2 Documentation](https://www.backblaze.com/b2/docs/)

The basics operation are done with the [command-line tool
](https://github.com/Backblaze/B2_Command_Line_Tool) which is packaged in debian
a _blackblaze-b2_, the python sdk is also packaged as _python3-b2sdk_.XS

B2 is [integrated in many softwares
](https://www.backblaze.com/b2/docs/integrations.html): [python command line tool
](https://www.backblaze.com/b2/docs/quick_command_line.html), a
[duplicity backend](https://github.com/matthewbentley/duplicity_b2), duplicati,
{{< iref "backup#duplicacy"  "duplicacy" >}},
{{< iref "backup#duplicati"  "duplicati" >}},
{{< iref "backup#hashbackup"  "HashBackup" >}},
{{< iref "backup#restic"  "Restic" >}},
{{< iref "#rclone" "Rclone" >}} ([B2 support](https://rclone.org/b2/)),
{{< iref "#opendedup" "opendedup" >}}
([B2 support](http://opendedup.org/odd/2018/04/04/backblaze-b2-enabled/)).

There is a [B2 fuse backend](https://github.com/sondree/b2_fuse) written in python.

It works with CyberDuck and it's command line {{< iref "#duck" "duck" >}}.


B2 Api is a web API like amazon S3. It was previously not compatible with S3,
but now B2 offer an
[S3 compatible API](https://www.backblaze.com/b2/docs/s3_compatible_api.htm)

# Box {#box}

[Box](http://www.box.com/)(box.com or box.net)
has  10 GB of free web-storage,
250M file size limit, some temporary promotion allow 50G free. The starter kit is 4€ * users / month for 100GB, 2GB file limit.
File sharing links, Mobile web access,
free android, iphone,  ipad application.

-   Wikipedia: {{< wp "Box.com" >}}
-   To know the current promotions follow the _promotions faq_ link
    in the [support Home Page](https://support.box.com/home)
-   Business plan 180$/year for 1TB max 2GB/file.
    Box support FTP and FTPS (not SFTP) only for Business
    and Enterprise customers.
-   Synchronization client is only available
    for windoze and Mac OS/
-   There is no linux client in the offer, but an unsupported dav
    access at <https://dav.box.com/dav/>.

    You can explore your repository with:

        $ cadaver https://dav.box.com/dav/

    or by using `gvfs`, it is easier with a frontend, many
    filemanagers use gvfs, in nautilus or pcmanfm you can open
    `davs://dav.box.com/dav`.


    If you are root mount it as a virtual fs with davfs2:

        $ sudo mount -t davfs https://dav.box.com/dav /tmp/box\
        -o uid=myuserid,gid=mygroupid,noexec

     Then it will ask for your username and password.

     You can also put in your fstab:

        https://dav.box.com/dav/ /media/box davfs noauto,user  0  0

    and mount as ordinary user with

        $ mount /media/box

    you don't need to set `uid`, `gid` that are taken as you uid, gid
    and `noexec` is implicit, but you need to belong to `davfs2`
    group.

    This method is only valid if no user will try to mount
    concurrently, because he would use the same mountpoint.
    but it has the benefit that your own options in
    `~/davfs2/conf` will be used, and you can store your password
    in `~/davfs2/secret`.

    To use box dav filesystem you should disable lock by option
    `use_locks 0` in {{< man "davfs2.conf" >}}. See also other options in
    {{< man "mount.davfs" >}}.

    A bash script is available in
    [boxdav GitHub repository](https://github.com/seecinq/boxdav).

-   [Box Developer Home](http://developers.box.com/) present the
    Box API.
-   [Box technical blog](https://tech.blog.box.com/) has  also informations for developers.
     There is an associated [Box technical blog GitHUb repository](https://github.com/box)
-   Note that the old box API V1, has been [replaced beginning 2012 with
    version 2](http://developers.blog.box.com/2012/04/25/introducing-the-v2-api/)
    and will  be [deprecated when the API V2 is generally available
    ](http://stackoverflow.com/a/10824276/965798) so the applications have to
    be updated or be obsoleted.
-   [Boxfs2](https://github.com/drotiro/boxfs2) by Domenico Rotiroti seems the more stable
     api V2 interface FUSE filesystem for box.com. There are some
     updates in the repository forks.
-   [Box Python Library: boxdotcom](https://github.com/dvska/python-boxdotcom)
    (Apache License) allow to store and retrieve files from Box.net,
    organize files into folders, move, rename and delete files, share files
    [boxdot.com is in pypi](http://pypi.python.org/pypi/boxdotcom/), _last commit 2012, old API_.
-   [BoxLinux](https://github.com/sebastiansam55/boxlinux) (GPL)
    by Sam Sebastian is a command line client with
    download/upload, and file managing (create, rename, delete
    files and folders). Synchronization is alpha. _2013_
-   [PyBoxFS (GitHub)](https://github.com/anthonybishopric/pyboxfs) (BSD like
    License) try to provides the
    [PyFilesystem](https://code.google.com/p/pyfilesystem/)
    interface for items in Box. _Last commit 2013._
    it._
-   [box-linux-sync](https://github.com/noiselabs/box-linux-sync) is a sync client for linux  using the WebDAV interface
    _alpha and last commit 2013_.

# Dropbox {#dropbox}
2GB storage free, 100$/year for 100GB
Dropbox is packaged for main linux distributions, and mobiles.

The dropbox daemon footprint is 50M res/16M shr

-   Wikipedia: {{< wp "Dropbox" >}}
-   [ArchLinux: Dropbox](https://wiki.archlinux.org/index.php/Dropbox)
-   [(Dropbox) secure remote storage using sshfs and encfs
    ](http://balau82.wordpress.com/2009/08/23/secure-remote-storage-using-sshfs-and-encfs/)
-   The dropbox daemon footprint is 50M res/16M shr
-   {{< iref "#rclone" "rclone" >}} support Dropbox.


## Dropbox API

-   [REST API Reference](https://www.dropbox.com/developers/reference/api)
-   [Dropbox SDK and documentation](https://www.dropbox.com/developers/reference/sdk)
-   [pypi: dropbox](http://pypi.python.org/pypi/dropbox/) is the
    official Dropbox REST API Client
-   [dropboxfs alias fs-dropbox](https://github.com/btimby/fs-dropbox/)
    is a file system for
    [PyFilesystem](https://code.google.com/p/pyfilesystem/)
    which uses the dropbox API. It uses the official Dropbox API for
    authentication process, and you are not required to provide
    your username/password
    [dropboxfs in pypi](http://pypi.python.org/pypi/dropboxfs/)
-   [Dropbox-Uploader](https://github.com/andreafabrizi/Dropbox-Uploader)
    (GPL) by Andrea Fabrizi Dropbox Uploader is a BASH script which
    can be used to upload, download, list or delete files from
    Dropbox.
-   [recursive-dropbox-uploader
    ](https://github.com/matzegebbe/recursive-dropbox-uploader)
    is a fork of Dropbox-Uploader that allows to download whole directories.
-   [dropbox wsgi](https://github.com/rianhunter/dropboxwsgi)
    provides a WSGI interface into the Dropbox API.
    [pypi: dropboxwsgi](http://pypi.python.org/pypi/dropboxwsgi/)

#  [Google One](https://one.google.com/) {#google_one}

Google One is the storage shared beetwen
<a name="gdrive"></a>[Google Drive](https://drive.google.com/), Google Mail, and Google
Photos.  Gmail message can have attachments as big as 10G. The free plan is of 15G.

The [Google one storages plans](https://one.google.com/storage) are _ 100GB 2€/month or
20€/year, 200G 3€/month or 30€/year, and 2TB 10€/month 100€/year. _August 2020 Pricing_

-   [Google developers: Publish Website Content
    ](https://developers.google.com/drive/publish-site)
-   [Google drive SDK](https://developers.google.com/drive/),
    [Google Drive REST API v2
    ](https://developers.google.com/drive/v2/reference/).
-   [Oauth play ground](https://developers.google.com/oauthplayground/)
    allows you to walk through each step of the OAuth 2.0 flow for
    server-side web applications: authorizing API scopes, exchanging
    authorization tokens , refreshing access tokens, and sending
    authorized requests to API endpoints.  At each step, the
    Playground displays the full HTTP requests and responses.
    -    an example is [looking for _webViewLink_ with Oauth play ground
        ](http://developinthecloud.drdobbs.com/author.asp?section_id=2409&doc_id=255477)
-   [odeke-em/drive](https://github.com/odeke-em/drive)
    is a client for google drive written in *go*.
    odeke-em/drive is [packaged in many distributions
    ](https://github.com/odeke-em/drive/blob/master/platform_packages.md)
    including Debian.
-   [Grive](https://github.com/Grive/grive) (GPL) linux go client for
    google drive. It is no longer updated since 2013.
    -   [How to Use Google Drive on Ubuntu Linux via Command Line
        ](http://www.howopensource.com/2015/01/google-drive-for-ubuntu-linux/)
        use _grive_.
-   [Grive2](https://github.com/vitalif/grive2) is the continuation of
    _Grive_, but it uses the new Drive REST API and allow partial sync.
-   [Insync](https://www.insynchq.com/linux), an unofficial _private_ Google
    Drive client for Linux.  Linux release of Insync has a cost of 15$
    for a single google account.
    -   [ArchWiki: Insync](https://wiki.archlinux.org/index.php/Insync)
    -   Insync daemon footprint is 104M res/35M shr
-   [PyDrive](https://github.com/googledrive/PyDrive)
    is a wrapper library of google-api-python-client.
    -   [PyPi: PyDrive](https://pypi.python.org/pypi/PyDrive)
    -   [PyDrive Documentation](http://pythonhosted.org/PyDrive/)
    -   [Duplicity with PyDrive backend for Google Drive
        ](https://blog.notmyhostna.me/duplicity-with-pydrive-backend-for-google-drive/).

-   [gcat](https://github.com/embr/gcat) a simple utility for grabbing
     or putting Google Drive spreadsheets.
-   [DAV-Pocket](http://dav-pocket.appspot.com/)
     allow free WebDAV access to Google Drive

         $ mount -t davfs https://dav-pocket.appspot.com/docso/ /media/gdrive/
-   {{< iref "#rclone" "rclone" >}} support Google Drive.

# [Mega](https://mega.co.nz/) {#mega}

This new-zealand company offer 50GB
free, linux desktop sync client, android and iphone apps, a chrome and
firefox extension. The paid plans are from 5€/month 400GB data, transfer 1TB  , 10€/month
2TB data, transfer 2TB, 20€/month data 8TB transfer 8TB, 30€/month 16TB data transfer 16TB.
_August 2020 pricing_

There is an official SDK and clients built upon the SDK:

-   [MEGA SDK - Client Access Engine](https://github.com/meganz/sdk)
    is a new SDK in C++; it provides two command line tools
    _megacli_  that allows to use all SDK features and
    _megasimplesync_ to use the synchronization engine; and some
    example apps. It is a very active project _in 2017_.
-   <a name="megacmd">[MEGAcmd](https://github.com/meganz/MEGAcmd)
    is a CLI built upon the SDK it features one server
    _MEGAcmdServer_, a ftp like interactive shell _MEGAcmdShell_ and
    several commands that will launch the non-interactive client
    _MEGAcmdClient_. The interactive shell offer the usual commands we
    find in ftp: ls, cd, lcd, pwd, lpwd, mkdir, rmdir, put, get,
    .... and more like find, disk usage, a command to sync a local and
    remote folder, manage global exclude patterns for sync....
-   <a name="megasync"></a>[MEGAsync](https://mega.nz/sync)
    is an official sync GUI client for mega, built upon the SDK. There
    are windoze, mac and linux binaries. The megasync binary memory
    footprints on an amd64 is 90M resident / 20M shared when doing a
    big sync (10G) which is reasonable for a synchronization program.

    Megasync does not do anyfile versionning but keeps in a folder
    clouds deleted files, and local overwritten files.

    -   [MEGAsync Help
        ](https://mega.nz/help/client/megasync/)
    -   [GitHub - MEGAsync](https://github.com/meganz/MEGAsync)

There are also some third party tools:


-   [Megatools - command line client for Mega.co.nz
    ](http://megatools.megous.com/)
    Megatools is a collection of programs for accessing Mega from
    command line.  Megatools allow you to copy individual files as
    well as entire directory trees to and from the cloud. You can also
    perform streaming downloads without needing to download the entire
    file.<br/>
    Megatools is active _in 2017_ and in Debian.
-   [go-mega (GitHub)
    ](https://github.com/t3rm1n4l/go-mega) is a client library in go.
    It was providing the now unmaintained
    [mega-cmd](https://github.com/t3rm1n4l/megacmd)
    which features a ftp like interface, plus some extensions.
    Now you can use the official
    {{< iref "#megacmd" "MEGAcmd" >}}
-   [Mega.py (GitHub)](https://github.com/ckornacker/mega.py)
    is a Python library for the Mega.co.nz API, currently supporting,
    login, uploading, downloading, deleting, searching,
    sharing, renaming, moving files.<br/>
    mega.py is in the [PPA named backup for Christian Kornacker
    ](https://code.launchpad.net/~ckornacker/+archive/ubuntu/backup).
    It is used  duplicity to backup on mega.co.nz.
    It is no longer updated since 2013 and is now obsolete.
-   [MegaFuse](https://github.com/matteoserva/MegaFuse)
    mount your Mega drive as a fuse fs. It is not actively maintained,
    and not very robust. I experienced occasional crashes.

    -   [Offsite Linux backup to Mega with duplicity
        ](http://itnerd.space/2016/10/26/offsite-backup-with-duplicity-and-mega/),
        use a docker image to install duplicity and mega_fuse.
-   {{< iref "#rclone" "rclone" >}} support Mega.

# Openstack {#openstack}

-   Wikipedia: {{< wp "OpenStack" >}} (Apache License) is a cloud computing
    project to provide an infrastructure as a service (IaaS).
-   [OpenStack Fondation](http://www.openstack.org/foundation/)
    [GitHub: OpenStack](https://github.com/openstack)
-   [Pyrax](https://developer.rackspace.com/sdks/python/)
    the official SDK for openstack clouds. It is hosted in the
    [OpenStack rackspace SDK](https://developer.rackspace.com/).
    -   [GitHub Pyrax](https://github.com/rackspace/pyrax)
-   Swift is the Openstack object storage
    [Swift’s documentation](http://docs.openstack.org/developer/swift/)
    [GitHub: OpenStack Swift](https://github.com/openstack/swift)
-   [Debian: OpenStack HOwto](http://wiki.debian.org/OpenStackHowto):
    [Openstack-Compute (aka Nova) environment (Essex)
    ](https://wiki.debian.org/OpenStackHowto/Essex),
    [Openstack Folsom](http://wiki.debian.org/OpenStackHowto/Folsom)
-   [OpenStackClient
    ](http://docs.openstack.org/developer/python-openstackclient/)
    is a command-line client for OpenStack
    that brings the command set for Compute, Identity, Image, Object
    Storage and Volume APIs together in a single shell with a uniform
    command structure.
    It is provided by the Debian package _python-openstackclient_.
-   [openstack/python-swiftclient
    ](https://github.com/openstack/python-swiftclient)
    _python-swiftclient is in Debian_.
-   [ftp-clouds](https://github.com/cloudfs/ftp-cloudfs)
    is an FTP interface to Swift the OpenStack Object Storage,
    i.e a ftp server acting as a proxy to OpenStack Object Storage
    (swift). It allow you to connect via any FTP client to do
    upload/download or create containers.
    It is in Debian.

    It is also used for [Sftp Cloudfs](https://github.com/Memset/sftpcloudfs).
-   [OpenStack Swift on Raspberry Pi
    ](http://programmerthoughts.com/openstack/swift-on-pi/)
-   [Swift Explorer](http://www.619.io/swift-explorer) (Apache License)
    is a java software.
    -   [swift explorer - GitHub](https://github.com/roikku/swift-explorer).

## Openstack storage providers
-   Openstack is underlying technology for {{< wp "Rackspace" >}} Cloud Servers. They
    provide [openstack object storage](https://www.rackspace.com/cloud/files)
    at the price of 0.095€/G x month with trafic at 0.10€/GB _2017 first TB storage and
    10T traffic_ so for 100G storage and 100G traffic ~ 20€/month.  _seems very
    expensive compared to OVH_.
-   <a name="ovh_openstack">{{< wp "OVH" >}} provides [openstack/swift object storage
    ](https://www.ovh.com/fr/public-cloud/storage/object-storage/)
    at the price of 0.0112€ G/month inbound traffic free, outbound
    traffic 0.011€/G _08/2020_ _If you use for backup you have few
    outbound traffic, if you use it for distributing content you might
    have an heavy outbound traffic_
    Ovh has [documentation on object storage management
    ](https://www.ovh.com/fr/public-cloud/storage/object-storage/).

    OVH provides also cold storage for archiving, retrieving you data
    can take up to few hours.  The price of cold storage is
    0.0023€/ GB-month, with inbound and outbound traffic at 0.011€ G that
    makes storing 100G at 0.230/month + traffic _08/2020_.  In addition to
    openstack/swift API OVH offers SFTP, Rsync, SCP, HTTPS access to
    the storage.


# [Owncloud](http://owncloud.org/) {#owncloud}

-   [OwnCloud Blog](http://owncloudtest.blogspot.com/)
-   [OwnCloud Documentation](http://doc.owncloud.org/):
    [User Manual](http://doc.owncloud.org/server/8.0/user_manual/),
    [Administrator Manual
    ](http://doc.owncloud.org/server/8.0/admin_manual/),
    [ownCloud Desktop Client Manual
    ](http://doc.owncloud.org/desktop/1.7/)
-   [pyOwnCloud](https://github.com/csawyerYumaed/pyOwnCloud)
    ownCloud CLI client written in python
-   Owncloud hosting
    -   [OwnCube](https://owncube.com/)
        has support for owncloud it offers plans beginning
        18€/year for 25GB, 60€ 1000GB, more until 20 TerraBytes.
-    [Owncloud](http://owncloud.org/index.php/Main_Page)
     has a webdav access
     You can access webdav with cadaver with the following syntax

        cadaver http://nas/owncloud/files/webdav.php

## Nextcloud
Nextcloud is a fork of owncloud

-   [Nextcloud](https://nextcloud.com/)
-   [nextcloud/server · GitHub](https://github.com/nextcloud/)

-   [OwnDrive](https://owndrive.com/)
    run nextcloud. There is free 1GB account
    with support for Calendar, Contacts, Bookmarks, Tasks and Notes;
    2€/month with more applications and 5GB 4€/25GB, 7€/month for your own
    cloud and 10GB. It allows to add external storage from many
    providers S3, Openstack, ...

## Cozy
[Cozy](https://cozy.io/fr/) is a self hosted cloud, it runs
a node.js daemons on top of CouchDB. It can be used on your own
server, even a Raspberrypi, with a minimum Ram of 1GB, or on a
Dedicated or Virtual Private Server. It supports many services, a
Files manager with synchronization, email, contact, photo gallery, a
music player, an IRC client, a task manager ....

There is a Docker image for cosy.

Cozy is a personal server, there are no user and account management.

-   [ArchWiki: Cozy](https://wiki.archlinux.org/index.php/Cozy).

# Rsync.net
[Rsync.net](http://www.rsync.net/) offer cloud storage on an Unix
platform with ZFS file systems and an SSH access. The standard offer
with 7 daily snapshots until 1TB 0.08$/ G x month, between 1T and 4T
0.06$/G x month, and over 10 T 0.04$/G x month. So 100G cost 96$/year.

As _Rsync.net_ is ssh based it can be used with
rsync, sftp, scp, sshfs, duplicity, rdiff-backup, unison git, git-annex,
subversion, or anything that could be piped to ssh.


There is also an offer for [Attic or Borg backup
](http://www.rsync.net/products/attic.html). It is without snapshots
since history is handled by Attic / Borg and the cost is 3$ G x month
begining at 25G. So our example 100G plan is 36$/year. _2017 prices_

### Scaleway Object storage {#scaleway_object}

{{< iref "#scaleway" "Scaleway" >}} provides S3 compatible object storage.
-   [S3-Compatible Object Storage](https://www.scaleway.com/en/object-storage/)
    is free for first 75GB and 0,01 € per GB up to 500GB.

    Incomming trafic _internal and external_ as Internal outgoing traffic to other
    Elements products in the same region is free, external outgoing trafic is free for
    first 75GB from 75GB to 500GB 0.01 € per GB/month.
-   [C14 Cold Storage](https://www.scaleway.com/en/c14-cold-storage/)
    75 GB is free then €0.002/GB/month. Archiving and recovering from C14 Cold
    Storage’s Glacier class to Object Storage’s Standard class is free of charge.


Most [S3 operations are supported
](https://www.scaleway.com/en/faq/object-storage/#-Which-S3-operations-are-supported)
and most tools usable with S3 like _s3cmd_, _aws-cli_, _s3fs_, _cyberduck_ ... are also
usable with Scaleway object storage. The are referenced in the
[object storage page](https://www.scaleway.com/en/object-storage/).

# Seafile
[Seafile (GitHub)](https://github.com/haiwen/seafile) (GPL)
is an open source replacement for Dropbox.
It provides a server that build on Linux, and clients for many OS.

-   [Seafile.com Home Page](http://seafile.com/en/home/).

# Wasabi {#wasabi}
Is a cloud block storage S3 compatible. The minimum plan is 1TB. And it applies an
uniform cost of 5.90$/TB/Month -August 2020 Pricing_, with free in and out trafic, and
free api calls.

# Yandex.Disk

[Yandex.Disk](http://disk.yandex.com/) gives 10GB free, 100G 20$year,
1T 100$/year _2017_.

There is a linux client allowing synchronization as well as Mac OS,
windows, android, iphone clients.

-   Wikipedia: {{< wp "Yandex Disk" >}}
-   Yandex allow webdav access, that you can use with davfs:

        $ mount -t davfs https://webdav.yandex.ru /tmp/yandex_disk

-   Yandex has a simple [http API
    ](http://api.yandex.com/disk/doc/dg/concepts/api-methods.xml)
-   [ypload](https://github.com/bobuk/ypload)
    is a python script to upload to yandex.
    [ypload on pypi](http://pypi.python.org/pypi/ypload/)


# Other clouds

-   {{< wp "Adrive" >}} (Wikipedia) it has only a web interface, in java, and
    Linux compatible.  ADrive offers 50 GiB of free data storage but
    with adds and Marketing Emails. The premium feature 100GB of
    storage cost $25 per year _2017_ provides Webdav SCP, SFTP and
    Rsync,file versionning and encryption.  The Data is not encrypted.

    -   [Adrive Home](http://www.adrive.com/) and
        [Adrive storage plans
        ](http://www.adrive.com/static/storageplans_overview)

-   <a name="azure_blob">[Microsoft Azure Blob storage
    ](https://azure.microsoft.com/en-us/pricing/details/storage/blobs/)
    has blob storage _hot_ at a price going fro 0.0184$/GBxmonth to
    0.021$ depending of the region. The downloads are free, and the
    API as a cost (see their calculator). These price are for local
    redundancy, they grow to 0.04$ if you want your data replicated in
    different regions. There is also _cool_ storage at 0.01$/GBxmonth,
    but here the downloads are also 0.01$/Gb and upload 0.0025$/Gb.
    -   [Pricing calculator
        ](https://azure.microsoft.com/en-us/pricing/calculator/?service=managed-disks).
-   [BarracudaDrive](http://barracudaserver.com/products/BarracudaDrive/)
    self hosted cloud on private server or
    [low end box](http://www.lowendbox.com/).
-   [Amazon Cloud Drive](http://www.amazon.com/clouddrive)
    5 GiB of free storage, unlimited photos,  2 GiB file size limit.
    No linux client. Unlimited storage for 60$/year.
    -   [acd fuse](https://github.com/handyman5/acd_fuse) is a fuse
        client for Amazon Cloud Drive built on the top of
        [PyAmazonCloudDrive (pyacd)
        ](http://code.google.com/p/pyamazonclouddrive/)

-   [CloudFlare](https://www.cloudflare.com) is a content delivery
    network (CDN) It has
    [Free plans](https://www.cloudflare.com/plans/)
    with a max client upload of 100MB.
-   [CloudMe](http://www.cloudme.com/en)
    3GB free with an upload Limit of 150MB / File, 10€/year 10G
    40€/year 25G, 80€/year 100GB, 140€/year 200G _2017_. It has an
    [CloudMe android App](http://www.cloudme.com/en/features/mobile/android),
    is also accessible from web as any of these solutions, with also
    an [interface for mobiles](http://cloudme.com/m), and has also a
    [WebDav option](https://www.cloudme.com/en/webdav)
-   [CloudWatt](https://www.cloudwatt.com/fr/)
    is a storage solution based on
    {{< iref "#openstack" "OpenStack" >}}
    It has storage plan free
    until 50G 10G trafic, 100G 26€/year, 1To 260€year; trafic
    1.4€/To _2017_.
    -   [Comment débuter avec CloudWatt
        ](http://support.cloudwatt.com/debuter/index.html).
    -   [configurer Duplicity avec le stockage objet de Cloudwatt
        ](https://support.cloudwatt.com/kb/faq/stockage-objet/configurer-duplicity.html)
-   [HiDrive](https://www.free-hidrive.com/)
    offer 5G free with webdav, ios and android app 100G 72€/year with
    webdav, smb, sftp, rsync over ssh, scp _2017_.
-   [Minus.com](http://minus.com/) had 10 GiB of free
    files are arranged in folders or *Gallery*, Now they have changed
    their focus and are competing with instagram and social
    networks. The plans and pricing are not on their home page, and I
    have not investigated further.
-   [MyDrive](https://www.mydrive.ch/) is a swiss company, that offer
    a webdav access, there is a free plan of 2G, They also offer a web
    online storage of 100M free.
-   <a name="onedrive"></a>[OneDrive](https://onedrive.live.com/)
    previously SkyDrive is a Microsoft cloud hosting.  It offers 15 GB
    of free storage. There is no built-in encryption, of course no
    linux client!  For a longer description look at Wikipedia
    {{< wp "OneDrive" >}}.
    -   [official OneDrive SDK for Python
        ](https://github.com/OneDrive/onedrive-sdk-python)
    -   [bash-onedrive-upload
        ](https://github.com/fkalis/bash-onedrive-upload)
        is a bash command line client to use the REST API to upload
        files.
    -   [onedrive-d
        ](https://github.com/xybu/onedrive-d-old)
        is a Microsoft OneDrive client on Linux platforms. It allows
        to sync with one or more OneDrive Personal account by
        synchronizing each remote OneDrive repository with a
        local directory. _It is now unmaintained_.
    -   [skillion/onedrive](https://github.com/skilion/onedrive) (GPL)
        a client written in D to sync with onedrive. It is packaged in
        Debian as _onedrive_ since _stretch_.
    -   {{< iref "#sme" "SME" >}} allows access to one drive.

-   [SpiderOak](https://spideroak.com/):
    [SpiderOak One](https://spideroak.com/one/) 150GB 69$/year, 400GB 115/year, 2TB
    149$/year _2020_
    [SpiderOak Android](http://www.appbrain.com/app/spideroak/com.spideroak.android)
    SpiderOak deamon _headless_ is 33M/5M shr, and with panel even
    minimized you add 66M/19M
-   [Storegate](http://www.storegate.com/)
    consumer plan is 24$/year 25G for mobile backup with Android app,
    72€/year 50G for computer backup _2017_. webdav, ftp, and sync are
    for the business plans.
-   [SugarSync](https://www.sugarsync.com/):
    [SugarSync vs Dropbox : The Alternative You Never Asked For
    ](http://www.groovypost.com/howto/review/sugarsync-vs-dropbox-alternative-you-never-asked-for/)
    The plans begin at 100GB 90$/year _2017_
    __There is no Linux support and the unofficial client have been
    abandoned.
    -   The [SugarSync: Sync server comparison
        ](https://www.sugarsync.com/sync_comparison.html)
        gives some feature comparison of main solutions.
    -   [ArchWiki: SugarSync](https://wiki.archlinux.org/index.php/SugarSync)
        explains how to use SugarSync with wine.

# Cloud frontends {#cloud_frontends}
See also the  {{< iref "#s3_clients" "S3 specific clients" >}}, that can be used with S3
compatible clouds or through a proxy like {{< iref "#s3proxy" "S3Proxy" >}}.

## Virtual File systems {#cloud_vfs}
-   [S3QL](https://github.com/s3ql/s3ql/) (GPL)
    is a file system that stores all its data online using storage
    services  like  Google  Storage,   Amazon  S3 and S3 compatible,  OpenStack,
    Blackblaze B2, local filesystem.

    S3QL offers all posix features of a local file system, it supports hardlinks,
    symlinks, standard unix permissions, extended attributes.

    _S3QL_ deduplicate and compress data, it allows an optional AES encryption,
    It allows Copy-on-Write/Snapshotting.

    _S3QL_ is packaged in Debian.
    -   [S3QL User’s Guide](http://www.rath.org/s3ql-docs/index.html)
    -   [s3ql Wiki](https://github.com/s3ql/s3ql/wiki) includes
        a comparison of S3QL and other S3 file systems.
-   [s3fs](https://github.com/s3fs-fuse/s3fs-fuse) (GPL)
    is a C++ software which allows Linux and macOS to mount an S3 bucket via FUSE. s3fs
    preserves the native object format for files. It is also compatible with Google
    Cloud Storage, and other S3-based object stores. _S3Fs_ is packaged in Debian.
    -   [PyFilesystem](https://docs.pyfilesystem.org/) (BSD License) is a Python module
        that provides a simplified common interface to many types of filesystem, like
        FTPfs, WebdavFs, tarFs, ZipFs,... including
        [support for f3fs](https://www.pyfilesystem.org/page/s3fs/)
-   [YAS3FS](https://github.com/danilop/yas3fs) (MIT Licence)
    (Yet Another S3-backed File System) is a Filesystem in Userspace (FUSE) interface
    to Amazon S3. It is a rewritting in python of s3fs which add a distributed cache
    synchronized by Amazon SNS notifications. A web console is provided to easily
    monitor the nodes of a cluster.
-   [goofys](https://github.com/kahing/goofys) (Apache License)
    similar to s3fs but written in go, better performance, and less POSIX compiliance.
    it works with Ceph (ex: Digital Ocean Spaces, DreamObjects, gridscale), EMC Atmos
    Google Cloud Storage, OpenStack Swift, {{< iref "#s3proxy" "S3Proxy" >}},
    {{< iref "#Minio" "Minio" >}} (limited),  Wasabi, Azure.
-   [s3backer](http://code.google.com/p/s3backer/) (GPL)
    is a filesystem that contains a single file backed by Amazon S3.
    The blocks of the file are stored as S3 objects.
    It provides a single normal file having a fixed size which is
    used to mount a loopback device then s3backer acts a virtual hard disk device.
    _S3backer_ is packaged in Debian.
-   <a name="s3proxy"></a>[s3proxy](https://github.com/gaul/s3proxy) (Apache License)
    is a Java software that provides S3 API and proxies requests, from S3 to Backblaze
    B2, EMC Atmos, Google Cloud, Microsoft Azure, and OpenStack Swift, and on-disk
    storage filesystem.  It can be used with the others S3 tools.
    There is a Docker image, or it can be used directly with java.


### OpenDedup – SDFS {#opendedup}
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


### Rclone {#rclone}

[Rclone](http://rclone.org/)
is a command line program to sync files and directories to and from
Amazon Drive, Amazon S3, Backblaze B2, Box, Ceph, Citrix share files, DigitalOcean
Spaces, Dreamhost, Dropbox, GetSky, Google Drive, Google Cloud Storage, Google Photos,
Hubic, Jottacloud, IBM COS S3, Kiifr, Mail.ru cloud, Memset Memstore, Mega, Memory,
Microsoft Azure, Microsoft OneDrive, {{< iref "#Minio" "Minio" >}}, NextCloud, OVH, OpenDrive, Openstack Swift,
Oracle Cloud Storage, ownCloud, pCloud, premiumize.me, put.io, QingStor, Rackspace cloud
files, Scaleway, StackPath, SugarSync Wasabi, Yandex Disk, HTTP (read only), FTP, SFTP,
WebDav, the local filesystem.

Features:  MD5SUMs checking, preserve timestamps, partial syncs,
Copy mode to just copy new/changed files, full sync including beetween
two cloud instances. See the
[Overview of cloud storage systems](https://rclone.org/overview/)
for features supported by each storage provider.

It allows to encrypts and decrypts a remote with the [Crypt backend
](https://rclone.org/crypt/), we should check that the corresponding config file is
encrypted as the password is stored in config.

It allows all files operation, smb, webdav, http, ftp, sftp servers and FUSE mount of
the providers. Rclone is in Debian.

-   The documentation is available inline at the [Rclone Home](https://rclone.org/).
-   [GitHub Rclone](https://github.com/ncw/rclone).
-   [Rclone Wiki](https://github.com/rclone/rclone/wiki)
-   [Third Party Integrations with rclone
    ](https://github.com/rclone/rclone/wiki/Third-Party-Integrations-with-rclone)
-   _Rclone_ itself allow only one way synchronization, there are several python
    applications that provide bidirectional synchronisation with _Rclone_:
    [rclonesync-V2](https://github.com/cjnaz/rclonesync-V2),
    [rsinc](https://github.com/ConorWilliams/rsinc),
    [PyFiSync](https://github.com/Jwink3101/PyFiSync).
-   _Rclone_ is supported by _emacs tramp_ since version 2.4.1.

## Command Line, ftp, dav clients
### Duck
<a name="duck"></a>[Duck the Cyberduck command line tool
](https://trac.cyberduck.io/wiki/help/en/howto/cli)
is available for Mac, Windows & Linux. A Deb repository is
available. It supports the following protocols:
ftp, ftps, sftp, WebDAV (HTTP/SSL), Swift, Amazon S3, Backblaze B2,
Google Cloud Storage, Windows Azure Storage, Rackspace Cloud Files,
iPlant Data Store. The desktop UI CyberDuck, and the virtual fs MountainDuck are
available only on windows and Mac OSX. But there are alternatives for Linux like
{{< iref "#rclone" >}}


### sme {#sme}

[Sme alias Storage Made Easy](http://storagemadeeasy.com/)
allow to use WebDav and ftp above clouds, inclusind S3, with their
CloudDav solution. The free plan is 5 GB free storage on Amazon
S3, 2GB bandwidth limit per month, and access to 3 clouds.  For
40$ lifetime you are free from bandwith restriction, and get 20
clouds  and with 60$ lifetime you also get FTP access.
There is a free Linux and
[android tool](http://storagemadeeasy.com/?p=static&page=Android).

-   [sme Wiki](https://eu.storagemadeeasy.com/wiki/) and
    [sme faq](https://eu.storagemadeeasy.com/faq/)
-   Sme can integrate the following cloud providers: Amazon S3 and S3
    compliant Clouds such as (Eucalyptus Walrus), Alfresco, Atmos,
    Azure Blob Storage, BaseCamp SaaS Service, Box.net, Caringo, Ceph,
    cifs, cleversaft, Cloudian, CloudMe, Dell Elastic cloud storage,
    DropBox, Email-as-a-Cloud, Egnyte, EMC Atmos, Evernote,
    FilesAnywhere (WebDav enabled), Glasscube, Google Docs, Google
    Drive, Google Storage, Google Sites, HP Object Cloud Storage,
    HostingSolutions.it, Gmail-as-a-Cloud, HP Cloud, HP Elion, HPSS,
    Hudle,IBM Bluemix,IBM cloud object storage,IBM File Clouds, iCloud
    Drive, Igneous, iKeepinCloud, IBM Connections Files, Jive,
    Leonovus, Memset Memstore, Mezeo, {{< iref "#Minio" "Minio" >}}, Mirantis, Microsoft
    OneDrive, Microsoft Office365, Microsoft Sharepoint, OpenIO, Open
    S3, OpenStack Swift, Oracle, PogoPlug, RackSpace Cloud Files,
    Salesforce, Scality, Softlayer, SugarSync, Swiftstack,
    Thinkon,Trend Micro, Wasabi, Zimbra Briefcase, and any WebDav
    enabled Cloud.
-   They propose access though
    [FTP](http://www.smestorage.com/wiki/cloudftp) and
    [webdav](http://www.smestorage.com/wiki/clouddav), your files are
    also shared by URL.
-   [The linux cloud tool package
    ](http://eu.storagemadeeasy.com/wiki/linuxcloudtools/)
     contains the clients, wich provide a qt interface. They are:
     -  _smeclient_ mount a virtual folder,  its footprint is  16M with 13M shared
        it launch the true workhorse wich is smemount a fuse client the daemon footprint
        is 18M/2M shared  a lot smaller that many cloud applications. After mounting the
        fuse filesystem you can exit the graphical client and use it again to unmount or
        use a simpler `fusermount -u`
     -  _smeexplorer_ is a cloud browser with similar features than the web file manager,
        footprint: 43M/17M shared
     - _smesynccenter_ The synchronization manager footprint: 38M/15M shared

## Cloud abstract interface libraries
-   [Apache libcloud](http://libcloud.apache.org/) (apache licence)
    is a Python library for interacting with 30 cloud
    service providers using a unified API. It supports AWS, Google
    cloud,  {{< iref "#eucalyptus" "Eucalyptus" >}}, rackspace, openstack, and many more.

### pkgcloud
[pkgcloud](https://github.com/pkgcloud/pkgcloud/)
is a standard library for node.js that abstracts away differences among multiple cloud
providers.  It support the following services: Compute, Storage, Database, DNS, Block
Storage, Load Balancers, Network, Orchestration, CDN.

The supported clouds storage APi are: Amazon, Azure, DigitalOcean, Google, HP,
Openstack, Rackspace.

The supported Databases are  Azure, Rackspace.


-   [multer · GitHub](https://github.com/expressjs/multer/) (MIT License)
    Multer is a node.js middleware for handling multipart/form-data, which is primarily
    used for uploading files.
-   [multer-storage-pkgcloud](https://github.com/dustin-H/multer-storage-pkgcloud)
    (MIT License) is a multer storage plugin to upload files into a from pkgcloud
    supported cloud object storage.
-   [skipper](https://github.com/balderdashy/skipper) ) (MIT License)
    makes it easy to implement streaming file uploads to disk, S3, gridfs, or any
    supported file upload adapters, it is used in [Sails ](http://sailsjs.com/) MVC
    framework for Node.js,
-   [skipper-pkgcloud ](https://github.com/urielaero/skipper-pkgcloud)  (MIT License)
    is a pkgCloud adapter for receiving object-mode Readable stream from skipper.

## Other frontends
-   [Otixo](http://otixo.com/) allow access to 30 services including Dropbox,
    Box, OneDrive, Google Drive, SugarSync, Amazon S3, Mega, Yandex.
    A free account allow 35 clouds and mobile and desktop
    applications, 2GB monthly data transfer, 10$/year you have 5GB
    monthly data transfer and a __webdav access__, other plans for 25GB or
    50GB traffic. _2017_
-   [MultiCloud](https://www.multcloud.com/)
    is a provider that offers to link many clouds, and allow transfer
    and synchronisation between clouds.

    It support Dropebox, Dropebox for business, Onedrive, Onedrive for
    business, Google Drive, Sugarsync, Cloudme, Amazon, Copy, Cubby,
    Mydrive, WEB.DE, Yandex, HiDrive, Baidu, MediaFire, OwnCloud,
    Afresco, ADrive, Flickr, Hubic, Evernote, Mega, Box, Amazon S3,
    Egnyte, Pcloud, Mysql, Webdav, (S)FTP.

    File transfer are down from their server, so they can be done
    offline for your own computer. You can sync files in a certain
    folder from one cloud to another.

    There is a free plan with a limit of 2TB traffic, a paid plan at
    70$/year, allow unlimited traffic, filters for file selection and
    to schedule cloud sync or cloud to cloud backup at a regular
    interval.

# Cloud servers on demands
-   [servermom: recommended vps
    ](http://www.servermom.org/recommended-vps/)
-   [Top 10+ Alternative to Linode Cloud VPS
    ](http://webhostingegg.com/vps/top-alternative-linode-cloud-vps/)
    _april 2016._

-   [1and1.fr](http://www.1and1.fr)
    cloud server 1G ram 50G ssd 12€/month, virtual cloud server 512K
    ram 30G SSD  6€/month, 1G ram, 50G SSD 12€/month , 2 cpu  2G ram,
    80G SSD 18€/month; all plans unlimited traffic _2017_.
-   <a name="digital_ocean">[Digital Ocean
    ](https://www.digitalocean.com/)
    cloud hosting.  Pricing plans start
    at $5/month  for 512MB of RAM, 20GB SSD, 1 CPU, and 1TB
    Transfer or $10/month for 1GB RAM, 30GB SSD, 1 CPU, and 2TB
    Transfer. For added SSD 100G for 10$/month _2017_.
    Each box comes with full root access, a choice of Linux
    distributions, and the ability to customize the setup.
    -   [How To Use the GitLab One-Click Install Image
        ](https://www.digitalocean.com/community/tutorials/how-to-use-the-gitlab-one-click-install-image-to-manage-git-repositories).
    -   [DigitalOcean - a review and comparison
        ](https://ochronus.com/digitalocean-review-comparison/)
        is favorable to digitalocean, while
    -   [Five reasons why you shouldn't choose Digital Ocean for your next project
        ](http://www.redbottledesign.com/blog/five-reasons-why-you-shouldnt-choose-digital-ocean-your-next-project)
        is very reluctant.
-   <a name="ovh_vps"></a>[OVH](https://www.ovh.com/) :
    -   [vps ssd](https://www.ovh.com/fr/vps/vps-ssd.xml)
        2G ram, 10G SSD disk raid 10 3.6€/month; 4G ram 20G SSD 7.2€/month,
        SSD suplementary storage 50G 6€/month ; _2017_
    -   [vps cloud](https://www.ovh.com/fr/vps/vps-cloudxml)
        KVM OpenStack 1v core 2G ram, 25G SSD disk, CEPH, 10€/month; 2
        v cores 4GB RAM, 50GB SSD, CEPH, 20€/month _2017_
    -   [kimsufi](https://www.kimsufi.com/fr/serveurs.xml)
        _from 2017 and still in october 2019 the lower priced plans where not available,
        did they intend to continue this offer?_;
        en serveur dédié _in october 2019_:
        -   KS-1 atom 1 core 4.80€/month 2G ram 500G disk
            illimité net.
       -    KS-2 2cores 6€/month 4G ram 1TB disk, with 2TB 9.60€/month, raid 2x2TB
           16.80€/month.
    -   [Serveurs de stockages "So you Start"
        ](https://www.soyoustart.com/fr/serveurs-stockage).
        -   ARM2T armv7  cortex A9 2G ram 2TB disk,  network 2.5Gbps, 6€/month; with 4TB
            10.80€/month; 6TB 16.80€
-   [Linode](https://www.linode.com/)
    1CPU, 1GB ram, 20GB ssd, 1TB transfer, 5$/month, optional backup 2$/month;
    1CPU, 2GB ram, 30GB ssd, 2TB transfer, 10$/month, optional backup 3$/month
-   [Vultr](https://www.vultr.com/) is a cheaper clone of
    DigitalOcean.
    768M + 1Terra bandwith + 15G SSD or 160G sata 60$/year. _2017_
    You can add SSD block storage: 10G for 1$/month.

## [Scaleway](https://www.scaleway.com/) {#scaleway}
-    __pricing__: cloud hosting _DEV1-S_ 200 Mbit/s starting at 5€/month for 2GB, 2
    vCPUs, 20 GB 200 Mbit/s. Additional block storage 5,000 IOPS: 0.08€/GB-month (i.e
    50GB €/GB month).
    A snapshot is €0.00004 /GB-hour or  €0.02 per GB--month, so a 20GB snapshot is
    0.4€/month.

    _August 2020 pricing_

    Reserved IP will be billed €0.002/hr per IP.

    See {{< iref "#scaleway_object" "above for object storage" >}}.

-   [Tutorials and documentations
    ](https://www.scaleway.com/docs/)
-   [Scaleway control panel](https://cloud.scaleway.com/#/login)
-   [Network](https://www.scaleway.com/faq/servers/network/)
    -   [Native IPv6 Connectivity on Scaleway
        ](https://blog.online.net/2016/03/31/introducing-native-ipv6-connectivity-on-scaleway/).
-   [Image Hub](https://www.scaleway.com/imagehub/)
-   [GitHub - Scaleway](https://github.com/scaleway)
    -   [scaleway-cli](https://github.com/scaleway/scaleway-cli)
         a tool to pilot your Scaleway infrastructure from your terminal.
    -   [python-scaleway](https://github.com/scaleway/python-scaleway)
-   [How to create an image from scratch
    ](https://www.scaleway.com/docs/create-an-image-from-scratch/)



# Comparison of storage plans {#comparison_table}

I take two case studies for low storage need: 200G of storage, stable,
first case you mainly store and want to download very rarely, except
the downloads implied by the backup software. 20G download per month;
the second case you download more, for the case of you either share the data, and it is
dowloaded multiple time, or you want to check your backup,
as you cannot compute hash remotely, you need to download the data; I consider
200G download per month. All the price here  and computed by month are
approximatives, they vary depending on the region, and what is shown is
the lower rate. I have not computed the API fees, because I don't know
how to estimate the request numbers, and you have to add it when
appropriate.

_This listing is unfair for providers thet only have plans at fixed levels, as it use
only a fraction of what you paid, for Mega for 200G, I take a price that is valid until
400G, for Wasabi aprice allowing 1T.


| provider        |            storage/GB | download&nbsp; |  API fees&nbsp; |     200/20&nbsp; | 200/200 | checked |
|-----------------|----------------------:|---------------:|:---------------:|-----------------:|--------:|--------:|
| [BlackBlaze B2] |       (>10G)  0.005 $ |   (>~20G) 0.01 | yes             |            0.95$ |   2.75$ |   08/20 |
| [OVH openstack] |               0.0112$ |          0.011 | no              |            2.46€ |   4.44€ |   08/20 |
| [Digital Ocean] |   (mini 250G) 0.02  $ |     (>1T) 0.01 | no              |            5.00$ |   5.00$ |    3/17 |
| [Wasabi]        |     (mini 1T) $.0059$ |           free | no              |  (1T mini) 6.00$ |   6.00$ |   08/20 |
| [Amazon S3]     |               0.023 $ |           0.09 | yes             |            6.40$ |  22.60$ |    3/17 |
| [Azure]         |               0.0184$ |           free | yes             |            3.68$ |   3.68$ |    3/17 |
| [OneDrive]      |        (<1T)  0.04  $ |           free | no              |            5.83$ |   5.83$ |    3/17 |
| -               |         (1T)  0.006 $ |           free | no              |                  |         |         |
| [Google One]    |       (200G)  0.015 € |           free | no              |            3.00€ |   3.00€ |   08/20 |
| -               |         (2T)  0.005 € |           free | no              |                  |         |         |
| [Mega]          |       (400G)  0.0125€ |     (<2T) free | no              | (400 mini) 5.00€ |   5.00€ |   08/20 |
| -               |          (2T) 0.005 € |     (<2T) free | no              |                  |         |         |
| [Scaleway]      | (75GB<s<0.5T) 0.01  € |   (>75GB) 0.01 | no              |            1.25€ |   2.50€ |   08/20 |
|                 |                       |                |                 |                  |         |         |

[Amazon S3]: #aws "internal reference"
[Azure]: #azure_blob "internal reference"
[BlackBlaze B2]: #b2  "internal reference"
[Digital Ocean]: #digital_ocean "internal reference"
[Google One]: #google_one "internal reference"
[OneDrive]: #onedrive "internal reference"
[OVH openstack]: #ovh_openstack "internal reference"
[Mega]: #mega "internal reference"
[Scaleway]: #scaleway_object  "internal reference"
[Wasabi]: #wasabi  "internal reference"

The backblaze calculator which is more detailled but list only
blackblaze, Azure and Google Cloud give for first case Blackblaze 1.40$
, Azure 4.60$, S3 5.20$, Google clouds 5.6$; for the second
case study Blackblaze 5.00$
, Azure 13.60$, S3 14.20$, Google clouds 20$; but It seems to be
erroneous for Azure, because their cost calculator indicate aroud 5$
depending of the location of the cloud service.

You find a comparison of pricing and speed in
[Gilbert Chen Cloud Storage Comparison
](https://github.com/gilbertchen/cloud-storage-comparison). _not updated between 2018
and 2020_.

Note that Google Drive is slow, Onedrive and Dropbox very slow.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
