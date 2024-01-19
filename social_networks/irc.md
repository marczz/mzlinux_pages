---
title: IRC

---

A page from{{< iref "social_networks" "Social Networks section" >}}.

See also {{< iref "xmpp" "XMPP" >}},
{{< iref "microblogging" "Micro Blogging" >}},
{{< iref "sip" "SIP" >}} and
{{< iref "p2p" "P2P" >}}.

# Common Internet Messaging refs
-   Wikipedia: {{< wp "Instant messaging" >}},
    {{< wp "list of instant messaging protocols" >}},
    {{< wp "Comparison of instant messaging protocols" >}},
    {{< wp "Comparison of instant messaging clients" >}},
    {{< wp "Instant messaging" >}}.


# IRC References

Some Jabber clients are also supporting IRC, they are listed in the
{{< iref "xmpp" "XMPP Page" >}}. There are also jabber to irc gateways that allow to
connect to irc from any jabber client.

-   Wikipedia:  {{< wp "Internet Relay Chat" >}},
    {{< wp "Comparison of Internet Relay Chat clients" >}},
    {{< wp "Comparison of instant messaging protocols" >}},
    {{< wp "Internet Relay Chat services" >}},
    {{< wp "Comparison of Internet Relay Chat services" >}},
    {{< wp "IRC daemon" >}},
    {{< wp "Comparison of Internet Relay Chat daemons" >}},
    {{< wp "List of Internet Relay Chat commands" >}}
