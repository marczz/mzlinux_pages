---
title: Backup
---

{{% toc /%}}

# General References

-   Wikipedia: {{< wp "Comparison of backup software" >}},
    {{< wp "List of backup software" >}},
    {{< wp "Comparison of online backup services" >}}
-   [Debian Wiki: Backup And Recovery
    ](https://wiki.debian.org/BackupAndRecovery)
    gives a list of backup related Debian Packages.
-   [Debian Reference Manual §10.2: Backup and recovery
    ](https://www.debian.org/doc/manuals/debian-reference/ch10.en.html#_backup_and_recovery)
-   [Debian Help: category backup
    ](http://www.debianhelp.co.uk/backup.htm)
    [Debian Help: tools Available for Linux Backup
    ](http://www.debianhelp.co.uk/backuptools1.htm)
-   [Arch Wiki: Synchronization and backup programs
    ](https://wiki.archlinux.org/index.php/Synchronization_and_backup_programs)
    gives a complete up-to-date list of programs.
-   <a name="cachedir"></a>
    [Cache Directory Tagging Standard _cachedir_
    ](http://www.brynosaurus.com/cachedir/spec.html)
    allow to identify cache directories. Usually yo won't backup
    them, {{< iref "#obnam" "obnam" >}} can exclude cachedir.

    A _cachedir_ is a directory containing a file named `CACHEDIR.TAG`
    containing as first 43 octets the string:

        Signature: 8a477f597d28d172789f06886806bc55

    A template for this file could be:

        Signature: 8a477f597d28d172789f06886806bc55
        # This file is a cache directory tag created by (application name).
        # For information about cache directory tags, see:
        #	http://www.brynosaurus.com/cachedir/

# Snapshot Backups

*Snapshot backup* consist to copy only the changed part of a
fs, and recreate the full file system from previous backups using
hard links ore more advanced *Copy On Write* file system.

Snapshot backup are a variant of mirror tools as they keep an image
or the original file system (or of some tree in a fs).But they
allow to keep a space efficient time history of this image without
duplication of the unchanged files by using hard links. Many of
these backup systems are gui or scripts around `rsync` which has an
option `--link-dest` for hard linking. Some others are based on a
[Copy On Write (COW)](http://en.wikipedia.org/wiki/Copy-on-write)
file system.

rdiff backup (and front ends) is an exception, it does not make
hard links but keep diff with the original files as does diff in
its transmission algorithm or git, so it is very efficients for big
files whose a small part is changing often (like a live database).
Recently some git based backup tools, like gibak,  make also their way
in the backup kit.

See also the {{< iref "#backup" "backup section" >}} that cover
classical backups where a changed file is copied again entirely
and the {{< iref "#synchronization" "Synchronization section" >}}
that includes {{< iref "#rsync" "rsync" >}}
 and its derived frontends and variants, like _unison_.

-   [from Arch Wiki:Incremental Backup Programs
    ](https://wiki.archlinux.org/index.php/Backup_Programs#Incremental_backups).



#  Chunk based increment snapshot
Chunk based increments are usefull when we need to save big files,
files based increments or rsync backups would save again the full file
even when only few bites have changed, chunk based increments will
save only the changed data blobs.

-    <a name="borg"></a>[Borg](https://github.com/borgbackup/borg/)
    is a fork of <a name="attic"></a>[Attic](https://github.com/jborg/attic/)
    which has no commit since 2015.
    Borg is a deduplicating backup program, written in Python > 3.2.
    The main features of Borg _and previously Attic_ are:
    -   __Space efficient storage__: Each file is split into a number of
        variable length chunks and only chunks that have never been
        seen before are compressed and added to the repository.
    -   __Optional data encryption__: All data can be protected using
        256-bit AES encryption and data integrity and authenticity is
        verified using HMAC-SHA256.
    -   __Backup over ssh__: if possible with Attic also installed
        on the remote host.
    -   __Backups mountable as filesystems__
    BorgBackup is in Debian.

    -   [Borg documentation
        ](http://borgbackup.readthedocs.io/en/stable/).
    -   [Borg Community resources
        ](https://github.com/borgbackup/community/)

    The backup programs closer to Borg bnam by its features was
    {{< iref "#obnam" "Obnam" >}}. Note that obnam can backup
    over SFTP without any software on the remote side, while Attic
    backup over ssh, by running attic /borg on the remote side.

    One advantage of Borg is that it uses an rsync-like
    rolling checksum method. This means that if you add 1 byte at the
    beginning of a 100MB file, Attic will upload a 1-byte chunk and
    then reference the other chunks after that, while Obnam will have
    to re-upload the entire file, since its chunks start at the
    beginning of the file in fixed sizes.

    -   [Comparison of Attic vs Bup vs Obnam
        ](http://librelist.com/browser/attic/2015/3/31/comparison-of-attic-vs-bup-vs-obnam/)
    -   [Roundup of remote encrypted deduplicated backups in Linux
        ](http://changelog.complete.org/archives/9353-roundup-of-remote-encrypted-deduplicated-backups-in-linux)
        compare attic and obnam.

-   <a name="duplicacy">[Duplicacy](https://github.com/gilbertchen/duplicacy)
    (Free for personal use, paid versions for commercial use)
    is a deduplicating incremental backup program written in go
    language.

    Backups are incremental but provide a full snapshot.
    The data is deduplicated, every backup can be deleted
    independently, it allows also snapshot migration. Multiple clients
    can back up to the same storage at the same time without locking
    the system thanks to
    [Lock Free Deduplication
    ](https://github.com/gilbertchen/duplicacy/wiki/Lock-Free-Deduplication).

    Duplicacy support many back-ends local drive, Amazon S3, Microsoft
    OneDrive, Microsoft Azure, Google Cloud Storage, Google Drive,
    HubiC, DigitalOcean Spaces, Backblaze (B2), Amazon Cloud Drive
    (AmzCD), Dropbox, Wasabi. The GitHub page contains a detailled
    comparaison of the costs and performance of these clouds; and a
    comparison with other populars backup programs. There is a deb
    package for each architecture in the [release section
    ](https://github.com/gilbertchen/duplicacy/releases).

    -   [Duplicacy Wiki
        ](https://github.com/gilbertchen/duplicacy/wiki)
        contain the User Guide.
    -   [Benchmarking scripts
        ](https://github.com/gilbertchen/benchmarking)
        used to benchmark the different backup software and the
        different backends.

-   <a name="obnam"></a>[Obnam](http://obnam.org/)
    is a snapshot local or remote through SSH SFTP backup program,
    that does data de-duplication, across files, and backup
    generations. It has a lot of configurable options, including chunk
    size, caching information, ect.  It is written in C and python
    (2.x) and is in Debian. _In August 2017 the author and maintainer
    of obnam announced, he is closing obnam and that it will be droped
    from Debian._

    -   [obnam manual
        ](http://code.liw.fi/obnam/manual/obnam-manual.en.html)
    -   [obnam FAQ](http://obnam.org/faq/)
    -   [Joey Hess about obnam
        ](http://joeyh.name/blog/entry/trying_obnam/)


    Obnam can be slow with a default improper config, some post
    compare it to other backup solutions, or explain how to configure
    it for speed:

    -   [Comparing rsnapshot and obnam for scheduled large backups
        ](https://blog.karssen.org/2013/01/04/comparing-rsnapshot-and-obnam-for-scheduled-large-backups/)
    -   [Understanding obnam performance
        ](https://listmaster.pepperfish.net/pipermail/obnam-support-obnam.org/2014-June/003086.html)
        very interesting paper on obnam performance tweaking also
        included in the [Obnam FAQ performance tuning
        ](http://obnam.org/faq/tuning/)

    From the last reference the settings for `lru-size` and
    `upload-queue-size` are critical, the default are 256 and 128 the
    most important is to increment `upload-queue-size` to 512
    _abridged option_ `-q=512`.  It has a very low impact on memory
    used. Increasing `lru-size` to 512 _abridged option_ `-l=512` as
    yet a small but signifiant impact on performance (from 2mn15 to
    2mn) at the price of an impact on memory (267M to 324M).

 -  <a name="hashbackup"></a>[HashBackup](http://www.hashbackup.com/) (free private license)
    is a command line for deduplicated, encrypted, compressed,
    block-level incremental backup.
    It is a rolling incremental backup, there is no concept of
    _full backup_.

    It can push backup on local storage, or remote offsite backup using:
    rsync, ssh, sftp, ftp, ftps, imap (email)
    WebDAV, Dropbox, Google Drive, NFS, and other mounted remote storage
    3rd-party storage: Amazon S3, Backblaze B2, Google Cloud Storage,
    Rackspace Cloud Files, Dreamhost DreamObjects and others.

    Compared  to the opensource existing deduplicating alternative like
    {{< iref "#attic" "Attic" >}},
    {{< iref "#borg" "borg" >}},
    {{< iref "#zbackup" "zbackup" >}},
    bup, {{< iref "#obnam" "obnaml" >}} it can
    access natively some 3rd-party storage while the rest can only
    mount them with fuse; and it invalidates programs that want
    to do checksumming on the remote backup, because
    it would imply to reload all the files.

-   <a name="restic"></a>[Restic](https://restic.github.io/) (BSD License)
    Is a go program that takes snapshots consisting of data blobs
    encrypted with AES-256.  You can mount an individual snapshot using
    a Fuse fs. Restic can use the following backends: local directory,
    sftp server (via SSH), HTTP REST server (protocol rest-server),
    AWS S3 (Amazon or Minio), OpenStack Swift, BackBlaze B2,
    Microsoft Azure, Google Cloud Storage

    Restic is in Debian and is active in 2017.
    -   [Restic documentation
        ](https://restic.readthedocs.io/en/stable/).
    -   [Restic GitHub repository
        ](https://github.com/restic/restic).
    -   [Analysis of borgbackup, restic, and zbackup
        ](http://www.sharons.org.uk/demise-of-obnam.html)

    There are some helpers to organize rastic backups:
    -   Sharon Kimble's
        [restic script](http://www.sharons.org.uk/restic4.html),
        [restic - integrity checking
        ](http://www.sharons.org.uk/restic2.html) and
        [restic - unlock](http://www.sharons.org.uk/restic3.html).
    -   [ansible-restic](https://github.com/donat-b/ansible-restic)
        an [ansible](https://www.ansible.com/) configuration for
        restic backups.
    -   [restic-tools](https://github.com/binarybucks/restic-tools)
        a bash script to organize restic backups.

-   <a name="zbackup">[zbackup](http://zbackup.org/) (GPL)
    is a globally-deduplicating C++ backup tool based on its own
    sliding window rolling hash for data deduplication, and SHA256 for
    backup integrity.  It allows LZMA compression & AES encryption.

    To backup set of directories, you tar them and pipe the result to
    zbackup. The data should be uncompressed and unencrypted
    otherwise no deduplication could be performed on it, and it would
    duplicate the zbackup compression and encryption. It is a drawback
    if you want to backup a directory containing a lot of compressed
    files _like odt files_ or encrypted like a git repository.

# btrfs snapshots

-   Btrfs Wiki:
    [How can I use btrfs for backups/time-machine?
    ](https://btrfs.wiki.kernel.org/index.php/UseCases#How_can_I_use_btrfs_for_backups.2Ftime-machine.3F),
    [Incremental Backup
    ](https://btrfs.wiki.kernel.org/index.php/Incremental_Backup)
-   [Snapper](http://snapper.io/)
    manage snapshots of Btrfs subvolumes and LVM volumes.
    It can create and compare snapshots, revert between snapshots,
    and supports automatic snapshots timelines.
    -   [ArchWiki: Snapper
        ](https://wiki.archlinux.org/index.php/Snapper)
    -   [Suse Administration Guide - Snapshots/Rollback with Snapper
        ](https://www.suse.com/documentation/sles11/book_sle_admin/data/cha_snapper.html).
-   [btrbk](http://www.digint.ch/index.html)
    is a backup tool for btrfs subvolumes, to create atomic snapshots
    and transfer them incrementally to a backup locations. It is
    written in Perl and is in Debian.

    Key Features:

    -   Atomic snapshots
    -   Incremental backups
    -   Configurable retention policy
    -   Backups to multiple destinations
    -   Transfer via ssh
    -   Resume of backups (if backup target was not reachable for a while)
    -   Encrypted backups to non-btrfs destinations
    -   Transaction log
    -   Display file changes between two backups

# Legacy programs
-   The [TimeMachine](http://www.apple.com/macosx/features/timemachine.html)
    backup system from apple, as many descendants in the Linux world.
-   <a name="timevault"></a>
    [TimeVault](https://wiki.ubuntu.com/TimeVault)
    use the _TimeMachine concept_. It is a simple front-end for making
    snapshots of a set of directories written in python.It needs some
    gnome libraries including gnome-python.   There is
    an alternative build for KDE.  _TimeVault_ is still available in
    Ubuntu but unmaitained since 2010, there is no longer a package in
    Debian. We should replace it with
    {{< iref "#backintime" "BackInTime" >}}.
-   [Zumastor](http://www.zumastor.org/)
    provides improved snapshots and remote replication.
    It needs we apply a set of kernel patches. _No more developed
    since 2008_


# Rdiff family {#rdiff-backup}

[rdiff-backup](http://www.nongnu.org/rdiff-backup/index.html) (GPL):
a remote incremental backup written in C and python
that can save also xattr-s and
acl-s. available as Debian package.
Like rsync based backups _rdiff-backup_ makes the backup directory
in a copy of the source directory.

It uses
<a name="librsync"></a>[librsync](http://librsync.sourceforge.net/)
which is based on the same algorithm than _rsync_ but is an
independent implementation that does not use the rsync network
protocol.

While rsync solutions use hardlinks to keep incremental backups
_rdiff-backup_ keep changes in the form of
{{< wp "Delta_encoding"  "delta files" >}}, these diff
can be applied also with [rdiff](http://librsync.sourceforge.net/).

The programs based on librdiff are chunk based backup and are
efficient for backing up large files. The __rsync__ program and backup
based on it while they can use chunks checksums for speeding network
transfers, are storing the full file when they cannot use hardlinks.

_rdiff-backup_ and _duplicity_ only do deduplication on new version of
the same file while _zbackup_, _attic_, _borg_ and the git format
based backup tools do global deduplication, so they can recognize two
similar or identical files.

-   Wikipedia {{< wp "Rsync#Variations"  "Rsync variations" >}}.
-   Tutorial:
    [Automated Backups With rdiff-backup
    ](http://howtoforge.com/linux_rdiff_backup)
-   [Gentoo: Rdiff-backup](http://wiki.gentoo.org/wiki/Rdiff-backup)
    is a set of command lines use of rdiff-backup _and nothing more!_
-   [rdiff-backup-fs](http://code.google.com/p/rdiff-backup-fs/) (GPL)
    is a fuse filesystem for accessing rdiff-backup archives.
    It allows transparent access of older backups.
-   <a name="backupninja"></a>
    [BackupNinja](https://labs.riseup.net/code/projects/backupninja)
    provides a centralized way to configure and schedule many
    different backup utilities. It can use _rdiff-backup_ or
    _duplicity_, make incremenetal _rsync_ backup with hardlinking.
    It can backup MySQL/PostgreSQL databases, subversion or trac
    repositories, burn CD/DVDs or create ISOs. BackupNinja minimally
    maintained since 2015. _BackupNinja_ is packaged in Debian.
-   [pybackpack](http://projects.sucs.org/projects/pybackpack/wiki)
    (GPL) is a gnome Gui (needs python-gnome2) for rdiff-backup
    written in python.
-   [Burp](http://burp.grke.org/index.html) (AGPL)
    is a network backup and restore program. It is based on Bacula but
    uses librsync.
-   [SafeKeep](http://safekeep.sourceforge.net/) (GPL).
    is a client-server program written in python and using rdiff-backup.
    it integrates with LVM snapshots and has an easy configuration.

# Duplicity {#duplicity}

[Duplicity](http://duplicity.nongnu.org/) (GPL)
backs directories by producing encrypted tar-format volumes and
uploading them to a remote or local file server.  It uses rdiffdir
that is an extension of {{< iref "#librsync" "librsync" >}} to
directories.  It is similar with _rdiff-backup_ but uses can use
encryption. _Debian package available_.

_Duplicity_ have two important features that distinguish it from
other backup solutions: content is encrypted, and you can put
your backup on servers where you have disk space but no real
control like most cloud storage services servers.  Duplicity
can use any file system with access thru ssh/scp/sftp, local file
access, rsync, ftp/ftps, HSI, WebDAV, Tahoe-LAFS, PAR2,
{{< iref "clouds" "Blackblaze B2" >}},
boto ({{< iref "clouds" "Amazon S3" >}},
Google Cloud Storage), {{< iref "clouds" "Mega" >}}
_but the interface library mega.py is obsolete, see below for an
alsternative way using MegaFuse_,
Rackspace,
{{< iref "clouds#dropbox" "Dropbox" >}},
google docs,
{{< iref "clouds" "OpenStack swift" >}},
{{< iref "clouds" "Hubic" >}}, (v > 7.0),
Azure (v > 7.0),
{{< iref "clouds" "Google Drive" >}}
through {{< iref "clouds#gdrive" "PyDrive" >}}.

-   [duplicity(1)](http://duplicity.nongnu.org/duplicity.1.html)
-   [ArchWiki: Duplicity](https://wiki.archlinux.org/index.php/duplicity)
-   [Debian Wiki: Duplicity](https://wiki.debian.org/Duplicity)
-   [Ubuntu Help: Duplicity Backup Howto
    ](https://help.ubuntu.com/community/DuplicityBackupHowto)
-   Tutorial: [Encrypted incremental backups with duplicity
    ](http://blog.sanctum.geek.nz/linux-crypto-backups/)
-   [DigitalOcean: How To Use Duplicity with GPG to Automate Backups
    ](https://www.digitalocean.com/community/tutorials/how-to-use-duplicity-with-gpg-to-securely-automate-backups-on-ubuntu).
-   [Offsite Linux backup to Mega with duplicity
    ](http://itnerd.space/2016/10/26/offsite-backup-with-duplicity-and-mega/),
    this article use a docker image to install duplicity and mega_fuse.


-   [Installation and configuration of duplicity for encrypted SFTP remote backup
    ](http://zertrin.org/how-to/installation-and-configuration-of-duplicity-for-encrypted-sftp-remote-backup/)
    an How-To by Zertrin.
-   [Box Backup](http://www.boxbackup.org/)
    (mixed BSD/GPL license) is a completely automatic, on-line,
    client-server encrypted backup system. All data is stored within
    the server file system on conventional hard disks.
    It uses rsync like diff for incremental backup. BoxBackup provides a
    [comparison with duplicity and hdup
    ](http://www.boxbackup.org/wiki/BoxComparison) _the hdup column apply to it's successor
    {{< iref "#rdup" "rdup" >}} for most items_. It is packaged in Debian.

## Duplicity frontends
Many frontends and wrapper for duplicity are availables:

-   The scripts listed in the
    [duplicity contrib page](http://duplicity.nongnu.org/contrib.html)
    : two minimal
    [full backup](http://duplicity.nongnu.org/contrib/jwfull) and
    [incremental backup](http://duplicity.nongnu.org/contrib/jwincr),
    a [LVM snapshot backup script](http://duplicity.nongnu.org/contrib/tmpback)
-   [duplicity-backup](git://github.com/zertrin/duplicity-backup.git)
    (GPL) by Zertrin is a 600 LOC shell duplicity wrapper
    designed to automate and simplify the remote backup process
    of duplicity on Amazon S3 instances or other backup
    destinations (ftp, rsync, sftp, local file…).
-   [Horcrux](http://chrispoole.com/project/general/horcrux/)
    is a 300 LOC shell wrapper for Duplicity’s
    most commonly-used options. It also includes functionality
    to check a restored backup to periodically ensure
    your backups are working. There is a slghtly modified fork in
    [GitHub: piffio/horcrux](https://github.com/piffio/horcrux).
    -   [Automating and encrypting duplicity backups using cron
        ](http://peterpetrakis.blogspot.fr/2013/06/automating-and-encrypting-duplicity.html)
        is an Horcrux case study.
-   [duply](http://duply.net/)  is packaged in Debian.
    Its' home page lists also some other wrappers.
    -   [Duply-documentation
        ](http://duply.net/wiki/index.php/Duply-documentation).
-   [simplicity](https://github.com/sitaramc/simplicity) (GPL) a
    300 LOC shell duplicity wrapper by  Sitaram Chamarty.
-   _Duplicity_ is one of the backends of
    {{< iref "#backupninja" "backupninja" >}}
-   _Duplicity_ has a gnome2 GUI
    [deja-dup](https://launchpad.net/deja-dup).
-   <a name="duplicati"></a>[w:Duplicati](LGPL)
    is a backup client written in C# that securely stores encrypted
    (AES 256), incremental, data deduplicated, compressed backups on
    cloud storage services and remote file servers. It is based on the
    duplicity model.  It works with: Amazon S3, OneDrive, Google
    Drive, Rackspace Cloud Files, HubiC, Backblaze (B2), Amazon Cloud
    Drive (AmzCD), Swift / OpenStack, WebDAV, SSH (SFTP), FTP. There
    is a deb package proposed on the download page, but it is not part
    of Debian.

    Among the limitations of Duplicati Wikipedia give, some flaws in
    security of the program, the fact that it is conceived to be used
    on a single machine with a display attached, it is extremely slow
    to browse files.
    -   [Duplicati Home](https://www.duplicati.com/)
    -   [Duplicati Guides](https://www.duplicati.com/articles/)
    -   [GitHub Duplicati](https://github.com/duplicati/duplicati)

# Git based
-   {{< wp "FlyBack"  "Wikipedia: FlyBack" >}},
    [FlyBack](http://flyback-project.org/)
    (GPL) is a python program that uses git is used in
    [Flyback – Snapshot-based backup tool based on rsync
    ](http://www.ubuntugeek.com/flyback-snapshot-based-backup-tool-based-on-rsync.html) and
    [Creating Snapshot-Backups with FlyBack On Ubuntu 7.10](http://howtoforge.com/creating-snapshot-backups-with-flyback-ubuntu-7.10).
    The documentation seems very scarse and the source is stalled
    since 2010.
-   Gibak is a backup tool written in ocaml. It is  based on Git and
    uses Git's hook system to save and
    restore the information Git doesn't track itself such as permissions,
    empty directories and optionally mtime fields.<br />
    The original gibak from Mauricio Fernandez is no more under active development,
    there are many dead forks.
-   [bup](https://github.com/apenwarr/bup#readme) (LGPL)
    is an incremental backup tool based on git. It is in debian.

# rsync based snapshots {#rsync_backup}

See also the {{< iref "#rsync" "rsync section" >}}

-   [Easy Automated Snapshot-Style Backups with Linux and Rsync
    ](http://www.mikerubel.org/computers/rsync_snapshots/)
    is a tutorial by Mike Rubel that induced the snapshot backup development.
-   [Do-It-Yourself Backup System Using Rsync
    ](http://www.sanitarium.net/golug/rsync_backups_2010) by Kevin Korb
-   [DebianHelp: rsync Backup Web interface or GUI Tools
    ](http://www.debianhelp.co.uk/rsyncweb.htm)
-   <a name="backintime"></a>
    [Back In Time](https://github.com/bit-team/backintime) (GPL)
    is a python frontend  for rsync. It uses hard-links as usual for
    rsync snapshots. It comes up with a QT4 gui.
    This is an active project in 2018 that is packaged in Debian.
    -   [[Back In Time Documentation
        ](http://backintime.readthedocs.io/en/latest/).
-   [Dirvish](http://www.dirvish.org/) (Open Software License)
    written in Perl.
    [Configuring and Using Dirvish for Snapshot  Backups
    ](http://wiki.edseek.com/howto:dirvish).
    _No longer an active project since 2008_
-   [Hourly Snapshot Style Backup
    ](http://wiki.excito.org/wiki/index.php/Hourly_Snapshot_Style_Backup)
    a Perl script which gives an alternative to rsnapshot.
-   [luckyBackup](http://luckybackup.sourceforge.net/) (GPL)
    is an rsync-based GUI data backup utility that uses snapshots.
    It comes with a QT gui and is available as Debian package.
-   [rlbackup (remote linked backup)
    ](http://www.math.ualberta.ca/imaging/rlbackup/)
    written in shell (year 2004) make backups with `rsync
    --link-dest.`
-   [rsbackup](http://www.greenend.org.uk/rjk/rsbackup/) (GPL)
    uses rsync with hardlinks. It is written in C++, actively
    maintained _in 2018_, and is in Debian.
    -   [rsbackup GitHub repository
        ](https://github.com/ewxrjk/rsbackup).
-   [rsync-backup](http://code.google.com/p/rsync-backup/) and
    [snapback2](http://www.perusion.com/misc/Snapback2) are
    perl scripts for rsync backup,
-   [RsyncIncr](http://colas.nahaboo.net/Software/RsyncIncr) (GPL)
    by Colas Nahaboo is a bash script that implement the maximilien Rubel
    idea with rsync.
    [RsyncIncr mercurial repository](http://hg.colas.nahaboo.net/rsync-incr/).
-   [Rsnap](http://web.chad.org/projects/rsnap/)
    is a backup and snapshot python utility based on rsync.
    _last release 2008_
-   <a name="rsnapshot"></a>[Rsnapshot](https://rsnapshot.org/)
    (GPL) written in Perl can take incremental snapshots of local and
    remote filesystems using of hard links following M Rubel
    idea. _Last release 2015, maintenance commits in 2017_.
     _Rsnapshot is packaged in Debian_
    -   [Using Rsnapshot and SSH](http://troy.jdmz.net/rsnapshot/)
        teach how to secure ssh for use with rsnapshot.
    -   [Comparing rsnapshot and obnam for scheduled large backups
        ](https://blog.karssen.org/2013/01/04/comparing-rsnapshot-and-obnam-for-scheduled-large-backups/)
-   [Rybackup](http://git.sysphere.org/rybackup/tree/)
    (git repository) from Adrian C. (anrxc) is a small (200 LOCs)
    python script based on rsync and rotating backup-snapshots.  It
    uses hard links copy but not the `--link-dest` option of rsync.
    <br /> Adrian
    [introduces his backup solution in his Blog
    ](http://sysphere.org/~anrxc/j/archives/2010/05/31/introducing_rybackup_again/index.html).
-   [S3_backup.sh](http://www.rath.org/s3ql-docs/contrib.html#s3-backup-sh)
    is an  example script  that demonstrates  how to  set up  a simple
    backup solution on amazon S3 using
    [S3QL](http://code.google.com/p/s3ql/) and rsync.
-   [TimeShift](https://github.com/teejee2008/timeshift)
    is an application written in vala that provides functionality
    similar to the System Restore feature in Windows and the Time
    Machine tool in Mac OS. Snapshots are taken using rsync and
    hard-links. TimeShift is similar to applications like
    {{< iref "#rsnapshot" "rsnapshot" >}},
    {{< iref "#backintime" "BackInTime" >}} and
    {{< iref "#timevault" "TimeVault" >}}
    but is designed to protect only system files and
    settings .o backup user data we should use
    {{< iref "#backintime" "BackInTime" >}}. It comes with a
    GTK GUI frontend.
    TimeShift is an active project _in 2018_, it is available in an
    Ubuntu ppa and in Debian since buster;
    -   [TimeShift source repository
        ](https://github.com/teejee2008/timeshift)


#  file based backups {#backup}
Some older tools where aimed to CD/DVD backups:
[scdbackup](http://scdbackup.webframe.org/main_eng.html)
(BSD License) _last release 2009_,
[cdbackup](http://www.muempf.de/) (BSD
License) _last release 2008_,
[yacdbak (Yet Another CD Backup Tool)](http://yacdbak.sourceforge.net/)
(GPL) _last release 2001_. Some other allow to do CD/DVD backup
among other backends and have recent release like
{{< iref "#dar" "DAR" >}}.

-   [afbackup](http://sourceforge.net/projects/afbackup) (GPL): a
    very robust client/server network backup tool, but with a cryptic
    documentation and the project is no longer very active nor
    maintained, yet a new release appeared in 2012 after five years of sleep.
-   [Bacula](http://en.wikipedia.org/wiki/Bacula): a network based
    backup program (GPL).
    -   [Bacula Home](http://www.bacula.org/)
    -   [bacula user manual](http://www.bacula.org/en/rel-manual),
    -   [Bacula Wiki](http://wiki.bacula.org/doku.php).
    -   {{< iref "#burp" "Burp" >}} is a fork of Bacula but with a
        different approach, it is based on librsync.
    -   [Bareos](http://www.bareos.org/en/) (AGPL) is a backup of
        Bacula, Bacula developpers [disagree with the fork
        ](http://blog.bacula.org/bareos-is-not-a-fork/).

    I have used successfully bacula to backup my servers and
    worstations, and recovered quite easily to bad data loss. It is a
    very clean and powerfull program. May be its weakness, like
    afbackup I used before bacula, is to be a one man project. All
    development, documentation and maintenance have been done by Kern
    Sibbald, it's great, it's dangerous!</br>

-   [DAR](http://dar.linux.free.fr/) (GPL) <a name="dar"></a>
    Disk ARchive support for differential backups, slices, compression,
    ATTR/ACL support. DAR also supports Pipes for remote operations,
    including with ssh. DAR is an old program but actively maintained.
-   [BackupPC](http://backuppc.sourceforge.net/)
    (GPL) is a Perl backup script
-   [rdup](http://miek.nl/projects/rdup11/) (GPL)
    is a program for incremental and full backups which allows encryption, compression,
    path encryption, remote backups. It builds on the older hdup.
-   [storebackup](http://www.nongnu.org/storebackup/) (GPL)
    Backup to another disk with reduced disk space.
    It includes tools for analyzing backup data and restoring.
-   [Linux Complete Backup and Recovery HOWTO
    ](http://www.charlescurley.com/Linux-Complete-Backup-and-Recovery-HOWTO/Linux-Complete-Backup-and-Recovery-HOWTO/)
    by Charles Curley is a step-by-step tutorial on how to back up a
    Linux computer so as to be able to rebuild it after a catastrophic
    failure. It uses a custom perl script with `tar`. _Dated 2011_

# Partition imager {#partition_image}
-   [partimage](http://www.partimage.org/) or _Partition Image_ is a
    partition imaging utility. It has support for many file systems
    The image file stores only used blocks and can be compressed in
    GZIP or BZIP2 , and split into multiple files. _partimage_ is in
    Debian.
-   [SystemImager](http://systemimager.sourceforge.net/)
    makes it easy to do automated installs (clones) of software
    distribution, content or data distribution, configuration changes,
    and operating system updates.
    -   [Systemimager. Documentation
        ](http://systemimager.sourceforge.net/documentation/)
    -   [Backing Up And Restoring Your Dedicated Server With SystemImager
    ](http://howtoforge.com/dedicated_server_backup_restore_systemimager)
    by Falko Timme explains the use of SystemImager for doing a remote
    back up, and restoring the remote server
-   [FSArchiver](http://www.fsarchiver.org/)
    is a system tool that allows you to save the contents of a
    file-system to a compressed archive file. The file-system can be
    restored on a partition which has a different size and it can be
    restored on a different file-system. It is in Debian.


# Synchronization {#synchronization}
## rsync {#rsync}
See also the {{< iref "#rsync_backup" "Section on rsync backup" >}}

-   {{< wp "rsync"  "Wikipedia: rsync" >}} is a detailled description of rsync and
    its algorithm. It also includes a list of rsync frontends.
-   [rsync web page](http://rsync.samba.org/),
    -   [rsync(1)](http://www.samba.org/ftp/rsync/rsync.html),
        [rsyncd.conf(5)](http://www.samba.org/ftp/rsync/rsyncd.conf.html),
    -   [How Rsync Works: A Practical Overview
        ](http://www.samba.org/rsync/how-rsync-works.html)

-   [rsync Tips & Tricks](http://72.14.189.113/howto/rsync/)
-   [Using Rsync and SSH](http://troy.jdmz.net/rsync/index.html)
    teach you how to set up a  secure rsync backup through ssh.
-   [Rsync mirroring howto and FAQ](http://sunsite.dk/info/guides/rsync/)
    by the rsync author Karsten Thygesen,
    is an old (1999) document but still usefull, it is mirrored
    [here
    ](http://202.201.1.130:8080/members/wangbj/wangbaojun/howtos/rsync-mirror-HOWTO/rsync-mirroring.html).
-   [rsync manual](http://www.samba.org/ftp/rsync/rsync.html)
    specify that _rsync treats a "bind" mount to the same device as
    being on the same filesystem_ we have to exclude explicitly the
    _mount bind_ points. That may be done by
    [this script](http://lists.samba.org/archive/rsync/2004-June/009739.html)
-   usefull options: `-S --sparse`, `-H, --hard-links`, `-v,
    --verbose`, `--numeric-ids`, _if interactive:_ `--progress`,
    `--partial`, _to have both:_ `-P`
-   Rsync as all I/O intensive program, can steal all your i/o
    activity,and bring down a mail server, an http server, mysql, or any other
    I/O dependent service.
    We can deal with it at the rsync command line with
    the --bwlimit option limit I/O bandwidth. It takes as
    argument the bandwidth in KBytes per second.
    For example, limit I/O banwidth to 10000KB/s (9.7MB/s):

        $ rsync --delete --numeric-ids --relative --delete-excluded \
        --bwlimit=10000 /path/to/source /path/to/dest/

-    CFQ scheduler is one way to limit  disk I/O for rsync, it is
     referenced on my page
     {{< iref "performances#io_scheduling" "Performance Tuning - Input/output scheduling" >}}.
-   You may need to control internet bandwith with the tools in the
    section
    {{< iref "performances#qos" "Performance Tuning -  Network bandwith control" >}}.

### Rsync frontends
-   [Grsync](http://www.opbyte.it/grsync/) (GPL)
    is a GTK Graphic User Interface for rsync. It is packaged in Debian.
-   [gadmin-rsync
    ](http://dalalven.dtdns.net/linux/gadmintools-webpage/app_pages/gadmin-rsync.html) (GPL)
    part of {{< wp "GADmintools" >}} ([Gadmin Tools Home
    ](http://dalalven.dtdns.net/linux/gadmintools-webpage/))
    is a C/GTK+ graphical user interface for rsync, it is packaged in
    debian. _There are also frontends for samba, proftpd, dhcpd3-server,
    openvpn-server/client, and bind9._
-   [Lsyncd](https://github.com/axkibe/lsyncd) (GPL)
    a light-weight live mirror, use inotify to watch files and rsync
    and ssh to synchronize them.
    -   [DigitalOcean: How To Mirror Local and Remote Directories
        on a VPS with lsyncd
        ](https://www.digitalocean.com/community/tutorials/how-to-mirror-local-and-remote-directories-on-a-vps-with-lsyncd)
-   [Rsyncrypto](http://rsyncrypto.lingnu.com/index.php/Home_Page)
    (GPL) allows you to encrypt a file or a directory structure.  It
    preserve locality such that the encrypted file can be synchronized
    by using rsync.  A Debian package is available.

## Other synchronization tool

-   {{< wp "Conduit" >}} (GPL)
    is a synchronization program for GNOME. It allows the user to
    synchronize photos, files, folders, RSS feeds, emails, notes,
    contacts, calendars, and tasks. It is packaged in Debian.
    -   [Conduit documentation
        ](https://live.gnome.org/Conduit/Documentation/UserDocumentation)
-   [Csync](http://www.csync.org/)
    is a client only bidirectional file synchronizer, _not to be
    confused with the following csync2 which is a cloud server
    mirroring tool_. _last stable csync-0.50.0 2013, last commit 2015,
    support owncloud_.
    [Csync manual](http://www.csync.org/userguide/csync.html).
    -   The native csync could use local, smb and sftp protocol.
    -   Klaas Freitag has added an owncloud protocol which he uses to build
        the
        [Owncloud Client](https://github.com/owncloud/client).
        Look at the [Owncloud Client Changelog
        ](https://owncloud.org/changelog/desktop/).
        and the [Klaas Freitag's blog tagged owncloud
        ](https://dragotin.wordpress.com/category/owncloud-2/)
        and [tagged csync](https://dragotin.wordpress.com/tag/csync/).
-   [Csync2]( http://oss.linbit.com/csync2/) (GPL)
    is a program to synchronizes files in a cluster using the
    rsync-algorithm through
    {{< iref "#librsync" "librsync" >}}. It maintains a
    database of modified files so it is able to handle deletion of
    files and file modification conflicts. It is provided in Debian.
    -   [csync2 git repository](http://git.linbit.com/csync2.git/)
    -   [csync2 paper](http://oss.linbit.com/csync2/paper.pdf)
        is the official information page, and configuration manual.
-   [FreeFileSync](http://freefilesync.sourceforge.net/) (GPLv3)
    is a synchronization tool written in C++. It can synchronize local
    folders, network share, or through SFTP. It is available for Linux
    _debian package_, windoze and Mac OS X. Although beeing open
    source and free, it shows an advertisement during installation,
    and there are also a payed _donation edition_.
-   [ftpsync.pl](https://savannah.gnu.org/projects/ftpsync/) (GPL)
    is a perl program for one way sync to FTP.
    following the [readme
    ](http://git.savannah.gnu.org/cgit/ftpsync.git/plain/doc/ReadMe.txt)
    it should be preferred to mirror, because
    ftpsync.pl is capable of PUTting, not only GETting stuff,
    and to sitecopy, since it can cope with a remote site changed by other
    tools and/or activites.
-   [Fullsync](https://fullsync.sourceforge.io/) (GPL) is a java
    program for mainly backup and one way synchronization over files,
    ftp, sftp, smb. It has a GUI and is available for linux, Mac OS X,
    and windoze. Two way sync is unable to manage conflicts.
    -   [FullSync documentation](https://fullsync.sourceforge.io/).
-   [lftp](http://lftp.yar.ru/) ftp client with a mirror option.
    -   [lftp mirror
        ](https://github.com/joedicastro/lftp-mirror)
        is a python wrapper around _lftp_ that extend the synchronization
        features.
-   [node-ftpsync](https://github.com/evanplaice/node-ftpsync/) (MIT
    License) is a ftp synchronizing application written in node.js, it
    seems _in 2017_ still in alpha stage with no detection of changed
    files through checksum or even timestamp.
-   [pyftpsync](https://github.com/mar10/pyftpsync/)
    is a bidirectional synchronization tool over FTP. It allows even
    FTP to FTP synchronization. pyftpsync uses file size and
    modification dates to detect file changes. This is not as robust
    as CRC checksums.
    -   [ftpsync documentation](http://pyftpsync.readthedocs.io/).
-   [syrep](http://0pointer.de/lennart/projects/syrep/)
    by Lennart Poettering   is a repository synchronization tool used to synchronize
    large file hierarchies bidirectionally by exchanging patch
    files.Files are tracked by their message digests, currently MD5.
    The patch files may be transferred via offline media,
    e.g. removable hard disks or compact discs. The last release is
    from 2006. The package is in debian.
-   [Sucsynct](https://launchpad.net/sucsynct) (GNU Affero GPL)
    is a bash distributed backup and syncing, triggered whenever a file in
    a watched replica changes. It requires unison at all  hosts,
    ssh-client on all initiating hosts, and ssh-server on all
    hosts to sync with from remote. _The project seems dead, nothing
    since 2012._
-   [Synkron](http://synkron.sourceforge.net/) (GPL)
    is a  C++-Qt application  for synchronising two or more folders.
    [Synkron manual](http://sites.google.com/site/synkrondocumentation/)
-   [Unison](http://www.cis.upenn.edu/~bcpierce/unison/) (GPL):
    an Ocaml file-synchronization tool that uses the rsync algorithm.
    -   [Manual for the stable version of Unison
        ](http://www.cis.upenn.edu/~bcpierce/unison/download/releases/stable/unison-manual.html)
        and [Manual for the development version of Unison
        ](http://www.cis.upenn.edu/~bcpierce/unison/download/releases/beta/unison-manual.html)
    -   [ArchWiki: Unison](https://wiki.archlinux.org/index.php/unison)
    -   [Markus Gattol Unison Page
        ](http://www.markus-gattol.name/ws/unison.html)
-   [Zsync](http://zsync.moria.org.uk/) (Artistic License)
    is a differential file transfer program to download files from
    remote web servers. It uses the same algorithm as rsync, but does
    not require any server software. The remote state is registered on
    the client side. It uses http for the data transfer.<br /> _Zsync_
    has special handling for gzipped files, which enables update
    transfers of gzip compressed files.  A Debian package is provided.
    Zsync has no dependency but libc.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
