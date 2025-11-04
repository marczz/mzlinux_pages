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
-   [AWS pricing calculator](https://calculator.aws/#/)
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
-   [Boto3](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)
    is the Amazon Web Services (AWS) SDK for Python.
    -   [Boto3 GitHub Repository](https://github.com/boto/boto3).
    -   _Boto3_ has [many frontends in Pypi
        ](http://pypi.python.org/pypi?%3Aaction=search&term=boto3&submit=search)
        but some where developed in python2 for the previous Boto version and are not
        compatible with the new _Boto3_.
-   [DragonDisk](http://www.dragondisk.com/) (proprietary software, free linux client)
    is a file manager for Amazon S3, Google Cloud Storage, and S3 compatibles cloud
    storage services. Debian packages are provided.
-   [Duck](https://docs.duck.sh/cli/)
    the Cyberduck command line tool is available for Mac, Windows & Linux. A Deb
    repository is available, *It is distinct from the homonym Debaian Duck package*. It
    supports the following protocols: ftp, ftps, sftp, WebDAV (HTTP/SSL), Swift, Amazon
    S3, Backblaze B2, Google Cloud Storage, Windows Azure Storage, Rackspace Cloud
    Files, iPlant Data Store.

    The desktop UI [CyberDuck](https://docs.duck.sh/), and the virtual fs MountainDuck
    are available only on windows and Mac OSX. But there are alternatives for Linux like
    {{< iref "#rclone" >}}
-   [JetS3t](https://github.com/mondain/jets3t) (Apache License)
    (pronounced "jet-set") is a Java toolkit and application suite
    for Amazon S3, Amazon CloudFront, and Google Storage.

    _JetS3t_ is packaged in Debian, but only the old version that is no more maintained,
    as of 2023 the new fork which is stalled is not used.
-   <a name="miniocli"></a>[MinIO Client (mc)](https://github.com/minio/mc)  (Apache Licence)
    provides a modern alternative to UNIX commands like ls, cat, cp, mirror, diff, find
    etc. It supports filesystems and Amazon S3 compatible cloud storage service.
    Home.
    -   [MinIO Client Complete Guide](https://docs.min.io/docs/minio-client-complete-guide).
        and [QuickStart Guide](https://docs.min.io/docs/minio-quickstart-guide).
    -   [MinIO-mc Linux reference
        ](https://min.io/docs/minio/linux/reference/minio-mc.html)

    The binary for Linux can be downloaded on Minio site, see the above documentation
    for details.  You can also install the sid package `golang-github-minio-cli-dev`
    which build it on your system. There is a snapcraft package for minio client,
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
        {{< iref "#scaleway_storage" "scaleway object storage" >}},
        {{< iref "network_filesystems#minio" "Minio" >}} or
        {{< iref "#eucalyptus" "Eucalyptus" >}} like explained in
        [how to use s3cmd with an eucalyptus instance
        ](https://github.com/eucalyptus/eucalyptus/wiki/HowTo-use-s3cmd-with-Eucalyptus).
    - _s3cmd_ is packaged in Debian.
-   [s4cmd](https://github.com/bloomreach/s4cmd) (Apache Licence)
    is a python alternative to _s3cmd_ tool, enhancing performance and support for
    large files, and coming with a number of additional features and fixes.  It also
    supports S3 compatible storage services such as DreamHost and Cloudian.
    _Packaged in Debian._
-   [s3curl](https://github.com/rtdp/s3curl) (Apache License)
    is a perl wrapper around curl to work with s3 buckets.
    -   [Amazon S3 Authentication Tool for Curl - AWS Code
        ](https://aws.amazon.com/code/amazon-s3-authentication-tool-for-curl/)
    -   It can also be used on an {{< iref "#eucalyptus" "Eucalyptus" >}} instance.
    -   s3curl is packaged in Debian.

# Object Storage

## Blackblaze B2 {#b2}
{{< wp "BlackBlaze" >}} has many products available at
[Backblaze Home](http://www.backblaze.com/).

[Personal backup](https://www.backblaze.com/cloud-backup/personal) is an online backup
tool using AES encryption ([more on BlackBlaze encryption
](http://blog.backblaze.com/2008/11/12/how-to-make-strong-encryption-easy-to-use/))
$99/Year by computer for unlimited data.  No linux client, and no open api.

Backblaze _B2 Cloud Storage_ works similar to Amazon S3 or Microsoft Azure.

It is among the cheapest price of S3 compatible object storage.

$0.006/GB a month with 10 GB storage free, uploads are
free, Download s free for 3x monthly storage then 0.01$/G, _API Calls_ $0.004 per 10,000 transactions
with 2500/day free (some transactions free). _December 2023 pricing_

The [pricing page](https://www.backblaze.com/b2/cloud-storage-pricing.html)
includes a cost calculator with comparison with S3, microsoft azure and google cloud.
but no comparison with cheap providers like Scaleway, Idrive or Wasabi.

[B2 Documentation](https://www.backblaze.com/b2/docs/)

The basics operation are done with the [command-line tool
](https://github.com/Backblaze/B2_Command_Line_Tool) which is packaged in debian
a _blackblaze-b2_, the python sdk is also packaged as _python3-b2sdk_.

B2 also provide a [S3 compatible API
](https://www.backblaze.com/docs/cloud-storage-s3-compatible-api).

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

## Digital Ocean Block Storage {#digital_ocean_storage}
[Digital Ocean Block Storage
](https://www.digitalocean.com/pricing/spaces-object-storage)
is a S3 compatible storage by small data amount. 250GB, with 1TB outbound transfer is
5$/month, additional storage is 0.02GB/month *the same rate than the first 250GB*, and
additional transfer 0.01$/month.

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

## Idrive e2 {#idrive_e2}

[Idrive e2](https://www.idrive.com/object-storage-e2/) is an S3 compatible object
storage. It provides storage beginning at 1TB at a uniform price of 30$ 1T/y *December
2023*.

They have a [price comparator](https://www.idrive.com/object-storage-e2/pricing) with
amazon S3, Microsoft Azure, and Google Cloud.

## Openstack {#openstack}

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

    It is also used for [Sftp Cloudfs](https://github.com/Memset/sftpcloudfs)
    which acts as a proxy between a SFTP client and openstack storage .
-   [OpenStack Swift on Raspberry Pi
    ](http://programmerthoughts.com/openstack/swift-on-pi/)
-   [Swift Explorer](http://www.619.io/swift-explorer) (Apache License)
    is a java software.
    -   [swift explorer - GitHub](https://github.com/roikku/swift-explorer).

### Openstack storage providers
-   Openstack is underlying technology for {{< wp "Rackspace" >}} Cloud Servers. They
    provide [openstack object storage](https://www.rackspace.com/cloud/files)
    *It seems very expensive compared to OVH*.
-   <a name="ovh_openstack">{{< wp "OVH" >}} provides [openstack/swift object storage
    ](https://www.ovh.com/fr/public-cloud/storage/object-storage/)
    at the price of 0.01€ G/month inbound traffic free, outbound
    traffic 0.01€/G *December 2023*.
    Ovh has [documentation on object storage management
    ](https://www.ovh.com/fr/public-cloud/storage/object-storage/).

    In addition to openstack/swift API OVH offers SFTP, Rsync, SCP, HTTPS access to
    the storage.

    OVH provides also cold storage for archiving *cold Archive*,  retrieving you data
    can take up to few hours.  The price of cold  archive is
    0.0024€/ GB-month, with inbound and outbound traffic at 0.011€/G.

    *December 2023*.

## Scaleway Object storage {#scaleway_storage}

{{< iref "#scaleway" "Scaleway" >}} provides S3 compatible object storage.
-   [S3-Compatible Object Storage](https://www.scaleway.com/en/object-storage/)

    The block storage comes in two variants *One Zone* 0.012€ HT GB/month;
    *multi AZ*, is replicated between regions and at a price 0.014€ GB/month.

    Incomming trafic _internal and external_ as Internal outgoing traffic to other
    Elements products in the same region is free, external outgoing trafic is free for
    first 75GB then 0.01 € per GB/month.
-   [Glacier Cold Storage](https://www.scaleway.com/en/c14-cold-storage/)
    0.002€ GB/month. Archiving from C14 Cold Storage’s Glacier class to
    Object Storage’s Standard class is free of charge, but recovering to standard class
    is 0.009€/G.

    Combined with the downloading from standard class downloading from Glacier costs
    0.0

    *The prices are from December 2023*

Documentation from Scaleway:
-   [Object Storage - Quickstart
    ](https://www.scaleway.com/en/docs/storage/object/quickstart/).
-   [Object Storage - Concepts
    ](https://www.scaleway.com/en/docs/storage/object/concepts/).
-   [How to restore an object from Glacier
    ](https://www.scaleway.com/en/docs/storage/object/how-to/restore-an-object-from-glacier/).

Most [S3 operations are supported
](https://www.scaleway.com/en/faq/object-storage/#-Which-S3-operations-are-supported)
and most tools usable with S3 like _s3cmd_, _aws-cli_, _s3fs_, _cyberduck_, _minio
mc_…  are also usable with Scaleway object storage. The are referenced in the
[object storage page](https://www.scaleway.com/en/object-storage/).

To estimate your consumption you can look at the [storage metric
](https://www.scaleway.com/en/docs/storage/object/how-to/monitor-consumption/).

## Wasabi {#wasabi}
[Wasabi](https://wasabi.com/) is a cloud block storage S3 compatible. The minimum
plan is 1TB. And it applies an uniform cost 7$/TB/Month - _December 2023 Pricing_,
with free in and out trafic, and free api calls.

They have a [cost estimator](https://wasabi.com/cloud-storage-pricing/#cost-estimates)
to compare with amazon S3, Microsoft azure, and google cloud. But bot with cheaper
providers like {{< iref "#idrive_e2" "IDrive e2" >}}.

# File System Storage

I list only a small number of available services look also at Wikipedia
{{< wp "Comparison of file hosting services" >}}.

## Box {#box}

[Box](http://www.box.com/)(box.com or box.net)
has 10 GB of free web-storage, 250M file size limit, some temporary promotion allow 50G
free.

The *Personnal Pro* plan costs 108€ for 100GB, 5GB file limit, 10 versions, file sharing
links, mobile web access, free android, iphone, ipad application. *December 2023 Price*.

-   Wikipedia: {{< wp "Box.com" >}}
-   To know the current promotions follow the _promotions faq_ link
    in the [support Home Page](https://support.box.com/home)
-   Business plan 162$*users/year, with a minimum of 3 users, which makes a minimum of
    486€/year; for unlimited storage, max 5GB/file.
-   Box support FTP and FTPS (not SFTP) only for Business
    and Enterprise customers.
-   Synchronization client is only available
    for windoze and Mac OS/
-   There is no linux client in the offer.

-   [Box Developer Home](http://developers.box.com/) present the
    Box API.
-   [Box technical blog](https://tech.blog.box.com/) has  also informations for developers.
    There is an associated [Box technical blog GitHUb repository](https://github.com/box)
-   Note that the old box API V1, has been [replaced beginning 2012 with
    version 2](http://developers.blog.box.com/2012/04/25/introducing-the-v2-api/)
    and is no longer available.
-   [Boxfs2](https://github.com/drotiro/boxfs2)
    by Domenico Rotirot is a FUSE filesystem
    for box.com. *Last commit 2015. There are some updates in the repository forks.*
-   Box is [supported by Rclone](https://rclone.org/box/).

## Dropbox {#dropbox}
2GB storage free, 100$/year for 100GB
Dropbox is packaged for main linux distributions, and mobiles.

The dropbox daemon footprint is 50M res/16M shr

-   Wikipedia: {{< wp "Dropbox" >}}
-   [ArchLinux: Dropbox](https://wiki.archlinux.org/index.php/Dropbox)
-   [(Dropbox) secure remote storage using sshfs and encfs
    ](http://balau82.wordpress.com/2009/08/23/secure-remote-storage-using-sshfs-and-encfs/)
-   The dropbox daemon footprint is 50M res/16M shr
-   {{< iref "#rclone" "rclone" >}} support Dropbox.


### Dropbox API

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

##  [Google One](https://one.google.com/) {#google_one}

Google One is the storage shared beetwen
<a name="gdrive"></a>[Google Drive](https://drive.google.com/), Google Mail, and Google
Photos.  Gmail message can have attachments as big as 10G. The free plan is of 15G.

The [Google one storages plans](https://one.google.com/storage) are _ 100GB
20€/year, 200G 30€/year, and 2TB 10€/month 100€/year. _December 2023 Pricing._

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
-   {{< iref "#rclone" "rclone" >}} support [Google Drive](https://rclone.org/drive/)
    and [Google Cloud Storage](https://rclone.org/googlecloudstorage/).

## Mega {#mega}

[Mega](https://mega.co.nz/) New-Zealand company offer 20GB free, with limited transfers
_previously it was 50G now unavailable_, linux desktop sync client, android and iphone
apps, a chrome and firefox extension.

The paid plans are 100€/year 2TB data, 24 TB transfer; 200€/year 8TB data, 96TB
transfer; 300€ 16TB data 192TB transfer. *December 2023 pricing*

-   [MEGA SDK - Client Access Engine](https://github.com/meganz/sdk)
    is a mega SDK in C++; it provides two command line tools _megacli_ that allows to
    use all SDK features and _megasimplesync_ to use the synchronization engine; and
    some example apps. It is a very active project _in 2023_.
-   <a name="megacmd">[MEGAcmd](https://github.com/meganz/MEGAcmd)
    is a CLI built upon the SDK.

    It features one server _MEGAcmdServer_, a ftp like interactive shell _MEGAcmdShell_
    and several commands that will launch the non-interactive client _MEGAcmdClient_.

    The interactive shell offer the usual commands we find in ftp: ls, cd, lcd, pwd,
    lpwd, mkdir, rmdir, put, get, .... and more like find, disk usage, a command to sync
    a local and remote folder, manage global exclude patterns for sync....
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


-   [Megatools - command line client for Mega.co.nz](http://megatools.megous.com/)
    Megatools is a collection of programs for accessing Mega from command line.
    Megatools allow you to copy individual files as well as entire directory trees to
    and from the cloud. You can also perform streaming downloads without needing to
    download the entire file.

    Megatools is active _in 2023_ and in Debian.
-   [go-mega (GitHub)
    ](https://github.com/t3rm1n4l/go-mega) is a client library in go.
-   [Mega.py (GitHub)](https://github.com/odwyersoftware/mega.py)
    is a Python library for the Mega.co.nz API, currently supporting, login, uploading,
    downloading, deleting, searching, sharing, renaming, moving files.
-   {{< iref "#rclone" "rclone" >}} support Mega.


## Nextcloud {#nextcloud}
Nextcloud is a fork of {{< wp "Owncloud" >}}, Owncloud presently only maintains a legacy
version of the PHP/MySQL Owncloud, and after being acquired by a new Owner focus on the
Private product *Infinite Scale*

-   [Nextcloud](https://nextcloud.com/)
-   [nextcloud/server · GitHub](https://github.com/nextcloud/)

-   <a name="kdrive"></a>[kdrive](https://www.infomaniak.com/en/kdrive)
    is a Nextcloud hosting proposal from the swiss company
    [Infomaniak](https://www.infomaniak.com/en).

    The free plan is 15GB storage with reduced functionalities; the kdrive solo plan
    gives 2T of space for 5€/month. There is also a
    [ksuite plan](https://www.infomaniak.com/en) for multiple users.
-   [OwnCube](https://owncube.com/)
    propose Nextcloud hosting. There are
    [many packages](https://owncube.com/vergleichen_en.html)
    the *Admin* package proposes 100GB 2€/month, 500GB 4€/mth, 1TB 6€/month, 2TB 8€/month
    *prices checked in December 2023*.

    They also propose a VPS hosted nextcloud.
-   [OwnDrive](https://owndrive.com/)
    run nextcloud. There is free 1GB account
    with support for Calendar, Contacts, Bookmarks, Tasks and Notes;
    2€/month 5GB with more applications; 30€/year 15GB; 40€/year 25GB; 54€/year 50GB ...
    *Pricing December 2023*

    It allows to add external storage from many providers S3, Openstack, ...
-   [ShadowDrive](https://shadow.tech/drive)
    is a modified nextcloud provider. It delivers only the filesystem interface to
    nextcloud, other option or apps are unavailable.

    The 2TB plan is at 5€/month *in December 2023*.
-   [Webo](https://webo.cloud/nextcloud/)
    has nextcloud plans, in the *single* category 3.05€/month 50G, 6.10€/month 100G,
    28.1€/month 500G.
    In the *admin* category 37.8€/year 50GB, 75,6€/year 100GB ....
    _prices December 2023_.


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

## Rsync.net {#rsync.net}
[Rsync.net](http://www.rsync.net/) offer cloud storage on an Unix
platform with ZFS file systems and an SSH access. The standard offer
with 7 daily snapshots from 800G to 9TB 0.012$/ G x month, between 10T and 99T
O.O1$/G x month, and over 100 T 0.06$/G x month. *Prices from December 2023*
So 1T costs 147$/year.

As _Rsync.net_ is ssh based it can be used with
rsync, sftp, scp, sshfs, duplicity, rdiff-backup, unison git, git-annex,
subversion, or anything that could be piped to ssh.


There is also an [offer for Borg backup](http://www.rsync.net/products/attic.html).  It
is without snapshots since history is handled by Borg, it may be used on a lowest data
limit than the ordinary plan as it begins at 100G instead of 800G. The cost is
0.015$/GB*month between 100G and 999G, 0.008$/GB*mth between 1T and 99T and 0.005$/GB*mth over 100T.
So as example 100G plan is 18$/year. _December 2023 prices_

## Seafile
[Seafile (GitHub)](https://github.com/haiwen/seafile) (GPL)
is an open source replacement for Dropbox.
It provides a server that build on Linux, and clients for many OS.

-   [Seafile.com Home Page](http://seafile.com/en/home/).

## Storage Box

### Hetzner storage box {#hetzner_storage_box}
[Hetzner](https://www.hetzner.com) propose a
[Storage Box](https://www.hetzner.com/storage/storage-box).
It supports any file access tool that is backed by ssh, as sftp, rsync, scp, borg
backup, restic; and also samba and webdav.


The pricing  is 1TB 3.81€/month, 5TB 12.87€/month i.e 2.58 €/TB*month,
there are also 10T and 20T all around 2.5€ /TB*month.

## Yandex.Disk {#yandex_disk}

[Yandex.Disk](http://disk.yandex.com/) gives 10GB free, 200G 16.4$ year,
2TB 54$/year, 3TB 72€/yead _December 2023_.

There is a linux client allowing synchronization as well as Mac OS,
windows, android, iphone clients.

{{< iref "#rclone" >}} has [Yandex support](https://rclone.org/yandex/).

-   Wikipedia: {{< wp "Yandex Disk" >}}
-   Yandex allow webdav access, that you can use with davfs:

        $ mount -t davfs https://webdav.yandex.ru /tmp/yandex_disk

-   Yandex has a simple [http API
    ](http://api.yandex.com/disk/doc/dg/concepts/api-methods.xml)


## Other clouds

-   {{< wp "Adrive" >}} (Wikipedia) it has only a web interface, in java, and
    Linux compatible.
    The premium plan feature 100GB of storage cost $25 per year, you can order what you
    need at the same rate of 25$/100GB *December 2023*.

    *Adrive* provides Webdav SCP, SFTP and Rsync,file versionning and encryption.  The
    Data is not encrypted.

    -   [Adrive Home](http://www.adrive.com/)
    -   [Adrive storage plans](http://www.adrive.com/plans)

-   <a name="azure_blob">[Microsoft Azure Blob storage
    ](https://azure.microsoft.com/en-us/pricing/details/storage/blobs/)
    has blob storage _hot_ at a price going fro 0.0181€/GB*month to 0.021$ depending
    of the region. The downloads are free, and the API as a cost (see their
    calculator). These price are for local redundancy, they grow to 0.037€ if you
    want your data replicated in different regions.

    There is also _cool_ storage at 0.01€$/GB*month or 0.02€ when replicated among
    regions for cool storage the downloads are also 0.01$/Gb. _checked 09/22_
    -   [Pricing calculator
        ](https://azure.microsoft.com/en-us/pricing/calculator/?service=managed-disks).

    You can [s3 compatible tools
    ](https://cloudblogs.microsoft.com/opensource/2017/11/09/s3cmd-amazon-s3-compatible-apps-azure-storage/)
    by using {{< iref "network_filesystems#minio" "Minio" >}} as bridge.
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
    40€/year 25G, 80€/year 100GB, 140€/year 200G _December 2023_. It has an
    [CloudMe android App](http://www.cloudme.com/en/features/mobile/android),
    is also accessible from web as any of these solutions, with also
    an [interface for mobiles](http://cloudme.com/m), and has also a
    [WebDav option](https://www.cloudme.com/en/webdav)
-   [MyDrive](https://www.mydrive.ch/) is a swiss company, that offer
    a webdav access, there is a free plan of 512MB, the other plans are only visible to
    registered users.
-   <a name="onedrive"></a>[OneDrive](https://onedrive.live.com/)
    previously SkyDrive is a Microsoft cloud hosting.  It offers 15 GB of free
    storage. There is no built-in encryption, of course no linux client!  For a longer
    description look at Wikipedia {{< wp "OneDrive" >}}.

    The Onedrive plans are packed with the Microsoft 365 suite. 20$/year 100G, 70$/y
    1TB, 100$/y 6 users each with 1TB. *prices december 2023*
    -    {{< iref "#rclone" >}} has [OneDrive support](https://rclone.org/onedrive/).
    -   [official OneDrive SDK for Python
        ](https://github.com/OneDrive/onedrive-sdk-python)
    -   [bash-onedrive-upload](https://github.com/fkalis/bash-onedrive-upload)
        (MIT License) _last commit 2017_ is a bash command line client to use the REST
        API to upload files.
    -   [skillion/onedrive](https://github.com/skilion/onedrive) (GPL)
        a client written in D to sync with onedrive. It is packaged in Debian as
        _onedrive_ since _stretch_.

-   [SpiderOak](https://spideroak.com/):
    [SpiderOak One](https://spideroak.com/one/) 150GB 69$/year, 400GB 115$/year, 2TB
    149$/year _2020_
    [SpiderOak Android](http://www.appbrain.com/app/spideroak/com.spideroak.android)
    SpiderOak deamon _headless_ is 33M/5M shr, and with panel even
    minimized you add 66M/19M
-   [Storegate](http://www.storegate.com/) seems targeted to windows users, no rclone
    interface no known SDK nor linux client.
-   [SugarSync](https://www.sugarsync.com/):
    [SugarSync vs Dropbox : The Alternative You Never Asked For
    ](http://www.groovypost.com/howto/review/sugarsync-vs-dropbox-alternative-you-never-asked-for/)
    The plans begin at 100GB 90$/year, 250GB 120$/year, 500G 228$/y *December 2023*

    There is no Linux support and the unofficial client has been abandoned but
    {{< iref "#rclone" "Rclone" >}} includes a
    [Support for SugarSync](https://rclone.org/sugarsync/).
    -   The [SugarSync: Sync server comparison
        ](https://www.sugarsync.com/sync_comparison.html)
        gives some feature comparison of main solutions.
    -   [ArchWiki: SugarSync](https://wiki.archlinux.org/index.php/SugarSync)
        explains how to use SugarSync with wine.

# Cloud frontends {#cloud_frontends}
See also the  {{< iref "#s3_clients" "S3 specific clients" >}}, that can be used with S3
compatible clouds or through a proxy like {{< iref "#s3proxy" "S3Proxy" >}}.

## Virtual File systems {#cloud_vfs}
-   <a name="s3proxy"></a>[s3proxy](https://github.com/gaul/s3proxy) (Apache License)
    is a Java software that provides S3 API and proxies requests, from S3 to Backblaze
    B2, EMC Atmos, Google Cloud, Microsoft Azure, and OpenStack Swift, and on-disk
    storage filesystem.  It can be used with the others S3 tools.
    There is a Docker image, or it can be used directly with java.


### Rclone {#rclone}

[Rclone](http://rclone.org/)
is a command line program to sync files and directories to and from Amazon Drive, Amazon
S3, Backblaze B2, Box, Ceph, Citrix share files, DigitalOcean Spaces, Dreamhost,
Dropbox, GetSky, Google Drive, Google Cloud Storage, Google Photos, Hubic, Jottacloud,
IBM COS S3, Kiifr, Mail.ru cloud, Memset Memstore, Mega, Memory, Microsoft Azure,
Microsoft OneDrive, {{< iref "network_filesystems#Minio" "Minio" >}}, NextCloud, OVH, OpenDrive, Openstack
Swift, Oracle Cloud Storage, ownCloud, pCloud, premiumize.me, put.io, QingStor,
Rackspace cloud files, Scaleway, StackPath, SugarSync Wasabi, Yandex Disk, HTTP (read
only), FTP, SFTP, WebDav, the local filesystem.

Features:  hashsums (many algorithms) checking, preserve timestamps, partial syncs,
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
-   _Rclone_ has a [bidirectional synchronizatrion option](https://rclone.org/bisync/)
    since v1.58.0 in March 2022.

    Previously it was featuring only only one way synchronization, and several python
    applications that provide bidirectional synchronisation with _Rclone_ were developed.
    -   [rclonesync-V2](https://github.com/cjnaz/rclonesync-V2)  (MIT License),
        deprecated since the addition of bidirectional synchronization to rclone.
    -   [rsinc](https://github.com/ConorWilliams/rsinc) (MIT License), last commit 2020.
    -   [PyFiSync](https://github.com/Jwink3101/PyFiSync) (MIT License) can use rsync or
        rclone..
    -   [syncrclone](https://github.com/Jwink3101/syncrclone)  (MIT License)
        written in Python by Justin Winokur _Jwink3101_ the author of PyFiSync, read
        [PyFiSync vs. syncrclone
        ](https://github.com/Jwink3101/syncrclone#differences-from-pyfisync).

        It features: fully non-interactive actions, backups before anything destructive,
        extensive test suite, configurable file comparison and conflict resolution, use of
        past sync state to accelerate checksum computation,  uses rclone's powerful filtering,
        configurable rename tracking even for remotes with incompatible hashes,
        robust to interruption, locking system, dry-Run mode.

        Documentation: [configuration tips
        ](https://github.com/Jwink3101/syncrclone/blob/master/docs/config_tips.md),
        [algorithm](https://github.com/Jwink3101/syncrclone/blob/master/docs/algorithm.md),
        [miscellaneous details](https://github.com/Jwink3101/syncrclone/blob/master/docs/misc.md),
        [testing](https://github.com/Jwink3101/syncrclone/blob/master/docs/tests.md).

        The [algorithms of syncrclone and `rclone --bisync`  differs
        ](https://github.com/Jwink3101/syncrclone/blob/master/docs/rclone_bisync_compare.md)
        two differences make them work distinctly depending on the backend.
            -   While rclone uses the modtime, syncrclone may use modtime or hashes,
                which make it more adapted on backends where the modification time is
                not available or not accurate.
            -   Rclone uses [Differential Synchronization with dual shadow method
                ](https://neil.fraser.name/writing/sync/)
                syncrclone compare *current* state and use previous to resolve
                conflicts.

-   _Rclone_ is supported by _emacs tramp_ since version 2.4.1.


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
/
    There is a free plan with a limit of 5GB/month traffic, paid plans for 1200GB/year at
    60$/year, 119$/year or 249$ life-time unlimited traffic _Price December 2023_.

    It allows filters for file selection and to schedule cloud sync or cloud to cloud
    backup at a regular interval.

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
-   <a name="digital_ocean">[Digital Ocean](https://www.digitalocean.com/)
    cloud hosting.  Pricing plans start
    at $4/month  for 512MB of RAM, 10GB SSD, 1 CPU, and 500GB
    Transfer or $12/month for 2GB RAM, 50GB SSD, 1 CPU, and 2TB
    Transfer. For added SSD 100G for 10$/month _September 2022_.
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

    See {{< iref "#scaleway_storage" "above for object storage" >}}.

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

I don't include here Microsoft Azure or Amazon S3 as they are a lot more expensive, and
also the S3 price depends of a multitude of factor that must be examined for a
specific use case. For details refers to their price calculator like
[AWS pricing calculator](https://calculator.aws/#/).

For a rough estimate you may use
[Idrive price comparator](https://www.idrive.com/object-storage-e2/pricing), or
[Wasabi cost estimator](https://wasabi.com/cloud-storage-pricing/#cost-estimates)
or [backblaze cost calculator](https://www.backblaze.com/b2/cloud-storage-pricing.html)
which includes a comparison with S3, microsoft azure and google cloud.

## Object storage

| Provider           | fix quota | price TB/y |    outbound/GB | API Fees | checked |
|--------------------|-----------|-----------:|---------------:|:---------|--------:|
| [BlackBlaze B2]    |           |        72$ | > 3*data 0.01$ | > 2500   |   12/23 |
| [Digital Ocean]    | >250G     |       245$ |  > 1Ti/m 0.01$ |          |   12/23 |
| [idrive e2]        | >1T       |        30$ |              - | -        |   12/23 |
| [OVH openstack]    | -         |       120€ |           0.01 |          |   12/23 |
| [Scaleway] Multi   | -         |       168€ |   >75G/m 0.01€ | -        |   12/23 |
| [Scaleway] OneZone | -         |       147€ |   >75G/m 0.01€ | -        |   12/23 |
| [Wasabi]           | >1T       |        84$ |              - | -        |   12/23 |

## Cold Storage
| Provider                | price TB/y | put 1TB | download 1T | API Fees | checked |
|-------------------------|-----------:|--------:|------------:|:---------|--------:|
| [OVH openstack] Archive |      29.5€ |   11.2€ |       11.2€ |          |   12/23 |
| [Scaleway] Glacier      |        24€ |       - |       19.5€ |          |   12/23 |
|                         |            |         |             |          |         |

*I d'ont put idrive here, as it is not a cold storage, but it's low price make it
competitive in front of other cold storage*

## File System Storage

| Provider      | fix quota | price TB/y | outbound | checked |
|---------------|-----------|-----------:|---------:|--------:|
| [Google One]  | =100G     |       200€ |          |   12/23 |
| [Google One]  | =200G     |       150€ |          |   12/23 |
| [Google One]  | =2T       |        50€ |          |   12/23 |
| [Hetzner SB]  | =1T       |        45€ |          |   12/23 |
| [Hetzner SB]  | =5T,=10T  |        31€ |          |   12/23 |
| [kdrive]      | =2T       |        30€ |          |   12/23 |
| [OneDrive]    | =1T       |        70$ |          |   12/23 |
| [Mega]        | =2T       |        50€ |     <24T |   12/23 |
| [Mega]        | =8T       |        25€ |     <96T |   12/23 |
| [Rsync.net]   | 800G<x<9T |       147$ |        - |   12/23 |
| [Yandex Disk] | =200G     |        82€ |          |   12/23 |
| [Yandex Disk] | =2TB      |        27€ |          |   12/23 |
| [Yandex Disk] | =6TB      |        12€ |          |   12/23 |
|               |           |            |          |         |


[Amazon S3]: #aws "internal reference"
[Azure]: #azure_blob "internal reference"
[BlackBlaze B2]: #b2  "internal reference"
[Digital Ocean]: #digital_ocean "internal reference"
[Google One]: #google_one "internal reference"
[Kdrive]: #kdrive "internal reference"
[Hetzner SB]: #hetzner_storage_box "internal reference"
[OneDrive]: #onedrive "internal reference"
[OVH openstack]: #ovh_openstack "internal reference"
[Mega]: #mega "internal reference"
[Rsync.net]: #rsync.net "internal reference"
[Scaleway]: #scaleway_storage  "internal reference"
[Wasabi]: #wasabi  "internal reference"
[Yandex Disk]: #yandex_disk "internal reference"

Note that the fixed amount for some plans imply that for some volume of data the
cheapest plan is not the one noted above as lowest by TB/year.  If you want to host only
400GB Google one and Mega will cost 100€, Wasabi 84€, Scaleway 65€, kdrive 60€, OVH
openstack 48€, Hetzner 45€, Yandex 32.8€, Idrive 30€, Blackblaze B2 28$.

Of course the price is not the only criteria, it does not includes the ingress and
egress trafic, these storage have very different characteristics, some are
geographically replicated, they may or may not have backups and versioning, some are
block storage, some file storage, some are encrypted on the server, and the latency and
transfer throughput may largely vary.

The price do not include taxes, in Europe Community all countries are subject to VAT
with rates varying from 16% to 27% and for most of the countries between 19% and
25%. Even not in EU Swiss has a 7.7% rate and Great Britain 20%. When buying some
product from EU in a country outside EU, it is billed without taxes and the VAT is added
by the carrier. I have no idea on what apply to some abroad computer service. It is
still move complicated if we consider that the company can be outside of Europe but the
Data center is located
in EU.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
