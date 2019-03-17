<!--
.. description:
.. date: 2011-09-04
.. slug: web_servers
.. tags:
.. link:
.. book: mzlinux
.. title: Web Servers
-->

[TOC]

-    The main stream servers have their own page:
    [Apache](/node/apache "internal reference"),
    [Lighttpd](/node/lighttpd "internal reference"),
    [Nginx](/node/nginx "internal reference").
-   See also [PHP-FPM](/node/php/php-fpm "internal reference").

# Server Architectures

:   The different server architectures and a comparison are
    introduced in the
    [Server Architectures chapter from Benjamin Erb's Thesis
    ](http://berb.github.io/diploma-thesis/community/042_serverarch.html#42).

    There are two main streams of httpd servers those which are
    **thread-based** and those who are **event-driven**.

    The **thread-based architecture** is achieved through thread proper or though processes.
    In this model each incoming connection is associated with a
    separate thread or process by using synchronous blocking I/O.
    In this model, each thread or process handle a single sequential
    task, and the concurrency is achieved by duplicating these single
    task processes or thread. This is the older model, and the easier
    to understand, code and debug, because each process/thread can be
    isolated as a single task sequential process/thread.

    This is the original model adopted by CERN first server, most of
    the older servers. The oustanding server for this model is
    [Apache httpd server](node/252"internal reference"), which
    offer a choice of multi-processes and multi-threaded servers.

    See the [comparison of thread-based and process-based server architectures
    ](http://berb.github.io/diploma-thesis/community/042_serverarch.html#thread)
    by Benjamin Erb for details.

    In the **event-driven architecture** a single thread is mapped to
    multiple connections. The events are queued and processed by an
    *event-loop* that multiplexes multiple connections to a single
    flow of execution. This is the model used by [lighttpd
    ](/node/lighttpd "internal reference"), [nginx](#nginx "internal reference"),
    the python web server [Tornado
    ](/node/web_frameworks#tornado "internal reference"),
    [cyclone](/node/web_frameworks#cyclone "internal reference"),
    the emacs server [elnode](/node/emacs#elnode "internal reference") and many
    new servers.

    For more details look at the B. Erb chapters on
    [I/O multiplexing patters](
    http://berb.github.io/diploma-thesis/community/042_serverarch.html#io)
    and [hybrid server architecture
    ](http://berb.github.io/diploma-thesis/community/042_serverarch.html#combined).


__ACME__ tiny http servers

:   -   [thttpd](http://www.acme.com/software/thttpd/)  has CGI, external
        SSI as cgi program, and a throttling feature,
    -   [mini\_httpd](http://www.acme.com/software/mini_httpd/) 0.7Meg,
        includes CGI,
    -   [micro\_httpd](http://www.acme.com/software/micro_httpd/) a
        tiny server that can run from inetd/xinetd


[memcached](http://www.danga.com/memcached/)
:   memcached is a high-performance, distributed memory object
    caching system used for speeding up dynamic web applications;
    [libmemcache](http://people.freebsd.org/~seanc/libmemcache/) is a C
    API to memcached,
    [CML aka Cache Meta Language](http://trac.lighttpd.net/trac/wiki/CacheMetaLanguage)
    is an implementation of memcached for lighttpd.



# Authentication

-   [Stanford WebAuth](http://webauth.stanford.edu/) is an
    authentication system for web pages and web applications. The
    first time a user attempts to access a web page protected by
    WebAuth, they will be sent to a central login server
    (weblogin.stanford.edu at Stanford) and prompted to
    authenticate. Normally, they will be asked for a username and
    password, although other authentication methods are possible. Once
    the user has logged in, the weblogin server will send their
    encrypted identity back to the original web page they were trying
    to access. Their identity will also be stored in a cookie set by
    the weblogin server and they will not need to authenticate again
    until their credentials expire, even if they visit multiple
    protected web sites.
-   Webauth is available in Debian as _webauth-weblogin_,
    _webauth-utils_; The the Apache module for the central
    authentication server is _libapache2-mod-webkdc_.
-   [WebAuth with UNIX Guide
    ](https://itservices.stanford.edu/service/web/centralhosting/webauth/unix).
-   [w:Pubcookie] (Apache License)
    Pubcookie is a protocol and a software package
    for providing single sign-on within web applications
    and websites of an organization.
    -   [PubCookie Home](http://www.pubcookie.org/)

# web log analysis
-   [w:analog] web log analysis program
-   Available in Debian as package _analog_.
-   If installed on localhost you can access it at
    [analog server statistics](/analog/)
-   Alternative _webalizer_, _visitors_, _lire_.



# Polipo
-   [Polipo Home page](http://www.pps.jussieu.fr/~jch/software/polipo/)
-   [comp.web.polipo.user at gmame
    ](http://dir.gmane.org/gmane.comp.web.polipo.us)
-   If polypo is installed locally:
    -   [Polipo Webserver](http://localhost:8123/polipo/) local interface:
        [Config](http://localhost:8123/polipo/config?),
        [servers statistic](http://localhost:8123/polipo/servers?),
        [indices of the disk cache](http://localhost:8123/polipo/index?)
    -   [Polypo local documentation](http://127.0.0.1:8123/doc/)

-   See DataNameServer for polipo resolv ignoring `/etc/hosts`
-   To switch polipo ON-LINE or OFF-line:

        sudo  /usr/lib/polipo/polipo-control go-online
        sudo  /usr/lib/polipo/polipo-control go-offline

# SSL Certificates

-   <http://wiki.cacert.org/> deliver free server certificates.
-   <http://wiki.cacert.org/wiki/ServerCerts> explain how
    to produce the certificate request (CSR), then we can combine the
    certificate and the private key in a file ` mycert.pem`
-   we can test the pem file with

        openssl s_server -cert mycert.pem -www

-   a browser pointed at `https://localhost:4433/` then gives the
    details of the certificate.
-   All these openssl command usage is described at
    [OpenSSL Command-Line HOWTO](http://www.madboa.com/geek/openssl/).
-   [HOWTO: Creating your own CA with OpenSSL
    ](http://svn.osafoundation.org/m2crypto/trunk/doc/howto.ca.html) uses the perl script CA.pl
-   [Introducing SSL and Certificates using OpenSSL
    ](http://old.pseudonym.org/ssl/wwwj-index.html) by Frederick J. Hirsch
-   [ldoc:apache2.2-common/README.Debian.gz]
-   The package ssl-cert  is a wrapper for openssl req  to create self-signed certificates.
-   we can use the command line

        openssl req -new -x509 -keyout server.pem -out server.pem -days 365 -nodes

-   [StartCom Free SSL Certification Authority](http://cert.startcom.org/)
-   To use https with virtual host we need [SNI
]https://wiki.apache.org/httpd/NameBasedSSLVHostsWithSNI)

# Mirroring Tools
-   [How To mirror your web site with rsync
    ](http://www.howtoforge.com/mirroring_with_rsync)
-   [httrack](http://www.httrack.com)
    download a website from the Internet to a local directory

# Free.fr conf

-   .htaccess allows Redirect, File and Directory access, htpasswd
-   RedirectMatch seems to no longer work properly, Rewrite is not allowed.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
