---
title: Web Browsers
---


# Firefox
-   [firefox help
    ](https://support.mozilla.org/en-US/products/firefox):
    [Keyboard Shortcuts
    ](https://support.mozilla.org/en-US/kb/keyboard-shortcuts-perform-firefox-tasks-quickly),
    [Search from the address bar
    ]((https://support.mozilla.org/en-US/kb/search-web-address-bar),
    [domain guessing
    ](https://support.mozilla.org/en-US/kb/search-web-address-bar#w_domain-guessing),
    [Command line arguments
    ](https://developer.mozilla.org/en-US/docs/Mozilla/Command_Line_Options),
    [geolocation
    ](https://www.mozilla.org/en-US/firefox/geolocation/).
-   ArchWiki pages: [Firefox](https://wiki.archlinux.org/index.php/Firefox),
    [Firefox/Privacy](https://wiki.archlinux.org/index.php/Firefox/Privacy),
    [Firefox/Profile on RAM](https://wiki.archlinux.org/index.php/Firefox/Profile_on_RAM),
    [Firefox/Tweaks](https://wiki.archlinux.org/index.php/Firefox/Tweaks)
-   [Mozilla developers tools](https://developer.mozilla.org/en-US/docs/Tools):
    -   [Web Console](https://developer.mozilla.org/en-US/docs/Tools/Web_Console),
    -   [Command Line Interpreter
        ](https://developer.mozilla.org/en-US/docs/Tools/Web_Console/The_command_line_interpreter),
-   [mozillaZine
    ](http://kb.mozillazine.org) gather mozilla news;
    -   [Command line arguments
        ](http://kb.mozillazine.org/Command_line_arguments).
    -   [File types and download actions
        ](http://kb.mozillazine.org/File_types_and_download_actions).
        When we cannot cope with the default or customized action in
        firefox, we may try to edit
        `.mozilla/firefox/xxxxx.default/mimeTypes.rdf`
    -   Along with file types we can also customize how firefox deal with
        protocols:
        [mozillaZine: Register protocol
        ](http://kb.mozillazine.org/Register_protocol)
-   There are many [about:addons](about:addons) the list
    of installed plugins is at [about:plugins](about:plugins) an in the
    `Tools/Add-on` menu entry.
-   Config options can be modified by opening
    [about:config](about:config) in your browser.
    -   The edition of preferences is described in
        [Customizing Mozilla](http://www.mozilla.org/unix/customizing.html), and
        [mozillazine: Editing configuration
        ](http://kb.mozillazine.org/Editing_configuration).
    -   The options are explained in
        [Firefox Tweak Guide
        ](http://www.tweakguides.com/Firefox_1.html)
        *([Firefox Tweak Guide
        ](http://www.tweakguides.com/Firefox_1.html) is a
        guide for the windoze version of firefox, but a a large part is
        common with linux firefox*).
    -   A more complete list of options is in
        [mozillaZine: About:config entries
        ](http://kb.mozillazine.org/About:config_entries) and in
        the
        [mozillaZine:Category:Preferences
        ](http://kb.mozillazine.org/Category:Preferences),
        the last being a list indexing pages on the ( approx. 420!)
        preference entries.
    -   [Chrome Edit+](http://webdesigns.ms11.net/chromeditp.html) is a
        plugin for editing preferences. It can replace the *Chrome Edit*
        and the *preferential* plugin which has not been updated since
        end of year 2006.
    -   For a linux programmer it is easier to modify with an editor the
        file `prefs.js` inside `~/.mozilla/firefox/*.default/`. This
        file is overwritten when firefox exits, to manage your own
        persistent preferences it may be easier to create in the same
        directory a file `user.js`, the preferences in this file
        override `prefs.js`.
        (see also [mozillazine: user.js
        ](http://kb.mozillazine.org/User.js_file))
    -   You may need to adjust the maximum amount of time in seconds a script can run
        [dom.max_script_run_time
        ](http://kb.mozillazine.org/Dom.max_script_run_time)
        and dom. max_chrome_script_run_time.
-   You can use an external mailer with mozilla, it is described in
    [Mozilla and external mailers](http://howto-pages.org/mozilla.php),
    I have written a bash script to decode the mailto url (
    [rfc2368](http://www.faqs.org/rfcs/rfc2368.html)) and call the mutt
    MUA.
-   [Dom inspector](http://www.mozilla.org/projects/inspector/) is a
    very useful tool in mozilla/firefox, when you open it and select
    under `Search` menu the item `Select Element by Click` you can when
    clicking on an element in the page find its place in the DOM tree.
    It is very usefull to find how to set your CSS for an effect.
-   [Conkeror](http://conkeror.org/) is a keyboard-driven, Mozilla-based
    web browser. It is no longer packaged in Debian.
    _Not to be confused with the KDE browser Konqueror._
    -   Wikipedia {{< wp "Conkeror" >}}.
-   The [compatibility of desktop and mobile browsers with HTML5, CSS3, SVG
    ](http://caniuse.com/)
    is summarized in these tables.

## Firefox addons {#firefox_addons}

-   [Browser extensions - ArchWiki](https://wiki.archlinux.org/index.php/Browser_extensions)
-   [Browser plugins - ArchWiki
    ](https://wiki.archlinux.org/index.php/browser_plugins)
    has informations about flash players.
-   Wikipedia: {{< wp "List of Firefox extensions" >}}

### Flash plugins {#flash_plugins}
For playing swf you can use
{{< iref "media_players#gnash" "Gnash" >}},
{{< iref "#adobe_swf" "Adobe Flash plugin non free" >}},
{{< iref "media_players#lightspark" "Lightspark" >}},
{{< iref "#pepperflash" "Pepper Flash Player" >}}
or {{< iref "#shumway" "Shumway" >}}.

But you can replace Flash by other formats following recipes of
[Triskell Wiki: Play Videos Without Using Flash
](https://trisquel.info/en/wiki/play-videos-without-using-flash)

You can also install
[Freshplayerplugin to use the Chromium PeperFlash plugin with Iceweasel
](https://wiki.debian.org/Freshplayerplugin).

-   [Debian Wiki: Flash](https://wiki.debian.org/Flash) gives the
    status of Flash support on Debian. _not up to date_.
-   <a name="adobe_swf"></a>[Debian Wiki: FlashPlayer
    ](https://wiki.debian.org/FlashPlayer)
    on Adobe SWF plugin on Debian.

    Adobe announced in 2012 it would not make newer versions of its
    NPAPI Flash player plugin available on Linux and would only
    provide security updates for Flash Player 11.2 until 2017.
    But in 2016 they began again to provide the NAPI plugin taht can
    be used with Firefox.

    But only the PPAPI plugin used in peper flash on Chrome, support
    DRM, GPU acceleration, Stage 3D, etc.

-   <a name="pepperflash"></a>[Debian Wiki: Pepper Flash Player
    ](https://wiki.debian.org/PepperFlashPlayer) can be used with
    Chromium.
    We can also use it with Firefox with the
    [Freshplayer plugin
    ](https://wiki.debian.org/Freshplayerplugin).
    The package is [browser-plugin-freshplayer-pepperflash
    ](https://packages.debian.org/sid/browser-plugin-freshplayer-pepperflash).
-   {{< wp "Google Swiffy" >}} is a web-based tool developed by Google that
    converts SWF files to HTML5. Its main goal is to display Flash
    contents on devices that do not support Flash.
    -   [Swiffy Home](https://developers.google.com/swiffy/)
-   <a name="shumway"></a>[Shumway
    ](https://github.com/mozilla/shumway/)
    is a Flash VM and runtime written in JavaScript. It replaces the
    adobe flash plugin that is no longer maintained in linux.
    _But Shumway itself don't seem to be anymore developped since 2015_.
    -   [Shumway Home page](https://mozilla.github.io/shumway/).
    -   [Debugging and Configuring Shumway - using the extension
        ](https://github.com/mozilla/shumway/wiki/Debugging-and-Configuring-Shumway#using-the-extension).
    -   [Mozilla: Test the Shumway SWF player
        ](https://oneanddone.mozilla.org/en-US/tasks/24/)
    -   To test use any of the
        [Shumway/Flash video sites
        ](https://wiki.mozilla.org/Shumway/Flash_video_sites)
-   YouTube can use Webm instead of swf you have only to opt for html5
    in the page
    [YouTube HTML5 Video Player](https://www.youtube.com/html5).

-   Some plugins try to get force the use of html5 or open video
    codecs instead of swf: [YouTube ALL HTML5
    ](https://addons.mozilla.org/en-US/firefox/addon/youtube-all-html5/),
    [Video WithOut Flash
    ](https://addons.mozilla.org/en-US/firefox/addon/video-without-flash/).


# Ads Blocking
 will not discuss this controversial topic, but I adhere to
[FiveFilters - Block Ads!
](https://blockads.fivefilters.org/acceptable.html).

Fivefilters has an [Ads Blocking Test page
](https://blockads.fivefilters.org/index.html)
The source is on
[GitHub fivefilters/block-ads
](https://github.com/fivefilters/block-ads).

For network level adds blocking see the page
{{< iref "ads_blocking" "blocking advertisements" >}}, and for cleaning all
the ininteresting stuff _it is more politicaly correct that «junk»!_
that is cluttering web pages see {{< iref "documents#readability_software" "Readability Software" >}}.

We can use css to avoid displaying advertisements it is described in
the [floppymoose.com page](http://www.floppymoose.com/) and in
[Ad Blocking page](http://www.gozer.org/mozilla/ad_blocking/)from
[www.gozer.org](http://www.gozer.org).

It is often more efficient to block loadind of images than hiding
them once loaded, you can add any advertisement sites to
`Preferences/Web Feature/Exceptions` they used to be stored inside
default folder in the file `hostperm.1`

So we could fill our `hostperm.1` with a
[list of common ad servers
](http://pgl.yoyo.org/adservers/serverlist.php?hostformat=hostperm.1&showintro=0)
you might want to read [about this list
](http://pgl.yoyo.org/adservers/).
_But hostperm.1 is deprecated in Gecko 1.9+._

A popular mozilla plugin to block adds is
[Adblock Plus ](http://adblockplus.org/en/), but we have to choose
a proper
[Adblock Plus subscriptions ](http://adblockplus.org/en/subscriptions).

There is also a GPLed blocker add-on for Firefox, Chromium,
Microsoft Edge, Safari [uBlock Origin
](https://github.com/gorhill/uBlock) that support and extend
the Adblock Plus filter syntax. *EasyList*, *Peter Lowe's Adservers*,
*EasyPrivacy* and *Malware domains* are enabled by default when you
install uBlock₀. uBlock₀ is leaner in memory and CPU than Adblock
Plus, and can block more ads.

-   [uBlock₀ Wiki](https://github.com/gorhill/uBlock/wiki)

Most of them don't block tracking and among it this _Google
Analytics_ that track most of the site we visite. To block it you
have to choose some subscription like
[EasyPrivacy ](http://easylist.adblockplus.org/en/)
or you can also use
[Google Analytics Opt-out Browser Add-on
](http://tools.google.com/dlpage/gaoptout).
Wladimir Palant tell us that it is not 100% reliable in
[The wrong way to deal with privacy concerns
](http://adblockplus.org/blog/the-wrong-way-to-deal-with-privacy-concerns).

Google has deleted add blockers from Google Play, but you can
still download from the site
[Addblock Plus for android ](http://adblockplus.org/en/android-about)


# Alternate browsers
I have down some memory comparisons on the alternate browsers, each
measure, is down after opening my home page, and they refer to
resident memory only. Of course virtual memory can be a lot greater
and the memory consumption increase, when you look to more pages, it
depends also of your settings like the plugins you use, memory
caching, type of content - plain html, html+javascript, html +
javascript doing ajax processing, html + flash ....  The comparison is
always difficult; so I use as benchmark a session just started with 3
tabs, two on this site, one with gmail. All the plugins are disabled for the test. Note
that gmail uses an intense javascript processing (even just opening the standard view)
so the footprints are a lot bigger with gmail standard view than with basic html view.
Of course you can expect to
double the memory footprint after some hours of browsing, note that most browsers don't
reclaim unused memory, so once your have used an heavy js demanding site, the footprints
stay high, even it the actual tabs are plain html.

I did two memory footprint tests one in 2011 with the same pages.

For javascript supporting browsers:

-   Firefox with this _3 tab startup_ has 166M Res/ 27 Shr footprint,
    but it increases very quickly
-   The webkit browsers Epiphany, Midori and Uzbl use 150M/35M
    starting with 3 tabs.

Non javascript Xwindow browsers:

-   A Netsurf session with 3 tab eat 28M res/14M shr <br />
-   The old Dillo 8.5 is 6.4M resident.

Terminal browsers:

-  Elinks with lua but without perl and ruby is 4.3M resident.
-  Lynx has a footprint of 2.8M.

A new test was made in 2014 with a greater load both in memory and
cpu, but the same three tabs give quite different results:

-   At start the three browsers firefox, uzbl, and qupzilla take around
    300M/30M.
-   Netsurf-gtk 47M/17M.

In the same 2014 test, to compare with  non-tabbed browsers
 only the present page was open:

-   qupzilla 85M/66
-   uzbl 58M/35M
-   surf 78M/56
-   Netsurf-gtk 42M/28M
-   Netsurf-fb 28M/19M
-   elinks 14M/7M
-   links2 graphic mode with X11 driver  8.4M/6M,fb driver (on console but with graphics!) 7M/5.2M, directfb driver (on console but with graphics!) 12.7M/6MM/2.5M text mode 5.7M/4.6M
-   w3m 6.5M/4.8M.

Begining 2017:

-   Firefox 652M/103M the used memory is bigger of 570M.
-   Chromium 2*140M/90M+2*90M/58M+44M/35M+11M/2M
    the used memory is bigger of 410M.
-   Vivaldi 474M/ 410M + 306M/100M +2*145M/100M+2*95M/60M.
    the used memory is bigger of 410M.
-   Qupzilla 232M/73M;  175M used memory
-   Midori 376M/96M;   300M used memory
-   poseidon: python3 103M/61M + WebKitWebProcess ( 411M/97M + 102M/69M +
    145M/84M) + WebKitNetworkProcess (50M/31M); 450M used memory.

Test in 2018

-   Falkon 3.0 : 309M/92M + QTWebEngineProcess  (313M/73M + 2 * 87M/53M + 53M/43M)
    global used memory 450M
-   Chromium 67 global memory 590M
-   Firefox esr 52.9 one process 520M/106M global 460M, slow to launch
-   Firefox 61.0 many processes global 560M; with gmail in basic html I get only 200M
-   Epihany 3.28 120M/58M + many Webkit processes  590M/100M + 3* 60M/54M global 520M
    slow to launch and to stop, high cpu load.
-   Surf 2.0 with only gmail 570M

With one tab no js

-  Netsurf-gtk 46M/31M only 15M of increased used memory


-   [Wikipedia: Comparaison of web browsers
    ](http://en.wikipedia.org/wiki/Comparison_of_web_browsers)n
    gives a complete comparison of web browsers features, but not of
    their performances (speed, memory and cpu consumption)
-   [List of applications Web Browsers - ArchWiki
    ](https://wiki.archlinux.org/index.php/List_of_applications/Internet#Web_browsers)
-   {{< wp "Google Chrome" >}} is a freeware but not fully open source. The
    open source browser behind chrome is
    [Chromium](http://www.chromium.org/)
    -   [Google Chrome Home](http://www.google.com/chrome)
    -   [Chrome Help](https://support.google.com/chrome)
    -   [Chromium - ArchWiki](https://wiki.archlinux.org/index.php/Chromium),
        [Chromium/Tips and tricks - ArchWiki
        ](https://wiki.archlinux.org/index.php/Chromium/Tips_and_tricks).
-   <a name="dwb"></a>[dwb](https://portix.bitbucket.io/dwb/)
    is a lightweight webkit/gtk browser based. The page
    [dwb - ArchWiki](https://wiki.archlinux.org/index.php/Dwb), flag it as
    insecure and outdated. _dwb_ is in Debian.
-   {{< wp "Lynx (web browser)" "Lynx" >}} (GPL) is a text browser.
-   [elinks](http://elinks.or.cz/) (GPL) Enhanced Links is a web browser
    in text mode with lua, guile, perl scripting; others features
    include mailcap support, tabbed browsing, gpm support, table and
    frames rendering, ssl, authentication, persistent cookies, xbel
    bookmarks and experimental css and javascript. _last release 2012_
    -   Wikipedia: {{< wp "Elinks" >}}
    -   [ELinks - ArchWiki](https://wiki.archlinux.org/index.php/ELinks)
-   [Falkon](https://www.falkon.org/) previously  _QupZilla_ (GPL)
    is based on WebKit and Qt Framework. It supports tabbed browsing,
    bookmarks, history, search in a page, screenshots, news
    feeds. Beginning of 2018 Qupzilla is renamed Falkon and becomes
    the KDE browser.
-   {{< wp "Links_(web_browser)"  "Links" >}} (GPL), the ancestor of elinks
    and an other offspring:
    <a name="links2">[Twibright Labs: Links
    ](http://atrey.karlin.mff.cuni.cz/~clock/twibright/links/)(links-2)
    offers both graphic and text browsing, it has no CSS, it do have
    some javascript but is not very usable for javascript driven
    sites.  Links is a minimal nice browser that can work in text
    mode, or graphic mode with X11, fb or framebuffer; with unmatched
    low footprints.
-   [Lariza](https://www.uninformativ.de/git/lariza/file/README.html) (MIT License)
    ia a simple web browser using GTK+ 3, GLib and WebKit2GTK+.
    It is considered to be one of the lightest front-end GUI interfaces to webkit2gtk.
    -   [lariza - ArchWiki](https://wiki.archlinux.org/index.php/Lariza).
-   [Luakit](https://luakit.github.io/) (GPL)
    Luakit is a highly-configurable browser framework based on WebKitGTK+. It is very
    fast and extensible by Lua. Luakit is packaged in Debian.
    -   [luakit - GitHub](https://github.com/luakit/luakit)
    -   [Luakit - ArchWiki](https://wiki.archlinux.org/index.php/Luakit)
-   {{< wp "Midori (web browser)" "Midori" >}}  is a web browser
    based on the {{< wp "Webkit" >}} engine as are Uzbl and Epiphany.
    It the default browser for Xfce, and many small distributions like Slitaz, Bodhi
    Linux, and other.
    -   [Midori Home](https://astian.org/midori/)
    -   [Midori - ArchWiki](https://wiki.archlinux.org/index.php/Midori).
-   [NetSurf](http://www.netsurf-browser.org/)
    (GPL) is a fast small footprint web browser for RISC OS and UNIX
    platforms. Netsurf can handle CSS but not javascript. A NetSurf
    package is in Debian _named: netsurf-gtk_.
    Netsurf is small but its main limitation is that it does not
    provide Javascript.

    There is a frame buffer version of netsurf, it has no shortcuts, menu, tabs, but has
    minimal memory footprint.
-   [Qutebrowser](https://www.qutebrowser.org/) (GPL)
    is a keyboard-focused browser with a minimal GUI. It’s based on
    Python and PyQt5. It was inspired by other browsers/addons like
    {{< iref "#dwb" "dwb" >}}  and Vimperator/Pentadactyl. QuteBrowser is in Debian.
    -   [ArchWiki: Qutebrowser
        ](https://wiki.archlinux.org/index.php/Qutebrowser).
-   [servo](https://servo.org/) (Mozilla public License)
    is a new browser written in Rust.
    -   [servo - GitHub](https://github.com/servo/servo)
-   [Surf](http://surf.suckless.org/) (GPL)
    from suckless tools is a simple web browser based on
    WebKit/GTK+. It supports the XEmbed protocol
    -   [ArchWiki: Surf](https://wiki.archlinux.org/index.php/Surf)
    -   [surf extension scripts](http://surf.suckless.org/files/)
-   [Web](https://wiki.gnome.org/Apps/Web)
    previously named _Epiphany_ is a web browser based on Gtk+ and {{< wp "Webkit" >}}
    engine as are Uzbl and Midori.  Previous releases of epiphany used gecko now
    replaced by webkit.
    -   [GNOME/Web - ArchWiki](https://wiki.archlinux.org/index.php/GNOME/Web).


    Epiphany footprints are bigger than midori.
    Epiphany 2.30 - 3.28 allow to display the javascript page of gmail while
    midori 0.3.6-0.5.11 does not.

    Displaying only one tab with gmail with epiphany open 1 epiphany
    process 94M res / 62M shr, 1 Webkit storage 31M / 24M, 1 Webkit
    network 60M / 34M, 1 Webkit Web 502M / 100M.

-   {{< wp "W3m" >}} (MIT License) is a console (and xterm) browser that can handle
    images, it is very small 3.6M.
    -   [W3m Home Page](http://w3m.sourceforge.net/),
    -   [w3m-mee](http://pub.ks-and-ks.ne.jp/prog/w3mmee/)
        Multilingualization of w3m,
    -   [Emacs-w3m](http://emacs-w3m.namazu.org/) a simple Emacs interface
        to w3m. The development of w3m began in 1995, it has evolved a lot
        until 2004, and slowed down since 0.5 release, even if new minor releases
        have been delivered in 2007 and 2011.
    -   [emacs Wiki: Emacs-w3m
        ](https://www.emacswiki.org/emacs/emacs-w3m),
        [w3m](ttps://www.emacswiki.org/emacs/w3m).

# Bookmarklet
A {{< wp "bookmarklet" >}} is a bookmark stored in a web browser that contains
JavaScript commands stored as the URL of a bookmark in a web
browser.

-   [YesWap mobile bookmarklets list](http://o.yeswap.com/)
-   [The Best Bookmarklets for Mobile Browsing
    ](http://www.lifehacker.com.au/2014/05/the-best-bookmarklets-to-make-mobile-browsing-less-annoying/)
-   [Bookmarklets.com](http://www.bookmarklets.com/)
-   [Jesse's bookmarklets site](http://www.squarefree.com/bookmarklets/),
-   [Mozillalinks bookmarklets
    ](http://mozillalinks.org/wp/resources/bookmarklets-collection/),


# Search engines {#search_engines}

-   Wikipedia {{< wp "Comparison of web search engines" >}},
    {{< wp "List of search engines" >}},
     {{< wp "Search engine privacy" >}}.

## Searx {#searx}
[Searx](https://asciimoo.github.io/searx/)
internet metasearch engine which aggregates results from more than
70 search services. Users are neither tracked nor
profiled. Additionally, searx can be used over Tor for online
anonymity.

-   [list of Searx public instances
    ](https://searx.space/)
-   [Framabee search](https://framabee.org/)
-   [Searx Wiki](https://github.com/asciimoo/searx/wiki)

Searx allows you to modify the default categories, engines and search
language via the search query in the
[Preference page](https://searx.me/preferences)

You can also use prefixes
-   Category/engine prefix: `!`
-   Language prefix: `:`
-   Prefix to add engines and categories to the currently selected
    categories: `?`

Examples:
-   Search in wikipedia for qwer: `!wp qwer` or `!wikipedia qwer`
-   Image search: `!images Cthulhu`
-   Custom language in wikipedia: `:hu !wp hackerspace`
-   Search in IT category and duckduckgo and wikipedia for qwer:
    `!it !ddg !wp qwer`.

Some Engines codes: archive  (ai), bing (bi), currency (cc), ddg
definitions (ddd), google (go), qwant (qw), reddit (re), wikipedia
(wp), yahoo (yh), yandex (yn), dictzone (dc).

## Search from command line
-   [hrs/engine-mode](https://github.com/hrs/engine-mode)
    is a minor mode for defining and querying search engines through Emacs.
-   <a name="surfraw"></a>[Surfraw](http://surfraw.org/) (public domain)
    is an unix command line interface to  WWW search engines.
    -   [surfraw -GitLab](https://gitlab.com/surfraw/Surfraw)
    -   [surfraw Wiki - GitLab](https://gitlab.com/surfraw/Surfraw)
    -   [Surfraw - ArchWiki](https://wiki.archlinux.org/index.php/Surfraw)
-   [zquestz/s](https://github.com/zquestz/s) (MIT License)
    a golanguage program to open a web search from terminal,
    I provides a Docker file and a snap package.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
