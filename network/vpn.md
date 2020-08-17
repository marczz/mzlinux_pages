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

To use a the [management interface
](https://openvpn.net/index.php/open-source/documentation/miscellaneous/79-management-interface.html)
just add the parameter:

    $ openvpn --management /run/openvpn/management unix

Then connect to the socket

    $nc -U /run/openvpn/management

`help` gives a comman list. You can also give an address, usually
127.0.0.1 and a port and use telnet.


## Using OpenVpn on small devices

If you have a tiny router with a light distribution your RAM may
require that you use a small executable.

The package OpenVPN requires libssl (and libcrypto provided in the
same ipkg) zlib lzo libpthread, There are multiple versions of this
package available on the web, compiled with diverse options

A main havoc with this package is the size of the required `lybcripto`
which is the main part of libopenssl, it is around 1.5Meg, you can
disable some encryption to reduce the size but you will gain 100/200
Kilobytes only. `openvpn` by itself is 0.35Meg and libssl 0.25Meg

If it is still too large for your rom , you have still some
options. You can change your tunnel to a smaller tunneling program,
using a lighter encryption than this big `libcrypto`, like
[vtun](http://vtun.sourceforge.net/)
when it is not linked with openssl; you can also put `libcrypto` on an
NFS partition, or put `libcrypto` in tmpfs in /var/lib, and upload it
at boot through http, ftp, scp or whatever.

OpenVPN needs a configuration of the tunnel but it must come also with
a configuration of the firewall


## Configuring OpenVpn with shorewall {#openvpn_with_shorewall}

The process of configuring ShoreWall for OpenVPN is very well described
in the [OpenVPN page of shorewall documentation](http://www.shorewall.net/OPENVPN.html).
I just extract some key points

I just give configuration on the left side, supposed to be at internet
address 206.162.148.9, with gateway local ip 192.168.1.1 serving local
network 192.168.1.0/24; of course you need to do it on both sides.

-   Declare your vpn zone in `/etc/shorewall/zones`

        vpn             VPN               Remote subnet

-   Declare the interface in `/etc/shorewall/interfaces`

        vpn        tun0

-   In `etc/shorewall/tunnels`

        openvpn:1194            net    134.28.54.2

    note the port number`1194`, it is better to give it than relying on
    defaults which may be incorrect or different on both sides.

-   Add to your policy the policies for the tunnel, probably at least:

        loc             vpn             ACCEPT
        vpn             loc             ACCEPT

    Depending of the level of security on each segment of your network,
    you can want to restrict this, or to extend it by adding say:

        fw             vpn             ACCEPT
        vpn            fw             ACCEPT

-   The fine tuning of access right is in `/etc/shorewall/rules`, and
    depends on the policies that you have chosen. If you don't want to
    accept blindly from vpn to fw but only by service, put a `REJECT`
    policy and add in your rules entries for the services you allow:

        #       Accept SSH connections from vpn network for administration
        #
        AllowSSH        vpn             fw
        #       Allow Ping To And From Firewall
        #
        AllowPing       vpn             fw
        AllowPing       fw              vpn

If you want to route and filter traffic from a tunnel to an other, don't
put a `client-to-client` in your openVPN server configuration but :

-   in your `interfaces` file:

        vpn     tun0            detect          routeback

-   in `policy`

        vpn             vpn             REJECT          ULOG

    The goal for this rule is not only to reject and log unknown vpn to
    vpn traffic, but to allow shorewall to build iptables chains to deal
    with intra vpn traffic. Once you have given a `policy` you have
    nothing more to set to admit `ESTABLISHED` traffic.

-   In your `rules`

        # Allow tun to tun
        ACCEPT          vpn:192.168.0.0/22      vpn:192.168.8.0/24

    to allow *new*traffic from your `192.168.0.0/22` private subnet to
    the `192.168.8.0/24`.

## Configuring OpenVPN with static keys

The configuration of open VPN is detailed in the [Open VPN HOWTO
](http://openvpn.sourceforge.net/howto.html) that you should read,
for a minimalistic configuration I just indicate how to set up a static
key configuration.

-   Set a directory for open VPN configuration, i.e `/etc/openvpn`
-   Create a static key with the following command:

        openvpn --genkey --secret static.key

-   Copy this key with any secure mean (ssh) on the peer openvpn
    directory
-   Generate a config file with at least

        dev tun
        # your (say left) internet address
        local 206.162.148.9
        # remote peer (right) internet address
        remote 134.28.54.2
        # Your (left) gateway ip on this local network 192.168.1.1
        # The gateway ip on remote (right) local network 10.0.0.1
        ifconfig 192.168.1.1 10.0.0.1
        # The up script will establish routes
        up  /etc/openvpn/openvpn.up
        # Our pre-shared static key
        secret secret.key
        #
        # new OpenVPN uses UDP port 1194 by default, old use 5000,
        # if unsure fix the port on both sides
        port 1194
        # Verbosity level.
        verb 5

    Of course this is only a minimal configuration to test openvpn, you
    will need to look at the doc to complete it.

-   Set your `openvpn.up` script

    The arguments will be:
    `tun_dev tun_mtu link_mtu ifconfig_local_ip ifconfig_remote_ip [ init | restart ]`

        ip route add 10.0.0.0/24 via $5

    `10.0.0.0/24` stand here for the remote (right) local network.

-   Configure your firewall to accept the traffic from the tunnel, look
    at the open VPN HOWTO to do so, if you use shorewall, I have
    sketched the process in an
    {{< iref "#openvpn_with_shorewall" "OpenVpn with Shorewall section" >}}
-   Configure the right endpoint in the same way
-   Test your file with launching by hand:

        openvpn --config openvpn.conf

    on both sides, and examine the ouput, be carefull, even if openvpn
    does not immediately fail, it may hang up later due to
    some misconfiguration.

    A bad problem of mtu path discovery, on one server made my nfs links
    hang up, until I fix the mtu manually. May be this problem is quite
    specific to this configuration, because I have to cross one externel
    firewall that eat my udp packets in one way when they are not in an
    ESTABLISHED connexion, and so forbid correct mtu path discovery;
    nevertheless similar problems are not uncommon.

## Configuring openVPN 2 with SSL/TLS

OpenVPN version 2. bring a great feature, a unique instance with a
unique tun/tap interface can be used for many clients, great on openwrt
where you don't have so much RAM, as to run a dozen of independent
tunnels

I use a single openVPN to serve both a tunnel between a home and
corporate private network, and also for a tunnel to wifi connected
laptops *roadwarriors*

Previously my clients where  running openVPN 1.6, because this was the
only release available on the LEAF router system,  in these case you are
limited in the multiple way of configuring your tunnel. Mainly you
cannot use the dynamic configuration of the client by the server ( The
`--push` directive), because you client cannot understand, nevertheless
with identification by RSA common name, and client specific
configuration directory, it is still possible.

In any case the main use of the push is to allow a flexible
configuration when you can connect to multiple servers, or to allow to
do the configuration only on the server, otherwise it is easier to put
the ip of the client side tunnel in the client configuration.\

Dynamic dhcp addresses add some level of complexity (see openvpn doc),
but I have attributed a fixed a ip depending of their MAC address, and
it is a lot simpler in this case.

With an openVPN server you have to use SSL/TLS RSA certificates and
keys.

The building of certicates and key are described in [OpenVPN
HOWTO](http://openvpn.net/howto.html), you can use either the `openssl`
command directly or via the [easy-rsa
scripts](http://openvpn.net/index.php/documentation/miscellaneous/rsa-key-management.html "openvpn.net rsa-key-management.html"),
to generate a master certificate authority, certificate/private-key
pairs for your server and each client, and Diffie Hellman parameters.
Take care to give to your key pairs a signifiant `common name`, because
your tunnel is configured for each client based on this name, at least
if you choose like I do a configuration directory. I advise you to do so
if you have to communicate with many clients.

Your server configuration file looks like that:

    mode server

    # comment client-to-client, so you don't act as a router
    # that allows firewall filtering of vpn to vpn traffic
    #client-to-client

    # "dev tun" will create a routed IP tunnel,
    # "dev tap" will create an ethernet tunnel for bridging.
    dev tun

    # Configure server mode and supply a VPN subnet
    # FOR OpenVPN to draw client addresses from.
    # The server will take 192.168.3.254 for itself, 192.168.3.253 i a virtual
    # tunnel endpoint. Each client will be able to reach the server
    # on 192.168.3.254 and will be given a subnet from the pool.
    # Clients can be given ad-hoc addresses from clients directory
    # They are identified by their certificate X509 common name (CN)
    ifconfig 192.168.3.254  192.168.3.253

    # pool of /30 subnets to be dynamically allocated to client instances
    # starting at 3.8 ending at 3.32
    ifconfig-pool 192.168.3.8 192.168.3.32

    # routes for roadwarriors
    route 192.168.3.3 255.255.255.255
    route 192.168.3.4 255.255.255.255
    # .....
    # routes for remote private subnet
    route 192.168.8.0 255.255.255.0
    # make sure that the end of tunnel keep a route out of vpn
    route 134.28.54.2 255.255.255.255 net_gateway
    # but send all traffic to all remote internet addresses of dmz servers
    # thru the tunnel
    route 134.28.0.0 255.255.0.0

    #Specify a directory dir for custom client config files.
    #  OpenVPN will look in this directory for a file having the same name
    # as the client's X509 common name.
    client-config-dir clients

    # this end point is the server
    tls-server

    # Diffie-Hellman Parameters (tls-server only)
    dh dh1024.pem

    # Certificate Authority file. The server and all clients will
    # use the same ca file.
    ca myserver-ca.crt

    # Our public/private key pair
    cert mySrv.crt
    key mySrv.key


    # OpenVPN uses UDP port 1194 by default (previously 5000).
    port 1194

    # TCP or UDP server?
    ;proto tcp
    proto udp

    # If OpenVPN is built with  LZO compression.
    # Enable compression on the VPN link. you must also
    # enable it in the client config file.
    comp-lzo

    # The maximum number of concurrently connected clients
    max-clients 15

    # The persist options avoid accessing certain resources on restart
    # that may no longer be accessible because of the privilege downgrade.
    persist-key
    persist-tun

    # reduce the OpenVPN daemon's privileges after initialization.
    user nobody
    group nobody

    # If you built OpenVPN with
    # LZO compression, uncomment
    # out the following line.
    comp-lzo

    #I use the IP layer fragmentation (not the internal mssfix/fragment)
    # tun-mtu is found by running openvpn --test-mtu.
    tun-mtu 1402
    #to use internal fragmentaion put
    ;tun-mtu 1500
    ;tun-mtu-extra 32
    ;mssfix 1450

    # Ping every 15 seconds, assume that remote peer is down if no ping
    # received during a 60 second time period.
    # same as ping 15 ping-restart 60
    keepalive 15 60

    # Output a short status file showing current connections, truncated
    # and rewritten every 2 minutes. Status can also be written to the
    # syslog by sending a SIGUSR2
    status /tmp/openvpn-status.log 120

    # Verbosity level.
    verb 5
Each client has a configuration file in clients directory, that looks
like:

    ifconfig-push 192.168.8.253 192.168.3.254
    iroute 192.168.8.0  255.255.255.0
    iroute 134.28.0.0   255.255.0.0

`iroute` commands **are not aimed at the ip level routing, but to the
vpn server**, to internally route traffic from the unique virtual tune
interface through the right actual client tun interface

The client configuration looks like:

    #client-side OpenVPN 1.6 config file for connecting to
    # multi-client v2 server.
    # This configuration can be used by multiple clients, however each
    # client should have  its own cert and key files.

    dev tun
    proto udp

    # The hostname/IP and port of the server.
    local 192.168.2.3
    remote 192.168.2.254
    port 1194

    # the local and remote end point can be configured on the server
    # either by ifconfig-push as above or statically by
    # remember that the proper use is to take private IP addresses
    # which are not a member of any existing subnet which is in use.
    # The ifconfig on the client use to be the reverse than the one on the server
    # (but the end point is completely virual and can be arbitrary chosen as long
    # as it does not conflict with existing IP)
    ifconfig 192.168.3.253 192.168.3.254

    # take the vpn as the default route
    redirect-gateway


    # Keep trying indefinitely to resolve the
    # host name of the OpenVPN server.  Very useful
    # on machines which are not permanently connected
    # to the internet such as laptops.
    resolv-retry infinite

    # Downgrade privileges after initialization
    user nobody
    group nobody

    # Try to preserve some state across restarts.
    persist-key
    persist-tun

    #trigger a SIGUSR1 restart after 60 seconds pass without reception of a packet
    # from remote. (the server is configured to ping every 15s)
    ping-restart 60

    # SSL/TLS parms.
    tls-client
    ca myserver-ca.crt
    cert Myclient.crt
    key Myclient.key

    # Enable compression on the VPN link as you did on the server.
    comp-lzo

    # Set log file verbosity.
    verb 5

    # to speak with v2 server with internal fragmentation
    ;tun-mtu 1500
    ;tun-mtu-extra 32
    ;mssfix 1450
    key-method 2
    # or with ip mtu (see server conf)
    tun-mtu 1402

# Connect OpenVpn to TigerVpn

Taken from  [TigerVpn: Linux OpenVPN setup
](https://help.tigervpn.com/support/solutions/articles/1000214258-linux-openvpn-setup)


Step by step instructions for OpenVPN:

1.  Open terminal (keyboard shortcut: Ctrl + Alt + T). Keep this open
    for all steps.
2.  Install OpenVPN client by entering "sudo apt-get install openvpn"
    (if you are requested a password, enter the password which you have
    used when creating your account).
3.  Login to tigervpn site. Go into Dashboard and download openvpn
    config to desktop. You will download the file  `config-256bit.zip`
4.  Navigate to dir that you downloaded the openvpn config to (like
    `cd ~/Downloads` depending on your download directory).
5.  Extract `config-256bit.zip` with command `unzip config-256bit.zip`
6.  Move the config directory wher you want to keep your config. I use
    `~/.config/openvpn/tigervpn`, but it's up to you.
7.  Go to the config directory, you can list all your config with `ls`.
8.  An optional step is nomalizing the filenames; delivered files have
    spaces in their name, which is error prone in linux, I use to
    remove the spaces with a command like:

        $ for n in *; do mv "$n" $(echo "$n" |sed 's/ //'g); done

9.  If you are still in the config folder, choose the wanted server
    you can start openvpn with

        $ sudo openvpn --config "US-Atlanta@tigervpn.com.ovpn"

    _The quotes arround the configuration file are optional if you
    followed the sped (8); but mandatory if the file name still
    contain space character._
10. OpenVPN will ask you for credentials, enter those which you can
    find on the tigerVPN dashboard. _This is_ __not__ _the credentials
    to log in the tigervpn web interface._
12. To disconnect from the OpenVPN connection simply open terminal and
    type `Ctrl + C` command.
13. You cannot launch openvpn from an other directory with the
    provided configuration; beecause the `ca.crt` file has no full
    pathname; If you want to use it from anywhere replace the line

        ca ca.crt

    by:

        ca ~/.config/openvpn/tigervpn/ca.crt

    in each configuration; then give the full pathname of the config
    file:

         $ sudo openvpn --config ~/.config/openvpn/tigervpn/US-Atlanta@tigervpn.com.ovpn

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
