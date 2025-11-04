---
title: P2P
---

See also {{< iref "irc" "IRC" >}},
{{< iref "xmpp" "XMPP" >}},
{{< iref "sip" "SIP" >}},
{{< iref "social_networks" "Social Networks" >}},
{{<iref  "file_sharing" "File Sharing" >}}.
<!-- [[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/social_networks/file_sharing.md][file_sharing.md]]
-->
-----------------


# P2P references
-   Wikipedia: {{< wp "P2P" >}}, {{< wp "Friend-to-friend" >}} _F2F_,
    {{< wp "Anonymous P2P" >}}, {{< wp "Private peer-to-peer" >}}, {{< wp "Darknet" >}},
    {{< wp "I2P" >}} _invisible internet project_,
    {{< wp "Comparison of file sharing applications" >}},
-   [infoAnarchy](http://www.infoanarchy.org/) is a wiki on the
    subject of information retrieval, distribution and management.
    It contains numerous references to P2P.
-   [awesome-peer-to-peer](https://github.com/kgryte/awesome-peer-to-peer)
    A list of peer-to-peer resources.
-   [Awesome decentralized](https://github.com/croqaz/awesome-decentralized)
    Awesome distributed, decentralized, p2p apps or tools.

## Direct connect
-   Wikipedia:     {{< wp "Direct Connect (protocol)"  "Direct Connect" >}},
    {{< wp "Advanced Direct Connect" >}}, {{< wp "Comparison of ADC software" >}}

-   [EiskaltDC++](https://github.com/eiskaltdcpp/eiskaltdcpp) (GNU-GPL)
    EiskaltDC++ is a cross-platform file sharing program that uses the Direct Connect
    (DC aka NMDC) and Advanced Direct Connect (ADC) protocols. It is compatible with
    DC++, AirDC++, FlylinkDC++ and other DC clients. EiskaltDC++ also interoperates with
    all common DC hub software. Debian has several _eiskaltdcpp_ packages with CLI
    interface or QT5 or GTK3.
-   [NCurses Direct Connect _ncdc_](https://dev.yorhel.nl/ncdc)
    is a lightweight direct connect client with a  ncurses interface.
    [ncdc is packaged in Debian](https://tracker.debian.org/pkg/ncdc).

# Bittorent {#bittorent}
Bittorent is a client application for the torrent peer-to-peer (P2P)
file distribution protocol.

-   Wikipedia: {{< wp "BitTorrent" >}},
    {{< wp "BitTorrent clients" >}},
    {{< wp "Comparison of BitTorrent clients" >}},
    {{< wp "BitTorrent tracker" >}},
    {{< wp "Comparison of BitTorrent tracker software" >}}
    {{< wp "Local Peer Discovery" >}},
    {{< wp "Peer exchange" >}},
    {{< wp "BitTorrent protocol encryption" >}}
-   [BitTorrent Home](http://www.bittorrent.com/)
-   [infoAnarchy BitTorrent page
    ](http://www.infoanarchy.org/wiki/index.php/BitTorrent)),
    [BitTorrent Links](http://www.infoanarchy.org/BitTorrent/Links).
-   [Brian's BitTorrent FAQ and Guide](http://www.btfaq.com/)
-   [etree](http://wiki.etree.org/index.php) legal music.
    [Bit Torrent Downloads
    ](http://wiki.etree.org/index.php?page=BitTorrentDownloads)
-   [Tutorial to Creating a Private Torrent File in uTorrent
    ](http://bootstrike.com/Articles/CreateTorrent/) use the
    _uTorrent_ popular windoze client, integrated tracker,
    but we could also use the _azureus_ integrated tracker.

Bittorent can be identified by `.torrent` files, {{< wp " Magnet link" >}}, or
by a sha1 hash sum. The Magnet link can contain many hashes used by
diverse protocols. Bittorents client use the _btih_ which is the SHA-1
hash sums of the "info" sections of BitTorrent metafiles i.e
`.torrent` files. In the magnet link the _btih_ is written
``xt=urn:btih:[ Info Hash (Hex) ]``. For more info on Magnet link
look at the {{< wp " Magnet link"  "Wikipedia Page" >}}.

[Torrent to Magnet](http://torrent2magnet.com/) is a web service to
convert between `.torrent` files and magnet links.

The npm library and command line [parse-torrent
](https://github.com/feross/parse-torrent) also gives all the
informations in a `.torrent` file.

## Bittorent clients
-   [ArchWiki: list of bittorent clients
    ](https://wiki.archlinux.org/index.php/List_of_applications#BitTorrent_clients).
-   {{< iref "file_transfer#aria2" "aria2" >}} is a utility for downloading
    files it supports BitTorrent and also HTTP(S), FTP, SFTP,
    and {{< wp "Metalink" >}}. It is referenced {{< iref "file_transfer#aria2" "in the File Transfer section" >}}
-   {{< wp "rTorrent" >}} is a text-based ncurses BitTorrent client written in
    C++, based on the libTorrent libraries for Unix.
    -   [rTorrent and LibTorrent Wiki
        ](https://github.com/rakshasa/rtorrent/wiki)
    -   [rTorrent User Guide
        ](https://github.com/rakshasa/rtorrent/wiki/User-Guide).
    -   [ArchWiki: rTorrent
        ](https://wiki.archlinux.org/index.php/RTorrent)
    -   ruTorrent is a PHP frontend/web interface to rTorrent,
        [ArchWiki: ruTorrent
        ](https://wiki.archlinux.org/index.php/RuTorrent)
    -   wTorrent is a web interface to rTorrent
        [ArchWiki: wTorrent
        ](https://wiki.archlinux.org/index.php/WTorrent)
-   {{< wp "Transmission_(BitTorrent_client)"  "Transmission" >}}
    is a light-weight and cross-platform BitTorrent client. It
    provides a daemon and cli, and an optional GTK or QT GUI.
    It is in any linux distribution including Debian.
    -   [Transmission Home](https://transmissionbt.com/)
        and [Wiki](https://trac.transmissionbt.com/wiki)
    -   [ArchWiki: Transmission
        ](https://wiki.archlinux.org/index.php/Transmission)
-   <a name="vuze"></a>[Vuze](https://www.vuze.com/) (previously _Azureus_) (GPL-2.0)
    is a java bittorrent client. In addition to downloading .torrent
    files, Azureus allows to view, publish and share DVD and HD
    quality video content.

    Vuze
    was in Debian, [it is no longer the case
    ](https://tracker.debian.org/pkg/azureus), there is some
    [licence incompatibility](https://wiki.vuze.com/w/Vuze_License).
    -   [Vuze Wiki](https://wiki.vuze.com/).

## WebTorrent {#webtorrent}
[WebTorrent](https://webtorrent.io/) protocol works just like
BitTorrent protocol, except it uses
{{< iref "#webrtc" "WebRTC" >}} instead of TCP/uTP as
the transport protocol, it implies changes to the tracker
protocol. Therefore, a browser-based WebTorrent client can only
connect to other clients that support WebTorrent/WebRTC.

[WebTorrent](https://webtorrent.io/) reference applications
are streaming torrent clients for Node.js and the web. WebTorrent
provides the same API in both environments.

The module in node.js is a simple torrent client, using TCP and
UDP to talk to other torrent clients; but which allow to communicate
also with WebTorrent WebRTC trackers. You can use it
[on your page by including the javascript library
](https://webtorrent.io/intro).

The Desktop reference client is
[WebTorrent Desktop](https://webtorrent.io/desktop/), they are
download for Linux (.deb package), Mac, Windoze.

In the browser, WebTorrent uses {{< iref "#webrtc" "WebRTC" >}}
(data channels) for peer-to-peer transport. _WebTorrent does not
support UDP/TCP peers in browser_.

To seed files to web peers, use a client that supports WebTorrent,
e.g. [WebTorrent Desktop](https://webtorrent.io/desktop),
[webtorrent-hybrid](https://github.com/feross/webtorrent-hybrid)
a command line program, or [Instant.io](https://instant.io/)
a website. Vuze has a [WebTorrent plugin
](https://wiki.vuze.com/w/WebTorrent) so it can connect to both
normal and web peers.

-   [WebTorrent Documentation
    ](https://webtorrent.io/docs).
-   [WebTorrent FAQ](https://webtorrent.io/faq).
-   [WebTorrent Desktop](https://webtorrent.io/desktop/) is a
    client for Linux, Mac, Windoze.
    WebTorrent Desktop connects to both BitTorrent and WebTorrent
    peers.
    [GitHub Repository](https://github.com/feross/webtorrent-desktop)

# WebRTC {#webrtc}
is a collection of communications protocols and application programming interfaces that
enable real-time communication over peer-to-peer connections for browsers and mobile
applications.

WebRTC is supported by Chrome ≥ 28, Brave, Firefox ≥ 22, Opera ≥ 18 , Safari
≥ 11, Vivaldi ≥ 1.9, edge ≥ 12 ,

On android it is supported by Chrome ≥ 28, Firefox ≥ 24 , Opera ≥ 12.

On IOS ≥ 11 Safari.

WebRTC is used for {{< iref "#webtorrent" "WebTorrents" >}},
{{< iref "#p2p_file_transfer" "P2P File Transfer" >}} and
{{< iref "#webrtc_conference" "WebRTC Video Conferences" >}}.

WebRTC use for transport as application layer the
{{< wp "Secure Real-time Transport Protocol" >}} *SRTP* the security layer is ensured by
{{wp "Datagram Transport Layer Security" >}}, a variant of TLS adapted to udp instead of
TCP. DTLS ensures the authenticity of the peers through certificate exchange, and
exchange the secret master cryptographic keys and the keys are derived on each side by
applying applying the key derivation function from a single master key, so the session
keys that will be used for the subsequent data transfer are never exchanged.

Then SRTP uses a strong 128 bits AES to encrypt datagrams, an HMAC tag appended to each
packet ensure message authentication, integrity protection, and replay protection.

This prevents an attacker from tampering with or re-injecting previously transmitted
data packets.

The SRTP security depends on the robustness of the implementations, and many breaches,
technically called CVE *Common vulnerabilities exposure* have been found in Google
chrome and Firefox.

The WebRTC API includes no provisions for signaling, that is discovering peers to
connect to and determine how to establish connections among them.

Applications use {{< wp "Interactive Connectivity Establishment" >}} *ICE*
for connections and are responsible for managing session.

{{< wp "Session Traversal Utilities for NAT" >}} *STUN* is a standardized protocol
for such address discovery including NAT classification. A client sends a request to a
STUN server on the internet, which replies with the client’s public address and port.

{{< wp "Traversal Using Relays around NAT" >}} *TURN* places a third-party server to
relay messages between two clients when direct media traffic between peers is not
allowed by a firewall.

The exchange of connection metadata, including ICE candidates, encryption details and
media capabilities (codecs, resolution), is formatted using the Session Description
Protocol (SDP), this SDP message is used for the initial handshake.

ICE which is not part of WebRTC protocol but is implemented by each application, is the
Achilles' heel of WebRTC application, and the target of MITM attacks which would
allow eavesdropping and information leakage; and the session hijacking and
impersonation.

As writing a new webRTC by using npm libraries for the encryption and signaling server
is not a complex task, so there are plenty webRTC file transfer application, some are
created and never updated; it may be difficult to know if they were only a coding
exercise, if they have vulnerability, or even if they have be audited, the same for the
used libraries. It is why I don't include old short lived applications in the following
lists.

For pair discovery the applications use a distinct techniques.
-   For lan, the pair discovery uses techniques like mDNS to gather potential pairs. Some
    file transfert application are exclusively targeted to local area network, like
    {{< iref "#localsend" "localsend" >}}, even without the complication of the signaling
    server needed on WAN, some applications may still exhibit some vulnerability, like
    the [LocalSend File Transfer Vulnerability
    ](https://securityvulnerability.io/vulnerability/CVE-2025-27142)
    in a previous release.
-   On wan a centralized signaling server acts as a temporary meeting point, relaying
    the SDP offer/answer and ICE candidates between the peers. Once a direct connection
    is found, the data stream bypasses the server entirely, flowing directly from peer
    to peer.  The security of this model is primarily dependent on the trustworthiness
    of the signaling and relay servers.

-   Wikipedia: {{< wp "WebRTC" >}}
-   [ WebRTC for the Curious](https://webrtcforthecurious.com/)
-   [Getting Started with WebRTC
    ](https://www.html5rocks.com/en/tutorials/webrtc/basics/) *2012*.
-   Chrome developpers [WebRTC Home](https://webrtc.org/)
-   [The WebRTC project on GitHub](https://github.com/webrtc)
    has [WebRTC samples](https://webrtc.github.io/samples/)
-   [WebRTC Experiment](https://www.webrtc-experiment.com/)
    includes many Tutorials and multiple samples of WebRTC applications including Video
    Multi-user Conferencing applications, File Sharing, Screen Sharing, messaging and
    more.
-   [WebRTC Hacks](https://webrtchacks.com/)
    is a blog on WebRTC.
-   [Awesome WebRTC](https://github.com/nuzulul/awesome-webrtc)
    is a list of awesome WebRTC modules and resources.

# P2P file sharing software {#p2p_file_sharing}
See also {{< iref "file_transfer" "File Transfer" >}},
{{< iref "file_sharing#temporary_storage" "Temporary storage" >}}
and {{< iref "clouds" "Clouds" >}}.

<!--[[file:/share/sync_folders/misc/mznotes/content/docs/mzlinux/social_networks/file_sharing.md::{#temporary_storage}][Temporary File storage]] -->

Before choosing a P2P file sharing protocol we must be aware of the
lack of privacy of P2P and the risk for anybody to  be framed for
copyright infringement, even without downloading any copyrighted or
DRM material. It is explained in an article from Washington university
cse [Tracking the Trackers](http://dmca.cs.washington.edu/index.html),
and the associated [FAQ](http://dmca.cs.washington.edu/faq.html).

Wikipedia {{< wp "Privacy in file sharing networks" >}} explain that most or
all P2P network can be tracked even eMule or Gnutella. So we have to
rely on {{< wp "Anonymous P2P" >}}, mainly through {{< wp "I2P" >}}; or on
{{< wp "Friend-to-friend"  "F2F (Friend to Friend" >}}.


-   [ArchWiki: list of P2P applications (other than bittorent)
    ](https://wiki.archlinux.org/index.php/List_of_applications#Other_P2P_networks).
-   {{< wp "Freenet" >}} is a censorship-resistant peer-to-peer distributed
    data store.
    -   [Freenet Home page](http://freenetproject.org/)
-   {{< wp "giFT" >}} stands for giFT: Internet File Transfer. It is a daemon
    that combines the capability of peer-to-peer file sharing
    protocols (Gnutella, Ares Galaxy, {{< wp "OpenFT" >}}, FastTrack, OpenNap)
    for a simple GUI client) _gift developpement stopped in 2004_.
    -   [giFT Home](http://gift.sourceforge.net/)
-   {{< wp "GNUnet" >}}
    GNUnet is a framework for secure and
    {{< wp "Anonymous_P2P"  "anonymous peer-to-peer networking" >}} that does
    not use any centralized or otherwise trusted services. It's goal
    is to provide  security and respects privacy.
    -   [GNUnet Home](https://gnunet.org/)
    -   [GNUnet user handbook](https://gnunet.org/user-handbook)
    -   [GNUnet FAQ](https://gnunet.org/faq-page)
    -   There are many packages in debian, the gnunet framework which
        provide the console client, a gtk interface, a fuse
        filesystem.
    -   [GNUnet Tutorial](https://gnunet.org/book/export/html/2239)
    -   [ArchWiki: GNUnet](https://wiki.archlinux.org/index.php/GNUnet).
    -   [gnunet-web](https://github.com/amatus/gnunet-web) is a port
        of the GNUnet secure peer-to-peer network to the browser using
        HTTP for browser-to-native communication and soon WebRTC for
        browser-to-browser communication. _still alpha in 2017_.
        -   [gnunet.io: gnunet-web server](https://gnunet.io/).
-   {{< wp "Gnutella" >}} is a popular P2P file sharing network;
    Gnutella is not associated with the GNU project.
    -   [Comparison of Gnutella software
    ](https://en.wikipedia.org/wiki/Gnutella#Software)
-   [MLDonkey](http://mldonkey.sourceforge.net/) is a multiprotocol
    p2p client and server written in Ocaml, it can access EDonkey (edonkey2000 _ED2K_,
    overnet, Kademlia, emule), BitTorrent, DC++, Gnutella 1/2. The server can be remote
    controled by telnet, WEB browser or GTK+ interface. It is available in Debian.
-   {{< wp "OneSwarm" >}} is a privacy-preserving P2P client developed at the
    University of Washington. It is written in java, and is based on {{< iref "#vuze"
    "Azureus (Vuze) BitTorrent client" >}}, it keeps compatibility with traditional
    BitTorrent clients, but is aimed at using {{< wp "F2F" >}} network in order that
    your data is shared with friends, shared with some friends but not others, and so
    forth. _Developpement of OneSwarm stopped in 2012_
    -   [GitHub OneSwarm](https://github.com/CSEMike/OneSwarm)
-   [OnionShare](https://onionshare.org/) (GPL)
    is a python tool that lets you securely and anonymously share a file of any size.
    It is available in many distributions including Debian
    [![packaging](https://repology.org/badge/tiny-repos/onionshare.svg?header=packages)
    ](https://repology.org/project/onionshare/versions);
    as well as F-Droid, IOS App store and testflight.
    -   [GitHub - OnionShare](https://github.com/micahflee/onionshare).
    -   [OnionShare Wiki](https://github.com/micahflee/onionshare/wiki)
        provides the OnionShare Manual.
-   {{< wp "RetroShare" >}} is an open source, cross-platform Friend-to-Friend
    application that in addition of social networking (chat) offers file sharing, even
    fo big files with 1GB or more.  Your privacy is protected with anonymous tunnels and
    only your direct friends might learn which files you download. In contrast with many
    P2P / F2F / I2P software it's developpement is active.
    <!--  [[file:../../../../../../../../srv/nfs_share/sync_folders/misc/mznotes/content/docs/mzlinux/social_networks/xmpp.md::Retroshare {#retroshare}][xmpp: retroshare]] -->
    It is referenced {{< iref "xmpp#retroshare" "in the Xmpp Page" >}}
-   {{< iref "xmpp#tox" "Tox" >}}  <!-- [[file:../../../../../../../../srv/nfs_share/sync_folders/misc/mznotes/content/docs/mzlinux/social_networks/xmpp.md::Tox Protocol {#tox}][xmpp - Tox]] -->
    out of instant messaging and video call Tox allows private and secure
    file sharing. Tox has clients for Linux, Windoze, OS X, FreeBSD,
    Android, IOS. See the {{< iref "xmpp#tox" "Tox entry in the Xmpp Page" >}}


## P2P file transfer {#p2p_file_transfer}
Is an alternative to store a file for exchange, as the file are not saved in the cloud
they are available for big files, and once the transfer done the file can not be stolen.

Some applications use dedicated applications, some have a web
interface with transfer in {{< wp "WebRTC" >}}, mainly those built on
{{< iref "#webtorrent" "WebTorrent" >}} and work with
{{< wp "WebRTC#Support"  "compatible browsers" >}}, some have both.

For uploading on android with the web interface see
{{< iref "clouds#android_web_upload" "this note" >}}.

Take care than for most {{< iref "#webtorrent" "WebTorrent" >}}
your file can be viewed by any body having or guessing the URL or magnet Link.

-   [list of WebRTC file transfert application - Awesome WebRTc
    ](https://github.com/nuzulul/awesome-webrtc?tab=readme-ov-file#file-transfer).

-   <a name="localsend"></a>
    [localsend](https://github.com/localsend/localsend) (Apache-2.0 license)
    is a cross-platform a Flutter/Dart app that enables secure communication between
    devices over your local network using a REST API and HTTPS encryption. LocalSend
    doesn't require an internet connection or third-party servers.

    A client for android is available in F-droid, for ios in AppStore, for Linux there
    are packages is some distributions, including a Nix package.
    [![packaging](https://repology.org/badge/tiny-repos/localsend.svg?header=packages)
    ](https://repology.org/project/localsend/versions),
    a Deb package is in the releases, it is also available in FlatHub.

    Localsend before version 1.17.0 had a [File Transfer Vulnerability
    ](https://securityvulnerability.io/vulnerability/CVE-2025-27142).

    -   [LocalSend Web App](https://github.com/localsend/web),
        is a web app integrating WebRTC and WebSockets to share files with other
        LocalSend peers. The README tell it can communicate native version.
        but I have experienced the [issue #9](https://github.com/localsend/web/issues/9).
        -   [LocalSend Web public instance](https://web.localsend.org/).
    -   [joecalsend](https://git.kittencollective.com/nebkor/joecalsend) (Apache
        License) is a Rust/Ratatui implementation of the LocalSend protocol, which
        provides a TUI. I allows to use localsend on headless servers, as as far as 2025
        the localsend CLI is not available (see
        [issue 31498](https://github.com/localsend/localsend/discussions/1498)).

-   [PairDrop](https://pairdrop.net/) (GPL-3.0)
    is a P2P WebRtc file transfer web application.
    It allows to share directly on the lan, it uses WebRTC signaling server, files are
    sent directly from pair to pair; they are encrypted during the transfer.

    When a pair is behind a NAT (behind a router) the contents are channeled through a
    TURN server.  To communicate on the wan the devices are first paired by creating
    long secrets on each pair.

    There is a pairdrop-cli to send files or text with PairDrop via command-line
    interface.

    A Progressive Web Application *PWA* is available, as well as extension for Linux
    Chromium browsers, Firefox, Android Chrome and ios Safari.

    -   [PairDrop - GitHub](https://github.com/schlagmichdoch/pairdrop).
    -   [PairDrop FAQ](https://github.com/schlagmichdoch/PairDrop/blob/master/docs/faq.md).
    -   Pairdrop can be hosted [locally with Docker
        ](https://github.com/schlagmichdoch/PairDrop/blob/master/docs/host-your-own.md).
    -   [PairdropWebExtension](https://github.com/ueen/PairdropWebExtension)
        on Chromium based browser displays a popup with the Pairdrop website so you can
        receive files and texts easily.
    -   [snapdrop-android](https://github.com/fm-sys/snapdrop-android) (GPL-3.0)
        Android client for local file sharing via https://pairdrop.net, available on F-Droid.

-   <a name="sendanywhere"></a> [Send Anywhere](https://send-anywhere.com/) (
    Private License)
    is mainly a P2P service, but also include cloud storage to free the sender from the
    constraint that both browser need to be open during all the transfer time.

    You can transfer up to 10G, registering is not deemed.

    There are dedicated desktop app for windows, ios, android, linux, chrome extension.

    File transfer using the 6-digit key transfers files directly between the two devices
    in P2P, and does not store files on the server.

    For link sharing and send to device, files are encrypted and uploaded to the server
    temporarily. With the free plan you can store up to 50GB, with a maximum file size
    of 10GB. The Send Anywhere link is valid by default for 48h, that you can extend up
    to 1 month.

    There are paid plans beginning at 6€/month for 200GB storage and 20GB/file. *prices
        from Aug 2025*.

    Send-Anywhere paid plans prices and features are not competitive compared to
    Tresorit or cloud storages.

    Note that the web interface is unavailable with an android user-agent, we are
    supposed to download the android apk. When setting the user-agent to desktop we can
    use the classic web interface.
-   [Feem](https://www.feem.io/index.html) (Private License)
    is an alternative to SendAnywhere but the free plan is quite limited and you have to
    subscribe a plan of 5 $/yr for up to 4 non ios device plus 5$/y for one Appleid on
    ios.
-   See also {{< iref "sip#jami" "Jami">}} _previously Ring_ a communication software
    with file sharing.

-   They are many other WebTorrent clients in the browser, for some of them your
    file are public and without protection, others uses the WebRTC encryption.

    To use it in wan, you have also to use a port which is not blocked by the firewall.
    You can also use it in lan on a port non available on wan, to mitigate the risk of
    your data being spied.

    Many WebTorrent applications were created when WebTorrent become popular and are no
    longer updated since 10 years, few of them are maintained among them:
    -   The reference implementation [instant.io](https://instant.io/) (
        [gitHub](https://github.com/feross/instant.io)) share by info hash
        url or magnet link;
    -   [justbeamit](https://www.justbeamit.com/) is a P2P file transfer
        service. It has no encryption or password protection.
        transfer from and to android work.
    -   [file-pizza](https://file.pizza/) (
        [GitHub](https://github.com/kern/filepizza)) can use the
        [Twillo STUN-TURN nat traversal service
        ](https://www.twilio.com/stun-turn) and generates info url human
        readable, all WebRTC communications are automatically encrypted
        using public-key cryptography;
    -   [peertransfer](https://github.com/perguth/peertransfer)
        Send a file p2p and e2e encrypted in your browser using WebRTC.
        A [hosted instance of Peertransfer](https://perguth.github.io/peertransfer/)
        is available

    Most of the previous applications have the ability to directly preview a media in
    the browser. Many other applications listed in the
    [WebTorrent FAQ](https://webtorrent.io/faq) are dedicated to music or video
    streaming.

### Wormhole protocol {#wormhole_protocol}
The {{< wp "Wormhole_(protocol)" "Wormhole Protocol" >}} makes it possible to get
arbitrary-sized files and directories (or short pieces of text) from one computer to
another. The two endpoints are identified by using identical "wormhole codes".

The protocol tries to create a direct connection between the two ends, but if that
fails, it uses a centralized relay server to ferry data between two separate TCP streams
(one to each client).The Transit Relay is a host which offers TURN
{{< wp "Traversal Using Relays around NAT" >}} like services for magic-wormhole instances.

Wormhole uses [SPAKE2](https://datatracker.ietf.org/doc/rfc9383/)
{{< wp "Password-Authenticated Key agreement" >}} a family of cryptographic algorithms
that uses a short low-entropy password to establish a strong high-entropy shared key.

Wormhole requires a “Mailbox Server” (also known as the “Rendezvous Server”): a simple
WebSocket-based relay that delivers messages from one client to another. This allows the
wormhole codes to omit IP addresses and port numbers. The default is a a freely
available public Applications which desire more reliability can easily run their own
relay.

-   <a name="magic-wormhole"></a>
    [magic-wormhole](https://github.com/magic-wormhole/magic-wormhole) (MIT License)
    is the reference python library and command-line tool named also wormhole.
    -   Magic Wormhole is available an all main distributions
        [![packaging](https://repology.org/badge/tiny-repos/wormhole.svg?header=packages)
        ](https://repology.org/project/wormhole/versions).
    -   Rust Magic Wormhole is also available
        [![packaging](https://repology.org/badge/tiny-repos/magic-wormhole-rs.svg?header=packages)
        ](https://repology.org/project/magic-wormhole-rs/versions),
        as well as the rust client
        [![packaging](https://repology.org/badge/tiny-repos/rust:magic-wormhole-cli.svg?header=packages)
        ](https://repology.org/project/rust%3Amagic-wormhole-cli/versions).
    -   The optional relay server is also packaged
        [![packaging](https://repology.org/badge/tiny-repos/magic-wormhole-transit-relay.svg?header=packages)
        ](https://repology.org/project/magic-wormhole-transit-relay/versions).

    -   [Magic-Wormhole documentation
        ](https://magic-wormhole.readthedocs.io/en/latest/index.html)
    -   Magic-Wormhole can [perform transferts over Tor
        ](https://magic-wormhole.readthedocs.io/en/latest/tor.html).

The wormhole protocol has many [End User / Client Applications
](https://magic-wormhole.readthedocs.io/en/latest/ecosystem.html#end-user-client-applications)
in rust, go, haskell; which are alternatives to the reference python application provided
with the magic-wormhole library.

-   <a name="wormhole-william"></a>
    [wormhole-william](https://github.com/psanford/wormhole-william) (MIT License)
    a Go implementation of the wormhole protocol, compatible with magic-wormhole.

    Binaries are provided in the releases page and in some distributions including
    Debian,
    [![packaging](https://repology.org/badge/tiny-repos/wormhole-william.svg?header=packages)
    ](https://repology.org/project//versions).
-   [rymdport](https://github.com/Jacalz/rymdport) (GPL-3.0)
    a magic-wormhole compatible GUI application written in Go.

    Rymdport is only packaged in few distributions
    [![packaging](https://repology.org/badge/tiny-repos/rymdport.svg?header=packages)
    ](https://repology.org/project/yhttps://github.com/Jacalz/rymdport/versions).
    but binaries are in the release, it is also available on FlatHub, and Go compiling is
    always quite easy.
-   [Warp](https://gitlab.gnome.org/World/warp) (GPL-3.0)
    is a Gnome GUI application for WormHole protocol. It is available in many distributions
    [![packaging](https://repology.org/badge/tiny-repos/warp.svg?header=packages)
    ](https://repology.org/project/warp/versions).
    As it is a Gnome project if your desktop don't use Gnome applications it can pull
    many dependencies, but the recommended installation is via a Flatpak binary which is
    available on FlatHub or for the last daily build on the gitlab repository.
-   [Winden](https://github.com/LeastAuthority/winden) (MIT License)
    is a web application for the magic-wormhole protocol.
    You can host Winden with docker or use it on the public server
    [winden.app](https://winden.app/).

    Winden is compatible with other magic-wormhole clients but if you are using the
    [winden.app](https://winden.app/) site you need to set the mailbox server to
    wss://mailbox.mw.leastauthority.com/v1 and the relay server to
    tcp://relay.mw.leastauthority.com:4001.

    So to send or receive from  {{< iref "#magic-wormhole" "magic-wormhole" >}} to winden
    or {{< iref "#destiny" "destiny" >}} you should use:
    ``` sh
    wormhole --relay-url wss://mailbox.mw.leastauthority.com/v1 \
             --transit-helper tcp:relay.mw.leastauthority.com:4001
    ```

For mobile we find
-   [wormhole-william-mobile](https://github.com/psanford/wormhole-william-mobile) (MIT License)
    is the android application for {{< iref "#wormhole-william" "wormhole-william" >}}
    written in Go and [GioUi](https://gioui.org/) available on the
    playstore, an apk is also in the releases.
-   [wormhole](https://gitlab.com/lukas-heiligenbrunner/wormhole) (GPL-3.0)
    for android, written in Flutter and rustup, available on the Google playstore.
-   [ivox-wormhole](https://github.com/iyox-studios/iyox-Wormhole) (GPL-3.0)
    for android written in rust and flutter. Available on F-Droid and Google PlayStore.
-   <a name="destiny"></a>i
    [Destiny](https://github.com/LeastAuthority/destiny) (MIT License)
    a  cross-platform Magic Wormhole graphical client build in Go with
    [Flutter](https://flutter.dev/) available on Android (Google Play & F-Droid), IOS
    App Store, Linux, Windows, MacOS.

    The Linux binaries are available as an AppImage.

    As described above for Winden to ensure compatibility with other magic-wormhole you
    should use the leastauthority mailbox and servers, as described in the
    [FAQ](https://github.com/LeastAuthority/destiny/blob/main/FAQ.md#more-help).

## Other WormHole applications
We group here some applications inspired by magic-wormhole and using also
[PAKE](https://datatracker.ietf.org/doc/rfc9383/) but are not compatible with
magic-wormhole.

-   [webwormhole](https://github.com/saljam/webwormhole) (BSD Licence)
    a WebRTC application, using also PAKE but with the [CPACE
    ](https://tools.ietf.org/id/draft-haase-cpace-01.html) implementation.
    It provides a command line and Firefox and Chrome extensions.

    The command line is available in NixPkgs
    [![packaging](https://repology.org/badge/tiny-repos/webwormhole.svg?header=packages)
    ](https://repology.org/project/webwormhole/versions),
    or can be compiled with Go.

    -   [WebWormhole](https://webwormhole.com/) a public web server to use webwormhole.
-   [croc](https://github.com/schollz/croc) (MIT License)
    is a file transfert tool written in go inspired by
    {{< iref "#magic-wormhole" "magic-wormhole" >}} but not compatible with it.
    The author wanted to avoid python *at a time where other go, rust, haskell clients
        where not yet available* and ensure to resume interrupted transferts.

    The croc binaries are available in many distributions
    [![packaging](https://repology.org/badge/tiny-repos/croc.svg?header=packages)
    ](https://repology.org/project/croc/versions),
    including NixPkgs and termux (not Debian as far as 2024), and an android application
    is available on F-Droid.
-   [wormhole.app](https://wormhole.app/) (Private Source)
    is a web public server to transfer files, the [encryption protocol is open source
    ](https://github.com/webtorrent/wormhole-crypto), the files are stored on their
    server.
    -   [wormhole.app security](https://wormhole.app/security)


# P2P WebRTC conferencing. {#webrtc_conference}

-   [Awesome WebRTC list of chat applications](http://awesome.openrtc.io/#chat)
-   [apptr.tc](https://appr.tc/)
    is a {{< iref "#webrtc" "WebRTC" >}} application from the
    [Chrome developers WebRTC samples](https://webrtc.github.io/samples/).
-   [WebRTC Experiment](https://www.webrtc-experiment.com/)
    includes many WebRTC Video Conferencing and Multi-user Conferencing applications,
    and also File Sharing, Screen Sharing.
-   [Multi-User Video Conference with WebRTC
    ](http://blog.mgechev.com/2014/12/26/multi-user-video-conference-webrtc-angularjs-yeoman/)
    _2014_ by Minko Gechev is a tutorial for how to implement a multi-user
    video conference with WebRTC, AngularJS and Yeoman. It includes
    explanation of how the ICE (Interactive-Connectivity
    Establishment) framework is used for NAT traversal.
-   [webrtcH4cKS]((https://webrtchacks.com/):
    [Your Browser as a Audio Conference Server with WebRTC & Web Audio
    ](https://webrtchacks.com/web-audio-conference/) by Alexey Aylarov
    include a [live demo](https://demos.voximplant.com/clientconf/).
-   [PubNub](https://www.pubnub.com/) can be used for
    [WebRTC Video Chat Signaling](https://www.pubnub.com/developers/demos/webrtc/)
-   [BigBlueButton](https://bigbluebutton.org/) (GPL)
    is a web conferencing system for online learning.  BigBlueButton
    enables real-time sharing of audio, video, slides (with
    whiteboard), polling, emote icons (including raise hand), chat,
    and the presenter’s desktop. [BigBlueButton source repository
    ](https://github.com/bigbluebutton/bigbluebutton)
    is hosted in GitHub.


In additions of the previous demos there are numerous sites to do
WebRTC videoconferencing:
[Appear.in](https://appear.in/), [gruveo.com](http://gruveo.com/) _2
users video_, [talky.io](https://talky.io/) _video chat
and screen sharing_,  ....

There are also many private expensive software that allow a big number
of clients, that would be impossible with the pure P2P mesh
architecture like :

-   [voxeet](http://www.voxeet.com/) has a free plan allowing up to six participants
    conferences and Android and iOS apps.
-   [Bluejeans](https://www.bluejeans.com/)
    allows videoconferencing up to 100 or thousands clients, and provides
    [BlueJeans Apps](https://support.bluejeans.com/knowledge/bluejeans-app)
    for Mac OS, Windows, and Linux, and
    [android](https://support.bluejeans.com/knowledge/bluejeans-android)
    and a [Chrome plugin](https://support.bluejeans.com/knowledge/optimize-chrome).
    It has free time limited trials but _no free plan_.

# Other P2P software

-   {{< wp "Bitcoin" >}}
    is a decentralized P2P electronic cash system without a central server or trusted
    parties. Users hold the cryptographic keys to their own money and make transactions
    directly with each other.

    As "Mining" for the cryptocurrency is heavily power-hungry, it is a _dirty
    currency_. There are many references and study on the web, no need to reference them
    here.

    -   [ArchWiki: Bitcoin](https://wiki.archlinux.org/title/Bitcoin).
    -   [BitCoin Home](https://bitcoin.org/en/)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
