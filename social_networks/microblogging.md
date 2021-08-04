---
title: Micro Blogging
---


See also the related page {{< iref "xmpp" "XMPP" >}},
{{< iref "irc" "IRC" >}},
{{< iref "sip" "SIP" >}} and
{{< iref "p2p" "P2P" >}}.

-----------------

# References
-   Wikipedia:  {{< wp "Microblogging" >}},
    {{< wp "Comparison of microblogging services" >}}
-   [Activity Streams](http://wiki.activitystrea.ms/w/page/1359261/FrontPage)
    is an open format specification for activity stream protocols,
    which are used to syndicate activities taken in social web
    applications and services.
    -   [Activity Streams Protocol Home](http://activitystrea.ms/)

For messaging applications, {{< iref "irc" "IRC" >}} came first using a de-facto
communication protocol, but without any standard, but soon many RFC appeared following
the evolution of IRC, but their support is irregular among clients.

{{< iref "xmpp" "XMPP" >}} enhanced the IRC protocol with an open standard, in XMPP the
diverse clients can communicate together, ven if all clients don't implement the same
RFC for some features like encryption. XMPP also allow to speak with other protocols
through Gateways.

The socials networks add to messaging, groups and privacy _yet available in XMPP_ and
services such as channels, blogging or micro-bloging, status mesage, media sharing, and
more.

Some private source social networks like Twitter or {{< iref "#facebook" "Facebook" >}}
don't care about communicating with software from an other source, and even try to
forbid it.

But open source software may communicate, but to do so they need either a common
protocol or a bridge.

For the older platforms they use their own protocol it is the case of
{{< iref "#diaspora" "Diaspora" >}} and {{< iref "#pumpio" "Pump.io" >}}.

The newer platforms use an open source protocol like
{{< iref "#ostatus" "Ostatus"  >}} and {{< iref "#activitypub" "ActivityPub" >}}.


When no common protocol exist, very often connectors or bridges allow
to communicate using at best a status protocol or at least a messaging
one like the open source IRC and XMPP, or the closed source
{{< iref "#slack" "Slack" >}},
twitter or {{< iref "#facebook" "Facebook messenger" >}}.


## Ostatus {#ostatus}
Many opensource microblogging frameworks now use the {{< wp "Ostatus" >}}
open standard for distributed status updates. The
[Ostatus Wiki](https://www.w3.org/community/ostatus/wiki/Main_Page)
contains the Ostatus documentation.

Ostatus allows federation of distinct services implementing the
protocol. The {{< wp "Ostatus" >}} protocol is implemented by
the following services in this section:
{{< iref "#friendica" "Friendica" >}},
{{< iref "#gnusocial" "Gnu Social" >}},
{{< iref "#mastodon" "Mastodon" >}}.

## ActivityPub {#activitypub}

The {{< iref "#ostatus" Ostatus >}} protocol is enhanced by the {{< wp "ActivityPub" >}}
protocol which allow more security for private messages. {{< wp "ActivityPub" >}} is an
extension of the {{< iref "#pumpio" "Pump.io" >}} protocol.

W3C publish
[W3C Recommendation for ActivityPub
](https://www.w3.org/TR/2018/REC-activitypub-20180123/)
which constitutes also the
[AcivityPub Home Page](http://w3c.github.io/activitypub/)
in the [W3C Github pages](https://w3c.github.io/).

The [AcivityPub repository](https://github.com/w3c/activitypub) is also in
[GithUb W3C repository](https://github.com/w3c/).



<a name="fediverse"></a>[Fediverse](https://fediverse.party/) is a common name for
federated social networks running on free open software which can intercommunicate with
each other. User known by an identity are able to post text and other media, or to
follow posts by other identities.

Fediverse includes [many applications](https://fediverse.party/en/miscellaneous) among
which
{{< iref "#friendica" "Friendica" >}},
{{< iref "#gnusocial" "Gnu Social" >}},
{{< iref "#mastodon" "Mastodon" >}},
{{< iref "#pleroma" "Pleroma" >}},
{{< iref "#diaspora" "Diaspora" >}}.

The {{< wp "Fediverse" "Fediverse Wikipedia page"  >}} has a
{{< wp "Fediverse#Fediverse_software_platforms" "table of Fediverse software platforms" >}}.

# Microblogging and social networks
Some microblogging servers are refered to in the
{{< iref "xmpp" "Xmpp Section" >}} as
{{< iref "xmpp#retroshare" "Retroshare" >}}


-   The most known closed private license services are
    {{< iref "#facebook" "Facebook" >}}, {{< wp "Twitter" >}} which track you and
    make you swallow ads.
-   [Open Source Twitter Alternatives - AlternativeTo.net
    ](http://alternativeto.net/software/twitter/?license%3Dopensource)

-   <a name="diaspora"></a>[Diaspora](https://diasporafoundation.org/)
    is an open source social network, _à la Facebook_ which enforce
    decentralization, freedom and privacy. Diaspora is part of
    {{< iref "#fediverse" "Fediverse" >}}

    -   [Getting started in Diaspora tutorial
        ](https://diasporafoundation.org/tutorials).
    -   [Diaspora Wiki](https://wiki.diasporafoundation.org/).
    -   [Diaspora GitHub repository
        ](https://github.com/diaspora/diaspora).
    -   [ArchWiki: Diaspora
        ](https://wiki.archlinux.org/index.php/Diaspora)
    -   [Diaspora fr](https://diaspora-fr.org/).
    -   [Framasphère](https://framasphere.org/)
        is a french node of Diaspora, it is among the most used nodes,
        and is maintained by [Framasoft](https://framasoft.org/)
        a French network dedicated to globally promoting  free software.
    -   [Diaspora : Le guide du parfait débutant
        ](https://fr.wikibooks.org/wiki/Diaspora_:_Le_guide_du_parfait_d%C3%A9butant)
        un WikiBook.
    -   [diaspora federation protocol](https://diaspora.github.io/diaspora_federation/)
-   [dweet.io](http://dweet.io/) messaging (and alerts) for the
    Internet of Things.
    -   [dweet.io - FAQ](http://dweet.io/faq),
    -   [dweet.io – Twitter for Social Machines
        ](http://www.artandlogic.com/blog/2014/08/dweet-io-twitter-for-social-machines/),
    -   [Why tweet when you can dweet??
        ](http://www.element14.com/community/community/design-challenges/forget-me-not/blog/2014/08/29/fmn05-why-tweet-when-you-can-dweet),
    -   [dweet.io (@dweet_io) | Twitter
        ](https://twitter.com/dweet_io)
-   <a name="friendica"></a>{{< wp "Friendica" >}} (AGPL)
    is a decentralised communications platform written in PHP/MySQL
    that integrates social communication. It support many
    communication protocols like  {{< iref "#ostatus" Ostatus >}}
    {{< iref "#diaspora" "Diaspora" >}}. As a member of
    {{< iref "#fediverse" "Fediverse" >}} you can connect with other
    {{< iref "#fediverse" "Fediverse" >}} software like
    {{< iref "#gnusocial" "Gnu Social" >}},
    {{< iref "#mastodon" "Mastodon" >}} {{< iref "#hubzilla" "Hubzilla" >}}
    and connectors allow also to join
    Facebook, Twitter, {{< iref "#pumpio" "Pump.io" >}}.

    In addition to these two way connections, users can also use Friendica as a
    publishing platform to post content to  WordPress, Tumblr and Libertree.

-   [Friendica Home Page](https://friendi.ca/)
    -   [Friendica public servers
        ](https://dir.friendica.social/servers)
    -   [GitHub - Friendica](https://github.com/friendica/friendica)
    -   [GitHub - Friendica add-ons
        ](https://github.com/friendica/friendica-addons)
        where you find the available connectors.

-   <a name="hubzilla"></a>[Hubzilla
    ](https://zotlabs.org/page/hubzilla/hubzilla-project)
    is an Open source platform for creating interconnected websites featuring a
    decentralized identity, communications, and permissions framework.

    It provides discussion threads, cloud file storage, CalDAV and CardDAV, CMS, wiki.
    See the  [table of Hubzilla features
    ](https://zotlabs.org/page/zotlabs/comparison+hubzilla+zap).

    It is based on the [Zot Protocol](https://start.hubzilla.org/page/admin/zot_intro).
    a JSON-based web framework for implementing secure decentralised communications and
    services. It differs from many other communication protocols by building
    communications on top of a decentralised identity and authentication framework.
    and belongs to  {{< iref "#fediverse" "Fediverse" >}} network.

    It supports many protocols {{< iref "#ostatus" "Ostatus" >}},
    {{< iref "#activitypub" "ActivityPub"  >}}, {{< iref "#diaspora" "Diaspora" >}},
    {{< iref "#pumpio" "Pump.io" >}}, Dreamwith, InsaneJournal, Libertree, LiveJournal,
    Twitter, WordPress.

    -   [Hubzilla Public Hubs](https://hubzilla.rocks/pubsites)
    -   [list of all nodes](https://the-federation.info/hubzilla)
    -   [Hubzilla source repository](https://framagit.org/hubzilla/core)
    -   [Hubzilla documentation](https://zotlabs.org/help/en/about/about)

-   <a name="gnusocial"></a>{{< wp "GNU social" >}} (GPL)
    previously known as StatusNet is a microblogging server written
    in PHP that implements the {{< iref "#ostatus"  "OStatus" >}} standard for
    interoperation. It publish updates via an XMPP/Jabber client,
    and provide a Twitter-compatible API. GnuSocial is part of
    {{< iref "#fediverse" "Fediverse" >}} network.
    -   [Gnu Social Home](https://gnu.io/social)
    -   Wikipedia {{< wp "GNU social" >}}
    -   {{< iref "#bitlbee" "BitlBee" >}} has support for
        Gnu Social.
-   <a name="pleroma"></a>[Pleroma](https://pleroma.social/) (AGPL)
    is a federated social networking server,
    based on "{{< iref "#activitypub" "ActivityPub" >}} protocol it is part of
    {{< iref "#fediverse" "Fediverse" >}} network and compatible with
    {{< iref "#gnusocial" "Gnu Social" >}},
    {{< iref "#mastodon" "Mastodon" >}} and other {{< iref "#fediverse" "Fediverse" >}}
    software.
    -   [Introduction to Pleroma](https://blog.soykaf.com/post/what-is-pleroma/)
-   {{< iref "xmpp#tox" "Tox" >}} provides
    messaging, group messaging, voice and video calling, voice and
    video conferencing, typing indicators, message read-receipts, file
    sharing, profile encryption, and desktop sharing.
    It is referenced
    {{< iref "xmpp#tox" "in the Xmpp page" >}}
-   [Trsst](http://www.trsst.com/) (apache license)
    encrypted and anonymized and decentralized alternative to
    Twitter. _Dead project last commit 2014_.
-   [twister](http://twister.net.co/) (MIT License)
    an Encrypted P2P microblogging platform.
    -   [Twister – An Open Source, Encrypted, Peer-to-Peer
        Alternative to Twitter - Infosecurity Magazine
        ](http://www.infosecurity-magazine.com/news/twister-an-open-source-encrypted-peer-to-peer/)
    -   GitHub [twister-core
        ](https://github.com/miguelfreitas/twister-core) and
        [twister-html](https://github.com/miguelfreitas/twister-html).

## Matrix {#matrix}
{{< wp "Matrix" >}} is an open protocol for real-time communication. It allows to users
to communicate via online chat, Voice over IP, and Videotelephony. It provides HTTP APIs
and open source reference implementations for securely distributing and persisting
messages in JSON format over an open federation of servers It can integrate with
standard web services via {{< wp "WebRTC" >}}.Matrix is not a pure peer-to-peer system;
instead each user has a well-defined homeserver which stores his data and that he can
depend upon.

-   [The Faq](https://matrix.org/docs/guides/faq.html)
    Explain the differences between Matrix and IM applications like Xmpp, Tox and other.
-   There are planty of [Matrix projects](https://matrix.org/docs/projects/).
-   <a name="element"></a>[Riot.im](https://riot.im/)
    [Element](https://element.io/) (Apache License)
    _formerly riot.im, formerly Vector_
    is an internet messaging app for group chat voip & video calling file transfer.  It
    is built on the top of Matrix. It has clients for Linux, Mac OS X, IOS, Android,
    Windoze, we can also use a Web interface.  That make it one of the F2F communication
    tool with the broader support.

    Element has a Debian package _element-desktop_ in a deb repository.

    -   [Element Web interface](https://app.element.io/).
-   [weechat-matrix-protocol-script
    ](https://github.com/torhve/weechat-matrix-protocol-script)
    is a {{< iref "irc#weechat" "WeeChat" >}} script in Lua that implements
    the matrix.org chat protocol.
-   [weechat-matrix](https://github.com/poljar/weechat-matrix)
    a Weechat{{< iref "irc#weechat" "WeeChat" >}} Matrix protocol python script.
    _In Debian._
-   [Unofficial selection of public Matrix servers
    ](https://www.hello-matrix.net/public_servers.php)
-   [Matrix Public Homeservers](https://www.anchel.nl/matrix-publiclist/)
-   [Matrix bridges](https://matrix.org/bridges/) the irc bridge is builtin,
    some public servers provide a bridge like [Telegram at utwente.io
    ](https://syscom.utwente.io/info/matrix/telegram/) or [t2bot.io
    ](https://t2bot.io/telegram/). The server [t2bot.io
    ](https://t2bot.io/) provides many bridges and bot: telegram, discord,
    [Slack compatible webhooks
    ](https://github.com/turt2live/matrix-appservice-webhooks),
    and many bots. Other bridges must be self-installed, some have light
    dependencies, some are quite heavy needing even yo have your own home server
    like the WhatsApp bridge.
-   [mxtoot](https://github.com/ma1uta/mxtoot)    (Apache License)
    is a Matrix <=> Mastodon bot written on java.
-    <a name= "zom"></a>[འཛོམས་](https://zom.im/)    or
    [Zom](https://zom.im/zomenglish.html) (Apache License)
    is an ios and android client for the Matrix protocol.
    -   [zom-android-matrix - GitHub](https://github.com/zom/zom-android-matrix)
    -   [zom-ios-matrix](https://github.com/zom/zom-ios-matrix)

## Mastodon {#mastodon}
{{< wp "Mastodon_(software)" "Mastodon" >}} (AGPL) is a federated social network written
in Ruby with front end in JavaScript, with similar microblogging features to Twitter.
It support the {{< iref "#ostatus" "Ostatus" >}} and
{{< iref "#activitypub" "ActivityPub" >}} protocols.  Each message has a privacy option,
private messages are only shared on the timelines of the user's followers, or can be
direct between users.

Mastodon is part of {{< iref "#fediverse" "Fediverse" >}} network.

-   [Mastodon Home](https://joinmastodon.org/)
    contains the list of public servers.
-   [GitHub - Mastodon](https://github.com/tootsuite/mastodon).
-   [Mastodon documentation](https://docs.joinmastodon.org/)
    including the [FAQ
    ](https://github.com/tootsuite/documentation/blob/master/Using-Mastodon/FAQ.md)
    and the [List of apps
    ](https://github.com/tootsuite/documentation/blob/master/Using-Mastodon/Apps.md)
    -   [Mastodon Documentation Source
        ](https://github.com/tootsuite/documentation)
-   [Mastodon Blog](https://blog.joinmastodon.org/)
    -   [Guides](https://blog.joinmastodon.org/categories/guides/)
-   [Awesome Mastodon](https://github.com/tleb/awesome-mastodon)
    Curated list of Mastodon-related stuff!
-   [Framapiaf](https://framapiaf.org) is the Mastodon instance of
    [Framasoft](https://framasoft.org/).
-   [umr](https://github.com/Ulrar/umrc)
    is a bot to allow using a Mastodon account from IRC
-   {{< iref "xmpp#bitlbee" "BitlBee" >}}
    [plugin for Mastodon](https://github.com/kensanata/bitlbee-mastodon),
    [How to Mastodon - BitlBee Wiki](https://wiki.bitlbee.org/HowtoMastodon),
    this plugin is also available from Debian..
-   [Mastodon Twitter Crossposter](https://crossposter.masto.donte.com.br/) is a
    service which allows you to connect a Mastodon account and a Twitter account and
    enable cross-posting between them.
-   [Moa](https://moa.party/) Link your Mastodon account to Twitter and Instagram.
    The code is on GitHub.
-   [Mastodon.py](https://github.com/halcy/Mastodon.py) (MIT License)
    Python wrapper for the Mastodon API. It is in the Debian package _python3-mastodon_.
    -   [Mastodon.py documentation](https://mastodonpy.readthedocs.io/en/stable/).

### Mastodon clients
-   [Brutaldon](https://git.carcosa.net/jmcbray/brutaldon) (AGPL)
    A [brutalist](https://brutalist-web.design/) web interface for Mastodon written in
    python.  It works in text-mode browsers such as Lynx, w3m, or elinks, and also in
    more heavy-weight graphical browsers, such as Firefox, or on mobile platform.  There
    is a hosted instance at [brutaldon.online](https://brutaldon.online/).
-   [feed2toot](https://gitlab.com/chaica/feed2toot) (MIT License)
    parses rss feeds, identifies new posts and posts them on Mastodon.
-   [madonctl](https://github.com/McKael/madonctl) (MIT License)
    a Go language mastodon CLI.
-   [mastodon.el](https://github.com/jdenen/mastodon.el)
    an Emacs client for Mastodon, you find it in MELPA.
-   [toot](https://github.com/ihabunek/toot/) (GPL)
    is a python Mastodon CLI client. There is also a ncurses UI.
    Since Debian 10 (buster) and Ubuntu 19.04 (disco), a deb package is available.
    -   [toot documentation](https://toot.readthedocs.io/en/latest/).
-   [tootstream](https://github.com/magicalraccoon/tootstream) (MIT License)
    a  python  Mastodon CLI client.

## Pump.io {#pumpio}
{{< wp "Pump.io" >}} (Apache License) is an activity streams engine that can be
used as a federated social networking protocol Pump.io is written in
Node.js and uses Activity Streams as the format for commands and to
transfer data via a simple REST inbox API.

Pump.io is the server software of many social networking sites,
including the well known {{< wp "Identi.ca" >}}. Pump.io is not tied to a
single site. Users across servers can subscribe to each other.

{{< wp "Identi.ca" >}} and other Pump.io sites accept reading and posting
through the Pump.io API and web, Xmpp, email, SMS, you can also
read as Atom or RSS streams.

-   [Pump.io Home](http://pump.io/)
-   [Pump.io User Guide
    ](https://github.com/e14n/pump.io/wiki/User-Guide)
-   [Pump.io FAQ
    ](https://github.com/e14n/pump.io/wiki/FAQ)
-   [Pump.io Clients](https://github.com/e14n/pump.io/wiki/Clients)
-   [Getting Started With Pump.io
    ](http://polari.us/dokuwiki/doku.php?id=gettingstartedwithpumpio)
    by Stephen Sekula.
-   [Communication Freedom
    ](https://communicationfreedom.wordpress.com/)
    How To  [Pump.io
    ](https://communicationfreedom.wordpress.com/pump-io/),
    [Some tips for a better experience using the Pump.io network
    ](https://communicationfreedom.wordpress.com/2014/03/17/pump-io-tips/)
-   [pumpio-el](https://github.com/cnngimenez/pumpio-el)
    is an emacs client for Pump.io. [Emacs Wiki : PumpioEl
    ](https://www.emacswiki.org/emacs/PumpioEl)
-   [Pump.io command line utility "p"
    ](https://github.com/xray7224/p) is the version for Pump.io
    of the [Twitter commande line utility t
    ](https://github.com/sferik/t) the author
    Jessica _xray7224_ also develop the python library
    [PyPump](https://github.com/xray7224/PyPump).
-   [Pump.io protocol and API](https://github.com/pump-io/pump.io/blob/master/API.md)
-   [MediaGoblin](http://mediagoblin.org/) (GPL)
    is a media publishing platform that anyone can run.  It is powered by
    {{< iref "#pumpio" "Pump.io" >}}.

## Facebook {#facebook}

-   [Reasons not to use Facebook
    ](<https://stallman.org/facebook.html>) Richard Stallman.
-   [Get your loved ones off Facebook
    ](<http://www.salimvirani.com/facebook/>)
-   [Protecting Yourself on Social Networks
    ](https://ssd.eff.org/en/module/protecting-yourself-social-networks)
-   [Pas de « Facebook » pour moi - L'internet rapide et permanent
    ](http://irp.nain-t.net/doku.php/nofb)
-   [What Facebook fails to recognise | The Guardian
    ](https://www.theguardian.com/commentisfree/cifamerica/2011/jun/14/facebook-facial-recognition-software)
-   [IEE: How To Opt Out of Receiving Facebook Ads Based on Your
    Real-Life Shopping Activity
    ](https://www.eff.org/deeplinks/2013/02/howto-opt-out-databrokers-showing-your-targeted-advertisements-facebook)
-   [Maskbook](https://maskbook.com/) encrypt your post on Facebook, you can choose who
    can decrypt.

If you truly need to use FaceBook messenger you can do it via an xmpp
client with Facebook support like
{{< iref "xmpp#profanity" "Profanity" >}}, or a
bridge like {{< iref "xmpp#bitlbee" "BitlBee" >}},
the client or bridges powered by
{{< iref "xmpp#libpurple" "libpurple" >}} like
{{< iref "xmpp#pidgin" "Pidgin" >}},
{{< iref "xmpp#spectrum2" "Spectrum2" >}},
{{< iref "xmpp#minbif" "minbif" >}}.

# Team collaborative software
I group here _Slack like_ software. IRC-like features:
- persistent and private chat rooms (channels) organized by topic,
  direct messaging
- Privacy organized by groups or _teams_.
- integratetion with third-party services


-   <a name="slack"></a>{{< wp "Slack_(software)"  "Slack" >}}
    is a cloud-based set of proprietary team collaboration tools and
    and messaging system for teams, there are now many open sources
    alternatives, see below.

    Many gateways bridge slack with IRC and XMPP
    after closing of old  official [IRC and XMPP gateway
    ](https://get.slack.help/hc/en-us/articles/201727913-Connect-to-Slack-over-IRC-and-XMPP)
    -   {{< iref "xmpp#weechat" "WeeChat" >}} has a
        plugin using native Slack api.
    -   {{< iref "xmpp#matterbridge" "matterbrige" >}}
        support Slack.
    -   {{< iref "xmpp#franz5" "Franz 5" >}}
    -   a {{< iref "xmpp#pidgin_plugins" "libpurple plugin" >}} used by
        Pidgin, {{< iref "xmpp#bitlbee" "BitlBee" >}} and
        {{< iref "xmpp#spectrum2" "Spectrum2" >}}.
    -   [slack-irc](https://github.com/ekmartin/slack-irc)
        is a slack irc bridge.
    -   {{< iref "xmpp#matterbridge" "matterbrige" >}} support Matrix.

-   <a name="gitter"></a>{{< wp "Gitter" >}} (MIT License)
    is an instant messaging and chat room system for developers and
    users of GitHub repositories. Individual chat rooms can be created
    for individual git repositories on GitHub private or public
    depending of the privacyof the associated repository.
    It automatically logs all messages in the cloud.
    Official Gitter apps for Windows, Mac, Linux, iOS and Android are
    available.
    -   [Gitter.im](https://gitter.im/)
    -   [Gitter IRC bridge](https://irc.gitter.im/)
        Connect to Gitter using the IRC protocol. at:
        host: irc.gitter.im, port: 6667 (or 6697).
        -   [client configuration
            ](https://github.com/gitterHQ/irc-bridge/wiki/Client-configuration)
        -   [source of the gitter-irc bridge
            ](https://github.com/gitterHQ/irc-bridge)
        -   [gitter.el](https://github.com/xuchunyang/gitter.el)
            is an Emacs Gitter client, with a partial support of the
            protocol. It is in melpa. You can also use an emacs IRC
            client with the gitter bridge.
        -   {{< iref "xmpp#matterbridge" "matterbrige" >}} support Gitter.
-   {{< iref "#element" "Element" >}} is above with the
    {{< iref "#matrix" "Matrix protocol" >}}.
-   <a name="rocketchat"></a>{{< wp "Rocket.Chat" >}} (MIT License)
    is an instant messaging and chat room system. There are electron based desktop
    application, ios, android, and web interfaces.  An xmpp access is under development.

    There is a {{< iref "xmpp#pidgin_plugins" "purple plugin" >}} for Rocket.Chat,
    {{< iref "xmpp#matterbridge" "matterbrige" >}}
    support Rocket.Chat

-   <a name="mattermost">[Mattermost](https://github.com/mattermost/mattermost-server)
    (MIT License)
    is an open source private cloud, Slack-alternative.  It's written in Golang and
    React and runs as a single Linux binary with MySQL or PostgreSQL.
    -   [Mattermost Inc.](https://about.mattermost.com/) run Mattermost Entreprise and
        has a free plan for a for small teams.
    -   There are many solutions of [Mattermost Integration
        ](https://docs.mattermost.com/overview/integrations.html)
    -   [Zapier](https://zapier.com/) allows to
        [integrates to a huge list of Apps and Clouds
        ](https://about.mattermost.com/community-applications/).
    -   Several bridges provide XMPP/IRC access :  a
        {{< iref "xmpp#pidgin_plugins" "purple plugin" >}},
        {{< iref "xmpp#matterbridge" "matterbrige" >}}.
    -   [Framateam](https://framateam.org) is the mattermost instance
        of [Framasoft](https://framasoft.org/).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
