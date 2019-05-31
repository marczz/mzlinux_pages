---
title: System Administration
---


# References
-   For basic concepts it is always usefull to refer to the bible i.e.
    [The gnu C library manual
    (chunked)](http://www.gnu.org/software/libc/manual/html_node/)
    or [(one page)
    ](http://www.gnu.org/software/libc/manual/html_mono/libc.html).
-   The [Red Hat 7 administrator's guide
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/system_administrators_guide/)
    has many useful chapters:
    -   [networking Guide
        ]( https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Networking_Guide/index.html)
        also in
        [Fedora 25: networking Guide
        ](https://docs.fedoraproject.org/en-US/Fedora/25/html/Networking_Guide/index.html)
    -   [Resource Management and Linux Containers Guide
        ](https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux/7-Beta/html/Resource_Management_and_Linux_Containers_Guide/index.html)
        deal with control groups, _cgroup_.
    -   [Kernel Crash Dump Guide
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Kernel_Crash_Dump_Guide/index.html)
        documents how to configure, test, and use the _kdump_ crash
        recovery service. It uses tools provided in debian as packages
        _kdump-tools_, _makedumpfile_, _crash-whitepaper_.
        (see also _kexec-tools_)
    -   [Performance Tuning Guide
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Performance_Tuning_Guide/index.html)
        describe Performance Monitoring Tools, Cpu, Memory, File Sytem,
        Networking tuning .
    -   [Storage Administration Guide
        ]( https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Storage_Administration_Guide/index.html)
    -   [LVM Administrator Guide
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Logical_Volume_Manager_Administration/index.html)
    -   [DM Multipath Configuration and Administration
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/DM_Multipath/index.html)
    -   [SELinux User's and Administrator's Guide
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/SELinux_Users_and_Administrators_Guide/index.html)
    -   [Security Guide
        ]( https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Security_Guide/index.html)
    -   Guides related to KVM virtualization.
    -   Guides to pacemaker clusters. Debian packages _pacemaker_,
        _pacemaker-cli-utils_, _pacemaker-mgmt_, _hartbeat_.
    -   [Linux Domain Identity, Authentication, and Policy Guide
        ]( https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/Linux_Domain_Identity_Authentication_and_Policy_Guide/index.html)
        ldap, kerberos, ntp, CA, Id
    -   [System-Level Authentication Guide
        ]( https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/System-Level_Authentication_Guide/index.html)
        using [FreeIpa](http://freeipa.org) _debian package
        freeipa-server_, _freeipa-admintools_ integrated solution to
        provide centrally managed Identity, Policy and Audit; ldap,
        NIS, Winbind, authentication, system passwords, Smart Cards,
        Fingerprints, [sssd](https://fedorahosted.org/sssd/) (System
        Security Services Daemon) debian package _ssd_, _sssd-tools_,
        _sssd-ad_, _sssd-ipa_, _sssd-krb5_,_sssd-ldap_, PAM, Kerberos,
        [certmonger](https://fedorahosted.org/certmonger/) debian
        package _certmonger_ D-Bus-based service which  simplify
        interaction with certifying authorities (CAs) on networks which
        use public-key infrastructure (PKI).
-   The new [Red Hat 8
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/]
    has also system administration documentation like
    -   [Managing Storage Devices
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_storage_devices/)
    -   [Managing Filesystems
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/managing_file_systems/).
    -   [Monitoring And Managing System Status And Performance
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/monitoring_and_managing_system_status_and_performance/)
-   [Fedora Documentation](http://docs.fedoraproject.org/en-US/index.html)
    -   [Fedora 30 -  System Administrator's Guide
        ](https://docs.fedoraproject.org/en-US/fedora/f30/system-administrators-guide/)
        locales, keyboard, date and time, Users and Groups, Services
        and Daemons, OpenSSH, [TigerVNC](http://tigervnc.org/)
        _available [here for Debian](http://vnc.devloop.org.uk/)_,
        apache, mail with postfix, procmail,  ldap, samba, ftp, cups,
        NTP Using chrony, NTP Using ntpd, PTP Using ptp4l,
        System Monitoring Tools (ps, top, free), Block Devices and
        File Systems (lsblk, blkid, partx, findmnt, df, du),
        Hardware Information (lspci, lsusb, lspcmia, lscpu),
        Net-SNMP, rsyslog, Cron (and Anacron, at, batch), oprofile
        _no longer in debian but
        [perf](https://perf.wiki.kernel.org/index.php/Main_Page) is in
        linux-base, and there are alternatives in [pixelbeat:profiling
        ](http://www.pixelbeat.org/programming/profiling/), boot
        loaders (grub, yaboot, os/400), Kernel Modules.
