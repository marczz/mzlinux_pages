---
title: Password Managers
---

_See also  {{< iref "authentication" "Authentication" >}},
{{< iref "security" "Security" >}},
{{< iref "../network/network" "Network Security" >}}._

---

A {{< wp "Password_manager"  "Password Manager" >}} holds your passwords in an
encrypted local database. Some password managers comes under the form
of a desktop application, others are web based, last some mobile
device application are also available.

-   [PasswordManagementService - SoftwareComparison
    ](https://wiki.koumbit.net/PasswordManagementService/SoftwareComparison)
    list _more than compare_ GPL password managers.

# Keyring

-   [FreeDeskop Secret Service API
    ](https://specifications.freedesktop.org/secret-service/)
    allows client applications to store secrets securely in a service running in the
    user's login session.  *gnome-keyring* and *ksecretservice* are both
    implementations of a Secret Service; {{< iref "#keepassxc" "KeepassXC" >}} can also be
    configured to provide the secret service API.

    Each secret is stored together with lookup attributes and a label. These together
    form an item.  A group of items together form a collection wich is what used to be
    called _keyring_.

    Client applications use lookup attributes to find items.

    A collection can have two states: _unlocked_ where items are accessible for reading
    and modifying, _locked_ where items cannot be read or modified. Some service may
    also define locking state item by item.

    Even if the user access secret by attribute. Each secret has also an _object path_
    which look like:

        /org/freedesktop/secrets/collection/xxxx/iiii

    where `xxxx` is the collection and `iiii` is an auto-generated item specific
    identifier.

    The default collection for client applications to store secrets is available under
    the path:

        /org/freedesktop/secrets/aliases/default

    -   [Libsecret](https://wiki.gnome.org/Projects/Libsecret) is a library for storing
        and retrieving passwords and other secrets. It communicates with the "Secret
        Service" using D-Bus. It [replaces the old libgnome-keyring
        ](https://wiki.gnome.org/Initiatives/GnomeGoals/LibsecretMigration).
    -   [Libsecret Library Reference Manual
        ](https://gnome.pages.gitlab.gnome.org/libsecret/).
    -   [GNOME / libsecret · GitLab](https://gitlab.gnome.org/GNOME/libsecret)
    -   The utility [secret-tool
        ](https://manpages.debian.org/unstable/libsecret-tools/secret-tool.1.en.html)
        is a command line tool to store and retrieve passwords. It is in its own package
        _libsecret-tool_.
    -   [SecretStorage](https://secretstorage.readthedocs.io/en/latest/)
        is a Python module for storing secrets using the D-Bus-based FreeDesktop.org
        Secret Service standard, supported by GNOME Keyring and KSecretsService.  It
        allows one to create, edit and delete secret items, manipulate secret
        collections, and search for items matching given attributes. It also supports
        locking and unlocking collections. It is in the Debian package
        _python3-libsecretstorage_.

-   [Gnome Keyring](https://wiki.gnome.org/Projects/GnomeKeyring)
     is "a collection of components in GNOME that store secrets, passwords, keys,
     certificates and make them available to applications.
    -   [ArchWiki Gnome-keyring](https://wiki.archlinux.org/index.php/GNOME/Keyring)

-   [Seahorse](https://wiki.gnome.org/Apps/Seahorse)
    is a GNOME application for managing encryption keys and passwords in the GNOME Keyring.
    Seahorse integrates with Nautilus, gedit and Evolution for encryption, decryption
    and other operations. It has HKP and LDAP key server support.

# Desktop password managers

Desktop password managers are usually written in Qt or Gtk+ (or Tk)
and they will eat between 10M and 20M of your resident memory (less if
you truly share the libraries). As they can stay open during a whole
session the memory and swap protection is a primary concern.

A comparison of main features of Password managers is givn in
[Password Management Service - Software Comparison](https://wiki.koumbit.net/PasswordManagementService/SoftwareComparison).


-   <a name="fpm2"></a>[Fpm2](http://als.regnet.cz/fpm2/)(GPL) is a GTK2 port from
    [Figaro's Password Manager](http://fpm.sourceforge.net/)
    Passwords are encrypted with the AES-256 algorithm. It can copy
    passwords or usernames to the clipboard/primary selection and keep
    track of the URLs of the login screens of web sites. You can
    export your entries in clear text or own Fpm2 xml format.  <br />
    Fpm2 has a GTK+ 2.x GUI but does not depends on a peculiar
    desktop.
    -   [Fpm2-Android](https://github.com/braiden/fpm2-android)
        provides read-only access to FPM2 password database on Android.
-   [GPass](http://projects.netlab.jp/gpass/)
    (GPL) is a password manager for Gnome. GPass encrypts the the
    password file by using Blowfish encryption.  It has a quite heavy
    dependency to a full Gnome desktop environment.
-   [Gringotts](http://gringotts.berlios.de/)
    is a gtk+ password manager, it put a strong emphasis on security,
    trying to protect his memory to any outer access. It stores
    unstructured information so it ignores what is a username, site or
    password and can only paste selection. It does not offer any data
    export
-   [Ked Password Manager](http://kedpm.sourceforge.net/)
    (GPL) is a python password manager, it is a replacement for
    [Figaro password manager](http://fpm.sourceforge.net/)
    or {{< iref "#fpm2" "Fpm2" >}}.
    Ked has both a  CLI and GTK2 based GUI front-ends.
-   [revelation](http://oss.codepoet.no/revelation/) (GPL)
    is a password manager for the GNOME 2 desktop. It organizes
    accounts in a tree structure, and stores them as AES-encrypted
    XML.  Revelation is written in python and depends of the
    python-gnome2 libraries.  A package is available for Ubuntu and
    Debian.  <br />
    You can read more on Revelation in this
    [Revelation review by Eric Fleming
    ](http://www.associatedcontent.com/article/730289/revelation_my_favorite_password_manager.html)
-   [Shamir's Secret Sharing Scheme (ssss)](http://point-at-infinity.org/ssss/)
    allows a secret to be split in to shares. These shares can then be distributed to
    different people. When the time comes to retrieve the secret then a preset number of
    the shares need to be combined.
-   [Universal Password Manager (UPM)](http://upm.sourceforge.net/)
    (GPL) is a java password manager availabe on Linux, Android,
    windows that encrypt its database with AES.

# KeePass (GPL) {#keepass}

[KeePass](http://keepass.info/) is a password manager for Windows written in C++ (v1) or
C#.  It is also available for ios, android and linux.  Keepass stores many different
information in a database encrypted {{< wp "AES" >}} for database v3 i.e. keepass 1.x
and v4 i.e. keepass 2.x or {{< wp "Twofish" >}} only for v3.

-   [Awesome Keepass](https://github.com/lgg/awesome-keepass)
    is a list of Keepass resources [this Tiki page
    ](https://suite.tiki.org/KeePass) also explore Keepass resources.
-   Wikipedia: {{< wp "KeePass" >}}
-   Two versions of Keepass are availables 1.x and 2.x, they use a
    different database format.
-   Keepass 2.x is a portable application written in mono that run
    in n Windows Vista and higher, Linux, Mac OS X, etc.
    The [ KeePass Edition Comparison
    ](http://keepass.info/compare.html) give a detailled table of
    similarities/differences. A package is available in Debian.
-   <a name="keepassx"></a>[KeePassX](http://www.keepassx.org/) (GPL)
    is a clone of Keepass written in C with a QT GUI.  Databases
    created by KeePassX 0.4.3 are binary-compatible with databases v3
    created by KeePass 1.x _standard suffix_ `.kbd`.  The new releases
    since  2.0 of KeepassX support databases v4 of KeePass 2.x _standard
    suffix_ `.kbdx`.  KeePassX dependencies are limited to QT
    libraries.  A package is available for Ubuntu and Debian.
    -   [KeePassX GitHub repository](https://github.com/keepassx/keepassx)
    -   KeePassX can copy passwords or usernames to the
        clipboard/primary selection and keep track of the URLs of the login
        screens of web sites. You can export your entries in CSV
        clear text or own xml format and import it from KeePassX xml,
        Kwallet xml, PwManager or from
        {{< iref "#password_gorilla" "password gorilla" >}} CSV.
-   <a name="keepassxc">[KeepassXC](https://keepassxc.org/) (GPL) is a fork or KeepassX,
    written in C++ with many additional features, including two factor authentication
    with Yubikey or OTP.  Packages are available for Linux, Windows, OS X.  The
    repository is in 2021 very active, while KeepassX itself is sleeping. Debian has a
    _KeepassXC_ package.

    KeePassXC currently uses the KeePass 2.x (.kdbx) password database format, but can
    import  KeePass 1.x databases.

    -   The project live on GitHub as
        [keepassxreboot](https://github.com/keepassxreboot/)
    -   [KeePassXC: Getting Started Guide
        ](https://keepassxc.org/docs/KeePassXC_GettingStarted.html)
    -   [KeePassXC: User Guide](https://keepassxc.org/docs/KeePassXC_UserGuide.html).
    -   [EFF - Surveillance Self-Defense](https://ssd.eff.org/) :
        [How to: Use KeePassXC](https://ssd.eff.org/en/module/how-use-keepassxc).
    -   KeepassXC support `org.freedesktop.secrets.service` which can also be provided
        by gnome-keyring, kde-wallet.

        The configuration is explained in [KeepassXC and secret service, a small
        walk-through.](https://avaldes.co/2020/01/28/secret-service-keepassxc.html).
    -   __keepassxc-cli__ is the command line client for Keypassx, it allows to do many
        operation _including the XML export_ with a command line client.

        But the operations on extended attributes are not availables.
    -   [KeePassXC Browser Extension
        ](https://github.com/keepassxreboot/keepassxc-browser)
        is compatible with Firefox or Chrome/Chromium or Microsoft Edge.
        Its use is described in [Setup Browser Integration Guide
        ](https://keepassxc.org/docs/KeePassXC_GettingStarted.html#_setup_browser_integration).

        The extension is provided in Debian package _webext-keepassxc-browser_.
    -   No application is provided for mobile, but KeepassXC site recommend
        for Android {{< iref "#keypassdx" "KeePassDX" >}}
        and {{< iref "#keypass2android" "KeePass2Android" >}};
        for iOS, [Strongbox
        ](https://itunes.apple.com/us/app/strongbox-password-safe/id897283731)
        _commercial 50$/y_  and
        [KeePassium
        ](https://apps.apple.com/us/app/keepassium-keepass-passwords/id1435127111)
        _commercial 50$/y_.

-   The standard CSV format for Keepass and KeepassX(C) is

    "Group","Account","Login Name","Password","Web Site","Comments"

    or _same fields with a different header_:

    "Group","Title","Username","Password","URL","Notes"

    -   [Keepass2 CVS importer help
        ](https://keepass.info/help/kb/imp_csv.html)
    -   [KeePassXC: Importing CSV files
        ](https://keepassxc.org/docs/KeePassXC_UserGuide.html#_importing_csv_file)

-   KeePass has a huge [list of plugins and extensions
    ](http://keepass.info/plugins.html) but most of them restricted to windoze.
-   [keepass-diff](https://github.com/Narigo/keepass-diff) (MIT License)
    is a A CLI-tool to diff Keepass (.kdbx) files. Useful, if syncing with some cloud
    or *syncthing* and getting multiple files due to conflicts.

## Keepass alternative CLI
-   <a name="keepassc">[KeePassC](https://github.com/raymontag/keepassc) (GPL)
    is a Python 3 curses-based password manager compatible to KeePass v.1.x only and
    KeePassX. No more developed since 2018. The author Karsten-Kai König
    _raymontag_, produced also the library  {{< iref "#kppy" "Kppy" >}}.
-   [kpcli](http://kpcli.sourceforge.net/) (Perl artistic Licence)
    is a command line perl interface to KeePass 1.x or 2.x database files
-   [passhole](https://github.com/purdueLUG/passhole) (GPL)
    is a CLI interface for KeePass 1.x (v3) and 2.x (v4) databases with support for
    dmenu inspired by pass.
-   <a name="keepmenu"></a>[keepmenu](https://github.com/firecat53/keepmenu)
    (MIT License)
    is a  Dmenu/Rofi frontend for managing Keepass databases inspired by _passhole_.
    It is based on the Python library {{< iref "#pykeepass" "pykeepass" >}}.
    _keepmenu is [in Pypi](https://pypi.org/project/keepmenu/).
-   [kp2](https://github.com/tobischo/kp2) (MIT)
    is a go language commandline tool for accessing Keepass 2 files (kdbx).

## Keepass web clients
-   [keepass.io](https://github.com/NeoXiD/keepass.io) (GPL) is a
    KeePass database reader in NodeJS. _last commit 09/2016 checked 03/2021_
-   [KeePass-Node](https://github.com/gesellix/keepass-node) (Apache License)
    Node.js with AngularJS implementation of a KeePass2 editor with a browser frontend .
-   [BrowsePass](https://bitbucket.org/namn/browsepass) (GPL)
    is a web application to read KDBX files, as produced by KeePass.
    BrowsePass also has a Chrome extension.
-   [keepass4web](https://github.com/lixmal/keepass4web/) (GPL)
    Application that serves KeePass database entries on a web frontend.
-   [keeweb](https://github.com/keeweb/keeweb) (MIT License)
    a password manager written in Node compatible with KeePass. The app can run either
    in browser, or as a desktop app. A deb package is available in the releases. An
    online frontend is at [app.keeweb.info](https://app.keeweb.info/). It is an ctive
    project in 2021.
    -   [nextcloud-keeweb](https://github.com/jhass/nextcloud-keeweb) (MIT License)
        integrate Keeweb into Nextcloud.
-   [CliPass](https://github.com/bartlomiej-dudala/clipass) (MIT License)
    is a PHP tool to connect and gather data from KeePass 2.x It
    uses KeePassHttp plugin, as the browser plugins PassIFox or chromeIPass.
    _last commit november 2015_

## Keepass Mobile applications
 -   [KeePassDroid](http://www.keepassdroid.com/) (components with
    various open source licenses) is a port of
    KeePass  for the Android platform it support both v3 and v4
    databases.
-    <a name="keypass2android"></a>
    [Keepass2Android](http://keepass2android.codeplex.com/) (GPL)
    has an user interface based on Keepassdroid , ported from Java to Mono for
    Android. The backend uses the original KeePass libraries to handle file access to
    ensure file format compatibility (database v4).
-   <a name="keypassdx"></a>
    [KeePassDX (github)](https://github.com/Kunzisoft/KeePassDX) (GPL)
    has support for .kdb and .kdbx files (version 1 to 4) with AES - Twofish - ChaCha20 -
    Argon2 algorithm. It allows AutoFill and provide a field filling keyboard
    It is available in F-Droid repository.

## Keepass browser plugins
-   [KeePassHttp](https://github.com/pfn/keepasshttp/)
    is a plugin for KeePass 2.x exposing KeePass entries via HTTP
    for clients to consume. it is used in
    [passifox](https://github.com/pfn/passifox/) which are
    extensions  to allow Chrome and Firefox (4.0+)
    to auto form-fill passwords from KeePass.
-   <a name="kee"></a>[Kee](http://kee.pm) (GPL)
    ([gitHub Repository](https://github.com/kee-org/browser-addon))
    is a bridge between Firefox and KeePass.
-   [KeepassXC-Brower for Firefox
    ](https://addons.mozilla.org/en-US/firefox/addon/keepassxc-browser/)
    and [KeePassXC-Browser for Chrome
    ](https://chrome.google.com/webstore/detail/keepassxc-browser/)
    are the official KeepassXC extensions. They discourage the use of _KeePassHttp_
    which is not secure.


## Keepass interface libraries
-   [libkeepass](https://github.com/libkeepass/libkeepass)
    is a Python module to read KeePass 1.x/KeePassX (v3)
    and KeePass 2.x (v4) files. Write is not supported.
    Argon2 key derivation and ChaCha20 encryption are unsupported.It is in the way to be
    deprecated for the following _pykeepass_  but still active in
    november 2018.
-   <a name="pykeepass"></a>[pykeepass](https://github.com/libkeepass/pykeepass)
    (GPL-3.0) is a library to read and write entries to a KeePass database (supports
    KDBX3 and KDBX4). It is in Pypi and the Debian package _python3-pykeepass_. It is
    used in the cli application{{< iref "#keepmenu" "keepmenu" >}}.  _active in Mars
    2021_.

    See also the fork [pschmitt/pykeepass](https://github.com/pschmitt/pykeepass).
-   [Python KeepassX](https://github.com/jamesls/python-keepassx)
    allow read access to Keepass v3 databases. The goal is to provide
    a CLI access to KeepassX; Seem to have stopped in 2015.
-   <a name="kppy">[kppy](https://github.com/raymontag/kppy)
    a python 3 module to read/write Keepass1.x database, no longer developed since 2018.
    The author, Karsten-Kai König _raymontag_, authored also
    {{< iref "#keepassc" "keepassc" >}}.

## Keepass database conversion

-   [lastpass-to-keepass](https://github.com/tibdex/lastpass-to-keepass)
    is a javascript application to  convert the LastPass CVS export
    to a KeePass XML import you can
    [find it online here](https://tibdex.github.io/lastpass-to-keepass/).
-   [lastpass2keepass](https://github.com/anirudhjoshi/lastpass2keepass)
    is a python script that allow you to convert the LastPass export
    to a KeePass XML import.

## Keepass database cracking

-  [A Case Study in Attacking KeePass
   ](https://www.harmj0y.net/blog/redteaming/a-case-study-in-attacking-keepass/)
   This study suppose an attacker having administrative rights on the user deskstop; so
   able to either start a keylogger, or slurp the keepass database. It uses
   {{< iref "authentication#hashcat" "hashcat" >}} or a custom python
   script to attack the database, some other methods (DAPI) are specific to windows.
-  [KeeThief – A Case Study in Attacking KeePass Part 2
   ](http://www.harmj0y.net/blog/redteaming/keethief-a-case-study-in-attacking-keepass-part-2/)
   the follow-up of the previous article, describe the use of _KeeFarce_ and
   _KeeThief_.
-   [How to Hack KeePass Passwords using Hashcat
    ](https://www.rubydevices.com.au/blog/how-to-hack-keepass) uses the popular hash
    cracker {{< iref "authentication#hashcat" "hashcat" >}}.

# Password Safe family
<a name="password_safe"></a>[w:Password Safe](Artistic License)
is a Windoze password manager. It now has a Linux Beta version.  In
the database v3 the passwords are sha256 hashed, and the database is
ancrypted with the Twofish algorithm.

-   [Password Safe Home](http://passwordsafe.sourceforge.net/)
-   [Password Safe Linux version
    ](http://passwordsafe.sourceforge.net/)
    (Artistic License)
    is a GTK+ / C++ program .available as source or compiled packages
    for debian, Ubuntu, Fedora.  It does not have yet all windoze
    program features.
    -   The memory footprint on Linux is 32M resident / 17 shared.
    -   Password Safe allows auto-typing of passwords.
-   The format of the password safe database is used by numerous
    applications, a sample of open sources applications available on
    Linux follows.
-   [Android Port: passwdsafe
    ](https://sourceforge.net/apps/mediawiki/passwdsafe/index.php)
    (Artistic License).<br />
-   Official list of [Password Safe related projects
    ](http://pwsafe.org/relatedprojects.shtml).
-   <a name="loxodo"></a>[Loxodo
    ](http://www.christoph-sommer.de/loxodo/) (GPL)
    is a Python application that uses {{< iref "#password_safe" "Password Safe" >}}
    v3 database format. [Loxodo GitHub repository
    ](https://github.com/sommer/loxodo).
-   [MyPasswordSafe](http://www.semanticgap.com/myps) (GPL)
    <a name="mypasswordsafe"></a> is a  QT application
    that uses Blowfish algorithm to encode passwords.
    MyPasswordSafe write to Password Safe db format v1 or v2
    <br /> My Password Safe is a
    simple password manager with a Gui but without bell and whistles,
    so it is small, and has few dependencies (out of  libqt3-mt).
    <br />
    MyPasswordSafe is no longer active the last release is from 2006
    and the doc is no longer updated since 2004.
    For the release  0.0.20050615-2.1 (last version in debian, has been
    updated in Ubuntu)
    I experienced numerous fatal errors
    errors of reading and writting database that make its use quite a
    challenge. So I shifted to password Gorilla
    that uses the same database format ( plus the v3 format), but is more stable.
-   [Password Gorilla](https://github.com/zdia/gorilla/wiki/) (GPL)
    <a name="password_gorilla"></a>
    is a cross platform application written in TCL/Tk. It stores
    passwords in a securely encrypted file, and can also copy your
    user name and password to the clipboard to help Web
    authentication.  <br />
    The main documentation is the
    [Help File](http://www.fpx.de/fp/Software/Gorilla/help.html).
    Password Gorilla uses a {{< iref "#passord_safe" "passwordsafe" >}} compatible
    database version 2 or 3. _Look at help file for comparison_.<br/>
    The memory foot print of password gorilla is 12M resident / 5M
    shared.<br />
    It can export to or import from plain text csv.<br />
    Password Gorilla is available in Ubuntu and Debian.
-   <a name="pwsafe"></a>[pwsafe](http://nsd.dyndns.org/pwsafe/) (GPL)
    is a command line client written in C++ that uses a database in
    the password safe 1 or 2 format.  It is also compatible with
    _MyPasswordSafe_ and _Password Gorilla (limited to v2 database)_
    which use the same database format. The code is dated 2005 with
    some fixes until 2007, so it cannot manage passwordsafe v3
    databases.<br />
    __pwsafe__ can copy to x11 selection/clipboard.
    <br />
    A new fork [gpwsafe](https://github.com/sakhnik/gpwsafe) update
    _pwsafe_ and allows the use of a v3 database.
-   [pwsafe.el](https://github.com/emacsmirror/pwsafe)
    is an  emacs interface to pwsafe.
-   <a name="pypwsafe"></a>[pypwsafe
    ](https://github.com/ronys/pypwsafe) (GPL)
    is a pure python library that support
    {{< iref "#password_safe" "password safe" >}} database V3.
-   [Java PasswordSafe (jpwsafe)
    ](http://sourceforge.net/projects/jpwsafe/)
    is a java clone of passwordsafe

# Console password Managers

-   [Pwman3](http://pwman3.github.io/pwman3/)xs
    (GPL) is a console based password manager written in python that
    stores passwords in a sqlite database encrypted with Blowfish, AES
    or DES3 algorithm. It is available in Debian.
    -   [pwman3 manual](http://pwman3.readthedocs.io/en/latest/)
-   [Sala](http://pypi.python.org/pypi/sala/) (MIT License)
    is a python application that store passwords and other bits of
    sensitive plain-text information to encrypted files on a directory
    hierarchy. The information is protected by GnuPG's symmetrical
    encryption. _Stalled since 2012_
-   [YAPET - Yet Another Password Encryption Tool
    ](http://www.guengel.ch/myapps/yapet/) (GPL v3)
    is a text based password manager written in C++, using the
    Blowfish encryption algorithm; it comes with a companion utility
    called csv2yapet that enables users to convert CSV files to YAPET
    _Last version 1.0 2014_.

# GPG based password managers

-   [Console Password Manager (CPM)
    ](https://github.com/comotion/cpm)
    (GPL) is a ncurses CDK based console tool that stores the
    passwords in a GnuPG encrypted file.  The programs data can be
    accessed via gpg as well. _The last commit is _2015_ and Debian
    package source is from 2014_.
    -   an older version of CPM is hostded at sourceforge under
        the name of  [Password Management System
        ](http://sourceforge.net/projects/passwordms/).
-   [Keyringer](https://keyringer.pw/) (GPL)
    lets you manage and share secrets using GnuPG and Git in a distributed fashion. It
    has custom commands to encrypt, decrypt and recrypt secrets as well as create key
    pairs and supports encryption to multiple recipients and groups of different
    recipients. Keyringer is in Debian.
    -   [keyringer source](https://git.fluxo.info/keyringer/)
-   [Pass](http://zx2c4.com/projects/password-store/)
    or _password_store_ (GPL) is a shell script which gpg-encrypt each
    password in a file named with the name of the resource.  And store
    the gpg encrypted files in git. Pass is in
    Debian.
    -   [GitHub: zx2c4 / password-store
        ](https://github.com/zx2c4/password-store).
-   [Pwman](http://pwman.sourceforge.net/)
    is a ncurses password manager based on the ui design of
    {{< iref "calendar#abook" "abook addressbook" >}}.
    It uses GPG to encrypt files. An unofficial Debian Package is
    available in the
    [pwman sourceforge repository
    ](https://sourceforge.net/projects/pwman/files/pwman/).
-   [SPD - the Simple Password Displayer](http://spd.sourceforge.net/)
    (GPL) SPD is a CLI-based passwordmanager, written in Perl
    _(old version)_ or python _(next release, may be!)_
    and using GnuPG to encrypt its data.
    [browse the SPD svn repository](http://spd.svn.sourceforge.net/viewvc/spd/trunk/).
-   [How to create a command-line password vault
    ](http://www.linux.com/archive/feature/114238) by
    Duane Odom, explains how to use gpg to compose a password manager
    script.
-   [GPG-Based Password Wallet
    ](http://www.linuxjournal.com/article/9861)
    an article by Carl Welch in linux-journal showing the use of gpg
    thru a bash script to keep passwords in an  encrypted file.
-   A script to
    [turn Vim into a Password Safe and edit openssl encrypted files
    ](http://www.vim.org/scripts/script.php?script_id=2012)
-   In the same way emacs user can use [EasyPg](http://www.easypg.org/)
    which has also a [page](http://www.emacswiki.org/emacs/EasyPG) on
    [Emacs Wiki](http://www.emacswiki.org/ "emacswiki.org").<br />
    If you want to do it in `org` mode you can follow the article
    [Keeping your secrets secret
    ](http://emacs.wordpress.com/2008/07/18/keeping-your-secrets-secret/).

# Web based password manager

-   [w3pw](http://sourceforge.net/projects/w3pw/)
    is a web based password manager written in PHP + MySQL using
    MCrypt for encryption.

# Browser plugins
-   [lastpass](https://lastpass.com/)
    is a Firefox plugin which uses one master password to encrypt your
    data on your PC. _But the encrypted data is stored on lastpass
    site, and you are fully dependent of them to retrieve your
    passwords. You need also to fully trust this proprietary plugin_
    It allows to import/export from/to Firefox, and export to popular
    password managers.<br /> LastPass Pocket allows offline access
    from a USB Key.
    -   [lastpass-cli](https://github.com/lastpass/lastpass-cli) is a
        CLI access to lastpass. It is written in C and runs on
        GNU/Linux, Cygwin and Mac OS X. It is in Debian.
        There is  an online [lpass(1) manpage
        ](https://lastpass.github.io/lastpass-cli/lpass.1.html).
    -   lastpass import in CVS with the format:

            url,type,username,password,hostname,extra,name,grouping
            http://sn,server,server1username,server1password,server1hostname,,Server 1,Server Group A
            http://sn,,,,,Adt349fme,Guest wireless key,Sys Admins
            http://community.spiceworks.com/login,,sysadmins@acme.com,spiceworkspassword,,confidential,Spiceworks Admin Login,Sys Admins

    -    lastpass and lpass export contains only the fields:

            url,username,password,extra,name,grouping,fav

        the fields are not quoted by default, but the _extra_ that
        contains notes with multiple lines should be quoted.
    -   [Lastpass help](https://helpdesk.lastpass.com/) :
        [Importing Passwords
        ](https://helpdesk.lastpass.com/importing-from-other-password-managers/),
        [export my sites or secure notes
        ](https://lastpass.com/support.php?cmd=showfaq&id=143),
        [export my LastPass data
        ](https://lastpass.com/support.php?cmd=showfaq&id=1206)


-   [MozillaZine FireFox Password Manager
    ](http://kb.mozillazine.org/Password_Manager) explains backing,
    restoring, printing passwords.
    -   [Mozilla Support: Using a Master Password
        ](https://support.mozilla.org/en-US/kb/use-master-password-protect-stored-logins)
-   [CryptFire](https://addons.mozilla.org/en-US/firefox/addon/12343)
    allows to encrypt/decrypt with AES inside Firefox.
    [cryptfire.com](http://cryptfire.com/) offers a Javascript standalone
    AES crypt/decript script.
-   See also {{< iref "#keefox" "Keefox" >}} above.


# Password Hashing
Password hashing is a strategy that uses a single master password that is hashed with a
salt made from the domain of the accessed site to generate a unique password that won't
be cracked if you don't know the master password.

Before using them you may read
[The case against password hashers](https://anarc.at/blog/2017-03-02-password-hashers/)
and
[A short history of password hashers](https://anarc.at/blog/2017-03-02-hashers-history/)
by _Anarcat_. It points out the cryptography havoc of old hashing mechanism _wich is
similar for every hashing use_, the necessity to copy  the username and password from
the hasher to the site, the necessity to reenter all your passwords when you change of
hasher, or from hashing function.

It is also to note that while these passsword hashers are used to avoid you use the same
password for many sites, when it is discovered either on a badly managed site that don't
hash or hash not properly your password and has its data stolen; or if it is stolen when
you type it because you javascript library has been replaced by a malicious one, or
because you type it in an unsecure environment where a key logger steal it; you are
actually giving access not only to one site but to all your private data.

An other problem with password hashers pointed out by _Anarcat_ is that one of their
benefit is to be stateless, serverless. But the sites have different requirements for
the passwords, so the options must be stored and available in every place you use
them. The recent password hashers offer a way to store them in the cloud or other
internet accessible place, even if this information is not sensitive, your hasher is no
longer stateless and don't work offline.

This defect is also object of the paper by Tony Arcieri:
[4 fatal flaws in deterministic password managers
](https://tonyarcieri.com/4-fatal-flaws-in-deterministic-password-managers).


But personally, I still find them usefull in some cases, in the past I was using the
same password for all harmless site, I mean all the shopping sites that you use once or
twice and where you are supposed not entering many critical data. I am a gardener who
buy seeds at many shops, what matter if my credentials are stolen, people will only
learn what I have sown the last years!

But this strategy is still dangerous, may be you use this password also on a site that
can use your credit card or have some sensitive data, if this password is captured on
one site, may be a fake site used for phishing, it is compromised everywhere.

But for these _low value_ sites the password hashers are still an help, you can put the
hash in your password manager and use it as usual, but in an environment where the
password manager is unavailable, and you fill it si not secure to log into its web site,
because you use an unknown computer you can still use the password hasher with the web
interface.


-   [Stanford PwdHash](https://pwdhash.github.io/webs)
    is the oldest password hasher with wide use.
    will come with browser extensions for Firefox, Chrome, Opera and a
    [local javascript stand alone page
    ](https://crypto.stanford.edu/PwdHash/RemotePwdHash/). It still use md5 which is no
    longer considered as secure.
-   There are many other extensions for hashing passwords in Firefox or Chrome that you
    get by looking for _password hasher_ in the extensions search. But many of them are
    limited to one browser, if you use many browsers, many systems or desktop and mobile
    like everyone today, it is of no use. Moreover the extensions are versions
    sensitive, and when you update say Firefox, you will soon or later see that the
    extension is no longer compatible, may be a new version of the extension will pop
    out some time later, but you can you login to your sites in the meantime.

    Some of these extension propose also a standalone javascript solution like
    [passhash-ng](https://github.com/phreaknerd/passhash-ng).
-   [SuperGenpass](https://chriszarate.github.io/supergenpass/) uses as basic method
    javascript bookmarklets that you can use in any javascript enabled browser.
    As it is a trivial script it has also be ported to many
    [alternative implementations
    ](https://github.com/chriszarate/supergenpass/wiki/Implementations)
    including browsers extensions and standalone programs, that will be very usefull to
    open sites in a non javascript enabled browser like elinks, w3m, ewww, ....
    Be aware that SuperGenPass defaults to MD5 with not enough rounds, you should select
    the SHA512 hashing function.
-   [LesPass](https://github.com/lesspass/lesspass) (GPL)
    by  Guillaume Vincent uses [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
    key derivation with 100,000 iterations and a hash function sha-256. out of the web
    interface it provides a [cli](https://github.com/lesspass/lesspass/tree/master/cli)
    a firefox and chrome extension and an Androip app.

    A _connected_ version  works by saving your password’s profile, in in database
    hosted by the site or your own server. Of course you have the problem mentioned
    above of being no longer stateless!

    There are also an alternative
    [python cli](https://github.com/mevdschee/lesspass.py),
    a [go implementation](https://github.com/mevdschee/lesspass.go) with a cli and gui,
    and a [php implementation](https://github.com/mevdschee/lesspass.php).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
