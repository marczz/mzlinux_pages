<!--
.. description:
.. date: 2017-02-17
.. slug: p2p
.. tags:
.. link:
.. book: mzlinux
.. title: P2P
-->

[TOC]

See also [IRC](/node/irc "internal reference"),
[XMPP](/node/xmpp "internal reference"),
[SIP](/node/sip "internal reference"),
[Social Networks](/node/social_networks "internal reference").

-----------------


# P2P references
-   Wikipedia: [w:P2P], [w:Friend-to-friend] _F2F_, [w:Anonymous P2P],
    [w:Private peer-to-peer], [w:Darknet], [w:I2P] _invisible internet
    project_, [w:Comparison of file sharing applications],
    [w:Direct Connect (protocol)|Direct Connect],
    [w:Advanced Direct Connect], [w:Comparison of ADC software]
-   [infoAnarchy](http://www.infoanarchy.org/) is a wiki on the
    subject of information retrieval, distribution and management.
    It contains numerous references to P2P.
-   [Awesome decentralized](https://github.com/croqaz/awesome-decentralized)
    Awesome distributed, decentralized, p2p apps or tools.

# Bittorent {#bittorent}
Bittorent is a client application for the torrent peer-to-peer (P2P)
file distribution protocol.

-   Wikipedia: [w:BitTorrent],
    [w:BitTorrent clients],
    [w:Comparison of BitTorrent clients],
    [w:BitTorrent tracker],
    [w:Comparison of BitTorrent tracker software]
    [w:Local Peer Discovery],
    [w:Peer exchange],
    [w:BitTorrent protocol encryption]
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

Bittorent can be identified by `.torrent` files, [w: Magnet link], or
by a sha1 hash sum. The Magnet link can contain many hashes used by
diverse protocols. Bittorents client use the _btih_ which is the SHA-1
hash sums of the "info" sections of BitTorrent metafiles i.e
`.torrent` files. In the magnet link the _btih_ is written
``xt=urn:btih:[ Info Hash (Hex) ]``. For more info on Magnet link
look at the [w: Magnet link|Wikipedia Page].

[Torrent to Magnet](http://torrent2magnet.com/) is a web service to
convert between `.torrent` files and magnet links.

The npm library and command line [parse-torrent
](https://github.com/feross/parse-torrent) also gives all the
informations in a `.torrent` file.

## Bittorent clients
-   [ArchWiki: list of bittorent clients
    ](https://wiki.archlinux.org/index.php/List_of_applications#BitTorrent_clients).
-   [aria2](/node/file_transfer#aria2) is a utility for downloading
    files it supports BitTorrent and also HTTP(S), FTP, SFTP,
    and [w:Metalink]. It is referenced [in the File Transfer section
    ](/node/file_transfer#aria2)
-   [w:rTorrent] is a text-based ncurses BitTorrent client written in
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
-   [w:Transmission_(BitTorrent_client)|Transmission]
    is a light-weight and cross-platform BitTorrent client. It
    provides a daemon and cli, and an optional GTK or QT GUI.
    It is in any linux distribution including Debian.
    -   [Transmission Home](https://transmissionbt.com/)
        and [Wiki](https://trac.transmissionbt.com/wiki)
    -   [ArchWiki: Transmission
        ](https://wiki.archlinux.org/index.php/Transmission)
-   [Vuze](https://www.vuze.com/) (previously Azureus)
    is a java bittorrent client. In addition to downloading .torrent
    files, Azureus allows to view, publish and share DVD and HD
    quality video content.
    Vuze is in Debian, but in _2017_ only an old version, may be
    because of the licence of new releases.
    -   [Vuze Wiki](https://wiki.vuze.com/).

## WebTorrent {#webtorrent}
[WebTorrent](https://webtorrent.io/) protocol works just like
BitTorrent protocol, except it uses
[WebRTC](#webrtc "internal reference") instead of TCP/uTP as
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

In the browser, WebTorrent uses [WebRTC](#webrtc "internal reference")
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
is a collection of communications protocols and application
programming interfaces that enable real-time communication over
peer-to-peer connections for browsers and mobile
applications.

WebRTC is supported by Chrome ≥ 28, Firefox ≥ 22, Opera ≥ 18 , Safari
≥ 11, Vivaldi ≥ 1.9,

On android it is supported by Chrome ≥ 28, Firefox ≥ 24 , Opera ≥ 12.

WebRTC is used for [WebTorrents](#webtorrent "internal reference"),
[P2P File Transfer](#p2p_file_transfer "internal reference") and
[WebRTC Video Conferences](#webrtc_conference "internal reference").

-   Wikipedia: [w:WebRTC]
-   [Getting Started with WebRTC
    ](https://www.html5rocks.com/en/tutorials/webrtc/basics/)
-   Chrome developpers [WebRTC Home](https://webrtc.org/)
-   [The WebRTC project on GitHub](https://github.com/webrtc)
    has [WebRTC samples](https://webrtc.github.io/samples/)
    [Awesome WebRTC](http://awesome.openrtc.io/)
    is a list of awesome WebRTC modules and resources.
-   [WebRTC Experiment](https://www.webrtc-experiment.com/)
    includes many Tutorials and multiple samples of WebRTC
    applications including Video Multi-user Conferencing applications,
    File Sharing, Screen Sharing, messaging and more.
    There is also a [Firefox extension
    ](https://addons.mozilla.org/en-US/firefox/addon/enable-screen-capturing/)
    to allow screen sharing with webrtc-experiment pages.
-   [WebRTC Hacks](https://webrtchacks.com/)
    is a blog on WebRTC.
-   [Korben](https://korben.info/) :
    [Toutes les bonnes raisons d’utiliser WebRTC dans vos projets
    ](https://korben.info/toutes-les-bonnes-raisons-dutiliser-webrtc-dans-vos-projets.html)
-   Chrome has extensions to do [WebRTC Desktop Sharing
    ](https://chrome.google.com/webstore/detail/webrtc-desktop-sharing/)
    there is also a [WebRTC Screen Sharing
    ](https://www.webrtc-experiment.com/Pluginfree-Screen-Sharing/)
    that you can also use on Firefox.

# P2P file sharing software {#p2p_file_sharing}
See also [File Transfer](/node/file_transfer "internal reference"),
[Temporary storage
](/node/clouds#temporary_storage "internal reference")
and [Clouds
](/node/clouds "internal reference").

Before choosing a P2P file sharing protocol we must be aware of the
lack of privacy of P2P and the risk for anybody to  be framed for
copyright infringement, even without downloading any copyrighted or
DRM material. It is explained in an article from Washington university
cse [Tracking the Trackers](http://dmca.cs.washington.edu/index.html),
and the associated [FAQ](http://dmca.cs.washington.edu/faq.html).

Wikipedia [w:Privacy in file sharing networks] explain that most or
all P2P network can be tracked even eMule or Gnutella. So we have to
rely on [w:Anonymous P2P], mainly through [w:I2P]; or on
[w:Friend-to-friend|F2F (Friend to Friend].


-   [infoAnarchy](http://www.infoanarchy.org/) Reviews of File Sharing /
    Anonymity Tools. [infoAnarchy Wiki
    ](http://www.infoanarchy.org/wiki/index.php/Main_Page)
-   [ArchWiki: list of P2P applications (other than bittorent)
    ](https://wiki.archlinux.org/index.php/List_of_applications#Other_P2P_networks).
-   [w:Freenet] is a censorship-resistant peer-to-peer distributed
    data store.
    -   [Freenet Home page](http://freenetproject.org/)
-   [w:giFT] stands for giFT: Internet File Transfer. It is a daemon
    that combines the capability of peer-to-peer file sharing
    protocols (Gnutella, Ares Galaxy, [w:OpenFT], FastTrack, OpenNap)
    for a simple GUI client) _gift developpement stopped in 2004_.
    -   [giFT Home](http://gift.sourceforge.net/)
-   [w:GNUnet]
    GNUnet is a framework for secure and
    [w:Anonymous_P2P|anonymous peer-to-peer networking] that does
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
-   [w:Gnutella] is a popular P2P file sharing network;
    Gnutella is not associated with the GNU project.
    -   [Comparison of Gnutella software
    ](https://en.wikipedia.org/wiki/Gnutella#Software)
-   [MLDonkey](http://mldonkey.sourceforge.net/) is a multiprotocol
    p2p client and server written in Ocaml, it can access
    EDonkey (edonkey2000 _ED2K_, overnet, Kademlia, emule),
    BitTorrent,  DC++, Gnutella 1/2. The server can be remote
    controled by telnet, WEB browser or GTK+ interface. It is
    available in Debian.
-   [w:OneSwarm] is a privacy-preserving P2P client developed at the
    University of Washington. It is written in java, and is based on
    Azureus (Vuze) BitTorrent client, it keeps compatibility with
    traditional BitTorrent clients, but is aimed at using [w:F2F]
    network in order that your data is shared with friends, shared
    with some friends but not others, and so forth.
    OneSwarm download are available for Linux, Windoze and Mac OS X.
    _Developpement of OneSwarm stopped in 2012_
    -   [OneSwarm Home](http://www.oneswarm.org/).
    -   [GitHub OneSwarm](https://github.com/CSEMike/OneSwarm)
    -   [OneSwarm Wiki](https://github.com/CSEMike/OneSwarm/wiki)
-   [OnionShare](https://onionshare.org/) (GPL)
    is a python tool that lets you securely and anonymously share a file of
    any size. A PPA repository provides `.deb` packages.
    -   [GitHub - OnionShare
        ](https://github.com/micahflee/onionshare).
    -   [OnionShare Wiki
        ](https://github.com/micahflee/onionshare/wiki)
        provides the OnionShare Manual.
-   [w:RetroShare] is an open source, cross-platform Friend-to-Friend
    application that in addition of social networking (chat) offers
    file sharing, even fo big files with 1GB or more.  Your privacy is
    protected with anonymous tunnels and only your direct friends
    might learn which files you download. In contrast with many
    P2P / F2F / I2P software it's developpement is active.

    It is referenced
    [in the Xmpp Page](/node/xmpp#retroshare "internal reference")
-   [w:Robert] is a file sharing application that relies upon the
    security and encryption of peers and tunnels inside of I2P.
-   [Tox](/node/xmpp#tox "internal reference")
    out of instant messaging and video call allow ptivate and secure
    file sharing. Tox has clients for Linux, Windoze, OS X, FreeBSD,
    Android, IOS. See the [Tox entry in the Xmpp Page
    ](/node/xmpp#tox "internal reference")


## P2P file transfer {#p2p_file_transfer}
Is an alternative to store a file for exchange, as the file are not
saved in the cloud they are available for big files, and once the
transfer done the file can not be stolen.

Some applications use dedicated applications, some have a web
interface with transfer in [w:WebRTC], mainly those built on
[WebTorrent](#webtorrent "internal reference) and work with
[w:WebRTC#Support|compatible browsers], some have both.

For uploading on android with the web interface see the [this note
](/node/clouds#android_web_upload "internal reference).

Take care than most [WebTorrent](#webtorrent "internal reference)
based application don't offer encryption or any privacy, your file can
be viewed by any body having or guessing the URL or magnet Link.

-   [justbeamit](https://www.justbeamit.com/) is a P2P file transfer
    service. It has no encryption or password protection.
    transfer from and to android work.
-   [reep.io](https://reep.io/) is a P2P file transfer service, which
    works with browsers supporting webrtc, namely chrome, firefox, or
    opera.  The file is encrypted and sent directly.
    Both browsers must remain open during the full transfer. A
    password protection is available.
    transfer from android with dolphin or chrome work but UC is rejected.
-   <a name="sendanywhere"></a>
    [Send Anywhere](https://send-anywhere.com/) is mainly a P2P
    service, but also include cloud storage to free the sender from
    the contraint that both browser need to be open during all the
    transfer time.

    You can transfer up to 1G for the web
    service, up to 20G using a dedicated desktop app
    (windows, ios, android, linux, chrome extension).Registering is
    not deemed, and the applications are free.

    File transfer using the 6-digit key transfers files directly between
    the two devices in P2P, and does not store files on the server.

    For link sharing and send to device, files are encrypted and
    uploaded to the server temporarily.

    The Send Anywhere link is valid 48h.  For gmail you can send up to
    10GB stored in the cloud for 7 days.

    Note that the web interface is unavailable with an android
    user-agent, we are supposed to download the android apk. When
    setting the user-agent to desktop we acn use the classic web
    interface, it is successful with chrome, but on Dolphin I always
    got the mobile site.

-   They are many other WebTorrent clients in the browser, but for
    most of them your file are public and without protection.
    You have also to use a port wich is not blocked by the firewall.

    Among them:
    The reference implementation [instant.io](https://instant.io/) (
    [gitHub](https://github.com/feross/instant.io)) share by info hash
    url or magnet link; [Lunik Instant Share](http://fs.lunik.xyz/)
    ([GitHub](https://github.com/Lunik/Instant-Share) similar to
    _instant.io_ but only with info hash url;
    [file-pizza](https://file.pizza/) (
    [GitHub](https://github.com/kern/filepizza)) can use the
    [Twillo STUN-TURN nat traversal service
    ](https://www.twilio.com/stun-turn) and generates info url human
    readable, all WebRTC communications are automatically encrypted
    using public-key cryptography; [Squidl.ink](http://Squidl.ink/)
    ([GitHub](https://github.com/darkenvy/Squidl.ink));
    [DropClickPaste](http://dropclickpaste.com/) (_source ?_);
    [P2PDrop](http://app.p2pdrop.com/profile)
    ([GitHub](https://github.com/ajainvivek/P2PDrop)) has support for
    user registration, you select the peers with which you share your
    file. Most of the previous applications have the ability to
    directly preview a media in the browser. But many other
    applications listed in the [WebTorrent FAQ
    ](https://webtorrent.io/faq) are dedicated to music or video
    streaming.
-   [sharefest](https://sharefest.me/) is a WebRTC file sharing
    application with STUN NAT traversal. The [Sharefest source
    Repository](https://github.com/peer5/sharefest) is on GitHub.
    Sharefest was written by the private company
    [peer5](https://www.peer5.com/) which propose _expensive_
    video CDN plan for big data (5TB to 500TB).



# P2P WebRTC conferencing. {#webrtc_conference}

-   [Awesome WebRTC list of chat applications
    ](http://awesome.openrtc.io/#chat)
-   [apptr.tc](https://appr.tc/)
    is a [WebRTC](#webrtc "internal reference") application from the
    [Chrome developers WebRTC samples
    ](https://webrtc.github.io/samples/).
-   [WebRTC Experiment](https://www.webrtc-experiment.com/)
    includes many WebRTC Video Conferencing and Multi-user
    Conferencing applications,
    and also File Sharing, Screen Sharing.
-   [Multi-User Video Conference with WebRTC
    ](http://blog.mgechev.com/2014/12/26/multi-user-video-conference-webrtc-angularjs-yeoman/)
    by Minko Gechev is a tutorial for how to implement a multi-user
    video conference with WebRTC, AngularJS and Yeoman. It includes
    explanation of how the ICE (Interactive-Connectivity
    Establishment) framework is used for NAT traversal.
-   [webrtcH4cKS]((https://webrtchacks.com/):
    [Your Browser as a Audio Conference Server with WebRTC & Web Audio
    ](https://webrtchacks.com/web-audio-conference/) by Alexey Aylarov
    include a [live demo](https://demos.voximplant.com/clientconf/).
-   [PubNub](https://www.pubnub.com/) can be used for
    [WebRTC Video Chat Signaling
    ](https://www.pubnub.com/developers/demos/webrtc/)
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

-   [voxeet](http://www.voxeet.com/) has a free plan allowing
    up to six participants conferences and Android and iOS apps.
-   [Bluejeans](https://www.bluejeans.com/)
    allow videoconferencing up to 100 or thousands clients, and
    provide
    [BlueJeans Apps
    ](https://support.bluejeans.com/knowledge/bluejeans-app)
    for Mac OS, Windows, and Linux, and [android
    ](https://support.bluejeans.com/knowledge/bluejeans-android)
    and a [Chrome plugin
    ](https://support.bluejeans.com/knowledge/optimize-chrome).
    It has free time limited trials but _no free plan_.

# Other P2P software

-   [w:Bitcoin]
    is a decentralized P2P electronic cash system without a central
    server or trusted parties. Users hold the cryptographic keys to
    their own money and make transactions directly with each other.
    -   [ArchWiki: Bitcoin]
    -   [BitCoin Home](https://bitcoin.org/en/)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
