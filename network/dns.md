---
title: Domain Name Server
---

<!--
[[file:../../../../content-org/notes/network_notes/dns_notes.org][DNS notes]]
-->
The network configuration guides are in the page
{{< iref "network" "Network references"  >}}.
See also {{< iref "netconf" "Network configuration" >}}, {{< iref "vpn" "VPN" >}}.


# References
-   [Domain Name System from Wikipedia](http://en.wikipedia.org/wiki/Domain_Name_System)
    (available also in
    [french](http://fr.wikipedia.org/wiki/Domain_Name_System)) explains
    the basis of DNS and provides a lot of links including links to the
    RFCs
-   Wikipedia: {{< wp "Category:Domain name system" >}},  {{< wp "BIND" >}},
    {{< wp "Dynamic DNS" >}}, {{< wp "Comparison of DNS server software" >}},
    {{< wp "Category:DNS server software for Linux" >}}.
-   The two main DNS RFC are
    [RFC 1034](http://tools.ietf.org/html/rfc1034)
    Domain Names - Concepts and Facilities and
    [RFC 1035](http://tools.ietf.org/html/rfc1035)
    Domain Names - Implementation and Specification
-   [DNS over TLS](https://en.wikipedia.org/wiki/DNS_over_TLS "wikipedia:DNS over TLS")
    ([RFC 7858](https://tools.ietf.org/html/rfc7858 "rfc:7858")),
-   [DNS over HTTPS](https://en.wikipedia.org/wiki/DNS_over_HTTPS "wikipedia:DNS over HTTPS")
    ([RFC 8484](https://tools.ietf.org/html/rfc8484 "rfc:8484")), or
-   [DNSCrypt](https://en.wikipedia.org/wiki/DNSCrypt "wikipedia:DNSCrypt").
-   [DNSSEC
    ](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions "wikipedia:Domain Name System Security Extensions")
    is a set of extensions to DNS which provide to DNS clients (resolvers) origin
    authentication of DNS data, authenticated denial of existence, and data integrity,
    but not availability or confidentiality.
    -   [DNSSEC - ArchWiki](https://wiki.archlinux.org/title/DNSSEC)
    -   [DNSSEC - Fedoraproject](https://fedoraproject.org/wiki/Networking/NameResolution/DNSSEC).
-   [ZoneEdit Web DNS lookup](http://www.zoneedit.com/lookup.html).
-   {{< wp "OpenDNS" >}} is a free DNS  resolution service that offers phishing
    protection. [OpenDNS Home](http://www.opendns.com/)
-   Daniel J. Bernstein [djbdns](http://cr.yp.to/djbdns.html),
    [Wikipedia page](http://en.wikipedia.org/wiki/Djbdns)
-   the use of the SRV record (
    [rfc 2782](http://tools.ietf.org/html/rfc2782)) for voip is detailled in
    [DNS SRV at voip-info.org](http://www.voip-info.org/wiki/view/DNS+SRV)
-   {{< iref "web_servers" "Polipo" >}} does not use
    `gethostbyname` but use its own resolve code, and it does not look at
    `/etc/hosts`, so we have to disable polypo for the domains where we
    want to use `/etc/hosts` or use the dns cache itself.

# Zeroconf {#zeroconf}
<a name="avahi"></a>
<!--
[[file:../../../../content-org/notes/network_notes/dns_notes.org::#avahi][Avahi notes]]
-->

[Zeroconf](http://en.wikipedia.org/wiki/Zeroconf) allows automatic address selection
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

-   Wikipedia: {{< wp "Zeroconf" >}}, {{< wp "Avahi_software)"  "Avahi" >}},
    {{< wp "Multicast DNS" >}} (mDNS), {{< wp "LLMNR" >}}.
-   [zeroconf.org: Zero Configuration Networking](http://www.zeroconf.org/).
-   The Zeroconf model is implemented in the
    [Apple Bonjour *(Wikipedia)*](http://en.wikipedia.org/wiki/Bonjour_%28software%29)
    *(apache license 2.0)* which is also available in linux and
    windoze; and
    [Avahi *(Wikipedia)*](http://en.wikipedia.org/wiki/Avahi_%28software%29) *(LGPL)*,
    {{< iref "#systemd-resolved" "Systemd-Resolved" >}} also implements both mDNS and
    LLMNR.

    {{< wp "LLMNR" >}} is a windows protocol that Microsoft is phasing out, as well than
    {{< wp "NetBIOS" >}} since 2022, in  favour of {{< wp "Multicast DNS" "mDNS">}}.

-   Avahi ([Avahi Home page](http://avahi.org/))
    uses D-Bus for communication between user applications and a system daemon.
-   [Arch Wiki: Avahi](https://wiki.archlinux.org/index.php/Avahi)
-   [Debian Wiki: Zeroconf](https://wiki.debian.org/ZeroConf)
    gives the current support of avahi by software.

# DNS Tools
-   Wikipedia: {{< wp "Category:DNS software" >}}, {{< wp "Dig_(command)"  "Dig" >}}.
-   [Bind](hpttps://www.isc.org/downloads/bind/) in the *bind-dnsutils* package includes
    dns lookup utilities: {{< man "nslookup(1)" >}}, {{< man "dig(1)" >}} and in the
    *bind-host* package the {{< man "host(1)" >}} utility.
-   [DIG HowTo](http://www.madboa.com/geek/dig/) by Paul Heinlein.
-   [LDNS](https://www.nlnetlabs.nl/projects/ldns/) library provides utilities in the package
    *ldnsutils*, which includes {{< man "drill(1)" >}} a dig like dns lookup utility.
-   {{< wp "Whois" >}} allows to determine the owner of a domain name or an IP address.
    You can learn about whois in the {{< wp "Whois"  "whois Wikipedia page" >}} or in the
    [whois overview](http://navigators.com/whois.html)
    and query it thru the command line
    [whois(1)](http://man.cx/whois) or a web gateway such as
    [ICANN Lookup](https://lookup.icann.org/en).
-   [DNSd](https://github.com/behrooza/dnsd) is a daemon that provides a local DNS
    backend to forward the queries/answers to/from {{< wp "Google Public DNS" >}} over
    HTTPS.

## DNS performances
-   [dnsperf](https://github.com/DNS-OARC/dnsperf) (Apache2 License)
    is a DNS Performance Testing Tools, it reports latency and throughput metrics for
    Domain Name Service, the companion application resperf systematically increases the
    query rate and monitors the response rate to simulate caching DNS services.
    [![packaging](https://repology.org/badge/tiny-repos/dnsperf.svg?header=packages)
    ](https://repology.org/project/dnsperf/versions).
-   [dnsperftest - GitHub](https://github.com/cleanbrowsing/dnsperftest) (GPL 3.0)
    Shell script to test the performance of the most popular DNS resolvers from your
    location.

    There is a predefined list of popular providers, but it is easy to add your
    preferred one.
-   [DNS Performance  - DNSPerf](https://www.dnsperf.com/)
    is a site that provide measures of DNS performance and uptime.
    -   [Benchmark your DNS provider with DNSPerfi
        ](https://www.dnsperf.com/dns-speed-benchmark/)
-  [DNS-OARC](https://www.dns-oarc.net/)
   The DNS Operations, Analysis, and Research Center.

   It provides many [online services](https://www.dns-oarc.net/index.php/oarc/services).
-  [DNS-OARC: Check My DNS](https://cmdns.dev.dns-oarc.net/)
   is an online service to analyze how you use DNS as a client by testing your
   configured resolvers using your browser and special crafted domain names.
-  [OARC's DNS Privacy Resolver
   ](https://www.dns-oarc.net/index.php/oarc/services/dnsprivacy)
   is a dual-stack (IPv4 and IPv6), open DNS Privacy resolvers that anyone can use to
   experiment with secured DNS over TLS services

   `tls-dns-u.odvr.dns-oarc.net` is available at `184.105.193.78` and
   `2620:ff:c000:0:1::64:25`.

#  DNS Servers

The DNS query may imply many [Security and Privacy risks
](https://wiki.archlinux.org/title/Domain_name_resolution#Privacy_and_security).
So we may want to use DNS over TLS, DNS over HTTPS, or DNSCrypt.

-   [Public recursive name server - Wikipedia
    ](https://en.wikipedia.org/wiki/Public_recursive_name_server#List_of_public_DNS_service_operators)
    a list which includes the security and privacy options offered by the servers.

    It includes providers which implement a filter against adds, trackers, malwares.
-   [Archwiki list of DNS servers
    ](https://wiki.archlinux.org/title/Domain_name_resolution#DNS_servers) .
-   [Archwiki: Alternative DNS servers
    ](https://wiki.archlinux.org/index.php/Resolv.conf#Alternative_DNS_servers).
-   Google provide free dns at `8.8.8.8` and `8.8.4.4`, it support IPV6 and delete IP
    information after 24h.

# Dynamic DNS
-   [Dyn](https://help.dyn.com/) is a commercial service to
    alias an IP address to a static hostname. It is priced in 2024 55$/year
    -   Dyn [Remote Access Update API](https://help.dyn.com/remote-access-api/)
    -  [CheckIP Tool](https://help.dyn.com/remote-access-api/checkip-tool/)
-   [ipcheck](http://ipcheck.sourceforge.net/)
    is an obsolete *2013* python script,
    [ddclient](https://help.dyn.com/ddclient/) perl script,
    are used to link the DHCP IP adress with the static hostname.
-   [no.ip](http://www.noip.com/) offer [free dyndns for one hostname
    ](http://www.noip.com/remote-access), and 5 hostnames for 48$/year *2024*.


# Registrars
-   [internic](http://www.internic.net/) has a list of registrars
-   [NameCheap](https://www.namecheap.com/)
    -   [How to use ddclient with Namecheap
        ](http://www.ducky-pond.com/posts/2014/Feb/how-to+-use-ddclient-with-namecheap/).
-   [Domain name - Gandi.net](https://www.gandi.net/en-US/domain)
-   DNS service providers:
    [zoneedit.com](http://www.zoneedit.com/),

# Unbound {#unbound}
[unbound](https://unbound.net/) (BSD license) is a validating,
recursive, and caching DNS resolver. Along {{< wp "Unbound (DNS server)"  "Wikipedia" >}}
> Unbound has supplanted the Berkeley Internet
> Name Daemon (BIND) as the default, base-system name server in several
> open source projects, where it is perceived as smaller, more modern,
> and more secure for most applications.

Unbound is packaged in Debian.

-   Wikipedia: {{< wp "Unbound (DNS server)"  "unbound" >}}
-   [ArchWiki: unbound](https://wiki.archlinux.org/index.php/Unbound).

# Bind {#bind}
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
<!--
[[file:../../../../content-org/notes/network_notes/netconf_notes.org::#dnsmask][Dnsmasq notes]]
-->

Dnsmasq (GPL) is a a lightweight tftp, DHCP and caching DNS server.

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
-   [Setting up dnsmasq - a lightweight DHCP and DNS server :: Fedora Docs
    ](https://docs.fedoraproject.org/en-US/fedora-server/administration/dnsmasq/)
-   [extensive example of configuration file for dnsmasq
    ](http://thekelleys.org.uk/dnsmasq/docs/dnsmasq.conf.example)
    You find there some otherwise *secret options* as how to configure
    your server for a bootp relay.
-   Man pages: [dnsmasq.8](http://thekelleys.org.uk/dnsmasq/docs/dnsmasq-man.html),
    and [dnsmasq setup](http://thekelleys.org.uk/dnsmasq/docs/setup.html), from
    the dnsmasq distribution.
-   [Using dnsmasq in NetworkManager to send DNS requests for a specific domain to a
    selected DNS server Red Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/configuring_and_managing_networking/using-different-dns-servers-for-different-domains_configuring-and-managing-networking#using-dnsmasq-in-networkmanager-to-send-dns-requests-for-a-specific-domain-to-a-selected-dns-server_using-different-dns-servers-for-different-domains)

# Host Name Resolution
-   [Archwiki: Domain name resolution
    ](https://wiki.archlinux.org/index.php/Domain_name_resolution)
-   Fedora documentation:
    [NameResolution](https://fedoraproject.org/wiki/Networking/NameResolution),
-   [GNU/Linux host name resolution - /dev/posts/
    ](https://www.gabriel.urdhr.fr/2020/04/20/linux-host-name-resolution/)
-   [Using different DNS servers for different domains Red Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/configuring_and_managing_networking/using-different-dns-servers-for-different-domains_configuring-and-managing-networking#doc-wrapper)

## Resolv.conf {#resolvconf}
{{< wp "resolvconf" >}} is a middleman between the network configuration services and
`/etc/resolv.conf`, It allows to manage the nameserver informations provided by
some network clients like
[dhcpd](https://wiki.archlinux.org/title/Dhcpcd#/etc/resolv.conf),
[NetworkManager](https://wiki.archlinux.org/title/NetworkManager#/etc/resolv.conf)
or a vpn.

`resolvconf` is either a stand alone script, or is provided by `openresolv` or
{{< iref "#systemd-resolved" "system-resolved" >}}.

When `resolvconf` is installed, the `/etc/resolv.conf` file is replaced by a symbolic
link, and the resolver instead uses the dynamically generated linked file.

-   [resolv.conf - Debian Wiki](https://wiki.debian.org/resolv.conf).
    describe the use of the two utilities _resolvconf_ and _openresolve.
-   [openresolv](https://roy.marples.name/projects/openresolv)
    is a resolvconf implementation. It supports the libc resolver,
    {{< iref "#bind" "Bind" >}}, {{< iref "#dnsmasq" "dnsmasq" >}},
    {{< iref "#unbound" "Unbound" >}}.
    -   [openresolv - ArchWiki](https://wiki.archlinux.org/title/Openresolv).

## Systemd-resolved {#systemd-resolved}
*systemd-resolved* is a system service that provides network name resolution to local
applications via a D-Bus interface. It implements a caching and validating DNS/DNSSEC
stub resolver, as well as an LLMNR and MulticastDNS resolver and responder.

Local applications may submit network name resolution requests via three interfaces: a
dbus API, the glibc getaddrinfo API, a local DNS stub listener on the IP addresses
127.0.0.53 and 127.0.0.54 on the local loopback interface.

-   [systemd-resolved.service - Freedesktop Manual
    ](https://www.freedesktop.org/software/systemd/man/systemd-resolved.service.html)
-   [systemd-resolved - ArchWiki](https://wiki.archlinux.org/index.php/Systemd-resolved)
-   [systemd-resolved and VPNs - systemd.io](https://systemd.io/RESOLVED-VPNS/)
-   [Systemd-resolved DNS configuration for VPN - /dev/posts/
    ](https://www.gabriel.urdhr.fr/2020/03/17/systemd-revolved-dns-configuration-for-vpn/)
-   [Using systemd-resolved in NetworkManager to send DNS requests for a specific domain
    to a selected DNS serve rRed Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/configuring_and_managing_networking/using-different-dns-servers-for-different-domains_configuring-and-managing-networking#using-systemd-resolved-in-networkmanager-to-send-dns-requests-for-a-specific-domain-to-a-selected-dns-server_using-different-dns-servers-for-different-domains)


The command line client is {{< man "resolvectl" >}} and the configuration is explained
in {{< man "systemd-resolved" >}}.

Systemd-resolved works with a {{< iref "netconf#syqtemd-networkd" "systemd-networkd" >}}
configuration, but you can also use
{{< iref "netconf#network-manager" "network manager" >}} and have systemd-resolved
manage you DNS resolution as explained in the [NetworkManager Reference Manual
](https://networkmanager.dev/docs/api/latest/index.html)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
