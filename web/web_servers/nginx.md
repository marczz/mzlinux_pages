---
title: Nginx
---


[Nginx](http://nginx.org/) (BSD-like license) is a small http server that can be used as
standalone HTTP server or as a reverse proxy server before another big server to reduce
load.  There are many plugins available to extend the core functionality of Nginx.

Wikipedia: {{< wp "Nginx" >}}.


On raspberry each nginx worker process begin at 1.6M/0.5M and grow to
2.6M/1M, the standard conf is 4 workers, but 2 are sufficient for a
single processor. The master process is 4M/1.4M.

On raspberry I now use nginx + php-fpm the nginx configuration for
fastcgi with php-fpm is commented {{< iref "#fastcgi_php" "below" >}}.

To the nginx processes are added the fastcgi processes, in the case of
this site for php-fpm and python.

Each php-fpm pool process is from 16M/9M to  51M/30M.

# References

-   [Nginx Home](http://nginx.org/)
-   [Nginx admins handbook](https://github.com/trimstray/nginx-admins-handbook)
    is an handbook in a GitHub repository. It contains a
    [list of resources
    ](https://github.com/trimstray/nginx-admins-handbook#external-resources).


# Debian packages
## _nginx-light_
contains:

Standard HTTP modules
:   Core, Access, Auth Basic, Auto Index, Charset, Empty
    GIF, FastCGI, Gzip, Headers, Index, Log, Map, Proxy, Rewrite, Upstream.
Optional HTTP modules
:   Auth Request, Debug, Gzip Precompression, IPv6, Real Ip,
    SSL, Stub Status.
Third party modules
:   Echo
## _nginx-full_
come with:

Standard HTTP modules
:   Core, Access, Auth Basic, Auto Index, Browser,
    Charset, Empty GIF, FastCGI, Geo, Gzip, Headers, Index, Limit Requests,
    Limit Zone, Log, Map, Memcached, Proxy, Referer, Rewrite, SCGI, Split
    Clients, SSI, Upstream, User ID, UWSGI.
Optional HTTP modules
:   Addition, Debug, GeoIP, Gzip Precompression, HTTP Sub,
    Image Filter, IPv6, Real IP, SSL, Stub Status, Substitution,
    [WebDAV](http://nginx.org/en/docs/http/ngx_http_dav_module.html),
    XSLT.
Mail modules
:   Mail Core, IMAP, POP3, SMTP, SSL.
Third party modules
:   Auth PAM, [DAV Ext](https://github.com/arut/nginx-dav-ext-module/),
    Echo, Upstream Fair Queue.

## _nginx-extra_
add to full:
Optional HTTP modules
:   Auth Request, Embedded Perl, FLV, MP4, Random Index, Secure Link,
    Spdy.
Third party modules
:   Chunkin, Embedded Lua, Fancy Index, HttpHeadersMore,
    HTTP Substitution Filter, http push, Nginx Development Kit,
    Upload Progress


# Configuration
-   [nginx documentation](http://nginx.org/en/docs/)
    include documentaition on each module.
-   [Nginx Wiki](https://www.nginx.com/resources/wiki/) -
    [Configuration index](ttps://www.nginx.com/resources/wiki/start/)
-   [nginxconfig.io](https://nginxconfig.io/) is an config generator for nginx.
    The source is
    [GitHub - digitalocean/nginxconfig.io](https://github.com/digitalocean/nginxconfig.io).

# Configuration for PHP-FPM
-   [Optimizing PHP-FPM for High Performance](https://geekflare.com/php-fpm-optimization/).
-   [Nginx and php-fpm for performance
    ](https://jeremymarc.github.io/2013/04/22/nginx-and-php-fpm-for-performance)
    from which following items are extracted.
    -   The global nginx configuration file is located to
            /etc/nginx/nginx.conf
    -   To find the number of worker_processes to allocate use
        2 * numbers of CPUs if dedicated, else use 1 * numbers of CPU.
    -   The worker_processes and worker_connections from the event sections
        allows you to calculate maxclients value:
        max_clients = worker_processes * worker_connections / keepalive_timeout.

# [Nginx Variables](http://nginx.org/en/docs/varindex.html)
-   `$request_filename`
    ::  file path for the current request, based on the
        [root](http://nginx.org/en/docs/http/ngx_http_core_module.html#root) or
        [alias](http://nginx.org/en/docs/http/ngx_http_core_module.html#alias)
        directives, and the request URI.
-   [$document_root
    ](http://nginx.org/en/docs/http/ngx_http_core_module.html#var_document_root)
    ::  [root](http://nginx.org/en/docs/http/ngx_http_core_module.html#root) or
        [alias](http://nginx.org/en/docs/http/ngx_http_core_module.html#alias)
        directive’s value for the current request.
-   [$fastcgi_script_name
    ](http://nginx.org/en/docs/http/ngx_http_fastcgi_module.html#var_fastcgi_script_name)
    request URI or, if a URI ends with a slash, request URI with an
    index file name configured by the
    [fastcgi_index](http://nginx.org/en/docs/http/ngx_http_fastcgi_module.html)
    directive appended to it. This variable can be used to set the
    `SCRIPT_FILENAME` and `PATH_TRANSLATED` parameters that
    determine the script name in PHP.

    When using the [fastcgi_split_path_info
    ](http://nginx.org/en/docs/http/ngx_http_fastcgi_module.html#fastcgi_split_path_info)
    directive, the `$fastcgi_script_name` variable equals the value of the first capture
    set by the directive and [$fastcgi_path_info
    ](http://nginx.org/en/docs/http/ngx_http_fastcgi_module.html#fastcgi_split_path_info)
    the second capture.

    So if there is no index, and we don't use `fastcgi_split_path_info` we have

        $request_filename = $document_root + $fastcgi_script_name

    but if using one of these element they can differ.

# directives

## [Location](http://nginx.org/en/docs/http/ngx_http_core_module.html#location)

Location are either prefix _no indicator_, case-insensitive regular
 expression after `~*` modifier, case-sensitive regular expression after
`~` modifier, or exact after the `=` modifier.

Only __one__ location directive is used.

If there is an exact match, it is  used and the search terminates.

If there is a prefix location, the longer prefix location is
remembered. Then the regular expression are checked in the order of
their appearance in the configuration file. If there is a match the
__first__ match is used, if there is no match the longest prefix is used.

# fastcgi with php-fpm configuration {: #fastcgi_php-fpm}
See also {{< iref "php#php" "PHP-FPM section" >}}.

The configuration that comes from distrib in `fastcgi_params`
configuration file is:

    fastcgi_param QUERY_STRING      $query_string;
    fastcgi_param REQUEST_METHOD    $request_method;
    fastcgi_param CONTENT_TYPE      $content_type;
    fastcgi_param CONTENT_LENGTH    $content_length;

    fastcgi_param SCRIPT_FILENAME   $request_filename;
    fastcgi_param SCRIPT_NAME       $fastcgi_script_name;
    fastcgi_param REQUEST_URI       $request_uri;
    fastcgi_param DOCUMENT_URI      $document_uri;
    fastcgi_param DOCUMENT_ROOT     $document_root;
    fastcgi_param SERVER_PROTOCOL   $server_protocol;

    fastcgi_param GATEWAY_INTERFACE CGI/1.1;
    fastcgi_param SERVER_SOFTWARE   nginx/$nginx_version;

    fastcgi_param REMOTE_ADDR       $remote_addr;
    fastcgi_param REMOTE_PORT       $remote_port;
    fastcgi_param SERVER_ADDR       $server_addr;
    fastcgi_param SERVER_PORT       $server_port;
    fastcgi_param SERVER_NAME       $server_name;

    fastcgi_param SCRIPT_FILENAME   $request_filename;
    fastcgi_param SCRIPT_NAME       $fastcgi_script_name;
    fastcgi_param REQUEST_URI       $request_uri;
    fastcgi_param DOCUMENT_URI      $document_uri;
    fastcgi_param DOCUMENT_ROOT     $document_root;
    fastcgi_param SERVER_PROTOCOL   $server_protocol;

    fastcgi_param GATEWAY_INTERFACE CGI/1.1;
    fastcgi_param SERVER_SOFTWARE   nginx/$nginx_version;

    fastcgi_param REMOTE_ADDR       $remote_addr;
    fastcgi_param REMOTE_PORT       $remote_port;e;

    fastcgi_param HTTPS             $https;

    # PHP only, required if PHP was bith --enable-force-cgi-redirect
    fastcgi_param   REDIRECT_STATUS   200;


To use php-fpm we use _before_ including the previous directives:

    fastcgi_split_path_info ^(.+\.php)(/.+)$;
    fastcgi_pass unix:/var/run/php5-fpm.sock;
    fastcgi_index index.php;

We should be very careful that
[try_files](http://nginx.org/en/docs/http/ngx_http_core_module.html#try_files)
directive changes URI of a request to the one matched on the file system, and subsequent
attempt to split the URI into `$fastcgi_script_name` and `$fastcgi_path_info` results in
empty path info - as there is no path info in the URI after `try_files`.

So we can either save the `$fastcgi_path_info` before the `try_files`
with

    set $path_info $fastcgi_path_info;
    fastcgi_split_path_info ^(.+\.php)($|/.*);
    try_files $fastcgi_script_name =404;

    include fastcgi_params;
    fastcgi_param PATH_INFO $path_info;

Or an easier way is to set the fastcgi parameters __before__ the `try_files`:

    include fastcgi_params;
    fastcgi_param PATH_INFO $fcgi_path_info;
    fastcgi_split_path_info ^(.+\.php)($|/.*);

This is commented in the
[nginx bug #321 (try_files & $fastcgi_path_info)](http://trac.nginx.org/nginx/ticket/321)
and
[Nginx Mailing List: Problem with fastcgi_split_path_info
](http://forum.nginx.org/read.php?2,238825,238825#msg-238825)

We can also use named captures in the location regexp:

    location ~ ^(?<script_name>.+\.php)(?<path_info>/.*)?$ {

Then use `$script_name` and `$path_info`.

# Converting `.htaccess`
Nginx don't uses the apache .htaccess, nor [apache mod_rewrite
](http://httpd.apache.org/docs/2.2/mod/mod_rewrite.html)
but instead the
[Nginx rewrite expressions](http://nginx.org/en/docs/http/ngx_http_rewrite_module.html)
which are close but not the same syntax.

Exemple:

    try_files $uri $uri/ /index.php?q=$uri&$args;

Some apache rewrite rules can also be replaced by [try_files
](http://nginx.org/en/docs/http/ngx_http_core_module.html#try_files)
checks for the existence of files in order, and returns the first file that is found.
In the event that no file is found, an internal redirect to the last parameter is
invoked.

Some converters are available to help the translation:
-   [winginx.com](http://winginx.com) _nginx web server on Windows_
    provide an [htaccess to nginx converter](http://winginx.com/en/htaccess).
-   [apache2nginx (online converter)
    ](http://www.anilcetin.com/)
    Convert apache htaccess rewrite rules to nginx rewrite rules.
    ([GitHub project](https://github.com/mow/apache2nginx) _code from
    year 2012_.

# SSL server
[Configuring HTTPS servers
](http://nginx.org/en/docs/http/configuring_https_servers.html)
is a guide in nginx documentation. It has a serction on
[Name-based HTTPS servers
](http://nginx.org/en/docs/http/configuring_https_servers.html#name_based_https_servers).

A [module for SPDY](http://nginx.org/en/docs/http/ngx_http_spdy_module.html)
is also available. [SPDY (Wikipedia)](http://en.wikipedia.org/wiki/SPDY)
is a networking protocol that reduce http latency by compression, multiplexing, and
prioritization so that only one connection per client is required.

# Memcached {#memcached}
[memcached](https://memcached.org/)
:memcached is a high-performance, distributed memory object
 caching system used for speeding up dynamic web applications;

-   [memc-nginx-module](https://github.com/openresty/memc-nginx-module)
    An extended version of the standard memcached module that supports set, add, delete,
    and  more memcached commands.
-   [openresty/srcache-nginx-module](https://github.com/openresty/srcache-nginx-module)
    Transparent subrequest-based caching layout for arbitrary nginx locations.

# Webdav
Webdav is provided with the [nginx_http_dav_module
](http://nginx.org/en/docs/http/ngx_http_dav_module.html)
which is not built by default, but is provided with its companion *Dav
ext* in the Debian package _nginx-full_.

The PROPFIND and OPTIONS command are not supported by
[ngx_http_dav_module](http://nginx.org/en/docs/http/ngx_http_dav_module.html)
you need a complementary module
[nginx-dav-ext-module](https://github.com/arut/nginx-dav-ext-module)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
