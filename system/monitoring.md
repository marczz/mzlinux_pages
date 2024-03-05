---
title: Monitoring
---

See also
{{< iref "configuration_management" "Configuration Management" >}} and
{{< iref "nettools#ip_tools" "Command line IP Tools" >}}.

# References

-   [ArchWiki](https://wiki.archlinux.org/index.php/):
    -   [Category Status monitoring and notification
        ](https://wiki.archlinux.org/index.php/Category:Status_monitoring_and_notification)
    -   [Benchmarking](https://wiki.archlinux.org/title/Benchmarking)
        refer to many tools to test Hdrives: __s__, __iozone__, __Bonnie++__, ...
-   Wikipedia {{< wp "System monitor" >}}
-   [Top 25 Best Linux Performance Monitoring and Debugging Tools
    ](http://www.thegeekstuff.com/2011/12/linux-performance-monitoring-tools/)
    by Ramesh Natarajan. _2011_
-   [High Performance Browser Networking
    ](http://chimera.labs.oreilly.com/books/1230000000545/index.html)
    by Ilya Grigorik. You can also browse the
    [blog of Ilya Grigorik](http://www.igvita.com/)
    with an impressive
    [list of performance related articles](http://www.igvita.com/archives/).
-   [Linux Profiling tools and techniques - Pixelbeat
    ](https://www.pixelbeat.org/programming/profiling/)
-   [System Monitoring Tools :: Fedora Docs
    ](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/monitoring-and-automation/System_Monitoring_Tools/)
    describe many basics system commands: ps, top, free, lsblk, blkid, partx, findmnt,
    df, du, lspci, lsusb, lspcmia, lscpu, hw-probe, Net-SNMP.
-   [System Monitoring Utilities - Suse Entreprise Server Documentation
    ](https://documentation.suse.com/sles/12-SP5/html/SLES-all/cha-util.html)
    exemple of basic utilities like vmstat, dstat, sar, iostat, mpstat, turbostat,
    pidstat, dmesg, lsof, udevadm monitor, ipcs, ps, pstree, top, hyptop, iotop, nice,
    renice, free, ip, nethog, ethtool, ss, procinfo, lspci, lsusb, tmon, file, mount,
    df, du, stat, fuser, w, time, RRDtool,
-   [Monitoring and managing system status and performance - Red Hat Enterprise Linux 9
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/monitoring_and_managing_system_status_and_performance/index)
    describe many utilities, tuned, Performance Co-Pilot (PCP); poxertop, perf,numastat,
    using the kernel cgroups, systemtap, ...


## CPU use
For the cpu usage the standard criterias are load average, cpu user
and system time, cpu wait, Memory and Swap space either used, free,
or buffered.

CPU Wait occurs when the CPU can't perform computations because it
is waiting on I/O operations. Most of the time this occurs because
of disk or network I/O operations including paging in the swap
area

-   [Wikipedia: {{ "wp" "Load (computing)" >}}
-   [Examining Load Average - Linux Journal](https://www.linuxjournal.com/article/9001).


# Monitoring Tools {#monitoring_tools}


<a name="conky"></a>[conky](https://github.com/brndnmtthws/conky) (GPL)
:   Conky is a light-weight system monitor which can display arbitrary information to
    the root window, in X11, wayland, or in a terminal.  A lot of plugin exists that
    allow to view information not only from system but also from running daemons like
    cupsd, mpd, xmm2, audacious

    In Debian there is three packages:

    -   The basic _conky-cli_ useful in servers or piped to a
        {{< iref "desktop#menu-system" "desktop menu application" >}} it includes
        _MPD_, _MOC_, _math_, _apcupsd_, _ncurses_ and _I/O stats_.
    -   _conky-std_ includes _X11_, _XDamage_, _XDBE_, _Xft_, _MPD_, _MOC_, _math_,
        _hddtemp_, _portmon_, _wireless_, _ncurses_, _apcupsd_, _I/O stats_, _argb_ and
        _Lua_.
    -   _conky-all_ includes _X11_, _XDamage_, _XDBE_, _Xft_, _MPD_, _MOC_, _math_,
        _hddtemp_, _portmon_, _wireless_, _ncurses_, _apcupsd_, _I/O stats_, _argb_,
        _Lua with cairo and imlib2 Lua bindings_, _IBM_, _nvidia_, _eve-online_,
        _Imlib2_, _Audacious_, _XMMS2_, and _PulseAudio_.

    A conky daemon for the standard plugins (in the _conky-std_ Debian package) and the
    standard configuration uses 4M res / 3.2M shared.  It is a pure X11 application and
    most shared space is probably the X libraries that are yet loaded, so I see only an
    increase of 1.5M of used memory under my fluxbox desktop.Of course it depends on
    both the building configuration, and the instance configuration in `.conkyrc`.

    But the more efficient way of running conky is to disable x and pipe to console,
    tmux, screen dzen, dmenu, rofi ...  A no-X conky daemon uses only 2.2M res/1.6shrd,
    with usually many threads or processes.  If you don't need to see your system with a
    refresh rate of 1s but are happy with an update each 5 of 10 second you can even
    launch discontinuous instance of conky.

    -   [Conky - GitHub](https://github.com/brndnmtthws/conky/)
    -   [Conky Wiki](https://github.com/brndnmtthws/conky/wiki)
    -   [Conky FAQ](https://github.com/brndnmtthws/conky/wiki/FAQ)
    -   [Conky Home (conky.cc)](https://conky.cc/)
        -   [List of conky variables (conky.cc)](https://conky.cc/variables), [on
            sourceforge](http://conky.sourceforge.net/variables.html)
        -   [List of configuration Settings (conky.cc)](https://conky.cc/variables), [on
            sourceforge](http://conky.sourceforge.net/config_settings.html)
        -   [Lua Api (conky.cc)](https://conky.cc/lua)
    -   {{< wp "Conky_(software)" "Wikipedia: Conky" >}}.
    -   [Gentoo Wiki: Conky Guide](https://wiki.gentoo.org/wiki/Conky/Guide).
    -   [ArchWiki: conky](https://wiki.archlinux.org/index.php/Conky), [Conky/Tips and
        tricks](https://wiki.archlinux.org/index.php/Conky/Tips_and_tricks)
    -   [linux.com guide to configuring Conky
        ](http://www.linux.com/archive/feature/136147) By Dmitri Popov.
    -   The [Ubuntu conky configuration thread
        ](http://ubuntuforums.org/showthread.php?t=281865) _huge! 23471 posts from 2006
        to 2020_.
    -   [Conky Companions PPA](https://launchpad.net/~conky-companions/+archive/ppa)
        Kaivalagi's Python Scripts collection _Conky_, mainly aimed at media player
        control. _Last release 2013._
    -   Conky has a built-in local email, pop3 and imap checker.  To use imap-tls you
        can combine with stunnel as stated in the
        [FAQ](http://conky.sourceforge.net/faq.html)
    -   There are also multiple way of checking a remote imap mailbox, some specific for
        gmail:
        -   [a script using
            curl](http://gnome-look.org/content/show.php/?content=125087),
        -   [conkygmailcheck](http://sourceforge.net/projects/conkygmailcheck/) written
            in python,
        -   conkyemail in [Conky Companions
            PPA](https://launchpad.net/~conky-companions/+archive/ppa)
    -   [Ubuntu fr - Conky](https://doc.ubuntu-fr.org/conky) publish conky scripts
        -   [conky system](https://doc.ubuntu-fr.org/conky_scripts_systeme),
        -   [conky multimedia](https://doc.ubuntu-fr.org/conky_scripts_multimedia),
    -   [using conky with screen or tmux
        ](https://github.com/brndnmtthws/conky/wiki/Window-Configuration#gnu-screen)
    -   [MerkeX/conky-manager2](https://github.com/MerkeX/conky-manager2) Fork of GUI
        for managing Conky widget.

<a name="gkrellm"></a>[Gkrellm](http://www.gkrellm.net/) (GPL)
:   Gkrellm is a gtk stack of system monitors that includes
    clock/cpu/proc/memory/swap/network/disk/mail notification monitors. It has a 20M
    resident memory footprint.
    -    Themail notifier support pop3/imap and ssl.

[HardInfo](https://github.com/lpereira/hardinfo)
:   is a small application that displays information about your hardware and operating
    system. Currently it knows about PCI, ISA PnP, USB, IDE, SCSI, Serial and parallel
    port devices.  [Debian - hardinfo](https://packages.debian.org/sid/hardinfo).

<a name="libstatgrab">[libstatgrab](http://www.i-scream.org/libstatgrab/) (GPL)
:   is a C library that provides access to statistics about CPU usage,
    memory utilisation, disk usage, process counts, network traffic,
    disk I/O.  _libstatgrab_ is in Debian.

    -   python bindings are in
        [pystatgrab](http://www.i-scream.org/pystatgrab/)
        _named python-statgrab in Debian_.
    -   _statgrab_ is a sysctl-style interface to the statistics
        gathered by libstatgrab.  Included with _statgrab_ is a
        script to generate an {{< iref "#mtrg" "MRTG" >}}
        configuration file to use _statgrab_.
    -   <a name="saidar"></a>[saidar](http://www.i-scream.org/libstatgrab/) (GPL)
        provides a curses-based interface to libstatgrab to view the current state of
        the system.
    -   <a name="bwm-ng"></a>[Bwm-ng](http://www.gropp.org/?id=projects&sub=bwm-ng)
        Bandwidth Monitor NG is a small and simple console-based live
        network and disk io bandwidth monitor. It uses libstatgrab.

[linfo](http://linfo.sourceforge.net/)
:   A PHP application that displays the system hardware and realtime
    server health.
    -   [GitHub: linfo](https://github.com/jrgp/linfo).

[linux-dash : Server Monitoring Web Dashboard](http://linuxdash.afaqtariq.com/)
:   written in go and javascript, gives system information, the UI is
    configurable.
    -   [GitHub: linux-dash](https://github.com/afaqurk/linux-dash).

[lm-sensors](http://www.lm-sensors.org/):
    -   [archlinux lm-sensors howto
        ](http://wiki.archlinux.org/index.php/Lm_sensors),
    -   [archlinux: fan speed control
        ](http://wiki.archlinux.org/index.php/Fan_speed_control)

[Netdata](https://github.com/netdata/) (GPL-3.0)
:   Netdata is distributed, real-time, performance and health monitoring for systems and
    applications. It provides insights of everything happening on the systems it runs
    using interactive web dashboards.

    It can run autonomously without any third party components or it can be integrated
    to existing monitoring tool chains (Prometheus, Graphite, OpenTSDB, Kafka, Grafana,
    etc).

    It is packaged in multiple Debian packages.

    The [Netdata Site](https://www.netdata.cloud) present the open source edition and
    paid extensions.

    For using Netdata on small sbc refer to the [Armbian discussion
    ](https://forum.armbian.com/topic/9785-netdata-is-awesome/)
    including the [advices of the Netdata author
    ](https://forum.armbian.com/topic/9785-netdata-is-awesome/?do=findComment&comment=73978).

[Nfswatch](http://sourceforge.net/projects/nfswatch/) (BSD License)
:   Nfswatch is a command-line tool for monitoring NFS traffic. It can
    monitor NFS requests and reply and measure the response time for
    each RPC on a particular network interface or on all interfaces.

[neofetch](https://github.com/dylanaraps/neofetch)
:   Is a fast, highly customizable system info bash script.

[phpsysinfo](http://phpsysinfo.sourceforge.net/) (GPL)
:   is a PHP script that displays information about uptime, CPU,
    Memory, PCI devices, SCSI devices, IDE devices, Network adapters,
    Disk usage on the iotop - simple top-like I/O monitor local host.
    It is in Debian.

[systat](http://sebastien.godard.pagesperso-orange.fr/)
:   is a suite of system monitoring tools. It is provided as a
    _systat_ Debian package.  The utilities include sar, sadf, mpstat,
    iostat, nfsiostat, cifsiostat, pidstat and sa tools.

    -   [24 iostat, vmstat and mpstat Examples for  Performance Monitoring
        ](http://www.thegeekstuff.com/2011/07/iostat-vmstat-mpstat-examples/)
        by Ramesh Natarajan _2011_.
    -   [pidstat(1)
        ](http://sebastien.godard.pagesperso-orange.fr/man_pidstat.html)
        is used to monitor processes and threads
        -   [Using pidstat tutorial
             ](http://sebastien.godard.pagesperso-orange.fr/tutorial.html#Section2)
    -   {{< wp "iostat" >}} report Central Processing Unit (CPU) statistics and
        input/output statistics for devices, partitions and network
        filesystems.
        -   [iostat(1) manual](http://linux.die.net/man/1/iostat) and
            [iostat(8) bsd manual](http://www.freebsd.org/cgi/man.cgi?iostat).
        -   [ On iostat, disk latency; iohist onward!
            ](http://blog.jcole.us/2007/05/08/on-iostat-disk-latency-iohist-onward/)
            by  Jeremy Cole.
        -   [Monitoring IO Performance with iostat
            ](http://www.igvita.com/2009/06/23/measuring-optimizing-io-performance/)
            by Ilya Grigorik.
    -   {{< wp "mpstat" >}} report processors statistics.
        [mpstat(1)](http://linux.die.net/man/1/mpstat).
    -   [sar(1)](http://sebastien.godard.pagesperso-orange.fr/man_sar.html)
        Collect, report, or save system activity information.
        -   [Using sar and sadf
            ](http://sebastien.godard.pagesperso-orange.fr/tutorial.html)
            a _systat_ tutorial.
        -   [10 Useful Sar (Sysstat) Examples for UNIX / Linux Performance Monitoring
            ](http://www.thegeekstuff.com/2011/03/sar-examples/)

## Profiling
[oprofile](https://oprofile.sourceforge.io/about/) (GPL-2)
is a profiler for Linux, capable of profiling all running code at low overhead.

There are many oprofile
[![packaging](https://repology.org/badge/tiny-repos/oprofile.svg?header=packages)
](https://repology.org/project/oprofile/versions), including Ubuntu, but not Debian.

-   [OProfile documentation](https://oprofile.sourceforge.io/docs/)
-   [OProfile :: Fedora Docs
    ](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/monitoring-and-automation/OProfile/)

<a name="perf"></a>[perf](https://perf.wiki.kernel.org/index.php/Main_Page)
:   is a tool to instrument CPU performance counters, tracepoints, kprobes, and uprobes
    (dynamic tracing). It is capable of lightweight profiling, and is included in the
    Linux kernel. *It is in the Debian package linux-perf.*
    -   [Linux perf Examples](https://www.brendangregg.com/perf.html) by
        [Brendan Gregg](https://www.brendangregg.com/index.html),
        which has many [performance related material
        ](https://www.brendangregg.com/overview.html).
    -   The section  Monitoring and managing system status and performance from the Red
            Hat entreprise documentation has several chapters dedicated to perf,
            [Chapter 16
            ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/monitoring_and_managing_system_status_and_performance/getting-started-with-perf_monitoring-and-managing-system-status-and-performance)
            to chapter 27.
[Valgrind Massif](https://valgrind.org/docs/manual/ms-manual.html) (GPL-2)
:   Massif is a heap profiler. It measures how much heap memory your program uses; it
    can allow you to reduce your program memory footprint.

## **Top** and friends
-   {{< man "top" >}} - real-time view of  system summary information as well as a list
    of processes or threads.
-   {{< man "atop" >}} - AT Computing's System & Process Monitor
-   [bottom](https://github.com/ClementTsang/bottom) (MIT License)
    a rust graphical process/system monitor for the terminal.

    A deb package is provided in the releases.
-   [btop](https://github.com/aristocratos/btop#help-menu) (apache 2)
    A resource monitor that shows usage and stats for processor, memory, disks, network
    and processes. Packaged in Debian.

    The keybindings are shown with the key **h** or **F1**.

    The configuration is not externally documented, but *btop* place an auto-generated
    commented configuration in `$HOME/.config/btop`, `vim_keys=true` allow to move
    with "h,j,k,l,g,G" keys.
-   [Glances](https://nicolargo.github.io/glances/)
    glances is a python ncurses program that replace and improve _top_ and _htop_. It
    can also work in client/server mode for remote monitoring, and also provide a Web
    interface. _Glances_ is in Debian.

    -   [GitHub - Glances](https://github.com/nicolargo/glances)
    -   [Glances documentation](https://glances.readthedocs.io/)
    -   [Tecmint Glances tutorial
        ](https://www.tecmint.com/glances-an-advanced-real-time-system-monitoring-tool-for-linux/)
-   [gotop](https://github.com/xxxserxxx/gotop) (MIT License)
    A Golang terminal based graphical activity monitor.

    A deb package is provided in the releases.
-   [htop](http://htop.dev) (GPL-2)
    ncurses-based process viewer.  It is similar to top, but allows to scroll the
    list vertically and horizontally to see all processes and their full command
    lines.  Tasks related to processes (killing, renicing) can be done with
    keyboards shortcuts.

    See the {<< man "htop" "manual page" >}} or the help menu (F1 or h inside htop)
    for a list of supported key commands.

    -   [htop - Github](https://github.com/htop-dev/htop/).
Many other alternatives are available, an incomplete list is inactive
[Alternatives - Gotop](https://github.com/xxxserxxx/gotop#alternatives).


## Misc Command line system monitoring tools
### Processes
-   {{< man "ps(1)"  >}} displays information about the active processes.
-   {{< man "fuser(1)"  >}} identify processes using files or sockets
-   {{< man "lsof(8)"  >}}  output file information about files opened by processes
    {{< man "lsof#lbAW" "examples at the end of lsof(8)" >}}
    and the QUICKSTART  and FAQ
-   {{< man "iostat" >}} - Report CPU statistics and input/output statistics for devices
    and partitions.

### I/O
-   {{< man "iotop" >}} - simple top-like I/O monitor.


### Performance

-   {{< man "dstat" >}} - monitor memory, process, network or disk space performance, it
    is a  replacement of ifstat, iostat, dmstat.
-   {{< man "free" >}} - Display amount of free and used memory in the system.
-   {{< man "nmon(1)" >}} - Display performance information of the system: CPU, memory,
    network, disks (mini graphs or numbers), file systems, NFS, top processes, Linux
    version & processors.
-   {{< man "slabtop(1)" >}} - Display kernel slab cache information in real time .



# Network Monitoring Tools {#network_monitoring}
I put here tools that are specifically aimed to network monitoring,
the tools that monitor both system and network are in the section
{{< iref "#system_monitoring" "System monitoring" >}}
while command line tools are in
{{< iref "#monitoring_tools" "Monitoring Tools" >}}.

Basic network monitoring tools like _netstat_, _ss_, _nmap_, _iptraf_,
_tracepath_, _traceroute_, _mtr_ , _nethogs_ are in the section
{{< iref "nettools#ip_tools" "IP Tools" >}}.

See also the section {{< iref "nettools#traffic_shaping" "Traffic shaping" >}}

-   [NetworkMonitoring - Debian Wiki](https://wiki.debian.org/NetworkMonitoring)
    is a list of Servers Monitoring Softwares Implementation Guides and Tutorials.

-   [bmon](https://github.com/tgraf/bmon/) (MIT License)
    is a command line bandwidth monitor and rate estimator. It supports an interactive
    curses interface, lightweight HTML output but also simple ASCII output.

    It is packaged in Debian.
-   [Cacti]( http://www.cacti.net/) (GPL)
    is a network graphing solution using
    [RRDTool's]( http://oss.oetiker.ch/rrdtool/), it is in Debian.
-   [cbm](https://github.com/resurrecting-open-source-projects/cbm) (GPL-2.0)
    Color Bandwidth Meter (CBM) - display in real time the network traffic speed.
-   [Darkstat](http://unix4lyfe.org/darkstat/) (GPL)
    captures network traffic, calculates statistics about usage,
    and serves reports over HTTP. Darkstat is in Debian.
-   <a name="flowgrind"></a>[flowgrind](https://flowgrind.github.io/) (GPL-3.0)
    is a TCP traffic generator for testing and benchmarking.
    Compared to similar tools like {{< iref "#iperf" "iperf" >}} or
    {{< iref "#netperf" "netperf" >}} it features a distributed architecture.
    It is packaged in debian.
-   [iftop]( http://www.ex-parrot.com/pdw/iftop/) (GPL)
    is a ncurses tool that listens to network traffic on a named
    interface and displays a table of current bandwidth usage by
    pairs of hosts. Ifttop is in Debian.
-   <a name="iperf"></a>[iperf2](https://sourceforge.net/projects/iperf2/)
    Measure TCP and UDP bandwidth performance,
    allowing the tuning of various parameters and characteristics.
    It is a software [distinct from iperf3
    ](https://iperf2.sourceforge.io/IperfCompare.html).

    Iperf is similar with {{< iref "#netperf" "netperf" >}},
    and {{< iref "#flowgrind" "Flowgrind" >}}, but this last tool has a ditributed
    architecture.
    -   [iperf3 - GitHub](https://github.com/esnet/iperf).
    In Debian *iperf2* is packaged as iperf, an iperf3 package is also available.
-   <a name="mtrg"></a>[MRTG](http://oss.oetiker.ch/mrtg/) (GPL)
    _The Multi Router Traffic Grapher_
    is a perl tool to monitor the network traffic load.  MRTG
    generates HTML pages which provide a live visual representation of
    this traffic.
    -    {{< wp "Mrtg"  "Wikipedia: Mrtg" >}}
-   <a name="netdata"></a>[netdata
    ](https://github.com/firehol/netdata) (GPL)
    is a distributed real-time performance and health monitoring tool.
    It collects data in realtime (per second), and produce a real-time
    interactive web representation of them.
    Netdata is part of the {{< iref "firewall#firehol" "FireHol project" >}}
    and is in Debian.
-   <a name="netperf"></a>[netperf](http://www.netperf.org/netperf/)
    is a benchmark that can be used to measure the performance of many different types
    of networking. It provides tests for both unidirecitonal throughput, and end-to-end
    latency.  It is in Debian section _non-free_.

    A distributed alternative to *netperf* is {{< iref "#flowgrind" "Flowgrind" >}}.
-   [ntop](http://www.ntop.org/products/ntop/)
    is a network traffic probe that shows the network usage.
    Ntop can use a web interface. Ntop is in Debian.
-   {{< wp "Snmp"  "SNMP - Simple Network Management Protocol" >}}
    SNMP is a set of standards from IETF used to monitor network-attached devices.
    -   [Linux Home Networking](http://www.linuxhomenetworking.com/wiki/index.php/
        in the
        [Chapter 22 Monitoring Server Performance
        ](http://www.linuxhomenetworking.com/wiki/index.php/Quick_HOWTO_:_Ch22_:_Monitoring_Server_Performance)
        deal with SNMP and with {{< iref "#mtrg" "MTRG" >}}.
    -   [Monitoring Performance with Net-SNMP :: Fedora Docs
        ](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/monitoring-and-automation/System_Monitoring_Tools/#sect-System_Monitoring_Tools-Net-SNMP)
-   [slurm](https://github.com/mattthias/slurm) command line network load monitor.
-   [VnStat](http://humdi.net/vnstat/) is a console-based network
    traffic monitor. It has graphing capabilities and in included in
    Debian as vnstat and vnstati.

# System monitoring tools {#system_monitoring}

Network or system monitoring systems and system management (or configuration) software
are related kinds of software, handsome system combine network and system monitoring.


In this page I focus on system and network monitoring,
the related _distributed configuration management_ is in the
{{< iref "configuration_management" "Configuration Management Software section" >}},
tools aimed at only network are in the
{{< iref "#network_monitoring" "Network Monitoring Tools section" >}},
while command line tools are in
{{< iref "#monitoring_tools" "Monitoring Tools" >}}.

-   Wikipedia:
    {{< wp "Category:Web server management software" >}},
    {{< wp "Network monitoring" >}},
    {{< wp "Network management system" >}},
    {{< wp "Comparison of network monitoring systems" >}},
    {{< wp "Web hosting control panel" >}},
    {{< wp "Comparison of web hosting control panels" >}},
    [Comparison of open-source configuration management software
    ](http://en.wikipedia.org/wiki/Comparison_of_open_source_configuration_management_software),
-   [softpanorama](http://www.softpanorama.org/):
    [System Monitoring](http://www.softpanorama.org/Admin/system_monitoring.shtml)

[Cockpit](https://cockpit-project.org/)
:   is an interactive server admin interface.

    Cockpit is the web administration interface of
    -   [Cockpit Guide](https://cockpit-project.org/guide/latest/)
    -   [Managing systems using the  web console - Red Hat Enterprise Linux
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/9/html/managing_systems_using_the_rhel_9_web_console/index)
        *Web Console is the name for Cockpit in RedHat entreprise.
    -   [Administering SUSE ALP Dolomite using Cockpit
        ](https://documentation.suse.com/alp/dolomite/html/cockpit-alp-dolomite/index.html)
{{< wp "Collectd" >}} (GPL)
:   is a UNIX-daemon which collects, transfers and stores performance data and provides
    mechanisms to store the values for example in {{< iref "#rrdtool" "RRDTool" >}}
    files.

{{< wp "Ganglia_(software)"  "Ganglia" >}} (BSD License)
:   is a scalable distributed system monitor tool for clusters and grids. It relies on a
    multicast protocol to monitor state within clusters

{{< wp "Icinga" >}}
:   Incinga (GPLv2) is a backward compatible fork of {{< iref "#nagios" "Nagios" >}}
    written like Nagios in C and Perl.  It adds to Nagios a modern Web2 based user
    interface, and additional database connectors.
     -   Icinga is available in Debian
     -   [Icinga Home](https://www.icinga.org/)

<a name="monit"></a>[monit](http://www.tildeslash.com/monit/) (GPL)
:   monit is a utility written in C that monitor files, directories and devices for
    changes. You can also monitor remote hosts. Monit can start/stop/restart a process
    depending of its state. It provides a built-in HTTP(S) interface.

    Monit is tiny on my _bananapi_ the basic footprint is 1.1M/0.7 shared.

    A monit package is available for {{< iref "openwrt" "OpenWrt" >}}.

    -   [howtoforge: Server monitoring with munin and monit on debian
        ](https://www.howtoforge.com/tutorial/server-monitoring-with-munin-and-monit-on-debian/2/)
    -   [Monit Manual](https://mmonit.com/monit/documentation/monit.html)
    -   [Monit Wiki](https://mmonit.com/wiki/)
        FAQ, How To, Suggestions, Configuration Examples

<a name="monitorix"></a>[Monitorix](http://www.monitorix.org/)
:   _Monitorix_ (GPL) is a lightweight system monitoring tool servers, as it has a small
    size, it can be used on embedded devices as well.<br /> It consists mainly of two
    programs: a Perl collector daemon and a CGI script.  _Monitorix_ includes its own
    HTTP server built in.
    -   [GitHub: monitorix](https://github.com/mikaku/Monitorix)

<a name="nagios"></a>{{< wp "Nagios" >}} (GPLv2)
:   is a computer system and network monitoring application software written in C. It
    can monitor network services as well as host resources.

    Nagios is available as Debian Package.
   -   [Nagios Home](http://www.nagios.org).
   -   [NConf](http://www.nconf.org/dokuwiki/doku.php) (GPL) is a PHP
       based web-tool for configuring the Nagios monitoring software.
   -   {{< wp "Opsview" >}} (GPL)  is a server and application monitoring tool
       written in Perl and C that uses Nagios as its monitoring 'engine'.
   -   See also {{< iref "#shinken" "Shinken" >}} a fork of Nagios

[OpenPanel](http://www.openpanel.com/) (GPL)
:   Provide full control over all technical processes through a web interface, and a
    command line client. It is developped on debian.

    It allows to manage ssl, network including apm, ipv6, apache2, webdav, ssh,
    bind9, mysql, iptables and apt software update.
    -   [Openpanel Documentation Wiki
        ](http://documentation.openpanel.com/index.php/Main_Page)

{{< wp "Pandora FMS" >}} (GPL)
:   Pandora Flexible Monitoring System watches your systems and applications, and allows
    you to know their status. Pandora is written in Perl and PHP and packages are
    offered for all main distributions, including Debian and Ubuntu.

<a name="rrdtool"></a>{{< wp "RRDTool" >}} (GPL)
:   RRDTool's is a data logging and graphing system for time series data.
    -   _RRDTool_ by itself it is not a System monitoring tool but is
        the heart of the graphing capabilities of many monitoring
        systems including cacti,  collectd, munin and
        [many others](http://oss.oetiker.ch/rrdtool/rrdworld/index.en.html).
    -   _RRDTool_ can be interfaced in shell scripts, perl, python,
        ruby, lua or tcl
    -   [RRDTool's Home]( http://oss.oetiker.ch/rrdtool/)

<a name="shinken"></a>{{< wp "Shinken" >}} (Affero General Public License) )
:   Shinken is a rewrite of the functionalities of
    {{< iref "#nagios" "Nagios" >}} in Python.
    -   [Shinken Home](http://www.shinken-monitoring.org/)
    -   [Shiken GitHub Repository](https://github.com/naparuba/shinken)
    -   Shinken is available in Debian, with multiple packages for the
        desired modules.

<a name="zabbix"></a>{{< wp "Zabbix" >}} (GPLv2)
:   Zabbix is a GPL software written in C with a PHP web interface
    to monitor and track the status of various network services on
    local or remote servers. it can use agents on hosts or monitor via
    snmp. It uses MySQL, PostgreSQL, SQLite or Oracle to store data.
    Zabbix is available on main linux distributions including
    {{< iref "openwrt" "OpenWrt" >}}.

    -   [Zabbix Home](http://www.zabbix.com/). It is
    -   [Zabbix documentation](http://www.zabbix.com/documentation.php)

# Benchmarks
## References
-   Wikipedia: {{< wp "Benchmark (computing)" >}},
    [w:Category:Computer benchmarks

## Filesystem I/O Benchmark
-   [blkreplay](https://github.com/schoebel/blkreplay/wiki) (GPL)
    is a C utility driving the block layer of the operating system while measuring
    latency and throughput of I/O operations for later visualisation. blkreplay can be
    used to test physical hardware, to compare different brands of hard disks or RAID
    controllers, to evaluate the effect of SSD caching, to compare different block level
    transports like iSCSI vs Fibrechannel and so on. It is in Debian.
-   [Bonnie++](https://www.coker.com.au/bonnie++/) (GPL)
    is a C toolkit for testing hard drive and file system performance.  The package
    comes with also the
    [Zcav](https://www.coker.com.au/bonnie++/zcav/) (GPL)
    tool to tests the performance of different zones of a hard drive. It avoid comparing
    the quicker tracks of a system to the slower ones of an other. Bonnie++ is in
    Debian.
-   [IOzone](http://iozone.org/) (Free but private License)
    is a filesystem benchmark tool written in C. The benchmark tests file I/O
    performance for the following operations: Read, write, re-read, re-write, read
    backwards, read strided, fread, fwrite, random read/write, pread/pwrite variants. It
    is in the Debian package iozone3.

## Network Benchmark

-   [Netperf](https://github.com/HewlettPackard/netperf) (Free
    opensource Hewlett packard License)
    is a benchmark written in C that can be used to measure the performance of many
    different types of networking. It provides tests for both unidirecitonal throughput,
    and end-to-end latency.  It is in Debian.
-   [NetPerfMeter](https://www.uni-due.de/~be0001/netperfmeter/) (GPL)
    is a network performance meter written in C for the UDP, TCP, SCTP and DCCP
    transport protocols over IPv4 and IPv6. It simultaneously transmits bidirectional
    flows to an endpoint and measures the resulting flow bandwidths and QoS. It is in
    Debian.
    -   [GitHub: Netperfmeter](https://github.com/dreibh/netperfmeter).
-   [netstress](https://sourceforge.net/projects/netstress/)
    (BSD License) Is a C client/server utility designed to stress & benchmark network
    activity of a given ethernet device or path using simulated (random) real world data
    and packet sizes instead of fixed data and packet sizes. It is in Debian.

## Stress Test Benchmark
-   [Phoronix Test Suite](http://www.phoronix-test-suite.com/) (GPL)
    is a cross platform test suite for Linux, BSD, Solaris, Mac OS X, and Windows
    systems. Phoronix site propose a Debian package.
    -   [GitHub - Phoronix-test-suite
        ](https://github.com/phoronix-test-suite/phoronix-test-suite/)
-   [Stress](http://people.seas.harvard.edu/~apw/stress/) (GPL)
    is a tool that imposes a configurable amount of CPU, memory, I/O, or disk stress on
    a POSIX-compliant operating system and reports any errors it detects. It is in
    Debian.
-   [Stress-ng](http://kernel.ubuntu.com/~cking/stress-ng/) (GRL)
    stress-ng is an improvement of _stress_ that will stress test a computer system in
    various selectable ways. It exercises various physical subsystems of a computer as
    well as the various operating system kernel interfaces. It is in Debian.

# Log Analyzers {#log_analyzers}
-   {{< wp "List_of_web_analytics_software#Free_.2F_Open_source_.28FLOSS.29"  "Wikipedia list of open source log analyzers" >}},
-   [Dmoz Log Analysis Freeware and Open Source
    ](https://www.dmoz.org/Computers/Software/Internet/Site_Management/Log_Analysis/Freeware_and_Open_Source/).
-   [Viewing and Managing Log Files :: Fedora Docs
    ](https://docs.fedoraproject.org/en-US/fedora/latest/system-administrators-guide/monitoring-and-automation/Viewing_and_Managing_Log_Files/)

[AWFFull](http://www.stedee.id.au/awffull/) (GPL)
:   AWFFull (A Webalizer Fork, Full o' features!) is a Web server
    log analysis program, forked from
    {{< iref "#webalizer" "Webalizer" >}}.
    It is written in C like webalizer, it adds a number of
    new features and improvements, _AWFFull_ is in Debian.

[AWStats](http://awstats.sourceforge.net/) (GPL)
:    is a log analyzer written in perl, that generates advanced web,
     streaming, ftp or mail server statistics, graphically.  it works
     as a CGI or from command line and is included in Debian and is
     said to give more detailed information and better graphical
     charts than webalizer, and to be easier to use.

[Folkert Vanheusden Linux software](http://www.vanheusden.com/Linux/)
:   Is a site that provide numerous open source tools mainly aimed
    at monitoring. Some present in [his gitHub repository
    ](https://github.com/flok99)
    among which is found
    [Multitail](http://www.vanheusden.com/multitail/)
    that creates multiple windows on your console with ncurses and lets
    you view multiple files like the original tail program.
    _Multitail_ is available in Debian.
    -   [Multitail Manual](https://www.vanheusden.com/multitail/manual.php)

[GoAccess](http://goaccess.io/)
:   is an open source real-time web log analyzer and interactive
    viewer that runs in a terminal in *nix systems.  GoAccess is being
    able to quickly analyze and view web server statistics in real
    time without having to generate an HTML report. Although it is
    possible to generate an HTML, JSON, CSV report.  You can see it
    more as a monitor command tool than anything else.

[Logq](http://www.logq.org/) (GPL)
:   _Logq_ by [Forest Bond](http://www.alittletooquiet.net/)
    is a flexible log analyzer written in python that parses log files
    into an SQLite database.  It allows fast querying that makes it
    possible to generate different reports from historical data
    without an excessive system stress.<br /> There is an input
    plugin for Apache traffic logs with arbitrary formatting; and
    outputs plugins for Raw/CSV, and bar graphs with ASCII,
    matplotlib or Google Charts.

[logwatch](http://sourceforge.net/projects/logwatch/)
:   Logwatch is a modular log analyser that runs every night and mails
    you the results. It can also be run from command line, most of the
    services commes preconfigured. Logwatch is written in perl and
    available in Debian.
    -   [ArchWiki: Logwatch
        ](https://wiki.archlinux.org/index.php/Logwatch).
    -   [DigitalOcean: How To Install and Use Logwatch Log Analyzer
        and Reporter on a VPS
        ](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-logwatch-log-analyzer-and-reporter-on-a-vps).

[swatch](http://sourceforge.net/projects/swatch/) (GPL)
:   The Simple Log Watcher is a perl log parser that uses Perl regular
    expressions for line matching. It is in Debian.

[Tenshi](http://dev.inversepath.com/trac/tenshi) (MIT style licence)
:   is a log monitoring program designed to watch a log file for lines
    matching user defined regular expressions and report on the
    matches. Tenshi is written in perl, and was initially a perl
    rewrite of [oak](http://www.ktools.org/oak) _written in C, no more developped_, it
    is in Debian.

{{< wp "Webalizer" >}}  (GPL) <a name=webalizer">
:   The Webalizer is a fast, free web server log file analysis
    program written in C wich produces reports in HTML.
    -   [Webalizer Home](http://www.mrunix.net/webalizer/)

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
