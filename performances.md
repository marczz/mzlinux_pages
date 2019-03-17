<!--
.. description:
.. date: 2014-08-26
.. slug: performances
.. tags:
.. link:
.. book:mzlinux
.. title: Performance Tuning
-->

[TOC]

# References

-   [ArchWiki: Maximizing performance
    ](https://wiki.archlinux.org/index.php/Maximizing_performance)
-   [Red Hat administration guide Performance Tuning Guide
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Performance_Tuning_Guide/index.html)
    describe Performance Monitoring Tools, Cpu, Memory, File Sytem,
    Networking tuning .
-   some chapters are not yet in the last beta edition so you find
    them in [Red Hat Enterprise Linux 6  Performance Tuning Guide
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html-single/Performance_Tuning_Guide/index.html)


# Input/output scheduling {#io_scheduling}
-   You find also an explication of different schedulers in
    [The Red Hat Enterprise Linux 6 Performance Tuning Guide - Input/output
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html-single/Performance_Tuning_Guide/index.html#main-io),
    it explains analysis of i/o with _vmstat_, and the tools in
    package blktrace: _blktrace_, _blkparse_ , _btt_.


For io scheduling we can use the [w:CFQ|cfq scheduler].

-   The role of scheduler is explained in [Linux Kernel Development
    ]( http://www.makelinux.net/books/lkd2/)
    [I/O Schedulers chapter
    ](http://www.makelinux.net/books/lkd2/ch13lev1sec5).
-   Explained in [Fedora : Resource management guide
    ](http://docs.fedoraproject.org/en-US/Fedora/17/html/Resource_Management_Guide/ch-Subsystems_and_Tunable_Parameters.html)
    , [RedHat Entreprise:  Resource management guide -blkio
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/6/html/Resource_Management_Guide/ch-Subsystems_and_Tunable_Parameters.html#sec-blkio)
-   Its use with ionice is summarized in
       [How To Avoid Sudden Outburst Of Backup Shell Script / Program Disk I/O](http://www.cyberciti.biz/tips/linux-set-io-scheduling-class-priority.html)

# QOS and Network bandwith control {#qos}

-   [RedHat Performance Tuning Guide - 6. Networking
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7/html/Performance_Tuning_Guide/sect-Red_Hat_Enterprise_Linux-Performance_Tuning_Guide-Networking-Configuration_tools.html)
    monitoring with: ss, ip, dropwatch, ethtool, /proc/net/snmp,
    SystemTap; . Configuration tools tuned-adm, ethtool, configuring
    with _sys_ subsystem.

Some tools to control bandwith usage:

-   [wondershapper](http://lartc.org/wondershaper/) (in debian)
-   [shaperd
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=shaperd) in debian.
-   [pyshaper](http://freenet.mcnabhosting.com/python/pyshaper/)  an older tool.
-   [trickle](http://monkey.org/~marius/pages/?page=trickle) in debian
    -   [trickle Github repository](https://github.com/mariusae/trickle)
    -   [ArchWiki: Trickle](https://wiki.archlinux.org/index.php/Trickle).
    -   [Use bandwidth shapers (wondershaper or trickle) to limit
        internet connection speed
        ](http://www.ubuntugeek.com/use-bandwidth-shapers-wondershaper-or-trickle-to-limit-internet-connection-speed.html)
    -   [Control your bandwidth with Trickle
        ](http://www.tuxradar.com/content/control-your-bandwidth-trickle).
    -   [stackexchange: How to change speed limit of running trickle instance
        ](http://unix.stackexchange.com/questions/109973/how-to-change-speed-limit-of-running-trickle-instance).
-   To display bandwidth usage on an interface you can use
    [iftop](http://www.ex-parrot.com/~pdw/iftop/),or
    [ntopng](http://www.ntop.org/).

# ACPI
-   [acpi wakeup](http://www.mythtv.org/wiki/ACPI_Wakeup)
-   Enabling wakeup by USB device interrupt (e.g. from mouse or keyboard)
     Execute the following, e.g. by adding it to /etc/rc.local at least once after each bootup:

         awk '/^USB.*disabled/ {print $1}' /proc/acpi/wakeup | while read dev; do echo $dev > /proc/acpi/wakeup ; done
