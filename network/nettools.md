---
title: Network Tools
---


See also {{< iref "IP" "IP protocols" >}},
{{< iref "network" "Network Security" >}}.

The monitoring tools are in the sections
{{< iref "monitoring#network_monitoring" "Network Monitoring Tools" >}} and
{{< iref "monitoring#system_monitoring" "System monitoring" >}}.

The network management utilities are in the
{{< iref "netconf" "Network Configuration Section" >}}.

# Ethernet tools

-   [Gentoo Wiki: Ethernet
    ](https://wiki.gentoo.org/wiki/Ethernet)
-   [Gentoo Wiki: Power_management/Ethernet
    ](https://wiki.gentoo.org/wiki/Power_management/Ethernet)

## Wake on lan {#wake_on_line}
{{< wp "Wake-on-LAN" >}} allows to switch on remote computers through special
network packets.


-   [ArchWiki: Wake on LAN
    ](https://wiki.archlinux.org/index.php/Wake-on-LAN)
-   The Gentoo [Wake on LAN HowTo
    ](http://www.gentoo-wiki.info/Wake_on_LAN)
    introduces the use of WOL.
-   [Debian wiki: Wake On LAN](http://wiki.debian.org/WakeOnLan)
    [Ubuntu Wiki - Wake On Lan
    ](https://help.ubuntu.com/community/WakeOnLan)
-   [Ubuntu-fr: Wake on lan](https://doc.ubuntu-fr.org/wakeonlan)

### Wake on lan tools

-   {{< man "etherwake" >}} or _ether-wake_ is a small c program written by David
    Becker, it is available as Debian package. There is a busybox version
    [busysbox ether-wake.c](https://git.busybox.net/busybox/plain/networking/ether-wake.c)
-   {{< man "wakeonlan" >}}
    is a perl script that uses UDP and does not require root privileges.
-   [gWakeOnLAN](http://www.muflone.com/jekyll/gwakeonlan/english/) (GPL)
    is a GTK+ application to Wake On LAN system, It is in Debian.
-   {{< man "ethtool(8)" >}} Display or change ethernet card settings, it is used to allow wake
    on lan on your internet card.


# IP Analysis and configuration tools. {#ip_tools}

-   {{< man "ip" >}} show and manipulate routing, devices, policy routing and
    tunnels see
    [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/index.html).
    The main reference is
    [ip-cref](http://student.ing-steen.se/IPv4/ip-cref.pdf) _pdf_,
    provided as a postscript file _ip-cref.ps_ in the package iproute2.
-   [Iproute2](http://linux-net.osdl.org/index.php/Iproute2) is a
    collection of utilites for controlling TCP / IP networking and
    Traffic Control in Linux. The commands are in the manual
    [ip(8)](http://man.cx/ip(8)), and in
    [Iproute2 Utility Suite Howto
    ](http://www.policyrouting.org/iproute2.doc.html),
-   [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/index.html)
    recall `ip` commands and gives also practical use cases of iproute2
    such GRE and ipv6 tunneling, IPSEC, multicast routing, combining
    with the netfilter marking to route packet depending of their
    characteristics, (re-)classifying packets, Building bridges, and
    pseudo-bridges with Proxy ARP, Dynamic routing - OSPF and BGP, and
    a cookbook for some specific cases.
-   [ping(8)](http://man.cx/ping(8)) send ICMP ECHO\\_REQUEST to
    network hosts.
-   [ifconfig(8)](http://man.cx/ifconfig(8)) configure a network
    interface
-   [ethtool(8)](http://man.cx/ethtool(8)) Display or change
    ethernet card settings
-   [nmap](http://nmap.org/) (GPL)
    is a network exploration tool and {{< wp "Port_scan"  "security     scanner" >}}. The man page is
    [nmap(1)](http://man.cx/nmap(1))
    There are GTK front ends `zenmap`, `nmapfe` or `xnmap`.
-   [tcpdump(1)](http://man.cx/tcpdump(1))
    dump traffic on a network
-   [dsniff](http://www.monkey.org/~dugsong/dsniff/)
    is a collection of tools for network auditing and penetration
    testing.
-   [sendip](http://www.earth.li/projectpurple/progs/sendip.html)
    is a commandline tool to allow sending arbitrary IP packets.
-   [arp(8)](http://man.cx/arp(8))
    manipulate the system ARP cache.
-   [ipvsadm](http://man.cx/ipvsadm)
    utility to administer the IP Virtual Server services
-   {{< man "arpwatch" >}} - keep track of ethernet/ip address pairings
-   [IpTraf](http://iptraf.seul.org/)
    ([iptraf(8)](http://man.cx/iptraf(8))) Interactive IP LAN Monitor.
    Refs: [Iptraf Manual](http://iptraf.seul.org/2.7/manual.html)
-   {{< wp "netstat"  "netstat (Wikipedia)" >}} Print network
    connections, routing tables, interface statistics, masquerade
    connections, and multicast memberships.
    [netstat(8)](http://man.cx/netstat(8))
-   {{< man "ss" >}} - r socket statistics is an alternative to netstat
-   {{< man "nethogs" >}} - Net top tool grouping bandwidth per process
-   <a name="authbind"></a>{{< wp "authbind" >}} (GPL)
    authbind allows the system administrator to permit specific users
    and groups access to bind to privileged TCP and UDP ports below
    1024. _authbind_ is in Debian.

    It has similar aim to
    {{< iref "#privbind" "privbind" >}} but this last one is a
    user space solution that need to be launched by root. Both
    override the bind() calls by a replacement library
    selected thanks to a `LD_PRELOAD` environment variable.


    We can also use the capability `CAP_NET_BIND_SERVICE` to allow a
    user program to bind to privileged ports.
    [Bind ports below 1024 without root on GNU/Linux
    ](http://www.wensley.org.uk/capabilities)
    for more informations.

    But _privbind_ Readme tell that that inheritance of capabilities
    has never been implemented so this solution is limited.

    <!-- more in the page
    [[file:filesystems_notes.md::#%20capabilities%20{#capabilities}][capabilities]] -->

-   <a name="privbind"></a>[privbind
    ](https://github.com/JiriHorky/privbind) (GPL)
    Privbind is a tool for running a command as an unprivileged user, with
    additional reserved port binding privileges.
    See also {{< iref "#authbind" "authbind" >}}.
    _privbind_ is in Debian.

## Tcpdump and Wireshark
[tcpdump](http://www.tcpdump.org/) dump traffic on a network

-   [tcpdump man page](http://www.tcpdump.org/tcpdump_man.html)
-   [tcpdump for Dummies
    ](http://www.alexonlinux.com/tcpdump-for-dummies)
    by Alexander Sandler.
-   [A tcpdump Tutorial and Primer
    ](http://danielmiessler.com/study/tcpdump/)
    by Daniel Miessler.
-   [Tcpdump filters (pdf)
    ](http://www.cs.ucr.edu/~marios/ethereal-tcpdump.pdf),
    by Marios Iliofotou.
-   [tcpdump cheat sheet
    ](http://packetlife.net/media/library/12/tcpdump.pdf)

{{< wp "Wireshark" >}} (GPL) is a tool to interactively browse network traffic.

-   [wireshark](http://www.wireshark.org/);
    [wireshark user guide
    ](http://www.wireshark.org/docs/wsug_html_chunked/),
    [wireshark man pages](http://www.wireshark.org/docs/man-pages/)
-   [Wireshark Wiki](http://wiki.wireshark.org/)
-   [wireshark-filter(4)
    ](http://www.wireshark.org/docs/man-pages/wireshark-filter.html)
    Wireshark filter syntax and reference.
-   [wireshark display filters cheat sheet
](http://packetlife.net/media/library/13/Wireshark_Display_Filters.pdf)
    see
    [tcpdump cheat sheet
    ](http://packetlife.net/media/library/12/tcpdump.pdf)
    for capture filters.
-   [tshark](http://www.wireshark.org/docs/man-pages/tshark.html)
    Dump and analyze network traffic in console
-   Remote captures can bee done using
    [captures from pipes
    ](http://wiki.wireshark.org/CaptureSetup/Pipes)
    An [example of remote capture
    ](http://blog.notreally.org/2007/01/24/how-to-monitor-packets-from-a-remote-interface/)
    in Jesús Roncero's blog.
-   A simple way to capture from an other host is:

        ssh root@host "/usr/sbin/tcpdump -w - -l -i eth1 not port 22" \\
        | wireshark -i - -k

-   We can also use a fifo as in
    [this article from Jason Antman's Blog
    ](http://blog.jasonantman.com/2011/04/using-wireshark-to-capture-packets-from-a-remote-host/)

## Traceroute

-   [traceroute(8)](http://man.cx/traceroute(8))
    _{{< wp "traceroute"  "Wikipedia: traceroute" >}}_ print the route
    packets take to network host using udp datagrams or ICMP with `-I`
    option.
-   [traceroute-nanog(8)](http://man.cx/traceroute-nanog(8))
    is an improved fork of traceroute including  AS  lookup,  TOS  support,
    microsecond timestamps,  path  MTU discovery, and parallel probing.
-   [nph-traceroute](http://www.demailly.com/~dl/nph-traceroute)
    (GPL) is a cgi script written in shell that provide a HTTP gateway to traceroute.
    It is available among the
    [Laurent Demailly WWW tools](http://www.demailly.com/~dl/wwwtools.html).
-   [traceroute.org](http://www.traceroute.org/) is a list _not always
    uptodate_ of web gateways to traceroute, classified by country.
-   [eu.org nph-traceroute](http://www.eu.org/cgi-bin/nph-traceroute)
    provides a trace route from Paris an gives a list of other locations in France.
-   [Geotrace](http://www.nabber.org/projects/geotrace/ "nabber.orggeotrace")
     provide a geographical  map of a traceroute path.
-   {{< wp "Tcptraceroute" >}} (GPL)
    [tcptraceroute(8)
    ](http://michael.toren.net/code/tcptraceroute/tcptraceroute.8.html)_
    is a  _traceroute_ implementation using TCP packets. By sending out
    TCP SYN packets instead of UDP or ICMP ECHO packets, tcptraceroute
    is able to bypass the most common firewall filters.
    -   [tcptraceroute(1)
        ](https://manpages.debian.org/stretch/tcptraceroute/tcptraceroute.1.en.html).
    -   [tcptraceroute Home
        ](http://michael.toren.net/code/tcptraceroute/)
        seems down there is a
        [GitHub Mirror](https://github.com/mct/tcptraceroute).
-   [tracepath(8)](http://man.cx/tracepath(8)) a not privileged
    program which sends UDP datagrams to trace path (and MTU) to a
    network host
-   [mtr(8)](http://man.cx/mtr(8)) combines _traceroute _and _ping_.

# TCP /UDP tools {#tcp_udp_tools}
## {{< wp " netcat" >}} {#netcat}
{{< wp " netcat" >}} is a C utility for reading from and writing to network
connections using TCP or UDP; The features from the original _nc110_
are:

-   Outbound or inbound (`-l`) connections, TCP or UDP (`-u`), to or
    from any ports.
-   Ability to broadcast UDP. (`-b`)
-   Full DNS forward/reverse checking, with appropriate warnings.
-   Ability to use any local source port.
-   Ability to use any locally-configured network source address.
-   Built-in port-scanning capabilities, with randomizer.
-   Built-in loose source-routing capability.
-   Can read command line arguments from standard input.
-   Slow-send mode, one line every N seconds. (`-i`)
-   Hex dump of transmitted and received data. (`-o`)
-   Optional ability to let another program service established
    connections.
-   Optional telnet-options responder. (`-t`)

These features are shared by all versions of netcat. Some details
differ.

### Different flavours of netcat

-   The _openbsd netcat_ allow to use ipv6 not the gnu or _nc110_;
-   The _openbsd netcat_ in listen mode `-l` can keep listening after
    its current connection is closed with `-k`, this option does not
    exist on _gnu netcat_ or _nc110_.
-   The _openbsd netcat_ can use UNIX-domain sockets with `-U`.
-   The _openbsd netcat_ can use a proxy (options `-P`, `-X`, `-x`)
-   The _openbsd netcat_ can use
    {{< wp "Datagram Congestion Control Protocol" >}} `-Z`.
-   _nc110_ and _gnu netcat_ provide `-c` and `-e` options to execute a
    command, this option does not exist in openbsd version. But
    you can still do this by a redirection as explained in
    [nc.openbsd manual](https://manned.org/nc.openbsd).
-   The _gnu netcat_ has a tunnel capability that you don't find
    elsewhere.
-   The _gnu netcat_ has some differences between options such as those
    mentionned in the [migration paper
    ](https://sourceforge.net/p/netcat/code/HEAD/tree/trunk/doc/migration).
    As it seems it is now less used than the two other versions, I
    don't explicit the details.

-   [nc110](http://nc110.sourceforge.net/) is the original netcat,
    free open source, but with an unclear license.<br/>
    The Debian package is _netcat-traditional_ and the canonical
    binary name is _nc_ on Debian it is _nc.traditional_ and can be
    linked to _nc_ and _netcat_ as an _alternative_.
    -   [netcat.traditional - nc(1)
        ](https://manpages.debian.org/unstable/netcat-traditional/nc.1.en.html)
-   [ gnu netcat ](http://netcat.sourceforge.net/) (GPL) is a rewrite of
    _nc110_. One goal of _gnu netcat_ was to have a full compatibility with
    netcat110 (which stopped developping in 1996) but the last
    release of gnu-netcat which date from 2004 is not completely
    compatible with _nc110_ (some details of differences in the
    [migration paper
    ](https://sourceforge.net/p/netcat/code/HEAD/tree/trunk/doc/migration)
    This program is not packaged by Debian.
-   [openbsd nc
    ](https://github.com/openbsd/src/tree/master/usr.bin/nc)
    (BSD License) is an improvement of _nc110_
    -   [nc.openbsd - nc(1)](https://manned.org/nc.openbsd) or in
        Debian manpages [nc.openbsd - nc(1)
        ](https://manpages.debian.org/unstable/netcat-openbsd/nc.1.en.html).

### Netcat documentation

-   The [manual of openbsd netcat
    ](https://manpages.debian.org/unstable/netcat-openbsd/nc.1.en.html)
    contains a detailled description an some simple examples.
-   The [wikipedia Netcat page](https://en.wikipedia.org/wiki/Netcat)
    contains many examples. _(but a note indicate the examples have to
    be moved elsewhere)_
-   For _nc110_ the manual [netcat.traditional - nc(1)
    ](https://manpages.debian.org/unstable/netcat-traditional/nc.1.en.html)
    is very succint, but it is because the core of the doc is in the big
    [nc110 README](http://nc110.sourceforge.net/) that is also
    installed with the _netcat.traditional_ package, this documentation
    contains a detailled description of all options and example with
    comprehensive comments. It is completed by the
    [script directory
    ](https://sourceforge.net/p/nc110/git/ci/master/tree/scripts/)
    that you find with  _netcat.traditional_ but not with the openbsd
    or the gnu version.
-   [Netcat for the Masses (pdf)
    ](http://www.infosecwriters.com/text_resources/pdf/Netcat_for_the_Masses_DDebeer.pdf)
    from Dean De Beer introduce in details many different uses
    of netcat.
-   The [nc introduction
    ](http://www.stearns.org/doc/nc-intro.current.html)
    by William Stearns focus on the usage as tcp server, and proxy.
-   Infosec institute [Netcat: TCP/IP Swiss Army Knife
    ](https://resources.infosecinstitute.com/netcat-tcpip-swiss-army-knife/)
-   [Hacking with Netcat part I
    ](https://www.hackingtutorials.org/networking/hacking-with-netcat-part-1-the-basics/),
    [part II
    ](https://www.hackingtutorials.org/networking/hacking-netcat-part-2-bind-reverse-shells/),
    [part III
    ](https://www.hackingtutorials.org/networking/hacking-with-netcat-part-3-advanced-techniques/).

## Other TCP/UDP tools
-   [ncat](https://nmap.org/ncat/) is an improved netcat from the nmap
    project. It support all _netcat_ features but add many features.

    Among the added features: chain Ncats together; redirection of
    TCP, UDP, and SCTP ports to other sites; SSL support; proxy
    connections (with optional proxy authentication) via SOCKS4 or
    HTTP proxies; ipv6 support; SCTP support; allows multiple hosts to
    connect to a centralized Ncat server and communicate with each
    other.

    Ncat is in the _nmap_ distribution, so if you have _nmap_ you
    should have _Ncat_ too.

    -   [ncat(1)
        ](https://manpages.debian.org/unstable/ncat/ncat.1.en.html).
    -   [Ncat User Guide](https://nmap.org/ncat/guide/index.html)

-   <a name="socat"></a>[socat](http://www.dest-unreach.org/socat/)
    is a command line based utility that establishes two bidirectional
    byte streams and transfers data between them.<br />
    A [vulnerability in the socat code
    ](http://www.dest-unreach.org/socat/contrib/socat-secadv7.html)
    affected Diffie-Helman encoding for socat 1.7.3.0 and 2.0.0-b8
    but it has been corrected in 1.7.3.1 and 2.0.0-b9.
    -   [socat(1)](http://www.dest-unreach.org/socat/doc/socat.html)
    -   [Examples from the manual
        ](http://www.dest-unreach.org/socat/doc/socat.html#EXAMPLES)
    -   [examples from the examples file
        ](https://raw.githubusercontent.com/craSH/socat/master/EXAMPLES)
    -   [Using socat as ssl-enabled Netcat
        ](http://lorgor.blogspot.com/2009/11/socat.html)
    -   [How to use git over an HTTP proxy, with socat
        ](http://gitolite.com/git-over-proxy.html)
-   [ucspi-tcp](http://cr.yp.to/ucspi-tcp.html)
    from [D. J. Bernstein site](http://cr.yp.to/djb.html),
    a tcp/ip toolbox that creates and accepts TCP connections.

# Traffic shaping {#traffic_shaping}
Some tools integrate bandwidth control as

    wget --limit-rate=10k
    curl --limit-rate 10k
    rsync --bwlimit=10.

-   [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/)
-   [Trickle](http://monkey.org/~marius/pages/?page=trickle)
    by Marius A. Eriksen allow traffic control when launching a process.
    _Trickle_ runs entirely in userspace
    -   [ArchWiki: Trickle](https://wiki.archlinux.org/index.php/Trickle)
    -   [Trickle: A Userland Bandwidth Shaper for Unix-like sytems
        ](http://monkey.org/~marius/trickle/trickle.pdf)
        by the _Trickle_ author.
    -   [Control your bandwidth with Trickle
        ](http://www.tuxradar.com/content/control-your-bandwidth-trickle)
-   [Wonder Shaper](http://lartc.org/wondershaper/)
    is a traffic shaping script.
-   [ip_relay](http://www.stewart.com.au/ip_relay/)
    is a perl user-space bandwidth shaping TCP proxy daemon. _named
    iprelay in Debian_.
-   [pyshaper](http://freenet.mcnabhosting.com/python/pyshaper/)
    is a python shaper script.
-   [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/)
    by Bert Hubert deals with iproute2, GRE, ipv6 tunneleing, IPSEC, multicast,
    queueing disciplines, netfilter packet marking/classifying,
    Kernel network parameters, proxyarp, OSPF and BGP.
-   [rfc 1256 ICMP Router Discovery Messages
    ](http://www.ietf.org/rfc/rfc1256.txt)
    describe the router discovery protocol, you can use
    as the command line utility {{< man "rdisc" >}}.
-   DNS service providers:
    [zoneedit.com](http://www.zoneedit.com/),
    [NoIP
    ](http://www.no-ip.com/services/managed_dns/free_dynamic_dns.html),
    [dyndns.org](//www.dyndns.org "dyndns.org"), or more generally the
    providers listed in the
    [Google directory list of dynamic DNS services
    ](http://www.google.com/Top/Computers/Software/Internet/Servers/Address_Management/Dynamic_DNS_Services/ "google directory Dynamic DNS Services")
    alias an IP address to a static hostname.
-   [rollernet.us](http://rollernet.us/) provides mail redirection
-   [ipcheck](http://ipcheck.sourceforge.net/)
    (python), and
    [DynIP](http://www.zikkurat.net/DynIP/) (sh),
    or
    [other clients](https://www.dyndns.org/services/dyndns/clients.html)
    are used to link the DHCP IP adress with the static hostname.
-   [GNU Zebra](http://www.zebra.org/) GPLed routing software
-   [Ports number list](http://www.iana.org/assignments/port-numbers)
    from
    [iana (internet assigned numbers authority)](http://www.iana.org/)
-   [GRC](http://www.grc.com/ "grc;com") Port Info Database:
-   [DSHIELD](https://secure.dshield.org/myisc.html)
    port/ip lookup/search:
-   [faq-modems-ppp](http://www.chez.com/epsylon2/modem.html) an old
    faq for an old technology!


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
