---
title: XMPP
---

See also {{< iref "irc" "IRC" >}},
{{< iref "social_networks" "Social Networks" >}},
{{< iref "sip" "SIP" >}} and
{{< iref "xmpp" "P2P" >}}.

-----------------

# References
-   Wikipedia: {{< wp "Xmpp"  "Extensible Messaging and Presence Protocol (Xmpp)" >}},
    {{< wp "Comparison of instant messaging protocols" >}},
    {{< wp "Comparison of instant messaging clients" >}},
    {{< wp "Comparison of XMPP server software" >}},
    {{< wp "Instant messaging" >}},
    {{< wp "Jingle (protocol)"  "Jingle Protocol" >}},
    {{< wp "SIMPLE_(instant_messaging_protocol)"  "Simple" >}}
    an instant messaging (IM) and presence protocol suite based on SIP.
-   [ArchWiki: List of instant messaging software
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Instant_messaging)
-   [XMPP Internet of Things](http://www.xmpp-iot.org/)
    _The Internet of Things (or IoT) is what we get when we connect
    Things, that are not operated by humans, to the Internet._
    -   [XMPP.org introduction to Internet of Things
        ](https://xmpp.org/uses/internet-of-things.html).
-   <a name="jabberfr"></a>[jabber.fr](http://www.jabberfr.org/):
    -   [Jabber.fr wiki (french)](http://wiki.jabberfr.org/)
        with plenty of _french_ jabber documentation, but quite outdated.<br />
    -   [Presence service](http://presence.jabberfr.org/)
    -   [Passerelles](http://wiki.jabberfr.org/Passerelles) _these bridges are mainly
        with non longer used or deprecated protocols._
    -   [Pages de la Catégorie:Fonctionnalité Jabber
        ](http://wiki.jabberfr.org/Cat%C3%A9gorie:Fonctionnalit%C3%A9_Jabber)
    -   [MUC](http://wiki.jabberfr.org/MUC)
    -   [Jwchat tutorial](http://wiki.jabberfr.org/JWChat)
    -   [linuxFR - xmpp](http://linuxfr.org/sections/xmpp)
-   The proprietary {{< wp "Yahoo! Messenger" >}} now closed was handled by many
    open source client.
-   XMPP is used in {{< wp "Distributed social network" >}} Wikipedia gives a
    {{< wp "Comparison of software and protocols for distributed social networking" >}}
-   [MucSearch](https://search.wensley.org.uk/) a conference web search service.
-   {{< wp "SIMPLE_(instant_messaging_protocol)"  "SIMPLE" >}} is IM over sip,
    ietf has [rfc 3428 SIP Extension for Instant Messaging
    ](http://www.ietf.org/rfc/rfc3428.txt)

## XMPP Specification
[XMPP Standards Foundation](http://www.xmpp.org/ ) references all xmmp standards and
extensions.


-   [XMPP software : Clients Servers Libraries Projects](http://xmpp.org/software)

[Technology Overview of XMPP](https://xmpp.org/about/technology-overview.html)
present the specifications of XMPP.

The core specification is defined in RFC:
    [RFC 6120 - XMPP Protocol Core](https://tools.ietf.org/html/rfc6120),
    [RFC 6121 - XMPP Instant Messaging and Presence](https://tools.ietf.org/html/rfc6121)
    [RFC 7622 - XMPP Address Format](https://tools.ietf.org/html/rfc7622),
    [RFC 7590 - Use of TLS in XMPP](https://tools.ietf.org/html/rfc7590).

It is complemented by extensions whose full list is in
the [table of XMPP extensions](https://xmpp.org/extensions/)


These extensions can be divided in core extensions,
{{< iref "#xmpp_muc" "MUC Multi user Chat" >}},
{{< iref "#xmpp_jingle" "Jingle multimedia messaging" >}},
{{< iref "#pubsub" "pubsub publish-subscribe functionality" >}},
{{< iref "#bosh" "BOSH Bidirectional-streams Over Synchronous HTTP" >}}.

And the extensions for secure messaging in {{< iref "#openpgp" "OpenPGP" >}},
{{< iref "#omemo" "OMEMO" >}},
{{< iref "#otr" "OTR" >}}.


Core extensions can extend the RFCS, some core extensions are:
-   [XEP-0280: Message Carbons](https://xmpp.org/extensions/xep-0280.html)
    In order to keep all IM clients for a user engaged in a conversation, outbound
    messages are carbon-copied to all interested resources. It allows to be easily
    simultaneously connected from many clients with the same account.  It is provided by
    most of the recent clients from this page.  _but pidgin need the plugin carbons_.
-   [XEP-0313: Message Archive Management](https://xmpp.org/extensions/xep-0313.html)
    and [XEP-0441: Message Archive Management Preferences
    ](https://xmpp.org/extensions/xep-0441.html)
    present in conversations, converse.js, gajim, xabber.
-   [XEP-0357: Push Notifications](https://xmpp.org/extensions/xep-0357.html).
    works with chatsecure, conversation,

### MUC - Multi user Chat{#xmpp_muc}
MUC brings IRC like  functionalities to XMPP, and allow multiple XMPP users to exchange
messages in the context of a room or channel.

It is described in
[MUC overview -xmpp.org](https://xmpp.org/about/technology-overview.html#muc)
Specification is in the following XEPs:
-   [XEP-0045: Multi-User Chat](https://xmpp.org/extensions/xep-0045.html)
-   [XEP-0249: Direct MUC Invitations](https://xmpp.org/extensions/xep-0249.html)
-   [XEP-0272: Multiparty Jingle](https://xmpp.org/extensions/xep-0272.html)

Most servers and Clients support MUC. The message encryption in MUC, is a more complex
and is only implemented in few clients.

### Jingle{#xmpp_jingle}}
<a name="jingle"></a>{{< wp "Jingle (protocol)"  "Jingle Protocol" >}}
is an extension to XMPP which adds peer-to-peer (P2P) session
control (signaling) for multimedia.  Interactions such as in voice
over IP (VoIP) or videoconferencing communications, or also for
p2p file transfer.  Jingle is supported by Xmpp software based on
telepathy like empathy, minirc; software base on it like pidgin,
Coccinella, Gajim, Macabber (file transfer only),
Pidgin, Psi, Jabbin, Tapioca. It is also supported by telephony
software like {{< wp "Yate_(telephony_engine)"  "Yate" >}} or
{{< wp "Asterisk_(PBX)"  "Asterisk" >}}.

It is defined in [several XEP documents
](https://xmpp.org/about/technology-overview.html#jingle)
(also listed on Wikipedia: {{< wp "Jingle (protocol)" >}}):

-   [XEP-0166: Jingle](http://www.xmpp.org/extensions/xep-0166.html)
    defines a framework for initiating and managing peer-to-peer
    multimedia sessions,
-   [XEPidiculously-0167: Jingle Audio via RTP
    ](http://www.xmpp.org/extensions/xep-0167.html)
    defines methods for negotiating Jingle audio sessions that use the Real-time
    Transport Protocol (RTP) for media exchange.  provided by jitsi, pidgin.
-   [XEP-0234: Jingle File Transfer](http://xmpp.org/extensions/xep-0234.html)
-   [XEP-0176: Jingle ICE-UDP Transport Method
    ](https://xmpp.org/extensions/xep-0176.html)
-   [XEP-0177: Jingle Raw UDP Transport Method
    ](https://xmpp.org/extensions/xep-0177.html)
-   [XEP-0181: Jingle DTMF](https://xmpp.org/extensions/xep-0181.html)
-   [XEP-0272: Multiparty Jingle](https://xmpp.org/extensions/xep-0272.html)

### BOSH {#bosh}
[BOSH  “Bidirectional-streams Over Synchronous HTTP”
](http://xmpp.org/about-xmpp/technology-overview/bosh/)
is a technology for two-way communication over the HTTP. BOSH has been used mainly as a
transport for traffic exchanged between Jabber/XMPP clients and servers. BOSH is more
bandwidth-efficient and responsive than AJAX.  Bosh is supported by Xmpp servers and
standalone XMPP connection managers;[Which BOSH Server Do You Need?
](http://metajack.im/2008/09/08/which-bosh-server-do-you-need/)
compare these two options.

BOSH is defined in two XEP specifications:
-   [XEP-0124: Bidirectional-streams Over Synchronous HTTP
    ](https://xmpp.org/extensions/xep-0124.html)
-   [XEP-0206: XMPP Over BOSH](https://xmpp.org/extensions/xep-0206.html)

The following clients have support for BOSH
{{< iref "#converse" "Converse" >}},
{{< iref "#gajim" "Gajim" >}},
{{< iref "#jwchat" "JWChat" >}},
{{< iref "#jsxc" "jsxc" >}},
{{< iref "#movim" "Movim" >}},
{{< iref "#pidgin" "Pidgin" >}},
{{< iref "#swift" "Swift" >}},
{{< iref "#xmpp4js" "xmpp4js" >}} and Soashable,
[Adium](https://adium.im/) _client for Mac OS X_.

The following XMPP servers include built-in support for BOSH:
{{< iref "#ejaberd" "ejabberd" >}},
Jabber XCP, M-Link, MongooseIM,
{{< iref "#openfire" "Openfire" >}},
{{< iref "#prosody" "Prosody" >}},
{{< iref "#tigasexmppserver" "Tigase" >}}.

### PubSub
[PubSub](https://xmpp.org/about/technology-overview.html#pubsub)
is an extension for generic publish-subscribe functionality.It enables
to publish information on nodes (topics) at a pubsub service.
An event notification is then broadcasted to all
entities that have subscribed to the node.

PubSub is defined in several specifications:
-   [XEP-0060: Publish-Subscribe](https://xmpp.org/extensions/xep-0060.html)
-   [XEP-0163: Personal Eventing Protocol](https://xmpp.org/extensions/xep-0163.html)
-   [XEP-0248: PubSub Collection Nodes](https://xmpp.org/extensions/xep-0248.html)

### Server compliance test

-   [XMPP Compliance Tester](https://compliance.conversations.im/)
-   [IM Observatory](https://xmpp.net/) evaluate the security of servers.

See also [How to choose you Jabber service?
](https://mov.im/?blog/debacle@movim.eu/1646bb0e-8d18-4fb9-8b1a-46a1b40e0143).

## Xmpp HowTo, comparison
-   [Secure Chat Guide](https://securechatguide.org/):
    [Decentralized Apps](https://securechatguide.org/decentralizedapps.html),
    [Centralized Apps](https://securechatguide.org/centralizedapps.html),
    [Peer to Peer Apps](https://securechatguide.org/p2papps.html)
    guides and detailed information on secure messaging apps for Android, iOS, Windows,
    Mac and Linux.
-   [Better than WhatsApp — Free Software Foundation India
    ](https://fsf.org.in/article/better-than-whatsapp/).
-   [Messagerie chiffrée. Pourquoi pas XMPP ? — echolib
    ](https://www.echolib.space/utiliser-messagerie-chiffree-xmpp)
-   [Secure Messaging Apps Comparison | Privacy Matters
    ](https://www.securemessagingapps.com/)
    Aclear table of features, but many apps are missing; XMPP is not even mentioned.

# Secure messaging
Secure Messaging is an essential feature of IM, but these days it is a mainly used as a
selling point, to make you adopt some proprietary protocol. So you have to convince all
your friends to buy the same product, or to buy yourself all the products owned by one
of your friend, and buy also a more powerfull mobile phone to host these multiple
software. But even if you do it, how can you use the _multi user chat_ or _group chat_
that is proposed by these software?

Imagine you have to have the same brand of phone to call somebody, the
same email software to read her emails....

To ensure interoperability there is presently few protocols,
{{< iref "#fish" "FiSH" >}} the older, obsolete security,
{{< iref "#openpgp" "OpenPGP" >}},
{{< iref "#omemo" "OMEMO" >}},
{{< iref "#otr" "OTR" >}}.  Supported by a fair number of clients, but now superseded by
{{< iref "#omemo" "OMEMO" >}}.

I give here also some other open source systems, but even if the
protocol is open source, it is used only by one product.

The first level of security is to use a
{{< wp "Transport_Layer_Security" "TLS" >}} connection, that avoid (if correctly
authentified) that your data is stolen during transport. But to be
secure it should provide {{< wp "Forward secrecy" >}}, and avoid
{{< wp "Man-in-the-middle attack" >}} by technics like
{{< wp "HTTP Public Key Pinning" >}} (HPKP).

But if it can protect again an occasional hacker taht intercept your communication, it
is of no use when the hacker is member or beak into the server organisation, or is as
powerful as to convince or force the provider to give its data. And of course it is of
no use whent the data is stolen at one end of the communication, which is so easy with
mobile devices.

-   Wikipedia {{< wp "Secure instant messaging" >}}, {{< wp "Secure communication" >}},
    {{< wp "Mobile security" >}},
    {{< wp "Deniable authentication" >}}, {{< wp "forward secrecy" >}},
    {{< wp "Comparison_of_instant_messaging_clients#Secure_messengers"  "Secure messengers" >}}
-   [End-to-End XMPP Cryptographic Protocol Desiderata
    ](https://developer.pidgin.im/wiki/EndToEndXMPPCrypto) from
    [Pidgin developer Wiki](https://developer.pidgin.im/wiki/).
-   [Propublica: Privacy Tools - The Best Encrypted Messaging Programs
    ](https://www.propublica.org/article/privacy-tools-the-best-encrypted-messaging-programs)
    has a [comparison of security features of secure messaging tools
    ](http://projects.propublica.org/graphics/privacy-tools).

For secure messaging we can expect the following features:

-   encrypted communications between all the links in the
    communication path.
-   end-to-end encryption, i.e the provider does not have access
    to keys.
-   authentication of correspondents e.g. by comparing key
    fingerprints.
-   {{< wp "forward secrecy" >}} i.e. having past communications secure if the
    encryption keys are stolen.
-   open source with documented security design and
    recent independent {{< wp "security audit" >}}.
-   no log or store any information  regarding message contents,
    senders and destination, timestamps, sessions or events.
-   Do not rely on a central authority for the relaying of messages
    ({{< wp "decentralized computing" >}}).



## OTR or _Off-the-Record Messaging_ {#otr}
{{< wp "Off-the-Record Messaging" >}} (GPL) Off the Record _(OTR)_ Messaging allows you
to have private conversations over instant messaging by providing encryption,
{{< wp "Deniable authentication" >}}, perfect {{< wp "forward secrecy" >}}.

OTR allow instant messaging, secure file transfer, the plugin supports multiple OTR
conversations with the same buddy who is logged in at multiple locations. MUC is not yet
supported.

-   [otr.cypherpunks: OTR Protocol Home](https://otr.cypherpunks.ca/)
-   [OTR.im: OTR user Home](https://www.otr.im/).
-   [XEP-0364: Current Off-the-Record Messaging Usage
    ](https://xmpp.org/extensions/xep-0364.html)
-   [XEP-0378: OTR Discovery](https://xmpp.org/extensions/xep-0378.html)
-   [OTR version 4 draft](https://bugs.otr.im/otrv4/otrv4)

We can use any server using TLS for OTR messaging. Some may offer more security
[jabber.otr.im](https://www.otr.im/chat.html) offers a free and secure server, or even a
[Tor hidden service: ](https://www.torproject.org/docs/hidden-services.html.en) their
server uses SSL/TLS, but the specific feature is that it forces communication to be OTR
encrypted, thus cleartext messages between clients is impossible. The server uses full
disk encryption taht will protect all data if the server is powered off, logging is
completely disabled on the Jabber server, even error logs.

In case of seizure if the server is kept online, the disk encryption is useless, and one
can still see your username and SHA1 hash of the password, your vcard _if you did
provide one_, your ip address if you don't use TOR, the encrypted content of offline
message and their destination and timestamp, and your roster including Jabber address of
contacts and their name and group if they are present. What is securely hidden is
message content as they are end-to-end encrypted by OTR, and they have no logs even you
connection timestamps.

You can inspect what provide your server to look if it offers an comparable level of
protection, it seems that for a higher security you have to go to a P2P connection that
avoid completely the server aspects; but it is beyond Xmmp, and you will miss many
features.


The main drawback of OTR compared to {{< iref "#omemo" "OMEMO" >}} is the lack of
offline delivery.

{{< iref "#openpgp" "OpenPGP" >}} has  offline delivery but not
 {{< wp "forward secrecy" >}} provided by OTR.

{{< iref "#omemo" "OMEMO" >}} meet the three  requirements of
{{< wp " forward secrecy" >}}, offline delivery, and
{{< wp "Deniable authentication" >}}.

For Linux use of OTR see also the
[EFF - Surveillance Self-Defense](https://ssd.eff.org/) guide
[How to: Use OTR on Linux](https://ssd.eff.org/en/module/how-use-otr-linux).

OTR is supported by many messaging clients, either a native
support or through plugin. For Linux native support we have:

-   {{< iref "#bitlbee" "Bitlbee" >}} since 3.0.
-   {{< iref "sip#blink" "Blink" >}} a sip client with messaging.
-   {{< iref "#cryptocat" "Cryptocat" >}} protocol _(not open
    XMPP)_ uses OTR for webbrowsers.
-   {{< iref "sip#jitsi" "Jitsi" >}} -  Video Calls
    and Chat.
-   {{< wp "Kopete" >}}  multi-protocol messaging for KDE.
-   {{< iref "#kadu" "Kadu" >}} _obsolete_
-   {{< iref "#mcabber" "Mcabber" >}}
-   [LeechCraft](https://leechcraft.org/) _modular live environment_ for Linux, Windows,
    OSX.
-   {{< iref "#profanity" "Profanity" >}}
-   {{< iref "#psi" "PSI+" >}}

The following Linux clients have OTR support through a plugin:

-   [bitlbee-otr](https://wiki.bitlbee.org/bitlbee-otr)
    for {{< iref "#bitlbee" "Bitlbee" >}}
-   [Off-the-Record Encryption plugin
    ](https://trac-plugins.gajim.org/wiki/OffTheRecordPlugin)
    through [gajim-otr](https://github.com/python-otr/gajim-otr)
    for {{< iref "#gajim" "Gajim" >}} _alpha plugin_.
-   [HexChat-OTR](https://github.com/TingPing/hexchat-otr)
    for {{< iref "irc#hexchat" "HexChat" >}}.
-   [Irsii-OTR](https://github.com/cryptodotis/irssi-otr/) for
    {{< iref "irc#irssi" "irsii" >}}.
-   [pidgin-OTR](https://bugs.otr.im/plugins/pidgin-otr)
    for {{< iref "#pidgin" "Pidgin" >}}.
-   {{< iref "#poezio" "poezio" >}}.
-   {{< iref "#tkabber" "Tkabber" >}}
-   [Weechat-OTR](https://github.com/mmb/weechat-otr) for
    {{< iref "irc#weechat" "Weechat" >}}.


Windows and Mac OSX clients

-   Adium  multiprotocol client for Mac OSX.
-   Blink SIP  Mac OSX client
-   {{< wp "climm" >}} IRC for Windows, OSX, and unix.
-   {{< iref "#kadu" "Kadu" >}} Unix Windows and Mac OSX
    gadu-gadu and Xmpp client.
-   Textual 5 (OS X)
-   {{< iref "#tkabber" "Tkabber" >}}

Android and IOS clients:

-   {{< iref "#beem" "Beem" >}}
-   {{< iref "#chatsecure" "Chatsecure" >}}
-   {{< iref "#conversations" "Conversations" >}}
-   {{< iref "#xabber" "Xabber" >}}  GPL Xmpp client for
    Android.


## OMEMO {#omemo}
[OMEMO](https://conversations.im/omemo/) is an XMPP Extension Protocol (XEP)
for secure multi-client end-to-end encryption. It features
[Future and Forward Secrecy](https://whispersystems.org/blog/advanced-ratcheting/)
and deniability, while allowing you to keep the benefits of
[message synchronization and offline delivery](http://conversations.im/#xmpp).

-   [LWN article: A look at the OMEMO protocol](https://lwn.net/Articles/691315/)
-   [Getting started with OMEMO
    ](https://gist.github.com/iNPUTmice/e3fe475752e39b40ea87ae5ed73b3e01).
-   [XEP-384 - OMEMO specification](https://xmpp.org/extensions/xep-0384.html).

There is a comparison of features of OTR {{< iref "#openpgp" "OpenPGP" >}}
and OMEMO on the [OMEMO Home page](https://conversations.im/omemo/).

The main drawback of OMEMO is the lack of support by some popular clients _as far as year
2021_  the list is given on the page [Are we OMEMO yet?](https://omemo.top/).

Begining 2021 this list include for Linux,
-   for graphical clients support for:
    {{< iref "#dino" "Dino" >}},
    {{< iref "#jsxc" "jsxc" >}},
    {{< iref "#gajim" "Gajim" >}}
    through the plugin [gajim-omemo](https://github.com/omemo/gajim-omemo),
    {{< iref "#pidgin" "pidgin" >}} through the plugin _lurch_,
    {{< iref "#psi" "PSI" >}},
    {{< iref "#psi_plus" "PSI+" >}},
    {{< iref "#salutatoi" "Salut à Toi" >}},
-   Web clients:
    {{< iref "#xabber_web" "Xabber for Web"  >}},
    {{< iref "#converse" "Converse.js" >}}
-   Console clients:
    {{< iref "#pidgin" "Finch" >}} (pidgin curse)  through the plugin _lurch_
    {{< iref "#poezio"  >}} _in progress_,
    {{< iref "#profanity" "profanity" >}},
    {{< iref "#salutatoi" "primitivus" >}},

For mobiles
-   ios client
    {{< iref "#chatsecure" "chatsecure" >}}
-   android client
    [blabber](https://blabber.im/),
    {{< iref "#conversations" "Conversations" >}} and many forks
    {{< iref "#zom" "Zom" >}},

On windows there is _Miranda_, {{< iref "#psi" "PSI" >}},
{{< iref "#pidgin" "pidgin" >}}, {{< iref "#gajim" "Gajim" >}}

On OS X _Adium_, {{< iref "#psi" "PSI" >}},{{< iref "#pidgin" "pidgin" >}},
{{< iref "#gajim" "Gajim" >}}.

## OpenPGP {#openpgp}

{{< wp "OpenPGP" >}} for XMPP was first decribed by
[XEP-0027: Current Jabber OpenPGP Usage
](http://www.xmpp.org/extensions/xep-0027.html) which is now
obsolete. There is a new experimental draft
[XEP-0373: OpenPGP for XMPP
](https://xmpp.org/extensions/xep-0374.html).

While {{< iref "#openpgp" "OpenPGP" >}} can be used for Xmpp, {{< iref "#OTR" "OTR" >}}
or {{< iref "#omemo" "OMEMO" >}} are more secure as they provide
{{< wp "forward secrecy" >}}, and {{< wp "deniability" >}} that is missing to OpenPGP,
OTR is also easier to use; on the other hand OpenPGP is a well known and simpler method
of asymetric encryption, and it can be applied easily to offline messages.

The IM clients supporting OpenPGP are

-   {{< iref "#conversations" "Conversations" >}}
    for Android,
    {{< iref "#mcabber" "Mcabber" >}},
    {{< iref "#pidgin" "Pidgin" >}}
    with the [GPG/OpenPGP Plugin for Pidgin
    ](https://github.com/segler-alex/Pidgin-GPG/wiki),
    {{< iref "#poesio" "poesio" >}},
    {{< iref "#profanity" "profanity" >}},
    {{< iref "#psi" "PSI" >}}, Gabber, Miranda ICQ
    (IRC/ICQ client for Windows),
    {{< iref "#tkabber" "Tkabber" >}},
    [wija](http://www.media-art-online.org/wija/) _no more developed
    since 2007_. Most are referenced on the [GPG software list
    ](https://www.gnupg.org/related_software/swlist.html).

You can find an _HOW TO_ in [Encrypted instant messaging with
Jabber and GnuPG](https://box.matto.nl/gnupgjabber.html).


# Xmpp public servers
-   [xmpp.net Public XMPP Server Directory](https://xmpp.net/directory.php)
    gives a  list of jabber servers by country,
    -   [IM Observatory](https://xmpp.net/) evaluate the security of servers.
-   [jabber.at: Public XMPP servers](https://list.jabber.at/) a larger list of servers.
-   [Cryptoparty list of secure jabber servers
    ](https://www.cryptoparty.in/connect/contact/jabber).
-   [jabber.org](https://www.jabber.org/) is the original XMPP service.  In 2010 the
    service was migrated to Isode's M-Link proprietary XMPP Server.
    -   [jabber.org FAQ](http://www.jabber.org/faq.html)
-   [jabber.apinc.org](http://jabber.apinc.org/) run the server
    {{< iref "#jabberfr" "jabber.fr" >}}
-   {{< wp "Movim" >}} run a jabber server, the domain of the obsolete xmpp client
    _jappix_ jappix.com is now handled by movim.
    -   [movim.eu](http://movim.eu)
-   [OTR.im](https://www.otr.im/chat.htm)
    offers a free and secure Jabber service nammed __jabber.otr.im__
    It is also possible to connect through our Tor hidden service.
    The server use SSL/TLS  and accept only
    {{< iref "#otr" "OTR encoded" >}} conversations.



# Xmpp  console clients

-   Wikipedia:
    {{< wp "Comparison of instant messaging clients" >}},
-   [Jabber.fr: Clients](http://wiki.jabberfr.org/Clients)
-   [xmpp.org: Clients](http://xmpp.org/xmpp-software/clients/)
-   [ArchWiki: xmpp console clients
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Console_6)
-   [ArchWiki: multiprotocol console clients
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Console_7)

-   [BarnOwl](https://github.com/barnowl/barnowl)
    Ncurses-based chat client with support for the Zephyr, Jabber,
    IRC, and Twitter protocols; forked and extended from the old Owl
    irc client. Seems to be no more maintained since 2019.
    -   [BarnOwl Wiki](https://barnowl.mit.edu/wiki)
-   [centerim](http://www.centerim.org/) is a ncurses IM client
    program that supports ICQ2000, Yahoo!, AIM, MSN, IRC and Jabber
    protocols. _centerim was in Debian but is no longer since wheezy._
-   {{< iref "#finch" "Finch" >}} the libpurple based client
    is in the {{< iref "#pidgin" "pidgin entry" >}}
-   {{< iref "irc#irssi" "Irssi" >}} support XMPP through a
    plugin, but if you want an Irssi like interface, and a more
    complete interface to XMPP you may prefer
    {{< iref "#profanity" "Profanity" >}} which support
    {{< iref "#omemo" "OMEMO" >}}.
-   <a name="emacs_jabber"></a>[jabber.el](http://emacs-jabber.sourceforge.net/)
    is an emacs Xmpp client. jabber.el support SSL and STARTTLS. It does not seem to be
    anymore developed, and OMEMO support is not even planed.

    -   [EmacsWiki JabberEl
        ](http://www.emacswiki.org/cgi-bin/wiki/JabberEl)
    -   [on-line jabber.el manual
        ](http://emacs-jabber.sourceforge.net/manual-0.8.0/).
    -   The stable version 0.8.0 is quite old _2009_ and you may want
        to install a more recent one either from ELPA or the
        [git repository](https://github.com/legoscia/emacs-jabber)
    -   [OTR support for jabber.el](https://github.com/legoscia/emacs-jabber-otr)
        _alpha stage and no commit since 2017_.

-   [jp](https://salut-a-toi.org/__b/doc/sat/jp/index.html)
    is the CLI frontend of {{< iref "#salutatoi" "Salut à Toi" >}}. With it you can send
    chat messages, share files, retrieve avatars, write blog entries, etc.
-   [Licq](http://licq.org/) (GPL)
    is a multiprotocol client supporting ICQ, MSN and XMPP.
    _no more maintained since 2014._
-   <a name="mcabber"></a>[Mcabber
    ](https://mcabber.com/)
    (GPL) by Mikael Berthe is a small Jabber console client that
    support ssl,  history logging, commands completion,   muc (multi
    user chat), external actions triggers
    [Xep 0146: client remote control
    ](http://xmpp.org/extensions/xep-0146.html); and encryption with
    {{< iref "#openpgp" "OpenPGP" >}} and
    {{< iref "#otr" "OTR (Off-the-Record Messaging)" >}}, but no OMEMO support.
    It uses a memory footprint of 13M res/8M shared.
    It that can connect only to one account.

    More documentation is in the:

    -   [Mcabber wiki](http://wiki.mcabber.com/).
        has documentation.
    -   [Mcabber wiki](http://wiki.mcabber.com/)
        list the supported XEP protocols.
    -   Mcabber has a long
        [list of plugins](http://wiki.mcabber.com/Modules.html)
    -   [Mcabber source repository](http://mcabber.com/hg/),
        [a mirror in GitHub](https://github.com/weiss/mcabber).

-   <a name="poezio"></a>[Poezio](https://poez.io/) {{< wp "Zlib License" >}}
    is a console XMPP client written in python Its main target is MUC
    (MultiUserChat). It support anonymous authentication, roster, one-to-one
    conversations, {{< iref "#otr" "OTR" >}}, {{< iref "#openpgp" "OpenPGP" >}},
    and {{< iref "#omemo" "OMEMO" >}} support is [in progress
    ](https://lab.louiz.org/poezio/poezio/-/issues/3280) _but don't seem to come-in
    quickly!_  through the plugin
    [poezio-OMEMO](https://lab.louiz.org/poezio/poezio-omemo).
    Poezio support only one account.
    Being a python3 client the memory footprints of poezio are quite heavy for a console
    client 37M res / 9.5M shr.
    -   [Poezio documentation](https://doc.poez.io/)
    -   Debian packages are provided by the
        [jabber.at apt repository
        ](https://jabber.at/p/apt-repository/).
-   <a name="profanity">[profanity](http://www.profanity.im) (GPL)
    is a C-ncurses console based client for XMPP,
    inspired by {{< iref "irc#irssi" "irssi" >}}.  It
    features XMPP chat services, including GoogleTalk and Facebook.
    {{< iref "#otr" "OTR encryption" >}},
    {{< iref "#openpgp" "OpenPGP" >}},
    {{< iref "#omemo" "OMEMO" >}},
    MUC (multi user chatroom), roster management with
    grouping, Desktop notifications via libnotify.  plugins in C,
    Python, Ruby, and Lua. Profanity take 27M res / 15M shr.
    Profanity is in debian.
    -   {{< wp "Profanity_(instant_messaging_client)"  "Wikipedia: Profanity" >}}
    -   [Profanity GitHub repo](https://github.com/boothj5/profanity)
    -   [Profanity user guide](http://www.profanity.im/userguide.html)

    -   [Profanity official plugins
        ](https://github.com/boothj5/profanity-plugins)
    -   [Profanity OMEMO plugin
        ](https://github.com/ReneVolution/profanity-omemo-plugin)
-   _primitivus_ is a console client for
    {{< iref "#salutatoi" "Salut à Toi" >}}
    the Debian package is _sat-xmpp-primitivus_.
-   {{< iref "irc#weechat" "Weechat" >}}
    has an
-   {{< iref "irc#weechat" "Weechat" >}} has an
    [xmpp plugin](https://github.com/weechat/scripts/blob/master/python/jabber.py)
    but it does not handle anonymous authentication nor chatrooms,
    but you can use a proxy like {{< iref "#bitlbee" "bitlbee" >}}
    or bitlbee-purple.
    You find it {{< iref "irc#weechat" "weechat on IRC section" >}}.
-   <a name="xmpp-client"></a>[xmpp-client](https://github.com/agl/xmpp-client)
    (BSD Licence) is a golang XMPP client with  {{< iref "#otr" "OTR" >}}support.
    {{< iref "#coyim" "coy.im" >}} is a fork of _xmpp-client_.

# Xmpp Graphical clients
_I don't mention client with heavy desktop dependencies
like_ gnome-jabber (gabber), gossip
_(said to be lightweight but need libgnome and all bonobo framework)_ ...

-   Wikipedia:
    {{< wp "Comparison of instant messaging clients" >}},
-   [Jabber.fr: Clients](http://wiki.jabberfr.org/Clients)
-   [xmpp.org: Clients](http://xmpp.org/xmpp-software/clients/)
-   [ArchWiki: xmpp graphical clients
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Graphical_clients)
-   [ArchWiki: multiprotocol graphical clients
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Graphical_4)


-   [ayttm](http://ayttm.sourceforge.net/) (GPL) is an instant
    messaging GTK+ client for AIM, Yahoo (with webcam support), MSN,
    jabber (including ssl and google talk), IRC, ICQ. _last release 2010, last commit
    2015 no longer in Debian since jessie._
    -   [ayttm git repo
        ](https://sourceforge.net/p/ayttm/git/ci/master/tree/)
-   <a name="coyim"></a>[coyIM](https://coy.im) (GPL)
    is a Go language / GTK3  xmpp client based on {{< iref "#xmpp" "xmpp-client" >}} and
    [otr3](https://github.com/twstrike/otr3) a Go implementation of the
    OTR 3 protocol.  {{< iref "#otr" "OTR" >}} is enabled by default, as Tor when it is
    available.  coyIM is in Debian. _very active development as far as 2021, OMEMO planed_
    -   [GitHub - coyim](https://github.com/coyim/coyim/).
-   <a name="dino"></a> [Dino](https://github.com/dino/dino)
    is a GTK+/Vala xmpp client with
    {{< iref "#omemo" "OMEMO" >}} support.
-   <a name="empathy"></a> [Empathy
    ](https://wiki.gnome.org/action/show/Apps/Empathy)
    is a messaging program which uses
    {{< iref "#telepathy" "Telepathy" >}} for
    protocol support and inherit from the large  Voice and Video
    protocol support from
    {{< iref "#telepathy" "Telepathy" >}},
    Look at {{< wp "Empathy_(software)"  "Wikipedia: Empathy" >}} for a
    full list of protocol, note that empathy support SIP and
    {{< wp "Jingle (protocol)"  "Jingle" >}} allowing Google Talk, on the other
    hand it lack the privacy support of Pidgin.  It is based on
    __gossip__ for the user interface, and inherit from gossip gnome
    dependencies. Nevetherless empathy just waiting idly is 35M
    Res/25M shr; but after a video call it climbs up to 65M/25M (still
    a lot less than java clients like jitsi!)._in Debian_
-   <a name="gajim">[Gajim](http://www.gajim.org/) (GPL)
    Jabber client written in PyGTK.  Gajim handle ssl connections and connect to google
    talk service.  Gajim can be either linked to gnome libraries and services or used
    without gnome. _in Debian_. _Gajim_ has support for {{< iref "#jingle" "Jingle" >}}
    voice protocol.

    Gajim is a python module that has for v 1.3.0 a memory footprint of 154M res / 89M
    shr.
    -   [ArchWiki: Gajim](https://wiki.archlinux.org/index.php/Gajim)
    -   [Gajim plugins list](https://trac-plugins.gajim.org/)
    -   [Gajim support status for various XEPs
        ](https://trac.gajim.org/wiki/GajimXEPSupport)
    -   [OMEMO Gajim plugin
        ](https://dev.gajim.org/gajim/gajim-plugins/-/wikis/OmemoGajimPlugin)
        allows support for  {{< iref "#omemo" "OMEMO" >}}.
-   <a name="kadu"></a>[Kadu](https://gitlab.com/kadu/kadu) (GPL v2)
    is a QT Gadu-Gadu and XMPPclient for Linux, BSD, Mac OS X and
    Windows.  It has numerous plugins (over 40 plugins) and support OTR.
    _No more developped since 2017_
-   {{< iref "sip#jitsi" "Jitsi" >}} (LGPL)
    is a xmpp and sip client written in java.  It support xmpp
    {{< wp "Jingle (protocol)" "Jingle" >}} allowing video calls.  It has also sip
    support. As usual for java apps, it is an heavy software, ~300M resident,
    {{< iref "sip#jitsi" "Jitsi entry in the Sip Section" >}}.
-   <a name="psi"></a>[Psi](http://psi-im.org/) (GPL)
    QT 5.x Jabber Client(26M/20M shared). Psi
    can handle ssl connections and [connect to google talk service
    ](http://www.google.com/support/talk/bin/answer.py?answer=24074)
    and is in Debian.
    -   {{< wp "Psi_(instant_messaging_client)"  "Wikipedia: Psi" >}}
    -   Psi has a nice [Wiki](http://psi-im.org/wiki) with documentation,
        not only for the client; but also aimed to jabber protocol
        use.
    -   [psi github repo](https://github.com/psi-im/psi)
    -   From 0.13 [voice calling is a standard feature of Psi
        ](http://psi-im.org/wiki/Voice_Calling) on all major platforms.
    -   Psi uses 26M res./20M shr this make it one of the lightest
        jabber graphical client with voice support.  Even if you use
        mainly a GTK desktop and you have to load the shared library,
        Psi is still lighter than Pidgin and Empathy.
    -   <a name="psi_plus"></a>[Psi +](http://psi-plus.com/wiki/en:main) is a fork of PSI
        that add numerous minor features including
        {{< iref "#otr" "OTR" >}} and {{< iref "#omemo" "OMEMO" >}} encryption.
        It has a debian and docker packages on the download section.
        It is also provided in Debian in the package _psi-plus_ and a numerous plugins
        in the required package _psi-plus-plugins_.
        -   [Psi+ list of plugins
            ](http://psi-plus.com/wiki/en:plugins)
        -   [GitHub repository with snapshots for Psi+
            ](https://github.com/psi-plus/psi-plus-snapshots).
    -   [Psimedia](https://github.com/psi-plus/psimedia)
        is an abstraction layer for providing audio and video RTP services to Psi-like
        IM clients.  The implementation is based on GStreamer. _In the Debian package
        psi-plus-plugin-psimedia_.
-   <a name="salutatoi"></a>[Salut à Toi](https://salut-a-toi.org/) (AGPL)
    is a Xmpp multi-frontends python tools wich allow in addition to
    jabber microblogging, file sharing, irc access, email client
    access. It has desktop, android, web server and client, console,
    and cli frontends.
    -   _primitivus_ is a console client for
        _Salut à Toi_ the Debian package is _sat-xmpp-primitivus_.
    -   [Libervia demo](https://www.libervia.org/) Libervia is the
        web frontend, that allow notifications via web push.
    -   [Salut à Toi Wiki](http://wiki.goffi.org/wiki/Sat)
-   <a name="spark"></a>[Spark](http://www.igniterealtime.org/projects/spark/index.jsp)
    (Apache License) is a java based client proposed by
    [ignite realtime](http://igniterealtime.org/) the authors of
    {{< iref "#openfire" "Openfire" >}} and of the obsoleted
    SparkWeb.
    It features built-in support for group chat, telephony
    integration, and strong security. It installs under windows, linux
    and mac.
    It is an heavy software but with {{< wp "Jingle (protocol)"  "Jingle" >}}
    support.
    -   [Spark GitHub repository](https://github.com/igniterealtime/Spark)
-    <a name=swift"></a>[Swift](https://swift.im/) (GPL) is a C++ / QT Xmpp client.
     Swift uses{{< iref "#bosh" "BOSH" >}}
    for connecting to servers over HTTP
    where network conditions prohibit standard connection methods.
    The debian package is *swift_im*. It is also available on windows
    and mac OS X.
-   <a name="tkabber"></a>[TKabber](http://tkabber.jabber.ru/) (GPL)
    TCL/TK Xmpp client available on many platforms
    (Linux, other Unixes, MacOS X and Windows). It supports IRC-style"
    chat commands, MUC, File transfers, BOSH, SASL authentication,
    IPv6,r gateways to legacy IM networks (AIM, ICQ, Microsoft
    Messenger service, Yahoo! Messenger and ...).
    It has also a plugin system including plugins for
    {{< iref "#otr" "Off-the-record messaging" >}}
    and {{< iref "#openpgp" "GPG-signed/encrypted messages" >}}.
    There are onlu maintenance commits since  since 2015.
    There is still a Debian package.

    -   Wikipedia: {{< wp "Tkabber" >}}
    -   [Tkabber documentation
        ](http://tkabber.jabber.ru/files/doc/tkabber.html).
    -   [Tkabbersource repository (fossil)
        ](https://chiselapp.com/user/sgolovan/repository/tkabber/)
    -   [Tkabber plugins
        ](https://chiselapp.com/user/sgolovan/repository/tkabber-plugins/).
    -   [Tkabber contribs (3rd party plugins)
        ](https://chiselapp.com/user/sgolovan/repository/tkabber-contrib/).

## Pidgin and Libpurple
<a name="pidgin"></a>[Pidgin](http://pidgin.im/) (GPL)
GTK2-based Instant Messaging (IM) application (50M res / 21
shared).
It uses {{< iref "#libpurple" "libpurple" >}} which ensure
supports for AIM, Gadu-Gadu, Google Talk, iChat, ICQ, IRC, Jabber,
{{< wp "Jingle (protocol)"  "Jingle" >}}, Lotus
Sametime, MSN, Napster, SILC, Tlen.pl, Yahoo!,and Zephyr.

To have a complete list of protocols look at
[Pidgin Plugins list](https://pidgin.im/plugins/).

Since version 2.6 pidgin support video and voice chat support over XMPP,
i.e.  {{< wp "Jingle (protocol)"  "Jingle protocol" >}}.

Pidgin is quite heavy, Pidgin without any extension is 46M res/24M shr.
If you don't run gnome you can still compile it as long as you
don't ask for evolution connectivity. *Pidgin was previously known
as Gaim.*.  Pidgin is documented in:

-   [Pidgin Home](http://pidgin.im/)
-   [Pidgin wiki](http://developer.pidgin.im/wiki).
-   [Pidgin FAQ](https://pidgin.im/development/faq/)
-   [Voice and Video](https://pidgin.im/development/voice-and-video/)
-   {{< wp "/Pidgin_(instant_messaging_client)"  "Wikipedia: Pidgin" >}}
-   [ArchWiki: Pidgin](https://wiki.archlinux.org/index.php/Pidgin)
-   {{< wp "Pidgin_(software)"  "Wikipedia: Pidgin" >}}
-   <a name="finch"></a>**finch** is a curse client for pidgin,
    finch allows to reuse your pidgin settings, and a great level
    of compatibility with pidgin, but it is a heavy ncurses client
    25M / 15M shared. It is in a separate Debian repository.

### Libpurple {#libpurple}
</a>[libpurple](https://developer.pidgin.im/wiki/WhatIsLibpurple)
is a multi-protocol instant messaging library it supports AIM/ICQ,
Yahoo!, MSN, IRC, Jabber/XMPP/Google Talk, Napster, Zephyr,
Gadu-Gadu, Bonjour, Groupwise, Sametime, SIMPLE, MySpaceIM, and
MXit, Facebook chat, Rocket.Chat, {{< Iref "Microblogging#Mattermost" "Mattermost" >}},
{{< iref "microblogging#matrix" "Matrix" >}}, Telegram, and more.

_libpurple_ is part of {{< iref "#pidgin" "pidgin" >}} and
used by
{{< iref "#finch" "finch" >}},
{{< iref "#minbif" "minbif" >}},
{{< iref "#telepathy" "telepathy haze" >}} and through it
by the telepathy clients,
{{< iref "#spectrum" "Spectrum" >}},
{{< iref "#bitlbee" "bitlbee-libpurple" >}}.



### Pidgin/libpurple plugins {#pidgin_plugins}
The [Pidgin Plugins list
](https://developer.pidgin.im/wiki/ThirdPartyPlugins)
includes numerous plugins to add features,
support many protocols, ensure privacy.

The [Additional protocols plugins
](https://developer.pidgin.im/wiki/ThirdPartyPlugins#AdditionalProtocols)
list plugins, _some of them are obsolete_, this list includes:
-   [Tox protocol plugin](http://tox.dhs.org/) (GPL) for
    {{< iref "#tox" "Tox protocol" >}}.
-   [telegram-purle plugin
    ](https://github.com/majn/telegram-purple)
    allow a bridge to {{< iref "#telegram" "Telegram" >}}
-   [purple-mattermost](https://github.com/EionRobb/purple-mattermost)
    connect to a
    {{< iref "social_networks#mattermost" "Mattermost" >}}
    server
-   [slack-libpurple](https://github.com/dylex/slack-libpurple)
    for access to {{< iref "social_networks#slack" "Slack" >}}
-   [purple-rocketchat
    ](https://bitbucket.org/EionRobb/purple-rocketchat)
    for {{< iref "social_networks#rocketchat" "Rocket.Chat" >}}.
-   [whatsapp-purple](https://github.com/davidgfnet/whatsapp-purple/)
    is obsolete, don't use.
-   [purple-facebook](https://github.com/dequis/purple-facebook).
-   [purple-matrix](https://github.com/matrix-org/purple-matrix)
    for {{< iref "social_networks#matrix" "Matrix" >}}.
-   [purple-hangouts](https://bitbucket.org/EionRobb/purple-hangouts/wiki/Home)
-   [libpurple-signald](https://github.com/hoehermann/libpurple-signald)
    for the {{< iref "#signald" "Signal Daemon - signald" >}}.

{{< iref "#pidgin" "Pidgin" >}} has many
[Security and privacy plugins
](https://developer.pidgin.im/wiki/ThirdPartyPlugins#SecurityandPrivacy):

-   [Pidgin encryption](http://pidgin-encrypt.sourceforge.net/),
    transparently encrypts your instant messages with RSA
    encryption. _low activity since 2007, last change 2010_, _is
    in Debian_.
-   [Tinfoil Chat OTP (TFC)](https://github.com/maqp/tfc-otp)
    high assurance encryption plugin for Pidgin IM client.
    Encryption is done with one-time pad that provides perfect
    secrecy even if the adversary has unlimited computing power.
    Authentication is done with unconditionally secure one-time
    MAC, Keys are generated with an open circuit design hardware
    random number generator.
    -   [TFC Manual (pdf)
        ](https://cs.helsinki.fi/u/oottela/tfc-manual.pdf)
    _In Debian_.
-   [GPG/OpenPGP Plugin for Pidgin
    ](https://github.com/segler-alex/Pidgin-GPG/wiki)
    works asynchronously and allows you to send an
    {{< iref "#openpgp" "GPG" >}}
    encrypted message to peer even if she is offline.
    _OTR would be possible only online_
    but PGP does not allow {{< wp "Deniable authentication"  "deniability" >}}.
    _In Debian_.
-   [pidgin-OTR](https://bugs.otr.im/plugins/pidgin-otr) an
    {{< iref "#otr" "OTR" >}} plugin for Pidgin _in
    Debian_. See also [How to: Use OTR on Linux
    ](https://ssd.eff.org/en/module/how-use-otr-linux)
    by The Electronic Frontier Foundation.


# Web clients

There are many web clients using Ajax or even java, I scarcely use
them on desktop, because Jabber does not need a full featured
Javascript (or worse Java) enabled brother.  Whenever I'm on a foreign
computer, a jabber client can be very useful, I had used googlechat
but the new _hangout_ has turned into a proprietary protocol.

<a name="bosh"></a>[BOSH  “Bidirectional-streams Over Synchronous HTTP”
](http://xmpp.org/about-xmpp/technology-overview/bosh/)
is a technology for two-way communication over the HTTP. BOSH has
been used mainly as a transport for traffic exchanged between
Jabber/XMPP clients and servers. BOSH is more bandwidth-efficient and
responsive than AJAX.  Bosh is supported by Xmpp servers and
standalone XMPP connection managers; [Which BOSH Server Do You Need?
](http://metajack.im/2008/09/08/which-bosh-server-do-you-need/)
compare these two options.

The following clients have support for BOSH
{{< iref "#converse" "Converse" >}}
{{< iref "#gajim" "Gajim" >}},
{{< iref "#jwchat" "JWChat" >}},
{{< iref "#jsxc" "jsxc" >}},
{{< iref "#movim" "Movim" >}},
{{< iref "#pidgin" "Pidgin" >}},
{{< iref "#swpeeqe" "Speeqe" >}},
{{< iref "#swift" "Swift" >}},
{{< iref "#tigaseweb" "Tigase Web client" >}},
{{< iref "#xmpp4js" "xmpp4js" >}} and Soashable,
Adium _client for Mac OS X_.

The following XMPP servers include built-in support for BOSH:
{{< iref "#ejaberd" "ejabberd" >}},
Jabber XCP, M-Link, MongooseIM,
{{< iref "#openfire" "Openfire" >}},
{{< iref "#prosody" "Prosody" >}},
{{< iref "#tigase" "Tigase" >}}.

-   [AjaxJabber](http://ajaxbber.sourceforge.net/)
    (LGPL) is what it's name announce!.
    It is comparable to JWChat but without popup.
-   <a name="converse"></a>[Converse.js](http://conversejs.org/)
    (Mozilla Public License _MPL_)
    is a javascript Xmpp web client that supports multi-user
    chatrooms.  Converse.js can use SSL, it makes an SSL encrypted
    connection to a secure connection manager which then uses SSL and
    TLS to connect to an XMPP server.
    -   [Converse.js documentation](https://conversejs.org/docs/).
    -   [GitHub - converse.js](https://github.com/jcbrand/converse.js).
    -   You can use converse.js with the service provided on
        [Converse.js Home](http://conversejs.org/) or in full screen
        at [Inverse](https://inverse.chat/).
    -   You can also [integrate Converse.js in your website
        ](https://conversejs.org/docs/html/setup.html).
    -   [List of supported XEP](https://conversejs.org/#features).
    -   [Converse.js Security
        ](https://conversejs.org/docs/html/security.html).
    -   [Converse supports OTR
        ](https://conversejs.org/docs/html/features.html),
        but quoting the author JC Brand
        > In its current state, JavaScript cryptography is fraught
        > with dangers and challenges that make it impossible to reach
        > the same standard of security that is available with native
        > “desktop” software.
        He explains it more in details in his post
        [Converse OTR support
        ](https://opkode.com/blog/2013/11/11/conversejs-otr-support/).
-   <a name="jsxc"></a>[jsxc](https://www.jsxc.org/) (MIT License)
    is a real-time xmpp javascript app it requires an external XMPP server. It supports
    {{< iref "#omemo" "OMEMO" >}}.  It is in the Debian package _libjs-jsxc_.<br/> They
    offer to install your
    [own managed virtual XMPP server](https://www.jsxc.org/managed.html)
    with a nextcloud app.
    -   [GitHub jsxc](https://github.com/jsxc/jsxc)
-   <a name=jwchat></a>[Jwchat](http://stefan-strigler.de/jwchat/)
    is a XMPP web client. It supports communication over
    {{< iref "#bosh" "BOSH" >}} and MUC. _Jwchat is in Debian_.
    Jwchat is  discontinued since 2011, but you can still find a live
    client
    -   [JWChat at jwchat.org](https://jwchat.org/).
    -   [Jwchat tutorial](http://wiki.jabberfr.org/JWChat).
    -   [Jwchat GitHub repo](https://github.com/sstrigler/jwchat)
-   <a name="movim"></a>{{< wp "Movim" >}}
    is a Web client, developed largely in PHP which can be
    deployed on a web server (Apache, nginx ... ) . This server
    provides a social network Web interface XMPP which will be the
    intermediary between the browser and the XMPP server that contains
    the user account.
    -   [Movim Wiki](https://github.com/movim/movim/wiki)
    -   [Movim.eu](https://movim.eu/)
        propose a jabber server, and movim service.
-   <a name="prodomus"></a>[Prodomus
    ](http://forge.webpresso.net/projects/prodromus) (AGPL)
    is a simple XMPP messaging client, mainly reasonable as contact form
    replacement/supplement or support contact utility.
-   <a name="speeqe"></a>[Speeqe
    ](https://github.com/thepug/speeqe/wiki) (AGPL)
    is a web python/javascript group chat client that works with the
    XMPP/MUC protocol. _development inactive since 2012_
    -   [List of SpeeqeInstances
        ](https://github.com/thepug/Speeqe/wiki/SpeeqeInstances)
        _The list is from year 2015 and most instances seems to be
        down by now._
-   <a name=tigaseweb></a>[Tigase Web client](http://www.tigase.net/content/web-client)
    (AGPL) supports XMPP Core - RFC 6120, XMPP IM - RFC 6121 and
    [many XEP extensions](http://www.tigase.net/webclient-features)
    including XMPP Over BOSH - XEP-0206.

    There are also two _tigase messenger_ Afero GPL applications for
    [ios](https://tigase.net/content/tigase-messenger-ios) and
    [android](https://tigase.net/content/tigase-messenger-android).

    -   [Online Tigase Web client](http://tigase.im/)
    -   [Tigase projects](https://tigase.tech/projects)
-   <a name="xabber_web"></a>[Xabber for Web](https://www.xabber.com/web/)
    support {{< iref "#omemo" "OMEMO" >}}
    -   [Xabber Web online client](https://web.xabber.com/)
-   <a name="xmpp4js">[Xmpp4Js](http://xmpp4js.sourceforge.net/) (LGPL)
    is an XMPP client library written in pure Javascript. It connects
    to a server using {{< iref "#bosh" "BOSH" >}}.  Xmpp4Js was
    originally derived from
    [Soashable](http://soashable.sourceforge.net/)

# Android clients
-   <a name="chatsecure"></a>[Chatsecure](https://chatsecure.org/)
    (GPL)
    is a Xmpp client for android and IOS supporting
    {{< iref "#otr" "OTR" >}} and
    {{< iref "#omemo" "OMEMO" >}}.
    It is developped by
    {{< wp "The_Guardian_Project_(software)"  "The Guardian Project" >}}
    -   [ChatSecure, Conversations and Zom — ChatSecure
    ](https://chatsecure.org/blog/chatsecure-conversations-zom/).
-   <a name="conversation"></a>[Conversations
    ](https://github.com/siacs/Conversations) (GPL)
    XMPP/Jabber client for Android 4.0+ with end-to-end encryption
    with {{< iref "#omemo" "OMEMO" >}},
    {{< iref "#otr" "OTR" >}}, or
    {{< iref "#openpgp" "OpenPGP" >}}.
    See the [homepage](https://github.com/siacs/Conversations)
    for a list of features and supported XEP.
-   {{< iref "#saluatoi" "Salut à Toi" >}} (AGPL) has an Android client.
-   <a name="stork"></a>[Stork](https://github.com/tigase/stork) (AGPL) by [Tigase
    Inc.](https://tigase.net/) is a XMPP client. It supports all XMPP specifications RFC
    6120 - XMPP COR, RFC 6121 - XMPP IM ,and many extensions including Multi-User Chat
    XEP-0045, and {{< iref "#omemo" "OMEMO" >}}.
-   [Beem](http://beem-project.com/projects/beem/) (GPL)
    _last release 2013_
-   [Xabber](https://www.xabber.com/)  (GPL) Xmpp client for
    Android, it supports {{< iref "#otr" "OTR" >}}.
-   <a name= "zom"></a>[Zom](https://zom.im/) is an ios and android
    xmpp client supporting
    {{< iref "#otr" "OTR" >}} and
    {{< iref "#omemo" "OMEMO" >}}
    created by the {{< iref "#chatsecure" "ChatSecure project" >}}.

# IRC to Xmpp gateways
By IRC to Xmpp we mean here a software allowing an IRC Client to talk
to remote Xmpp clients.

-   <a name="bitlbee"></a> {{< wp "bitlbee" >}} (GPL) is an IRC to other chat
    networks gateway, such as AIM, ICQ, Microsoft Messenger, Yahoo!,
    Jabber, Facebook Messenger, Twitter, Identi.ca,
    and status.net.  It allows you to browse other chat protocols with
    your irc client. Bitlbee can be usefull if you want to use only a
    light irc client to take part in chats from many protocols
    including jabber/ssl as in gmail accounts.

    Bitlbee has support for {{< iref "#otr" "OTR" >}}
    with _libotr_.

    The bitlbee
    daemon is tiny 1.2M res./0.8M shared. _in Debian_.

    -   [bitlbee Home](http://www.bitlbee.org/)
    -   [Bitlbee documentation
        ](http://www.bitlbee.org//user-guide.html)
    -   [Bitlbee Wiki](https://wiki.bitlbee.org/)
        offer on-line searchable BitlBee documentation.
        There is a list of supported protocols in the first page.
    -   [list of public bitlbee servers
        ](http://www.bitlbee.org/main.php/servers.html)
        they allow to use Bitlbee without installing
        it.
    -   [ArchLinux BitlBee Tutorial
        ](http://wiki.archlinux.org/index.php/Bitlbee)
        explains how to connect to Jabber using your Gmail account.
    -   [ArchLinux Screen Irssi Bitlbee and SSH
        ](http://wiki.archlinux.org/index.php/Screen_Irssi_Bitlbee)
        explains how to have a persistent connection to messaging
        services.
    -   [Emacs and BitlBee
        ](http://www.emacswiki.org/cgi-bin/wiki?BitlBee)
    -   [bitlbee-otr](https://wiki.bitlbee.org/bitlbee-otr) add
        support for {{< iref "#otr" "Off-the-Record Messaging (OTR)" >}} either by a plugin
        _bitlbee-plugin-otr is in Debian_ or Bitlbee has an
        optional native support for OTR since 3.0, which can be
        enabled at compile time.
    -   [Bitlbee development daily package
        ](https://wiki.bitlbee.org/Packages) may be fresher then the
        Debian standard one.
    -   [BitlBee native support to Twitter
        ](https://wiki.bitlbee.org/HowtoTwitter) partly [deprecated
        ](https://wiki.bitlbee.org/HowtoTwitter/StreamDeprecation).
    -   [BitlBee native support for Gnu Social
        ](https://wiki.bitlbee.org/HowtoStatusNet).
    -   [BitlBee support for Facebook
        ](https://wiki.bitlbee.org/HowtoFacebookMQTT).
    -   [BitlBee plugin for Mastodon
        ](https://github.com/kensanata/bitlbee-mastodon).

    [BitlBee can be compiled to use libpurple
    ](https://wiki.bitlbee.org/HowtoPurple)
    instead of the built-in code. It offers a few extra features
    (like file transfers on all IM networks) and
    support more networks protocols.  It
    adds a lot of dependencies (around 100MBytes of extra
    packages), and it makes the program more resource-hungry at
    runtime.

    But _bitlbee-libpurple_ allow to use some more protocols
    like [Skype with skypeweb](https://wiki.bitlbee.org/HowtoSkypeWeb),
    GaduGadu, SIPE, Microsoft's OCS, Lync (on Office 365 as well), Skype for Business,
    Telegram through [telegram-purle plugin](https://github.com/majn/telegram-purple),
    Slack, Rocket.Chat, {{< Iref "Microblogging#Mattermost" "Mattermost" >}}, Google Hangout through
    [purple hangout plugin](https://bitbucket.org/EionRobb/purple-hangouts),
    WhatsApp no longer work due to whatsapp forbidding libpurple access.

    _bitlbee-libpurple_ is in debian. See also the
    {{< iref "#libpurple" "libpurple section" >}}.
    -   [Using BitlBee with the libpurple IM backend
        ](https://wiki.bitlbee.org/HowtoPurple)
-   [jatter](https://github.com/binfalse/jatter) (GPL)
    is a java bot providing a  a Jabber-Twitter-bridge.
-   <a name="matterbridge"></a>[Matterbridge](https://github.com/42wim/matterbridge)
    (Apache License)
    is a bridge written in go between {{< Iref "Microblogging#Mattermost" "Mattermost" >}}, IRC, Gitter, xmpp,
    {{< iref "microblogging#slack" "Slack" >}},
    {{< iref "microblogging#gitter" "Gitter"  >}},
    Discord,  {{< iref "#telegram" "Telegram" >}},
    {{< iref "microblogging#keybase" "Keybase" >}},
    {{< iref "microblogging#rocketchat" "Rocket.Chat" >}}
    Hipchat (via xmpp), Steam,
    Twitch, ssh-chat and  {{< iref "microblogging#matrix" "Matrix" >}} with REST API.
-   <a name="spectrum2">[Spectrum2](http://spectrum.im/) (GPL)
    is a proxy  allowing to connect from Xmpp or
    {{< iref "microblogging#slack" "Slack" >}} to many protocols. We can choose the
    backend we use with {{< iref "#libpurple" "libPurple" >}} we can all the lipurple plugins
    : AIM, Jabber, ICQ, MSN, Yahoo, Skype, Telegram, Facebook;
    with _LibCommuni_ we bridge to IRC; Twitter backend is for Twitter (!); Swiften
    backend allows XMPP; [Transwhat backend](https://github.com/stv0g/transwhat) is used
    for WhatsApp.

    The repository offer an apt repo with source deb packages,
    and a Docker image.
    -   [Spectrum2 GitHub repository](https://github.com/hanzz/spectrum2)

# Xmpp servers software
-   Wikipedia: {{< wp "Comparison of XMPP server software" >}} compare
    RFC implementation and XEP implementation from each server software.
-   [xmpp.org: Servers](http://xmpp.org/software/servers.html)
-   [ArchWiki: xmpp servers
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Servers)

-   [ejabberd](http://www.ejabberd.im/)
    is an Erlang jabber server, looking at
    [Xmpp.org Service page](http://xmpp.org/services/)
    with Prosody they are the two most widely used server.
-   [Jabberd2](http://jabberd2.org/)(GPL)
    is a Xmpp server written in C. It is maintained by
    [xiaoka](http://codex.xiaoka.com/wiki/)
    which also maintain [Chrome.pl](http://www.chrome.pl/)
    a polish XMPP/Jabber service with integrated e-mail accounts and
    option to host own domain accounts.
-   <a name=openfire"></a>[Openfire
    ](http://www.igniterealtime.org/projects/openfire/index.jsp)
    (Apache License) is a real time collaboration (RTC) XMPP server
    written in Java, proposed by
    [ignite realtime](http://igniterealtime.org/).
    _Openfire_ provide a Debian package, the related client is
    {{< iref "#spark" "Spark" >}}.
    Openfire does not seem to be used by many public servers but
    the french [ForumAnalogue](http://www.forumanalogue.fr/).
    -   [Openfire Documentation
        ](http://www.igniterealtime.org/projects/openfire/documentation.jsp).
    -   [Openfire GitHub repo](https://github.com/igniterealtime/Openfire).
-   <a name="prosody"></a>[Prosody](http://prosody.im/)
    (MIT/X11 license) is a  Xmpp/Jabber server written in Lua.
    with ejaberd they are the two most widely used server.
    -   [ArchWiki: Prosody
        ](https://wiki.archlinux.org/index.php/Prosody)
    -   A french [prosody Tutorial
        ](http://www.vanaryon.tk/2010/01/prosody-un-serveur-jabber-leger/)
-   <a name="tigasexmppserver"></a>[Tigase Xmpp Server
    ](http://www.tigase.net/content/tigase-xmpp-server)  (AGPL)
    Is a java Xmpp web server.
    It supports RFC 6120 - XMPP CORE and RFC 6121 - XMPP IM  along
    with a [many extensions](http://www.tigase.net/server-features).
    It is designed to run from very small machines, to standard
    servers.
-   [IMSpector](http://www.imspector.org/wordpress/) (GPL)
    is an Instant Messenger proxy written in C++ with monitoring,
    blocking and content-filtering capabilities. It supports MSN,
    Jabber/XMPP, AIM, ICQ, Yahoo, IRC and Gadu-Gadu.  IMSpector is
    normally deployed on the network’s router. _It is in debian._


# Xmpp Libraries
## C or C++
-   {{< iref "#libpurple" "Libpurple" >}}
    is above with its main frontend {{< iref "#pidgin" "Pidgin" >}}.
-   <a name="telepathy"></a>[Telepathy
    ](http://telepathy.freedesktop.org/wiki/) is a framework
    that provide communication as a desktop service by using a unified
    [D-Bus](http://dbus.freedesktop.org/) API.
    Telepathy provides protocol backends for Jabber/XMPP/Jingle,
    link-local XMPP, SIP, Yahoo/AIM and IRC. It supports instant
    messaging, voice calls and video calls. The gnome messaging
    clients are
    {{< iref "#empathy" "Empathy" >}} and _polari_.
    Telepathy and it's plugins are in Debian.

    -   The _haze_ plugin is a Telepathy connection manager based on
        libpurple, this allows to connect to all protocols supported
        by libpurple (Pidgin) including AIM, Windows Live (MSN),
        Yahoo!, Gadu-Gadu, Groupwise and ICQ.
    -   _rakia_ is a SIP connection manager for
        Telepathy based on the
        [SofiaSIP](http://sofia-sip.sourceforge.net/development.html)
        stack.
    -   _Gabble_ is a Jabber/XMPP connection manager for Telepathy,
        it handles Google Talk and Facebook Chat.
    -   _Idle_ is an IRC connection manager for the Telepathy.

## Python, Lua
-   [jabberpy](http://jabberpy.sourceforge.net/)
    python Xmpp library  _not maintained_.
-   [pyxmpp2](https://github.com/Jajcus/pyxmpp2) (LGPL)
    python Xmpp library  _based on libxml2 _,
-   [Twisted Words](http://twistedmatrix.com/documents/current/words/)
    (MIT License) python Xmpp library.
-   [Verse](http://matthewwild.co.uk/projects/verse/home)
    is a Jabber library in Lua.
-   [Xmpp on Google App Engine
    ](http://code.google.com/appengine/articles/using_xmpp.html)
-   [xmpppy](http://xmpppy.sourceforge.net/) (GPL)
    a python Xmpp library _aims to work with jabberd2_,

## PHP
-   [XmpPhp](http://code.google.com/p/xmpphp/)
    is a Xmpp library, that supports TLS.

## Javascript
-   [Strophe](http://strophe.im/)
    the library on which {{< iref "#converse" "Converse.js" >}}
    is built
-   [JSJaC - JavaScript Jabber Client Library
    ](https://github.com/sstrigler/JSJaC) (GPL + LGPL +Mozilla )


# Xmpp Bots
-   Wikipedia: {{< wp "Internet bot" >}}
-   [list of bots](http://xmppcomm.com/#!/page_jbots). _empty when
    last consulted_.
-   [jabber.fr: Robots](http://wiki.jabberfr.org/Robot).
-   [Robopsychology - Jabber, XMPP & Chatbots
    ](http://meta-guide.com/bots-agents-assistants/chatbots/jabber-xmpp-chatbots)
    _outdated an unreliable list_.

-   [Jabberbot](http://thp.io/2007/python-jabberbot/) (GPL)
    is a simple framework for creating Jabber/XMPP bots and services
    in Python.
    -   [dvcs-autosync](http://mayrhofer.eu.org/dvcs-autosync)
        an open source replacement for Dropbox, uses jabberbot to
        synchronize remote directories with git.
    -   [System status bot
        ](http://www.uhoreg.ca/programming/jabber/systembot)
        (public domain) use jabberbot to monitor system statistics, on
        remote machines.
-   [JabRSS](http://dev.cmeerw.org/jabrss/) (GPL)
    is a simple RSS (RDF Site Summary) headline notification service
    for Jabber.
-   [rss2jabber](http://rss2jabber.berlios.de/)
    is a PHP, MySQL application that gathers articles from RDF/RSS/Atom
    feeds and sends them to an IM client.
    It is available at `rss2jabber@jabber.fr`.
-   [Talkfeed](http://code.google.com/p/talkfeed/) (Apache License)
    is a tool to receive new posts from RSS and Atom feeds
    directly in your Jabber client.
    The application is
    [hosted on Google App Engine](http://talkfeed.appspot.com)



# Google Talk and Hangouts

In 2013 Google closed Google Talk in favor of
{{< wp "Google Hangout" >}} which uses  a proprietary protocol.

Google [announced
](https://blog.google/products/workspace/latest-google-hangouts-and-upgrade-google-chat/)
that it will close hangout in 2021, it will be replaced by {{< wp "Google Meet" >}}
and {{< wp "Google Chat" >}}.

Google Chat is a product which is rerved to user of Google Worspace account (paid plan).

In beginning 2021 Google meet can be used freely and it is announced that it will be
also the case of Google Chat mid 2021, and the hangout accounts will be migrated to Chat.

There are attempts to provide access to the Hangout proprietary
protocol.

-   [Hangup](https://github.com/tdryer/hangups) (MIT License)
    is a third-party instant messaging client for Google Hangout written in python, it
    is implemented by reverse-engineering the protocol.

    It supports features like group messaging that aren't available in clients that
    connect via XMPP.

    There are many project using Hangup [see the project page
    ](https://github.com/tdryer/hangups) among which many bots,
    [hangups.el](https://github.com/jtamagnan/hangups.el) an Hangout client for emacs,
    [pickups](https://github.com/mtomwing/pickups) an IRC to Hangout gateway,
    [telepathy-hangups](https://github.com/davidedmundson/telepathy-hangups) telepathy
    bindings for hangout,
    [jabber-hangouts-transport](https://github.com/ZeWaren/jabber-hangouts-transport)
    a XMPP transport/gateway for Google Hangouts.

-   [purple-hangouts](https://github.com/EionRobb/purple-hangouts) is an hangout plugin
    for libpurple

# Multiprotocols clients

-   <a name="ramhost"></a>[Rambox](http://rambox.pro/) (GPL)
    is a  messaging and emailing app that combines common web
    applications into one. There are 96 sevices supported. Rambox is
    written in Node.js on top of Electon and Sencha ExtJs.
    There are AppImages and Deb packages available.

    XMPP and IRC are not in the proposed services, we may add them via
    custom script, see [this issue
    ](https://github.com/saenzramiro/rambox/issues/38)
    and [the issues labelled IRC
    ](https://github.com/saenzramiro/rambox/issues?utf8=%E2%9C%93&q=is%3Aissue+IRC).

    For Weechat we ca add [glowing-bear](https://www.glowing-bear.org/)
    by following the recipe in [this issue
    ](https://github.com/saenzramiro/rambox/issues/1110)

    Rambox AppImage on x64 takes 58M of disk file, and a resident mem
    of 150M and each open service between 160M and 280M. When you
    disable the service, you also close the process managing it, and
    free the corresponding memory.

    -   [GitHub Rambox](https://github.com/saenzramiro/rambox)
-   <a name="franz5"></a>[Franz 5](https://meetfranz.com/)
    Franz is a Windows, OS X, and linux messaging app for Facebook
    Messenger, Gitter, HipChat, {{< Iref "Microblogging#Mattermost" "Mattermost" >}},
    {{< iref "microblogging#rocketchat" "RocketChat" >}}, Skype, Slack,
    Telegram, WhatsApp,and more.
    There is a Debian/Ubuntu package.
    -   [GitHub - meetfranz/franz
        ](https://github.com/meetfranz/franz) (Apache License).
    -   [meetfranz/plugins](https://github.com/meetfranz/plugins)
        Franz 5 - Plugins/Recipes.
    -   [Franz 5 xmpp plugin
        ](https://github.com/alexander-schranz/franz-xmpp-client)


# Other secure messaging clients

## Other secure protocols

-   <a name="fish"></a>FiSH is an IRC plugin providing {{< wp "Blowfish" >}}.
    encryption to IRC chat. It is an old protocol aimed to IRC, which was
    [proposed in 2009
    ](http://blog.bjrn.se/2009/01/proposal-for-better-irc-encryption.html)
    and never adopted in a RFC.
    You can find it in
    {{< iref "irc#irssi" "irssi" >}}, [FISHLIM
    ](http://fishlim.kodafritt.se/) for
    {{< iref "irc#hexchat" "HexChat" >}} or
    {{< iref "irc#xchat" "XChat" >}},
    {{< iref "irc#weechat" "WeeChat" >}},
    the python package [pyIRCFiSH
    ](https://pypi.python.org/pypi/pyIRCFiSH/),
    the android
    IRC client [AndroIRC](http://wiki.androirc.com/start).
    It is also available in the windows IRC client _mirc_ through a
    plugin.

## Tox Protocol {#tox}

{{< wp "Tox_(protocol)"  "Tox" >}} (GPL)
is a peer-to-peer instant messaging and video calling protocol that offers end-to-end
encryption. All traffic over Tox is end-to-end encrypted, and provides
{{< wp "authenticated encryption" >}} and {{< wp "forward secrecy" >}}. Tox clients aim
to provide support for messaging, group messaging, voice and video calling, voice and
video conferencing, typing indicators, message read-receipts, file sharing, profile
encryption, and desktop sharing.

-   [Tox Home](https://tox.chat/)
-   [ArchWiki: Tox](https://wiki.archlinux.org/index.php/Tox).
-   [GitHub: Tox core protocol](https://github.com/irungentoo/toxcore).

There are many clients for Tox protocol you find a
[comparison of their features in Tox wiki](https://wiki.tox.chat/clients#features):

-   [Antidote](https://antidote.im/) (MIT License) for iOS.
-   [Antox](https://wiki.tox.chat/clients/antox)
    (Apache License) written in scala for Android.
-   [gtox](https://github.com/KoKuToru/gTox) (GPL)
    a C++/QT client for linux.
-   Miranda Ng the windows messenger has a [plugin for Tox
    ](http://forum.miranda-ng.org/index.php?topic=2502.0).
-   [qtox](https://wiki.tox.chat/clients/qtox) (GPL)
    a client in C++/QT for linux, windows, OS X. It has Debian
    package in the project home.
    -   [qtox GitHub repository](https://github.com/tux3/qTox).
-   [RaTox](http://ratox.2f30.org/) (MIT Licence)
    is a no-gui, Linux and BSD FIFO client that communicate
    through named pipes. _unmaintained_
-   [Ricin](https://ricin.im/) (GPL)
    a VALA/GTK3 client for linux.It is in the Debian
    repo of Tox.
-   [Toxic](https://wiki.tox.chat/clients/toxic) (GPL)
    a C/ncurses command-line Tox client for Linux, BSD, OS X.
    It is in the Debian repo of Tox.
-   [Toxygen](https://wiki.tox.chat/clients/toxygen) is a Linux, OSX
    and Windoze Tox client written in Python3. It is in the Debian
    repo of Tox.
    -   [ToxygenGitHub repository
        ](https://github.com/toxygen-project/toxygen)
-   [tox-prpl](http://tox.dhs.org/) (GPL)
    is a Tox Protocol Plugin For Pidgin / libpurple.
-   *Toxy* for Windows
-   [µTox](https://wiki.tox.chat/clients/utox) (GPL) It is in the
    Debian repo of Tox.
-   [XwinTox](https://wiki.tox.chat/clients/xwintox) (GPL or AGPL)
    a C++/FLTK client for Linux and other unixes.


## Cryptocat {#cryptocat}

{{< wp "CryptocatCryptocat" >}} (GPL) is a javascript encrypted online chatting
application created by {{< wp "Nadim Kobeissi" >}}.

It uses end-to-end encrypted chat conversations, and allow to
exchange one-to-one messages, encrypted files and audio/video
recordings. All devices linked to Cryptocat accounts will receive
messages, even when offline.

For the transport layer encryption _Cryptocat_ uses the
{{< iref "#omemo" "OMEMO Multi-End Message and Object Encryption" >}}. _Cryptocat_'s network uses XMPP
over WebSockets and only relays encrypted messages and does not
store any data. In addition to the Cryptocat client's end-to-end
encryption protocol, client-server communication is protected by
TLS. It provide {{< wp "forward secrecy" >}} of messages, that is protects
past sessions against future compromises of secret keys or
passwords.

 _Cryptocat_ is available for Linux, windows, OSX.

 {{< wp "Nadim Kobeissi" >}}
 [answering to a request declared on 2016-04-28
 ](https://github.com/cryptocat/cryptocat/issues/77)
 «Cryptocat is no longer offered on mobile devices and will not be
 offered on mobile devices in the forseeable future...»

The main drawback of _Cryptocat_ is that even if it uses a combination of known open
source protocols, you can not communicate with any other software and you can only
encrypt messages between Cryptocat users, and use Cryptocat server..

-   [Cryptocat Home](https://crypto.cat/)
-   [Cryptocat Security](https://crypto.cat/security.html)
-   [Cryptocat Help](https://crypto.cat/help.html)
-   [Cryptocat GutHub repo](https://github.com/cryptocat/cryptocat)
-   [Blog - Cryptocat, ou le piège du client magique
    ](https://nl.movim.eu/?blog/edhelas@movim.eu/ebc3a98e-3a37-440f-8cb4-8de1fa7eed3b).

## Retroshare {#retroshare}
{{< wp "RetroShare" >}} (GPL) is a cross-platform decentralised
{{< wp "Friend-to-Friend" >}} application that offers social networking and
file sharing features. It uses Transport encryption with TLS, and
authentication with PGP It offers secure chat, VoIP with video,
multi-user chat, file search, file sharing file sharing, forums, link
sharing, Retroshare mail.

It is available on Windows, Linux, OS X, FreeBSD.  Retroshare is
available for Linux (many distributions), Windows, Mac OS,
Android. It is not in Debian but a Debian repository is provided.


-   [RetroShare Home Page](http://retroshare.net)
-   [Retroshare Documentation
    ](https://retroshare.readthedocs.io/en/latest/)
-   [Retroshare GitHub repo
    ](https://github.com/RetroShare/RetroShare).
-   [Retroshare Wiki
    ](https://github.com/RetroShare/documentation/wiki)
    seems partly replaced by the Documentation.
-   [RetroShare development blog
    ](https://retroshareteam.wordpress.com/).

## Signal {#signal}
{{< wp "Signal" >}} (GPL) is an encrypted voice calling and instant messaging
application developed by {{< wp "Open Whisper Systems" >}} for Android and iOS
taht uses end-to-end encryption to send instant messages, group
messages, attachments and media messages. It uses a modified OTR
protocol, however, without interopability with standard Xmpp networks.

On Android, Signal can be used to send and receive unencrypted SMS
messages in addition to the standard end-to-end encrypted Signal
messages. Signal requires that the user has a phone number for
verification not necessarily the same as on
the device's SIM card; it can also be a VoIP number or a
landline as long as the user can receive the verification code and
have a separate device to set-up the software. A number can only
be registered to one device at a time.

Signal messages and calls are routed through Open Whisper Systems'
servers (in more than 10 countries).

All client-server communications are protected by TLS, but each
message contains as metadata the phone number, which could, if
disclosed, allow to know the time and recipient of call. Open
Whisper Systems have asserted that their servers do not keep this
metadata or any logs about who called who and when.

__Signal Desktop__ is an  Electron  packaged app that links with the
Signal-iOS or Signal-Android client.

_Signal_ was previously called {{< wp "TextSecure" >}} in November 2015,
_TextSecure_ was merged with an encrypted voice calling application
called _RedPhone_ and was renamed as _Signal_.  The authors of _Signal_
and _TexSecure_ _Whisper Systems_ partnered with _WhatsApp_ in
November 2014 to encrypt users’ messages by default using their
_TextSecure/Signal_ protocol.

Since WhatsApps was sold to Facebook, {{< wp "Brian acton" >}}
who co-founded WhatsApps with {{< wp "Jan Koum" >}}, gave $ 50,000,000 to launch
the new [Signal fundation](https://signal.org/blog/signal-foundation/).

-   [Signal Home](https://signal.org/)
-   [Signal support](https://support.signal.org/hc/en-us):
    [Getting Started on Android, iOS, and Desktop
    ](https://support.signal.org/hc/en-us/categories/360000674771-Getting-Started),
    [Signal Messenger Features
    ](https://support.signal.org/hc/en-us/sections/360001602792-Signal-Messenger-Features),
    [Security
    ](https://support.signal.org/hc/en-us/categories/360000674811-Security),
    [Troubleshooting FAQ
    ](https://support.signal.org/hc/en-us/sections/360001602812-Troubleshooting-FAQ),
    [General FAQ](https://support.signal.org/hc/en-us/sections/360001602832-General-FAQ).
-   [Signal-Desktop GitHub repo
    ](https://github.com/signalapp/Signal-Desktop)
-   [EFF - Surveillance Self-Defense](https://ssd.eff.org/) :
    [How to: Use Signal on iOS
    ](https://ssd.eff.org/en/module/how-use-signal-ios),
    [How to: Use Signal on Android
    ](https://ssd.eff.org/en/module/how-use-signal-android).

The is an an alternate CLI
[GitHub - AsamK/signal-cli](https://github.com/AsamK/signal-cli).
This CLI can also be used with the netcurses interface
[GitHub - jwoglom/signal-curses](https://github.com/jwoglom/signal-curses)
or through weechat with
[GitHub - thefinn93/signal-weechat](https://github.com/thefinn93/signal-weechat).

<a name=signald></a>[signald](https://git.callpipe.com/finn/signald) (GPL)
is a daemon that facilitates communication over Signal bu sending messages in the signald
protocol.

Some libraries are available to encapsulate the protocol, there is also a
{{< iref "#libpurple" "libpurple" >}} plugin.

## Telegram {#telegram}
{{< wp "Telegram (software)"  "Telegram" >}} (GPL)
is a cloud-based instant messaging service on Android, iOS, Windows
Phone, Ubuntu Touch and Windows, OS X, Linux. Users can send with
optional end-to-end encryption messages, photos, videos, stickers
_high-definition emoji_ and any file.

Accounts are tied to telephone numbers and are verified by SMS or
phone call.

Default messages are cloud-based and can be accessed on any of the
user's connected devices. All data is stored heavily encrypted and the
encryption keys in each case are stored in several other DCs in
different jurisdictions. This way local engineers or physical
intruders cannot get access to user data

Messages can also be sent with client-to-client encryption in
secret chats.  Messages sent within a secret chat can be accessed only
on one sender and one reiver device, they can optionally
self-destruct.

There are some critisisms to the [Telegram security
](https://en.wikipedia.org/wiki/Telegram_(software)#Security)

Official Telegram applications are provided for IOS, Android, and other mobile
applications, and a [Desktop client
](https://desktop.telegram.org/) for windows and Linux and OSX  ,  a
[plugin for Chrome](https://chrome.google.com/webstore/detail/telegram),
and [tg: telegram-cli](https://github.com/vysheng/tg) a CLI
for linux.

A third party [firefox extension
](https://addons.mozilla.org/en-US/firefox/addon/telegram-web/)
is also available.

Users can also access Telegram's
cloud-based messages via an official web browser interface called
[Telegram Web](https://web.telegram.org/), the source are in the
[GiyHub repository Webogram](https://github.com/zhukov/webogram).



There are bridges to IRC with [teleirc](https://github.com/FruitieX/teleirc)
an also to IRC,XMPP, and numerous protocols using
{{< iref "#matterbridge" "Matterbrige" >}} or {{< iref "#libpurple"  "libpurple" >}}.


## Whatsapp {#whatsapp}
{{< wp "WhatsApp" >}} __proprietary__ cross-platform instant messaging
client for smartphones.  It uses the Internet to send text
messages, documents, images, video, user location and audio media
messages to other users using standard cellular mobile numbers.
_WhatsApp_ has been acquired by Facebook in 2014.

There are applications for all kind of mobile phone systems,
 WhatsApp Web is a a client used through a web
browser by syncing with the mobile device's connection.

A Pidgin plug-in called whatsapp-purple aimed to XMPP
interoperability was blocked by whatsapp by blocking the phone
itself that used this application.

_WhatsApp_ uses a customized version of XMPP; Multimedia messages
are sent by uploading the image, audio or video to be sent to an
HTTP server and then sending a link to the content, all messages
are first stored on _WhatsApp_ servers then poll the receiver to
ask an ack, when the message is delivered it is dropped, there is
a miximum time of 30 days for delivery.

_Whatsapp_ has shown [many security breaches
](https://en.wikipedia.org/wiki/WhatsApp#Security) even since the
adoption _but unpublished_ of encryption.

As well _Whatsapp_ as displayed
[many privacy problems ](https://en.wikipedia.org/wiki/WhatsApp#Privacy). In
February 2015, a Dutch university studen proved that anyone could
track a _WhatsApp_ user's status and profile pictures, privacy
settings or status messages regardless of their privacy settings.

Sinxe _Whatsapps_ was acquired by Facebook it is sharing data with
the rest of Facebook’s services. Look at
[Data transfer from WHATSAPP to FACEBOOK: CNIL publicly serves formal
notice for lack of legal basis
](https://www.cnil.fr/en/data-transfer-whatsapp-facebook-cnil-publicly-serves-formal-notice-lack-legal-basis)
_the CNIL is an independent administrative authority that exercises
its functions with accordance to the French Data Protection Act_.

if you have to use it read the
{{< iref "#eff_whatsapp" "following guides of the Electronic Frontier Foundation" >}}.

There are many opensource secure alternatives to _WhatsApp_ like
all the {{< iref "#otr" "OTR" >}} and
{{< iref "#omemo" "OMEMO" >}}
clients and if you want some mere extension, at the price of
loosing the interoperability,
{{< iref "#cryptocat" "Cryptocat" >}},
{{< iref "#signal" "Signal" >}},
and
{{< iref "#telegram" "Telegram" >}}.

-   <a name="eff_whatsapp"
    [Electronic Frontier Foundation (EFF)](https://www.eff.org/) guide
    [Surveillance Self-Defense (SSD) HowTo
    ](https://ssd.eff.org/) :
    : [How to: Use WhatsApp on Android
    ](https://ssd.eff.org/en/module/how-use-whatsapp-android),
    [How to: Use WhatsApp on iOS
    ](https://ssd.eff.org/en/module/how-use-whatsapp-ios).
    The EFF [don't recommend WhatsApp for secure communications
    ](https://www.eff.org/deeplinks/2016/10/where-whatsapp-went-wrong-effs-four-biggest-security-concerns)
-   <a name="yowsup"</a>[Yowsup](https://github.com/tgalal/yowsup)
    (GPL) a python library that enables you build application which
    use WhatsApp service. It includes a client application
    [yowsupcli](https://github.com/tgalal/yowsup/wiki/yowsup-cli-2.0)

    _It seems that WhatsApp now detect Yowsup and  ban  your number, so don't use it
    until they find a workaround_.

    Yowsup allows you to login and use the WhatsApp service, providing
    encryption of messages. This program can be used for multiple
    purposes as to send message to phones, receive messages from
    network servers or appliances, notifying about issues, via direct
    command or by special agents. There is also a
    {{< iref "irc#weechat" "WeeChat" >}} plugin using
    Yowsup library.
-   [Whatsapp-Desktop](https://github.com/Enrico204/Whatsapp-Desktop)
    (GPL) Unofficial whatsapp web desktop client for OSX, Linux and
    Windows. Build with Electron.
-   {{< iref "#franz5" "Franz5" >}} supports _Whatsapp_.
-   {{< iref "#libpurple" "libpurple" >}} has a
    {{< iref "#pidgin_plugins" "plugin" >}} for WhatsApp.

## Other secure messengers
-   [surespot](https://www.surespot.me/)
    is an encrypted messenger for Android and IOS, the Gihub repo has
    also a javascript node server. _Surespot_ uses 256 bit
    AES-GCM encryption using keys created with 521 bit ECDH
    your key is not stored on the servers, and support voice messages,
    emoji, pictures, multiple identities, multiple devices,
    authentication.

    As many encryption software, one of its drawback is to allow only
    communication with people holding the same software. One other
    havoc is the lack of perfect of forward security.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