-   [Awesome IRC](https://github.com/davisonio/awesome-irc)
    a list of tools, software & other resources related to the Internet Relay Chat (IRC)
    protocol.
-   Wikibooks: [Internet Technologies/IRC
    ](https://en.wikibooks.org/wiki/Internet_Technologies/IRC),

-   RFC:
    -   [RFC 1459](http://www.faqs.org/rfcs/rfc1459.html) - Original IRC Protocol,
    -   [RFC 2810](http://www.faqs.org/rfcs/rfc2810.html) - Updated IRC Architecture,
    -   [RFC 2811](http://www.faqs.org/rfcs/rfc2811.html) - Channel Management,
    -   [RFC 2812](http://www.faqs.org/rfcs/rfc2812.html) - IRC Client Protocol,
    -   [RFC 2813](http://www.faqs.org/rfcs/rfc2813.html) - Server Protocol.
-   [IRCv3 Specifications - IRCv3](https://ircv3.net/irc/)
-   [Internet Relay Chat Help](http://www.irchelp.org/) or _irchelp_, comprehensive set
    of resources for IRC.
    -   [The IRC Prelude](https://www.irchelp.org/faq/new2irc.html) basic IRC
        documentation,
    -   [An IRC Tutorial](https://www.irchelp.org/irchelp/irctutorial.html)
    -   [IRCHelp.org — Privacy on IRC](https://www.irchelp.org/security/privacy.html).
-   [Libera Chat](https://libera.chat/)
    IRC network for FOSS projects collaboration. It replaced
    {{< wp "Freenode" >}} after the takeover by the businessman Andrew Lee,
    and the staff of Freenode and all the FOSS projects moved from frenode to
    libera.chat.
    -   Wikipedia {{<wp "Libera Chat" >}} and   {{<wp "Freenode" >}}
    -   [Guides | Libera Chat](https://libera.chat/guides)
         explain _Choosing a client_, _Connecting to libera.chat_, _Connecting with
         SASL_,  _Nickname Registration_, _Channels use and administration_.
    -   [Libera Chat Web client](https://web.libera.chat/) is an instance of
        {{< iref "#kiwiirc" "KiwiIRC" >}}.
    -   [Libera Chat - gamja web client](https://web.libera.chat/gamja/) is an instance
        of {{< iref "#gamja" "Gamja" >}}.
-   IRC Channel discovery:
   -   In a client connected to a server you can do `/list *keyword*`.
   -   [Search Irc](https://search.mibbit.com/) for channels or servers.
   -   [IRC Chat Rooms Search - netsplit.de](https://netsplit.de/channels/)
       Search chat rooms among 500 IRC networks.
-      [IRC access from Matrix - Meta](https://meta.wikimedia.org/wiki/Matrix.org)

## IRC Commands
A List of commands is givent in Wikipedia: {{< wp "List of IRC Commands" >}}
and also available in the help of most clients.

-   [IRC - Wikibook: Basic commands
    ](https://en.wikibooks.org/wiki/Internet_Technologies/IRC#Basic_commands)
-   [IRC/Instructions - meta.wikimedia
    ](https://meta.wikimedia.org/wiki/IRC/Instructions)
    explains how you connect to the libera.chat IRC network. It contains also the
    commands to register your nickname, identify, and enforce it; and instructions for
    channel ops.

# IRC Clients {#irc_clients}
-   Wikipedia:
    {{< wp "Comparison of instant messaging clients" >}},
    {{< wp "Comparison of Internet Relay Chat clients" >}}
-   {{< iref "xmpp#bitlbee" "bitlbee" >}} is an IRC to other chat networks gateway, such
    as AIM, ICQ, Microsoft Messenger, Yahoo!, Jabber and Google Talk, and Facebook
    Messenger, Twitter, Identi.ca, and status.net.  Iit allows you to browse other chat
    protocols with your irc client. bitlbee can be usefull if you want to use only a
    light irc client to take part in chats from many protocols including jabber/ssl as
    in gmail accounts.

    {{< iref "xmpp#bitlbee" "Bitlebee main entry" >}} is in the
    {{< iref "xmpp" "XMPP Page" >}}

## Console IRC clients {#console_irc_clients}
See {{< iref "#weechat" "Weechat" >}} below.

-   [CenterIm5](https://github.com/petrpavlu/centerim5) (GPL) is a ncurses
    ICQ/Yahoo!/AIM/IRC/MSN/Jabber/GaduGadu/RSS/LiveJournal Client,
    which replaced {{< wp "Centericq" >}} dead since 2007.

    _Centerim is an old client, which seems to have now a low activity, it
    [was in Debian but is no longer since wheezy
    ](https://tracker.debian.org/pkg/centerim)._

-   [epic](http://www.epicsol.org/) programmable irc-II client.
    -   [epic5.git](http://git.epicsol.org/epic5.git/)
    -   [EPIC 5 Help Pages](http://www.epicsol.org/help_root)
-   <a name=irssi></a>[irssi](https://irssi.org/)
    is a terminal based IRC client for UNIX systems. It also supports
    {{< iref "xmpp#otr" "OTR" >}}
    with [Irsii-OTR](https://github.com/cryptodotis/irssi-otr/)
    _in Debian_, FISH and alternate  protocols ( XMPP, SILC, ICB,
    [RobustIRC](robustirc.net)) via  [modules](https://irssi.org/modules/).
    _irssi_ can be scripted in Perl, and via modules in python, lua, tcl.  _irssi_ and
    it's plugins are in Debian.
    -   [Irssi documentation](https://irssi.org/documentation/)
    -   [ArchWiki: Irssi](https://wiki.archlinux.org/index.php/Irssi)
        and [Irssi-otr](https://wiki.archlinux.org/index.php/Irssi-otr).

## Graphical irc clients
-   <a name="polari"><a>[Polari](https://wiki.gnome.org/Apps/Polari) (GPL-v2.0)
    is a gnome graphical irc client that uses the
    {{< iref "xmpp#telepathy" "Telepathy framework" >}}. _It is in Debian._

-   <a name="xchat"></a>[XChat](http://xchat.org) (GPL) is a GTK+
    IRC client. _No development since 2010_. It stayed in Debian until 2020, and
    [is now removed](https://tracker.debian.org/pkg/xchat).

    -   [xchat doc](http://xchat.org/docs/).
        [Xchat Documentation](http://xchat.org/docs/)
    -   Xchat allows plugins in C, C++, guile, Perl, Python, Tcl and Ruby. Xchat is one
        of the more intuitive client for the irc newcomer. It is quite big 15M of
        res. mem. for an IRC only client.

    <a name="hexchat"></a>[HexChat](http://hexchat.github.io/) (GPL-2.0)
    is an IRC client based on {{< iref "#xchat" "XChat" >}}, but unlike XChat it’s
    completely free for both Windows and Unix and it is actively
    developed it is scriptable with Python and Perl. It supports
    {{< iref "xmpp#fish" "FISH encryption" >}} through
    [FISHLIM addon](http://fishlim.kodafritt.se/) _in Debian package hexchat-plugins_,
    and OTR through the plugin
    [HexChat-OTR](https://github.com/TingPing/hexchat-otr). _in Debian_.

    -   [hexchat - GitHub](https://github.com/hexchat/hexchat)
    -   [HexChat Documentation](https://hexchat.readthedocs.io/en/latest/)
    -   [ArchWiki: Hexchat](https://wiki.archlinux.org/index.php/HexChat)

## Emacs irc client {#emacs_irc}
There are sveral emacs iRC clients _under  GPL License_.

-   [Emacswiki: InternetRelayChat](http://www.emacswiki.org/emacs/InternetRelayChat)
    give a list of clients and IRC references.
-   [Circe](https://github.com/jorgenschaefer/circe/) (GPL-3.0)
    uses standard Emacs key bindings and indicates activity in channels in the status
    bar.

    The complexity-wise of _circe_ is between the minimal _rcirc_  and _ERC_.
    -   [Circe wiki](https://github.com/jorgenschaefer/circe/wiki).
-   [ERC _EmacsIRCClient_
    ](https://www.emacswiki.org/cgi-bin/wiki/EmacsIRCClient)
    is included in Emacs.
    -   [ERC Manual](https://www.gnu.org/software/emacs/manual/html_node/erc/index.html)
        is distributed with emacs as an info manual.
    -   [ERC - EmacsWiki](https://www.emacswiki.org/cgi-bin/wiki/EmacsIRCClient)
        is the index if an extensive documentation on ERC, it includes a long list of
        modules, bots and commands.
    -   [ZNC.el](https://github.com/sshirokov/ZNC.el) (MIT License)
        is an _ERC_ module to manage IRC connections through one or many ZNC servers.
-   [IrChat](http://www.emacswiki.org/cgi-bin/wiki/IrChat) _obsolete since 2017_
-   [Riece]( http://www.nongnu.org/riece/) is the continuation of _Liece_ is obsolete _2012_.
-   [rcirc](http://www.emacswiki.org/cgi-bin/wiki/rcirc) part of GNU Emacs
-   [weechat.el (Emacs)](https://github.com/the-kenny/weechat.el) is a client for the
    {{< iref "#weechat_relay" "WeeChat protocol" >}}.
-   [ZenIRC](http://www.zenirc.org/)  is a scriptable IRC client for EMACS.
    -   [ZenIRC - EmacsWiki](http://www.emacswiki.org/cgi-bin/wiki/ZenIRC)).

It is uneasy to compare the size of these client to other clients, if you have always an
emacs running from the beginning of your session to the end, as I use to do on my main
desktop, it costs you virtually nothing (circe is tiny and loading it is not perceptible
when looking at res. mem. size).

## Weechat {#weechat}
<!-- [[file:../../../../content-org/notes/social_networks_notes.org::#weechat][social_networks_notes - weechat]] -->

[WeeChat](http://www.weechat.org/) (GPL)
is an irc ncurses client, extensible by C plugins or script language (Perl, Python,
Ruby, guile, Lua, Tcl, javascript, php).

It uses ncurses an take 6M to 13M/6M cached of Resident size _depending of loaded
plugins_. WeeChat lack of an easy menu from the client, so to use it you have to be (or
get) accustomed with IRC commands. But Weechat helps you by providing an extensive help.

Debian has a weechat-curse, and a weechat-headless client, and packages for plugins, and
for the support of programming/script languages: tcl, guile, lua, php, python, ruby.

Weechat is a very active project which has a long development history. It is born
in 2003.  WeeChat 0.3.x (september 2009) was a major update new plugin api, new plugins,
new scripts, then each version includes new features, new language support and new
plugins. Version 1.0 was isssued in august 2014, and 2.0 in december 2017 and version
3.0 in november 2020.

Weechat has an extensive documentation:

-   [Quick Start Guide
    ](http://www.weechat.org/files/doc/stable/weechat_quickstart.en.html)
    ([development version
    ](http://www.weechat.org/files/doc/devel/weechat_quickstart.en.html))
-   [User Manual](http://www.weechat.org/files/doc/stable/weechat_user.en.html) (
    [dev](http://www.weechat.org/files/doc/devel/weechat_user.en.html),
    [ascidoc source](https://github.com/weechat/weechat/blob/master/doc/en/weechat_user.en.adoc)).
-   [Scripting Guide
    ](http://www.weechat.org/files/doc/stable/weechat_scripting.en.html)
    ([dev](http://www.weechat.org/files/doc/devel/weechat_scripting.en.html)).
-   [Plugin API Reference
    ](http://www.weechat.org/files/doc/stable/weechat_plugin_api.en.html)
    ([dev](](http://www.weechat.org/files/doc/devel/weechat_plugin_api.en.html)).
    [FAQ](http://www.weechat.org/files/doc/stable/weechat_faq.en.html) (
    [dev](http://www.weechat.org/files/doc/devel/weechat_faq.en.html))
-   [Tester’s Guide](http://www.weechat.org/files/doc/stable/weechat_tester.en.html)
    ([dev
    ](http://www.weechat.org/files/doc/devel/weechat_tester.en.html)).
    are available _with many translations_ on
    [WeeChat  Home](http://www.weechat.org/).
-   You find  info on recent development in the [WeeChat Blog](http://dev.weechat.org/).
-   [GitHub WeeChat](https://github.com/weechat/).
-   [WeeChat Wiki](https://github.com/weechat/weechat/wiki):
    -   [Alias examples](https://github.com/weechat/weechat/wiki/Alias-examples)
    -   [buflist](https://github.com/weechat/weechat/wiki/buflist)
    -   [Cursor mode](https://github.com/weechat/weechat/wiki/Cursor-mode)
    -   [Links](https://github.com/weechat/weechat/wiki/Links)
    -   [Miscellaneous](https://github.com/weechat/weechat/wiki/Miscellaneous)
    -   [Script aliases](https://github.com/weechat/weechat/wiki/Script-aliases)
    -   [Triggers](https://github.com/weechat/weechat/wiki/Triggers)
-   [weechat list of scripts](https://weechat.org/scripts/) and
    [gitHub script repository](https://github.com/weechat/scripts).
-   weechat.org provides
    [Debian packages for the development version](http://weechat.org/download/debian/).

External Documentation:

-   [ArchWiki: WeeChat](https://wiki.archlinux.org/index.php/WeeChat)
-   [Gentoo Wiki: WeeChat](https://wiki.gentoo.org/wiki/WeeChat).
-   Wikipedia {{< wp "Weechat" >}}
-   [My always up-to-date WeeChat configuration (weechat-dev)
    ](https://gist.github.com/pascalpoitras/8406501) by Pascal Poitras
-   [InWee](https://github.com/susam/inwee)
    is a wrapper script to send text messages and commands to WeeChat from shell or from
    within WeeChat via
    [WeeChat's FIFO pipe
    ](http://www.weechat.org/files/doc/stable/weechat_user.en.html#fifo_plugin),
    In the Home page the author Susam Pal explains also how to use
    the  FIFO pipe plugin _without imwee_.

Plugins for other protocols:

-   [weechat xmpp plugin](https://weechat.org/scripts/source/jabber.py.html/).
-   [weechat-matrix](https://github.com/poljar/weechat-matrix)
    a Weechat {{< iref "microblogging#matrix" "Matrix protocol" >}} python script. _In
    Debian._
    There is also an older [weechat-matrix-protocol-script
    ](https://github.com/torhve/weechat-matrix-protocol-script)
    written in Lua.
-   [whatsapp.py](https://weechat.org/scripts/source/whatsapp.py.html/) is a plugin to
    talk to {{< iref "xmpp#whatsapp" "WhatsApp" >}} using
    {{< iref "xmpp#yowsup" "Yowsup" >}}. _Obsolete?_
-   [weetweet.py](https://weechat.org/scripts/source/weetweet.py.html/)
    is a plugin for twitter messaging, it requires the python library twitter lib.
-   [wee-slack](https://github.com/wee-slack/wee-slack)
    is a WeeChat native client for Slack.com which connects via the Slack API, and
    maintains a persistent websocket for notification of events. It provides
    supplemental features only available in the web/mobile clients such as synchronizing
    read markers, typing notification, threads (and more)!.

    Wee-slack prints URLs for things like attachments and calls, they may be then
    handled directly by your terminal if you configure it to open the attachments in the
    proper application.

In addition to these plugins we can use a bridge IRC to other protocol
via {{< iref "xmpp#bitlbee" "BitlBee" >}},
{{< iref "xmpp#spectrum2" "Spectrum2" >}},
{{< iref "xmpp#matterbridge" "matterbrige" >}}

Plugins for secure messaging:

-   [Weechat-OTR](https://github.com/mmb/weechat-otr#readme)
    is a plugin allowing to use {{< iref "xmpp#otr" "OTR" >}} with weechat.
-   [crypt.py](https://weechat.org/scripts/source/crypt.py.html/)
    Encrypt/decrypt messages using openssl.
-   `ircrypt.py` in the  GitHub project
    [ircrypt-weechat](https://github.com/IRCrypt/ircrypt-weechat)
    which use openpgp for IRC encryption with
    [IRCrypt ptotocol ](https://github.com/IRCrypt/documentation).
-   [weechat-fish](https://github.com/freshprince/weechat-fish) provides
    {{< iref "xmpp#fish" "FiSH encryption" >}}.

<a name="weechat_relay"></a>Weechat has a
[relay plugin](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_plugin)
which has two variants
-   [IRC proxy
    ](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_irc_proxy)
    used to share connections to IRC servers with one or many other IRC clients
-   [Weechat protocol
    ](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_weechat_protocol)
    used by remote interfaces to display and interact with WeeChat.

Both protocol can connect via IP, [websocket
](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_websocket),
or [unix domain socket
](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_unix_socket).

The relay is established by the [/relay command
](https://weechat.org/files/doc/stable/weechat_user.en.html#relay_commands).

The available remote interfaces are
-   [QWeeChat](https://github.com/weechat/qweechat).
    is the official python/QT GUI
-   [Glowing-Bear](https://www.glowing-bear.org/) (GPL)
    is a WeeChat web frontend. The [source is in GitHub
    ](https://github.com/glowing-bear/glowing-bear).
    -   [Installation de Weechat et Glowing Bear comme client IRC distant
        ](https://mathdatech.fr/?post/2018/07/30/Installation-de-Weechat-et-Glowing-Bear-comme-client-IRC-distant).
-   [WeeChat-Android](https://github.com/ubergeek42/weechat-android)
-   [weechat.el (Emacs)](https://github.com/the-kenny/weechat.el)
    is an emacs interface for weechat. It is available in _melpa_.
-   [WeeCloud](https://github.com/eirikb/weecloud)
    Node.js library for relaying WeeChat to a webapp. _last commit 2014._


# IRC Web clients

-   <a name="kiwiirc"></a>[KiwiIRC](https://kiwiirc.com/) (Affero GPL)
    is a node.js web irc client. It supports ssl, user scripts, plugins; and is themable.
    -   [KiwiIRC GitHub repository](https://github.com/prawnsalad/KiwiIRC)
    -   [KiwiIRC Wiki](https://github.com/kiwiirc/kiwiirc/wiki)
    -   [KiwiIRC - ArchWiki](https://wiki.archlinux.org/title/KiwiIRC)
    -   <a name="webircgateway"></a>KiwiIrc
        [webircgateway](https://github.com/kiwiirc/webircgateway) (Apache-2.0 License)
        A go language Websocket gateway to IRC networks
    -   [KiwiIRC live client](https://kiwiirc.com/nextclient/):
        [Kiwi IRC - libera.chat](https://kiwiirc.com/nextclient/irc.libera.chat/) is
        also available as a Libera.chat instance
        [Libera Chat Web client](https://web.libera.chat/).
    -   [Kiwi IRC - mobile](https://github.com/kiwiirc/kiwiirc-mobile) (Apache-2.0 License)
        An open source IRC client for iOS and Android built using
        [NativeScript-Vue](http://nativescript-vue.org/).
-   <a name="gamja"></a>[gamja](https://sr.ht/~emersion/gamja/) (AGPL-3.0)
    by [Simon Ser (emersion)](https://emersion.fr/) is a light node.js irc web server.
    -   _gamja_ can use the {{< iref "#webircgateway" "KiwiIRC webgateway" >}}.
    -   Libera.chat hosts an instance :
        [Libera Chat - gamja web client](https://web.libera.chat/gamja/)
-   <a name="thelounge"></a>[The Lounge](https://thelounge.chat/) (MIT License)
    A self-hosted web IRC client an bouncer.
    It has two mode of operations:

    In private mode, The Lounge acts like a bouncer and a client combined.

    In public mode, it acts as an open chat available to anyone without
        registration.

    -  [Documentation — The Lounge](https://thelounge.chat/docs)
    -  [The Lounge - GitHub](https://github.com/thelounge/thelounge)
    -  [The Lounge Demo](https://demo.thelounge.chat/#/connect)
-   {{< wp "Mibbit" >}} (proprietary)
    is a web IRC, Yahoo! Messenger, and Twitter client.

    Firefox 3.5 and beyond support Mibbit as the default IRC protocol handler with
    support for encrypted SSL/TLS connections with the `ircs://` URI.

    In july 2021 «Access to Libera.Chat via Mibbit is not available due to repeated
    abuse.»

   -   [mibbit.com](https://mibbit.com/)
   -   [Mibbit client](https://chat.mibbit.com)
-   [qwebirc](http://www.qwebirc.org/) (GPL-2.0)
    is a python AJAX irc client for web.
    -   [qwebirc - GitHub](https://github.com/qwebirc/qwebirc/).

# Mobile Clients
-   [HoloIRC](https://github.com/holoirc/HoloIRC) (GPL-3.0 License)
    IRC client for Android.
-   [Revolution IRC](https://github.com/MCMrARM/revolution-irc) (GPL-3.0)
    for Android. It is [on f-droid](

# IRC bouncers
-   [KiwiBNC](https://github.com/kiwiirc/kiwibnc) (Apache-2.0 License)
    a Node.js irc bouncer, with javascript plugins, websocket support for direct web
    clients, built in web client.
-   [Soju](https://sr.ht/~emersion/soju/) (AGPL-3.0)
    by Simeon Ser _emersion_, is a bouncer written in Go language, accepting multiple
    users, and multiple clients.
    -   [soju Manual](https://soju.im/doc/soju.1.html)
    -   Soju IRC channel is #sxsoju on libera.chat.

## ZNC {#znc}
[ZNC](https://wiki.znc.in/ZNC) (Apache-2.0 License)
is a bouncer written in C
-   [ZNC - GitHub](https://github.com/znc/znc)
-   [ZNC Wiki](https://wiki.znc.in/)
-   List of all [Configuration items](https://wiki.znc.in/Configuration)
    The configuration file can only be edited manually when znc is stopped, on a
    live server you can use the [Webadmin](https://wiki.znc.in/Webadmin) module.
    The [ControlPanel](https://wiki.znc.in/Controlpanel) allows you to
    add/remove/edit users and settings on the fly via IRC messages.
-   [Modules](https://wiki.znc.in/Modules) are used to extend and modify
    the way ZNC functions.
-   [#znc on Libera.Chat](ircs://irc.libera.chat:6697/#znc) is the irc channel.

### Some modules
I list mainly modules for a
[Multiple clients usage](https://wiki.znc.in/Multiple_clients).


#### Included module {#included-module}

-   [route replies](https://wiki.znc.in/Route%5Freplies)
    Send replies only to the client who requested them and not to all clients.
    Without it a ZNC user with multiple clients, you may see a lot of useless stuff
    like /who replies, it is an essential module if you have multiple clients.

    ```nil
    /znc loadmod route_replies
    ```
-   [savebuff module](https://wiki.znc.in/Savebuff)
    saves your channel buffers into an encrypted file so they can survive restarts and reboots.
-   [simple\_away](https://wiki.znc.in/Simple%5Faway)
    is part of ZNC set you away on IRC while you are disconnected from the
    bouncer.

    The argument can be `-notimer` or `-timer x`.
    Commands:
    -   `settimer x` x is a number of seconds.  `settimer` display the current timer or if
        it is disabled.
    -   `reason <reason why you are away>`,- `reason` without argument display the current
        reason.


### External modules {#external-modules}

-   [The backlog module](https://wiki.znc.in/Backlog) request backlog,
-   [Chanfilter module](https://wiki.znc.in/Chanfilter)
    maintains client specific channel lists for identified clients. A typical use case
    is to have a subset of channels visible to a mobile client.
-   [Clientbuffer module](https://wiki.znc.in/Clientbuffer)
    maintains client specific buffers for identified clients. It is the buffer playback
    ZNC offers, but it keeps track of which client has received the buffer and which
    client hasn't.
-   [The Playback module](https://wiki.znc.in/Playback)
    allows IRC clients to request the module to send a partial buffer
    playback starting from and ending to a certain point of time. It is recommended for
    a multiple client configuration.
    To use it we need to disable `AutoClearChanBuffer` and `AutoClearQueryBuffer`
-   The __ControlPanel module__ allows you to add/remove/edit users and settings on the
    fly via IRC messages.



# IRC Bots
-   Wikipedia: {{< wp "IRC bot" >}} with a comprehensive
    {{< wp "IRC_bot#Comparison" "Comparison of IRC bots" >}}
-   [Eggdrop](http://www.eggheads.org/) (GPL-2.0) is an IRC bot written in the C
    language and has plugins in C and TCL.
    -   [eggdrop - GitHub](https://github.com/eggheads/eggdrop)
    -   [Eggdrop's documentation](https://docs.eggheads.org/)
    -   Wikipedia: {{< wp "Eggdrop" >}}
-   [EnergyMech](http://www.energymech.net/) (GPL) is a fork of Eggdrop is also
    programmed in C language, It is lighter than _Eggdrop_ and is scriptable in Perl,
    TCL, Python.
    -   [Comparison of EnergyMech and Eggdrop features
        ](http://www.energymech.net/features.html) _the comparison uses an old version
        of Eggdrop_.
    -   [EnergyMech GitHub repo](https://github.com/EnergyMech/energymech)
-   [EmacsWiki: Er Bot](https://www.emacswiki.org/emacs/ErBot)
    is an emacs-lisp irc bot. Main instances are fsbot on #emacs the
    [Emacs Channel](https://www.emacswiki.org/emacs/EmacsChannel).
-   [LogBot](https://freenode.logbot.info/) (MIT License)
    is an IRC logging bot, it logs many freenode channels.
-   [Sopel](https://sopel.chat/)
    ([Eiffel Forum License](http://opensource.org/licenses/EFL-2.0))
    formerly [Willie](http://willie.dftba.net/) is a python IRC bot with a lot of
    features: SSL Support, user and channel settings database using MySQL or SQLite, can
    run as daemon, meetbot, YouTube, Reddit, movie information, list RSS, google
    calculator, Searches Google, Bing, and Duck Duck Go and a
    [lot more](https://github.com/embolalia/willie/wiki/Commands).
    In 2021 [Debian package](https://tracker.debian.org/pkg/sopel) is only in unstable.
    -   [Sopel GitHub repository](https://github.com/sopel-irc/sopel)
    -   [Sopel documentation](https://sopel.chat/docs/)
    -   [Sopel GitHub repositories](https://github.com/sopel-irc)
        contains several plugins: weather _with DarkSky_, channel logging, Twitter,
        youtube, Github _print details of posted URLs_.

### Limnoria and Supybot forks {#limnoria}
-   [limnoria](https://github.com/ProgVal/Limnoria) (BSD License)
    by Valentin Lorentz is the continuation of Supybot with Python 3 and IRCv3 support
    including SASL, localisation, GPG authentication, TLS, and other
    enhancements and bug fixes.  This project is active in 2020. It is
    [in Debian](https://tracker.debian.org/pkg/limnoria).
    -   [Limnoria’s documentation](https://docs.limnoria.net/).
    -   [ProgVal/Supybot-plugins](https://github.com/ProgVal/Supybot-plugins)
        Valentin Lorentz Collection of plugins for Limnoria.
    -   [oddluck/limnoria-plugins](https://github.com/oddluck/limnoria-plugins)
        an other distinct collection of plugins for Limnoria.
-   [SupyBot](http://sourceforge.net/projects/supybot/) (BSD License)
    is the predecesor of Limnoria, the last final version was 0.84 in 2018, but the
    core project is from  2009. SupyBot is now replaced by
    {{< iref "#limnoria" "limnoria" >}}.
    -   [GitHub Supybot git repository](https://github.com/Supybot/Supybot/)
-   [Gribble](https://sourceforge.net/projects/gribble/)
    is a modified supybot written for for the Freenode IRC channel,
    #sourceforge. _last commit 2014._
    -   [Gribble plugins and enhancements
        ](https://sourceforge.net/p/gribble/wiki/Gribble_Project_Git_Repository/)
    -   [Gribble: SupyBot Resources
        ](https://sourceforge.net/p/gribble/wiki/Supybot_Resources/) _outdated_.
-   [MeetBot](http://wiki.debian.org/MeetBot)
    is a plugin to the IRC bot Supybot to facilitate taking of notes
    during IRC meetings.
    -   [MeetBot Manual](http://meetbot.debian.net/Manual.html).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
