---
title: File Transfer
---

See also {{< iref "../system/backup#synchronization" "Synchronization" >}},
{{< iref "../system/backup" "Backup" >}},
{{< iref "p2p#p2p_file_sharing" "P2P file sharing software" >}},
{{< iref "clouds#temporary_storage" "Temporary storage" >}}.

{{< iref "webdav" "Webdav" >}} is in a separate page.

# Common references

-   Wikipedia: {{< wp "File sharing" >}}, {{< wp "List of file transfer protocols" >}},
    [List of FTP applications - ArchWiki
    ](https://wiki.archlinux.org/index.php/List_of_applications#FTP),
    [List of download managers - ArchWiki
    ](https://wiki.archlinux.org/index.php/List_of_applications#Download_managers).

# FTP {#ftp}
-   Wikipedia: {{< wp "List of file transfer protocols" >}},
    {{< wp "File Transfer Protocol" >}}, {{< wp "FTPS" >}}, {{< wp "Trivial File Transfer Protocol" >}},
    {{< wp "List of FTP server software" >}}, {{< wp "Comparison of FTP server software" >}},
    {{< wp "Comparison of FTP client software" >}},
    {{< wp "Trivial File Transfer Protocol" >}}.
-   [Wikibook: Communication Networks/File Transfer Protocol
    ](http://en.wikibooks.org/wiki/Communication_Networks/File_Transfer_Protocol)

## FTP servers
-   [atftp](https://sourceforge.net/projects/atftp/) (GPL-2.0)
    is the standard  {{< wp "Trivial File Transfer Protocol" >}} server used for
    {{< iref "IP#network_boot" "Network Boot" >}}. It is packaged in Debian.

    The software from Jean-Pierre Lefebvre, was unmaintained since 2011, since version
    7.1 2012 it has been updated by the new maintainer Martin Dummer .
-   _FTP-Proxy_ is a transparent, application-level proxy server for FTP connections,
    designed to protect FTP servers against attacks based on the FTP protocol.
    It performs chroot(), setuid(), setgid() to avoid possible vulnerabilities, and is
    believed to be immune against current known attacks.
    There is a Debian _FTP-Proxy_ package.
-   [glFTPd](http://en.wikipedia.org/wiki/Glftpd) (closed source, free binaries)
    FTP server with many security features.
-   [proftpd](http://www.proftpd.org/), modular FTP/SFTP/FTPS server. It is packaged in
    many Debian packages.
    - [Proftpd doc index](http://www.proftpd.org/docs/)
    - [ProFTPD mini-HOWTO Index](http://www.proftpd.org/docs/howto/)
    - [ProFTPD FTPS support](http://www.proftpd.org/docs/howto/TLS.html)
-   {{< wp "Pure-FTPd" >}} (BSD License) the BSD ftpd server. Multiple opackages in
    Debian.
    -   [Pure-FTPd Home Page](https://www.pureftpd.org/project/pure-ftpd/)
-   [tftp-hpa](https://git.kernel.org/pub/scm/network/tftp/tftp-hpa.git)
    is the {{< wp "Trivial File Transfer Protocol" >}} BSD TFTP server
    with  number of bugfixes and enhancements over the original.
    Packaged in Debian.
-   [vsftpd](https://security.appspot.com/vsftpd.html) (GPL)
    FTP server, seems no longer maintained since 2015;
    The developper [Chris Evans](https://scarybeastsecurity.blogspot.com/)
    last post is
    [Security: vsftpd-3.0.3 released... and the horrors of FTP over SSL
    ](https://scarybeastsecurity.blogspot.com/2015/07/vsftpd-303-released-and-horrors-of-ftp.html).
    _vsftpd_ is still [packaged in Debian](https://tracker.debian.org/pkg/vsftpd)
    _in 2021_.
    -   [vstpd conf manual
        ](https://security.appspot.com/vsftpd/vsftpd_conf.html)


## FTP clients {#ftp_clients}
-   [axel](https://github.com/axel-download-accelerator/axel) (GPL-2.0)
    Lightweight CLI download accelerator,  Axel can speed up a download up to 60%.
    Axel supports HTTP, HTTPS, FTP and FTPS protocols. _In Debian._
-   [FileZilla](https://filezilla-project.org/) (GPL)
    supports FTP, FTP over TLS (FTPS) and SFTP, HTTP/1.1, SOCKS5 and FTP Proxy
    support. It has a wxWidgets GUI.
    -   [Documentation - FileZilla Wiki
        ](https://wiki.filezilla-project.org/Documentation).
-   {{< wp "FireFTP" >}} (Mozilla Public License) was a ftp client plugin _add-on_ for
    mozilla. It supports FTP, FTPS, and SFTP. Firefox has now
    officially removed FireFTP and FireSSH support from the browser. It is still
    available for [Waterfox](https://www.waterfox.net/).
-   [gFTP](https://github.com/masneyb/gftp) (GPL)
    multithreaded file transfer gtk-2 client, it supports the FTP,
    FTPS (control connection only), FXP transfer,  HTTP proxy.
    gFTP can also be compiled as a console client.

    Debian provide a _gftp-GTK_ and _gftp-text_ package.
-   <a name="lftp"></a>[lftp](http://lftp.yar.ru/) (GPL)
    file transfer program supporting ftp, http, sftp, fish, and torrent.
    -   [LFTP - the manual page](http://lftp.yar.ru/lftp-man.html)
    -   [LFTP - torrent usage examples](https://lftp.tech/torrent.html)
    -   [lftp tips and tricks](https://linux.overshoot.tv/wiki/lftp)
-   [Net2ftp](http://www.net2ftp.com) (GPL)
    web based FTP client, written in PHP. You can use the
    [Net2ftp online client](http://www.net2ftp.com) _unsecure_ or intall it on your lan.


# HTTP download {#http_download}
See also among the  {{< iref "#ftp_clients" "FTP clients" >}} _axel_, _lftp_, _wget_.

-   <a name="curl"></a>[cURL and libcurl](http://curl.haxx.se/) (MIT license)
    _cURL_ is a command line tool for transferring data, supporting DICT, FILE, FTP,
    FTPS, Gopher, HTTP, HTTPS (including {{< iref "webdav" >}}, IMAP, IMAPS, LDAP,
    LDAPS, POP3, POP3S, RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, Telnet and TFTP.  curl
    supports SSL certificates, HTTP POST, HTTP PUT, FTP uploading, HTTP form based
    upload, proxies, cookies, user+password authentication (Basic, Digest, NTLM,
    Negotiate, kerberos...), {{< wp "Metalink" >}}, file transfer resume, proxy
    tunneling, socks, IPV6.
    -   Wikipedia {{< wp "cURL" >}}
    -   [cURL Documentation](http://curl.haxx.se/docs/):
        [cURL Manual](http://curl.haxx.se/docs/manual.html),
        [cURL FAQ](http://curl.haxx.se/docs/faq.html)
    -   See the
        {{< iref "webdav#dav_with_curl" "use for WebDav in the WebDav page" >}}.
    -   [Using cURL to interact with Google Data services
        ](https://developers.google.com/gdata/articles/using_cURL)
        article in the [Google Data APIs pages (gdata)
        ](https://developers.google.com/gdata/).
-   [HTTrack](http://www.httrack.com)
    download a website from the Internet to a local directory.
    It is in debian packages _httrack_ and _webhttrack_, and _proxytrack_.
    -   [HTTrack Documentation](http://www.httrack.com/html/index.html).
    -   [GitHub - HTTrack](https://github.com/xroche/httrack/tree/master).
-   {{< iref "#lftp" "lftp" >}} is above with ftp clients.
-   [pavuk](http://www.pavuk.org/) (GPL) is a web grabber to do
    recursive HTTP, HTTPS, FTP, SFTP and Gopher document retrieving, the software is no
    longer maintained since 2007 and has been removed from Debian in 2017.
-   <a name="wget"></a>[Wget2](https://gitlab.com/gnuwget/wget2) (GPL-3.0)
     is the successor of GNU Wget, a file and recursive website downloader.
     Wget2 is multi threaded, Wget is single threaded.
     Wget2 downloads much faster than Wget1.x due to HTTP2, HTTP compression, parallel
     connections and use of If-Modified-Since HTTP header.
    -   [Wget2 User Manual](https://gitlab.com/gnuwget/wget2/-/blob/master/docs/wget2.md)
    -   [Wget -gnu.org](http://www.gnu.org/software/wget/) (GPL),
    -   Wikipedia: {{< wp "Wget" >}},
    -   [GNU Wget Manual
        ](http://www.gnu.org/software/wget/manual/html_node/index.html),
    -   [The Wget Wgiki
        ](http://wget.addictivecode.org/),
    -   [Wget Frequently Asked Questions
        ](http://wget.addictivecode.org/FrequentlyAskedQuestions).
-   [How To mirror your web site with rsync
    ](http://www.howtoforge.com/mirroring_with_rsync)


# Multiprotocol download utilities

Many applications are listed in [List of download managers - ArchWiki
](https://wiki.archlinux.org/index.php/List_of_applications#Download_managers).

-   {{< wp "cURL" >}} (MIT License)
    Client-side URL transfer library and command-line client,
    supporting FTP, FTPS, Gopher, HTTP, HTTPS, SCP, SFTP, TFTP,
    Telnet, DICT, the file URI scheme, LDAP, LDAPS, IMAP,
    POP3, SMTP and RTSP. See the
    {{< iref "#curl" "Curl main entry" >}}
-   <a name=aria2></a>[aria2](https://aria2.github.io/)
    is a utility for downloading files. The supported protocols are
    HTTP(S), FTP, SFTP, BitTorrent, and {{< wp "Metalink" >}}.
    -   [Aria2 Manual](https://aria2.github.io/manual/en/html/index.html).
    -   [ArchWiki: aria2](https://wiki.archlinux.org/index.php/Aria2).
    -   see also [Metalink client feature comparison
        ](https://en.wikipedia.org/wiki/Metalink#Metalink_client_feature_comparison)
-   {{< iref "#wget" "wget" >}}
    supports HTTP, HTTPS, and FTP protocols.

# Asynchronous File Transfer
In contrast with the older technologies {{< wp "UUCP" >}} and {{< wp "BITNET" >}}
the file transfer protocols (s)FTP, SFTP, SCP, HTTP(s), Gopher are synchronous. Both
ends of the file transfer must be active simultenously to set up a connection.

To mitigate this problem we use a relay server, which is supposed to stay online.

The previous {{< iref "#temporary_storage" "Temporary Storage provider" >}}
allow to copy the whole file to the server, then the recipient get it back using
HTTP(S), FTP(S) or webdav(s). It needs to have been given an encryption key, and/or a
password.

To avoid the problems inherent to the transmission via an FTP server, or by mail
a new protocol [Asynchronous File Transfert Protocol - SAFT
](http://fex.belwue.de/saft/) , and a [sendfile
](http://fex.belwue.de/saft/sendfile.html) software to implement this protocol  have
been devised by Ulli Horlacher at university of Stuttgart.

_Sendfile_ is still available and packaged in Debian.

But the author himself point some drawbacks of this approach.

- the recipient needs a sendfiled installation on his host which is available only on
  unix, or an interactive account on the saft-server
- the recipient's saft-server must be permamently online
- the tcp port 487 must not be blocked by any firewall or ip-filter all the whole way
  from the sender to the recipient

So they created an other software, a file server named
{{< iref "clouds#fex" "F*EX - Fram's Fast File EXchange" >}}.
With _F*EX_ The sender uploads the file to the _F*EX_ server using a WWW upload form and the
recipient automatically gets a notification e-mail with a download-URL.


<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
