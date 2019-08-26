---
title: Power Management
---

    _This page deal also with __cpu frequency__ but the hard drive power consumption is
on the  {{< iref "hdrive" "HardDrive page" >}}_

-   ArchWiki: [Power management](https://wiki.archlinux.org/index.php/Power_management),
-   [CPU frequency scaling](https://wiki.archlinux.org/index.php/CPU_frequency_scaling),
    [ACPI modules](https://wiki.archlinux.org/index.php/ACPI_modules),
    [acpid](https://wiki.archlinux.org/index.php/Acpid),
-   The [Gentoo Power Management Guide
    ](https://wiki.gentoo.org/wiki/Power_management/Guide)
-   Ubuntu wiki has a [power-management-in-Ubuntu
    ](https://wiki.ubuntu.com/power-management-in-Ubuntu) page _2008_,
    [Ubuntu wiki: Reduced Power Usage](https://wiki.ubuntu.com/ReducedPowerUsage)
    _2008_.
    explains how to fiddle the {{< iref "filesystems#sysctl" "/proc/sys/vm/" >}}
    parameters.
-   [Power Management Guide - Red Hat Enterprise Linux 7
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/power_management_guide/index)
    -   [3.2. CPUfreq
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/power_management_guide/cpufreq_governors)
-   [Monitoring and managing system status and performance - Red Hat Enterprise Linux 8
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/monitoring_and_managing_system_status_and_performance/index)
    -   [Chapter 1. Getting started with Tuned
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/monitoring_and_managing_system_status_and_performance/getting-started-with-tuned_monitoring-and-managing-system-status-and-performance)
        _tuned is also a Debian package_.
    -   [Chapter 5. Managing power consumption with PowerTOP
        ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/monitoring_and_managing_system_status_and_performance/managing-power-consumption-with-powertop_monitoring-and-managing-system-status-and-performance)
-   [How to reduce power consumption - ThinkWiki
    ](http://www.thinkwiki.org/wiki/How_to_reduce_power_consumption)
-   [How to use cpufrequtils - ThinkWiki
    ](http://www.thinkwiki.org/wiki/How_to_use_cpufrequtils)
-   [kernel Documentation - cpu-freq
    ](https://www.kernel.org/doc/Documentation/cpu-freq/index.txt),
    [cpu-freq governors](https://www.kernel.org/doc/Documentation/cpu-freq/governors.txt)
    [cpu-freq drivers](https://www.kernel.org/doc/Documentation/cpu-freq/cpu-drivers.txt),

-   _cpufrequtils_ is available as  Debian/Ubuntu package contains two utilities
    [cpufreq-info](http://www.kernel.org/pub/linux/utils/kernel/cpufreq/cpufreq-info.html)
    for inspecting and
    [cpufreq-set](http://www.kernel.org/pub/linux/utils/kernel/cpufreq/cpufreq-set.html)
    for setting the cpu frequency through both the sysfs and procfs CPUFreq kernel
    interfaces.
-   {{< man "cpufreqd"  >}} is a deamon to manage cpu frequencies.
    [cpufreqd - Gentoo Power management/Guide
    ](https://wiki.gentoo.org/wiki/Power_management/Guide#Using_cpufreqd)
-   {{< man "powertop" >}} shows power sucking
    processes in a screen, and gives related advice to reduce power
    consumption. It is mainly tunnings in /proc/sys/ keys that are documented in
    {{< iref "filesystems#sysctl" "/proc/sys filesystem" >}}.
-   [Powertop - ArchWiki](https://wiki.archlinux.org/index.php/Powertop)
-   [Powertop User Guide (pdf)
    ](https://01.org/sites/default/files/page/powertop_users_guide_201412.pdf)
    from the [Powertop Home](https://01.org/powertop/).
-   {{< man "cpupower" >}} allows inspection and control of cpufreq and cpuidle tunables
    for hardware that support these features. It replaces "cpufreq-info" and
    "cpufreq-set" in cpufrequtils.
    _linux-cpupower is a Debian package._



{{< iref "hdrive#laptop_mode" "laptop_mode" >}} is dealed with on the
{{< iref "hdrive" "Hard Drive page" >}}

## power suspend
-   {{< wp "Hibernation_(computing)"  "Hibernation" >}}
    is implemented in standard kernel tree
    by {{< wp "Swsusp" >}}
-   [kernel documentation- HOWTO Suspend and hibernation utilities - s2ram, s2disk,
    s2both
    ](https://git.kernel.org/pub/scm/linux/kernel/git/rafael/suspend-utils.git/tree/HOWTO?id=HEAD)
-   [Power management/Suspend and hibernate - ArchWiki
    ](https://wiki.archlinux.org/index.php/Power_management/Suspend_and_hibernate)
-   {{< man "uswsusp" >}}  is a set of user space tools used for hibernation
    (suspend-to-disk) and suspend (suspend-to-RAM or standby)
    _uswsusp is a Debian package._
    -   [uswsusp - ArchWiki](https://wiki.archlinux.org/index.php/Uswsusp)

    -   [uswsusp Home ](http://suspend.sourceforge.net/),
-   Open Suse Documentation
    -   [Suspend to RAM](http://en.opensuse.org/SDB:Suspend_to_RAM)
        by Stefan Seyfried.
    -   [Suspend to Disk](http://en.opensuse.org/SDB:Suspend_to_disk).
    -   [Pm-utils](http://en.opensuse.org/SDB:Pm-utils)
-   The kernel Tree has some documentation on the sysfs pm management in the
    [Power directory](http://www.mjmwired.net/kernel/Documentation/power),
    for more_:
    -   [System Power Management States (states.txt)
        ](http://www.mjmwired.net/kernel/Documentation/power/states.txt)
    -   [swsusp.txt](http://www.mjmwired.net/kernel/Documentation/power/swsusp.txt)
        a general information and FAQ about the kernel suspend (ram and disk).
    -   [How to get s2ram working (s2ram.txt)
        ](http://www.mjmwired.net/kernel/Documentation/power/s2ram.txt) and
        [Debugging hibernation and suspend (basic-pm-debugging.txt)
        ](http://www.mjmwired.net/kernel/Documentation/power/basic-pm-debugging.txt)
        for suspend and hibernate debugging.
    -   [Using swap files with software suspend
        ](http://www.mjmwired.net/kernel/Documentation/power/swsusp-and-swap-files.txt)
-   [Systemd](https://wiki.archlinux.org/index.php/Systemd#ACPI_power_management)
    handles ACPI power management without requiring pm-utils.
