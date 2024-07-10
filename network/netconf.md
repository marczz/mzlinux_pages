---
title: Network Configuration
---


See also at readthedocs
[Unix Memo](http://unix-memo.readthedocs.org/en/latest/):
[Network Commands Memo](http://unix-memo.readthedocs.org/en/latest/net_commands.html)
[Wpa Supplicant](http://unix-memo.readthedocs.org/en/latest/wpa.html),
[Network Manager Memo
](http://unix-memo.readthedocs.org/en/latest/net_commands.html#network-manager).


The network configuration guides are in the page
 {{< iref "network" "Network references"  >}}.
See also {{< iref "dns" "Domain Name Server (DNS)" >}}, {{< iref "vpn" "VPN" >}}.

# How to manage your network

To manage your network connections, and peculiarly the wireless
connections, you have to choose between to paths.

-   The legacy script way, using the basic driver, route and wireless
    tools to do configuration, report, and management of the
    network. It is used by the *ifup/ifdown* script, or also by the
    new _netctl_. If you follow this path you can benefit from many
    helpers like _guessnet_ or the many _wpa_supplicant_ clients. It
    can aloow you to finely tune-up your configuration to automatize
    most of the process following your particular needs, and
    environment.
-   The network manager way, that aleviate the task of programming the
    scripts configuration.  The managers detect every change in your
    network environment, and let you choose among the available
    networks, and can either auto-connect to private network if you
    have registered the proper authentication data, or propose you to
    fill it through a Gui.

The choice between the two ways of configuring your network is not
easy, the network manager way is the easier, that makes it the primary
choice for people that cannot, or does not want to write a complex
configuration.  But these managers, and still more the graphical
interface are heavy not appropriate for headless machines. There is a
total lack of portability of the registered data from one piece of
software to another one, and even moving the configuration from one
machine to another one with the same software, is possible, but not
clearly proposed.

Using the legacy scripts allow you to finely tweak your
configuration. On my laptop I say _If there is an ethernet link and
you can join by arp one of these servers, use this configuration,
otherwise if you join this other ...._ And when I am inan environment
that I use to meet, my configuration is completely automatic. I can
not achieve that with these network managers.  On the other hand
configuring, by hand, a new network, will require a true proficiency
and knowledge of many networking tools. Even when you use to find it
easy, after a pause of some months, you begin again to do mistakes. So
when in a new situation, that you meet only once or few times, the
network manager way is easier, if you accept the cost.

So you may end up wanting to use combine both. but it is difficult,
the configuration are completely distinct, the change you do in one
place is not reflected in the other one.  Worse when two management
tools compete to control a driver, they can produce an unusable
network.  When trying to make my _ifup/down_ an network-manager
collaborate, I get contradictory routes, and have no more
connectivity. So I choose to keep both but to have only one enabled,
usually the script way, and when roaming, and I don't feel to plunge
in the gears of the wireless extension and tools, I switch to a
manager.

# Network management references

-   [ArchWiki: Network Configuration
    ](https://wiki.archlinux.org/index.php/Network_configuration).
-   [Router - ArchWiki](https://wiki.archlinux.org/title/Router)
    is a tutorial for turning a computer into an internet gateway/router.
-   [Debian Reference: Network setup
    ](http://www.debian.org/doc/manuals/reference/ch05.en.html)
    even if the manual is updated the chapter seems partially obsolete and uses old
    tools, and a pre-systemd configuration _version 2.98 2022_.
-   [Debian Handbook - 8.2. Configuring the Network
    ](https://www.debian.org/doc/manuals/debian-handbook/sect.network-config.en.html).
-   [Debian Wiki: Network Configuration](http://wiki.debian.org/NetworkConfiguration)
    updated 2021.
-   [Debian Wiki Network FAQ](https://wiki.debian.org/NetworkFAQ).
-   [Debian Wiki: How to use a WiFi interface](https://wiki.debian.org/WiFi/HowToUse)

# Network management Tools

-   [connman](http://connman.net/) is a light daemon for managing
    Internet connections within embedded Linux devices.
    It can be controled by a command-line front-end, by menu
    indicators, or a gtk frontend.<br />
    Note that the Debian (sid) package is (as 2013) very outdated, and
    barely usable and does not includes any frontend.
    -   [git.kernel.org: connman
        ](http://git.kernel.org/cgit/network/connman/connman.git/tree)
    -   [GitHub: connman-deb](https://github.com/pfl/connman-deb)
        unofficial packaging of the last connman.
    -   [ArchLinux: connman](https://wiki.archlinux.org/index.php/Connman)
    -   [Ubuntu Wiki:connman](https://wiki.ubuntu.com/ConnMan)
    -   [UnbuntuGeeks: Connection Manager (ConnMan)
        ](http://www.ubuntugeek.com/connection-manager-connman-managing-internet-connections-in-linux.html)
-   __Guessnet__ is a network detection tool to use when moving a machine among networks
    which don't necessarily provide DHCP. _Still packaged in Debian, but source repo
    seems unavailable_.
-   [netctl](https://wiki.archlinux.org/index.php/Netctl)
    is the standard networking management for Archlinux since it
        switched to systemds. It is also packaged in Debian.
    -   [Git repo](http://guessnet.alioth.debian.org/)
        and [GitHub mirror](https://github.com/joukewitteveen/netctl)
-   [wpa_supplicant - ArchWiki](https://wiki.archlinux.org/title/Wpa_supplicant)
-   **wpa_gui**  is a graphical frontend for *wpa_supplicant*
    using the *qt4* toolkit. It belongs to the
    [kernel.org WPA supplicant software
    ](http://wireless.kernel.org/en/users/Documentation/wpa_supplicant).
    *wpa_gui* can report network scanning, choose an AP, and fill in
    the *wpa_supplicant* configuration.  It has a footprint of 20M
    resident/17M shared.

## Systemd-networkd {#systemd-networkd}

From the
[Manual](https://www.freedesktop.org/software/systemd/man/systemd-networkd.service.html)
_systemd-networkd is a system service that manages networks. It
detects and configures network devices as they appear, as well as
creating virtual network devices_.

Networks are configured in .network files, see
[systemd.network](https://www.freedesktop.org/software/systemd/man/systemd.network.html)
and virtual network devices are configured in .netdev files, see
[/systemd.netdev](https://www.freedesktop.org/software/systemd/man/systemd.netdev.html).

You can use it instead of the _ifupdown_ scripts and Network manager.

You don't have to install anything, it is included in systemd since July 2014, systemd
version 215.

-   [ArchWiki: systemd-networkd](https://wiki.archlinux.org/index.php/Systemd-networkd)
    is an extensive howto on the configuration and use of _systemd-networkd_.

There are many tutorials to explain how to switch in Debian from
{{< iref "#network" "Network-Manager" >}}
to _systemd-networkd_:

-   [How to switch from NetworkManager to systemd-networkd on Linux
    ](http://xmodulo.com/switch-from-networkmanager-to-systemd-networkd.html)
    a Xmodulo tutorial _updated 2020_.
-   [Using systemd-networkd to work your net
    ](https://www.redpill-linpro.com/techblog/2016/08/17/systemd-network.html)
    on Redpill Linpro Blog _2016_.


## Network Manager {#network-manager}

See my memo at readthedocs
[nm memo
](http://unix-memo.readthedocs.org/en/latest/net_commands.html#network-manager)

{{< wp "NetworkManager" >}} ( GPL) is a networking configuration daemon which try to
provide a painless and automatic network setup. It is part of the gnome project but
communicate thru dbus and has no gnome dependencies by itself. The gnome front-end add
some more dependencies.  In Debian you can install `network-manager` with few
package dependencies if you disable unused _recommended_ packages.

NetworkManager by itself is a small daemon 13M/10M shared.

If you want the systray *nm-applet* you have to add the package `gnome-network-manager`.
The applet itself adds 37M/30M shared _(vers 1.8.20 2019, and only ~10M added mem)_


Network Manager allow to manage DNS with
{{< iref "dns#dnsmasq" "dnsmasq" >}} or
{{ iref "dns#systemd-resolved" "Systemd-Resolved" >}}.

-   [NetworkManager Reference Manual
    ](https://networkmanager.dev/docs/api/latest/index.html)
-   [NetworkManager  Gnome Home
    ](https://wiki.gnome.org/Projects/NetworkManager) references
    all the official man pages and documents. _But pages moves and
       many links are broken in the gnome wiki._
    -   [Network Manager Configuration plugins
        ](https://wiki.gnome.org/Projects/NetworkManager/SystemSettings)
    -   [Network Manager System Setting
        ](https://wiki.gnome.org/Projects/NetworkManager/SystemSettings).
    -   [NetworkManager FAQ](https://wiki.gnome.org/DarrenAlbers/NetworkManagerFAQ)
-   [ArchWiki: Network Manager](https://wiki.archlinux.org/index.php/NetworkManager)
    after the Reference Manual Archwiki is the most complete page on _nm_ settings.
    It includes a [Command line section
    ](https://wiki.archlinux.org/index.php/NetworkManager#Command_line)
    with _nmcli_, _nmtui_, _nmcli-dmenu_.
-   [Debian Wiki: Network Configuration](https://wiki.debian.org/NetworkConfiguration),
    [Network Manager](http://wiki.debian.org/NetworkManager)
-   [Ubuntu community help: NetworkManager](https://help.ubuntu.com/community/NetworkManager),
    [Roaming Profiles With NetworkManager
    ](https://help.ubuntu.com/community/RoamingProfilesWithNetworkManager).
-   [Gentoo: Network Manager](https://wiki.gentoo.org/wiki/NetworkManager)
-   [nmcli](http://fedoraproject.org/wiki/Features/NetworkManagerCmdline)
    is a command line client included in Network Manager since version 0.8.0
-   [Configuring and managing networking - Red Hat Enterprise Linux 8
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_networking/index)
    :
    -   [Chapter 3. managing networking with NetworkManager Red Hat
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_networking/)
    -   [Chapter 5. Configuring IP networking with nmtui
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_networking/configuring-ip-networking-with-nmtui_configuring-and-managing-networking)
    -   [Chapter 6. Configuring networking with nmcli
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/configuring_and_managing_networking/configuring-networking-with-nmcli_configuring-and-managing-networking)
-   [Networking Guide Fedora 25
    ](https://docs.fedoraproject.org/en-US/Fedora/25/html/Networking_Guide/index.html)
    :
    -   [2.4. Using nmcli
        ](https://docs.fedoraproject.org/en-US/Fedora/25/html/Networking_Guide/sec-Using_the_NetworkManager_Command_Line_Tool_nmcli.html)
    -   [4.5. Channel bonding using nmcli
        ](https://docs.fedoraproject.org/en-US/Fedora/25/html/Networking_Guide/sec-Network_Bonding_Using_the_NetworkManager_Command_Line_Tool_nmcli.html)
-   [Fedora Wiki: Network Manager](https://fedoraproject.org/wiki/Tools/NetworkManager),
    [Networking/CLI](https://fedoraproject.org/wiki/Networking/CLI),
    [Networking/Bridging Using NetworkManager
    ](https://fedoraproject.org/wiki/Networking/Bridging#Using_NetworkManager_.28permanent.29)
    [IPv6 tunnel via Hurricane Electric
    ](https://fedoraproject.org/wiki/IPv6_tunnel_via_Hurricane_Electric)
-   In recent releases _greater than 0.9.10_ you find also a ncurses
    client _nmtui_ wich allows to connect/disconnect, choose
    connections and edit them.
-   [networkmanager-dmenu](https://github.com/firecat53/networkmanager-dmenu) (MIT License)
    is a python script to control network manager with
    {{< iref "desktop#dmenu" "dmenu" >}}, {{< iref "desktop#rofi" "rofi" >}},
    {{< iref "desktop#wofi" "wofi" >}},  {{< iref "desktop#bemenu" "bemenu" >}},
    or {{< iref "desktop#fuzzel" "fuzzel" >}}.
-   [nmstate](https://nmstate.io/)
    is a  Declarative Network API which uses NetworkManager as backend.
    -   [Quick start guide | nmstate](https://nmstate.io/user/quick_guide.html).

# Wireless configuration

-   [Network configuration/Wireless - ArchWiki
    ](https://wiki.archlinux.org/title/Network_configuration/Wireless)
-   [ArchWiki: Android tethering](https://wiki.archlinux.org/index.php/Android_tethering)
-   {{< wp "Wicd" >}} (GPL): [Wicd Home](http://wicd.sourceforge.net/)
    is a python network manager. there is a python-GTK client,
    as well as command-line and an ncurses clients. Wicd
    has no gnome dependency. It uses
    wpa-supplicant
    to manage wireless connections. Wicd being a python daemon is not
    slim 13M/3M shared for the daemon, 10M/4M for the monitor.
    -   [ArchLinux: Wicd](https://wiki.archlinux.org/index.php/Wicd)
    -   [Debian Wiki: wicd usage](https://wiki.debian.org/WiFi/HowToUse#Wicd)
-   [wifi-radar](http://wifi-radar.tuxfamily.org/) (GPL)
    is a Python/PyGTK2  utility for managing WiFi profiles on GNU/Linux.

## Low level Wireless Tools

-   [Linux Wireless LAN Howto
    ](http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Wireless.html)
    _(2007)_
    wireless LAN resources for Linux from Jean Tourrilhes [
    [Wireless LANs in use
    ](http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Linux.Wireless.usage.html),
    [Wireless Extensions for Linux
    ](http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Linux.Wireless.Extensions.html),
    [Wireless LAN technology overview
    ](http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Linux.Wireless.Overview.html),
    [Wireless Tools
    ](http://www.hpl.hp.com/personal/Jean_Tourrilhes/Linux/Tools.html)
    ]
-   [Linux Wireless Networking
    ](http://www.linuxhomenetworking.com/linux-hn/wmp11-linux.htm)
    chapter 13 of
    [Linux Home Networking](http://www.linuxhomenetworking.com/#Linux)
-   [Wireless Security](http://www.linux-wireless.org/) (sniffers,
    standards, encryption, drivers, Access Point, WPA, antenna,
    connectors) *Not updated since 2005*
-   [Debian Wiki: Wifi](https://wiki.debian.org/WiFi)
-   A [Wireless Distribution System (Wikipedia)
    ](http://en.wikipedia.org/wiki/Wireless_Distribution_System)
    enables the interconnection of access points wirelessly, openWRT
    support a
    [WDS configuration
    ](http://wiki.openwrt.org/OpenWrtDocs/Configuration).
-   [Debian Wiki: WiFi AdHoc](http://wiki.debian.org/WiFi/AdHoc)
    describes how to establish a decentralized WiFi network without
    access point.  see also Wikipedia: {{< wp "Wireless ad hoc network" >}}
-   Wikipedia: {{< wp "Wireless intrusion prevention system" >}}.
-   [hostapd](http://hostap.epitest.fi/hostapd/)
    (GPL and BSD): IEEE 802.11 AP, IEEE 802.1X/WPA/WPA2/EAP/RADIUS
    Authenticator with dynamic TKIP/CCMP keying, that run on
    Prism2/2.5/3, madwifi (Atheros ar521x), Prism54.org (Prism
    GT/Duette/Indigo)



## wifi analyzers

-   [Kismet](http://www.kismetwireless.net/)
    is an 802.11 layer2 wireless network detector, sniffer, and
    intrusion detection system.
-   [Horst
    ](http://br1.einfach.org/gitweb?p=horst;a=blob;f=README;hb=HEAD)
    is a scanning and analysis tool for IEEE802.11 wireless ad-hoc
    networks and the OLSR mesh routing protocol.
-   [aircrack-ng](http://www.aircrack-ng.org/doku.php)
    an 802.11 WEP and WPA-PSK keys cracking program and set of tools
    for auditing wireless networks.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
