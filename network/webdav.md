---
title: WebDAV
---

See also {{< iref "file_transfer" "File Transfer" >}}.


# References
-   [WebDAV *(Wikipedia)*](http://en.wikipedia.org/wiki/WebDAV)
    or Web-based Distributed Authoring and Versioning is a set of
    extensions to the Hypertext Transfer Protocol (HTTP) that allows
    users to collaboratively edit and manage files on remote Web
    servers.
-   [webdav.org](http://webdav.org) is a central
    resource for WebDAV documentation, specifications, and
    [software](http://webdav.org/projects/)
-   The main IETF RFC for WebDAV are
    [RFC 4918](http://tools.ietf.org/html/rfc4918)
    *HTTP Extensions for Web Distributed Authoring and Versioning (WebDAV)*,
    [RFC 3648](http://tools.ietf.org/html/rfc3648),
    *Web Distributed Authoring and Versioning (WebDAV) Ordered Collections Protocol*,
    [RFC 3744](http://tools.ietf.org/html/rfc3744)
    *eb Distributed Authoring and Versioning (WebDAV) Access Control Protocol*,
    [RFC 4331](http://tools.ietf.org/html/rfc4331)
    *Quota and Size Properties for Distributed Authoring and Versioning (DAV) Collections*,
    [RFC 4437](http://tools.ietf.org/html/rfc4437)
    *Web Distributed Authoring and Versioning (WebDAV) Redirect Reference Resources*,
    [RFC 5397](http://tools.ietf.org/html/rfc5397)
    *WebDAV Current Principal Extension*.<br />
    You find them also __nicely formattted__ on
    [webdav.org: WebDAV Specifications](http://webdav.org/specs/)

<a name="dav_protocol"></a>
The protocol consists of a set of new methods and headers for use in
HTTP. The  methods include HTTP methods HEAD, GET, PUT, DELETE:

-   PROPFIND — used to retrieve properties, stored as XML, from a web
    resource. It is also overloaded to allow one to retrieve the
    collection structure (a.k.a. directory hierarchy) of a remote
    system.
-   PROPPATCH — used to change and delete multiple properties on a
    resource in a single atomic act
-   MKCOL — used to create collections (a.k.a. a directory)
-   COPY — used to copy a resource from one URI to another
-   MOVE — used to move a resource from one URI to another
-   LOCK — used to put a lock on a resource. WebDAV supports both
    shared and exclusive locks.
-   UNLOCK — used to remove a lock from a resource


# Webdav clients

Most Unix _dav_ clients (_cadaver_, _fusedav_,davfs2) and pieces of
software that provide a direct _dav_ access, are based on the
[neon library](http://www.webdav.org/neon/doc/html/) (GPL), including
the
{{< iref "filesystems#gvfs" "gvfs" >}} _webdav access_ is based on
{{< iref "filesystems#fuse" "fuse" >}}, since _fusedav_ uses neon.

{{< iref "filesystems#gvfs" "gvfs" >}} is used by all the _gnome_ stuff
such as _nautilus_, and the [Emacs tramp package
](http://www.gnu.org/software/tramp/#GVFS-based-methods)

The kde stuff as _konqueror_  use the _libkio_ library.

# Virtual file systems
-   [davfs2](http://savannah.nongnu.org/projects/davfs2) (GPL)
    is a Linux file system driver that allows you to mount a WebDAV
    resource into your file system. Applications can use the file
    system without knowing about WebDAV.
    [davfs2 README
    ](http://cvs.savannah.gnu.org/viewvc/davfs2/README).
-   [davfs2 - ArchWiki](https://wiki.archlinux.org/title/Davfs2).
-   [fusedav](http://0pointer.de/lennart/projects/fusedav/) is an user
    space file system using _fuse_ that access _webdav_ shares thru the
    [neon library](http://www.webdav.org/neon/doc/html/)

# command line or graphics clients

-   [cadaver](http://www.webdav.org/cadaver/)
    is a command-line client to _webdav_. It supports file upload,
    download, on-screen display, in-place editing, namespace
    operations (move/copy), collection creation and deletion, property
    manipulation, and resource locking.<br /> The cadaver interface is
    vey similar to _ftp_, _sftp_. and it supports https connections.
-   <a name="dav_with_curl"></a>{{< iref "file_transfer#curl" "cURL" >}}
    support webdav as a subset of its HTTP support. You can download a file with basic
    curl command, and do other operations by using `-X`, `--request <command>` with any
    command of the  {{< iref "#dav_protocol" "WebDav protocol" >}}.

    To upload a file use `-T`, `--upload-file <file>`.

    Authentication basic or digest is also available,

    See the [curl Manpage](https://curl.haxx.se/docs/manpage.html) for options details,
    some exemples are also in the tutorial
    [Using Curl commands with Webdav
    ](https://www.qed42.com/blog/using-curl-commands-webdav).

-   [nd](http://gohome.org/nd/) (MPL/GPL/LGPL) a tiny  command line
    WebDAV interface.  It is smaller than the alternative tool _cadaver_. However, nd
    has neither an interactive mode, nor has it support for SSL or TLS encrypted
    transmissions.<br /> It was also used by the _emacs_ library
    [eldav](http://www.gohome.org/eldav/) that provides transparent _dav_ access from
    _emacs_.<br /> _nd_ is still in Debian buster but _nd and eldav have not changed
    since 2003_ and can be considered as obsolete.
-   There are some WebDAV clients and servers for Android
    but not yet an open source one.
-   [easywebdav](https://github.com/amnong/easywebdav) (ISC licence =
    BSD or MIT) is a webdav client in python. It is
    [in pipy](http://pypi.python.org/pypi/easywebdav/).

# Emacs dav access
-   Emacs uses a
    [Tramp GVFS based external method
    ](http://www.gnu.org/software/tramp/#GVFS-based-methods)to access
    dav over http or https (davs).
-   A native client provided with emacs >=22, is
    [url-dav.el _in emacs.git_
    ](http://repo.or.cz/w/emacs.git/blob/HEAD:/lisp/url/url-dav.el)
-   [eldav](http://www.gohome.org/eldav/)
    was an older client which has no ssl support. It is no longer in emacs.


# server libraries
-   [pywebdav](http://code.google.com/p/pywebdav/) (GPL) features a
    python library that provide WebDAV server capabilities,
    It is [in pypi](https://pypi.python.org/pypi/PyWebDAV); It does
    not seem to be developped since 2012 but the package is in Debian
    as _python-webdav_.
-   [wsgiDav](https://github.com/mar10/wsgidav) (MIT License)
    WebDAV wsgi server written in Python, it is in pypi.
-   [SabreDAV](http://sabre.io/dav/) (BSD License)
    is a WebDAV server PHP library. It is in the Debian package
    _php-sabre-dav_.
-   [WebDAV CGI](https://danrohde.github.io/webdavcgi/) (GPL)
    is a Perl CGI script that enables the WebDAV protocol (class
    1,2,3). It is an old project but which seems well maintained
    in 2017.
-   [chezdav](https://wiki.gnome.org/phodav) (GPL)
    is a gnome tool build upon the gnome dav server library
    [Phodav](https://wiki.gnome.org/phodav), and it allows to serve a
    folder with Webdav. Debian as packages for _chezdav_ and
    _libphodav_.
-   [litmus](http://webdav.org/neon/litmus/) is a WebDAV server protocol
    compliance test suite. _litmus_ is built using the _neon_ library.
-   {{< iref "apache" "Apache" >}} has a
    [webdav module](http://httpd.apache.org/docs/2.0/mod/mod_dav.html)
-   {{< iref "lighttpd" "Lighttpd" >}} has a
    [mod_webdav module](http://redmine.lighttpd.net/wiki/1/Docs:ModWebDAV)
-   {{< iref "nginx" "Nginx" >}} has a [ngx_http_dav_module
    ](http://nginx.org/en/docs/http/ngx_http_dav_module.html)
    that is complemented with [nginx-dav-ext-module
    ](https://github.com/arut/nginx-dav-ext-module) to have the
    PROPFIND and OPTIONS operations.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
