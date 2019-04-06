---
title: Firewall
---

{{% toc /%}}

See also {{< iref "IP" "IP" >}}

# References
-   Wikipedia: {{< wp "Comparison of firewalls" >}},
    {{< wp "List of router and firewall distributions" >}}
-   [firewall howto](http://www.tldp.org/HOWTO/Firewall-HOWTO.html)
    _2000_.
-   [FAQ: Firewall Forensics
    ](http://www.linuxsecurity.com/resource_files/firewalls/firewall-seen.html)
    explains what you see in firewall logs, especially what port
    numbers means _2000_.
-   [ArchWiki: Router](https://wiki.archlinux.org/index.php/Router).

# Firewall Software
-   [Alpine Wall (Awall)
    ](https://git.alpinelinux.org/cgit/awall/about/)
    is a Linux firewall configuration tool, using a set of json
    configuration files.
    -   [Zero-To-Awall
        ](https://wiki.alpinelinux.org/wiki/Zero-To-Awall)
        or _Awall_ for dummies.
    -   [How-To Alpine Wall
        ](https://wiki.alpinelinux.org/wiki/How-To_Alpine_Wall)
-   [Ubuntu Uncomplicated Firewall(ufw)
    ](https://wiki.ubuntu.com/UncomplicatedFirewall) has a gui:
    [gufw](http://gufw.org/) in Python-GTK. Both are in Debian.
    -   [Ubuntu Help - ufw
        ](https://help.ubuntu.com/community/UFW).
    -   [ufw manual
        ](http://manpages.ubuntu.com/manpages/bionic/en/man8/ufw.8.html).
    -   [ArchWiki - Uncomplicated Firewall
        ](https://wiki.archlinux.org/index.php/Uncomplicated_Firewall).
-   [Firewall Builder](http://fwbuilder.sourceforge.net/) (GPL)
    is a GUI firewall configuration and management tool that supports
    iptables (netfilter), ipfilter, pf, ipfw, Cisco.
    It is available in Debian and Ubuntu distributions.
    -   [GitHub - fwbuilder](https://github.com/fwbuilder/fwbuilder)
        clone of the SourceForge fwbuilder repostiory.
-   <a name="firehol"></a>{{< wp "FireHOL" >}} (GPL)
    is a Bash shell script designed as a wrapper for iptables.
    It uses a plain text configuration file. The companion script
    _FireQOS_ is used to set up traffic shaping.
    FireHol is in Debian.
    -   [FirHol Home](https://firehol.org/).
    -   [GitHub - FireHol](https://github.com/ktsaou/firehol).
    -   [ArchWiki - FireHol
        ](https://wiki.archlinux.org/index.php/Firehol).
    -   _FireHol_ also produce the
        {{< iref "monitoring#netdata" "netdata monitoring application" >}}.

# Firewall distributions {#firewall_distributions}
There are many Open Source Linux distributions that run as
replacement of original firmware of routers. They add to
the routing, firewall, dhcp basic software many features like
Bandwith Measurement, DNS forwarder (dns cache), DNS Server,
Dynamic DNS,
[IPv6](http://en.wikipedia.org/wiki/IPv6),
private
[Hotspot](http://en.wikipedia.org/wiki/Hotspot_%28Wi-Fi%29),
port fowarding, Network File System (nfs), Qos Bandwidth
Management, ssh client and server, Samba file sharing,
[socks proxy server](http://en.wikipedia.org/wiki/SOCKS),
{{< iref "streaming#upnp" "Upnp" >}},
{{< iref "vpn" "Virtual Private Networkss (VPN)" >}}
of different flavours (IPsec, OpenVpn, PPTP),
[Wireless Distribution System
](http://en.wikipedia.org/wiki/Wireless_Distribution_System),
[WDS Bridging
](http://www.dd-wrt.com/wiki/index.php/WDS_Linked_router_network#WDS_Bridging_without_Access_Point_Function),
[WPA](http://en.wikipedia.org/wiki/Wi-Fi_Protected_Access),
[WPA2](http://en.wikipedia.org/wiki/WPA2).

-   Wikipedia: {{< wp "Comparison of firewalls" >}},
    {{< wp "List of router and firewall distributions" >}}
-   [Hardware Firewall: Choosing the Right Firewall Distribution
    ](https://www.datamation.com/security/before-building-a-hardware-firewall.html)
    consider _PfSense_, _OPNSense_, _Untangle_, _Smoothwall Express_,

-   {{< wp "fli4l" >}} (GPL)
    acronym for __fl__exible __i__nternet router __for__ __l__inux
    is a Linux distribution for small   i386, x86-64. If can run from
    a SD card, or CDrom.
    -   [fli4l Home](http://www.fli4l.de/en/)
-   [ipcop](http://www.ipcop.org/) is a Linux firewall distribution
    that run on disk or compact-flash, download for i486 are provided.
    This is a fork of the old open source _Smoothwall_. The latest
    version is from _2015_ (seen in _2018_).
-   [ipfire](https://www.ipfire.org/)
    Is a firewall distribution with an advanced configuration tool.
    It runs on an  Intel Pentium I (i586), 512MB RAM and 2GB hard
    drive space, or [few arm platforms
    ](https://wiki.ipfire.org/hardware/arm/start) including
    LeMaker - BananaPi, and sinovoip - Bananapi M1.
-   [Milkfish
    ](http://wiki.milkfish.org.sipwerk.com/index.php?n=TheMilkfish.TheMilkfish)
    is a [project of VoIp
    ](http://wiki.milkfish.org.sipwerk.com/index.php?n=TheMilkfish.Idea) over
    over some brands of routers, it can be
    [added to dd-wrt
    ](http://wiki.milkfish.org.sipwerk.com/index.php?n=Milkfish-dd.RouterConfiguration)
    _MilkFish seems no more maintained since 2010._
-   {{< wp "OPNSense" >}} (BSD Licence)
    is a FreeBSD-based firewall and router.  It is a fork of
    {{< iref "#pfsense" "pfSense" >}}
    in 2015 when the later changed its license.
    {{< iref "#pfsense" "pfSense" >}} itself was forked from
    _m0n0wall_.  It is supported on i386 and amd64 and some arm
    platforms.
    -   [Opensense Home](https://opnsense.org/)

-   <a name="pfsense"></a>{{< wp "PfSense" >}} (Apache License)
    is a FreeBSD-based firewall and router based on
    {{< wp "FreeBSD" >}}.  It provides
    firewall, router, wireless access point, DHCP server, DNS server,
    and as a VPN endpoint. pfSense supports installation of
    third-party packages like Snort or Squid through its Package
    Manager.


     It is a fork of _m0n0wall_. It is now property of
     _Netgate_ that sell routers with PfSense pre-installed.

    -   [Pfsense Home](https://www.pfsense.org/).

-   [Smoothwall Express](http://www.smoothwall.org/) (GPL)
    GNU/Linux firewall distribution. It can run on almost any old PC,
    which becomes a dedicated firewall appliance.
    _The last release is in 2014_.
    (*The [smoothwall Inc. company](https://www.smoothwall.com/)
    also sell commercial versions of the smoothwall firewall*)



# Iptables {#iptables}
-   {{< wp "Netfilter"  "Wikipedia: Netfilter" >}}
-   [Netfilter](http://www.netfilter.org/)
    is a very maintained project as seen in the
    [Netfilter Git Repo](https://git.netfilter.org/)
    even if the documentation is quite old.
-   [netfilter documentation
        ](http://www.netfilter.org/documentation/index.html)
    :
    -   [IP Masquerade HOWTO
        ](http://www.tldp.org/HOWTO/IP-Masquerade-HOWTO.html)

        [
        [netfilter/iptables FAQ
        ](http://www.netfilter.org/documentation/FAQ/netfilter-faq.html)
    _2007_,
    -   [networking concept howto
        ](http://www.netfilter.org/documentation/HOWTO/networking-concepts-HOWTO.html)
        _2001_,
    -   [Netfilter Hacking HOWTO
        ](http://www.netfilter.org/documentation/HOWTO/netfilter-hacking-HOWTO.html)
        _2012_,
    -   [Nat Howto
        ](http://www.netfilter.org/documentation/HOWTO/NAT-HOWTO.html) _2202_,
    -   [Double Nat Howto
        ](http://www.netfilter.org/documentation/HOWTO/netfilter-double-nat-HOWTO.html),
    -   [Netfilter Extensions HOWTO
        ](http://www.netfilter.org/documentation/HOWTO/netfilter-extensions-HOWTO.html)
        _2005_
-   [ArchWiki: iptables
    ](https://wiki.archlinux.org/index.php/Iptables)
-   [ArchWiki: Simple stateful firewall
    ](https://wiki.archlinux.org/index.php/Simple_stateful_firewall)
    explains how to set up a stateful firewall using iptables.
-   [iptable tutorial](http://www.frozentux.net/iptables-tutorial/iptables-tutorial.html)
    by Oskar Andreasson provides a very complete guide, v 1.2.2 is
    dated november 2006, he wrote also a
    [sysctl tutorial
    ](http://www.frozentux.net/ipsysctl-tutorial/ipsysctl-tutorial.html)
    _2002_.
-   [Debian Wiki - Iptables](https://wiki.debian.org/iptables)
-   manual: {{< man "iptables" >}}
-   [piste](http://ipset.netfilter.org/)
    is a companion application for the iptables. It allows you to
    setup rules to quickly and easily block a set of IP addresses
    _ipset_ is in Debian.
    -   [ArchWiki - ipset](https://wiki.archlinux.org/index.php/Ipset).
-   [PeerGuardian Linux (pgl)
    ](https://sourceforge.net/projects/peerguardian/) (GPL)
    is an application to block connections to and from hosts in huge
    block lists.
    -   [ArchWiki - PeerGuardian
        ](https://wiki.archlinux.org/index.php/PeerGuardian_Linux).

# Nftable

_Nftables_ is the successor of _iptables_ first released in 2009. It
is also [developed by Netfilter
](https://netfilter.org/projects/nftables/index.html).
_Nftables_ replaces the existing _iptables_, _ip6tables_, _arptables_,
and _ebtables_ framework. It uses the Linux kernel and a new userspace
utility called _nft_.

-   [Nftables Wiki
    ](https://wiki.nftables.org/wiki-nftables/index.php/Main_Page)
    -   [Moving from iptables to nftables
        ](https://wiki.nftables.org/wiki-nftables/index.php/Moving_from_iptables_to_nftables).
-   [nft man page
    ](https://www.netfilter.org/projects/nftables/manpage.html)
-   [Wikipedia: Nftables](https://en.wikipedia.org/wiki/Nftables).xs
-   [Nftables quick howto
    ](https://home.regit.org/netfilter-en/nftables-quick-howto/).
-   [ArchWiki: Nftables
    ](https://wiki.archlinux.org/index.php/Nftables).
-   [Debian Wiki: Nftables
    ](https://wiki.debian.org/nftables).
-   [Gentoo Wiki: Nftables
    ](https://wiki.gentoo.org/wiki/Nftables).

#   Packet Filter
[Packet Filter (PF)](https://en.wikipedia.org/wiki/PF_(firewall))
is a  stateful packet filter, a central piece of software for
firewalling. It is comparable to iptables, {{< wp "ipfw" >}}, and
{{< wp "ipfilter" >}}. This is an OpenBSD project.



# Types of NAT

Full Cone NAT
:   A full cone NAT is one where all requests from the same internal IP
    address and port are mapped to the same external IP address and port.
    Furthermore, any external host can send a packet to the internal host,
    by sending a packet to the mapped external address.

Restricted Cone:
:   A restricted cone NAT is one where all requests from the same internal
    IP address and port are mapped to the same external IP address and port.
    Unlike a full cone NAT, an external host (with IP address X) can send a
    packet to the internal host only if the internal host had previously
    sent a packet to IP address X.

Port Restricted Cone
:   A port restricted cone NAT is like a restricted cone NAT, but the
    restriction includes port numbers.

    Specifically, an external host can send a packet, with source IP address
    X and source port P, to the internal host only if the internal host had
    previously sent a packet to IP address X and port P.

Symmetric Nat
:   A symmetric NAT is one where all requests from the same internal IP
    address and port, to a specific destination IP address and port, are
    mapped to the same external IP address and port. If the same host sends
    a packet with the same source address and port, but to a different
    destination, a different mapping is used. Furthermore, only the external
    host that receives a packet can send a UDP packet back to the internal
    host.

You can find out which one you are using by trying a stun client: e.g.:
[stun client and server](http://sourceforge.net/projects/stun/)


# Port knocking

Port knocking is a method of externally opening ports on a firewall by
generating a connection attempt on a set of prespecified closed ports.

-   [Wikipedia: Port knocking
    ](http://en.wikipedia.org/wiki/Port_knocking)
-   [ArchWiki: Port Knocking
    ](https://wiki.archlinux.org/index.php/Port_knocking).
    describe port knocking with iptable only and with the
    {{< iref "#knockd" "knockd" >}} daemon.

-   [portknocking.org](http://www.portknocking.org/)
    gives some documentation and list
    [implementations](http://www.portknocking.org/view/implementations)
    of port knocking. _Don't seem updated since 2010!_
-   [Port Knocking](http://www.linuxjournal.com/article/6811)
    By Martin Krzywinski _linux journal 2003_.
-   wknock project
    is similar to port knocking but applied to wifi lan. It is
    described in
    [Sécuriser un réseau wifi avec Wknock
    ](http://secuobs.com/news/20042005-securisation-reseau-wifi.shtml)
    and in this [Black Hat 2005 presentation
    ](http://blackhat.com/presentations/bh-europe-05/BH_EU_05-Oudot/BH_EU_05-Oudot.pdf)
    (pdf) _The project seems dead_.
-   <a name="knockd"></a>[Knockd
    ](http://www.zeroflux.org/projects/knock)
    is a simple port-knocking daemon.
    [How to safely connect from anywhere to your closed Linux firewall
    ](http://www.ducea.com/2006/07/05/how-to-safely-connect-from-anywhere-to-your-closed-linux-firewall/)
    is a tutorial to the use of knockd.
-   [Doorman](http://doorman.sourceforge.net/)
    port knocker daemon that watch for a single udp packet containing
    an md5 encoded identification. _No more developed since 2005._
-   [WebSpa](https://www.owasp.org/index.php/OWASP_WebSpa_Project)
    is a Java web knocking tool for sending a single HTTP/S
    request to your web server, in order to authorize the execution of
    a premeditated Operating System command on it.
    -   [WebSpa sourceforge project
        ](https://sourceforge.net/projects/webspa/)
    -   [GitHub - OWASP WebSpa](https://github.com/OWASP/WebSpa)

# Shorewall

[Shorewall](http://www.shorewall.net/)
is a high-level tool for configuring a Netfilter firewall.

-   [Shorewall Documentation
    ](http://www.shorewall.net/Documentation_Index.html)
-   [ArchWiki - Shorewall
    ](https://wiki.archlinux.org/index.php/Shorewall)
-   [shorewall manpage
    ](http://shorewall.net/manpages/shorewall.conf.html)

## shorewall configuration

To configure the first time, if you are new to shorewall look at the
shorewall doc (see below), then test your firewall's configuration
by running `shorewall check` and `shorewall start` (or `restart` )
this will ensure you configuration is syntactically correct. Run
your firewall with `shorewall start`, and check it is working ok.
then run `/etc/init.d/shorewall rebuild` to restart the firewall
saving the tables so that they may be restored on reboot. Last move
(or link) `/etc/init.d/shorewall` to `/etc/init.d/S45shorewall` To
allow shorewall to be launched at startup

When you upgrade from a previous version, your configuration is
moved to `/tmp/shorewall-backout` and you have to merge it with the
new configuration files in `/etc/shorewall`

## Shorewall logging

is explained in detail [shorewall.net doc: shorewall logging
](http://www.shorewall.net/shorewall_logging.html).

`ULOG` targets or `LOG` allow to choose between syslog and ulogd.
With `ulogd` package (11K pkg 27k jffs2) you can use a database, but
the commands of shorewall(-lite) use a log file, so you cannot drop
the logging to a file without dropping the shorewall
report capabilities.

You will use the ulogd module with ulogd\_LOGEMU.so used to log in a
file and available in the package ulogd-mod-extra (8k package,
27k jffs2)

You have to make sure that the log file stand where shorewall is
looking for it's messages. You have to put in your /etc/ulogd.conf:

    syslogfile /var/log/shorewall.log

If you opt for logging to a file, it is wise to add in your
`crontab` a command to rotate the log, because depending of your
rules and your traffic the log file can become huge.

`shorewall hits` that gives a very convenient statistics of hits in
shorewall log, classified by ip number and by port

To analyze the shorewall logs I use also
[fwlogwatch](http://fwlogwatch.inside-security.de/) for an offline
analysis of the logs

iptables by itself keeps an accounting of the network traffic that
cross every chain. It gives a very interesting image of your
firewall activity you display the traffic on a chain by
`shorewall show` *chain*.

I use very often `shorewall show blacklst` that allows me to check,
without logging them, which entries in my blacklist are still
active, and to delete those which are no longer used and

## Shorewall administration

The [Documentation of shorewall
](http://www.shorewall.net/Documentation_Index.html) references
all configuration options.

The administration of shorewall is described in
[starting and stopping page
](http://www.shorewall.net/starting_and_stopping_shorewall.htm)
which gives all commands. On openwrt `shorewall help` gives all
commands, and `shorewall help cmd` gives a summary of a
specific command.


## Shorewall IPV6
-   [Shorewall IPV6 support](http://shorewall.org/IPv6Support.html)
-   [Protecting your IPV6 world
    ](https://statusq.org/archives/2012/07/21/4297/) uses shorewall.


## prerequisites to run shorewall or shorewall-lite

For running shorewall on a light firewall like openwrt.

shell

:   shorewall ( lite or not ) suppose that printf, is available. new
    openwrt release have busybox compiled with `printf` but some older
    did not, and you must either upgrade busybox or replace it by an
    `awk printf`

:   `ip` is also prerequisite of `shorewall` a package is available. We
    can also use busybox with ip applet compiled in,but the `busybox ip`
    applet does not support `ip rule`, the commands `ip` {ldelim} `addr`
    | `route` | `link` {rdelim} `show` are supported but you cannot
    substitute `ls` to `show` as the busybox code does. So if you want
    to save some memory and use the `ip` applet from busybox you have to
    translate the ip commands.

iptables save/restore

:   `iptables save/restore` is available from iptables-utils package,
    you have to check your `iptables` version is the same than the one
    used by the `save/restore` program

    For a new firmware you can include it in your firmware build. If
    your firmware which does not provide them, and you don't want to
    build a new ipackage there are some workarounds.

    If you have a buildroot you can change `make/openwrt.mk` under the
    target `openwrt-prune`, you just comment the two lines

                # rm -f $(TARGET_DIR)/usr/sbin/iptables-save
                # rm -f $(TARGET_DIR)/usr/sbin/iptables-restore

    then you recompile and copy the two executables in `/usr/sbin`.

iptables kernel facilities

:   Depending upon your firewall rules, shorewall needs iptables
    capabilities compiled in the kernel or loaded as modules, these
    capabilities are in you kernel config as `CONFIG_IP_`... options:.
    We need at least `NETFILTER`(y), `IP_NF_CONNTRACK`(y different from
    `MATCH_CONTRACK`), `IP_NF_IRC`(y), `IP_NF_TFTP`(y), `IP_NF_FTP`(y),
    `IP_NF_IPTABLES`(y), `IP_NF_MATCH_LIMIT`(m `ipt_limit`),
    `IP_NF_MATCH_STATE`(y), `IP_NF_FILTER`(y),
    `IP_NF_MATCH_MULTIPORT`(y), `IP_NF_TARGET_REJECT`(y),
    `IP_NF_NAT`(y), `IP_NF_NAT_FTP`(y), `IP_NF_NAT_TFTP`(y),
    `IP_NF_NAT_IRC`(y), `IP_NF_TARGET_MASQUERADE`(y),
    `IP_NF_TARGET_REDIRECT`(y), `IP_NF_TARGET_LOG`(y), optionally
    `IP_NF_MATCH_STATE`(y), `IP_NF_MATCH_ECN` (m `ipt_ecn` used for
    Explicit Congestion Notification ) , `IP_NF_MATCH_TOS` (m `ipt_tos`,
    required for tos rules), `IP_NF_MATCH_MAC` (m `ipt_mac` required for
    [mac addresses control](http://shorewall.net/MAC_Validation.html)),
    `IP_MATCH_CONNTRACK` (m `ipt_conntrack`) \[ the module name can be
    misleading, it is not the obligatory connection tracking capability,
    but the elective matching on contrack\], `IP_NF_MATCH_IPRANGE` ( m
    `ipt_iprange` necessary if you want to use address range
    in shorewall&gt;2.1) `IP_NF_TARGET_ULOG` (m
    `ipt_ULOG`),IP\_NF\_MATCH\_PKTTYPE (m `ipt_pkttype` \[ used if
    `PKTTYPE=yes` in shorewall.conf\])

    The capabilities followed by a (y) are included in the standard
    kernel 2.4.30 (check your config), but the modules, even if they are
    compiled, are not included in the rom image.

iptables modules

:   If a module is not built in the kernel nor included in the firmare
    you need to load it from an ipackage file.

    `LOG`, `limit`, `owner`, `physdev` , `pkttype`, `recent` modules.
    :   They are divided in two packages:
        -   `iptables-mod-extra` provide the user spaces libraries:
            libipt\_recent.so, libipt\_limit.so, libipt\_physdev.so,
            libipt\_owner.so, libipt\_LOG.so, libipt\_pkttype.so.
        -   `kmod-ipt-extra` provides the kernel modules: ipt\_limit,
            ipt\_LOG, ipt\_owner, ipt\_physdev,
            ipt\_pkttype, ipt\_recent. It is loaded as dependency by
            `iptables-mod-extra`.

    `ulog`

    :   `ulog` is an alternative to log in shorewall files, it is better
        suited to shorewall because it allows to keep a separate log
        file for shorewall messages, it needs the **ulogd** daemon, and
        is explained below in {{< iref "#shorewall_logging" "Shorewall logging" >}}.

        The package `kmod-ipt-ulog` (4K pkg 6K jffs2) gives
        ipt\_ulog module. and the package `iptables-mod-ulog` (2.5 K
        package, 4K jffs2) the ipt\_ulog user space library

    When starting, shorewall-lite try to load the modules in
    `/usr/share/shorewall-lite/modules`, those who are not present are
    silently ignored. It used to produce some errors in the first
    releases iof shorewall qhen a rule use a capability present in the
    user space but not in the kernel. This option was silently ignored.
    If you include a limit field, even if `shorewall` find your rules
    correct, shorewall will fail because limit capability needs to load
    a module.

    Now in shorewall lite the capabilities of your kernel are checked by
    shorecap so it must no longer be an issue, but I recall that you
    must be careful to set properly the MODULESDIR as it is not standard
    in OpenWRT.

    The shorewall configuration is based on [this kernel
    configuration](http://shorewall.net/kernel.htm), which may be
    different from the standard openwrt one, usually some netfilter
    capabilities are built in the kernel in openwrt modules.

    if you never use a module you can just delete it in from
    `` /lib/modules/`uname -r` ``.

    Be warned that when shorewall try to use a module not loaded, as
    when you use a `limit` without `ipt_limit`, or a mac address without
    `ipt_mac`, shorewall fail with a meaningless message and restore
    your previous configuration, only when running shorewall with
    `debug` you can see a message from iptables, and even there not
    so clear. As a rule of thumb I advise you to load at least
    `ipt_limit` and `ipt_mac`


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
