---
title: File Transfer
---

{{% toc /%}}

See also {{< iref "backup#synchronization" "Synchronization" >}},
{{< iref "backup" "Backup" >}},
{{< iref "p2p#p2p_file_sharing" "P2P file sharing software" >}},
{{< iref "clouds#temporary_storage" "Temporary storage" >}}.

{{< iref "webdav" "Webdav" >}} is in a separate page.

# Common references

-   Wikipedia: {{< wp "File sharing" >}}, {{< wp "List of file transfer protocols" >}},


# FTP {#ftp}
-   Wikipedia: {{< wp "List of file transfer protocols" >}},
    {{< wp "File Transfer Protocol" >}}, {{< wp "FTPS" >}}, {{< wp "Trivial File Transfer Protocol" >}},
    {{< wp "List of FTP server software" >}}, {{< wp "Comparison of FTP server software" >}},
    {{< wp "Comparison of FTP client software" >}},
-   [Wikibook: Communication Networks/File Transfer Protocol
    ](http://en.wikibooks.org/wiki/Communication_Networks/File_Transfer_Protocol)

## clients
-   {{< wp "FireFTP" >}} (Mozilla Public License) is a ftp client plugin for
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
-   {{< wp "Pure-FTPd" >}} (BSD License)
-   [vsftpd](https://security.appspot.com/vsftpd.html) (GPL)
    FTP server
    -   [vstpd conf manual
        ](https://security.appspot.com/vsftpd/vsftpd_conf.html)

# HTTP download {#http_download}
See also the {{< iref "IP#http" "main HTTP section" >}}

-   <a name="wget"></a>[wget](http://www.gnu.org/software/wget/) (GPL),
    Wikipedia: {{< wp "Wget" >}},
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
    {{< wp "Metalink" >}}, file transfer resume, proxy tunneling, socks, IPV6.
    -   Wikipedia {{< wp "cURL" >}}
    -   [cURL Documentation](http://curl.haxx.se/docs/):
        [cURL Manual](http://curl.haxx.se/docs/manual.html),
        [cURL FAQ](http://curl.haxx.se/docs/faq.html)
    -   [Using cURL to interact with Google Data services
        ](https://developers.google.com/gdata/articles/using_cURL)
        article in the [Google Data APIs pages (gdata)
        ](https://developers.google.com/gdata/)


# Multiprotocol download utilities

-   {{< wp "cURL" >}} (MIT License)
    Client-side URL transfer library and command-line client,
    supporting FTP, FTPS, Gopher, HTTP, HTTPS, SCP, SFTP, TFTP,
    Telnet, DICT, the file URI scheme, LDAP, LDAPS, IMAP,
    POP3, SMTP and RTSP. See the
    {{< iref "#curl" "Curl main entry" >}}
-   <a name=aria2></a>[aria2](https://aria2.github.io/)
    is a utility for downloading files. The supported protocols are
    HTTP(S), FTP, SFTP, BitTorrent, and {{< wp "Metalink" >}}.
    -   [ArchWiki: aria2
        ](https://wiki.archlinux.org/index.php/Aria2).
    -   see also [Metalink client feature comparison
        ](https://en.wikipedia.org/wiki/Metalink#Metalink_client_feature_comparison)
-   {{< iref "#wget" "wget" >}}
    supports HTTP, HTTPS, and FTP protocols.

# File sharing with android and ios

{{< iref "p2p#p2p_file_sharing" "P2P file sharing software" >}} can be supported in the
browser or with dedicated application,
{{< iref "clouds#temporary_storage" "Temporary storage" >}} have usually a web interface
and sometime an ftp access.

If we want to share files with linux, we can use {{< iref "#ftp" >}}, or sftp with an
ftp/sftp client on the mobile device.

There are also clients for smb, and webdav.

-   [shareviahttp](https://github.com/marcosdiez/shareviahttp) (BSD Licence)
    is an application th share files from Android via http.
    it is available on F-Droid




<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
