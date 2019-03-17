<!--
.. description:
.. date: 2014-12-17
.. modified:
.. slug: php
.. tags:
.. link:
.. book: mzlinux
.. title: PHP
-->

[TOC]

# PHP references

[PHP Hypertext Preprocessor](http://www.php.net/):
    [PHP Manual](http://www.php.net/manual/en/),
    and [PHP Tutorial](http://www.php.net/tut.php)

-   [PHP Freaks](http://www.phpfreaks.com/)
    website dedicated to learning and teaching PHP.
-   [xdebug extension for PHP](http://www.xdebug.org/)
    helps you debugging your script by providing debug information.
-   [SuPhp](http://www.suphp.org/)
    allows to execute PHP with the id of the user (as module or cgi)
-   [PEAR](http://pear.php.net/):
    [pear manual](http://pear.php.net/manual/en/)
-   [Smarty](http://www.smarty.net) template engine for PHP:
    [Smarty wiki](http://smarty.incutio.com/)
-   [Parser](http://www.parser.ru/en/)
    An object-oriented RAD for web sites.
-   The php fuction `get_browser` allows to retrieve the browser
    capabilities from
    browscap.ini file, the ini variable `browscap` must point on this file.
-   [PHP Everywhere](http://phplens.com/phpeverywhere/)
    (ADOdb database abstraction library)
-   [PHPBuilder](http://www.phpbuilder.com/),
-   [Codewalkers](http://codewalkers.com/)
-   [QUISP (QUIck Server Pages) ](http://quisp.sourceforge.net/)
    solution for developing database-driven dynamic web sites. It
    includes its own embedded SQL database and an embedded data.
    charting package (ploticus).
-   [APC (Alternative PHP Cache)](http://php.net/manual/en/book.apc.php)
    framework for caching and optimizing PHP intermediate code. it is
    part of PECL.

# PHP configuration
-   The PHP configuration can be checked with `<?php phpinfo(); ?>`
    available [here](http://nas.lan/status/phpinfo.php).
-   PHP documentation [How to change configuration settings
    ](http://php.net/manual/en/configuration.changes.php)
    There are 3 types of settings
    `PHP_INI_ALL`, `PHP_INI_PERDIR`, or `PHP_INI_SYSTEM`,
    settings are described in [List of php.ini directives
    ](http://php.net/manual/en/ini.list.php).
-   With  `PHP_INI_ALL`or `PHP_INI_PERDIR` we use
    `php_value name value` or `php_flag name on|off`.
-   With `PHP_INI_SYSTEM` or any other value the setting cannot be
    changed in `ini_set()` and can only be changed with
    `php_admin_value name value` or `php_admin_flag name on|off`.
-   for pydio we need to change `post_max_size = 3G` (default 8M),
    `upload_max_filesize = 3G` (default 2M),
    `max_file_uploads = 200` (default 20)
    The maximum number of files allowed to be uploaded
    simultaneously. (PHP_INI_SYSTEM). These value are to adjust and
    only my current settings.
-   PHP documentation only tell about apache configuration but for fpm
    I change these values in the *pool*, and let the shared php.ini unchanged.

# PHP FPM {: #php-fpm}

-   [PHP: FastCGI Process Manager (FPM) - Manual)
    ](http://php.net/manual/en/install.fpm.php),
    for all the configuration variables look at
    [fpm configuration
    ](http://php.net/manual/en/install.fpm.configuration.php).
-   [How to monitor PHP-FPM (fpm status) - Stack Overflow
    ](http://stackoverflow.com/questions/15465333/php-fpm-processes-monitoring-profiling/15473307#15473307)
-   [PHP-FPM Configuration (php-fpm.conf, www.conf) | myjeeva blog
    ](http://myjeeva.com/php-fpm-configuration-101.html)
-   [Nginx and php-fpm for performance
    ](http://jeremymarc.github.io/2013/04/22/nginx-and-php-fpm-for-performance/)
    from which following item is extracted.
-   To find the maximum number of process you want to allocate in
    `pm.max-children`,
    you use:
    total available RAM / process memory.<br/>
    To find the average process memory you can use

        $ ps u -C php5-fpm

    or

        $ ps -lyC php5-fpmp

    The available memory is what is left of the RAM when you substract
    other services. It can be something like RAM - 500M

As the server on raspberry don't use php on a constant basis, I set
the policy for fpm as `ondemand` with:

    pm = ondemand;
    pm.process_idle_timeout = 10s;
    pm.status_path = /status/fpm;

## differrent php settings for different applications

When running *mod_php* un der apache we can use `php_flag` in apache
configuration or in `.htaccess` to override php.ini configuration.

For _php-fpm_ if we cannot find an acceptable config for all
configuration we may assign different pools with different `listen`
socket or port to different applications.

You can add in the pool configuration additional php.ini defines,
specific to this pool of workers.

These settings override the values previously defined in the php.ini.

# PHP Optimization

To optimize php there is a [talk from Rasmus Ledorf
 ](http://talks.php.net/show/confoo10/1) to sum up:

-   Run a phpinfo() and disable PHP extensions that you don't use. They can take a lot of memory (imagick, curl, ...)
-   Generate a graph of your includes using the inclued.so extension. You might load useless functions in your wordpress setup.
-   Run benchmarks with siege. Sometimes, tiny optimisations have great impact on performance, so make sure you have metrics, to help you make your decisions.
-   Use callgrind to show where you're loosing performance. In one of my project I was using md5() to hash my SQL queries and cache them. The md5() calls where using 20% of the CPU time.

I would definitely start by disabling PHP extensions if possible.

# PHP info
You obtain php inpo by evaluating:

    <?php  phpinfo(); ?>


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
