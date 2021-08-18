---
title: Web Conferencing
---


See also the related page {{< iref "xmpp" "XMPP" >}}
where are included the XMPP/Jingle clients like {{< iref "xmpp#pidgin" "Pidgin" >}},
{{< iref "xmpp#psi" "Psi" >}}, {{< iref "xmpp#jabbin" "Jabbin" >}},
{{< iref "xmpp#jabbin" "Gajim" >}}.

Other related pages are {{< iref "irc" "IRC" >}},
{{< iref "xmpp" "XMPP" >}}
and {{< iref "microblogging" "Micro Blogging" >}}

# Voice transport - SIP

## VoIp protocols references

-   Wikipedia: {{< wp "Voice over IP" >}}, {{< wp "Session Initiation Protocol" >}},
    {{< wp "H.323, [w:IAX" >}}, {{< wp "List of SIP software" >}},
    {{< wp "Comparison of VoIP software" >}}, {{< wp "List of codecs" >}},
    {{< wp "Comparison of audio coding formats" >}}
-   [voip-info.org](http://voip-info.org) a reference guide to all
    things VOIP (
    [VOIP Service Providers
    ](http://www.voip-info.org/wiki/view/VOIP+Service+Providers))
-   [Erlang](http://www.erlang.com/support.html) gives a
    [Voice over IP protocols](http://www.erlang.com/protocols.html)
    article that is a simple desription of the layered hierarchy of the protocols
    involved in the transmission of voice samples through an IP based network.
    You find also a
    [Bandwith whitepaper](http://www.erlang.com/bandwidth.html)
    which explain the bandwidth calculations.

    It also ofers [on line calculators](http://www.erlang.com/calculator/)
    among which
    [Lines to VoIP Bandwidth Calculator](http://www.erlang.com/calculator/lipb/)
    which is very usefull to know how many voice paths you can manage
    knowing your bandwith and codec.
-   [Session Initiation Protocol (SIP)](http://www.cs.columbia.edu/sip/)
    at cs.columbia.edu
-   <a="cusax"></a>[CUSAX RFC 7081](https://tools.ietf.org/html/rfc7081)
    Combined Use of the Session Initiation Protocol (SIP) and the Extensible Messaging
    and Presence Protocol (XMPP)
-   [Klaus Darilion's VoIP bookmarks](http://www.pernau.at/kd/voip/index.html)
-   [Search google for VoIp tests sites](http://www.google.com/search?q=voip+test).
    [Klaus Darilion's SIP Test Tools bookmarks
    ](http://www.pernau.at/kd/voip/bookmarks-sip-test.html).
-   Some bandwith calculators:
    [asteriskguru bandwidth calculator
    ](http://www.asteriskguru.com/bandwidth_calculator.php)
    [bandcalc Bandwidth Calculator](http://www.bandcalc.com/),
    [voiptroubleshooter.com javascript bandwith calculator
    ](http://www.voiptroubleshooter.com/diagnosis/emodel.html).
-   [voip-info:Codecs](http://www.voip-info.org/wiki-Codecs) gives
    a table of codecs used for VoIp _seems obsolete_,
    and links to each one.
-   [opus.org](http://opus-codec.org/) gives a
    [codecs comparison with Opus](http://opus-codec.org/comparison/)
-   [SIPSorcery](http://www.sipsorcery.com/) is an online call
    management application, allowing you using multiple SIP providers
    services.
-   The [GNU Telephony Secure Calling initiative
    ](http://www.gnutelephony.org/index.php/Secure_Call)

## VoiP servers and proxys

-   {{< wp "FreeSWITCH" >}} is a  telephony platform that lie between
    a softphone and a PBX or a carrier-class softswitch.
    [FreeSwitch Wiki
    ](https://freeswitch.org/confluence/display/FREESWITCH/FreeSWITCH+Explained) and
-   {{< wp "OpenSER" >}} now named [Kamailio](http://www.kamailio.org/) (GPL)
    is a SIP proxy server, call router, and user agent registration
    server. It is a fork from __SER__ in 2004.
    [Kamailo has a Debian repository
    ](http://www.kamailio.org/wiki/packages/debs).
-   [OpenSIPS](http://www.opensips.org/) (GPL)
    is a fork from  OpenSER, it is also a SIP Registrar server,
    Location server, Proxy server and Redirect server; gateway to
    SMS/XMPP; .
-   [RTPProxy](http://www.rtpproxy.org) (GPL) is a relay
    for Real-time Transport Protocol (RTP) media streams.
    It can work together with  SIP Express Router (SER),
    OpenSIPS,  Kamailio, Sippy B2BUA.
-   [Sippy B2BUA](https://github.com/sippy/b2bua) (GPL)
    is a RFC3261-compliant Session Initiation Protocol (SIP)
    Back-to-back user agent (B2BUA) server software.  Unlike a SIP
    proxy server, which only maintains transaction state, the B2BUA
    maintains complete call state and participates in all call
    requests, so it can perform accurate call accounting, fail over
    call routing etc.  Unlike PBX-type solutions such as Asterisk for
    example, the B2BUA doesn't perform any media relaying or
    processing.
-   {{< wp "SIP Express Router" >}} (GPL) is a SIP server, SIP registrar,
    proxy or redirect server. It is packaged in Debian.
-   The [SIP Router Project](http://sip-router.org/)
    is the common development framework for SER and Kamailio.

### Asterisk
-   {{< wp "Asterisk" >}} is a complete PBX in software.
    Asterisk does voice over IP in four protocols, and can interoperate
    with almost all standards-based telephony equipment.
    Asterisk uses the {{< wp "Inter-Asterisk eXchange" >}} or __IAX2__ protocol.
-   [Asterisk Home](http://www.asterisk.org/),
    [Asterisk Wiki](https://wiki.asterisk.org/wiki/display/AST/Home),
    [vo-ip.org: Asterisk](http://www.voip-info.org/wiki/view/Asterisk).
-   [archWiki: Asterisk](https://wiki.archlinux.org/index.php/asterisk)
-   [Asterisk page](http://voip-info.org/wiki/index.php?page=Asterisk)
    at [Asterisk channels](http://voip-info.org/wiki-Asterisk+channels)
    at [voip-info.org](http://voip-info.org)
-   [asterisk tutorials](http://www.asteriskguru.com/tutorials/) from
    [asteriskguru.com](http://www.asteriskguru.com/)
-   [Getting started with asterisk
    ](http://www.automated.it/guidetoasterisk.htm) by Andy Powell
    _2003_
-   [voip-info](http://voip-info.org/wiki/index.php) gives a list of
    [Asterisk hardware
    ](http://www.voip-info.org/wiki/view/Asterisk+hardware).
    The classical digium fxo X100P is no longer distributed,
    but there are a lot of
    [X100P clones
    ](http://www.voip-info.org/wiki/view/X100P+clone)


## Sip Test/Administration tools
-   [SIPp](http://sipp.sourceforge.net/) (GPL) is a a performance
    testing tool for the SIP protocol. it is packaged in the debian
    package _sip-tester_.
-   [sipsak](http://sipsak.org/) (GPL) is a small command line tool
    that can be used for some simple tests on SIP applications and
    devices.

## Voip clients
_mainly sip clients_

-   <a name="blink"></a>[Blink](http://icanblink.com/) (either open
    source or shareware)
    a python/QT Linux and windows, or python/Cocoa Mac OS X, sip client
    with instant messaging, OTR support, file transfer and multi-party
    conferencing, remote desktop sharing using RFB protocol (VNC), and
    SIMPLE presence.
-   [Ekiga](http://www.ekiga.org/) previously known as *Gnomeeting* a
    sip and H.323 compatible videoconferencing and VOIP/IP-Telephony
    application. The documentation is in
    [Ekiga Wiki](http://wiki.ekiga.org/)
-   {{< wp "Empathy_(Software)"  "Empathy" >}} (GPL) is an instant messaging
    client which supports text, voice, video, file transfers, and a
    large inter-application communication nearly identical to pidgin
    but including SIP. It is written in C against gnome libraries, so
    it has importants Gnome dependencies. See
    {{< iref "xmpp#empathy" "Empathy in my xmpp page" >}}.
-   The [eZuce SRN](http://srn.ezuce.com/) is a distributed
    collaboration system for research community.
-   [Linphone](http://www.linphone.org/) (GPL)
    is an audio and video GTK+ SIP client.  linphone takes 21M
    resident/15M shared; it is comparable with twinkle.  There is also
    a console client and an android platform build.  `linphonec` that
    uses only 7M resident/5M shared.
-   [Minisip](http://www.minisip.org/) (LGPL for the libraries, GPL
    for the application) User Agent running on Linux.
-   {{< wp "Pidgin_(software)"  "Pidgin" >}} (GPL)
    is a multi-platform instant messaging client for many commonly
    used instant messaging protocols _(but not yet SIP!)_. It is
    written in C, Python, Perl. See
    {{< iref "xmpp#pidgin" "Pidgin in my xmpp page" >}}.
-   {{< wp "Mumble" >}} (BSD License) is a voice chat application for groups.
    It is primarily intended for gaming.
-   [w:QuteCom](GPL) _[QuteCom Home](http://www.qutecom.org/)_
    previously _Wengophone_ is a sip client written in C++ with Qt
    lybraries, available on linux, windoze, and MacOs. It is packaged
    on Debian and Ubuntu.  It pretends to support also the xmms
    protocol and allows video-calls.  The front end is build with QT
    without extra KDE dependencies.<br /> The _meager_ documentation
    is in the [QuteCom Wiki](http://trac.qutecom.org/wiki).  Qutecom
    take 60M Resident/32 shr, 38M when disabling video, even before
    the first call, quite heavy compared to the 20M of twinkle.<br />
    Qutecom has kept from Wengophone some features that push you to
    connct with one provider, and make mainly landlines and mobile
    calls.<br /> The configuration interface is quite disappointing,
    you have to configure a main sip accounts, and add some alternates
    accounts for other protocols,wich are at a sub level of the main
    account. There is no way to enter a firewall traversing option, or
    simply set a stun server, but editing the advanced
    configuration. Very few is configurable even for sip, and still
    less for other protocols. I have been able to register on some of
    my accounts, but it refuses some others. And some of my jabber
    contacts, appears on-line, some others don't, even if they are
    online. So I renounced to use this version 2.2 from 2010.
-   [sflphone](http://www.sflphone.org/) (GPL) sip and IAX2  client for
    linux.
-   [Twinkle](http://twinkle.dolezel.info/)
    soft phone for VOIP using SIP protocol. It has a light interface not depending
    of any desktop, even if it can integrate with Kde. It takes 20M
    Resident/15M shared.
    -   Wikipedia {{< wp "Twinkle (software)" >}}

## Alt Open source Protocols
-   {{< wp "Mumble" >}} (BSD License) Mumble is a voice over IP (VoIP)
    application written in C++/QT primarily designed for use by gamers
    and is similar to programs such as TeamSpeak.  It features
    encrypted communication encoded in Opus with high sound quality
    and low latency.  It uses the
    {{< wp "Interactive Connectivity Establishment" >}} (ICE) protocol.
    -   [Mumble Home](https://wiki.mumble.info/wiki/Main_Page).
    -   [GitHub - Mumble](https://github.com/mumble-voip/mumble)
    -   {{< wp "TeamSpeak" >}} (proprietary, Freeware)
        is a VoIP  application for audio conference.

## sip registrars and Public Switched Telephone Network gateways

-   sip registrars and PSTN gateways:
    [directcentrex.com](http://www.directcentrex.com/)(PSTN),
    [FreeWorldDialup](http://www.freeworlddialup.com),
    [SipPhone](http://www.sipphone.com/)(PSTN) more known as
    [Gizmo Project](http://www.gizmoproject.com/) _now bought by Google_
    [voipgate.co](http://www.voipgate.com)(PSTN),
    [voipuser.org](http://www.voipuser.org/) (uk PSTN)
    [sipgate.com](http://www.sipgate.com)(us PSTN),
    [sipgate.co.uk](http://www.sipgate.co.uk)(uk PSTN),
    [www.voipstunt.com](http://www.voipstunt.com/en/)(PSTN, many free
    destinations),
    {{< wp "SIP_Broker" >}},
-   A list of SIP provider prefixes, as well as SIP providers,
    can be found in the [Provider WhitePage
    ](http://www.sipbroker.com/sipbroker/action/providerWhitePages)

# Video and voice
-   <a name="discord"></a>{{< wp "Discord_(software)"  "Discord" >}} (proprietary)
    is a proprietary freeware VoIP application designed for
    gaming communities. The multi-platform Discord client is built
    on the Electron framework. It allows voice calling, video calling
    and screensharing, text messaging, media and files.

    There are paid addons and gadgets.
    -   [Discord Home](https://discord.com/) has a web frontend to Discord.
-   <a name="jami"></a>[Jami (previously Gnu Ring)](https://jami.net/) (GPL)
    is a secure and distributed voice, video, file sharing and chat communication
    platform that replaced _sflphone_. It supports SIP, IAX2, RTP,
    STUN, SRV and accept many codecs including {{< wp "Opus" >}}.  It features
    a daemon and desktop clients, and can output to pulseaudio.
    On Linux Desktop clients for gnome, and kde  are available. The
    gnome version is in Debian and Ubuntu under the name _ring_ until stretch (debian 8)
    and from buster (debian 9) the package is named _jami_.
    There are also clients for  OS X, Windows, Android, iOS
    -   {{< wp "Ring_(software)"  "Wikipedia: Ring" >}}.
    -   [Jami repository](https://git.jami.net/savoirfairelinux/ring-project/)
    -   [Jami Wiki](https://git.jami.net/savoirfairelinux/ring-project/wikis/home)

-   {{< iref "xmpp#tox" "Tox" >}} (GPL)
    is a Voice, video, instant messaging, file transfers client it is
    {{< iref "xmpp#tox" "in the XMPP section" >}}.
    It uses its {{< iref "xmpp#tox" "Tox protocol" >}}
    and has suport for {{< wp "Opus" >}} codex.

## Jitsi {#jitsi}
<!-- See [[file:/share/sync_folders/misc/mznotes/content-org/weblinks/network.org::#jitsi][Liste d'instances Jitsi]] -->
{{< wp "Jitsi" >}} (apache License) is a VoIP, videoconferencing, instant messaging
application for Windows, Linux, Mac OS X and Android written in Java. It supports XMPP
including {{< iref "xmpp#jingle" "Jingle" >}},
{{< iref "xmpp#jingle" "OTR encryption" >}} and other proprietary IM protocols like
{{< wp "Microsoft Notification Protocol" >}} _MSN, .NET, or Live_;
{{< wp "OSCAR_PROTOCOL" "OSCAR" >}},_AIM/ICQ/MobileMe_, the {{< wp "SIMPLE" >}}
_IM and presence protocol suite based on SIP_, {{< wp "Facebook Messenger" >}}
and voice/video conferencing (SIP/RTP/SRTP/ZRTP).

_Jitsi_ supports {{< iref "#cusax" "CUSAX" >}} and has built-in IPv6, NAT traversal and
DNSSEC.
-   [Jitsi Home](https://jitsi.org/)
-   [Jitsi Meet](https://jitsi.org/Projects/JitsiMeet) (apache License)
    is the VideoConferencing application of Jitsi. It is a WebRTC JavaScript
    application the communication is Encrypted by default, and provide HD audio with
    Opus. The desktop application is packaged for Debian/Ubuntu. There is a Web
    application that works in a WebRtc able Browser.
-   [Docker container of Jitsi-Meet
    ](https://hub.docker.com/r/robertoandrade/jitsi-meet/).
-   [meet.jit.si](https://meet.jit.si/) the reference Jitsi _irish_server.
-   [List of Jitsi Meet instances](https://framatalk.org/accueil/en/info/)
    from [Framatalk](https://framatalk.org/).

## Proprietary protocols
I just give a pointer to most popular VoIP solutions. We should prefer
open source.

-   {{< wp "Skype" >}} or [Skype Home Page](http://www.skype.com/)
    P2P telephony and videoconferences is a closed proprietary
    protocol,
    There are [numerous reasons to prefer an open source protocol
    ](https://wiki.ubuntu.com/SkypeEthics)
    considered only the  {{< wp "Skype#Privacy"  "Skype lack of privacy" >}}
    and its use for censorship. Morever skype pretend to have
    encryption but {{< wp "Skype#Security_and_privacy"  "is not secure" >}} and it
    {{< wp "Global_surveillance_disclosures_(2013–present)"  "has been shown" >}}
    that that agencies such as the NSA and the FBI have
    the ability to eavesdrop on Skype.
    <br />
    But we can be pushed to use it to communicate
    with skype addicts, _at least until they give up their addiction_,

    -   [Ubuntu Community: Skype
        ](https://help.ubuntu.com/community/Skype),
        [troubleshoot skype
        ](https://help.ubuntu.com/community/SkypeTroubleshooting)
    -   [Debian Wiki: Skype](https://wiki.debian.org/skype)


<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
