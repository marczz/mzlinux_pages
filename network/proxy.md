---
title: Proxy
---


# HTTP Proxies {#http_proxies}
Wikipedia: {{< wp "Proxy server" >}} review the different types of proxy
servers.  An {{< wp "open proxy" >}} is a proxy server that is accessible by
any Internet user. An {{< wp "anonymizer" >}} or an _anonymous proxy_ make
activity on the Internet untraceable by acting as an intermediary and
privacy shield between a client and the Internet. A
[Reverse proxy](http://en.wikipedia.org/wiki/Reverse_proxy)
is on server routing web connection to an other server.

A _Transparent proxy_ or _intercepting proxy_ intercepts normal
communication at the network layer without modifying the request or
response beyond what is required for proxy authentication and
identification.

-   Wikipedia: {{< wp "Proxy server" >}}, {{< wp "HTTP Tunnel" >}},
    {{< wp "Category:Free proxy servers" >}}, {{< wp "Category:Forward_proxy" >}},
    {{< wp "Category:Reverse proxy" >}},
    {{< wp "Category:Proxy server software for Linux" >}}.
-   [proxycheck](http://www.corpit.ru/mjt/proxycheck.html) (GPL)
    is a  tool to check whenever a given host or set of hosts has
    an open proxy server running. One use is to allow to know which
    hosts has an unsecure open proxy, and block them.
    _proxycheck_ is in Debian. _Last release 2004_.

-   [micro-proxy](http://www.acme.com/software/micro_proxy/)
    from [acme]((http://www.acme.com) is a tiny (500 slocs)
    HTTP/HTTPS proxy which is run from inetd, so it has poor
    performance, but is adequate for low traffic.
    It is in Debian _last release 2014, Debian seems behind!_.
-   [mitmproxy](https://mitmproxy.org/) (MIT License)
    is an interactive, SSL-capable intercepting proxy with a console
    interface written in python3.
    It comes wit a CLI _mitmdump_ and a Web GUI _mitmweb_.
    mitmproxy is in Debian.
    -   [mitmproxy documentation](https://docs.mitmproxy.org/stable/).
    -   [Explanation of unencrypted explicit proxy and
        transparent proxying of TLS-protected traffic
        ](https://docs.mitmproxy.org/stable/concepts-howmitmproxyworks/).
-   {{< iref "nginx" "Nginx" >}} can be used as a
    proxy/reverse_proxy see the {{< iref "nginx" "nginx section" >}}, the
    [proxying examples ](http://wiki.nginx.org/Configuration#Proxying_examples)
    and the module
    [ngx_http_proxy_module
    ](http://nginx.org/en/docs/http/ngx_http_proxy_module.html).
-   [Pound](http://www.apsis.ch/pound/) (GPL) is a reverse proxy, load
    balancer and HTTPS front-end. Pound proxies HTTPS to HTTP allowing
    to offer https, with an http only backend. Pound is in Debian.
-   _phpMyProxy_ (GPL) is a PHP proxy script. While PHPMyProxy is live
    in many places in the web [like here
    ](http://6toyens.free.fr/phpMyProxy_1.0.3/) but the download site
    is down. You can find the source in [this Git Repository
    ](https://github.com/oskarp/4ME102/tree/master/Workshop3/phpMyProxy),
    or an other version [here
    ](http://www.thomascandrian.ch/index.php?id=40).

# CGI Proxies
A [CGI proxy](https://en.wikipedia.org/wiki/Proxy_server#CGI_proxy)
target URLs using a Web form and return the result and returns the
results to the user's browser. It is used when the browser proxy
settings to be changed.

   [cgiproxy](http://www.jmarshall.com/tools/cgiproxy/) (free private
    License) is a CGI perl
    script acts as an HTTP or FTP proxy.
     _actively maintained in 2017_
-   [Glype](http://www.glype.com/) (closed source - free download)
    PHP5 proxy script.
-   [PHPproxy](https://bitbucket.org/arkadi/phpproxy/src/default/)
    (GPL) small script (110 slocs) programmed in PHP to bypass
    firewalls and other proxy restrictions through a Web
    interface. The repository contains also a (110 slocs) python proxy
    script. _Last release 2006_.
-   [PHP Web Proxy](http://sourceforge.net/projects/php-proxy/) (GPL)
    php proxy script not updated since 2002.

# Socks Proxy servers {#socks_proxy}

-   Wikipedia: {{< wp "SOCKS" >}}
-   [Antinat SOCKS server](http://www.malsmith.net/antinat/)
    is a SOCKS 4, SOCKS 4a, SOCKS 5 proxy with authentication, CHAP,
    XML firewalling, server chaining, and UDP.
-   <a name="dante"></a>[Dante](http://www.inet.no/dante/) (BSD License)
    is a SOCKS server and a SOCKS client. _active in 2018_
    -   [Dante documentation](http://www.inet.no/dante/doc/).
    -   [Dante FAQ](http://www.inet.no/dante/doc/faq.html).
    -   [how to set up danted (dante-server) SOCKS proxy on
        Linux/Debian with authentication
        ](https://tech.tiq.cc/2012/06/how-to-set-up-danted-dante-server-socks-proxy-on-linuxdebian-with-authentication/).
    -   [User based access control for Skype
        ](http://blog.davidvassallo.me/2011/03/16/user-based-access-control-for-skype/)
        uses _Dante_ socks server.
-   {{< wp "shadowsocks" >}} (Apache License)
    encrypted socks proxy project, widely used in mainland China to
    circumvent Internet censorship. The GitHub repositories provides
    client and servers in many languages C, Go, python, rust ...
    _shadowsocks_ is in Debian.
    -   [Shadowsocks Home](https://shadowsocks.org/)
    -   [GitHub - Shadowsocks](https://github.com/shadowsocks/)
-   [SS5](http://ss5.sourceforge.net/) (GPL)
    is a socks server that implements the SOCKS v4 and v5 protocol.
    _Last release 2013_.
-   [3proxy](https://3proxy.ru/)  (BSD License)
    A multiprotocol proxy DNS, FTP, HTTP, HTTPS, POP, SMTP, SOCKSv4,
    SOCKSv5, TCP and UPD port forwarding. With Proxy chaining,
    Logging, Accesscontrol.It allows support for chroot, setgid,
    setuid _active in 2018_
    -   [GitHub - 3proxy](https://github.com/z3APA3A/3proxy/).
    -   [3proxy Documentation](https://3proxy.ru/documents/).
    -   [3proxy SOCKS5 Proxy with Authentication
        ](https://community.online.net/t/3proxy-socks5-proxy-with-authentication/614)
        How To with the address of an Arm V7 download.
    -   3proxy has [many plugins](https://3proxy.ru/plugins/)
        for transparent proxying, ssl plugin, pcre plugin, log
        analyzers.
    -   The last version source code is in the [releases directory
        ](https://github.com/z3APA3A/3proxy/releases).
    -   [Insomnia247](https://www.insomnia247.nl/):
        [compilation  script
        ](http://kokakukidotai.insomnia247.nl/3proxy/).
    -   benjamin74 [3proxy installation script
        ](https://github.com/benjamin74/3proxy)
    -   There were a [PPA for 3proxy
        ](https://launchpad.net/~silvenga/+archive/ubuntu/3proxy/)
        for installing on Debian/Ubuntu, but it host only an old
        version of 3proxy.

# Caching Proxies
-   <a name="squid"></a>[w:Squid_(software)|Squid](GPL)
    is an internet Object Cache and proxy server written in C++
    -   [Squid Home](http://www.squid-cache.org/)
    -   [Feature: HTTPS](https://wiki.squid-cache.org/Features/HTTPS)
        describe the challenge of caching HTTPS with squid.
        It uses the Feature [SslBump Peek and Splice
        ](https://wiki.squid-cache.org/Features/SslPeekAndSplice)
        for TLS traffic.
    -   [ArchWiki - Squid](https://wiki.archlinux.org/index.php/Squid).
    -   [jesred](http://www.linofee.org/~jel/webtools/jesred/) (GPL)
        is a [redirector
        ](https://wiki.squid-cache.org/Features/Redirectors)
        for _Squid_. It is in Debian.
    -   [adzapper](http://adzapper.sourceforge.net/) (BSD License)
        ad zapping with squid.
    -   [SquidGuard](http://www.squidguard.org/) (GPL)
        is a URL redirector used to use blacklists with  _Squid_.
        _Last release 2015._
-   [microproxy](https://github.com/thekvs/microproxy) (MIT License)
    is a lightweight non-caching HTTP/HTTPS proxy server
    It can have IP-based black and white access lists.
    _active in 2018_.
-   [trafficserver](http://trafficserver.apache.org/) (Apache License)
    by Apache is a scalable reverse proxy server which may operate as
    forward proxy as well.
    It supports caching, filtering, anonymization, load balancing,
    scaling. It is a very active _in 2018)_ and proven software, it is
    used for 400TB a day at Yahoo the company which developped it.
    It is in Debian.

# Filtering Proxies
-   [BFilter](http://bfilter.sourceforge.net/index.php) (GPL)
    a bayesan filtering web proxy _Last update 2009_
-   [ffproxy](http://ffproxy.sourceforge.net/) (GPL)
    is a filtering HTTP/HTTPS proxy server. It is in Debian. _Last
    release 2005_.
-   <a name="polipo"></a>{{< wp "Polipo" >}} (MIT License) is a caching web
    proxy. It is designed to be fast, and lightweight. It supports
    IPv4, IPv6, traffic filtering and privacy-enhancement.  It can be
    configured to use on-disk cache, but in contrast to Squid there is
    no control of the cache size. Polipo can be used with
    {{< iref "#privoxy" "Privoxy" >}} for intercepting
    advertisement and other undesirables.  The development of Polipo
    stopped at end of year 2016, the author of Polipo Juliusz
    Chroboczek says:
    >   the web has changed, and HTTP proxies are no longer useful:
    >   most traffic is encrypted, and a web proxy merely acts as a
    >   dumb intermediary for encrypted traffic.
    >   - if you need your HTTP traffic to originate from a remote IP
    >   address, use a VPN or a SOCKS5 proxy;
    >   - if you need better caching, use a better browser;
    >   - f you need to share your cache, or you need  HTTP/1.1
    >   pipelining, you're out of luck.

    Note that the first assumption is no more valid, because you can
    intercept the HTTPS with a MITM proxy.

    If you want to use a caching proxy, you can now replace it with
    {{< iref "#squid" "Squid" >}} and for filtering
    {{< iref "#privoxy" "Privoxy" >}}.
    Polipo is in Debian.
    -   [Polipo Home](https://www.irif.fr/~jch//software/polipo/).
    -   [Polipo Manual
        ](https://www.irif.fr/~jch//software/polipo/manual/index.html).
    -   [Polipo FAQ
        ](https://www.irif.fr/~jch//software/polipo/faq.html).
    -   [ArchWiki: Polipo
        ](https://wiki.archlinux.org/index.php/Polipo)
-   <a name="privoxy"></a>[Privoxy](http://www.privoxy.org/) (GPL)
    a filtering web proxy.
    It is an improvement of the now obsolete Internet Junkbuster .
    It is in Debian. _active in 2018_.
    -   [freeedom-privoxy](https://github.com/jvasile/freedombox-privoxy)
        _2012_,  is a mod of Privoxy
        tailored for use on a
        [Freedom Box](http://wiki.debian.org/FreedomBox)
-   {{< wp "Tinyproxy" >}} (GPL) is a HTTP proxy server daemon for
    Unix. Designed to be fast and small, it is useful when the system
    resources for a larger proxy are unavailable. It has been put to
    uses such as a tether on the iPhone, and on the OpenWrt.

    TinyProxy can be used as a transparent proxy and reverse proxy.
    It can filter HTTP Headers allowing to implement privacy features
    by filtering inward and outward HTTP traffic. It is in Debian
    -   [TinyProxy Home and Documentation
        ](https://tinyproxy.github.io/).
    -   [GitHub - TinyProxy](https://github.com/tinyproxy/tinyproxy).

# Content Filtering Proxies
-   <a name="dansguardian"></a>{{< wp "DansGuardian" >}} (GPL)
    is a web content filter. It filters the actual content of pages
    based on many methods including phrase matching, PICS filtering
    and URL filtering.

    {{< iref "#squid" "Squid" >}} is the recommended Proxy
    but DansGuardian work also many proxy servers, such as
    {{< iref "#polipo" "Polipo" >}}  or
    {{< iref "#tinyproxy" "Tinyproxy" >}}.

    _DansGuardian_ development stopped in 2012.
    {{< iref "#e2guardian" "E2Guardian" >}} is a recent fork of
    _DansGuardian_. _DansGuardian_ is in Debian.
-    <a name="e2guardian"></a>{{< wp " E2Guardian" >}} (GPL)
    e2guardian filters the content of pages based on many methods
    including phrase matching, PICS filtering and URL filtering.
    _e2guardian_ works with a caching Proxy like
    {{< iref "#squid" "Squid" >}}. E2Guardian is in Debian.
    -   [GitHub: e2guardian](https://github.com/e2guardian/e2guardian)
    -   [e2guardian Wiki
        ](https://github.com/e2guardian/e2guardian/wiki).
    -   E2Guardian can filter HTTPS content by
        [implementing  a MITM proxy
        ](https://github.com/e2guardian/e2guardian/wiki/MITM---Filtering-HTTPS),
        see also the note [ssl_mitm
        ](https://github.com/e2guardian/e2guardian/blob/v5.1/notes/ssl_mitm).

# Proxifiers {#proxifier}

When an application has builtin support for socks (or HTTP) proxy this allow to
use it from the lan to internet through a proxy in the firewall.
For other applications we need a proxifier that intercept TCP (and
possibly UDP) connection and send them through the SOCKS or HTTP
proxy.


-   {{< iref "#dante" "Dante" >}} contains the
    [proxify](http://www.inet.no/dante/doc/1.4.x/socksify.1.html)
    utility for runtime socksification of selected programs by
    redirecting all networking-related system calls to a library in
    the `LD_PRELOAD` path.
-   [Proxychain](http://proxychains.sourceforge.net/) (GPL)
    force any tcp connection made by any given tcp client to follow
    through proxy (or proxy chain). It is a kind of proxifier. It
    supports SOCKS4, SOCKS5 and HTTP CONNECT proxy servers.
    _Proxychain_ is in Debian. _last release 2013_.
-   <a name=redsocks"></a>[Redsocks](http://darkk.net.ru/redsocks/)
    (Apache License)
    transparently tunnel any TCP connection via a remote SOCKS4,
    SOCKS5 or HTTP proxy server. It uses the system firewall's
    redirection facility to intercept TCP connections.
    Redsocks supports tunneling TCP connections and UDP packets.

    It can be sused WHEN you use tor and don't want any TCP connection
    to leak.

    _RedSocks_ is in Debian _and is active in 2018_.

    -   [GitHub - Redsocks](https://github.com/darkk/redsocks/)

-   [tsocks](http://tsocks.sourceforge.net/about.php)
    provides transparent network access through a SOCKS version 4 or 5
    proxy (usually on a firewall). tsocks intercepts the calls
    applications make to establish TCP connections and transparently
    proxies them as necessary. This allows applications without
    builtin socks support to use SOCKS.

    _tsocks_ is still in Debian, but _no more developed since
    2002_. You may prefer {{< iref "#dante" "Dante" >}} which
    has a similar library _socksify_ or
    {{< iref "#tor" "torsocks" >}}
    which is an improved version of tsocks or
    {{< iref "#redsocks" "Redsocks" >}}.

# HTTP Tunnel {#http_tunnel}
We can capture the output of a network application and encapsulate it
in HTTP packets. This a simpler alternative to proxyfier and is often
used for ssh when we are inside a firewall that allows only
HTTP/HTTPS.


-   [connect-proxy](https://bitbucket.org/gotoh/connect) (GPL)
    make tunnel TCP connection via SOCKS or HTTPS proxies. It is
    mainly intended to be used as proxy command of OpenSSH.
    -   [connect manpage
        ](https://bitbucket.org/gotoh/connect/raw/2e080df38b35a529f51d8dd13569816f145d14d8/doc/manual.txt)
-   [corkscrew
    ](https://web.archive.org/web/20170510154150/http://agroman.net/corkscrew/)
    tunnel TCP connections through an HTTP proxy supporting the CONNECT method.
    It can be used to connect to an SSH server running on a remote 443
    port through a strict HTTPS proxy. Corkscrew is in Debian.
    -   The original site is down, but there is a copy of the source
        code on
        [GitHub - bryanpkc/corkscrew
        ](https://github.com/bryanpkc/corkscrew).
-   [desproxy](http://desproxy.sourceforge.net/) (GPL)
    tunnel  TCP traffic through a HTTP proxy.
    It is in Debian. _Last release 2004_
-   [Proxytunnel](http://proxytunnel.sourceforge.net/intro.php) (GPL)
    is a program that connects stdin and stdout to a server somewhere
    on the network, through a standard HTTPS proxy. We mostly use it
    to tunnel SSH sessions through HTTP(S) proxies.

    The last stable release _1.9.0_ is dated _2008_.
    Debian package a version from the svn repo, _2012/2014_.
    In the [Github project
    ](https://github.com/proxytunnel/proxytunnel).
    there are some new commits on the source code.

    -   [Proxytunel svn repository
        ](https://sourceforge.net/p/proxytunnel/)
    -   [GitHub - Proxytunnel
        ](https://github.com/proxytunnel/proxytunnel).
    -   [Tunneling SSH over HTTP(S)
        ](http://dag.wiee.rs/howto/ssh-http-tunneling/)
        by Dag Wieers uses proxytunnel.




# Debugging proxies
-   [Fiddler](http://www.telerik.com/fiddler)
    a .net web debugging proxy, closed source, free downloads.
    it can work on a virtualbox windows.
    To use it with Linux you could try [Fiddler for Mono
    ](http://fiddler.wikidot.com/mono)
-   [NetTool](http://nettool.sourceforge.net/)
    is a developer tool for debugging and testing networked
    applications, with a specific emphasis on webapps and web services
    (i.e. HTTP-based applications).

    NetTool consists of two distinct tools: HTTP Client, and TCP Tunnel.

-   [Zaproxy](https://github.com/zaproxy/zaproxy) from OWASP, is the
    fork of the old [Paros](http://sourceforge.net/projects/paros/)
    which is unmaintained since 2004. It is an integrated penetration
    testing tool for finding vulnerabilities in web applications.



# Tor {#tor}
{{< wp "Tor_(anonymity_network)"  "Tor" >}} routes Internet traffic through a
worldwide volunteer network of servers. It uses {{< wp "Onion routing" >}}
to encrypt multiple times the data, and send it through successive Tor
relay.

This concept is also used in the {{< wp "I2P anonymous network" >}}.

-   [Tor Project](https://www.torproject.org/).
-   [Tor documentation
    ](https://www.torproject.org/docs/documentation).
-   [Tor ManPage](https://www.torproject.org/docs/tor-manual.html.en).
-   [Tor Wiki
    ](https://trac.torproject.org/projects/tor/wiki/WikiStart).
-   [Torsocks
    ](https://trac.torproject.org/projects/tor/wiki/doc/torsocks)
    is a torifying wrapper that is primarily used to
    redirect all the network traffic of individual SOCKS-friendly
    applications through the Tor network. It also ensures DNS queries
    are handled correctly and explicitly blocks all UDP traffic from
    the application. Torsocks is the successor of tsocks
    and is
    actively maintained. It is in Debian.
-   [Tor Bridges](https://www.torproject.org/docs/bridges.html.en)
    are Tor relays that aren't listed in the main Tor directory, and
    the ISP may be unable to block.
-   [Tor Pluggable Transports
    ](https://www.torproject.org/docs/pluggable-transports)
    are used when
    the censor can use DPI to recognize and filter Tor traffic flows
    even when they connect to unexpected IP addresses like a Tor
    Bridge.
-   [Tor list of Pluggable Transports
    ](https://www.torproject.org/docs/pluggable-transports.html.en#list-of-pts)
-   [obfs4](https://github.com/Yawning/obfs4/)
    is a pluggable transport for Tor written in _Go language_.  It is
    in the Debian package _obfs4proxy_. Note that it improves and
    replaces the Python Pluggable transport _ScrambleSuit_ that is in
    the Debian package _obfsproxy_.  For use inside TorBrowser you
    don't need an external package as it is already deployed inside
    TorBrowser Code
-   [ArchWiki: Tor](https://wiki.archlinux.org/index.php/Tor)
-   Tor provides a socksproxy.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
