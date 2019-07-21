---
title: Ads blocking
---

{{% toc /%}}

# Why blocking
I will not discuss this controversial topic, but I adhere to
[FiveFilters - Block Ads!
](https://blockads.fivefilters.org/acceptable.html).

# Methods
In these time whatever page you read on the web you get ad banners. But
if you look at the source of the web page you are visualizing, you can
see than most of these banners are stored in ads servers, and **You**
ask them, or at least the browser on **Your** machine ask them, when
instructed to do so by a `src` attribute of an `img` tag or by a
`javascript` request.

If you don't want ads don't ask for them, it looks simple, but how to do
it? You can act at diverse levels

## Block at the browser level
Blocking at the browser level can be done only if your browser allows
it, and most modern browsers like Firefox, Chrome, Safari are known to
support these methods. There are two possibilities:

-   You accept the adds from the network but you instruct the
    browser not to display them.
-   You forbid to load images or frames from a list of ad servers.

There are references to description of these two methods in my
{{< iref "browsers" "browser section" >}}.

If you want to block ad servers you will want to look at
the {{< iref "#ads_site_lists" "lists of ads serving sites" >}}.

Blocking at browser level has the following advantages

-   It is the only possibility when staying at the user level
-   It has the benefit of being without impact on other applications
-   You can block only some URL from a server, you can accept
    `www.mixedserver.com/white` while rejecting
    `www.mixedserver.com/black`, you can only have such a thin
    filtering at the level of the browser, or the proxy, but not at
    the firewall or DNS level. But you can adopt a raw filtering at
    DNS (or firewall) level and a thiner at browser level.
-   In the same way all other methods can avoid to access to an ad
    server but cannot hide the links to them if they are directly in
    the page you are viewing (i.e. not inside an image or loaded via
    javascript). These links can nevertheless be hidden by css
    rules.
-   Even if you adopt for your site an other method, you can still
    block supplementary sites, when browsing with firefox, just by
    right clicking on a image, then on the `Block images from ...`
    menu entry. It is a very good way to test the effect of adding a
    new site to your blocking list.

But it has the following drawbacks:

-   I have no measure of the impact on the performance, but a
    browser is not conceived to do filtering, css is interpreted, it
    cannot be compared with ipfilter or a dns server.
-   One main drawback is that every user has to set is rules for
    every browser it uses.
-   The css matching syntax is complicated, prone to error, needs to
    be carefully validated. It is not at all well adapted to a very
    unstable set of rules, as are produced by these flickering ads.
-   The availability is limited to  browsers accepting an extension
    like the [uBlock Origin](https://github.com/gorhill/uBlock)
    family. What about the others browsers?

## Blocking with a proxy
If you run an {{< iref "proxy" "HTTP Proxy" >}}
it is probably the good place to block ads, it is the minimal load
because you have to test only request to http. It has an easy and
centralized administration, you have the ability to filter with
regexps. If you can have such a proxy on a server for
your whole lan, It is surely the best place to block ads.



Note that this solution is only efficient if you can ensure that the
proxy is in use. the proxy is be configured for each browser of each
user, if you have many computers and users on your lan this can be
tedious.

If the only server always up on your lan is a gateway/firewall with
proprietary software, or too small to run a proxy, you have to find an
other solution or add a new device.

## Block with a firewall
You can block at the IP level on the firewall, but as the list of ad
servers is quite long, you will add a lot of iptables rules which may
slow down your firewall if you don't limit the filtering to a table
that is used only for http request. It is also a very aggressive way
of filtering, and you have to check you are not blocking an important
site. Also if there is many users behind your firewall, there are
probably some ads lovers and you may have to let them get ads, which
complicates a lot your firewall rules.

## Block at name server resolution
Blocking at the name server level is a simple strategy, you redirect
the request to your local host during name resolution. You have to
filter only DNS access not all your network requests. It is
inefficient if the site is given by it's IP address, but presently
it seems unusual for ads (it can become usual if a lot of people
reject DNS for ad servers!).

This solution is also quite aggressive, since a user of your name
server cannot any longer interact with the blocked server, whichever
networking application he uses, so in the same way as for firewall
filtering, if you have some ad lover as user you may have to give
her/him a second unfiltered name server.

To which server can you redirect the blocked url? The usual solution
is to redirect to the localhost (loopback interface) it is the
solution proposed by [The adservers page
](http://pgl.yoyo.org/adservers/index.php). This solution as
numerous drawbacks, usually the url on the ad server does not exist
on your local site and yo get a *404 not found* message, not very
explicit but not too bad. But sometime the url does exist, this is
the case for the empty url or the index, in this case you replace
the ad by your page and it can be very confusing. It is a lot better
to deal with the ad. urls in a more specific way.

I use to bind a specific server on an alias of tan interface of my
http server to deal with advertisements, so I can give a
comprehensive reject message or even transform the url to get some
hiden information as the address of the site I truly wanted to
visit. In fact if you can have some *virtual server* selected by the
socket they use (and not the host name) you don't need a distinc
http daemon. This is the case of lighttpd with the `SERVER["socket]`
configuration option.

You can find in my {{< iref "dns#dnsmasq" "dnsmasq section" >}}
how to use dnsmasq to block ads. A similar strategy is used by Sam
Hocevar in the old page _2002_
[Eradicating doubleclick.net from the planet
](http://sam.zoy.org/writings/internet/doubleclick.html).

An all-in-one solution for adds blocking at the DNS level is
{{< wp "Pi6-Hole" >}} (European Union Public License) which use
{{< iref "dns#dnsmasq" "dnsmasq" >}},
cURL, Lighttpd, PHP and the
[AdminLTE Dashboard](https://github.com/almasaeed2010/AdminLTE)
to block DNS requests for known tracking and advertising domains.

The main references are:

-   [Pi-Hole GitHub Repository](https://github.com/pi-hole/)
-   [Pi-Hole Home Page](https://pi-hole.net/)
-   [Pi-Hole Wiki](https://github.com/pi-hole/pi-hole/wiki)
-   [Pi-Hole FAQ](https://github.com/pi-hole/pi-hole/wiki/FAQs)
-   [Pi-Hole Forums](https://discourse.pi-hole.net/)
-   [Nginx Configuration
    ](https://github.com/pi-hole/pi-hole/wiki/Nginx-Configuration)
    explains how to replace the default lighttpd with Nginx.

The basic principles of Pi-Hole don't seem to be stated clearly in the documentation. Of
course we ca check manually the 2500 lines of the install script, but it can be tedious.

You can also have a look of the outdated 2014 blogs
[Pi-hole: A Raspberry Pi Ad-Blocker with DNS Caching
](https://jacobsalmela.com/2014/06/11/raspberry-pi-block-ads-adtrap/)
and [Block Millions Of Ads Network-wide With A Raspberry Pi-hole 2.0
](https://jacobsalmela.com/2015/06/16/block-millions-ads-network-wide-with-a-raspberry-pi-hole-2-0/)
.

# Lists of intrusive ads urls {#ads_site_lists}

-   [adservers page at pgl.yoyo.org](http://pgl.yoyo.org/adservers/)
-   [AdAway](http://adaway.org/) is an android application to block
    ads their [GitHub repository
    ](https://github.com/sufficiently-secure/ad-away).
    The [Wiki
    ](https://github.com/sufficiently-secure/ad-away)
    has valuable information on ads blocking including a
    [list of lists of ads host
    ](https://github.com/sufficiently-secure/ad-away/wiki/HostsSources).

You can combine many lists with a
[script like this one](https://gist.github.com/smlb/e4b7d25b4be94c1d0ef6).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
