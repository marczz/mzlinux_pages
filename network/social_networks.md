---
title: Social Networks
---

{{% toc /%}}

See also the related page {{< iref "xmpp" "XMPP" >}},
{{< iref "irc" "IRC" >}},
{{< iref "sip" "SIP" >}} and
{{< iref "p2p" "P2P" >}}.

-----------------

# References
-   Wikipedia: {{< wp "Social Software" >}} with references to specific service
    page, {{< wp "Social networking service" >}}, {{< wp "Distributed social network" >}},
    {{< wp "Comparison of software and protocols for distributed social networking" >}},
    {{< wp "List of social networking websites" >}},
    {{< wp "Microblogging" >}}, {{< wp "Comparison of microblogging services" >}}
-   [Activity Streams](http://wiki.activitystrea.ms/w/page/1359261/FrontPage)
    is an open format specification for activity stream protocols,
    which are used to syndicate activities taken in social web
    applications and services.
    -   [Activity Streams Protocol Home](http://activitystrea.ms/)

Most opensource microblogging frameworks now use the {{< wp "Ostatus" >}}
open standard for distributed status updates. The [W3c Ostatus
Home Page](https://www.w3.org/community/ostatus/)
seems quite outdated but the
[Wiki](https://www.w3.org/community/ostatus/wiki/Main_Page)
contains the Ostatus documentation.

Ostatus allows federation of distinct services implementing the
protocol. The {{< wp "Ostatus" >}} protocol is implemented by
the following services in this section:
{{< iref "#friendica" "Friendica" >}},
{{< iref "#gnusocial" "Gnu Social" >}},
{{< iref "#mastodon" "Mastodon" >}}.

The Ostatus protocol is enhanced by the {{< wp "ActivityPub" >}} protocol which
allow more security for private messages. {{< wp "ActivityPub" >}} is an
extension of the Pump.io protocol.

W3C has a [W3C Recommendation for ActivityPub] and on GithUb the
[AcivityPub Home Page](http://w3c.github.io/activitypub/) and
[repository](https://github.com/w3c/activitypub).

The XMPP based software can communicate together by the XMPP protocol.

{{< iref "#diaspora" "Diaspora" >}} uses it's own protocol as
{{< iref "#pumpio" "Pump.io" >}}.

When no common protocol exist, very often connectors or bridges allow
to communicate using at best a status protocol or at least a messaging
one like the open source IRC and XMPP, or the closed source Slack,
twitter or Facebook messenger.


# Microblogging and social networks
Some microblogging servers are refered to in the
{{< iref "xmpp" "Xmpp Section" >}} as
{{< iref "xmpp#jappix" "Jappix" >}},
{{< iref "xmpp#retroshare" "Retroshare" >}}


-   The most known closed private license services are
    {{< wp "Facebook" >}}, {{< wp "Google+" >}}, {{< wp "Twitter" >}} this gang of three are
    making you swallow ads.
-   [Open Source Twitter Alternatives - AlternativeTo.net
    ](http://alternativeto.net/software/twitter/?license%3Dopensource)

-   <a name="diaspora"></a>[Diaspora](https://diasporafoundation.org/)
    is an open source social network, _à la Facebook_ which enforce
    decentralization, freedom and privacy.
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
-   [dweet.io](http://dweet.io/) messaging (and alerts) for the
    Internet of Things.
    -   [dweet.io - FAQ](http://dweet.io/faq),
    -   [dweet.io – Twitter for Social Machines
        ](http://www.artandlogic.com/blog/2014/08/dweet-io-twitter-for-social-machines/),
    -   [Why tweet when you can dweet??
        ](http://www.element14.com/community/community/design-challenges/forget-me-not/blog/2014/08/29/fmn05-why-tweet-when-you-can-dweet),
    -   [dweet.io (@dweet<sub>io</sub>) | Twitter
        ](https://twitter.com/dweet_io)
-   <a name="friendica"></a>{{< wp "Friendica" >}} (AGPL)
    is a decentralised communications platform written in PHP/MySQL
    that integrates social communication. It support many
    communication protocols like Ostatus (Gnu Social, Mastodon) ,
    Diaspora and connectors allow also to join Facebook, Pump.io,
    Libertree, Twitter, Google+, Wordpress and Tumblr and others.

    -   [Friendica Home Page](https://friendi.ca/)
    -   [Friendica public servers
        ](https://dir.friendica.social/servers)
    -   [GitHub - Friendica](https://github.com/friendica/friendica)
    -   [GitHub - Friendica add-ons
        ](https://github.com/friendica/friendica-addons)
        where you find the available connectors.


-   <a name="gnusocial"></a>{{< wp "GNU social" >}} (GPL)
    previously known as StatusNet is a microblogging server written
    in PHP that implements the {{< wp "OStatus" >}} standard for
    interoperation. It publish updates via an XMPP/Jabber client,
    and provide a Twitter-compatible API.
    -   [Gnu Social Home](https://gnu.io/social)
    -   Wikipedia {{< wp "GNU social" >}}
    -   {{< iref "#bitlbee" "BitlBee" >}} has support for
        Gnu Social.
-   <a name="keybase">[keybase](https://keybase.io/) (BSD Licence)
    is a security app for mobile phones and computers powered by
    public-key cryptography.
    -   [keybase docs](https://keybase.io/docs)
    -   <a name="kbpgp">[kbpgp](https://keybase.io/kbpgp)
        is Keybase's implementation of PGP in JavaScript
        it is used in the client side web pgp key generators
        [Fncontact - Pgpkeys](https://fncontact.com/pgpkeys),
        [PgpKeyGen](https://pgpkeygen.com/)
-   <a name="matrix"></a>{{< wp "Matrix" >}}
    is an open protocol for real-time communication. It
    allows to users to communicate via online chat, Voice over IP, and
    Videotelephony. It provides HTTP APIs and open source reference
    implementations for securely distributing and persisting messages
    in JSON format over an open federation of servers.[2][3] It can
    integrate with standard web services via {{< wp "WebRTC" >}}.Matrix is not
    a pure peer-to-peer system; instead each user has a well-defined
    homeserver which stores his data and that he can depend upon.

    -   [The Faq](https://matrix.org/docs/guides/faq.html)
        Explain the differences between Matrix and IM applications
        like Xmpp, Tox and other.
    -   There are planty of [Matrix projects
        ](https://matrix.org/docs/projects/).
    -   <a name="riotim"></a>[Riot.im](https://riot.im/)
        _formerly Vector_ (Apache License)
        is an internet messaging app for group chat voip & video
        calling file transfer.  It is built on the top of Matrix. It
        has clients for Linux, Mac OS X, IOS, Android, Windoze, we can
        also use a Web interface.  That make it one of the F2F
        communication tool with the broader support.
    -   [weechat-matrix-protocol-script
        ](https://github.com/torhve/weechat-matrix-protocol-script)
        is a WeeChat script in Lua that implements the matrix.org chat
        protocol.

-   {{< wp "Mastodon_(software)"  "Mastodon" >}} (AGPL)
    is a federated social network written in Ruby with front end in
    JavaScript, with similar microblogging features to Twitter.
    It support the Ostatus and  ActivityPub protocols.
    Each message has a privacy option,  private messages are only
    shared on the timelines of the user's followers, or can be direct
    between users.

    -   [Mastodon Home](https://joinmastodon.org/)
        contains the list of public servers.
    -   [GitHub - Mastodon](https://github.com/tootsuite/mastodon).
    -   [Mastodon Documentation
        ](https://github.com/tootsuite/documentation)
        including the [FAQ
        ](https://github.com/tootsuite/documentation/blob/master/Using-Mastodon/FAQ.md)
        and the [List of apps
        ](https://github.com/tootsuite/documentation/blob/master/Using-Mastodon/Apps.md)
        [Awesome Mastodon](https://github.com/tleb/awesome-mastodon)
        Curated list of Mastodon-related stuff!
    -   [Framapiaf](https://framapiaf.org) is the Mastodon instance of
        [Framasoft](https://framasoft.org/).
    -   [umr]((https://github.com/Ulrar/umrc)
        is a bot to allow using a Mastodon account from IRC
    -   {{< iref "xmpp#bitlbee" "BitlBee" >}}
        [plugin for Mastodon
        ](https://github.com/kensanata/bitlbee-mastodon).
    -   [mastodon.el](https://github.com/jdenen/mastodon.el)
        an Emacs client for Mastodon, you find it in MELPA.
    -   [toot](https://github.com/ihabunek/toot/) (GPL)
        is a python  Mastodon CLI client. There is an apt repository
        with the package.
    -   [tootstream](https://github.com/magicalraccoon/tootstream)
        another  python  Mastodon CLI client.
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
    an Encrypted P2P microblogging platform. _active in 2018_
    -   [Twister – An Open Source, Encrypted, Peer-to-Peer
        Alternative to Twitter - Infosecurity Magazine
        ](http://www.infosecurity-magazine.com/news/twister-an-open-source-encrypted-peer-to-peer/)
    -   GitHub [twister-core
        ](https://github.com/miguelfreitas/twister-core) and
        [twister-html](https://github.com/miguelfreitas/twister-html).

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
-   [Pump.io command line utility p
    ](https://github.com/xray7224/p) is the version for Pump.io
    of the [Twitter commande line utility t
    ](https://github.com/sferik/t) the author
    Jessica _xray7224_ also develop the python library
    [PyPump](https://github.com/xray7224/PyPump).


-   [MediaGoblin](http://mediagoblin.org/) (GPL)
    is a media publishing platform that anyone can run.
    It is powered by {{< iref "#pumpio" "Pump.io" >}}.

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

    The official [IRC and XMPP gateway
    ](https://get.slack.help/hc/en-us/articles/201727913-Connect-to-Slack-over-IRC-and-XMPP)
    has stopped, but there are alternatives.
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
-   {{< iref "#riotim" "Riot.im" >}} is above with the
    {{< iref "#matrix" "Matrix protocol" >}}.
-   <a name="rocketchat"></a>{{< wp "Rocket.Chat" >}} (MIT License)
    is an instant messaging and chat room system. There are electron
    based desktop application, ios, android, and web interfaces.
    An xmpp access is under development.

    There is a {{< iref "xmpp#pidgin_plugins" "purple plugin" >}} for Rocket.Chat,
    {{< iref "xmpp#matterbridge" "matterbrige" >}}
    support Rocket.Chat

-   <a name="mattermost">[Mattermost](https://about.mattermost.com/)
    (MIT License) is a  private cloud, Slack-alternative.
    It's written in Golang and React and runs as a single Linux binary
    with MySQL or PostgreSQL.
    Mattermost has a free plan for a self-hosted  instance for small
    teams.

    There are many solutions of [Mattermost Integration
    ](https://docs.mattermost.com/overview/integrations.html)

    It [integrates to a huge list of Apps and Clouds]
    ](https://about.mattermost.com/community-applications/), though
    [Zappier](https://zapier.com/).

    For XMPP/IRC access we there is:  a {{< iref "xmpp#pidgin_plugins" "purple plugin" >}},
    {{< iref "xmpp#matterbridge" "matterbrige" >}},

    -   [GitHub Mattermost Server
        ](https://github.com/mattermost/mattermost-server)
    -   [Framateam](https://framateam.org) is the mattermost instance
        of [Framasoft](https://framasoft.org/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
