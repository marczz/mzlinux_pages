---
title: Encrypted File Systems
---

See also the companion pages on
{{< iref "filesystems" "filesystems" >}},
{{< iref "network_filesystems" "network filesystems" >}}.

And also other reference on encryption:
{{< iref "encrypt" "Encryption" >}},
{{< iref "authentication" "Authentication" >}},
{{< iref "security" "Security" >}}.

----

# General References
-   Wikipedia {{< wp "Comparison of disk encryption software" >}}.
-   [ArchWiki: Disk Encryption
    ](https://wiki.archlinux.org/index.php/Disk_Encryption)
    includes a very good
    [Encryption comparison table
    ](https://wiki.archlinux.org/index.php/Disk_Encryption#Comparison_table).
-   [RSA Laboratories' Crypto FAQ
    ](http://www.rsasecurity.com/rsalabs/node.asp?id=2152)
-   [Securely wipe disk - ArchWiki
    ](https://wiki.archlinux.org/index.php/Securely_wipe_disk)

-   [Sirikali](https://mhogomchungu.github.io/sirikali/)
    provides a Qt/C++ GUI front end to cryfs,gocryptfs,securefs and
    encfs, allowing the user to create, mount, and unmount encrypted
    volumes. It is in Debian.
    -   [GitHub: Sirikali](https://github.com/mhogomchungu/sirikali)
-   [zuluCrypt](https://mhogomchungu.github.io/zuluCrypt/)
    does hard drives encryption and it can manage PLAIN dm-crypt
    volumes, LUKS encrypted volumes, TrueCrypt encrypted volumes and
    VeraCrypt encrypted volumes. zuluCrypt is provided in the Debian
    packages _zulucrypt-cli_ and _zulucrypt-gui_ and
    _zulusafe-cli_ (responsible for the safe storage files in a wallet).

    zuluMount bundled with zuluCrypt mount and unmount zuluCrypt
    supported encrypted volumes as well as unencrypted volumes
    and it can be used as a substitute to udisks, pmount and related
    tools. zuluMount-gui can also be used as a frontend to encfs,
    gocryptfs, securefs, ecryptfs and cryfs. It is in the Debian package
    _zulumount-cli_.
    -   [GitHub: zuluCrypt](https://github.com/mhogomchungu/zuluCrypt)

# Loop Aes
 Loop aes (GPL) is an older project but still maintained.

-   [Loop-Aes sourceforge Home](http://loop-aes.sourceforge.net/)
    and [ReadMe](http://loop-aes.sourceforge.net/loop-AES.README)
-   [Gentoo Wiki:  AES-encrypted root partition using LVM2
    ](http://gentoo-en.vfose.ru/wiki/AES-encrypted_root_partition_using_LVM2)
-   [Gentoo Wiki: Linux Disk Encryption Using LoopAES And SmartCards
    ](http://gentoo-en.vfose.ru/wiki/Linux_Disk_Encryption_Using_LoopAES_And_SmartCards)

# dm-crypt {#dm-crypt}
-   [dm-crypt Home](https://gitlab.com/cryptsetup/cryptsetup/wikis/DMCrypt)
    device-mapper crypto target.
-   __Luks__ is the
    standard for Linux hard disk encryption. LUKS for dm-crypt
    is implemented in an enhanced version of cryptsetup.
    [Cryptsetup and LUKS - open-source disk encryption
    ](https://gitlab.com/cryptsetup/cryptsetup)
    is the Luks Home page
-   Wikipedia  {{< wp "dm-crypt" >}}
-   [Luks FAQ
    ](https://gitlab.com/cryptsetup/cryptsetup/wikis/FrequentlyAskedQuestions)
-   [dm-crypt git repository
    ](https://git.kernel.org/cgit/utils/cryptsetup/cryptsetup.git/)
-   [Kernel.org cryptsetup releases
    ](https://www.kernel.org/pub/linux/utils/cryptsetup/)
    with  the release notes.
-   ArchWiki:
    [dm-crypt](https://wiki.archlinux.org/index.php/Dm-crypt),
    [dm-crypt/System configuration
    ](https://wiki.archlinux.org/index.php/Dm-crypt/System_configuration),
    [dm-crypt/Device encryption
    ](https://wiki.archlinux.org/index.php/Dm-crypt/Device_encryption),
    [dm-crypt/Drive preparation
    ](https://wiki.archlinux.org/index.php/Dm-crypt/Drive_preparation),
    [dm-crypt/Encrypting a non-root file system
    ](https://wiki.archlinux.org/index.php/Dm-crypt/Encrypting_a_non-root_file_system),
    [dm-crypt/Encrypting an entire system
    ](https://wiki.archlinux.org/index.php/Dm-crypt/Encrypting_an_entire_system),
    [dm-crypt/Specialties
    ](https://wiki.archlinux.org/index.php/Dm-crypt/Specialties)
-   [Ubuntu Help EncryptedFilesystems
    ](https://help.ubuntu.com/community/EncryptedFilesystems)
    is the index page for all encrypted disk and filesystem guides.
    -   [Ubuntu Encrypted file-systems HowTo 3: Encrypted Swap and Home with LUKS
        ](https://wiki.ubuntu.com/EncryptedFilesystemHowto3)
-   [HOWTO: Disk encryption with dm-crypt / LUKS and Debian
    ](http://www.hermann-uwe.de/blog/howto-disk-encryption-with-dm-crypt-luks-and-debian)
    by Uwe Hermann.
-   [Gentoo wiki: Dm-crypt full disk encryption
    ](https://wiki.gentoo.org/wiki/Dm-crypt_full_disk_encryption).



# Encfs {#encfs}

As encfs is built on the top of Fuse look also at the
{{< iref "filesystems#fuse" "Fuse section" >}}

-   [EncFS Encrypted Filesystem](https://vgough.github.io/encfs/)(GPL) uses
    the FUSE library and Linux kernel module to provide the filesystem
    interface.Encfs is different from the loopback encrypted filesystem
    because it works on files at a time, not an entire block device.
-   [Encfs GitHub repository](https://github.com/vgough/encfs).
-   [EncFS Introduction
    ](https://sites.google.com/a/arg0.net/www/encfs)
-   [EncFS Manpage
    ](https://github.com/vgough/encfs/blob/master/encfs/encfs.pod)
-   Wikipedia: {{< wp "Encfs" >}}
-   [ArchWiki: EncFS](https://wiki.archlinux.org/index.php/EncFS)
    is a detailled article that
    includes a comparison with
    {{< iref "#ecryptfs" "Ecryptfs" >}}, which stand that
    _EncFS is definetely the simplest software
    if you want to try disk encryption on Linux_
-   [Gentoo Wiki: encfs](https://wiki.gentoo.org/wiki/Encfs)
-   [Cryptkeeper](http://tom.noflag.org.uk/cryptkeeper.html) (GPL)
    is a Linux system tray applet that manages EncFS encrypted folders.
    It is packaged in Debian
-   [Debian Wiki: Transparent Encryption For Home Folder
    ](https://wiki.debian.org/TransparentEncryptionForHomeFolder)
    use _encfs_.
-   [encfsui](https://github.com/bulletmark/encfsui) is a bash script
    that provides a simple gui around _encfs_ to mount and unmount an
    encrypted directory. This script requires encfs, zenity, and
    xdg-open.
-   [Encdroid](https://github.com/mrpdaemon/encdroid)
    is an Android application for accessing EncFS volumes on cloud
    storage.
-   [enc](https://github.com/erlcash/enc) is a bunch of bash functions
    to manage encfs.
-   [encfsgtk](https://github.com/wolfprogrammer/encfsgtk)
    a python/gtk interface to encfs.

# Ecryptfs {#ecryptfs}

-   [eCryptfs](http://ecryptfs.org/)
    is a stacked cryptographic filesystem for Linux. It is available in Debian.
-   [ecryptfs man pages](http://ecryptfs.org/documentation.html)
-   [ecryptfs faq](http://ksouedu.com/doc/ecryptfs-utils/ecryptfs-faq.html)
-   [kernel documentation for ecryptfs
    ](https://www.kernel.org/doc/Documentation/filesystems/ecryptfs.txt).
-   [Stack Exchange ecryptfs QA](http://stackexchange.com/filters/33360/ecryptfs) (
    [ecryptfs search](http://stackexchange.com/search?q=ecryptfs)),
    [StackOverflow Question tagged ecryptfs
    ](http://stackoverflow.com/questions/tagged/ecryptfs)
-   [Ubuntu: Encrypted Private Directory motivation and specification](https://wiki.ubuntu.com/EncryptedPrivateDirectory) and a complete
    [Tutorial](https://help.ubuntu.com/community/EncryptedPrivateDirectory)
    including the encrypted directory recovery.
-   [Gentoo wiki: Ecryptfs](https://wiki.gentoo.org/wiki/Ecryptfs)
    describe the basic use of a pam mounted private directory.
-   [ArchLinux: eCryptfs](https://wiki.archlinux.org/index.php/eCryptfs)
-   Adrian C. (anrxc): [eCryptfs and $HOME](http://sysphere.org/~anrxc/j/articles/ecryptfs/index.html)
    is a detailed tutorial on ecryptfs.
-   [bodhizazen tutorial:Ecryptfs](http://bodhizazen.net/Tutorials/Ecryptfs)
-   Linux Journal: [eCryptfs: a Stacked Cryptographic Filesystem](http://www.linuxjournal.com/article/9400) by Mike Halcrow
-   [Dustin Kirkland ecryptfs posts](http://dustinkirkland.wordpress.com/category/ecryptfs/)
-   Markus Gattol has an uptodate,  big, _even too fat, at my own taste_
    [Debian Security manual _Security - Technology and Humans_
    ](http://www.markus-gattol.name/ws/debian_security.html)
    with a chapter on
    [Filesystem-level Encryption
    ](http://www.markus-gattol.name/ws/debian_security.html#filesystem-level_encryption)
    with a detailed description and use case of Ecryptfs.

# VeraCrypt and Truecrypt
Development on TrueCrypt is discontinued since May 2014.
Alternatives are dm-crypt or forks of Truecrypt like _tcplay_,
_zuluplay_, _Veracrypt_  see the also alternatives in Archlinux Wiki.

-   Wikipedia: {{< wp "TrueCrypt" >}}
-   Wikipedia: {{< wp "BitLocker" >}} is the official replacement of Truecrypt
    on windows developped by microsoft.
-   [TrueCrypt Homepage](http://www.truecrypt.org/)
-   [ArchWiki: TrueCrypt](https://wiki.archlinux.org/index.php/TrueCrypt)
-   [Gentoo Wiki:  TrueCrypt](http://en.gentoo-wiki.com/wiki/TrueCrypt)
-   [tc-play (GitHub)](https://github.com/bwalex/tc-play) (BSD)
    a BSD licenced implementation of TrueCrypt.
-   [zuluplay](https://github.com/mhogomchungu/zuluplay)
    is a fork of tcplay that support VeraCrypt volumes.
-   [ArchLinux: tcplay](https://wiki.archlinux.org/index.php/Tcplay)
-   {{< wp "VeraCrypt" >}} is a fork and continuation of Truecrypt it supports
    {{< wp "VeraCrypt#Plausible_deniability"  "Plausible deniability" >}}.

Miscellaneous
:

-   [Elettra](http://www.winstonsmith.info/julia/elettra/)
    provide a {{< wp "deniable encryption" >}} as introduced in
    [phrack issue 65](http://www.phrack.org/issues.html?issue=65)

# Cryfs
[Cryfs](https://www.cryfs.org/) is an encryption system aimed to
encrypt in the cloud, like Dropbox, iCloud, OneDrive and others.
Cryfs is in Debian.

-   [GitHub: Cryfs](https://github.com/cryfs/cryfs)


# Gocryptfs

[gocryptfs](https://nuetzlich.net/gocryptfs/) is built on top of
[go-fuse](https://github.com/hanwen/go-fuse)
and its LoopbackFileSystem API.

This project was inspired by EncFS and strives to fix its security issues.

Gocryptfs is in Debian.

-   [GitHub: gocryptfs](https://github.com/rfjakob/gocryptfs)
-   [gocryptfs comparison and benchmarks](https://nuetzlich.net/gocryptfs/comparison/).

# Keybase
<a name="keybase">[keybase](https://keybase.io/) (BSD Licence)
is a security app for mobile phones and computers powered by
public-key cryptography.
-   [Keybase Book](https://book.keybase.io/) documentation for Keybase.
-   [Keybase server documentation](https://book.keybase.io/docs/server).

Keybase group several services

Keybase Chat
:   see the {{< iref "xmpp#keybase_chat" "entry in the messaging page" >}}

[Keybase for Files](https://book.keybase.io/files)
:   store and share end-to-end encrypted and signed files from any device you use
    Keybase on. You can store up to 250 GB.

    Keybase files are served in a fuse mounted directory under `/keybase` hierarchy.

    -   [Introducing the Keybase Filesystem](https://book.keybase.io/docs/files).
    -   [In depth description of the Filesystem
        ](https://book.keybase.io/docs/files/details)
    -   [Crypto spec: the Keybase filesystem](https://book.keybase.io/docs/crypto/kbfs).

[Keybase Git](https://book.keybase.io/git)
:   Keybase supports free, encrypted, authenticated, and private Git repositories.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
