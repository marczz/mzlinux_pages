---
Title: File Sharing
---

# Temporary File storage services{#temporary_storage}
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

### image files servers
-   <a name="lutim"></a>[Lutim](https://framagit.org/luc/lutim) (AGPL) is a Perl server
    application for image sharing. The file are optionally encrypted
    on the server, _not the browser like in Lufy,_ which allow to use
    it even with a browser without javascript.
    -   [Lutim Wiki](https://framagit.org/luc/lutim/wikis/).
-  [TeDomum / TedImg](https://forge.tedomum.net/tedomum/tedimg) (Beer-ware License)
   a flask image server, written in python, Node.js

## Codepad {#codepad}
-   <a name="codepad.org">[codepad.org](http://codepad.org/)
    ([closed source](http://codepad.org/about))
    is an online compiler/interpreter, and a simple collaboration tool. It's
    a pastebin that executes code for you. It can interpret code in C, C++, D, haskell,
    lua, ocaml, php, perl, python, ruby, scheme, Tcl.
-   [LaKing/codepad](https://github.com/LaKing/codepad) (MIT License) is a
    collaborative online code editor and project written in node.js manager running
    online in the browser. It relies on a MongoDB database.
-   [Ideone.com](https://ideone.com/) (proprietary software)
    is an online codepad compiler/interpreter and IDE for many languages.

# Pastebin {#pastebin}

There are many similar services that we name with the common name {{< wp "Pastebin" >}}
from the first {{< wp "pastebin.com" >}} they allow a free web clip by pasting some
text, and they give you an url to retrieve the text.

Some pastebin have unclear license, and no source
available, so it is difficult to know if your data and metadata is monitored. If you
have to store sensible data you should use a {{< iref "#crypted_bin" "Crypted Bin" >}}.


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
    -   For linux an old client written in Python2
        [pastbin-cl](https://github.com/tupton/pastebin-cl)
    -   [elpastebin](https://github.com/nicferrier/elpastebin) or _pastebin.el_
        is an interface to _pastebin.com_ see also
        [EmacsWiki: pastebin](https://www.emacswiki.org/emacs/pastebin) for other
        versions of  _pastebin.el_.  _pastebin.el_ is in MELPA.
    -    {{< iref "#webpaste.el"  "webpaste.el" >}} supports _pastebin.com_.

    _pastebin.com_ was [written by Paul Dixon
    ](https://github.com/lordelph/pastebin) and released under AGPL-3.0 Licence, but he
    sold the domain in 2010, and it is now a commercial site.

    There was many controversies about pastebin.com, quoting
    [Pastebin Services - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications#Pastebin_services)

    > An acceptable pastebin service does not require enabling JavaScript for viewing,
    > does not display adverts, manipulate the pasted content or require a
    > login. pastebin.com is blocked for some people because of malware found on the
    > site and has a history of annoying issues (requires JavaScript, displays adverts,
    > inserts CRLF line-endings and displaying CAPTCHAs at random). Do not use it.

    Following the monitoring of content by Pastebin _Anonymous_ launched
    {{< iref "#anonpaste" "Anonpaste" >}}.
-   <a name="bpaste"></a>[bpaste](https://bpa.st/) (MIT Licence)
    is the free instance of [pinnwand](https://github.com/supakeen/pinnwand)
    a Python pastebin software with _pygments_ syntax highlighting,
    using _tornado_, _sqlalchemy_, and a database driver.

    You can use curl to paste on bpaste:
    ``` sh
    € echo "foo" | curl -X POST http://localhost:8000/curl -F 'raw=<-'
    Paste URL:   http://localhost:8000/OE
    Raw URL:     http://localhost:8000/raw/GU
    Removal URL: http://localhost:8000/remove/GQBHGJYKRWIS34D6FNU6CJ3B5M
    ```
    -   [Steck](https://supakeen.com/project/steck) is a CLI for _bpaste_/_pinnwand_.
    -   [pinnwand documentation](https://pinnwand.readthedocs.io/en/latest/)
    -   {{< iref "#wgetpaste" "wgetpaste">}} can paste to _bpaste_.

-   <a name="dpaste.com"></a>[Dpaste.com](https://dpaste.com/) (closed source)
    is a pastebin on a python / Django application. It has code syntax highlighting with
    _pygments_.

    Dpaste.com has many [Scripts, Tools, Integrations](https://dpaste.com/help)
    including:
    -   [dpaste.sh](https://hg.sr.ht/~paulbissex/dpaste-tools/) (MIT Licence)
        command-line client for creating dpaste items from stdin.
    -   [dpaste.el](https://github.com/gregnewman/dpaste.el)
        is an emacs client to post a region or buffer to
        dpaste.com and put the paste URL into the kill-ring.
    -   {{< iref "#webpaste.el"  "webpaste.el" >}} supports _dpaste.com_.
    -   {{< iref "#wgetpaste"  "wgetpaste" >}} supports _dpaste.com_.
-   < a name="dpaste.org"></a>[Dpaste.org](https://dpaste.org/) ( MIT License )
        is a django application implementing a pastebin.

        _paste.org_ was previously named _paste.de_.

    -   [pastebin.mozilla.org the Mozilla Community Pastebin
        ](https://pastebin.mozilla.org/) is an other instance of _dpaste.org_.
    -   [dpaste.org API](https://dpaste.readthedocs.io/en/latest/api.html)
        You can paste your file content to the API via curl,
        directly from the command line:
        ``` sh
        $ alias dpaste="curl -F 'format=url' -F 'content=<-' https://dpaste.org/api/"
        $ cat foo.txt | dpaste
        https://dpaste.de/ke2pB
        ```
    -   [dpaste.org - GitHub](https://github.com/bartTC/dpaste)
    -   [dpaste.org documentation](https://dpaste.readthedocs.io/en/latest/)
    -   [dpaste_de.el](https://github.com/theju/dpaste_de.el) is an emacs package to
        paste to _paste.org_. _in ELPA_
    -   {{< iref "#webpaste.el"  "webpaste.el" >}} has support for dpaste.org.

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
    [CLI programs](https://paste.ee/wiki/Programs). It is the CentOs pastbin.

    It is an instance of [Stikked](https://paste.centos.org/about) an Open-Source PHP
    Pastebin, with features like Syntaxhighlighting for many languages, including live
    syntax highlighting with CodeMirror, Paste replies and diff view between the
    original paste and the reply, API, anti-spam, themes, multilanguage.

    A _Stikked_ instance needs a web server, a database: MySQL, Postgres or sqlite, PHP and
    PHP GD.
    -   [Stikked - GitHub](https://github.com/claudehohl/Stikked)
        ( [WTFPL](http://www.wtfpl.net/))
    -   For Linux there is [past-ee-cli](https://git.meow.tf/paste-ee/cli) written in
        go. The releases includes binaries and rpm and deb packages.
    -   [Run Your Own Pastebin with Stikked
        ](https://www.maketecheasier.com/run-your-own-pastebin-with-stikked/).
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
-   <a name="paste.fedora"></a>[paste.fedoraproject.org or fpaste
    ](https://paste.fedoraproject.org/) is the fedora pastebin service
    you use it with the program [fpaste](https://pagure.io/fpaste).
-   <a name="paste.gg"></a>[paste.gg](https://paste.gg/)
    is powered by [paste](https://github.com/ascclemens/paste) (MIT License)
    by Anna  Clemens. The _paste_ repository is also in
    [~jkcclemens/paste - SourceHut](https://git.sr.ht/~jkcclemens/paste)

    _paste_ is a rust software with heavy requirements rust, ruby, postgres, redis,
    nginx, sidekiq.

    {{< iref "#bins" "bins" >}} from the same author is a command line client with
    _paste_ support.
-   [pastemyst](https://paste.myst.rs/) (MPL-2.0 License)
    is a pastebin with syntax highlighting, and optional encryption.
    -   [pastemyst - GitHub](https://github.com/codemyst/pastemyst)
    -   [pastemyst API](https://paste.myst.rs/api-docs/index) is used by many libraries
        in a variety of languages. See the [pastemyst API page
        ](https://paste.myst.rs/api-docs/index) for a list.
    -   [pastry](https://github.com/CodeMyst/pastry) (MIT License)
        is the official client written in D language. Binaries are provided in the
        [releases page](https://github.com/CodeMyst/pastry/releases).
-   [paste.ofcode.org](https://paste.ofcode.org/) is an instance of
    [ofcode](https://github.com/bbangert/ofcode) it has _of course_ syntax highlighting,
    the paste is limited to 1 week. An emacs client in elpa is [paste-of-code.el
    ](https://github.com/spebern/paste-of-code.el) (GPL-3.0) It pastes the region or the
    whole buffer and place the url in the kill ring. _in MELPA_.
-   <a name="lodgeit"></a>[paste.opendev.org](https://paste.opendev.org/) _or
    paste.openstack.org via a redirection_
    is [an instance of _lodgeit_](https://paste.opendev.org/about/)
    which was a previous project from _Pocoo_ which was [retired due to spam
    ](https://www.reddit.com/r/Python/comments/swrj8/pastepocooorg_is_now_gone_because_of_spams_and/).
    -   [lodgeit-el](https://github.com/ionrock/lodgeit-el) (GPL-2.0) is an emacs client
        for _lodgeit_ based pastebins.
    -   [spacepaste](https://github.com/shirkey/spacepaste) is a fork on GitHub, after
        the project ws retired.
    -   _lodgeitlib_ is a client library and command line client for _lodgeit_ based
        pastebins,  the documenttion is still on _pythonhosted_
        [lodgeitlib documentation](https://pythonhosted.org/lodgeitlib/index.html),
        and [lodgeitlib code was forked on GitHub](https://github.com/TC01/pastelib).
-   [pastery.net](https://www.pastery.net/) _unknown source_
    is a pastebin with syntax highlighting. Its [API](https://www.pastery.net/api/)
    is illustrated by _curl_ examples, and is the base of many
    [plugins](https://www.pastery.net/plugins/).
    -   [pastery.el](https://github.com/diasbruno/pastery.el) (MIT License)
        is an emacs client. _in MELPA_.
    -   [pastery.vim](https://github.com/skorokithakis/pastery.vim) and
        [vim-pastery](https://github.com/fishbullet/vim-pastery).
    -   [bakeit](https://github.com/skorokithakis/bakeit) (MIT License) a python client.
    -   [rust-bakeit](https://gitlab.com/stavros/rust-bakeit) is a port of _bkeit_ to
        rust.
-   {{< iref "#teknik"  "Teknik" >}} has a   [Pastebin](https://paste.teknik.io)
    with a [paste shell script
    ](https://git.teknik.io/Teknikode/Tools/src/branch/master/Paste/paste.sh)
    you can also use {{< iref "#uugush" "uugush" >}}.

## pastebin without public instance
-  [paste.cf](https://sr.ht/~kota/paste.cf/) (3-Clause BSD License)
   a simple ftp based pastebin server and client.

   It is used by doing a ftp to the site and doint a `put myfile` in the `incoming`
   directory. The sha1sum of the file is the the key by which you find your file on the
   web server.

   The hosted `paste.cf` site is down and redirect to `pastebin.net` then to
   `pastebin.com`.

   The installation on your server is detailed in the repository.
   -   [paste.cf - sourcehut git](https://sr.ht/~kota/paste.cf/) (3-Clause BSD License)
   -   [pcf - sourcehut git](https://git.sr.ht/~kota/pcf) (GPL-3.0)
       is a golang CLI for paste.cf.


## Minimal pastebins with access from curl/nc
Some pastebin listed above have also, an access from curl, the following light pastebin
don't have syntx highlighting.

-   <a name="ix.io"></a>[ix.io](http://ix.io/) (said open source, but unpublished source!)
    is a command line pastebin.

    You use it with curl like this:
    ``` sh
    ~$ echo Hello world. | curl -F 'f:1=<-' ix.io
    http://ix.io/fpW
    ```
    or
    ```sh
    curl -F 'f:1=<-' ix.io < file
    ```

    More detailled usage on the [ix.io Page](http://ix.io/).

    You can also use the [bash client](http://ix.io/client), or from emacs
    [ix.el](https://github.com/theanalyst/ix.el) _in MELPA_ which snd the selection or
    entire buffer to ix.io, the url is notified in the minibuffer and saved in the kill
    ring.
-   [clbin.com](https://clbin.com/) _no source available?_
    is a command line pastebin similar to _ix.io_.

    You use it with curl in the same way than _ix.io_
    ``` sh
    $ cat hello-world.c | curl -F 'clbin=<-' https://clbin.com
    https://clbin.com/y94KD
    ```
    There is a [gist with a bash script for clbin
    ](https://gist.github.com/GermainZ/9177423) and an [emacs interface
    ](https://gist.github.com/welliam/9788acbc2d46530a8a9974ab7fc2afa8).
-   [localpaste](https://github.com/petermaloney/localpaste) (GPL-2.0)
    is a python clone of clbin.
-   [paste.c-net.org](https://paste.c-net.org/)
-   <a name="sprunge"></a>[sprunge](http://sprunge.us/) is a python command line
    pastebin that you use with:

        <command> | curl -F 'sprunge=<-' http://sprunge.us

    -   [sprunge source at GitHub](https://github.com/rupa/sprunge).
-   [el-sprunge](https://github.com/eschulte/el-sprunge) (GPL-3.0)
    An emacs powered command line paste server with Emacs highlighting in the style of
    sprunge.  Pastes may be submitted to the server from the command line using `curl'
    as follows.
    ``` sh
    $ <command> | curl -s -F 'sprunge=<-' %s
    ```
    The server will respond with the path at which the URL is available.  To enable
    syntax highlighting append "?foo" to the returned URL and the server will return the
    paste highlighted with "foo-mode".
-   [paste.c-net.org](https://paste.c-net.org/) (no source available)
    is a pastebin that allows pasting binary files.
    It is used with curl like this:
    ``` sh
    $ curl -s --data 'Hello World!' 'https://paste.c-net.org/'
    $ curl --upload-file '/tmp/file' 'https://paste.c-net.org/'
    $ curl --upload-file - 'https://paste.c-net.org/' <'/tmp/file'
    ```
    or with wget:
    ``` sh
    $ wget --quiet -O- --post-file='/tmp/file' 'https://paste.c-net.org/'
    ```
    or with nc:
    ``` sh
    $ nc paste.c-net.org 9999 <'/tmp/file'
    ```
    The [author](https://blog.dhampir.no/content/binary-pastebin) gives no information
    on the program source.
-   [termbin](http://termbin.com/) is a command line pastebin that
    requires only _netcat_, you use it like this:

        <command> | nc termbin.com 9999

    [fiche the termbin source on GitHub](https://github.com/solusipse/fiche)
    is a 484 sloc C program. _fiche_ support ipv6. It is packaged ind Debian.

    There is also an Android termbin application.

## cli for multiple pastebin
-   [anypaste](https://anypaste.xyz/) (GPL-3.0)
    Anypaste is a file sharing bash script which uses the mime type of a file to
    automatically detect compatible hosting sites.

    The actual upload site is found in a
    [list of plugins](https://anypaste.xyz/#plugins), you can configure enabled plugins,
    and us a specific one with an option. It can be used for pastebins or file sharing
    including images and videos.

    The provided plugins for text are {{< iref "#ix.io" "ix.io">}},
    [Pastie](http://pastie.org/) __syntax highlighting, closed source, no https_,
    [P.defau.lt](https://p.defau.lt/) _no syntax ghlighting, unknown software_,
    [Paste2](https://paste2.org/) _syntax highlighting support, unknown source_,
    {{< iref "#hastebin" "Hastebin" >}},
    ([Docdroid](https://docdroid.net/) for pdf, docx, ODS, ...).
    -   [anypaste - Github](https://github.com/markasoftware/anypaste).
    -   [anypaste documenttion](https://anypaste.xyz/) on the Home site.
-   <a name="bins"></a>[bins](https://github.com/ascclemens/bins) ( MPL-2.0 License)
    is a rust client for  [GitHub Gist](https://gist.github.com/),
    {{< iref "#pastebin.com" "pastebin.com" >}}, {{< iref "#hastebin" "hastebin" >}},
    {{< iref "#sprunge" "sprunge" >}}, Bitbucket snippets,
    {{< iref "#paste.fedora" "fedora pastebin" >}}, and
    {{< iref "#paste.gg" "paste.gg"  >}}.

    A compiled binary is provided in the Release.
-   <a name="pastebinit"></a>[pastebinit](https://help.ubuntu.com/community/Pastebinit)
    can use
    [pastebin.ca](http://pastebin.ca) _unavailable_,
    {{< iref "#dpaste.org" "pastebin.mozilla.org" >}}_,
    {{< iref "#paste_debian" "paste.debian.net" >}},
    paste.drizzle.org _unavailable_,
    [paste.kde.org](https://paste.kde.org/) _gitlab snippet_,
    paste.openstack.org _renamed_ [paste.opendev.org](https://paste.opendev.org/),
    paste.pocoo.org _retired service_,
    paste.ubuntu.org.cn,
    [paste.ubuntu.com](http://paste.ubuntu.com),
    [pastie.org](http://pastie.org/) _syntax highlighting, closed source, no https_,
    [Paste2](https://paste2.org/) _syntax highlighting, unknown software_,
    pb.daviey.com _unavailable_,
    slexy.org _ads powered_, {{< iref "#sprunge" " sprunge.us" >}},
    [yourpaste.net](http://yourpaste.net) _unavailable_,


    To see all services do `pastebinit -l` or look at  [all conf files
    ](http://bazaar.launchpad.net/~pastebinit-developers/pastebinit/trunk/files/head:/pastebin.d/).

    There is a pastbinit Debian package.
-   [sleeksnap](https://pastee.github.io/docs/) written in java dedicated to screenshots.
-   <a name="uguush"></a>[uguush](https://gitlab.com/jschx/uguush/-/tree/master) (MIT
    License) is a shell command-line uploader for [uguu](https://uguu.se/),
    {{< iref "#teknik" "Teknik" >}}, [0x0](https://0x0.st/), ptpb _obsolete_, mixtape
    _obsolete_, [lewd](https://lewd.se/), fiery _obsolete_ or doko _obsolete_.
-   <a name="wgetpaste">__wgetpaste__ (open source) is a script relying only on bash,
    sed, coreutils , and wget to paste to {{< iref "#codepad.org" "codepad.org" >}},
    {{< iref "#bpaste" "bpaste" >}}, {{< iref "#dpaste.com" "dpaste.com" >}}, gists,
    [gitlab snippets](https://gitlab.com/api/v4/snippets).
    -   [Wgetpaste gentoo manual](https://wiki.gentoo.org/wiki/Wgetpaste)
    -   [wgetpaste source](https://wgetpaste.zlin.dk/)

-   [ix.io syntax highlighter](https://github.com/xero/ix.io-syntax) highlight code
    pastes on sprunge or clbin.

### Emacs pastebin cli {emacs_pastebin_cli}
-   [dpaste.el](https://github.com/gregnewman/dpaste.el) (GPL-2.0)
    is an emacs client to post a region or buffer to
    {{< iref "#dpaste.com" "dpaste.com" >}} and put the paste URL into the
    kill-ring. _in ELPA_
-   [debpaste.el](https://github.com/alezost/debpaste.el) (GPL-3.0)
    the  emacs client for {{< iref "#debpaste" "debpaste" >}} is in ELPA.
-   [ix.el](https://github.com/theanalyst/ix.el) the  emacs client for
    {{< iref "#ix.io" "ix.io" >}} is _in ELPA_.
-   [scpaste.el](https://git.sr.ht/~technomancy/scpaste)  (GPL 3.0)
    is an emacs library which place an HTML copy of a buffer on the web on a server to
    which the user has SSH access.
    It uses scp as its transport and uses Emacs' font-lock as its syntax highlighter.
    _in MELPA_.
-   <a name="webpaste.el"></a>[webpaste.el](https://github.com/etu/webpaste.el)
    (GPL-3.0) is an emacs client to paste to many services
    {{< iref "#ix.io" "ix.io" >}}, [paste.rs](https://paste.rs),
    {{< iref "#dpaste.com" "dpaste.com" >}},
    {{< iref "#dpaste.org" "dpaste.org" >}},
    [paste.mozilla.org](https://paste.mozilla.org/), gist,
    [bpa.st](https://bpa.st/).

## Crypted pastbin {#crypted_bin}
<!-- [[file:/share/sync_folders/misc/mznotes/content-org/weblinks/network.org::*Privatebin][My list of Privatebin services]] -->

Some pastebin offer encryption

-   <a name="anonpaste"></a>[AnonPaste](https://anonpaste.org/).
    _The Ultimate Secure Pastebin_ launched by _Anonymous_after Pastebin.cm
    move to censor content and pass on the IP addresses of people posting on its site
    to law enforcement authorities.
    It is said to use real 256bit AES encryption, which takes place directly in your
    browser. At launch in 2012 it was said powered by ZeroBin, but now all information
    pages on the site is only the same _Lorem ipsum dolor_ blob.
-   <a name="privatebin"></a>[PrivateBin](https://privatebin.info/) (Zlib/libpng license)
    is a minimalist, opensource online pastebin/discussion board where the server has
    zero knowledge of hosted data. Data is encrypted/decrypted in the browser using 256
    bits AES.

    It is the continuation of
    [Zero Bin](http://sebsauvage.net/wiki/doku.php?id=php:zerobin)
    by Sebastien Sauvage, an instance of Zerobin is online on
    [Seb sauvage site](http://sebsauvage.net/paste/),

    -   [PrivateBin - GitHub](https://github.com/PrivateBin/PrivateBin/).
    -   [PrivateBin Instance Directory](https://privatebin.info/directory/)

# Collaborative services
See also voice and video calling {{< iref "sip#jitsi" "Jitsi" >}},
{{< iref "sip#bigbluebutton" "BigBlueButton" >}}

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

## Collaborative editors
-  See also {{< iref "#codepad" "codepad" >}} in the
   {{< iref "#pastbin" "pastbin list" >}}).

### Etherpad {#etherpad}
[Etherpad](http://etherpad.org/) (Apache License)
is a customizable online editor written in nodejs providing real-time collaborative
editing. There are many online instances of etherpad .
-   [list of instance running Etherpad Lite
    ](https://github.com/ether/etherpad-lite/wiki/Sites-that-run-Etherpad-Lite)

There are numerous (~200) [Etherpad plugins](https://static.etherpad.org/index.html)
adding new functionalities.

Many free services hosting uses
[Mypads](https://framagit.org/framasoft/Etherpad/ep_mypads) which add privates pads:
-   users and their authentication;
-   groups of pads per user, unlimited, sharable;
-   attached pads, with choice between invite known users to use them, making them private
    with password or letting them public.

<a name="libreto"></a>[Libreto](https://github.com/Ventricule/libreto) (GPL-3.0)
is a collaborative notebook based on etherpad, It can become a mini-website, a workshop
logbook or a collective book writing tool.

The demonstration site [libreto.net](https://libreto.net)
allows to create libretto book on many etherpads: framapad, wikimedia, allmende, factor,
etherpad, la quadrature du net.

### Cryptpad {#cryptpad}
[CryptPad](https://github.com/xwiki-labs/cryptpad)(AGPL and private licence)
is the zero knowledge realtime online _node.js_ collaborative editor, it can use
_MongoDB_ or [leveldb](https://en.wikipedia.org/wiki/LevelDB). A docker configuration,
and an Ansible recipe is also provided.

-   [cryptpad.fr](https://cryptpad.fr/)
    is an online  instance that offer temporary 90 days encrypted pads to anonymous
    users, lasting encrypted pad up to a total 1GB to free registered user, and from 5GB
    to 50GB for 60€/year to 180€/year.

-   [Bim CryptPad](https://doc.bim.land/)   temporary 90 days encrypted pads to anonymous
    users, lasting encrypted pad up to a total 100MB to free registered users.

## Spreadsheet
[Ethercalc](https://github.com/audreyt/ethercalc) (Common Public Attribution License (CPAL) and
Artistic License 2.0) is a node web spreatsheet


## Slides
-   [Strut](https://strut.io/)
    is an HTML5 Presentation Editor
    -   [strut.io instance](http://strut.io/dist/index.html)

## Diagrams
- [diagrams.net](https://app.diagrams.net/)  is an online diagramming web site
- [jgraph/drawio: Source to app.diagrams.net](https://github.com/jgraph/drawio)
  (Apache License)

## Poll System {#poll_system}
They are {{< wp "Doodle_(website)" "Doodle" >}} open source alternatives.

A list of alternatives is [given in jawanndenn Readme
](https://github.com/hartwork/jawanndenn#goals)


-   [Framadate](https://framadate.org/) has its source at
    [Framadate · Framagit](https://framagit.org/framasoft/framadate/framadate).

    It is powered by [OpenSondage](https://github.com/leblanc-simon/OpenSondage) which
    is a fork of _Studs_.

    In 2021 is in maintenance mode, will be replaced by
    [funky framadate - Framagit](https://framagit.org/framasoft/framadate/funky-framadate-front).

-   [Nuages](https://nuages.domainepublic.net/) A collaborative meeting poll system,
    similar to doodle or rdvz.  It is build in python, using the django framework and a
    little of javascript.

-   [jawanndenn](https://github.com/hartwork/jawanndenn) (AGPL-3.0)
    Simple alternative to Doodle polls and scheduling (Python 3, Django 3, JavaScript)
    -   [jawanndenn demo instance](https://jawanndenn.de/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
