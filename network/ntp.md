---
title: Network Time Protocol
---

{{% toc /%}}

# References
-   Ntp is defined in
    [rfc 1305 Network Time Protocol (Version 3)
    ](https://tools.ietf.org/html/rfc1305),
    and
    [rfc 4330: Simple Network Time Protocol (SNTP) Version 4 for IPv4, IPv6 and OSI
    ](https://tools.ietf.org/html/rfc4330).
    both are updated as
    [RFC 5905 - Network Time Protocol Version 4
    ](https://tools.ietf.org/html/rfc5905)
-   [Network Time Synchronization Research Project
    ](http://www.eecis.udel.edu/~mills/ntp.html)
-
    .
-   [Wikipedia: NTP](http://en.wikipedia.org/wiki/Network_Time_Protocol)
    explains the basics of ntp, as does the tutorial by Mike Chirico
    [NTP, UTC, and Working with Time on Linux
    ](http://souptonuts.sourceforge.net/readme_working_with_time.html).
    We have of course to understand {{< wp "UTC" >}}, and look at the
    {{< wp "list of time zones by UTC offset" >}}.
-   [ArchWiki: Time](https://wiki.archlinux.org/index.php/Time)
-   [Red Hat Entreprise (7) System Administrator's Guide
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/)
    -   [Chapter 3: Configuring the Date and Time
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/chap-configuring_the_date_and_time)
        covers the commands `timedatectl`, `date` and `hwclock`,
    -   [Chapter 17: Using chrony
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/sect-Using_chrony).
    -   [Chapter 18: Configuring NTP Using ntpd
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/ch-configuring_ntp_using_ntpd).
    -   [18.17. Configure NTP
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/s1-configure_ntp)
        is a clear explanation of ntp configuration `ntp.conf`.
-   [Openntpd](http://www.openntpd.org/) (BSD license), is a
    lighter implementation of ntp protocol. Also described in the
    [Wikipedia: OpenNTPD](http://en.wikipedia.org/wiki/OpenNTPD).
-   [chrony](http://chrony.tuxfamily.org/)
    (GPL) is a pair of programs. `chronyd` is a daemon that adjusts
    the system time according to measurements it obtains from the
    network. `chronyc` is a command-line driven control and monitoring
    program.Chronyd implements the NTP protocol and can act as either
    a client or a server.
    -   [ArchWiki: chrony
        ](https://wiki.archlinux.org/index.php/Chrony)
    -   [Red Hat Entreprise System Administrator's Guide - Chapter 14:
        Configuring NTP Using the chrony Suite
        ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7-Beta/html/System_Administrators_Guide/ch-Configuring_NTP_Using_the_chrony_Suite.html)
    -   {{< man "chrony" >}}
-   [sntp](http://manpages.debian.org/cgi-bin/man.cgi?query=sntp)
    is the standard sntp query client.
-   {{< man "msntp" >}} (GPL) is a simple and portable SNTP client/server.
-   [Ntpclient](http://doolittle.icarus.com/ntpclient/)
    by Larry Doolittle, is a light client to ntpd servers, you can find
    on his page the downloads and a
    [README](http://doolittle.icarus.com/ntpclient/README)
    and
    [HOWTO](http://doolittle.icarus.com/ntpclient/HOWTO).
    <br/>The last release is from 2010.
-   [adjtimex
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=adjtimex)
    is an utility to manipulate the kernel time variables.
    it is packaged in Debian.
-   [ntpdate is now deprecated
    ](http://support.ntp.org/bin/view/Dev/DeprecatingNtpdate)
    we can replace it with

        $ ntpd -gqc /dev/null server1.name.net server2.name.org server3.name.com

    or with `sntp`:

        $ sntp -sS -c poolName
        # or
        $ sntp -sS hostname

## ntpd

-   [The NTP Public Services Project
    ](http://support.ntp.org/bin/view/Main/WebHome)
    contains references to ntp documentation and a NTP Time Server:
    [Public NTP Time Server Lists
    ](http://support.ntp.org/bin/view/Servers/WebHome)
-   [ntp.org home page](http://www.ntp.org/)
    contains the
    [ntp reference implementation
    ](http://www.eecis.udel.edu/~mills/ntp/html/index.html)
    from David Mills.
    [openbsd faq](http://www.openbsd.org/faq/faq6.html#OpenNTPD)
    describe it as being
    *a nontrivial program to set up, difficult code to audit, and
    with a large memory requirement* but my
    ntp daemon takes 1M of resident memory and it's not so bad!
-   [NTP Documentation
    ](http://www.eecis.udel.edu/~mills/ntp/html/index.html)
-   [NTP FAQ and HOWTO](http://www.ntp.org/ntpfaq/NTP-a-faq.htm)
-   [NTP Support Web
    ](https://support.ntp.org/bin/view/Support/)
    Community Supported Documentation for the reference
    implementation of NTP
    -   [Getting Started With NTP
        ](https://support.ntp.org/bin/view/Support/GettingStarted)
    -   [Configuration
        ](https://support.ntp.org/bin/view/Support/ConfiguringNTP)
        is the most usefull guide on ntp configuration.
    -   [ntpd access restrictions
        ](https://support.ntp.org/bin/view/Support/AccessRestrictions)
    -   [Troubleshooting NTP
        ](https://support.ntp.org/bin/view/Support/TroubleshootingNTP)
-   [ArchWiki: Network Time Protocol daemon
    ](https://wiki.archlinux.org/index.php/Network_Time_Protocol_daemon)
-   [Red Hat Entreprise System Administrator's Guide - Chapter 15.
    Configuring NTP Using ntpd
    ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7-Beta/html/System_Administrators_Guide/ch-Configuring_NTP_Using_ntpd.html)

### Ntpd manuals
This is the development manuals, to find current stable and older look
at [NTP Documentation Archive](http://doc.ntp.org/)

-   [ntpd manual
    ](http://www.eecis.udel.edu/~mills/ntp/html/ntpd.html)
-   [ntpq - standard NTP query program
    ](http://www.eecis.udel.edu/~mills/ntp/html/ntpq.html)
    -   [System variables
        ](https://www.eecis.udel.edu/~mills/ntp/html/ntpq.html#system)
    -   [Peer variables
        ](https://www.eecis.udel.edu/~mills/ntp/html/ntpq.html#peer)
-   [ntpdc manual- special NTP query program
    ](https://www.eecis.udel.edu/~mills/ntp/html/ntpdc.html)
-   [NTP Debugging Techniques
    ](https://www.eecis.udel.edu/~mills/ntp/html/debug.html)
    explains also simple verification of correct operations.
    The older [4.2.1: Debugging Techniques
    ](http://doc.ntp.org/4.1.2/debug.htm)
    contains examples that are non longer in the above version.

# Precision Time Protocol (PTP)
The Precision Time Protocol (PTP) is a protocol used to synchronize
clocks in a network. When used in conjunction with hardware support,
PTP is capable of sub-microsecond accuracy, which is far better than
is normally obtainable with NTP.

-   Wikipedia: {{< wp "Precision Time Protocol" >}}
-   [RedHat System administrator guide -
    Chapter 19. Configuring PTP Using ptp4l
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/ch-configuring_ptp_using_ptp4l).
-   [OpenSuse System Analysis and Tuning Guide -
    Chapter 18 Precision Time Protocol
    ](https://doc.opensuse.org/documentation/leap/tuning/html/book.sle.tuning/cha.tuning.ptp.html)
-   available also at:
    [Suse SLE -  System Analysis and Tuning Guide -
    Precision Time Protocol
    ](https://www.suse.com/documentation/sles-12/book_sle_tuning/data/tuning_ptp_ntp.html).
-   [linuxptp project](http://linuxptp.sourceforge.net/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
