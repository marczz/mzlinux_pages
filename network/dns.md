---
title: Data Name Server
---


# References
-   [Domain Name System from Wikipedia
    ](http://en.wikipedia.org/wiki/Domain_Name_System)
    (available also in
    [french](http://fr.wikipedia.org/wiki/Domain_Name_System)) explains
    the basis of DNS and provide a lot of links including links to the
    RFCs
-   Wikipedia: {{< wp "Category:Domain name system" >}},  {{< wp "BIND" >}},
    {{< wp "Dynamic DNS" >}}, {{< wp "Comparison of DNS server software" >}},
    {{< wp "Category:DNS server software for Linux" >}}.
-   The two main RFC are
    [RFC 1034](http://tools.ietf.org/html/rfc1034)
    Domain Names - Concepts and Facilities and
    [RFC 1035](http://tools.ietf.org/html/rfc1035)
    Domain Names - Implementation and Specification
-   Fedora documentation: [NameResolution
    ](https://fedoraproject.org/wiki/Networking/NameResolution),
    [DNSSEC
    ](https://fedoraproject.org/wiki/Networking/NameResolution/DNSSEC).
-   [Archwiki: Domain name resolution
    ](https://wiki.archlinux.org/index.php/Domain_name_resolution).
-   [ZoneEdit Web DNS lookup](http://www.zoneedit.com/lookup.html).
-   {{< wp "OpenDNS" >}} is a free DNS  resolution service that offers phishing
    protection. [OpenDNS Home](http://www.opendns.com/)
-   Daniel J. Bernstein [djbdns](http://cr.yp.to/djbdns.html),
    [Wikipedia page](http://en.wikipedia.org/wiki/Djbdns)
-   the use of the SRV record (
    [rfc 2782](http://tools.ietf.org/html/rfc2782)) for voip is
    detailled in
    [DNS SRV at voip-info.org](http://www.voip-info.org/wiki/view/DNS+SRV "voip-info.org: DNS+SRV")

## Zeroconf

[Zeroconf](http://en.wikipedia.org/wiki/Zeroconf)
allows automatic address selection
([rfc 3927](http://tools.ietf.org/html/rfc3927),
[rfc 2462](http://tools.ietf.org/html/rfc2462)
for ipV6), name resolution by multicast DNS *mDNS*
([rfc 4795](http://tools.ietf.org/html/rfc4795)
Link-Local Multicast Name Resolution (LLMNR)) , and DNS based
Service Discovery (DNS-SD)(
[rfc2782](http://tools.ietf.org/html/rfc2782))
also implemented in the Service Location Protocol (SLP) (
[rfc 2608](http://tools.ietf.org/html/rfc2608)
and
[rfc 3224](http://tools.ietf.org/html/rfc3224)).

-   Wikipedia: {{< wp "[Zeroconf" >}}, {{< wp "Avahi_software)"  "Avahi" >}},
    {{< wp "Multicast DNS" >}} (mDNS),
-   [zeroconf.org: Zero Configuration Networking
    ](http://www.zeroconf.org/).
-   The Zeroconf model is implemented in the
    [Apple Bonjour *(Wikipedia)*
    ](http://en.wikipedia.org/wiki/Bonjour_%28software%29)
    *(apache license 2.0)* which is also available in linux and
    windoze; and
    [Avahi *(Wikipedia)*
    ](http://en.wikipedia.org/wiki/Avahi_%28software%29)
    *(LGPL)*
-   Avahi ([Avahi Home page](http://avahi.org/)
    uses D-Bus for communication between user applications and a system
    daemon.
-   [Arch Wiki: Avahi](https://wiki.archlinux.org/index.php/Avahi)
-   [Debian Wiki: Zeroconf](https://wiki.debian.org/ZeroConf) gives
    the current support of avahi by softwares.

# DNS Tools
-   Wikipedia: {{< wp "Category:DNS software" >}}, {{< wp "Dig_(command)"  "Dig" >}}
-   [DIG HowTo](http://www.madboa.com/geek/dig/) by Paul Heinlein.
-   [host (1) manual](ftp://ftp.isc.org/isc/bind9/9.11.1/doc/arm/man.host.html)
-   {{< wp "Whois" >}} allows to determine the owner of a domain name or an IP address.
    You can learn about whois in the {{< wp "Whois"  "whois Wikipedia page" >}} or in the
    [whois overview](http://navigators.com/whois.html "navigators.com whois.html")
    and query it thru the commandline
    [whois(1)](http://man.cx/whois) or a web gateway such as
    [geektools whois gateway](http://www.geektools.com/whois.php)
-   [DNSd](https://github.com/behrooza/dnsd) is a daemon that provides
    a local DNS backend to forward the queries/answers to/from
    {{< wp "Google Public DNS" >}} over
    HTTPS.


# Useful Registrars

-   [Archwiki: Alternative DNS servers
    ](https://wiki.archlinux.org/index.php/Resolv.conf#Alternative_DNS_servers).
-    Google provide free dns at `8.8.8.8` and `8.8.4.4`.
-   [internic](http://www.internic.net/) has a list of registrars
-   registrar: <https://www.gandi.net/>
-   [zoneedit.com](http://zoneedit.com/) *have had* free DNS.
-   DNS service providers:
    [zoneedit.com](http://www.zoneedit.com/),
    [NoIP](http://www.no-ip.com/services/managed_dns/free_dynamic_dns.html),
    [dyndns.org](//www.dyndns.org), [DynIP](https://www.dynip.com/),
    [Dyn](https://help.dyn.com/)
    alias an IP address to a static hostname.
-   Dyn [Remote Access Update API
    ](https://help.dyn.com/remote-access-api/) and
    [CheckIP Tool
    ](https://help.dyn.com/remote-access-api/checkip-tool/)
-   [ipcheck](http://ipcheck.sourceforge.net/)
    (python),  [ddclient](https://help.dyn.com/ddclient/) and
    [other clients](https://www.dyndns.org/services/dyndns/clients.html)
    are used to link the DHCP IP adress with the static hostname.
-   [dyndns](http://www.dyndns.com/) was previously
    free.  Now dyn is 25$/year. See also
    [dyndns Developers’ Connection](https://dyn.com/developers).<br />
-   [no.ip](http://www.noip.com/) offer [free dyndns for 3 hostnames
    ](http://www.noip.com/remote-access).
    -   [Dynamic DNS with No-IP on Debian tutorial
        ](http://www.ducky-pond.com/posts/2012/Jul/dynamic-dns-with-no-ip-on-debian/)
    -   [How to use ddclient with No-IP
        ](http://www.ducky-pond.com/posts/2014/Feb/how-to-use-ddclient-with-no-ip/)
-   [ddclient](http://sourceforge.net/p/ddclient/wiki/Home/)
    is a Perl client used to update dynamic DNS entries.
-   [NameCheap](https://www.namecheap.com/) is cheap!  €8,44/year for
    an *org* domain,  €6,24/year for *us*,  €7,04/year for *eu*,
    €4,33/year for *org.uk* or *me.uk*, €6,89/year for *fr*
    -   [How to use ddclient with Namecheap
        ](http://www.ducky-pond.com/posts/2014/Feb/how-to-use-ddclient-with-namecheap/).
-   {{< iref "web_servers" "Polipo" >}} does not use
    `gethostbyname` but use its own resolve code, and it does not look at
    `/etc/hosts`, so we have to disable polypo for the domains where we
    want to use `/etc/hosts` or use the dns cache itself.

# Systemd-resolved
systemd-resolved is a system service that provides network name resolution to local
applications via a D-Bus interface. It implements a caching and validating DNS/DNSSEC
stub resolver, as well as an LLMNR and MulticastDNS resolver and responder.
-   [systemd-resolved.service - Freedesktop Manual
    ](https://www.freedesktop.org/software/systemd/man/systemd-resolved.service.html)
-   [systemd-resolved - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-resolved)

# Unbound
[unbound](https://unbound.net/) (BSD license) is a validating,
recursive, and caching DNS resolver. Along {{< wp "Unbound (DNS server)"  "Wikipedia" >}}
> Unbound has supplanted the Berkeley Internet
> Name Daemon (BIND) as the default, base-system name server in several
> open source projects, where it is perceived as smaller, more modern,
>  and more secure for most applications.

Unbound is packaged in Debian.

-   Wikipedia: {{< wp "Unbound (DNS server)"  "unbound" >}}
-   [ArchWiki: unbound](https://wiki.archlinux.org/index.php/Unbound).

# Bind
-   Wikipedia: {{< wp "BIND" >}}
-   Paul Vixie Bind
    [Internet Systems Consortium official Page](http://www.isc.org/index.pl?/sw/bind/)
    and
    [Bind Wikipedia page](http://en.wikipedia.org/wiki/BIND "en.wikipedia.org BIND")
-   [BIND 9 Administrator Reference Manual](http://www.bind9.net/manual/bind/9.3.3/Bv9ARM.html)
-   [DNS HOWTO](http://www.langfeldt.net/DNS-HOWTO/BIND-9/)
    by Nicolai Langfeldt is a guide to _Bind_, dated _2008 but still very useful.
-   [DNS for Rocket Scientists](http://www.zytrax.com/books/dns/)
    is a DNS and Bind9 complete guide.


# Dnsmasq {#dnsmask}

DNSMASQ (GPL) is a a lightweight tftp, DHCP and caching DNS server.

As DNS cache dnsmasq accepts DNS queries and either answers them from a
small, local, cache or forwards them to a real, recursive, DNS server.

Dnsmasq is also a dhcpd server. It supports static address assignments,
multiple networks, Bootp and vendor-encapsulated options, DHCP-relay and
RFC3011 subnet specifiers.

-   Wikipedia: {{< wp "dnsmasq" >}}
-   [Dnsmasq Home page documentation](http://thekelleys.org.uk/dnsmasq/doc.html)
-   [Dnsmasq FAQ](http://thekelleys.org.uk/dnsmasq/docs/FAQ)
-   [Dnsmasq french tutorial](http://www.drazzib.com/docs-dnsmasq.html)
-   [ArchWiki: Dnsmasq](https://wiki.archlinux.org/index.php/Dnsmasq)
-   [extensive example of configuration file for dnsmasq
    ](http://thekelleys.org.uk/dnsmasq/docs/dnsmasq.conf.example)
    You find there some otherwise *secret options* as how to configure
    your server for a bootp relay.
-   Man pages: [dnsmasq.8](http://thekelleys.org.uk/dnsmasq/docs/dnsmasq-man.html),
    and [dnsmasq setup](http://thekelleys.org.uk/dnsmasq/docs/setup.html), from
    the dnsmasq distribution.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
