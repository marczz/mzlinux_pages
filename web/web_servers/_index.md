---
title: Web Servers
---

-    The main stream servers have their own page:
    {{< iref "apache" "Apache" >}},
    {{< iref "lighttpd" "Lighttpd" >}},
    {{< iref "nginx" "Nginx" >}}.
-   See also {{< iref "php" "PHP-FPM" >}}.

# Server Architectures

The different server architectures and a comparison are
introduced in the
[Server Architectures chapter from Benjamin Erb's Thesis
](http://berb.github.io/diploma-thesis/community/042_serverarch.html).

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
flow of execution. This is the model used by {{< iref "lighttpd" "lighttpd" >}}, {{< iref "#nginx" "nginx" >}},
the python web server {{< iref "python_web#tornado" "Tornado" >}},
{{< iref "python_web#cyclone" "cyclone" >}},
the emacs server {{< iref "emacs#elnode" "elnode" >}} and many
new servers.

For more details look at the B. Erb chapters on
[I/O multiplexing patters](
http://berb.github.io/diploma-thesis/community/042_serverarch.html#io)
and [hybrid server architecture
](http://berb.github.io/diploma-thesis/community/042_serverarch.html#combined).

## Acme httpd servers
-   [thttpd](http://www.acme.com/software/thttpd/)  has CGI, external
    SSI as cgi program, and a throttling feature,
-   [mini\_httpd](http://www.acme.com/software/mini_httpd/) 0.7Meg,
    includes CGI,
-   [micro\_httpd](http://www.acme.com/software/micro_httpd/) a
    tiny server that can run from inetd/xinetd

# web log analysis
-   {{< wp "analog" >}} web log analysis program
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
