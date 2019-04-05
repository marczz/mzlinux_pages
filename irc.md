<!--
.. description:
.. date: 2016-04-28
.. slug: irc
.. tags:
.. link:
.. book: mzlinux
.. title: IRC
-->

[TOC]

-----------------

See also [XMPP](/node/xmpp "internal reference")

# common Internet Messaging refs
-   Wikipedia: [w:Instant messaging],
    [w:list of instant messaging protocols],
    [w:Comparison of instant messaging protocols],
    [w:Comparison of instant messaging clients],
    [w:Instant messaging].


# IRC References

Some Jabber clients are also supporting IRC, they are listed in the
[XMPP Page](/node/xmpp "internal reference"). There are also jabber to
irc gateways that allow to connect to irc from any jabber client.

-   Wikipedia:  [w:Internet Relay Chat],
    [w:Comparison of Internet Relay Chat clients],
    [w:Comparison of instant messaging protocols],
    [w:Internet Relay Chat services],
    [w:Comparison of Internet Relay Chat services],
    [w:IRC daemon],
    [w:Comparison of Internet Relay Chat daemons],
    [w:List of Internet Relay Chat commands]
-   [Awesome IRC](https://github.com/davisonio/awesome-irc)
    a list of tools, software & other resources related to the
    Internet Relay Chat (IRC) protocol.
-   [RFC 1459](http://www.faqs.org/rfcs/rfc1459.html) - Original IRC
    Protocol, [RFC 2810](http://www.faqs.org/rfcs/rfc2810.html) -
    Updated IRC Architecture,
    [RFC 2811](http://www.faqs.org/rfcs/rfc2811.html) - Channel
    Management, [RFC 2812](http://www.faqs.org/rfcs/rfc2812.html) - IRC
    Client Protocol, [RFC 2813](http://www.faqs.org/rfcs/rfc2813.html) -
    Server Protocol.
-   [The IRC Prelude](http://irchelp.org/irchelp/new2irc.html) basic
    IRC documentation from [irchelp](http://www.irchelp.org/),
    [An IRC Tutorial](http://www.irchelp.org/irchelp/irctutorial.html)
-   [freenode](http://freenode.net/) IRC servers,
    the [freenode Knowledge Database](http://freenode.net/kb/all)
    explains _Channels_, _Connecting to freenode_, _Connecting with SASL_
    _General Expectations for Conduct_, _Nickname Registration_.
    -   Wikipedia: [w:Freenode]
-   [SwiftIRC](http://www.swiftirc.net/) has a
    [Wiki](http://wiki.swiftirc.net/wiki/Main_Page) with commands
    memos.
-   [Search Irc](http://searchirc.com/) for channels or servers.

## IRC Commands
A List of commands is givent in Wikipedia: [w:List of IRC Commands]
and also available in the help of most clients.

-   [toxin](http://toxin.jottit.com/) has list of
    -   [General IRC Commands](http://toxin.jottit.com/irc_commands)
    -   [XChat Help Commands
        ](http://toxin.jottit.com/xchat_help_commands)
    -   [Freenode NickServ Commands
        ](http://toxin.jottit.com/freenode_nickserv_commands)
    -   [Freenode ChanServ Commands
        ](http://toxin.jottit.com/freenode_chanserv_commands)
    -   [Freenode MemoServ Commands
        ](http://toxin.jottit.com/freenode_chanserv_commands)
-   [SwiftIRC Wiki](http://wiki.swiftirc.net/wiki/Main_Page):
    -   [general commands
        ](http://wiki.swiftirc.net/wiki/Other_commands)
    -   [NickServer](http://wiki.swiftirc.net/wiki/NickServ)
    -   [ChanServ](http://wiki.swiftirc.net/wiki/Chanserv)
    -   [MemoServ](http://wiki.swiftirc.net/wiki/Memoserv)
    -   [BotServ](http://wiki.swiftirc.net/wiki/Botserv)

    There are also FAQS for the services.

# IRC Clients {#irc_clients}
-   Wikipedia:
    [w:Comparison of instant messaging clients],
    [w:Comparison of Internet Relay Chat clients],
-   [bitlbee](/node/xmpp#bitlbee) is an IRC to
    other chat networks gateway, such as AIM, ICQ, Microsoft Messenger, Yahoo!,
    Jabber and Google Talk, and Facebook Messenger,
    Twitter, Identi.ca, and status.net.
    Iit allows you to browse other chat
    protocols with your irc client. bitlbee can be usefull if you want
    to use only a light irc client to take part in chats from many
    protocols including jabber/ssl as in gmail accounts.</br>
    [Bitlebee main entry](/node/xmpp#bitlbee "internal reference")
    is in the [XMPP Page](/node/xmpp "internal reference")
-   [CenterIm](http://www.centerim.org/) (GPL) is a ncurses
    ICQ/Yahoo!/AIM/IRC/MSN/Jabber/GaduGadu/RSS/LiveJournal Client.<br />
    it replaced [w:Centericq] dead since 2007.
-   <a name="emacs_irc"></a>__Emacs irc clients__ are numerous,
    all of them are GPLed:

    -   [Emacswiki: InternetRelayChat](http://www.emacswiki.org/emacs/InternetRelayChat)
        give a list of clients and IRC references
    -   [Circe](https://github.com/jorgenschaefer/circe/wiki).
    -   [EmacsIRCClient
        ](http://www.emacswiki.org/cgi-bin/wiki/EmacsIRCClient)
        aka ERC.,
        [IrChat](http://www.emacswiki.org/cgi-bin/wiki/IrChat),
    -   [LieceIrcClient
        ](http://www.emacswiki.org/cgi-bin/wiki/LieceIrcClient),
    -   [rcirc](http://www.emacswiki.org/cgi-bin/wiki/rcirc),
    -   [RieceIrcClient
        ](http://www.emacswiki.org/cgi-bin/wiki/RieceIrcClient),
    -   [ZenIRC](http://www.zenirc.org/) (
        [ZenIRC emacswiki links](http://www.emacswiki.org/cgi-bin/wiki/ZenIRC)).

    It is uneasy to compare the size of these client to other clients,
    if you have to launch emacs only to chat, it cost you 18M, it is
    my mean emacs size, that is 13M bare size + 5M packages. But if
    you have always an emacs running from the beginning of your
    session to the end, as I use to do on my main desktop, it costs
    you virtually nothing (circe is tiny and loading it is not
    perceptible when looking at res. mem. size).

-   [epic](http://www.epicsol.org/) programmable irc-II client, and
    online [EPIC Help Pages](http://help.epicsol.org)
-   <a name=irssi></a>[irssi](https://irssi.org/)
    is a terminal based IRC client for UNIX systems. It also supports
    [OTR](/node/xmpp#otr "internal reference")
    with [Irsii-OTR](https://github.com/cryptodotis/irssi-otr/)
    _in Debian_, FISH and alternate  protocols ( XMPP, SILC, ICB,
    [RobustIRC](robustirc.net)) via
    [modules](https://irssi.org/modules/). _irssi_ can be scripted in
    Perl, and via modules in python, lua, tcl.
    _irssi_ and it's plugins are in Debian.
    -   [ArchWiki: Irssi](https://wiki.archlinux.org/index.php/Irssi)
        and [Irssi-otr
        ](https://wiki.archlinux.org/index.php/Irssi-otr).
-   [Naim](http://naim.n.ml.org/) (GPL)
    is a console AIM, ICQ, IRC, and Lily CMC client  written in C.
-   [Polari](https://wiki.gnome.org/Apps/Polari)
    is a gnome graphical irc client that uses the
    [Telepathy framework](/node/xmpp#telepathy "internal reference").

-    <a name="xchat"></a>[XChat](http://xchat.org) (GPL) is a GTK+
    IRC client _no development since 2010_

    -   [xchat doc](http://xchat.org/docs/).
    -   [toxin](http://toxin.jottit.com) :
        [Xchat Documentation](http://toxin.jottit.com/xchat)
    -   [XChatData.net](http://xchatdata.net/) is also a Schat
        documentation wiki.
    -   Xchat allows plugins in C, C++, guile, Perl, Python, Tcl and
        Ruby. Xchat is one of the more intuitive client for the irc
        newcomer. It is quite big 15M of res. mem. for an IRC only
        client.

    <a name="hexchat"></a>[HexChat](http://hexchat.github.io/)
    is an IRC client based on XChat, but unlike XChat it’s
    completely free for both Windows and Unix and it is actively
    developed it is scriptable with Python and Perl. It supports
    [FISH encryption](/node/xmpp#fish "internal reference")
    thru [FISHLIM addon
    ](http://fishlim.kodafritt.se/) _in Debian package hexchat-plugins_,
    and OTR through the plugin
    [HexChat-OTR](https://github.com/TingPing/hexchat-otr) _in Debian_.

    -   [HexChat Documentation
        ](https://hexchat.readthedocs.io/en/latest/)
    -   [ArchWiki: Hexchat
        ](https://wiki.archlinux.org/index.php/HexChat)

## Weechat {#weechat}
[WeeChat](http://www.weechat.org/) (GPL)
is an irc ncurses client,  extensible by C plugins
or  script language (Perl, Python, Ruby, guile, Lua, Tcl, javascript,
php).
It can also be used for Jabber with a python plugin.
It uses ncurses an take 6M to 13M/6M cached of Resident
size _depending of loaded plugins_. WeeChat lack of an easy menu
from the client, so to use it you have to be (or get) accustomed
with IRC commands. But Weechat helps you by providing an extensive
help.

Weechat is a very active project which has a long development
history. It is born in 2003.
WeeChat 0.3.x (september 2009) was a major update new plugin api,
new plugins, new scripts, then each version includes new features, new
language support and new plugins. Version 1.0 was isssued in august
2014, and 2.0 in december 2017.


Weechat has an extensive documentation:

-   [Quick Start Guide
    ](http://www.weechat.org/files/doc/stable/weechat_quickstart.en.html)
    ([development version
    ](http://www.weechat.org/files/doc/devel/weechat_quickstart.en.html))
-   [User Manual
    ](http://www.weechat.org/files/doc/stable/weechat_user.en.html) (
    [dev
    ](http://www.weechat.org/files/doc/devel/weechat_user.en.html)).
-   [Scripting Guide
    ](http://www.weechat.org/files/doc/stable/weechat_scripting.en.html)
    ([dev
    ](http://www.weechat.org/files/doc/devel/weechat_scripting.en.html)).
-   [Plugin API Reference
    ](http://www.weechat.org/files/doc/stable/weechat_plugin_api.en.html)
    ([dev](
    ](http://www.weechat.org/files/doc/devel/weechat_plugin_api.en.html)).
    [FAQ
    ](http://www.weechat.org/files/doc/stable/weechat_faq.en.html) (
    [dev](http://www.weechat.org/files/doc/devel/weechat_faq.en.html))
-   [Tester’s Guide
    ](http://www.weechat.org/files/doc/stable/weechat_tester.en.html)
    ([dev
    ](http://www.weechat.org/files/doc/devel/weechat_tester.en.html).
    are available _with many translations_ on
    [WeeChat  Home](http://www.weechat.org/).
-   You find  info on recent development in the
    [WeeChat Blog](http://dev.weechat.org/).
-   [GitHub WeeChat](https://github.com/weechat/).
-   [WeeChat Wiki](https://github.com/weechat/weechat/wiki).
-   [weechat list of scripts
    ](https://weechat.org/scripts/) and [gitHub script repository
    ](https://github.com/weechat/scripts).
-   weechat.org provides
    [Debian packages for the development version
    ](http://weechat.org/download/debian/).

External Documentation:

-   [ArchWiki: WeeChat
    ](https://wiki.archlinux.org/index.php/WeeChat)
-   [Gentoo Wiki: WeeChat
    ](https://wiki.gentoo.org/wiki/WeeChat).
-   Wikipedia [w:Weechat]
-   [InWee](https://github.com/susam/inwee)
    is a  wrapper script to send text messages
    and commands to WeeChat from shell or from within WeeChat via
    [WeeChat's FIFO pipe
    ](http://www.weechat.org/files/doc/stable/weechat_user.en.html#fifo_plugin),
    In the Home page the author Susam Pal explains also how to use
    the  FIFO pipe plugin _without imwee_.
-   [Weechat.el](https://github.com/the-kenny/weechat.el)
    is an emacs interface for weechat. It is available in _melpa_.

Plugins for other protocols:

-   [weechat xmpp plugin
    ](https://weechat.org/scripts/source/jabber.py.html/).
-   [whatsapp.py
    ](https://weechat.org/scripts/source/whatsapp.py.html/)
    is a plugin to talk to
    [WhatsApp](/node/xmpp#whatsapp "internal reference") using
    [Yowsup](/node/xmpp#yowsup "internal reference").
-   [weetweet.py](https://weechat.org/scripts/source/weetweet.py.html/)
    is a plugin for twitter messaging, it requires the python library
    twitter lib.
-   [wee-slack](https://github.com/wee-slack/wee-slack)
    is a WeeChat native client for Slack.com which connects via the
    Slack API, and maintains a persistent
    websocket for notification of events. It  provides supplemental
    features only available in the web/mobile clients such as
    synchronizing read markers, typing notification, threads (and
    more)!.

In addition to these plugins we can use a bridge IRC to other protocol
via [BitlBee](/node/xmpp#bitlbee "internal reference"),
[Spectrum2](/node/xmpp#spectrum2 "internal reference"),
[matterbrige](/node/xmpp#matterbridge "internal reference")



Plugins for secure messaging:

-   [Weechat-OTR](https://github.com/mmb/weechat-otr#readme)
    is a plugin allowing to use [OTR](/node/xmpp#otr) with weechat.
-   [crypt.py](https://weechat.org/scripts/source/crypt.py.html/)
    Encrypt/decrypt messages using openssl.
-   `ircrypt.py` in the  GitHub project
    [ircrypt-weechat](https://github.com/IRCrypt/ircrypt-weechat)
    which use openpgp for IRC encryption with
    [IRCrypt ptotocol ](https://github.com/IRCrypt/documentation).
-   `fish.py` from [GitHub weechat-fish
    ](https://github.com/freshprince/weechat-fish) provide
    [FiSH encryption](/node/xmpp#fish "internal reference").

Weechat has some frontends:

-   [QTWeechat](https://github.com/weechat/qweechat).
    is the official python/QT GUI
-   [glowing-bear](https://www.glowing-bear.org/) (GPL)
    is a WeeChat web frontend. The [source is in GitHub
    ](https://github.com/glowing-bear/glowing-bear).

# IRC Web clients

-   [qwebirc](http://www.qwebirc.org/)
    is a python AJAX irc client for web. An online site is at
    [freenode webchat](https://webchat.freenode.net/).
-   [KiwiIRC](https://kiwiirc.com/) (Affero GPL)
    is a node.js irc client.
    -   [KiwiIRC GitHub repository
        ](https://github.com/prawnsalad/KiwiIRC)
    -   [KiwiIRC live client](https://kiwiirc.com/)

# IRC Bots
-   Wikipedia: [w:Internet Relay Chat bot] and
    [w:Comparison of Internet Relay Chat bots]
-   [w:Eggdrop] (GPL] is written in the C language and has plugins
    in C and TCL. _last release 2011_.
    -   [Eggdrop Home](http://www.eggheads.org/)
-   [EnergyMech](http://www.energymech.net/) (GPL) is a fork of Eggdrop
    is also programmed in C language,
    It is lighter than _Eggdrop_ and is scriptable in Perl, TCL,
    Python.
    -   [Comparison of EnergyMech and Eggdrop features
        ](http://www.energymech.net/features.html).
    -   [EnergyMech GitHub repo
        ](https://github.com/MadCamel/energymech)
-   [Gozerbot](http://gozerbot.org/) (BSD License) is an IRC and
    Jabber bot written in python. It is in Debian.
    -   [Pypi:Gozerbot](https://pypi.python.org/pypi/gozerbot)
-   [Sopel](https://sopel.chat/)
    ([Eiffel Forum License](http://opensource.org/licenses/EFL-2.0))
    formerly [Willie](http://willie.dftba.net/)
    is a python IRC bot with a lot of features: SSL Support, user and
    channel settings database using MySQL or SQLite, can run as
    daemon, meetbot, YouTube, Reddit, movie information, list RSS,
    google calculator, Searches Google, Bing, and Duck Duck Go and a
    [lot more](https://github.com/embolalia/willie/wiki/Commands).
    It is in Debian.
    -   [Sopel GitHub repo](](https://github.com/sopel-irc/sopel))
-   [Tiny Tiny IRC](http://tt-rss.org/redmine/projects/tt-irc/wiki)
     (GPL) is an AJAX-powered IRC client allowing to stay connected to
     IRC without a dedicated software or even stable network
     connection. There is also an android client.

### Supybot and forks

[SupyBot](http://sourceforge.net/projects/supybot/) (BSD License)
is an IRC bot framework written in python. It is in Debian, but
only the old _2009_ v0.83.4.1 stable release. The last commit is
in 2015 but there where no official release between 2009 and 2015
_as seen  in 2018_. SupyBot is now replaced by
[limonaria](#limonaria "internal reference").

-   [GitHub Supybot git repository
    ](https://github.com/Supybot/Supybot/)
    ( The [sourceforge repo
    ](https://sourceforge.net/p/supybot/code/) is up to date for
    commits but not the tags!).
-   The Supybot manual is the
    [SupyBook](http://supybook.fealdia.org/devel/).
    but is no longer available
-   [limonaria](https://github.com/ProgVal/Limnoria)
    is a modified version of Supybot with Python 3 and IRCv3 support
    including SASL, localisation, GPG authentication, TLS, and other
    enhancements and bug fixes.  This project is active in 2018. It is
    in Debian.
      -   [Limnoria’s documentation
          ](https://limnoria.readthedocs.io/en/latest/)
          at read the doc, or [here
          ](http://doc.supybot.aperio.fr/en/latest/).
     -    Valentin Lorentz [Collection of plugins for Supybot/Limnoria
         ](https://github.com/ProgVal/Supybot-plugins)
-   [Gribble](https://sourceforge.net/projects/gribble/)
    is a modified supybot written for for the Freenode IRC channel,
    #sourceforge.
    -   [Gribble Wiki
        ](https://sourceforge.net/p/gribble/wiki/Main_Page/)
    -   [Gribble git repository
        ](https://sourceforge.net/p/gribble/code/ci/master/tree/)
    -   [Gribble plugins and enhancements
        ](https://sourceforge.net/p/gribble/wiki/Gribble_Project_Git_Repository/)
-   [Gribble: SupyBot Resources
    ](https://sourceforge.net/p/gribble/wiki/Supybot_Resources/)
-   [MeetBot](http://wiki.debian.org/MeetBot)
    is a plugin to the IRC bot Supybot to facilitate taking of notes
    during IRC meetings.
    [MeetBot Manual](http://meetbot.debian.net/Manual.html).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
