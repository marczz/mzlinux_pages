<!--
.. description:
.. date: 2014-12-19
.. slug: apache
.. tags:
.. link:
.. book: mzlinux
.. title: Apache httpd
-->


[TOC]

# Apache documentation
- [APACHE](http://www.apache.org)
-   [Apache 2.2 Documentation](http://httpd.apache.org/docs/2.2/):
-   [Last Apache documentation (2.4)](http://httpd.apache.org/docs/current/):
    -   [Directives](http://httpd.apache.org/docs/current/mod/directives.html)
    -   [Apache modules](http://httpd.apache.org/docs/current/mod):
   [mod actions](http://httpd.apache.org/docs/current/mod/mod_actions.html),
   [mod CGI](http://httpd.apache.org/docs/current/mod/mod_cgi.html),
   [mod proxy](http://httpd.apache.org/docs/current/mod/mod_proxy.html),
   [mod rewrite](http://httpd.apache.org/docs/current/mod/mod_rewrite.html),
   [mod\_ssl](http://httpd.apache.org/docs/current/mod/mod_ssl.html),
   - External modules:
     [mod\_fastcgi](http://www.fastcgi.com/mod_fastcgi/docs/mod_fastcgi.html)
     from [fcgi.com](http://www.fastcgi.com/),
     [mod\_fcgid](http://fastcgi.coremail.cn/),
     [mod\_[wsgi](http://code.google.com/p/modwsgi/).
-   [Apache HowTos:](http://httpd.apache.org/docs/current/howto/)
-   [Apache Virtual Host documentation](http://httpd.apache.org/docs/current/vhosts/)
    used to implement [w:Virtual hosting]
    -   There are difficulties to have a proper certificate when using
    [w:https://en.wikipedia.org/wiki/Virtual_hosting#Name-based|Name Based Virtual hosting]
    as described in the previous Wikipedia Page and
    [HTTPS Virtual Hosts in Apache](http://www.crsr.net/Notes/Apache-HTTPS-virtual-host.html)
    [Dynamic Content with CGI](http://httpd.apache.org/docs/current/howto/cgi.html)
-   <strong>mod_ssl</strong> documentation:
    [SSL/TLS Strong Encryption: An Introduction
    ](http://httpd.apache.org/docs/current/ssl/ssl_intro.html),
    [SSL/TLS Strong Encryption: How-To
    ](http://httpd.apache.org/docs/current/ssl/ssl_howto.html),
    [Apache Module mod_ssl
    ](http://httpd.apache.org/docs/current/mod/mod_ssl.html),
    [SSL FAQ](http://httpd.apache.org/docs/current/ssl/ssl_faq.html). See also the page [SSL/TLS](/node/159).
-   [Apache XML Project](http://xml.apache.org/)
    (Xerces: XML parsers in Java and C++, Xalan: XSL stylesheet processors in Java & C+,
    Cocoon: XML-based web publishing, FOP: XSL Formatting Object
    processor in Java, SOAP: Simple Object Access Protocol,&nbsp;)
-   [TangentOrg](http://tangent.org/) by Brian Aker, provides Open
    Source apache modules, **memcache\_engine**, **mod\_mp3**,
    **mod\_layout** *(add footer and header)* ...
-   [Extracting Google Queries from Apache Logs](http://www.madboa.com/geek/apache-google/)
    from Paul Heinlein.
-   [mod\_security crs](http://www.modsecurity.org/)
    the OWASP ModSecurity Core Rule Set
    is a module that provides a request filter, simpler and more
    efficient than mod\_rewrite to filter spam.

     CRS is based on generic rules which focus on attack payload
     identification. It uses following techniques: HTTP request
     validation, HTTP protocol anomalies, Global constraints, HTTP
     Usage policy, Malicious client software detection, Generic Attack
     Detection (SQL injection, Cross Site Scripting, OS Command
     Injection, ColdFusion, PHP and ASP injection, etc.), Trojans &
     Backdoors Detection, Error Detection, XML Protection, Search
     Engine Monitoring.

    -   [ModSecurity Documentation](http://www.modsecurity.org/documentation.html)
    -   [How To Set Up modsecurity with Apache on Debian/Ubuntu | DigitalOcean
        ](https://www.digitalocean.com/community/tutorials/how-to-set-up-mod_security-with-apache-on-debian-ubuntu)
    -   [modsecurity on Apache - Linode Tutorial
        ](https://www.linode.com/docs/websites/apache-tips-and-tricks/modsecurity-on-apache)
    -   [présentation du module ModSecurity
        ](http://www.hsc.fr/ressources/breves/modsecurity.html.fr)
        par Stéphane Milani _2006_.

# How the sections are merged
_taken from [Configuration Sections
](http://httpd.apache.org/docs/current/sections.html)_

-  a ``<Directory>`` section apply to the named filesystem directory and
   all subdirectories of that directory (as well as the files in those
   directories).
-  The ``<Location>`` directive and its regex counterpart, on the other
   hand, change the configuration for content in the webspace.
   It need not have anything to do with the filesystem.

The order of merging is:

1. ``<Directory>`` (except regular expressions) and .htaccess
   done simultaneously (with .htaccess, if allowed, overriding ``<Directory>``)
2. ``<DirectoryMatch>`` (and ``<Directory ~>``)
3. ``<Files>`` and ``<FilesMatch>`` done simultaneously
4. ``<Location>`` and ``<LocationMatch>`` done simultaneously
5. ``<If>``

``<Directory>`` (group 1 above) is processed in the order shortest
directory component to longest.

So for example, ``<Directory /var/web/dir>`` will be processed before
``<Directory /var/web/dir/subdir>``. If multiple ``<Directory>`` sections apply to the
same directory they are processed in the configuration file order.

Later sections override earlier ones

We should take care that the [Options
](http://httpd.apache.org/docs/current/mod/core.html#options)
are __not merged__ but the later one replace the previous ones.
However if __all__ the options on the Options directive are preceded
by a + or - symbol, the options are merged.

Mixing Options with a + or - with those without is rejected by the
config syntax checker.


The `<ProxyPass>` and   `<ProxyPassMatch>` directives are not merged
The first which apply win, so you should place first the most specific
one.

# Apache Authentication Authorization and Access Control

General references on httpd authentication are in the section
[Authentication](/node/156/)

Each Apache security policy is handled by an
[Apache modules](http://httpd.apache.org/docs/current/mod/) they
are summarized in
[Apache Howto: Authentication, Authorization and Access Control](http://httpd.apache.org/docs/current/howto/auth.html).

The
[Access Control](http://httpd.apache.org/docs/current/howto/access.html)
is distinct from [authentication
](http://httpd.apache.org/docs/current/howto/auth.html),
the goal of access control is to limit some part of your site to some _hosts_, but the aim of authentication
is  to limit some part of your site to some _people_.

Access control is done with [mod authz_core
](http://httpd.apache.org/docs/current/mod/mod_authz_core.html)
which allow some user to access a resource and [mod authz_host
](http://httpd.apache.org/docs/current/mod/mod_authz_host.html)
that allow some hosts to have access.

Both authorization and authentication now (in apache 2.4) use the
_Require_ directive.

The _[Require
](http://httpd.apache.org/docs/current/mod/mod_authz_core.html#require)_
directive, replace the older _Allow_, _Deny_ directive, yet available
through a [backward compatibility module
](http://httpd.apache.org/docs/current/mod/mod_access_compat.html).

-   **Authentication type** can be
    [mod\_auth\_basic](http://httpd.apache.org/docs/current/mod/mod_auth_basic.html)
    wich allows the use of HTTP Basic Authentication or
    [mod\_auth\_digest](http://httpd.apache.org/docs/current/mod/mod_auth_digest.html)
    Digest authentication. Digest authentication is not supported
    by dillo, lynx. It is supported by firefox, elinks, w3m.

-   The **authentication provider** can be
    [mod\_authn\_alias](http://httpd.apache.org/docs/current/mod/mod_authn_alias.html)
    that is a convenient alias to an other authentication provider,
    [mod\_authn\_anon](http://httpd.apache.org/docs/current/mod/mod_authn_anon.html)
    that allows access to anonymous users under some conditions (like a
    valid email) and allows to log them,
    [mod\_authn\_file](http://httpd.apache.org/docs/current/mod/mod_authn_file.html)
    provides an authentication by passwords in a file,
    [mod\_authn\_dbm](http://httpd.apache.org/docs/current/mod/mod_authn_dbm.html)
    and
    [mod\_authn\_dbd](http://httpd.apache.org/docs/current/mod/mod_authn_dbd)
    provides authentication front-ends such as mod\_auth\_digest and
    mod\_auth\_basic to authenticate users by looking up users in dbm
    password files or in in SQL tables,
    [mod\_authnz\_ldap](http://httpd.apache.org/docs/current/mod/mod_authnz_ldap.html)
    provides authentication front-ends such as mod\_auth\_basic to
    authenticate users through an ldap directory.

-   The **authorization**is through:
    [mod\_authz\_owner](http://httpd.apache.org/docs/current/mod/mod_authz_owner.html)
    that authorize the owner of some file,
    [mod\_authz\_user](http://httpd.apache.org/docs/current/mod/mod_authz_user.html)
    that allows users authentication,
    [mod\_authnz\_ldap](http://httpd.apache.org/docs/current/mod/mod_authnz_ldap.html),
    that does both authentication and authorization by querying a
    ldap server,
    [mod\_authz\_groupfile](http://httpd.apache.org/docs/current/mod/mod_authz_groupfile.html)
    provides authorization capabilities so that authenticated users can
    be allowed or denied access to portions of the web site by group
    membership. Similar functionality is provided by
    [mod\_authz\_dbm](http://httpd.apache.org/docs/current/mod/mod_authz_dbm.html).
-   [CAS](http://www.ja-sig.org/products/cas/) is an authentication
    system created by Yale University that provides Single Sing On.
    -   [mod-cas (sourceforge)](http://mod-cas.sourceforge.net/) is an
        Apache module integrating CAS authorization.
-   You can mix Authorization and Access control, you can ask to
    satisfy both with `<RequireAll>` block, or either of them with
    a `<RequireAny>` block.

    If you want to let the user to access the ressource if it
    either authenticate _or_   the request comes from an allowed host,
    you can use the `<RequireAny>` block can be
    used, but by default all Require directives are handled as though
    contained within a <RequireAny> container directive,
    the _any_ is the implied so you can use:

        <Location /here>
            Require all granted
            AuthBasicProvider file
            AuthType Basic
            AuthName "Secret zone"
            AuthUserFile "secret_allowed"
            Require valid-user
            Require ip 10.172.20.0/24
        </Location>

    The older (<=2.2) way was to use `Satisfy`
    directive as in the following:

        <Location /here>
            Order deny,allow
            Deny from all
            Allow from 10.172.20.0/24
            AuthType Basic
            AuthName "Secret zone"
            AuthUserFile "secret_allowed"
            Require valid-user
            Satisfy Any
        </Location>

# Apache configuration
With apache2-mpm-prefork we need the modules:

-   libapache2-mod-php5 libapache2-mod-fcgid (apache2-mpm-prefork) wwwconfig-common
-   mysql-server-5.0, mysql-admin (not mysql-query-browser that would
    install half of gnome), phpmyadmin, dbconfig-common
-   for drupal php5-mysql php5-gd

-   [web htpasswd generation](http://www.xs4all.nl/~remcovz/htpasswd.html)
-   to check a crypt entry in .htpasswd we can use python and crypt library:

        crypt.crypt(cleartext, cryptedpasswd) == cryptedpasswd

## apache memory footprint
-   sur nas apache2-mpm-prefork 4.6M/1.2 root process +3.9M/0.6+ 4.8M/1.2 + 4 procs 3.7M/0.4
-   sur nas apache2-mpm-worker is threaded 2.6/1.3 + 2 process 2.2/740
    with many threads , can be configured.
-   raspberry apache-mpm-events 2 processes, many threads 5M/1.4M
-   lighttpd is 2.7M/1.3
-   marcltop apache2-mpm-prefork 5x5.6/0.4

- php-cgi processes uses 13M/5.6M

# php5 fcgi on apache 2.2
We should prefer __php-fpm__ for configuration look at
[php-fpm (section)](/node/php#php-fpm "internal reference").

-   For apache2.2 we can use [mod_fcgid
    ](https://httpd.apache.org/mod_fcgid/mod/mod_fcgid.html#fcgidwrapper)
-   With apache 2.2 ``php-fpm`` is available but we need ``mod_fastcgi``, which is
    not available in Debian, and not at all compiled with raspberry.
    we can compile it using the instructions of
    [Raspberry PI: Installing LAMP with FastCGI, PHP-FPM and APC
    ](http://raspberryserver.blogspot.fr/2013/02/installing-lamp-with-fastcgi-php-fpm.html) or
    [Installing LAMP with FastCGI and PHP-FPM on Raspberry PI
    ](http://www.wirasoenaryo.com/installing-lamp-with-fastcgi-and-php-fpm-on-raspberry-pi/), or
    [Installing LAMP with FastCGI, PHP-FPM and APC
    ](http://raspberryserver.blogspot.fr/), or _the more detailled tutorial_
    [How to install Apache2 + PHP-FPM on Raspberry Pi
    ](https://raspberry-hosting.com/en/faq/how-install-apache2-php-fpm-raspberry-pi).
-   For Debian amd64 there is a fastcgi and we can use
    [Install Mod-FastCGI and PHP5-FPM on Ubuntu
    ](http://blog.starcklin.com/2013/08/install-mod-fastcgi-and-php5-fpm-on-ubuntu/)
-   To use a simple inefficient fcgi with mode fcgid we follow the
    apache doc: [mod<sub>fcgid</sub>: fcgidwrapper
    ](https://httpd.apache.org/mod_fcgid/mod/mod_fcgid.html#fcgidwrapper)
-   the wrapper is in `/usr/local/bin/php-wrapper` and has its own
    php.ini, in the directory.
-   The file ``mods-enabled/mod_fcgid.conf`` is changed in:

        <IfModule mod_fcgid.c>
          AddHandler    fcgid-script .fcgi
          FcgidConnectTimeout 20
          # to replace fcgi by fcgid+ cgi executed in a wrapper
          AddHandler fcgid-script .php
          Options +ExecCGI
          FcgidWrapper /usr/local/bin/php-wrapper .php
        </IfModule>

-    But each php-cgi takes 80M/30M or 75M/27M.

# php-fpm on apache 2.4
for configuration look at
[php-fpm (section)](node/php#php-fpm "internal reference")

-   With apache 2.4 standard on jessie, we can
    [use php-fpm out of the box as reverse proxy
    ](https://wiki.apache.org/httpd/PHP-FPM) _from Httpd Wiki_
-   It is also usable on raspberry with lighttpd as set in
    [How To Setup A Web Server On Your Raspberry Pi
    ](http://www.raspberrypi-spy.co.uk/2013/06/how-to-setup-a-web-server-on-your-raspberry-pi/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
