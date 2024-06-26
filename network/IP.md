---
title: IP protocols
---

See also {{< iref "netconf" "Network Configuration" >}},
{{< iref "nettools" "Network Tools" >}}.

The {{< wp "Link layer" >}} _layer 2 of OSI_ group
ARP, NDP, OSPF, Tunnels (L2TP), PPP, MAC,
(Ethernet, DSL, ISDN, FDDI)

The OSI Layer 3 [network layer] or the TCP/IP {{< wp "Internet layer" >}}
group many protocols among which
IPv4/IPv6 (see {{< iref "nettools#ip_tools" "iptools" >}},
ICMP, ICMPv6, ECN, IGMP, IPsec.

The {{< wp "Transport layer" >}} _Layer 4 of OSI_ contains
TCP, UDP (see {{< iref "nettools#tcp_udp_tools" "TCP /UDP tools" >}},
DCCP, SCTP, RSVP  we can add
{{< iref "#socks" "SOCKS" >}} in the OSI layer 5
{{< wp " session layer" >}}.

The {{< wp "Application layer" >}} OSI Level 7 and Application Layer of TCP
stack from {{< wp "internet protocol suite" >}} _TCP/IP stack_ group many
protocols, some referenced in other pages it groups
BGP, {{< iref "#dhcp" "DHCP" >}},
{{< iref "dns" "DNS" >}},
{{< iref "file_transfer#ftp" "FTP" >}},
{{< iref "#gemini" "Gemini" >}},
{{< iref "#gopher" "GOPHER" >}},
{{< iref "#http" "HTTP" >}},
{{< iref "mail" "IMAP" >}},
{{< iref "irc" "IRC" >}},
LDAP MGCP, {{< iref "feed#nntp" "NNTP" >}},
{{< iref "ntp" "NTP" >}},
{{< iref "mail" "POP" >}},
ONC/RPC, RTP, RTSP, RIP,
{{< iref "sip" "SIP" >}},
{{< iref "mail" "SMTP" >}},
{{< iref "monitoring" "SNMP" >}},
SSH, Telnet, {{< iref "ssl" "TLS/SSL" >}},
{{< iref "xmpp" "XMPP" >}}

-----------------

# General References

-   Wikipedia: {{< wp "Lists of network protocols" >}}, {{< wp "Internet Protocol" >}}
    (IP) , {{< wp "Internet protocol suite" >}} (TCP/IP),    {{< wp "UDP" >}}
-   Wikipedia {{< wp "OSI model" >}},
    {{< wp "Link layer" >}} _layer 2 of OSI_, {{< wp "Internet layer" >}} or
    [network layer] _Layer 3 of OSI_,
    {{< wp "Transport layer" >}} _Layer 4_,
    {{< wp " session layer" >}} _layers 5_ , _6 presentation_ and {{< wp "Application layer" >}}
    _layer 7_,
-   UDP protocol is defined in the  [rfc 768](https://tools.ietf.org/html/rfc768)
    an TCP protocol in the [rfc 793](https://tools.ietf.org/html/rfc/793)
-   [Cisco: Internetworking Technology Handbook
    ](http://docwiki.cisco.com/wiki/Internetworking_Technology_Handbook).
-   [linux foundation - Kernel Networking
    ](http://www.linuxfoundation.org/collaborate/workgroups/networking/)
-   [Omnisecure - TCP/IP articles](https://www.omnisecu.com/tcpip/index.php) with
    explanations OSI and TCP/P layers.

# Bridge

-   {{< wp "Bridging (networking)"  "Wikipedia Bridging" >}},
    {{< wp "Address Resolution Protocol"  "ARP" >}}
-   [Kernel networking: Bridges
    ](http://www.linuxfoundation.org/collaborate/workgroups/networking/bridge)
-   [Cisco: Bridging and Switching Basics
    ](http://docwiki.cisco.com/wiki/Bridging_and_Switching_Basics)
-   [Ebtables](http://ebtables.sourceforge.net/) is a filtering
    tool for a bridging firewall. It is similar at the link layer level
    to iptables at the ip level.
-   [Linux Advanced Routing & Traffic Control HOWTO Chapter 16.
    Building bridges, and pseudo-bridges with Proxy ARP
    ](http://lartc.org/howto/lartc.bridging.html).
-   [ProxyARP Subnetting HOWTO
    ](http://www.faqs.org/docs/Linux-mini/Proxy-ARP-Subnet.html)
    by Bob Edwards.
-   [Proxy ARP with Linux](https://www.televationcomm.com/linux/proxyarp/)
    by David Weis.
-   [Virtual Square
    ](http://wiki.v2.cs.unibo.it/wiki/index.php?title=Main_Page)
    :
    [VDE](http://wiki.v2.cs.unibo.it/wiki/index.php?title=VDE)
    (GPL) .is an ethernet compliant virtual network that can be spawned
    over a set of physical computer over the Internet. VDE switch
    implements is a virtual switch. Read also
    [VDE Basic Networking Tutorial
    ](http://wiki.v2.cs.unibo.it/wiki/index.php?title=VDE_Basic_Networking).
-   A {{< wp "network switch" >}} is a device that use packet switching to
    receive data from a source device, process and forward it to the
    destination device.
-   The {{< wp "Spanning Tree Protocol" >}} (STP) is a network protocol that builds
    a logical loop-free topology for Ethernet networks.

# SOCKS {#socks}
{{< wp "SOCKS" >}} is an Internet protocol of the OSI {{< wp "session layer" >}}
(layer 5). It forward packets between a client and server through a proxy server.
SOCKS5 additionally provides authentication.

See also {{< iref "proxy#socks_proxy" "Socks Proxy servers" >}}.

-   [RFC 1928](http://www.ietf.org/rfc/rfc1928.txt)
    SOCKS Protocol Version 5
-   [RFC 1929](http://www.ietf.org/rfc/rfc1928.txt)
    Username/Password Authentication for SOCKS V5
-   [RFC1961](http://www.ietf.org/rfc/rfc1961.txt),
    GSS-API Authentication Method for SOCKS Version 5.

-   [Proxy-Server Based Firewalls (pdf)
    ](https://engineering.purdue.edu/kak/compsec/NewLectures/Lecture19.pdf)
    from Avinash Kak at Purdue
    [Computer and Network Security lecture notes
    ](https://engineering.purdue.edu/kak/compsec/Lectures.html)
    in Lecture 19.

# DHCP {#dhcp}

-   [Wikipedia: DHCP](http://en.wikipedia.org/wiki/DHCP),
    {{< wp "Comparison of DHCP server software" >}}, {{< wp "DHCPD" >}}.
-   [DHCP RFC - Dynamic Host Configuration Protocol RFC's
    ](http://www.bind9.net/rfc-dhcp) , and
    [DHCP Articles and Links](http://www.bind9.net/dhcp) at bind9.net.
-   Out of the 56 current dhcp rfcs, you can want to use:
    -   [RFC 2131 Dynamic Host Configuration Protocol
        ](https://tools.ietf.org/html/rfc2131)
    -   [RFC 2132 DHCP Options and BOOTP Vendor Extensions
        ](https://tools.ietf.org/html/rfc2132)
        (supersedes rfc 1497 BOOTP Vendor Information Extensions)
    -   [RFC 2937 The Name Service Search Option for DHCP
        ](https://tools.ietf.org/html/rfc2937) extended by
    -   [RFC 3397 DHCP Domain Search Option](https://tools.ietf.org/html/rfc3397)
    -   [RFC 3004 The User Class Option for DHCP
        ](https://tools.ietf.org/html/http://rfc.net/rfc3004)
    -   [RFC 3046 DHCP Relay Agent Information Option
        ](https://tools.ietf.org/html/rfc3046)
        (extend rfc2132)
    -   [RFC 3397 DHCP Domain Search Option](https://tools.ietf.org/html/rfc3397)
    -   [RFC 3442 The Classless Static Route Option for DHCP version 4
        ](https://tools.ietf.org/html/rfc3442)
    -   [RFC2855 DHCP for IEEE 1394 (FireWire)](https://tools.ietf.org/html/rfc2855)
    -   [RFC 4390 DHCP over InfiniBand](https://tools.ietf.org/html/rfc4390)
-   [ISC dhcp page](https://www.isc.org/downloads/dhcp/) has
    reference material links and links to their tools suite DHCP server,
    DHCP client, DHCP relay agent.
-   [dhcpd](https://www.isc.org/downloads/dhcp/) is the reference
    implementaion of DHCP Server by Internet Systems Consortium.
    -   [ArchWiki: dhcpd](https://wiki.archlinux.org/index.php/Dhcpd).
    -   [Debian Wiki: DHCP Server](https://wiki.debian.org/DHCP_Server)
-   [dhcpcd](https://roy.marples.name/projects/dhcpcd/)
    is a full RFC2131 compliant DHCP and DHCPv6
    client and the only open source DHCP client to support out of
    [RFC2131 Dynamic Host Configuration Protocol](https://tools.ietf.org/html/rfc2131),
    [RFC 3004 The User Class Option for DHCP](https://tools.ietf.org/html/rfc3004),
    [RFC 3397 DHCP Domain Search Option](https://tools.ietf.org/html/rfc3397),
    [RFC 3442 The Classless Static Route Option for DHCP version 4
    ](https://tools.ietf.org/html/rfc3442),
    [RFC 2855 DHCP for IEEE 1394 (FireWire)](https://tools.ietf.org/html/rfc2855),
    [RFC 4390 DHCP over InfiniBand](https://tools.ietf.org/html/rfc4390).

    Dhcpd is
    said to be less memory and cpu hungry than the isc dhclient, it
    works under Linux and BSD.

    -   [dhcpd - Git repository](https://roy.marples.name/git/dhcpcd/tree) and
        [dhcpd - Github mirror](https://github.com/NetworkConfiguration/dhcpcd).
    -   [ArchWiki: dhcpcd](https://wiki.archlinux.org/index.php/Dhcpcd)
    -   Man pages {{< man "dhcpd" >}}, [man: dhcpcd.conf)

-   [udhcp Server/Client Package](http://udhcp.busybox.net) are a
    lightweight implementation of dhcp daemon and client, they are now
    integrated in busybox the ref for the client is
    [Readme udhcpc](http://udhcp.busybox.net/README.udhcpc),
    [udhcpc(8)](http://man.cx/udhcpc "man.cx man page") and for the
    server: [Readme udhcpcd](http://udhcp.busybox.net/README.udhcpd),
    [Readme dumpleases](http://udhcp.busybox.net/README.dumpleases)
    and [udhcp.conf example configuration
    file](http://udhcp.busybox.net/udhcpd.conf).
-   {{< iref "dns" "Dnsmasq" >}} (GPL)
    beside a dns cache server is also a dhcpd server. It supports
    static address assignments, multiple networks, Bootp and
    vendor-encapsulated options, DHCP-relay and RFC3011 subnet
    specifiers.
-   [Dibbler](http://klub.com.pl/dhcpv6/) (GPL) is
    a portable DHCPv6 implementation.
-   [DHCP Forwarder](http://www.nongnu.org/dhcp-fwd/) is
    a small dhcp relay.
-   [DHCP mini-HOWTO](http://tldp.org/HOWTO/DHCP/index.html) _2000_.

# Network Boot (PXE, Bootp) {#network_boot}
-   [Wikipedia: PXE (Preboot eXecution Environment)
    ](http://en.wikipedia.org/wiki/Preboot_Execution_Environment),
    {{< wp "Bootstrap Protocol" >}} (Bootp),
-   [Network Boot and Exotic Root HOWTO
    ](http://tldp.org/HOWTO/Network-boot-HOWTO/index.html) _2002_.
-   [ArchWiki: Diskless system](https://wiki.archlinux.org/index.php/Diskless_system),
    has a chapter on PXE.
-   [ArchWiki: Pxe](https://wiki.archlinux.org/index.php/PXE)
-   [Pxelinux](https://www.syslinux.org/wiki/index.php?title=PXELINUX)
    is a SYSLINUX derivative, for booting Linux off a network server.
-   [Archwiki: Syslinux - Pxelinux
    ](https://wiki.archlinux.org/index.php/Syslinux#PXELINUX)
-   [Remote Network Boot via PXE](http://www.kegel.com/linux/pxe.html),
    [Intel PXE specification](http://www.pix.net/software/pxeboot/archive/pxespec.pdf).
    ](http://www.munts.com/diskless/Docs/pxespec.pdf)
-   [Debian Installation Guide 4.5. Preparing Files for TFTP Net Booting
    ](https://www.debian.org/releases/stable/amd64/ch04s05)
-   [Installing Debian using PXE](https://wiki.debian.org/PXEBootInstall)
-   [Root over nfs clients & server Howto
    ](http://tldp.org/HOWTO/Diskless-root-NFS-HOWTO.html) _1999_,
    [Root over NFS - Another Approach
    ](http://tldp.org/HOWTO/Diskless-root-NFS-other-HOWTO.html) _2001_,
    [NFS-Root-Client Mini-HOWTO
    ](http://tldp.org/HOWTO/NFS-Root-Client-mini-HOWTO/index.html) _1999_.
-   [Preparing Debian for Tftp (PXE) Booting
    ](https://www.debian.org/releases/stable/amd64/ch04s05.html)
    from [Debian Installation Manual
    ](https://www.debian.org/releases/stable/amd64/).
-   Kernel Documentation:
    [Mounting the root filesystem via NFS (nfsroot)
    ](https://www.kernel.org/doc/Documentation/filesystems/nfs/nfsroot.txt)
-   [DRBL (Diskless Remote Boot in Linux)](http://drbl.sourceforge.net/)
    provides a diskless or systemless environment for client machines.  DRBL uses
    distributed hardware resources and makes it possible for clients to fully access
    local hardware.  It also includes
    {{< iref "hdrive#clonezilla" "Clonezilla" >}}
    partition and disk cloning utility.

# HTTP {#http}
See also {{< iref "file_transfer#http_download" "HTTP file download" >}},
{{< iref "proxy" "Proxy" >}}, {{< iref "web_servers" "HTTP daemons"  >}},
{{< iref "html" "HTML" >}}.

-   {{< wp "Hypertext_Transfer_Protocol"  "Wikipedia: Hypertext Transfer Protocol" >}}
-   RFC:
    -   [RFC1945 - HTTP/1.0](https://tools.ietf.org/html/rfc1945).
    -   [RFC2616 - HTTP/1.1](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
        ([sec 10 Status Code Definitions
        ](https://www.w3.org/Protocols/rfc2616/rfc2616-sec10.html)),
    -   [RFC2617 - HTTP Authentication: Basic and Digest Access
        ](https://tools.ietf.org/html/rfc2617),
    -   [RFC1867 - Form-based File Upload in HTML](https://tools.ietf.org/html/rfc1867).
    -   [RFC3875 - The Common Gateway Interface (CGI) Version 1.1
        ](https://tools.ietf.org/html/rfc3875)
-   Http Headers are given in
    {{< wp "List_of_HTTP_headers"  "Wikipedia: List of HTTP headers" >}},
    [The Quick reference to HTTP headers
    ](http://www.cs.tut.fi/~jkorpela/http.html)
    gives cross references to the
    [RFC2616](http://www.w3.org/Protocols/rfc2616/rfc2616.html).
-   [W3C http page](http://www.w3.org/Protocols/)
-   [HTTP Made Really Easy](http://www.jmarshall.com/easy/http/)
    A Practical Guide to Writing Clients and Servers by James
    Marshall.

-   [Red Bot](http://mnot.github.io/redbot/) (MIT License) is a python
    web tool that  check and report HTTP resources.
    A public instance of RED is available at
    [redbot.org](http://redbot.org).
    It allows to follow all redirects on an URL, you just follow the
    succession of *Location* headers. It can be very useful to see how
    big server redirect a download depending on your ip geographic
    zone.

There are many link checkers:
-   [Checklinks](http://www.jmarshall.com/tools/cl/) and
        [linklint]( http://www.linklint.org/) are two old _year 2000 and 2001_
        PERL links checker, _linklint_ is packaged in Debian.
-   [linkchecker](https://github.com/linkchecker/linkchecker) (GPL-2.0)
    is a python link checker. Debian offer  two packages a CLI _linkchecker_ and web
    interface _linkchecker-web_.
    -   [linkchecker manual](https://linkchecker.github.io/linkchecker/), .
-   See also other Python programmatic browsers tools in the
    {{< iref "python_web#web" "Web client side programming section" >}}

# WEB Protocols {#web_protocols}
-   {{< wp "CGI" >}}
    -   [CGI resource index](http://cgi.resourceindex.com/)
    -   [W3C Forms](http://www.w3.org/TR/html4/interact/forms.html)
        are used to call CGI scripts.
    -   [W3C CGI Page](http://www.w3.org/CGI/) (old doc!)
    -   [CGI Made Really Easy](http://www.jmarshall.com/easy/cgi/)
        by James Marshall.

-   {{< wp "FastCGI" >}}
    Under the CGI model, you have to pay the price of spawning a new
    process for each request. To spawn child processes under different
    user accounts, your gateway probably runs under quite high
    privileges which is insecure. The FastCGI/SCGI approach keep the
    process alive and the gateway talk to that process to serve the request.
    Because the gateway doesn't spawn the processes that serve
    requests, the gateway can run with far less privileges enabled.
-   {{< wp "SCGI" >}}
    Simple Common Gateway Interface (SCGI) is a protocol similar to
    FastCGI  as an alternative to the CGI protocol.
    -   Samuel Alexander [scgi-c-library
        ](https://github.com/semitrivial/scgi-c-library)
        and [Introducing: The SCGI C Library
        ](http://www.xamuel.com/scgilib/)
-   {{< wp "Web Server Gateway Interface"  "WSGI" >}} the main page is
    {{< iref "python_web#wsgi" "Python Web - WSGI" >}}
    some non python links follow.
    -   [The uWSGI project documentation
        ](http://uwsgi-docs.readthedocs.org/en/latest/)
    -   [uwsgi_client.c example
        ](https://github.com/unbit/uwsgi/blob/master/contrib/uwsgi_client.c)
        and [uwsgi_dynamic_client.c
        ](https://github.com/unbit/uwsgi/blob/master/contrib/uwsgi_dynamic_client.c).
        from [uwsgi repository
        ](https://github.com/unbit/uwsgi).

# Gemini {#gemini}
{{< wp "Gemini_(protocol)" "Gemini" >}} is an application layer protocol for distributed
hypertext. It aims at being simpler and more secure than http/html, and is inspired by
{{< iref "#gopher" "Gopher" >}}, but uses TLS.

In the same way that HTTP distribute information in WWW, Gemini gives access to
information in {{< wp "Gemini Space" >}}.

-   [Awesome Gemini](https://github.com/kr1sp1n/awesome-gemini)
-   [Circumlunar Space - Project Gemini](https://gemini.circumlunar.space/)
    -   [Project Gemini FAQ](https://gemini.circumlunar.space/docs/faq.html)
    -   [Gemini documentation](https://gemini.circumlunar.space/docs/)
    -   [Gemini software](https://gemini.circumlunar.space/software/)
    -   [Known Gemini servers](https://gemini.circumlunar.space/servers/)
-   [Wikipedia:List of Gemini Software
    ](https://en.wikipedia.org/wiki/Gemini_(protocol)#Software).
-   [Gemini Wiki Space](https://transjovian.org:1965/gemini/) List of Gemini :
    -   [Servers](https://transjovian.org:1965/gemini/page/Servers)
    -   [Clients](https://transjovian.org:1965/gemini/page/Clients)
    -   [Web Proxies](https://transjovian.org:1965/gemini/page/Web%20Proxies)
    -   [Other Software](https://transjovian.org:1965/gemini/page/Other%20Software)
    -   [Sites](https://transjovian.org:1965/gemini/page/Sites)
    -   [Chat](https://transjovian.org:1965/gemini/page/Chat)
-   [portal.mozz.us - Gemini to HTTP proxy](https://portal.mozz.us/)
-   [proxy.vulpes.one - Gemini to HTTP proxy ](https://proxy.vulpes.one/)
-   [geminispace.info search engine](https://gemini.circumlunar.space/x/geminispace.info/)
-   [Gemini mailing list](https://lists.orbitalfox.eu/listinfo/gemini)
-   [Medusae Gemini Directory](https://portal.mozz.us/gemini/medusae.space/) (gemini://medusae.space/)
    a catalog of capsules organised into categories.

-   {{< iref "elpher"  "Elpher Gopher and Gemini Client  for Emacs" >}}.
-   [Lagrange](https://gmi.skyjake.fi/lagrange/)
    desktop GUI client for browsing Geminispace.  It is written in C and uses SDL for
    graphics and OpenSSL for secure communications. It features: sidebar for page
    outline, bookmarks and identities, and viewing history; multiple tabs,
    identity management. It create and use TLS client certificates, and allow audio
    playback for MP3, Ogg Vorbis, WAV.

    Lagrange is in flathub.

# Gopher {#gopher}
The {{< wp "Gopher" >}} internet protocol released in mid-1991 is a predecessor of World
Wide Web designed for distributing, searching, and retrieving documents in IP networks.

Gopher is defined by [rfc 1436](https://tools.ietf.org/html/rfc/1436) _year 1993_.

A list of gopher software, browser support, http gateways, and gopher server is given in
[Wikipedia gopher page](https://en.wikipedia.org/wiki/Gopher_(protocol)#Client_software).


-   [Why still use Gopher? What makes Gopher relevant?
    ](http://gopher.floodgap.com/overbite/relevance.html) by Cameron Kaiser, from the
    Overbite Project.
-   The master Gopherspace search engine is
    [Veronica](https://en.wikipedia.org/wiki/Veronica_(search_engine)).
-   [Public Gopher to HTTP Proxy @ Floodgap.com](http://gopher.floodgap.com/gopher/)
    allow to access Gopher Sites from any Browser withoutin-browser gopher support.
-   <a name="elpher"></a>[Elpher Gopher and Gemini Client for Emacs
    ](https://thelambdalab.xyz/elpher/)
    _elpher_ is in melpa. The full documentation for Elpher can be found in the Info
    manual.
    -   The _elpher_ gopher home page is  gopher://thelambdalab.xyz/1/projects/elpher/
-   [OverbiteWX](https://addons.mozilla.org/en-US/firefox/addon/overbitewx/)
    is an extension for Firefox 56+, that redirect gopher url through the floodgap
    gopher proxy.
-   [OverbiteNX](https://addons.mozilla.org/en-US/firefox/addon/overbitenx/)
    (Floodgap Free Software License)
    is an extension for Firefox 59+ that allows access to gopher content using
    [Onyx native Gopher component](https://github.com/classilla/overbitenx).
-   [Burrow chrome extension](https://gitlab.com/burrow-project/burrow-chrome-extension)
    (MIT License) rewrites all gopher:// links to point to Floodgap's Public Gopher
    Proxy.
-   [PocketGopher](https://github.com/afonsotrepa/PocketGopher) (Unlicense License)
    Gopher browser for android written in java available in F-Droid repository.

# IP routing
_The {{< iref "netconf" "network management utilities" >}}
are in the {{< iref "netconf" "Network Configuration Section" >}}._

-   kernel source tree documentation:
    [Documentation networking
    ](https://www.kernel.org/doc/Documentation/networking/),
    [Documentation of /proc/sys
    ](https://www.kernel.org/doc/Documentation/sysctl/)
-   [sysctl tutorial
    ](http://www.frozentux.net/ipsysctl-tutorial/ipsysctl-tutorial.html)
    _2002_ by Oskar Andreasson
-   [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/)
    by Bert Hubert deals with iproute2, GRE, ipv6 tunneleing, IPSEC,
    multicast, queueing disciplines, netfilter packet
    marking/classifying, Kernel network parameters, proxyarp, OSPF and
    BGP.
-   [rfc 1256 ICMP Router Discovery Messages](http://www.ietf.org/rfc/rfc1256.txt)
    describe the router discovery protocol, you can use it
    as the command line utility {{< man "rdisc" >}}.
-   [rollernet.us](http://rollernet.us/) provides mail redirection
-   [Quagga Software Routing Suite](https://www.nongnu.org/quagga/)
    provides implementations of OSPFv2, OSPFv3, RIP v1 and v2, RIPng and BGP-4 for Unix
    Quagga is a fork of Quagga is a fork of [GNU Zebra](http://www.zebra.org/).
-   [Service Name and Transport Protocol Port Number Registry
    ](https://www.iana.org/assignments/service-names-port-numbers/service-names-port-numbers.xhtml)
    from
    [iana (internet assigned numbers authority)](http://www.iana.org/)
-   [GRC Port Info Database](https://www.grc.com/PortDataHelp.htm).
-   [DSHIELD](https://secure.dshield.org/) port/ip lookup/search:
-   [Debian: Network Configuration](https://wiki.debian.org/NetworkConfiguration)
-   [ArchWiki: Router](https://wiki.archlinux.org/index.php/Router).
-   [Advanced traffic control - ArchWiki
    ](https://wiki.archlinux.org/title/Advanced_traffic_control).

# IP V6 {#ipv6}

-   {{< wp "IPv6"  "Wikipedia: IPv6" >}}, {{< wp "IPv6 address" >}}, {{< wp "IPv6 packet" >}},
    {{< wp "ICMPv6" >}}, {{< wp "Multicast_address#IPv6"  "IPv6 Multicast address" >}},
    {{< wp "DHCPv6" >}}, {{< wp "Comparison of IPv6 support in operating systems" >}}.
-   Wikipedia: {{< wp "IPv6 transition mechanism" >}}, {{< wp "Tunnel broker" >}},
    {{< wp "List of IPv6 tunnel brokers" >}}, {{< wp "6in4" >}}, {{< wp "6to4" >}}, {{< wp "Teredo tunneling" >}},
    {{< wp "IPv6 rapid deployment" >}} or 6rd, {{< wp "NAT64" >}}.
-   [IPv6 Homepage](http://www.worldipv6launch.org/)
-   [Deep Space 6](http://www.deepspace6.net/), the Linux IPv6 Portal
    -   [IPV6 Documentation
        ](http://www.deepspace6.net/sections/docs.html).
    -   [Current Status of IPv6 Support for Networking Applications
        ](http://www.deepspace6.net/docs/ipv6_status_page_apps.html),
-   Peter Bieringer
    [Linux IPv6 Howto Page](http://www.bieringer.de/linux/IPv6/),
    -   Latest [Linux+IPv6-HOWTO
        ](http://mirrors.bieringer.de/Linux+IPv6-HOWTO/),
        [Linux+IPv6-HOWTO (fr)
        ](http://mirrors.bieringer.de/Linux+IPv6-HOWTO-fr/)
    -   Stable at tldp [Linux+IPv6-HOWTO
        ](http://www.tldp.org/HOWTO/Linux+IPv6-HOWTO/)
    -   [Current Status of IPv6 Support for Networking Applications
        ](http://www.deepspace6.net/docs/ipv6_status_page_apps.html)
-   [Debian Wiki: IPV6 Configuration
    ](https://wiki.debian.org/DebianIPv6)
-   [Debian Administration: Running IPv6 in practice
    ](https://debian-administration.org/article/655/Running_IPv6_in_practice)
    gives a configuration for Huricane Electric IPV6 tunnel.
-   [Madduck: IPv6 with Debian](http://madduck.net/docs/ipv6/)
    gives more advanced setting and tunnels configuration.
-   [ArchWiki: IPV6](https://wiki.archlinux.org/index.php/IPv6)
-   [Gentoo IPv6 router guide
    ](https://wiki.gentoo.org/wiki/IPv6_router_guide)
-   [Ubuntu Wiki - IPv6 ](https://wiki.ubuntu.com/IPv6)
-   [The initscripts-ipv6 Homepage
    ](http://www.deepspace6.net/projects/initscripts-ipv6.html)
-   [Association G6: Livre IPv6](http://livre.g6.asso.fr/index.php/Table_des_mati%C3%A8res)
-   [6DEPLOY-2](http://www.6deploy.eu/) :
    [6DEPLOY-2 Tutorials](http://www.6deploy.eu/index.php?page=tutorials2) list of pdf tutorials
-   [Thorsten - tagged ipv6](http://yorickdowne.wordpress.com/tag/ipv6/).
-   [Omnisecu.com IPV6 Tutorials](http://www.omnisecu.com/tcpip/ipv6/index.php).
-   [SI6 Networks](https://www.si6networks.com/) network security:
    [Articles](https://www.si6networks.com/publications/articles/),
    and see below their {{< iref "#pv6toolkit" "[IPv6 Toolkit" >}}."


## DNS64/NAT64
{{< wp "NAT64" >}} is an IPv6 transition mechanism that allows ipv6 only systems to
communicate with IPV4 only sytems. I uses network address translation mechanism
to associates an IPV4 address to an IPV6 address with a prefix. The DNS64 server
gives such AAAA record with a fake ipv6 address using a fixed prefix for an ipV4
only domain.

The associated NAT64 gateway route a NAT64 ipv6 encapsulated packet to the IPV4 host.

-   [Public NAT64 Services - nat64.xyz](https://nat64.xyz/),
    [NAT64 public servers status](https://stats.uptimerobot.com/GQ5RyTJLKZ).
    Each of this service provides a DNS64 server which route packets encapsulated with a
    specific prefix to a NAT64 gateway.
-   Google has a [Google Public DNS64
    ](https://developers.google.com/speed/public-dns/docs/dns64)
    but it should be associated with a NAT64 relay server using the same prefix
    `64:ff9b::/96`.
-   [TAYGA - NAT64 for Linux](http://www.litech.org/tayga/)
    a stateless {{< wp "NAT64" >}} implementation for Linux.
-   [jool](https://www.jool.mx/en/index.html)
    a statefull {{< wp "NAT64" >}} implementation for Linux.
-   [TNAT64](https://github.com/andrewshadura/tnat64) (GPL-2.0)
    is an interceptor which redirects outgoing TCPv4 connections through NAT64,
    thus enabling an application running on an IPv6-only host to communicate with the
    IPv4 world, even if that application does not support IPv6 at all.

## Ipv6 Tunnels
### 6to4 doc
You find both the name {{< wp "6to4" >}}, and {{< wp "6in4" >}}. {{< wp "6to4" >}} is the
Internet transition mechanism, it uses for the packet transport the
protocol {{< wp "6in4" >}}. BUt the two names are often used interchangeably.

-   [Quick and dirty IPv6 with 6to4
    ](http://backreference.org/2010/06/27/quick-and-dirty-ipv6-with-6to4/)
-   [Setting up 6to4 on Debian
    ](https://mithrandi.net/blog/2010/05/setting-up-6to4-on-debian/)
-   [ArchWiki: IPv6 - 6in4 Tunnel
    ](https://wiki.archlinux.org/index.php/IPv6_-_6in4_Tunnel)
-   [shorewall: 6to4 and 6in4 Tunnels](http://www.shorewall.net/6to4.htm) with a section
    on [Connecting two IPv6 Networks](http://www.shorewall.net/6to4.htm#Tunnel6to4).

### Tunnel Brokers
-   Wikipedia: {{< wp "Tunnel broker" >}}, {{< wp "List of IPv6 tunnel brokers" >}}
-   [Hurricane Electric Free IPv6 Tunnel Broker
    ](http://tunnelbroker.net/index.php)
-   [ArchWiki: IPv6 tunnel broker setup
    ](https://wiki.archlinux.org/index.php/IPv6_tunnel_broker_setup)
    gives Linux settings for Hurricane Electric tunnel
-   [SixXS](http://www.sixxs.net/main/) free  IPv6 Tunnel Broker,
    -   [aiccu](https://www.sixxs.net/tools/aiccu/)
        is a client that configures IPv6 connectivity without having
        to manually configure interfaces etc. Debian has an aiccu
        package.

### Tunnel Tools
-   [Miredo : Teredo for Linux and BSD](http://www.remlab.net/miredo/)
    used for terredo and packaged in Debian.

    The {{< wp "Teredo_tunneling" "Teredo IPv6 tunneling protocol" >}} encapsulates IPv6
    packets into UDP/IPv4 datagrams, to allow hosts behind NAT devices to access the
    IPv6 Internet.  Miredo can provide IPv6 connectivity to a dual-stack IPv6/IPv4. It
    can also operate as a Teredo relay which forwards IPv6 packets between the IPv6
    Internet and remote Teredo clients.

-   [BOSixNet](https://github.com/tehnick/bosixnet)
    – Build Own IPv6 Network. BOSixNet includes the collection of tools for automatic
    updating the list of your computers distributed through different networks and
    connected via NAT.  *bosixnet-webui* is the Debian package.

## IPV6 Testing and tools
-   [test-ipv6.com - Test your IPv6](https://test-ipv6.com/)
    Test your IPv6 connectivity. It is an ipv4 test client-side javascript.It sends a
    series of ajax requests are made from the web server, using various DNS names that
    force the use of IPv6 only.  It is also available in ipv6 at
    [ipv6.test-ipv6.belwue.net](http://ipv6.test-ipv6.belwue.net/) and other mirrors.
-   [www.ipv6.bieringer.de (native IPv6 only)](http://www.ipv6.bieringer.de/)
-   [ipv6calc](http://www.deepspace6.net/projects/ipv6calc.html)
    is an utility can convert between different formats of IPv4 or IPv6 addresses. It
    can also show information about the addresses, including who they are assigned to on
    the Internet.  _ipv6calc_ is packaged in debian.
-   [ipv6 calculator](http://www.ipv6calculator.net/) online javascript tool.
-   [Online TraceRoute IPv6
    ](http://www.subnetonline.com/pages/ipv6-network-tools/online-ipv6-traceroute.php)
-   [hackertarget.com: check your ports](http://hackertarget.com/port-check/)
-   [Online IPv6 Port Scanner](http://ipv6.chappell-family.com/ipv6tcptest/)
    allow to test from a text browser the standard or specified list of ports.
-   <a name="ipv6toolkit"></a>[SI6](https://www.si6networks.com/) -
    [IPv6 Toolkit](https://www.si6networks.com/research/tools/ipv6toolkit/).
    Networks' IPv6 Toolkit A security assessment and troubleshooting tool for the IPv6
    protocols. _ipv6toolkit_ is packaged in Debian.

    List of tools:

    -   addr6: An IPv6 address analysis and manipulation tool.
    -   flow6: A tool to perform a security asseessment of the IPv6 Flow Label.
    -   frag6: A tool to perform IPv6 fragmentation-based attacks and to perform a
        security assessment of a number of fragmentation-related aspects.
    -   icmp6: A tool to perform attacks based on ICMPv6 error messages.
    -   jumbo6: A tool to assess potential flaws in the handling of IPv6 Jumbograms.
    -   na6: A tool to send arbitrary Neighbor Advertisement messages.
    -   ni6: A tool to send arbitrary ICMPv6 Node Information messages, and assess
        possible flaws in the processing of such packets.
    -   ns6: A tool to send arbitrary Neighbor Solicitation messages.
    -   ra6: A tool to send arbitrary Router Advertisement messages.
    -   rd6: A tool to send arbitrary ICMPv6 Redirect messages.
    -   rs6: A tool to send arbitrary Router Solicitation messages.
    -   scan6: An IPv6 address scanning tool.
    -   tcp6: A tool to send arbitrary TCP segments and perform a variety of TCP-based
        attacks.

-   [thc-ipv6](https://github.com/vanhauser-thc/thc-ipv6) (AFFERO GPL)
    is an attack toolkit for testing IPv6 and ICMPv6 protocol weaknesses.

    List of tools:

    -   alive6: an effective alive scanning.
    -   denial6: try a collection of denial-of-service tests against a target.
    -   detect-new-ip6: detect new ip6 devices which join the network.
    -   dnsdict6: parallelized dns ipv6 dictionary bruteforcer.
    -   dos-new-ip6: detect new ip6 devices and tell them that their chosen IP collides
        on the network (DOS).
    -   exploit6: test known ipv6 vulnerabilities against a target.
    -   fake_mld6: announce yourself in a multicast group of your choice on the net.
    -   fake_router6: announce yourself as a router on the network.
    -   flood_advertise6: flood a target with random neighbor advertisements.
    -   flood_router6: flood a target with random router advertisements.
    -   implementation6: performs various implementation checks on ipv6.
    -   parasite6: icmp neighbor solitication/advertisement spoofer.
    -   redir6: redirect traffic to you intelligently (man-in-the-middle) with a clever
        icmp6 redirect spoofer.
    -   rsmurf6: remote smurfer (known to work only against Linux at the moment).
    -   thcping6: sends a hand crafted ping6 packet.

# IPv6 Address Scopes:

```example
::/128 unspecified address
::1/128 localhost
fe80::/10 link local
fc00::/7 unique local unicast  (RFC 4193)
fc00::/8 centrally assigned by unkown, routed within a site (RFC 4193)
fd00::/8 free for all, global ID must be generated randomly, routed within a site (RFC 4193)
ff00::/8 multicast, ff=4bits flags+4 bits scope
::ffff:0:0/96 IPv4 to IPv6 Address, eg: ::ffff:10.10.10.10 (RFC 4038)
2000::/3 global unicast
2001::/16 /32 subnets assigned to providers, they assign /48, /56 or /64 to the customer
2001:db8::/32 reserved for use in documentation
2001:678::/29 Provider Independent (PI) adresses and anycasting TLD nameservers
2002::/16 6to4 scope, 2002:c058:6301:: is the 6to4 public router anycast (RFC 3068)
```

-   {{< wp "Unique local address" >}} are non-globally reachable ip v6 addresses. They
    are routable only within the scope of private networks. ULAs are somewhat analogous
    to IPv4 private network.

    ULA locally assigned addresses use the prefix `fd00::/8`.

    By following the two bytes `fd` by ten arbitrary bytes (i.e 40 arbitrary bits) we
    obtain all the /48 prefixes. Within each prefix each of the following 4 bytes
    i.e. 16 bits gives 65536 `/64`subnets.

# Computing EUI-64
This is MAC Address based IPv6 Address used in
[Stateless address autoconfiguration (SLAAC)
](https://en.wikipedia.org/wiki/IPv6_address#Stateless_address_autoconfiguration)

To turn into a 64-bit EUI-64 address a MAC address follow the recipe:

-   Suppose your MAC address is 00:0c:29:0c:47:d5
-   insert FF:FE in the middle: 00:0c:29:ff:fe:0c:47:d5
-   Invert the the local link flag which is bit seven of the sixty four bit MAC. here it
    is the third bit of the second hexadecimal digit 0, which become 0010 or 2 in
    hexadecimal.  So the EUI64 suffix is 02:0c:29:ff:fe:0c:47:d5
-   If you use it in a link local address you obtain fe80::20c:29ff:fe0c:47d5/10 or if
    you use it in a 2001:db8:1:2::/64 network it yields the address
    2001:db8:1:2:20c:29ff:fe0c:47d5/64


If you want a tool to compute for you, use
[ipv6calc](http://www.deepspace6.net/projects/ipv6calc.html), like this:

    $ ipv6calc --in mac 00:0c:29:0c:47:d5 --out eui64
    20c:29ff:fe0c:47d5
    $ ipv6calc --in prefix+mac  fe80::/10 00:0c:29:0c:47:d5
    fe80::20c:29ff:fe0c:47d5/10
    $ ipv6calc --in prefix+mac 2001:db8:1:2::/64 00:0c:29:0c:47:d5
    2001:db8:1:2:20c:29ff:fe0c:47d5/64

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
