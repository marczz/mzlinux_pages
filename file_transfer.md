<!--
.. description:
.. date: 2017-02-25
.. slug: file_transfer
.. tags:
.. link:
.. book mzlinux
.. title: File Transfer
-->

[TOC]

See also [Synchronization
](/node/backup#synchronization "internal reference"),
[Backup](/node/backup "internal reference"),
[P2P file sharing software
](/node/p2p#p2p_file_sharing "internal reference"),
[Temporary storage
](/node/clouds#temporary_storage "internal reference").

[Webdav](/node/webdav "internal reference") is in a separate page.

# Common references

-   Wikipedia: [w:File sharing], [w:List of file transfer protocols],


# FTP {#ftp}
-   Wikipedia: [w:List of file transfer protocols],
    [w:File Transfer Protocol], [w:FTPS], [w:Trivial File Transfer Protocol],
    [w:List of FTP server software], [w:Comparison of FTP server software],
    [w:Comparison of FTP client software],
-   [Wikibook: Communication Networks/File Transfer Protocol
    ](http://en.wikibooks.org/wiki/Communication_Networks/File_Transfer_Protocol)

## clients
-   [w:FireFTP] (Mozilla Public License) is a ftp client plugin for
    mozilla. It supports FTP, FTPS, and SFTP.
-   [gFTP](http://gftp.seul.org/) (GPL)
    multithreaded file transfer client, it supports the FTP,
    FTPS (control connection only), HTTP, HTTPS, SSH and FSP protocols
-   [lftp Home Page](http://lftp.yar.ru/)([lftp(1)](http://man.cx/lftp(1)))
-   [Net2ftp](http://www.net2ftp.com) (GPL)
    web based FTP client, written in PHP.
-   [Yafc FTP Client](http://www.yafc-ftp.com/) (GPL)
    [Yafc Manual](http://www.yafc-ftp.com/manual/).

## servers
-   [glFTPd](http://en.wikipedia.org/wiki/Glftpd) (closed source, free binaries)
    FTP server with many security features.
-   [proftpd](http://www.proftpd.org/),
    - [Proftpd doc index](http://www.proftpd.org/docs/)
    - [ProFTPD mini-HOWTO Index](http://www.proftpd.org/docs/howto/)
    - [ProFTPD FTPS support](http://www.proftpd.org/docs/howto/TLS.html)
-   [w:Pure-FTPd] (BSD License)
-   [vsftpd](https://security.appspot.com/vsftpd.html) (GPL)
    FTP server
    -   [vstpd conf manual
        ](https://security.appspot.com/vsftpd/vsftpd_conf.html)

# HTTP download {#http_download}
See also the [main HTTP section
](/node/IP#http "internal reference")

-   <a name="wget"></a>[wget](http://www.gnu.org/software/wget/) (GPL),
    Wikipedia: [w:Wget],
    [GNU Wget Manual
    ](http://www.gnu.org/software/wget/manual/html_node/index.html),
    [The Wget Wgiki
    ](http://wget.addictivecode.org/),
    [Wget Frequently Asked Questions
    ](http://wget.addictivecode.org/FrequentlyAskedQuestions).
-   [WGET software for FTP and Web Auto-mirroring
    ](http://www.ccp14.ac.uk/mirror/wget.htm)
-   [pavuk](http://www.pavuk.org/) (GPL) is a web grabber to do
    recursive HTTP, HTTPS, FTP, SFTP and Gopher document retrieving.
-   <a name="curl"></a>[cURL and libcurl](http://curl.haxx.se/) (MIT license)
    _cURL_ is a command line tool for transferring data, supporting
    DICT, FILE, FTP, FTPS, Gopher, HTTP, HTTPS, IMAP, IMAPS, LDAP,
    LDAPS, POP3, POP3S, RTMP, RTSP, SCP, SFTP, SMTP, SMTPS, Telnet and
    TFTP.  curl supports SSL certificates, HTTP POST, HTTP PUT, FTP
    uploading, HTTP form based upload, proxies, cookies, user+password
    authentication (Basic, Digest, NTLM, Negotiate, kerberos...),
    [w:Metalink], file transfer resume, proxy tunneling, socks, IPV6.
    -   Wikipedia [w:cURL]
    -   [cURL Documentation](http://curl.haxx.se/docs/):
        [cURL Manual](http://curl.haxx.se/docs/manual.html),
        [cURL FAQ](http://curl.haxx.se/docs/faq.html)
    -   [Using cURL to interact with Google Data services
        ](https://developers.google.com/gdata/articles/using_cURL)
        article in the [Google Data APIs pages (gdata)
        ](https://developers.google.com/gdata/)


# Multiprotocol download utilities

-   [w:cURL] (MIT License)
    Client-side URL transfer library and command-line client,
    supporting FTP, FTPS, Gopher, HTTP, HTTPS, SCP, SFTP, TFTP,
    Telnet, DICT, the file URI scheme, LDAP, LDAPS, IMAP,
    POP3, SMTP and RTSP. See the
    [Curl main entry
    ](#curl "internal reference")
-   <a name=aria2></a>[aria2](https://aria2.github.io/)
    is a utility for downloading files. The supported protocols are
    HTTP(S), FTP, SFTP, BitTorrent, and [w:Metalink].
    -   [ArchWiki: aria2
        ](https://wiki.archlinux.org/index.php/Aria2).
    -   see also [Metalink client feature comparison
        ](https://en.wikipedia.org/wiki/Metalink#Metalink_client_feature_comparison)
-   [wget](#wget "internal reference")
    upports HTTP, HTTPS, and FTP protocols.

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
