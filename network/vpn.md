---
title: VPN and Tunneling
---

{{% toc /%}}

# References
-   Wikipedia: {{< wp "IP tunnel" >}}, {{< wp "Tunneling protocol" >}}, {{< wp "HTTP tunnel" >}}
    {{< wp "Point-to-Point Tunneling Protocol" >}} (PPTP),
    {{< wp "Hole punching (networking)" >}}, {{< wp "ICMP hole punching" >}},
    {{< wp "TCP hole punching" >}}, {{< wp "UDP hole punching" >}}, {{< wp "Stunnel" >}},
    {{< wp "OpenVPN" >}}, {{< wp "SoftEther VPN" >}}, {{< wp "IPsec" >}},
    {{< wp "Layer 2 Tunneling Protocol" >}}, {{< wp "OpenConnect" >}},
    {{< wp "Secure Socket Tunneling Protocol" >}} (SSTP),
-   [VPN HOWTO](http://www.tldp.org/HOWTO/VPN-HOWTO.html) _2002_
-   [VPN Masquerading HOWTO
    ](http://www.tldp.org/HOWTO/VPN-Masquerade-HOWTO.html) _2000_.
-   [ip in ip tunneling](http://lartc.org/howto/lartc.tunnel.ip-ip.html) _in
-   [Linux Advanced Routing & Traffic Control HOWTO
    ](http://lartc.org/howto/) _2012_ has chapters on _ip in ip
    tunneling_, _GRE Tunneling_, _IPv6 Tunneling_, _IPSEC_

-   [Linux IP Tunnel Mini-Mini HOWTO](http://linas.org/linux/iptunnel.html)
-   [GRE tunneling](http://lartc.org/howto/lartc.tunnel.gre.html) _in
    [Linux Advanced Routing & Traffic Control HOWTO](http://lartc.org/howto/)_.
-   [tinc](http://www.tinc-vpn.org/) a Virtual Private Network (VPN)
    daemon that uses tunnelling and encryption.
-   [VTun - Virtual Tunnels over TCP/IP networks
    ](http://vtun.sourceforge.net/) _2012_.
-   [The official IPsec Howto for Linux
    ](http://www.ipsec-howto.org/) 2006
-   [ipsec tools](http://ipsec-tools.sourceforge.net/) _2011_
-   [udpproxy](https://github.com/vincentbernat/udpproxy)
    is a Netfilter powered UDP proxy.  udpproxy allows to tunnel UDP
    datagrams into a SSH tunnel with the help of NFQUEUE target from
    Netfilter. This enables easy selection of flow to be tunneled.
-   {{< iref "ssh" "ssh" >}} allow socks and tun.
-   [sshuttle](https://github.com/sshuttle/sshuttle) (GPL)
    from Avery Pennarun creates a transparent proxy server, using
    iptables, that will forward all the traffic through an SSH tunnel
    to a remote copy of sshuttle.  It does not require installation on
    the remote server, which just needs to have python installed.
    _sshuttle is in Debian._
    -   [sshuttle documentation](https://sshuttle.readthedocs.org/).


# Openvpn {#openvpn}
[OpenVPN](http://openvpn.net/) (GPL) is a SSL VPN. It uses SSL/TLS
protocol, supports flexible client authentication methods based on
certificates, smart cards, and/or 2-factor authentication.
There are clients for Linux and other Unixes, Windoze, Mac OS, IoS,
and Android

-   Wikipedia: {{< wp "OpenVPN" >}}.
-   [OpenVPN Home](http://openvpn.net/)
-   [OPenVPN](http://openvpn.sourceforge.net/),
-   [OpenVPN Documentation Page
    ](https://openvpn.net/index.php/open-source/documentation.html)
    has an extensive documentation.
-   [OpenVpn Wiki](https://community.openvpn.net/openvpn/wiki)
-   [OpenVPN HOW-TO](http://openvpn.net/index.php/documentation/howto.html)
    and [OpenVPN 2.3 man page
    ](https://community.openvpn.net/openvpn/wiki/Openvpn23ManPage)
    are the most usefull in admin tasks once you have understood the
    general principles of operations.
-   [OpenVPN sample configuration files
    ](https://openvpn.net/index.php/open-source/documentation/howto.html#examples)
    is the best starting point for your own configuration.  after installing openvpn in
    Linux. You can also find them in the directory `/usr/share/doc/openvpn/examples`.
-   [ArchWiki - OpenVPN](https://wiki.archlinux.org/index.php/OpenVPN).
-   [Debian Wiki - OpenVPN](http://wiki.debian.org/OpenVPN)
-   [Fedora Wiki - OpenVPN](http://fedoraproject/wiki/Openvpn).
-   [Gentoo Wiki - OpenVPN](https://wiki.gentoo.org/wiki/OpenVPN)
-   [configuring shorewall for OpenVPN](http://www.shorewall.net/OPENVPN.html)
    [Private Tunnel VPN for Android
    ](https://play.google.com/store/apps/details?id=net.openvpn.privatetunnel).
    is an Android client.
-   [Install and configure OpenVPN
    ](https://www.supinfo.com/articles/single/6908-install-and-configure-openvpn)
    a tutorial by  Baptiste Nowicki.

# SoftEther VPN
{{< wp "SoftEther VPN" >}} (GPL) is a cross-platform, multi-protocol VPN client
and VPN server software. It supports  SSL VPN, {{< wp "L2TP" >}}/{{< wp "IPsec" >}},
{{< iref "#openvpn" "OpenVPN" >}},
and Microsoft {{< wp "Secure Socket Tunneling Protocol" >}}.

-   [SoftEther VPN Project](https://www.softether.org/).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
