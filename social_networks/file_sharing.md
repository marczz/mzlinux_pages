---
Title: File Sharing
---

# Temporary File hosting {#temporary_storage}
See also {{< iref "p2p#p2p_file_sharing" "P2P File sharing" >}},
{{< iref "task_management" "Task Management" >}},
{{< iref "task_management#note_taking" "Notes Taking" >}}.

_I list only services with a password protection and/or encryption._


<a name="android_web_upload"></a>
For the web interface android browsers you cannot use drag & drop, but
the file loader allow _docs_ as intent that allow to choose either the
android native file manager, or an other like ES file manager, or
drive, or numerous other options. UC browser has a different interface
but that works also.

-   Wikipedia: {{< wp "File hosting service" >}}
-   [Send large files: 10 free tools
    ](http://www.creativebloq.com/design-tools/send-large-files-clients-free-tools-3132117)
    _february 2016_
-   [15 Super Quick Ways to Share Files Without Cloud Storage
    ](http://www.makeuseof.com/tag/15-super-quick-ways-share-files-without-cloud-storage/)
-   [Alternatives to Send Anywhere](http://alternativeto.net/software/send-anywhere/)
-   [Alternative to Senduit](http://alternativeto.net/software/senduit/)

-   [filebin.ca](http://filebin.ca/) up to 50 megabytes, without time
    limit, but deleted after 6 months of inactivity. No registration
    necessary but file password protection, expiration dates and
    download limits are available to registered users.
-   [filesharing24.com](https://filesharing24.com/) up to 5GB kept
    24h, password protection available. Transfers are encrypted.
    Worked to send from android with uc browser, (no file manager for
    chrome or dolphin)
-   [mozilla/send](https://github.com/mozilla/send) (Mozilla Public Licence)
    share file from firefox with encryption and a link that expires.
    The main instance [Firefox Send](https://send.firefox.com/) allowed a maximum of 1GB
    without registration and 2.5GB with registration. The repository is now archived,
    and the extension no longer available.
-   Free file sending service [dl.free.fr] (http://dl.free.fr).
    An javascript free web interface
    [is also available](http://dl.free.fr/index_nojs.pl)

    We can also send files by ftp on `dl.free.fr` the login is the email address where
    we receive the name for the download.

    The files are not deleted until there is at least one download per period
    of at least 30 days (depending on the space available on the servers). The maximum
    size per file uploaded by FTP is 10GB. and 1GO on the web.  Files are password
    protected.
-   [Hightail](https://www.hightail.com/) up to 50MB encrypted. Needs
    to register. free 100MB/upload, max 2G; other plans are expensive.
-   {{< iref "#lufi" "Lufi free hosted instances" >}} see
    {{< iref "#lufi" "below" >}}
-   {{< iref "#lutim" "Lutim free hosted instance" >}} for image sharing.
-   [mediafire](http://www.mediafire.com/) 3€/month 1TB permanent
    storage, 20GB per file; free plan add supported up to 10GB.
-   [Send Anywhere](https://send-anywhere.com/) described
    {{< iref "p2p#sendanywhere" "in the P2P file sharing section" >}} is
    mainly a P2P service, but it includes cloud storage to free the
    user from the contraint that both browser need to be open during
    all the transfer time.
-   [Ufile.io](https://ufile.io/) up to 5G kept 30 days
    for the free service.No registration, encrypted. The download is
    by url, with a speed limit of 1MB/s so 1G has a minimal time of
    1000s ie 17mn. Paid plans are expensive.
-   [wetransfer](https://www.wetransfer.com/) up to 2G, 7 days for
    free account, No encryption or password protection. It is one of
    the more used site for file exchange, but to get 20G and password
    without even encryption, you have to pay 120$ annual!
-   [wikisend](http://wikisend.com/) up to 100MB, free, no registration
    necessary, password protection, default save time 7 days, when
    registered it can be set up to 90 days.

## Pastebin {#pastebin}

There are many similar services that we name with the common name {{< wp "Pastebin" >}}
from the first {{< wp "pastebin.com" >}} they allow a free web clip by pasting some
text, and they give you an url to retrieve the text.

You can use to create you post a web page and most sites have a REST HTTP Api that allow
to create posts with a script. _I list only the sites offering an API, and not too much
adds, and the FOSS software_.

They can offer optional features like expiration dates, private posts, syntax
highlighting,

-   Wikipedia {{< wp "Pastebin" >}}.
-   [Pastebin Services - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications#Pastebin_services)
-   See also {{< iref "desktop#clipboard_share" "Clipboard Sharing" >}}.


-   [pastebin.com](https://pastebin.com/) has syntax highlighting, expiration dates,
    private posts, ads, see wikipedia {{< wp "Pastebin.com" >}} for more informations.
    [API](https://pastebin.com/api), many official
    [command line clients](https://pastebin.com/tools#pastebincl)
    written in many programming languages. The [original code
    ](https://github.com/lordelph/pastebin) is available in GitHub.
    -   There are extension for Chrome, Firefox, Opera.
    -   The ios client is [PasteMe
        ](https://apps.apple.com/us/app/pasteme-pastebin-client-for/id1191488320).
    -   For android: [Pastebin for Android
        ](https://play.google.com/store/apps/details?id=com.jmz.pastedroidapp).
    -   For linux and old client written in Python2
        [pastbin-cl](https://github.com/tupton/pastebin-cl)

    There was many controversies about pastebin.com, quoting  [Pastebin Services - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications#Pastebin_services)

    > An acceptable pastebin service does not require enabling JavaScript for viewing,
    > does not display adverts, manipulate the pasted content or require a
    > login. pastebin.com is blocked for some people because of malware found on the
    > site and has a history of annoying issues (requires JavaScript, displays adverts,
    > inserts CRLF line-endings and displaying CAPTCHAs at random). Do not use it.

    Following the monitoring of content by Pastebin _Anonymous_ launched
    {{< iref "#anonpaste" "Anonpaste" >}}.

-   [Hastebin](https://hastebin.com/about) (MIT License)
    is a FOSS alternative to pastebin.com.
    -   [Haste server](https://github.com/seejohnrun/haste-server)
        is written in node.js, you can use as backend the filesystem, reddis, Postgres,
        MongoDB, Memcached, RethinkDB, Google Datastore, Amazon S3.
        A Docker build is also available.
    -   [haste-client](https://github.com/seejohnrun/haste-client)  is a ruby CLI for
        Haste.
    -   You can also use a simple bash function:
        ``` sh
        haste() { a=$(cat); curl -X POST -s -d "$a" https://hastebin.com/documents |\
           awk -F '"' '{print "https://hastebin.com/"$4}
        ```
    -   Or the bash script [hastebin.sh
        ](https://github.com/diethnis/standalones/blob/master/hastebin.sh)
    -   Python scripts
        [kevr / hastebin](https://github.com/kevr/hastebin/blob/master/hastebin)
        [RobertKolner / hastebin-client
        ](https://github.com/RobertKolner/hastebin-client) (MIT License) and
        [jirutka / haste-client ](https://github.com/jirutka/haste-client).
    -   in Go [zneix / haste-client](https://github.com/zneix/haste-client) (AGPL-3.0)
        and [lus / hastebin-cli ](https://github.com/lus/hastebin-cli) (MIT License)
    -   In Rust [upaste](https://github.com/jaemk/upaste) (MIT License)
        works also with paste.rs, and the  personal server
        [upaste-server](https://github.com/jaemk/upaste-server).
        It has a companion vim-plugin [vim-upaste](https://github.com/jaemk/vim-upaste)
    -   [Emacs Haste client](https://github.com/rlister/emacs-haste-client) (GPL-2.0)
    -   [davidjcralph/hastebin-bot](https://github.com/davidjcralph/hastebin-bot) (MIT
        License) is a node.js {{< iref "sip#discord" "Discord" >}} bot that posts data
        to Hastebin.
    -   [drforse/hastebin_bot](https://github.com/drforse/hastebin_bot)
        is a telegram bot written in Python for uploading code to hastebin.com.

    There are some lighter clones of _Haste_:
    -   [mkr bin](https://bin.mkr.pw/)
        is a lightweight hastebin alternative with no frontend JS dependency.
        -   [mkr bin server](https://github.com/MKRhere/bin) ( MIT License )
            in node.js, use  mogoDB backend.
-   [Paste.ee](https://paste.ee) is a free pastebin with no ads, SSL,
    IPv6, [API](https://pastee.github.io/docs/),
    [CLI programs](https://paste.ee/wiki/Programs).
    -   For Linux there is [past-ee-cli](https://git.meow.tf/paste-ee/cli) written in
        go. The releases includes binaries and rpm and deb packages.
-   <a name="paste_debian"></a>[paste.debian.net](http://paste.debian.net/)
    is a pastebin, targeted to source code with enlightening. It has an
    [xml RPC interface](http://paste.debian.net/rpc-interface.html)  and
    [xml RPC clients](http://paste.debian.net/paste.pl?show_template=clients)
    including {{< iref "#pastebinit" "pastebinit" >}},
    [paste.py](https://github.com/gebi/debianpaste-clients),
    [paste-dn.pl](http://ankh-morp.org/~vetinari/tools/paste-dn.pl) and an
    emacs client [debpaste](https://github.com/alezost/debpaste.el) in elpa.
    -   [paste.pl - Github](https://github.com/formorer/paste.pl) (AGPL-3.0)
        is the perl software powering _paste.debian.net_
    -   [EmacsWiki: Debpaste](https://www.emacswiki.org/emacs/Debpaste).
-   [fpaste or paste.fedoraproject.org
    ](https://paste.fedoraproject.org/) is the fedora pastebin service
    you use it with the program [fpaste](https://pagure.io/fpaste).
-   {{< iref "#teknik"  "Teknik" >}} has a   [Pastebin](https://paste.teknik.io)
    with a [paste shell script
    ](https://git.teknik.io/Teknikode/Tools/src/branch/master/Paste/paste.sh)
    you can also use {{< iref "#uugush" "uugush" >}}.

## Codepad
-   <a name="codepad">[codepad.org](http://codepad.org/)
    is an online compiler/interpreter, and a simple collaboration tool. It's
    a pastebin that executes code for you. It can interpret code in C, C++, D, haskell,
    lua, ocaml, php, perl, python, ruby, scheme, Tcl.
-   [LaKing/codepad](https://github.com/LaKing/codepad) (MIT License) is a
    collaborative online code editor and project written in node.js manager running
    online in the browser. It relies on a MongoDB database.

## pastebin cli
here are many text clip, screenshot clip, file sharing programs that
can interface with many pastebin. Many of them have unclear license, and no source
available, so it is difficult to know if your data and metadata is monitored, for
sensible data use a {{< iref "#crypted_bin" "Crypted Bin" >}}

### pastebin with access from curl/nc
-   <a name="ix.io"></a>[ix.io](http://ix.io/) (said open source, but unpublished source!)
    is a command line pastebin.

    You use it with curl like this:
    ```
    ~$ echo Hello world. | curl -F 'f:1=<-' ix.io
    http://ix.io/fpW
    ```

    or
    ```
    curl -F 'f:1=<-' ix.io < file
    ```

    More detailled usage on the [ix.io Page](http://ix.io/).

    You can also use the [bash client](http://ix.io/client), or from emacs
    [ix.el](https://github.com/theanalyst/ix.el) _in MELPA_.
-   [clbin.com](https://clbin.com/) _no source available?_
    is a command line pastebin similar to _ix.io_.

    There is a [gist with a bash script for clbin
    ](https://gist.github.com/GermainZ/9177423) and an [emacs interface
    ](https://gist.github.com/welliam/9788acbc2d46530a8a9974ab7fc2afa8).
-   [localpaste](https://github.com/petermaloney/localpaste) (GPL-2.0)
    is a python clone of clbin.
-   <a name="sprunge"></a>[sprunge](http://sprunge.us/) is a python command line
    pastebin that you use with:

        <command> | curl -F 'sprunge=<-' http://sprunge.us

    -   [sprunge source at GitHub](https://github.com/rupa/sprunge).
-   [termbin](http://termbin.com/) is a command line pastebin that
    requires only _netcat_, you use it like this:

        <command> | nc termbin.com 9999

    [fiche the termbin source on GitHub](https://github.com/solusipse/fiche)
    is a 484 sloc C program. _fiche_ support ipv6. It is packaged ind Debian.

    There is also an Android termbin application.

### cli for multiple pastebin
-   [anypaste](https://anypaste.xyz/)
    Anypaste is a file sharing bash script which uses the mime type of a file to
    automatically detect compatible hosting sites.

    The actual upload site is found in a
    [list of plugins](https://anypaste.xyz/#plugins), you can configure enabled plugins,
    and us a specific one with an option. It can be used for pastebins or file sharing
    including images and videos.

    The provided plugins for text are {{< iref "#ix.io" "ix.io">}},
    [Pastie](https://pastie.org/), [P.defau.lt](https://p.defau.lt/),
    [Paste2](https://paste2.org/), {{< iref "#hastebin" "Hastebin" >}},
    ([Docdroid](https://docdroid.net/) for pdf, docx, ODS, ...).

-   <a name="pastebinit"></a>[pastebinit](https://help.ubuntu.com/community/Pastebinit)
    can use
    [pastebin.ca](http://pastebin.ca),
    [pastebin.mozilla.org](http://pastebin.mozilla.org),
    {{< iref "#paste_debian" "paste.debian.net" >}},
    paste.drizzle.org,
    [paste.kde.org](https://paste.kde.org/),
    paste.openstack.org, paste.pocoo.org,
    paste.pound-python.org, paste.ubuntu.org.cn,
    [paste.ubuntu.com](http://paste.ubuntu.com),
    [pastie.org](http://pastie.org/),
    [Paste2](https://paste2.org/),
    pb.daviey.com,
    slexy.org, {{< iref "#sprunge" " sprunge.us" >}},
    [yourpaste.net](http://yourpaste.net),


    To see all services do `pastebinit -l` or look at  [all conf files
    ](http://bazaar.launchpad.net/~pastebinit-developers/pastebinit/trunk/files/head:/pastebin.d/).

    There is a pastbinit Debian package.
-   [sleeksnap](https://pastee.github.io/docs/) written in java dedicated to screenshots.

-   <a name="uguush"></a>[uguush](https://gitlab.com/jschx/uguush/-/tree/master) (MIT
    License) is a shell command-line uploader for [uguu](https://uguu.se/),
    {{< iref "#teknik" "Teknik" >}}, [0x0](https://0x0.st/), ptpb _obsolete_, mixtape
    _obsolete_, [lewd](https://lewd.se/), fiery _obsolete_ or doko _obsolete_.
-   [ix.io syntax highlighter](https://github.com/xero/ix.io-syntax) highlight code
    pastes on sprunge or clbin.


## Crypted pastbin {#crypted_bin}
<!-- [[file:/share/sync_folders/misc/mznotes/content-org/weblinks/network.org::*Privatebin][My list of Privatebin services]]
-->
Some pastebin offer encryption

-   <a name="anonpaste"></a>[AnonPaste](https://anonpaste.org/).
    _The Ultimate Secure Pastebin_ launched by _Anonymous_after Pastebin.cm
    move to censor content and pass on the IP addresses of people posting on its site
    to law enforcement authorities.
    It is said to use real 256bit AES encryption, which takes place directly in your
    browser. At launch in 2012 it was said powered by ZeroBin, but now all information
    pages on the site is only the same _Lorem ipsum dolor_ blob.

-   <a name="privatebin"></a>[PrivateBin](https://privatebin.info/) (Zlib/libpng license)
    is a minimalist, opensource online pastebin/discussion
    board where the server has zero knowledge of hosted data. Data is
    encrypted/decrypted in the browser using 256 bits AES.

    It is the continuation of
    [Zero Bin](http://sebsauvage.net/wiki/doku.php?id=php:zerobin)
    by Sebastien Sauvage, an instance of Zerobin is online on
    [Seb sauvage site](http://sebsauvage.net/paste/),

    -   [PrivateBin - GitHub](https://github.com/PrivateBin/PrivateBin/).
    -   [PrivateBin Instance Directory](https://privatebin.info/directory/)

## Web file sharing servers
_They are self-hosted solutions._

-   [Open source alternatives to ZendTo
    ](http://alternativeto.net/software/zendto/?license=opensource)


-   [Bozon](https://github.com/broncowdd/BoZoN) (AGPL)
    is a self-hosted php drag & drop file sharing app.It allows to
    stream mp3, to manage users, to display a photo gallery.  BoZoN
    doesn't use any database back end. Files are shared by url, with
    an optional password protection. You can Access BoZoN on a
    smartphone with your browser, and use a qrcode to share your link
    with smartphone users. You can share a whole folder and Download
    its contents into a zip.
-   [Coquelicot](https://coquelicot.potager.org/) (AGPL)
    _one-click_ file sharing with a focus on privacy. While being uploaded, files are
    written to the disk using symmetric encryption. The encryption key is either part
    of the download URL, or specified by the uploader. More details in the
    [Readme](https://coquelicot.potager.org/README). Coquelicot is written in ruby.
    The last release is from 2016, it was packaged in Debian until stretch.
-   <a name="fex"></a>[F*EX](http://fex.rus.uni-stuttgart.de/) (Artistic Licence)
    _Frams' Fast File EXchange_ is a PERL service to send big files
    between two users. The sender uploads the file to the F*EX server
    using a WWW upload form and the recipient automatically gets a
    notification e-mail with a download-URL. _Fex_ is in a Debian
    package, the client utilities are in a separate package _fex-utils_.
-   [FileTea](https://github.com/elima/FileTea) (AGPL)
    functions as a web server. Users can drag files into their web
    browser and a URL will be generated for each one. Those URLs can
    be sent to other people, who will be able to start downloading the
    files immediately.

    An HTML5 capable browser is required in order to share the files, but
    any HTTP client can download them, including command-line tools such
    as curl or wget.

    Files are sent through the server, but no data is stored there:
    FileTea is only used to route the traffic. This also means that
    there's no limit to the size of shared files.

    The service is anonymous and does not require user registration.

    _Filetea is not updated since january 2014. It is still in Debian_

-   [FileZ](https://github.com/FileZ/FileZ) (GPL)
    is a php Web service to upload and manage files and
    share them through unique URLs. _not active since 2014_.
-   [File2Link](https://framagit.org/kepon/file2link)
    ([Beerware License](https://en.wikipedia.org/wiki/Beerware))
    is a PHP File sharing service. A database is not necessary.
    -   [File 2 Link instance - dl.zici.fr](https://dl.zici.fr/)
-   [Jirafeau](https://gitlab.com/mojo42/Jirafeau) (AGPL)
    is a self-hosted php web service for file sharing, it uses no
    database, files can be protected by password and encrypted, and
    have expiration time for downloads.
-   <a name="lufi"></a>[Lufi](https://framagit.org/luc/lufi/) (AGPL)
    is a Perl server application of file sharing. The files are encrypted in the browser
    and stored on the server. All the encryption/decryption processes take place in your
    browser. The encryption key is never sent over the network. You can host Lufi on
    your server or use a free instance.
    -   [Lufi Wiki](https://framagit.org/luc/lufi/wikis/home).
    -   [Lufi Cli](https://framagit.org/luc/lufi-cli)
        is a javascript client for Lufi.
    -   Many on line service offer a free Lufi, instance, the available services change
        quite quickly, so I don't give a list but you can see some european instances at
        the page [framasoft: lufi](https://alt.framasoft.org/en/framadrop).
-   <a name="lutim"></a>[Lutim](https://framagit.org/luc/lutim) (AGPL) is a Perl server
    application for image sharing. The file are optionally encrypted
    on the server, _not the browser like in Lufy,_ which allow to use
    it even with a browser without javascript.
    -   [Lutim Wiki](https://framagit.org/luc/lutim/wikis/).
-   [Plik](https://github.com/root-gg/plik/tree/master) (MIT License)
     is a scalable & friendly temporary file upload system in golang.  It uses as data
     backend Files, OpenStack Swift, or S3 this last allow server side encryption; and
     as metadata backend Sqlite3 or postgresql. There is a go client with packages for
     all platforms, and a bash client in the repository.

     -   [Plik vulpecula.fr](https://plik.vulpecula.fr/#/) is a free hosted instance of
     Plik.
-   <a name="sharik"></a>[Sharik](https://github.com/marchellodev/sharik) ( MIT License)
    is a golang cross-platform solution for sharing files via Wi-Fi or Mobile Hotspot.
    it is available for Android, Windows, Linux, iOS. Sharik provides an HTTP server
    allowing to download the file you want to share, so the client can download without
    installing a specific client.
    -  There is also a go cli-only version
       [sharic](https://github.com/marchellodev/sharic).

    _Sharik_ serve the files on HTTP on the localhost, neither the protocol, nor the
    files are encrypted. So it is only acceptable if the local network is on a firewall
    protected lan. When connected to an hotspot, we should not send private files. For
    mobile to mobile transmission we can also use a wifi connection sharing protected by
    password, giving some protection against _naive_ intruder, the main benefit here is
    that don't require a wifi internet connection and it does not count against your
    data plan.

    So Sharik is good for _quick and dirty_ file exchange, all the protected file
    storages servers of this section offer a more secure solution, at the price of
    needing a relay, and an internet connection.
-   [weborf](https://github.com/ltworf/weborf) (GPL-3.0)
    is a python instant server to share files using the HTTP protocol. It provides CLI
    and It comes with a Python/QT5 GUI called _qweborf_, allows using webdav, can
    compress directories on the fly.  The server has CGI and (x)inetd support, and
    systemd integration. It can do NAT traversal to share files outside of the local
    network.

    Weborf can
    [cache the server generated contents](https://ltworf.github.io/weborf/cache.html)
    With the expense of a small amount of disk space, this can greatly increase the
    speed.

    [_weborf_, _weborf-daemon_ and  _qweborf_ are in Debian
    ](https://tracker.debian.org/pkg/weborf)..
-   [Zendto](https://zend.to/) (Open source _Unknown licence_)
    is a PHP service to share files.  It will also integrate with any Active Directory,
    LDAP or IMAP system.  MyZendTo has a restricted access to your users there is no
    public acces. Zend needs PHP and a database SQLite or MySQL.
    -   [ZendTo documentation](https://zend.to/documentation)

# Collaborative services
-   <a name="technik"></a>[Teknik](https://www.teknik.io/)
    provide many services
    -   Free: [Encrypted File Uploads](https://upload.teknik.io/) _24h, filesize 1GB_,
        [Pastebin](https://paste.teknik.io)
        Technical Podcasts, Url Shortener, Mumble Server.
    -   Free registered users: Non-Expiring Uploads, Unlimited pubic or private Git
        Repos with a {{< iref "git#gitea" "Gitea instance" >}}, Personal Blog,
        Service Data.
    -   5$ lifetime account: Email Account {{< iref "mail#rainloop" "RainLoop" >}},
        Upload Size 2GB/file, total 50GB, No Embed Limits
    -   [API Help](https://help.teknik.io/API)
    -   [Tool Help](https://help.teknik.io/Tools) you find there  a [paste shell script
        ](https://git.teknik.io/Teknikode/Tools/src/branch/master/Paste/paste.sh),
        a command line script to upload files [tekup
        ](https://git.teknik.io/danthebeastman/tekup), a [weechat script
        ](https://git.teknik.io/Teknikode/Tools/src/branch/master/Weechat/teknik.py)
        to interact with the Teknik Services, including file uploads, pastes, and url
        shortening, [Hexchat script
        ](https://git.teknik.io/Teknikode/Tools/src/branch/master/Hexchat/teknik.py),
        and a firefox and chrome extension to access teknik services.

# Collaborative editors
-  [Etherpad](http://etherpad.org/) (Apache License)
   is a customizable online editor written in nodejs providing real-time collaborative
   editing. There are many online instance of etherpad that you can find in
   [this list
   ](https://github.com/ether/etherpad-lite/wiki/Sites-that-run-Etherpad-Lite),
   like the french [framapad](https://framapad.org/).
-  See also {{< iref "#codepad" "codepad" >}} in the
   {{< iref "#pastbin" "pastbin list" >}}).
-  [CryptPad](https://github.com/xwiki-labs/cryptpad)(AGPL and private licence)
   is the zero knowledge realtime online _node.js_ collaborative editor, it can use
   _MongoDB_ or [leveldb](https://en.wikipedia.org/wiki/LevelDB). A docker configuration,
   and an Ansible recipe is also provided.
   [cryptpad](https://cryptpad.fr/)
   is an online service instance that offer encrypted pad to registered user, and
   temporary encrypted pads to anonymous users.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
