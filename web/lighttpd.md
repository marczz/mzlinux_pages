---
title: Lighttpd
---

{{% toc /%}}

[lighttpd](http://www.lighttpd.net/) is a low memory footprint http server (1.3 Meg
    base+cgi) with FastCGI, CGI, SSI, Auth, Output-Compression,
    URL-Rewriting, SSL.

-   The live documentation is on the
    [lighttpd wiki](http://redmine.lighttpd.net/projects/lighttpd/wiki/).
-   A [collection of lighttpd tutorials
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Tutorials)
-   Gentoo [Lighttpd How-To](http://en.gentoo-wiki.com/wiki/Lighttpd)
-   [lighttpd forums](http://redmine.lighttpd.net/projects/lighttpd/boards)
     and
    [lighttpd news list at gmame](http://news.gmane.org/gmane.comp.web.lighttpd).
-   [lighttpd local doc](http://localhost/doc/lighttpd-doc/)

## [Lighttpd configuration](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:Configuration)

Look at the [Lighttpd wiki documentation](http://redmine.lighttpd.net/projects/1/wiki/Docs) for full documentation, I just give here some pointers on sections that I use most.

-   [Configuration File Syntax
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:Configuration)
    gives the general syntax the use of contexts which allows
    conditional configuration based on url, host, remote ip, referer,
    user agent, cookie ... and the use of variables
-   [Configuration Options
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ConfigurationOptions)
    gives all options for each module.
-   [SSL and HTTPS
    server](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:SSL)
-  htpasswd can be replaced by
   [htpasswd.py from Trac project](http://trac.edgewall.org/browser/trunk/contrib/htpasswd.py)

## Configuration parsing
The parsing, and evaluation of the configuration is not documented in Lighttpd Site
_or I have not found the right place!_. But it is very important to understand it because the result could be very different to what one expect.

The parsing is done sequentially, and the variable local to a block are initialized from their global value.
This mean that global changes of variables will unseen in a conditional previously declared.

The evaluation is not done sequentially, the global config is overriden by the conditional block that applies.

It means that with a configuration like:

    alias.url += ( "/a/" => "/home/user/a/" )
    $HTTP["remoteip"] == "127.0.0.1" {
        alias.url += ( "/doc/" => "/usr/share/doc/" )
    }
    alias.url += ( "/b/" => "/home/user/b/" )

`http://localhost/a` is aliased but not `http://localhost/b`.

The failure to recognize it is the [bug 1427](http://redmine.lighttpd.net/issues/1427)

## Main modules

-   [mod\_accesslog
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModAccessLog)
    logs are configurable like those of Apache
-   [mod\_auth](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModAuth)
    support basic and digest authentication using plain file,
    htpassword, htdigest or ldap.
-   [mod\_cgi
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModCGI)
    which can assign an extension to some cgi script, with the use of _contexts_
    the cgi is usually limited to some urls, hosts, ...
-   [mod\_compress
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModCompress)
    allows output compression and caching of compressed files.
-   [mod\_evhost
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModEVhost)
    or Enhanced Virtual-Hosting to select the document-root based on a pattern.
    It extend the module
    [mod\_simple\_vhost
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModSimpleVhost)
    in which  every virtual host is in a directory whose name is the vhost name.
    In [mod\_mysql\_vhost
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModMySQLVhost)
    the path to a given host's document root is stored in a MySQL database,
-   [mod\_fastcgi](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModFastCGI)
    support the FastCGI interface that can improve the bad performance
    of cgi protocol. Lighttpd provides an internal FastCGI
    load-balancer  to balance the load over multiple FastCGI Servers.

     The fastcgi server can be selected from the file extension
     _and an appropriate context_. This module is used for serving
     _php_, _python_, _perl_ or _C/C++_ programs.

    [mod\_scgi](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModSCGI)
    is a clone of _mod_fasctcgi_, but using the {{< wp "SCGI" >}} protocol instead of
    {{< wp "FastCGI" >}}. Perl, Python, PHP have a _SCGI_ interface as well as a
    FastCGI one, _SCGI_ is also used with Java, Haskell, Ruby ...
-   [mod\_magnet](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModMagnet)
    allows you to do more complex URL rewrites and caching than
    _mod_rewrite_ would allow.

    When using _mod_magnet_ you can control the request handling thru a
    _lua_ program.

    [AbsoLUAtion](http://redmine.lighttpd.net/projects/lighttpd/wiki/AbsoLUAtion)
    gives numerous examples or pointers to example for numerous tasks , including the
    _now standard_ way of serving _drupal_ thru lighttpd, and a rewrite in
    _mod_magnet_ of the Apache _mod_security_.
-   [mod\_rewrite
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModRewrite)
    implement internal redirects, url rewrite, it has a memo below.
-   [mod\_webdav](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModWebDAV)
    is a very minimalistic implementation of RFC 2518 implementing  _PROPFIND_,
    _OPTIONS_, _MKCOL_, _DELETE_, _PUT_, _LOCK_  and the usual GET,
    POST, HEAD from HTTP/1.1.
-  [ModWebDAV](http://redmine.lighttpd.net/wiki/lighttpd/Docs:ModWebDAV)
-  [How To Set Up WebDAV With Lighttpd On Debian Squeeze
   ](http://www.howtoforge.com/how-to-set-up-webdav-with-lighttpd-on-debian-squeeze)

## __Common modules__
that require options but no complicated    configuration

-   [mod\_access
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModAccess)
    to deny access to some urls,
-   [mod\_alias
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModAlias)
    to alias an url to some file system directory,
-   [mod\_dirlisting
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModDirlisting),
-   [mod\_expire
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModExpire)
    controls the expiration of content in caches,
-   [mod\_setenv
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModSetEnv)
    allows influencing the environment external applications are
    spawned in and the response headers the server sends to the
    clients, see the previous reference to get a proper
    _Content-Encoding_ header to induce decompression by the user
    agent of compressed text files,
-   [mod\_status
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModStatus)
    generates the status overview of the webserver,
-   [mod\_userdir
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModUserDir)
    provides a simple way to link user-based directories into the
    global namespace of the webserver,

## __Modules used for a specific task__

-   [mod\_evasive](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModEvasive)
    to limit the number of connections by ip,
-   [mod\_expire](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModExpire)
    controls the expiration of content in caches,
-   [mod\_extforward
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModExtForward)
    for servers behind reverse proxy servers,
-   [mod\_flv\_streaming
    ](http://blog.lighttpd.net/articles/2006/03/09/flv-streaming-with-lighttpd)
    to stream flv in the lighttpd server,
-   [mod\_mysql\_vhost
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModMySQLVhost)
    store the path to a given host's document root in a MySQL database,
-   [mod\_rrdtool
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModRRDTool)
    to store and display time-series data,
-   [mod\_secdownload
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModSecDownload)
    allows secure download by introducing a way to authenticate a URL
    for a specified time,
-   [mod\_ssi
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModSSI)
    is for the deprecated _ssi_ protocol,
-   [mod\_trigger\_b4\_dl
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModTriggerBeforeDownload)
    implement for server request a protocol analogous to what is port
    knocking at the IP level. An url is authorized only after the
    client has hit a _trigger-url_.
-   [mod\_usertrack
    ](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModUserTrack)
    is a _user click tracking_ module.


This memo is extracted from the main
[mod\_rewrite documentation](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModRewrite) to which you can refer for more details.

Be warned that url rewriting does not work within a $HTTP["url"] conditional
(but it does with other conditions like  $HTTP["referer"]).
We have also to remember that the rewrite is done __before__ url are handled.
If you have  an _alias_ or a _redirect_ it is matched to the rewritten
url. (
[mod\_rewrite
documentation](http://redmine.lighttpd.net/projects/lighttpd/wiki/Docs:ModRewrite)
gives a trick to skip the redirection).

# Lighttpd rewrite memo
There are two options  url.rewrite-once and url.rewrite-repeat they have both the same syntax:

    url.rewrite-once = (
      "<regex1>" => "<relative-uri1>",
      "<regex2>" => "<relative-uri2>"
      ....
    )

The regex are standard extended regular expressions

-   .  match any character
-   \*  - match zero or more of the previous symbol
-   \+  - match one or more of the previous symbol
-   ? - match zero or one of the previous symbol
-   \^ (caret) - match the start of a string
-   $ (dollar) - match the end of a string
-   [set] - match any one of the symbols inside the square braces.
    [\^set] - match any symbol that is NOT inside the square braces.
-   (pattern) - used for grouping, remember what the pattern matched as a
    special variable
-   {n,m} - from n to m times matching the previous character (m could
    be omitted to mean >=n times)
-   (?!expression) - match anything BUT expression at the current
-   \\x (backslash-something) - match special characters


$1..$9 in the replacement refer to the captured text in the
matching group.

When the replacement occur within a condition using a regex
 %0 is replaced by the entire substring matching the regexp;
 %1, %2,... by the firs (second, ...) subexpression

Lighttpd from version  1.4.24 has two more rewrite rules
url.rewrite-[repeat-]if-not-file that skip the rewrite it the pattern
match an existing file (but not directory, socket, ...) and
mimic Apache´s "!-f" RewriteRule.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
