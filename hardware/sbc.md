---
title: ARM Single Board Computers
---


# Arm Architectures
-   Wikipedia: {{< wp "ARM architecture" >}},
    {{< wp "List of single-board computers" >}},
    {{< wp "Comparison of single-board computers" >}},
    {{< wp "Open-source computing hardware" >}}
-   Wikipedia {{< wp "List of ARM microarchitectures" >}},
    {{< wp "ARM architecture" >}}

Recent arm architectures includes

-   ARMv5: provided by [wARM7EJ], {{< wp "ARM9E" >}}, {{< wp "ARM10E" >}}
    The  {{< wp "ARM9E" >}} was produced between  1998 to 2006 and widely used
    in older SBC like the Plug computers (sheevaplug, todido,
    guruplug, dreamplug ...)
-   ARMv6: provided by {{< wp "ARM11" >}} and some {{< wp "Cortex-M" >}}.
-   <a name="armv7"></a>ARMv7: provided by {{< wp "Cortex-M" >}}, {{< wp "Cortex-R" >}},
    and {{< wp "Cortex-A" >}} 5 to 17.
    -   Wikipedia: {{< wp "Comparison of ARMv7-A cores" >}}
    -   {{< wp "ARM_Cortex-A7" >}} is a popular processor launched in 2011, that has many
        system-on-chips (SoC) by {{< iref "Allwinner_Technology"  "Allwinner" >}}
        ([A20](https://en.wikipedia.org/wiki/Allwinner_A20, A31, A83T ,H3, H8),
        {{< wp "Broadcom" >}}, {{< wp "Freescale_Semiconductor"  "Freescale" >}},
        {{< wp "Marvell_Technology_Group"  "Marvell" >}}, Mediatek, Qualcomm,
        Samsung _list on {{< wp "ARM_Cortex-A7" "Wikipedia">}}.
     -  {{< wp "ARM Cortex-A9 MPCore" >}} is a 32-bit multicore processor
        providing up to 4 cores, each implementing the ARM v7 instruction set.
        {{< wp "Cortex-A9" >}} is provided by [Texas Instrument OMAP4
        ](https://en.wikipedia.org/wiki/Texas_Instruments_OMAP#OMAP4),
        [Nvidia Tegra 2 series
        ](https://en.wikipedia.org/wiki/Nvidia_Tegra#Tegra_2_series)
        and
        [Freescale i.MX6x series (Wikipedia)
        ](https://en.wikipedia.org/wiki/I.MX#i.MX6x_series),
        [Freescale i.MX6x Home Page
        ](https://www.freescale.com/webapp/sps/site/taxonomy.jsp?code=IMX6X_SERIES).
    -   <a name=armada38x"></a>[Marvell ARMADA 38X
        ](https://www.marvell.com/embedded-processors/armada/armada-38x)
        is a family of ARMv7 multicore Socs with DDR3/DDR3L/DDR4 Ram
        (including ECC), PCI-e2.0, 2 or 3 Gigabits internets, 1 OSB
        3.0, 1 to 4 SATA, and a TDP of 3W to 4W.
-   <a name="arm-v8"></a>ARMv8: provided by {{< wp "Cortex-A32" >}} _32 bits only_ and for
    32bits/64bits {{< wp "Cortex-A" >}} > 35 among which the most used in SBC
    is {{< wp "Cortex-A53" >}}, and Qualcom {{< wp "Snapdragon" >}}.
    -   ARMv8-A _2011_ also named ARMv8.0-A introduce 64 bits AArch64
        [Arm64](https://linux-sunxi.org/Arm64) architecture.
        ARMv8-A allows 32-bit applications to be executed in a 64-bit
        OS.
    -   Then it was improved in ARMv8.1-A _2014_, {{< wp "ARMv8.2-A" >}}_2016_
        supported by  {{< wp "Cortex-A55" >}} and {{< wp "Cortex-A75" >}} ,
        ARMv8.3-A _2016_.
    -   Wikipedia: {{< wp "Comparison of ARMv8-A cores" >}}
    -   <a name="cortex-a53"></a>{{< wp"Cortex-A53" >}} launched in 2012 is the
        successor of the Cortex-A7. It is the architecture of
        [Marvell’s ARMADA 3700](https://www.marvell.com/embedded-processors/armada-3700/)
        found in EspressoBin,
        Broadcom BCM2837B0  used in Raspberry B-3+ and
        [Actions SOC S700](https://www.actions-semi.com/en/productview.aspx?id=225)
        found in Cubieboard 7, and AllWinner
        [H64](https://linux-sunxi.org/H64),
        [H5](https://linux-sunxi.org/H5),
        [H6](https://linux-sunxi.org/H6),
        [A64](https://linux-sunxi.org/A64).
-       [ArchWiki - Armv8 Platforms
        ](https://archlinuxarm.org/platforms/armv8)

## Allwinner Technology {#allwinner_technology}

{{< wp "Allwinner_Technology"  "Allwinner" >}} is one of the more popular
manufacturer of arm SoC.

It produces the A1x serie of {{< wp "Cortex-A8" >}} ArmV7 SoC;
the A2x and A3x serie of {{< wp " Cortex-A7" >}} ArmV7 SoC; the A8x family
of  {{< wp " Cortex-A7" >}} and {{< wp "Cortex-A15" >}} ArmV7 SoC; The Hx family where
H2, H3, H8 are {{< wp " Cortex-A7" >}} ArmV7 SoCs and  AllWinner
[H64](https://linux-sunxi.org/H64), [H5](https://linux-sunxi.org/H5),
[H6](https://linux-sunxi.org/H6)are {{< iref "#cortex-A53" "Cortex-A53" >}} armV8-A Socs.

-   Wikipedia: {{< wp "Allwinner_Technology"  "Allwinner" >}}
-   [AllWinner - A series
    ](https://www.allwinnertech.com/index.php?c=product&a=index&pid=2)
-   [AllWinner - H series
    ](https://www.allwinnertech.com/index.php?c=product&a=index&pid=6)
-   [Installing Debian On Allwinner
   ](https://wiki.debian.org/InstallingDebianOn/Allwinner)
-   [AllWinner armv7 platform comparison - ArchLinux
    ](https://archlinuxarm.org/platforms/armv7/allwinner)
-   [linux-sunxi](https://linux-sunxi.org/Main_Page)
    is an open source software community dedicated to Allwinner SoC
    based devices.
    -   [Sunxi devices as NAS - linux-sunxi.org
        ](https://linux-sunxi.org/Sunxi_devices_as_NAS).
    -   [SATA - linux-sunxi.org](https://linux-sunxi.org/SATA) describes the sata interface
        available on Allwinner A10, A20 and R40 SoCs.It contains a performance tuning
        section, and it considers the support of port multipliers. A list of devices
        with SATA is also provided but not updated since 2019, the previous ArchLinux
        list may be also considered.

        A SATA speed comparison is in [this T. Kaiser armbian post
        ](https://forum.armbian.com/topic/1917-armbian-running-on-pine64-and-other-a64h5-devices/?do=findComment&comment=20316).
    -   [How to make a bootable sunxi SD-card - linux-sunxi.org
        ](https://github.com/linux-sunxi/u-boot-sunxi/wiki),
        this is also described on the following LeMaker resource.
-   LeMaker development documentation:
    -   [BananaPro/Pi:Building u-boot, script.bin and linux-kernel
        ](http://wiki.lemaker.org/BananaPro/Pi:Building_u-boot,_script.bin_and_linux-kernel)
         contains instructions to get a cross dev platform, build kernel and uboot
         and set the sdcard. It also link to sunxi.org documentation.
    -   [BananaPro/Pi:Making a bootable .img image file
        ](http://wiki.lemaker.org/BananaPro/Pi:Making_a_bootable_.img_image_file)
    -   [BananaPro/Pi:Setting up the bootable SD card
        ](http://wiki.lemaker.org/BananaPro/Pi:Setting_up_the_bootable_SD_card).
    -   [BananaPro/Pi:Setting up the Linux distribution root file system
        ](http://wiki.lemaker.org/BananaPro/Pi:Setting_up_the_Linux_distribution_root_file_system)
-   [Powering the boards and accessories - linux-sunxi.org
    ](https://linux-sunxi.org/Powering_the_boards_and_accessories)
    is a set of advices to avoid under-power failures which are common.
    -   [SATA drives](https://linux-sunxi.org/Powering_the_boards_and_accessories#SATA)
        can use up to 1-4W when spinning up and 0.5-2W when idle. SSD drives use a lot
        less power.

        SATA 3.5" drives typically require 12V DC instead of 5V, and need to be powered
        externally with a SATA-DC/SATA Y-shaped cable.
    -   The [soc power consumption
        ](https://linux-sunxi.org/Powering_the_boards_and_accessories#Power_consumption)
        is the sum of the board and electronics usually 1-2A when busy, each USB device
        may use from 100 to 500mA.
-   The linux-sunxi site has also instructions for building the kernel.
    [Linux Kernel - linux-sunxi.org](https://linux-sunxi.org/Linux#A20), and
    [Toolchain - linux-sunxi.org](https://linux-sunxi.org/Toolchain)
-   Banana dev - GitHub  allow to [Build Banana Pi Image
    ](https://github.com/bananapi-dev/BPi/blob/master/HowToBuild_BPi_image.en.txt)

## Allwinner Socs
-   {{< wp "Allwinner A1X" >}} can boot GNU/Linux distributions such as Debian,
    Ubuntu, Fedora, from an SD card, in addition to the Android OS
    installed on the flash memory.
-   [Allwinner A10 CPU](https://elinux.org/Allwinner_A1X)
    is an 1.5ghz ARM Cortex A8 with a MALI400 GPU,
    2160p Hardware-accelerated Video playback with  HDMI out up to
    1080p, USB 2.0 Host
    as well as a 2nd USB-OTG  Interface, 10/100
    Ethernet, SATA-II 3gb/sec., audio input and
    output, DDR3 512MB / 1GB, 4GB NAND storage,
    SDHC card slot supporting up to 32GB. <br />
    It run Linux or Android. It powers up
    [many tablets](https://elinux.org/A10_tablets) and
    [boards and minipc](https://elinux.org/A10_boards_and_minipc)
    on the Chinese market.
    The A10 can update the firmware from USB, so it can not be
    bricked, and it can be securely
    [hacked](https://elinux.org/Hack_A10_devices).
-   [Allwinner A20](https://elinux.org/Allwinner_A20)
    contains an {{< wp "Cortex-A7" >}} dual core, GPU – ARM Mali400 MP2, DDR3
    ram, 10/100 Ethernet, 4Gb Nand Flash, HDMI 1080p Output with
    3840×1080@30fps 3D decoding, 2 USB Host, 1 micro SD slot, 1 SATA,
    1 IR.

## Platform comparison.

-   [H2+/H3/H5 boards overview
    ](https://forum.armbian.com/topic/1351-h3-board-buyers-guide/?do=findComment&comment=44979).
    by [T Kaiser in armbian forum](https://forum.armbian.com/profile/7-tkaiser/).
-   [Raspberry vs Banana vs A10-OLinuXino : powering and SATA performance
    ](https://hardware-libre.fr/2014/06/raspberry-vs-banana-vs-a10-olinuxino-powering-and-sata-performance/).
-   [OpenBenchmarking.org](https://openbenchmarking.org/)  contains tests of many
    platforms and comparisons, including SBC. Search for your preferred product.

# Linux Arm support

-   [Debian ARM port](https://www.debian.org/ports/arm/):
    -   [Intel IOP support](https://www.cyrius.com/debian/iop/)
        like the Thecus NAS,
    -   [Marvell's Kirkwood Debian Support
        ](https://www.cyrius.com/debian/kirkwood/)
        like {{< wp "SheevaPlug" >}}, {{< wp "Guruplug" >}}, [D2Plug
        ](https://www.globalscaletechnologies.com/p-43-d2-plug.aspx)
    -   [Marvell's Orion Debian Support
        ](https://www.cyrius.com/debian/orion/) like
        {{< iref "#qnap" "Debian on QNAP" >}},
-   [Debian Cheap ServerBox Hardware](https://wiki.debian.org/CheapServerBoxHardware)
    is a list of arm small boxes that we can consider for open source
    project development.
-   [Ubuntu support ARM](https://wiki.ubuntu.com/ARM/),
    including [Ubuntu OMAP/OMAP4 support](https://wiki.ubuntu.com/ARM/OMAP).
    [Ubuntu ARM  device support](https://wiki.ubuntu.com/ARM/DeviceSupport).
-   [Arch Linux ARM](https://archlinuxarm.org/),
-   [Arm Platforms comparison](https://archlinuxarm.org/platforms).
-   [Bitkistl: Linux on ARM powered Devices](https://bitkistl.blogspot.fr/)
-   [elinux: RaspberryPi Comparison](https://elinux.org/RaspberryPi_Comparison)
    give a comparison of arm-linux development boards.
-   [Neil William](https://linux.codehelp.co.uk/) the previous leader
    of the project _Embedian_ has a
    [blog about ARMMP](https://linux.codehelp.co.uk/?s=armmp)
    Software are in [CodeHelp Github Repository](https://github.com/codehelp).
-   [ArmPorts - Debian Wiki](https://wiki.debian.org/ArmPorts)
    includes:
    -   Arm Port  using the obsolete ABI (OABI) for Arm v3 last released with 5.0
        (lenny).
    -   [ArmEabiPort](https://wiki.debian.org/ArmEabiPort) _arm-linux-gnu_ for ARM
        architecture versions 4T, 5T, and 6, but from Debian 10 (buster), 4T is no
        longer supported.  For this reason the support of Debian for orion processors
        like those found in Qnap TS-109, TS-209, TS-409 stopped at Debian buster.

        Arm 4T and 5T is tills supported in Debian.
    -   [armhf - Arm Hard Float](https://wiki.debian.org/ArmHardFloatPort)
        _arm-linux-gnueabi_ using the hard-float version of EABI, targeting Arm v7.
    -   [Arm64Port](https://wiki.debian.org/Arm64Port)
        for the 64-bit Armv8 architecture 64-bit arm64 also called AArch64.
-   [OmapPedia](https://www.omappedia.org/wiki/)
    reference the support across the miscellaneous distributions
    of the {{< wp "Omap" >}} arm processors developed by Texas Instruments

## Freedom Box
-   [FreedomBox - Debian Wiki](https://wiki.debian.org/FreedomBox)
    is a self-hosting server. It can be used as a private Cloud, a NAS, or a router.
-   The Freedom box supports
    [many applications](https://wiki.debian.org/FreedomBox/Features).
    Ths page list the role of FreedomBox applications, and their use case.
-   The are many FreedomBox
    [compatible Hardware](https://wiki.debian.org/FreedomBox/Hardware).
-   [FreedomBox Manual](https://wiki.debian.org/FreedomBox/Manual).
-   [FreedomBox Clients](https://wiki.debian.org/FreedomBox/Clients)
    list the Debian packages with clients for freedombox service.
-   [Install Freedombox in the Cloud](https://wiki.debian.org/FreedomBox/Cloud)
    gives an example with AWS.
-   [list of configuration of each service](https://wiki.debian.org/FreedomBox/Backups).
-   [FreedomBox Forum](https://discuss.freedombox.org).
-   [Joseph Nuthalapati Wiki](https://njoseph.me/mediawiki/Main_Page) has
    [notes about using FreedomBox](https://njoseph.me/mediawiki/FreedomBox)

    -   In the [Tips and Trick](https://njoseph.me/mediawiki/FreedomBox/Tips_and_Tricks)
        you find [how to increase storage
        ](https://njoseph.me/mediawiki/FreedomBox/Tips_and_Tricks#Increase_Storage_with_Additional_Volumes)
    -   If you want not only to increase storage but replace the partition on sdcard by
        the partition on sate drive, rather than a _btrfs balance_ you can use a
        _btrfs replace stated in [this post
        ](https://discuss.freedombox.org/t/move-file-system-onto-another-drive/2150/14).

        ~~~ console
        $ sudo btrfs replace start -B /dev/mmcblk0p2 /dev/sda1 /
        $ sudo btrfs filesystem resize max /
        ~~~

## Armbian {#armbian}
[Armbian](https://www.armbian.com/)
by Igor Pečovnik is a lightweight Debian or Ubuntu based Linux distribution for arm
platforms.

It supports many platforms you can find the list [on the download section
](https://www.armbian.com/download/) and inthe [boards directory in GitHub
](https://github.com/armbian/build/tree/master/config/boards).
They are classified a _general purpose_, _iot_, _nas_, networking_, _desktop_
to facilitate the choice of a board.
<--! unfinished list
Banana Pi(M1, M2+, Pro, M64), ClearFog (base, pro), DevTerm A06, Espressobin,
Firefly RK3399, Helios4, JetHub (D1, H1), Jetson Nano, Khadas (edge, vim1, vim2,
vim3, vim4), La Frite, Le Potato, Nanopc T4, NanoPi (M4 v2, Neo/core, Neo2, neo2
black, neo plus 4, Duo, R1, R2s, R4s), Odroid (C2, C4, HC4, N2, N2, N2+, XU4,HCx),
Olimex (Lime 2, Lime A64), Orange Pi (Plus 2E, 3, 4, Lite, Lite2, One, One, Pc, PC2,
PC+, Prime, R1, R1+, Zero Zero +2H3, Zero2 Zero+) Pine H64 B, Pine64, Pinebook pro,
pcDuino2/3, Raxda zero ...
-->
-   [Armbian Documentation](https://docs.armbian.com/).
-   [Armbian Community Forums](https://forum.armbian.com/).
-   [Armbian on twitter](https://twitter.com/armbian)

#  Raspberry
{{< wp "Raspberry Pi" >}} is a single-board computer

-   version 1 had a  ArmV6 Broadcom BCM2835 ARM11 700Mhz cpu,
    512 Mb ram, SD Card Slot, USB 2.0, RCA video, HDMI socket,
    10/100 BaseT Ethernet socket
    power consumption of 3.5 W and a price of 45€.
-   version 2 uses a ArmV7 Broadcom BCM2836 SoC with a 900 MHz 32-bit
    quad-core ARM {{< wp "Cortex-A7" >}} processor, 1Gb RAM
-   version 3 uses a ArmV8-A Broadcom BCM2837 SoC with a 1.2 GHz
    64-bit quad-core ARMv8-A {{< iref "#cortex-A53" "Cortex-A53" >}} processor, 1Gb RAM
-   The B-3+ launched in march 2018 has a Broadcom BCM2837B0 SoC with
    1.4 GHz 64-bit quad-core ARMv8-A {{< iref "#cortex-A53" "Cortex-A53" >}}, 1Gb RAM,
    4xUSB-2.0, HDMI, analog audio I/O, MicroSDHC, 10/100/1000 Mbit/s
    Ethernet (real speed ~300 Mbit/s), 802.11ac dual band 2.4/5 GHz
    wireless, Bluetooth 4.2, 17× GPIO, power from 2.3W idle to 5.7w

## Refs
-   [raspberrypi.org](https://www.raspberrypi.org/).
-   [The Pi Hut](https://thepihut.com/) sells Raspberry and accessories.
-   [MagPi](https://www.themagpi.com/) is a magazine for Raspberry Pi
    users.
-   [The Embedded Linux Wiki (elinux.org)](https://elinux.org/Main_Page)
    host the Raspberry Pi wiki
    [RPi Hub](https://elinux.org/R-Pi_Hub).
    You find there
    [Tutorials](https://elinux.org/RPi_Tutorials),
    [liste of Guides](https://elinux.org/RPi_Guides),
    [RPi Troubleshooting](https://elinux.org/R-Pi_Troubleshooting),
    [Hardware specification](https://elinux.org/RPi_Hardware),
    [Expansion Boards](https://elinux.org/RPi_Expansion_Boards),
    [Cases](https://elinux.org/RPi_Cases),
    [VerifiedPeripherals](https://elinux.org/RPi_VerifiedPeripherals),
    [RPiconfig](https://elinux.org/RPiconfig),
    [RPi Software](https://elinux.org/RPi_Software),
    [RPi Distributions](https://elinux.org/RPi_Distributions),
    [RPi Performance](https://elinux.org/RPi_Performance),
    [RPi Programming](https://elinux.org/Raspberry_Pi_Programming),
    [RPi VideoCore APIs](https://elinux.org/Raspberry_Pi_VideoCore_APIs),
    and many more subjects .....
-   [Debian: RaspBerry](https://wiki.debian.org/RaspberryPi)
    with a list of open source alternatives
-   [ArchWiki: Raspberry Pi](https://wiki.archlinux.org/index.php/Raspberry)
-   [raspberry-pi Questions - Stack Overflow
    ](https://stackoverflow.com/questions/tagged/raspberry-pi),
-   [RaspBerry Pi Stack Exchange](https://raspberrypi.stackexchange.com/)
-   [Raspbian](https://www.raspbian.org/) is a  Debian  variant optimized for
    the Raspberry Pi hardware. The [Raspbian FAQ](https://www.raspbian.org/RaspbianFAQ)
    and [Raspbian Documentation](https://www.raspbian.org/RaspbianDocumentation)
    give hints on package compiling.
-   <a name="omxplayer">[OMXPlayer](https://github.com/popcornmix/omxplayer/)
    is the command line OMX player for the Raspberry PI.

    Omxplayer is deprecated and should be replaced by vlc , his is due to: omxplayer
    uses openvg for OSD and subtitles which isn't supported on Pi4. omxplayer uses
    openmax which has been deprecated for a long time and isn't supported with 64-bit
    kernels. omxplayer does not support software decode omxplayer does not support
    advanced subtitles omxplayer does not support playback from ISO files. omxplayer
    does not integrate with the X desktop.

    Don't miss the keyboard shortcut listed on this page, ore in the
    [Github repository](https://github.com/popcornmix/omxplayer).

    There is no manual, and the command line options are in the usage string (from -h or
    missing arguments), but the keybindings are missing from the distribution.
    -   [GitHub - OMXPlayer](https://github.com/popcornmix/omxplayer).
    -   [OMXPlayer - Raspbian
        ](https://www.raspberrypi.org/documentation/raspbian/applications/omxplayer.md)
-   [Gentoo Wiki: Raspberry Pi Cross building
    ](https://wiki.gentoo.org/wiki/Raspberry_Pi_Cross_building)
-   There are many expansion boards for Raspberries most are listed
    in [RPIHub: Expansion Boards
    ](https://elinux.org/RPi_Expansion_Boards),
    you find also some sata expansion cards (by
    [SupTronics
    ](https://www.suptronics.com/Xseries.html),
    or [WDLabs
    ](https://wdlabs.wd.com/products/sata-adapter-board/))
    but they use an usb to sata bridge, so you cannot expect better
    performances than the usb provide.
-   [Ducky Pond Raspberry-pi tutorials
    ](https://www.ducky-pond.com/tag/raspberry-pi.html)
-   [HiFiBerry DAC/Digi/Amp products](https://www.hifiberry.com/) allow to build
    an high-quality and affordable audio distribution systems, based on RaspBerry.
    -   [DLNA/UPnP Server + Renderer – HiFiBerry
        ](https://support.hifiberry.com/hc/en-us/community/posts/115000045625-DLNA-UPnP-Server-Renderer/.

## Kodi on RaspBerry

{{< iref "media_players#kodi" "Kodi" >}}
[run on Raspberry](https://kodi.wiki/index.php?title=Raspberry_Pi)
either with a choice of specific distributions, like the minimal
[Xbian](https://wiki.xbmc.org/index.php?title=XBian),[osmc](https://osmc.tv/),
or on a modern Raspbian or following the
[Raspbian build recipe](https://www.raspbian.org/RaspbianXBMC).

-   [HOW-TO:Install Kodi on Raspberry Pi - Kodi Wiki
    ](https://kodi.wiki/view/HOW-TO:Install_Kodi_on_Raspberry_Pi),
    [On Raspbian](https://kodi.wiki/view/HOW-TO:Install_Kodi_on_Raspberry_Pi#Raspbian)
-   [Raspberry Pi FAQ - Kodi Wiki](https://kodi.wiki/view/Raspberry_Pi_FAQ)

# Banana Pi
All the development and tecnical documentation is above in the
{{< iref "#allwinner_technology" "AllWinner Section" >}}.

## Documentation
-   [Banana Pi - Wikipedia](https://en.wikipedia.org/wiki/Banana_Pi)
-   [LeMaker Banana Pi - linux-sunxi.org](https://linux-sunxi.org/LeMaker_Banana_Pi)
    gives the differences between [bananapi variants
    ](https://linux-sunxi.org/LeMaker_Banana_Pi#Variants).
-   [Banana Pi gitbook](https://www.gitbook.com/book/bananapi/).
-   [LeMaker](http://www.lemaker.org/):
    -   [Banana Pi Home Page](http://www.lemaker.org/product-bananapi-index.html).
    -   [Banana Pi Wiki - lemaker.org](https://wiki.lemaker.org/Main_Page),
    -   [LeMaker Banana Pro/Pi](http://wiki.lemaker.org/LeMaker_Banana_Pro/Pi)
        includes an extensive [Documentation
        ](http://wiki.lemaker.org/LeMaker_Banana_Pro/Pi#Documentation).
    -   [FAQ](https://wiki.lemaker.org/FAQ),
    -   [GitHub: LeMaker resources](https://github.com/LeMaker).
-   [bananapi.org - Banana Pi](https://www.bananapi.org/): site officiel (?) du Banana Pi
    [Banana Pi specifications and layout diagrams
    ](https://www.bananapi.org/p/product.html),
-   [BananaPi - Google Groups
    ](https://groups.google.com/forum/#!forum/bananapien)
-   [Banana Pi - ArchWiki](https://wiki.archlinux.org/index.php/Banana_Pi)

## Bananapi Models
-   [Bananapi M1](https://wiki.banana-pi.org/Banana_Pi_BPI-M1)
    launched in 2014 has an ArmV7 {{< wp "Allwinner A20" >}} {{< wp "ARM Cortex-A7" >}}
    Dual-Core 1GB DDR3, 10/100/1000 Ethernet, HDMI, CVBS, LVDS/RGB Video output, 3.5mm
    jack and HDMI Audio output, SATA 2.0, 2 x USB 2.0 ports, the same GPIO headers as
    the Raspberry Pi 1 Model A & B.

    Note That the allwinner A20 was a nice improvement over the first single-core
    Raspberry Pis few years ago but is pretty slow by today’s standards. The native SATA
    was very slow until Kernel 5.3 but it improved from 35MB/s to 100MB/s with a [patch
    ](https://www.phoronix.com/news/Faster-Allwinner-SATA-Patch) see also the
    [discussion on ArmBian Forum
    ](https://forum.armbian.com/topic/10352-a20-sata-write-speed-improvement/).
    The gigabit is not fully capable of 940 Mbits/sec in both
    directions.  Armbian suggested to replace it with better alternatives like
    the H3 socs listed in [This T. Kaiser post
    ](https://forum.armbian.com/topic/1351-h3-board-buyers-guide/?tab=comments#comment-28169)
    but it may be obsoleted by the new software.
-   [Banana Pro](https://linux-sunxi.org/LeMaker_Banana_Pro) launched in 2014 uses the
    same A20 soc than Bananapi M1. It's an updated version of M1, using a microSD slot,
    onboard WiFi (AP6181) and a 40 pin GPIO header.
    -   [FreedomBox BananaPro](https://wiki.debian.org/FreedomBox/Hardware/BananaPro)
        we can suppose that it applies also to Bananapi M1, as wifi is unused, even if
        we cannot use the microSD.
-   Bananapi M2 improve CPU with an Allwinner A31S {{< wp "ARM Cortex-A7" >}}
    Quad-Core 1GHz, 4 x USB 2, but drop SATA.
-   Bananapi M2+ CPU is H3 Quad-core {{< wp "ARM Cortex-A7" >}} Quad-Core, one
    USB 2.0 HOST, NO SATA, Wifi,
-   [Bananapi M2 Ultra
    ](https://www.gitbook.com/book/bananapi/bpi-m2-ultra-open-source-single-board-computer/details)
    _November 2016_ has an
    [Allwinner R40](https://en.wikipedia.org/wiki/Allwinner_Technology#R-Series)
    {{< wp "ARM Cortex-A7" >}} Quad-Core 2GHz, 2GB DDR3 SDRAM, 8G eMMC flash on
    board, bluetooth 4.0 and SATA interface. The Allwinner R40’s
    advantage over the H3 and A31 is the addition of eMMC flash and
    native SATA support.
    -   [Banana Pi M2 Ultra Allwinner R40  with SATA & GbE - CNX Software
        ](https://www.cnx-software.com/2016/11/16/banana-pi-m2-ultra-allwinner-r40-development-board-with-sata-gbe-sells-for-46/).
-   [Banana PI BPI-M2 Berry
    ](https://www.gitbook.com/book/bananapi/bpi-m2-ultra-open-source-single-board-computer/details)
    has the same [Allwinner R40
    ](https://en.wikipedia.org/wiki/Allwinner_Technology#R-Series)
    {{< wp "ARM Cortex-A7" >}} Quad-Core 2GHz, 2GB DDR3 SDRAM, bluetooth 4.0 and SATA interface.
    WIFI+BT on board.  The main difference with M2 Ultra is the
    absence of eMMC and the support of Wifi onboard. Ultra has also a
    Built-in 3.7V Lithium Battery Charging Circuit, which is absent on
    Berry.

    Both models have the same size than raspberry and can use the same
    boxes, the 40 pin GPIO header is pin-compatible with Raspberry Pi.
-   Banana Pi M3 _2015_ is an octa-core version of Banana Pi, it
    supports onboard Wi-Fi and SATA Port, but SATA is via an
    innefficient USB to SATA bridge.
-   [Bananapi-M5](https://wiki.banana-pi.org/Banana_Pi_BPI-M5)
    is powered by Amlogic S905X3 quad-core armV8 Cortex-A55 (2.0 XXGHz) processor.Onboard 4GB
    LPDDR4 memory and 16GB EMMC storage, and supports 4 USB 3.0 interface, a gigabit
    network port.

    It is very close to Banana Pi BPI-M2 Pro and Odroid C4 since these platforms uses the
    same  Amlogic S905X3 soc. A comparison is given in the banana-pi.org, on this page
    you find the system support which includes Debian, and numerous Linux distributions.
    in the [Bananapi-M5](https://wiki.banana-pi.org/Banana_Pi_BPI-M5) page.

    T. Kaiser indicates [in armbian forum
    ](https://forum.armbian.com/topic/15228-banana-pi-bpi-m5-with-amlogic-s905x3-chip-design/#comment-109756)
    that Odroid C4 is to be preferred, because banana-pi power circuitry suffer from
    the usual Banana undervoltage.

    In 2022 it is priced 92€ at reichelt store. _10% more than Odroid C4_.


## Banana Pi development

## Vente du Banana Pi

-   [banana-pi.com](https://www.banana-pi.com/)
    a la [liste des revendeurs](https://www.banana-pi.com/egsjj.asp?id=12)
-   [lextronic.fr](https://www.lextronic.fr/), principallement raspberry et
    alternatives mais a le  Banana Pi et nombreux modèles de modules.
-   [BananaPi.fr (vente)](https://e.banana-pi.fr/) et
    [BananaPiFr | Facebook](https://www.facebook.com/BananaPiFrance?ref%3Dhl)
    _Site assez cher avec peu d'accessoires, mais livraison bon marché._
-   [reichelt.de - Banana PI](https://www.reichelt.de/)
    un des meilleurs sites européens, a le BananaPi, RaspberryPi et
    beaucoup de materiels.
-   [Amazon.fr : banana-pi](https://www.amazon.fr/s?k=bananapi)
-   [New It : Banana Pi](https://www.newit.co.uk/shop/All-Banana-Pi)
-   China banana PI, orange Pi, Suppliers  Aliexpress.com
    [banana Pi](https://www.aliexpress.com/wholesale?SearchText=banana+pi).

# ESPRESSObin

Specifications:

-   [Marvell’s ARMADA 3700](https://www.marvell.com/embedded-processors/armada-3700/)
    {{< iref "#cortex-A53" "Cortex-A53" >}} dual-core  up to 1.2 GHz.
-   1x [Topaz Networking Switch](https://wiki.espressobin.net/tiki-index.php?page=Topaz+Switch)
    _The Marvell® Link Street®-88E6341 device is single-chip, 6-Port
    Ethernet Switch with four integrated 10/100/1000Mbps Ethernet
    transceivers and one high speed SerDes interfaces supporting
    2500-BaseX, 1000Base-X, and SGMII. The device also includes an
    integrated 200MHz microprocessor with 60Kbytes of internal memory to
    enable smart or lightly managed switches without the need of an
    external CPU. On ESPRESSObin we find 1 2.5G and two 10/100/1000Mbps._
-   1x uSD card slot with footprint for an optional 4GB EMMC
-   1GB DDR3 & 2GB DDR3 options
-   2x Gb Ethernet LAN
-   1x Ethernet WAN
-   1x SATA interface for HDD storage
-   1x USB 3.0 and 1x USB 2.0, 1 1x micro USB port
-   1x MiniPCIe for Wireless/BLE peripherals
-   2x Row of 46-pin GPIO headers for accessories and shields
    with I2C, GPIOs, PWM, UART, SPI, MMC, etc.
-   Reset button, JTAG interface
-   Power supply 12V DC jack or 5V via micro USB port
-   Power consumption: less than 1W thermal dissipation at 1 GHz

-   [ESPRESSObin Wiki](https://wiki.espressobin.net/).
-   [I/O ports and connectors
    ](https://wiki.espressobin.net/tiki-index.php?page=Quick+User+Guide#I_O_ports_and_connectors),
    and [hardware brief outline
    ](https://espressobin.net/espressobin-hardware-brief-outline/)
-   [ESPRESSObin Quick User Guide
    ](https://wiki.espressobin.net/tiki-index.php?page=Quick+User+Guide).
-   [Software How To
    ](https://wiki.espressobin.net/tiki-index.php?page=Software+HowTo)
    many pages on building and bootin a kernel image and how to
    [update the bootloader
    ](https://wiki.espressobin.net/tiki-index.php?page=Update+the+Bootloader)
-   [Getting Started Tutorials
    ](https://wiki.espressobin.net/tiki-index.php?page=Getting+Started+Tutorials)
-   [Running OpenSSL speed test on ESPRESSObin
    ](https://wiki.espressobin.net/tiki-index.php?page=Running+OpenSSL+speed+test+on+ESPRESSObin).


The ESPRESSObin is unbrickable you can always do
[boot ESPRESSObin from SATA drive
](https://wiki.espressobin.net/tiki-index.php?page=Boot+ESPRESSObin+from+SATA+drive)


-   [Marvell ESPRESSObin Forum](https://espressobin.net/forums/)
-   [Debian Wiki - Installing debian on Marvell ESPRESSOBin
    ](https://wiki.debian.org/InstallingDebianOn/Marvell/ESPRESSOBin)


-   {{< iref "#armbian" "ArmBian" >}} supports the espressobin,
    -   [armbian - Espressobin](https://www.armbian.com/espressobin/)
    -   [Espressobin support development efforts
        ](https://forum.armbian.com/topic/4089-espressobin-support-development-efforts/)
    -   [ESPRESSObin Forum](https://espressobin.net/forums/) :
        [Armbian Ubuntu / Debian
        ](https://espressobin.net/forums/topic/armbian-ubuntu-debian/),
    -   [Real Time preemptible kernels
        ](https://wiki.linuxfoundation.org/realtime/documentation/technical_details/start)
        are available in armbian and support ESPRESSObin
        [
        https://forum.armbian.com/topic/5576-fully-preemptible-kernels/
-   [ESPRESSObin | Arch Linux ARM
    ](https://archlinuxarm.org/platforms/armv8/marvell/espressobin)
-   [ESPRESSOBin - Gentoo Wiki
    ](https://wiki.gentoo.org/wiki/ESPRESSOBin#What.27s_Required)

## Hardware
-   [Howto: set up your ESPRESSObin as a home router
    ](https://indietech.rocks/howto/espressobin-home-router.html)
-   [My EspressoBIN board is up
    ](https://upon2020.com/blog/2017/05/my-espressobin-board-is-up/)
-   [Molex to SATA power adapter - Marvell ESPRESSObin
    ](https://espressobin.net/forums/topic/molex-to-sata-power-adapter/)

## Resellers
-   [Amazon.com: ESPRESSObin
    ](https://www.amazon.com/ESPRESSObin-SBUD102-Single-Computer-Network/dp/B06Y3V2FBK)


# Helios4

[Helios4](https://kobol.io/helios4/) 200€

-   Helios4 Datasheet
    -   {{< iref "#armada38x" "Marvell Armada 388" >}} (88F6828), Dual-core ARMv7 32b
        Cortex A9 CPU clocked at 1.6 Ghz with Cryptographic and XOR DMA engines,
    -   Gigabit ethernet, 2 x USB 3.0, microSD (SDIO 3.0)
    -   2GB DDR3L ECC RAM,
    -   4× SATA 3.0 ports maximum 12 TB drive x 4,
    -   Boot Mode Selector  - SPI, SD Card, UART, SATA
    -   board 100mm x 100mm, Color Casing 182 mm x 107 mm x 210 mm,
        2× 70mm PWM ball bearing FAN,
-   [Kobol Wiki](https://wiki.kobol.io/)
-   [Kobol Blog](https://blog.kobol.io/)
-   [Install - Helios4 Wiki](https://wiki.kobol.io/install/)
-   [Hardware - Helios4 Wiki](https://wiki.kobol.io/hardware/)
-   On  [Armbian forum](https://forum.armbian.com/)
    -   [Support of Helios4 - Intro - Armbian forum
        ](https://forum.armbian.com/topic/3045-support-of-helios4-intro/)
    -   [Helios4 Support](https://forum.armbian.com/topic/6033-helios4-support/)
    -   [Helios4 ECC - CPU freq info - air flow
        ](https://forum.armbian.com/topic/11536-helios4-ecc-cpu-freq-info-air-flow)
    -   [Helios4 disk benchmarks  - Armbian forum
        ](https://forum.armbian.com/topic/3045-support-of-helios4-intro/?page=2&tab=comments#comment-39582)

# Raxda
-   [Single Board Computers from Radxa](https://rockpi.org/)
-   [Rock Pi 4](https://rockpi.org/rockpi4)
    model C based on a Rockchip RK3399 processor that features two ARM Cortex-A72 cores
    and four ARM Cortex-A53 cores. This is supplemented by an ARM Mali-T864 GPU that
    supports modern APIs like OpenGL ES 3.2 and Vulkan 1.0. The Rock Pi 4 Model C also
    has 4 GB of RAM, a micro HDMI 2.0a port and a mini DP 1.2 port for high-resolution
    video output.

    It provides a NVMe port in a M2 socket factor. The socket supports 4-lane NVMe SSDs
    and is complemented by 4 MB of SPI flash for booting NVMe drives.
    The SBC requires an expansion board for connecting NVMe drives.

    It is compatible with existing Rock Pi 4 accessories.

    -   [Rock Pi 4 documentation](https://rockpi.eu/Rockpi4)
# Plug Computers
Wikipedia {{< wp "Plug computer" >}}.

The {{< wp "SheevaPlug" >}} is a plug computer with ARM-compatible CPU.
It features

-   a Marvell Kirkwood 6281 CPU (ARM-v5) at 1.2 GHz with 256 KB L2
    cache, 512 MB RAM, 512 MB flash U-boot, included Kernel, and File
    System,
-   1xSD
-   Gigabit Ethernet _no proprietary microcode_, 1x USB 2.0 Host, 1
    mini-USB with RS-232 COM port connector serial console and
    ARM-compliant JTAG connector
-   Dimensions 110 x 69.5 x 48.5 (mm), Power: 2.3w idle, 7.0w at 100%
    CPU (~ 5v 1000ma)
-   There is an eSata type II model

-   Martin Michlmayr [Debian support
    ](https://www.cyrius.com/debian/kirkwood/sheevaplug/) and
    [Plug Computer models and how well they are supported in Debian
    ](https://www.cyrius.com/debian/kirkwood/sheevaplug/plugs.html)
-   [Martin Michlmayr review of SheevaPlug
    ](https://www.cyrius.com/journal/debian/kirkwood/sheevaplug/nslu2-killer)
-   Distributed by [globalscaletechnologies.com
    ](https://www.globalscaletechnologies.com/p-26-sheevaplug-dev-kit-europe.aspx)
    and [NewIt](https://www.newit.co.uk/shop/All-SheevaPlug/) (~120€)
-   [ArchLinux Platforms](https://archlinuxarm.org/platforms)
    support some plug computers.

[Tonido Plug 2](https://www.tonidoplug.com/tonido_plug.html)
is a variant of SheevaPlug, with 512 MB of DDR3, 512 MB of Flash, USB
2.0, Gigabit Ethernet, WiFi, 2.5 inch SATA.
It runs Ubuntu to provide a nas and media streaming. It is discounted 59€
_2022_ at
[NewIT](https://www.newit.co.uk/shop/All-TonidoPlug/TonidoPlug2).

{{< wp "GuruPlug" >}} is the successor of Sheevaplug.  with 1.2 GHz ARM Marvell
Kirkwood 6281 (ARM9E i.e. ARM-v5), 512MB SDRAM, 512MB NAND, USB 2.0,
Gigabit Ethernet, JTAG, Bluetooth 2.1, Wi-Fi 802.11 b/g
It is [supported in Debian](https://www.cyrius.com/debian/kirkwood/sheevaplug/plugs/).

{{< wp "DreamPlug" >}} is the successor of GuruPlug. Its specifications are: 71.2 GHz ARM
Marvell Kirkwood 88F6281 SoC (ARM9 i.e. ARM-v5), 2MB Flash for uboot, 2
GB Flash, 512MB SDRAM, 1xMicro-SD system + 1SD Slot,2xUSB 2.0
Microphone in, Headphone out, 2xgibabits Ethernet,1xeSata, SP/DIF out,
WiFi /BT, Jtag and Uart. It costs 188€ /2022/
[at NewIt](https://www.newit.co.uk/shop/DreamPlug-Multi-Boot).
It is [supported in Debian](https://www.cyrius.com/debian/kirkwood/sheevaplug/plugs/).


#  BeagleBoard

[BeagleBoard](https://en.wikipedia.org/wiki/BeagleBoard) and BeagleBone
There is two _BeagleBones_
they both adhere to the same standard for expansion and interfacing.
[beagleboard.org](https://beagleboard.org/) is the Beagleboard Home
page where you can find technical and commercial information on
these boards.

The {{< wp "BeagleBoard" "Wikipedia BeagleBoard page" >}} gives the specification of the
different models of BeagleBoard and BeagleBone.

The BeagleBoards/BeagleBones don't have SATA support.

## Beagle Bone
-    BeagleBone had 720 MHz superscalar ARM Cortex-A8 AM3358/9, 256 MB DDR2 RAM, MicroSD
     slot, USB 2.0 host, USB mini OTG, Storage-over-USB or Ethernet-over-USB on other
     USB device port, Power consumption of 300-500mA at 5V.
-   [Embedded Linux Wiki (elinux): BeagleBoard ](https://elinux.org/BeagleBoard) is
    related to BeagleBoard and BeagleBoard-xM that both use
    {{< wp "Texas instrument OMAP" >}} Single-board computer (ARM architecture).
    A distinct SoC is used for the following _BeagleBone.
-   [Embedded Linux Wiki (elinux): BeagleBone](https://elinux.org/BeagleBone)
    gives a description of the two boards the original _BeagleBone_ and the new
    _BeagleBone Black_ .

    The _BeagleBone_ has support in Angstrom,
    [Debian](https://elinux.org/BeagleBoardDebian), Ubuntu,
    [ArchLinux](https://archlinuxarm.org/platforms/armv7/beaglebone),
    Gentoo, and more ...

## BeagleBone Black
-   [System Reference Manual · beagleboard/beaglebone-black Wiki · GitHub
    ](https://github.com/beagleboard/beaglebone-black/wiki/System-Reference-Manual)

-    BeagleBone Black in original version is a 1 GHz superscalar ARM Cortex-A8 AM3359,
     with 512 MB DDR3 RAM, 2 GB eMMC flash, MicroSD slot, USB 2.0 host, mini-USB 2.0
     client, HDMI output, power consumption of 210-460 mA at 5V. _no SATA_.
-   [Farnell - BeagleBone
    ](https://uk.farnell.com/seeed-studio/102110420/beaglebone-black/dp/3520081)
    42€ from UK.
-   [FreedomBox BeagleBone](https://wiki.debian.org/FreedomBox/Hardware/BeagleBone)

## BeagleBone Black C
-   The BeagleBone Black C revision C3 was delivered in August 2021, it is described
    in the [System Reference Manual
    ](https://github.com/beagleboard/beaglebone-black/wiki/System-Reference-Manual).
    It features a Sitara AM3358BZCZ100 1GHz, 2000 MIPS processor,
    SGX530 3D, 20M Polygons/S Graphics Engine, SDRAM Memory: 512MB DDR3L 606MHZ,
    4GB, 8bit Embedded MMC, Power Source: miniUSB USB or DC Jack, 5VDC External Via
    Expansion Header, miniUSB USB 2.0 Client Port, USB A 2.0 Host Port, Serial Port
    UART0, Ethernet 10/100, RJ45, SD/MMC Connector microSD,
    Video Out: 16b HDMI, 1280x1024 (MAX), Audio Via HDMI Interface, Stereo.
-   [Adafruit - BeagleBone Black C with preinstalled Debian
    ](https://www.adafruit.com/product/1996) 80$ with a starter pack 90$, and enclosure
    at 10$. They have
    [Distributors in many countries](https://www.adafruit.com/distributors/).
-   [digikey - BeagleBone Black C
    ](https://www.digikey.fr/fr/products/detail/ghi-electronics-llc/BBB01-SC-505/6210999).
    96€.
-   [BeagleBoneBlack - eLinux.org](https://www.elinux.org/Beagleboard:BeagleBoneBlack)

# CubieBoard
{{< wp "Cubieboard" >}} is a single-board computer manufacured by
[cubietech.com](https://www.cubietech.com/).

The processors goes from  AllWinner A10 {{< wp "Cortex-A8" >}} for cubieboard
1,  AllWinner A20 2x{{< wp "Cortex-A7" >}} for CubieBoard 2 and 3, Allwinner A80
4x Cortex-A15 and 4x{{< wp "Cortex-A7" >}} {{< wp "ARM big.LITTLE" >}} for CubieBoard 4,
Allwinner H8 8x{{< wp "Cortex-A7" >}} CubieBoard 5, Actions SOC S500
4x{{< wp "Cortex-A9" >}}

The {{< wp "Cubieboard"  "Cubieboard Wikipedia Page" >}} lists the specifications
of the models. A lot of the actual platforms are on sell on
[NewIt](https://www.newit.co.uk/shop/All_Cubieboard).

-   [CubieBoard.org](https://cubieboard.org/)
-   [Cubie Forums](https://www.cubieforums.com/)
-   [Debian CubieBoard Page](https://wiki.debian.org/CubieBoard)
-   [Cubian](https://cubian.org/),
    [GitHub Cubian](https://github.com/cubieplayer/Cubian) is a
    Debian distribution for CubieBoard 1 and 2 based on Debian wheezy.
    _Not updated since 2014_
-   [sunxi: Cubieboard wiki](https://linux-sunxi.org/Cubieboard)
-   ArchLinux: [Cubieboard
    ](https://archlinuxarm.org/platforms/armv7/allwinner/cubieboard),
    [Cubieboard 2
    ](https://archlinuxarm.org/platforms/armv7/allwinner/cubieboard-2),
    [CubieBoard3 / Cubietruck
    ](https://archlinuxarm.org/platforms/armv7/allwinner/cubietruck);

-   [Cubieboard2 - Wikipedia
    ](https://en.wikipedia.org/wiki/Cubieboard#Cubieboard2)
    is based on the A20 board; the newer improved models are the
    _Cubieboard 3_ and _Cubieboard 6_.
    _Cubieboard 6_

-   [CubieBoard3 / CubieTruck](https://cubieboard.org/tag/cubietruck/)
    also called CubieBoard3 is an improvement of
    CubieBoard2 with VGA, SPDIF, Gigabit ethernet, and 2Gb
    RAM. It support an 2"5 sata disk or a
    [3"5 sata witn an HDD adon board
    ](https://cubieboard.org/2013/09/24/how-to-support-3-5-inch-hdd-on-cubieboard/)

-   [Cubieboard 4
    ](https://www.cubietech.com/product-detail/cubieboard4/)
    _8 cores, 2GB DDR3, HDMI&VGA, 1GB ethernet, wifi,
    4 x USB HOST, 1 x OTG_, [On NewIt
    ](https://www.newit.co.uk/shop/All_Cubieboard/Cubieboard4) 133€.

-   [Cubietruck Plus (Cubieboard 5)
    ](https://www.cubietech.com/product-detail/cubieboard5/)
    has the same PCB layout and almost the same features as the CubieTruck.
    Specifications: Allwinner H8 Cortex-A7 @ 2 GHz octa-core,
    GPU: PowerVR SGX544 @ 700 MHz, HDMI 1.4 1080p and DisplayPort,
    2 GiB DDR3,  8 GB EMMC, 1x microSD, 1x SATA 2.0 port
    (Hard Disk of 2,5") via USB bridge,  RJ45 Gigabit Ethernet,
    2x USB Host, 1x USB OTG,  S/PDIF, headphone, and HDMI audio out,
    Wi-Fi (dual-radio 2.4 and 5 GHz) and Bluetooth on board with PCB
    antenna

    In [this release note
    ](https://cubieboard.org/2016/03/15/cubietruck-pluscubieboard5-released-now/)
    CubieTruck Plus can be connected directly to the SATA hard disk,
    but also can be built to a dual hard disk array by HDD-RAID
    subboard which transformed from USB3.0/SATA III to Dual SATA III
    interfaces. HDD can be configured as  : RAID0, RAID1, JOBD, PM.

    [Sold On NewIt
    ](https://www.newit.co.uk/shop/All_Cubieboard/Cubieboard5) 133€

-   [CubieBoard 6
    ](https://www.cubietech.com/product-detail/cubieboard6/)
    is an enhencement of _CubieBoards 2 and 3_ with a distinct chip
    _S500_ instead of _A20_ and sata 3 instead of sata 2.

    Specifications: [Actions SOC S500
    ](https://www.actions-semi.com/en/productview.aspx?id=209)，
    ARM Cortex-A9 Quad-Core CPU,Imagination PowerVR SGX544 GPU 2GB
    LPDDR3, 8GB eMMC, Micro SD card slot, up to 32GB, SATA3 support
    2.5 inch HDD/SSD up to 4TB, 2xUSB HOST Port, 1xUSB Device port,
    HDMI Port A, HDMI V1.4a, support 1080P@60Hz resolution, 10M/100M
    RJ45, Wifi 2.4GHz, 802.11 b/g/n, Bluetooth 4.0 (HS) BLE, IR
    receiver, audio 3.5 jack in and out, DCIN 5V@2.5A power, Support
    USB power input

    [Sold On NewIt
    ](https://www.newit.co.uk/shop/All_Cubieboard/Cubieboard6)
    83€

-   [CubieBoard 7
    ](https://www.cubietech.com/product-detail/cubieboard7/)
    Specifications: [Actions SOC S700
    ](https://www.actions-semi.com/en/productview.aspx?id=225)
    {{< iref "#cortex-A53" "Cortex-A53" >}} Quad-Core CPU, Mali450 MP4 GPU, 2GB LPDDR3, 8GB
    eMMC, micro SD card slot, up to 32GB, Support 2.5 inch HDD/SSD up
    to 4TB, USB HOST Port x2, and USB Device port x1, HDMI V1.4a,
    1080P@60Hz, 10M/100M RJ45, Wifi, Bluetooth, IR, audio jack in and
    out, RTC.

    It costs 98€ on amazon.

-   They are many
    [CubieBoard Resellers](https://cubieboard.org/buy/)
    -   [NewIt](https://www.newit.co.uk/shop/All_Cubieboard)
        Cubieboard2 (53€ vat included), Cubieboard 3 / CubieTruck 91€,
        Cubieboard 4 133€, Cubieboard 5 137€, Cubieboard 6 86€.

# ODROID
-   <a name="odroid-C4"></a>
    [ODROID-C4 – ODROID](https://www.hardkernel.com/shop/odroid-c4/)
    is powered by Amlogic S905X3 quad-core armV8 Cortex-A55 (2.0 XXGHz) processor.Onboard 4GB
    LPDDR4 memory and 16GB EMMC storage, and supports 4 USB 3.0 interface, a gigabit
    network port.

    It is the same soc than {{< iref "#bananapi-m5" "Banana pi M5" >}}
    see this entry for a comparison.

    It is priced 54€ _2022_ at
    [HardKernel Site](https://www.hardkernel.com/shop/odroid-c4/)
    where you find also accessories like a 5€4€ case, 5€50 power supply and EMMC modules
    from 15€ for 16G to 45€ for 128G.
-   [ODROID-XU4](https://www.hardkernel.com/shop/odroid-xu4q-special-price/)
    Samsung Exynos5422 Cortex-A15 2Ghz and Cortex-A7 Octa core CPUs,
    Mali-T628 MP6, 2Gbyte LPDDR3 RAM, eMMC5.0 HS400 Flash Storage,
    2 x USB 3.0 Host, 1 x USB 2.0 Host, Gigabit Ethernet, HDMI 1.4a,
    Power: 5V/4A input,
    -   On [hardKernel](https://www.hardkernel.com/shop/odroid-xu4q-special-price/)
        it is sold for 53$ _2022_, you find there accessories case, emmc modules, power
        supply ...
    -   [ ] In europe reichelt.de sell it a 89€ _2022_.
     A close sbc, with a different soc but with close functionalities is
    [ODROID-N2+](https://www.hardkernel.com/shop/odroid-n2-with-4gbyte-ram-2/)
     with similar USB-3 throughput but a slightly better GPU, it costs on hardkernel 84$
    and reichtel.de 136€ _2022_.
-   [Odroid-M1](https://www.hardkernel.com/shop/odroid-m1-with-8gbyte-ram/)
    features:
    Rockchip RK3568B2 CPU,
    LPDDR4 RAM,
    Micro USB2.0 Device only, 2 x USB 2.0, 2 x USB 3.0,
    Gb RJ45 Ethernet Port,
    HDMI 2.0,
    eMMC Module Socket,
    SPI Flash 16MiB,
    __M.2 NVMe M-Key PCIe3.0 2-Lane__,
    __SATA3__, SATA power.
    four-lane MIPI-DSI port,
    two-lane MIPI-CSI port.


    The four-lane MIPI-DSI port can be directly connected to a LCD panel like the
    [ODROID-Vu8M kit](https://www.hardkernel.com/shop/odroid-vu8m/).

    The two-lane MIPI-CSI port can be directly connected to a camera sensor like the
    [M1 MIPI-CSI Camera Kit](https://www.hardkernel.com/shop/m1-mipi-csi-camera-kit/).

    he M1 power consumption is about 4.5Watt with a very heavy computing load and
    1.3Watt in the idle state.

    On hardkernel Odroid-M1 with 8GB memory costs /in 2022/ 90$ the vU7A 7 inch display 73$,
    MIPI-CSI camera 20$, a metal case 9$40,  and EMMC modules
    from 15€ for 16G to 45€ for 128G power supply 9$40,  and EMMC modules from 15€ for
    16G to 45€ for 128G.

    On reichtel.de ODROID M1 8GB is priced 140€40 /in 2022/.

# OLinuXino
{{< wp "OLinuXino" >}} is an open hardware single-board computer capable of
running Android or Linux designed by OLIMEX Ltd in Bulgaria.

There are products based on i.MX233 ARM926J, Allwinner A13, A10S
Cortex-A8, Allwinner A20, Allwinner A64 - 1.2 GHz Quad-Core ARM-V8A
{{< iref "#cortex-a53" "Cortex-A53" >}}.

See {{< wp "OLinuXino" "Wikipedia OLinuXino" >}} for a list of all products

-   [OLimex OLinuxxino products](https://www.olimex.com/Products/OLinuXino/)
-   [GitHub  OLIMEX / OLINUXINO](https://github.com/OLIMEX/OLINUXINO)

-   [OlinuXino A64
    ](https://www.olimex.com/Products/OLinuXino/A64/A64-OLinuXino/open-source-hardware)
    CPU: [Allwinner A64](https://linux-sunxi.org/A64) 1.2 GHz Quad-Core
    {{< iref "#arm-v8" "ARM-V8" >}} {{< iref "#cortex-a53" "Cortex-A53" >}} 64-bit
    [Arm64](https://linux-sunxi.org/Arm64) architecture,
    Memory: 1GB or 2GB RAM DDR3L @ 672Mhz,
    0/4/16GB eMMC flash memory,
    MicroSD  up to 32GB,
    serial UART debug header,
    10/100/1000Mbps GbE Ethernet,
    on-board WIFI and bluetooth 4.0 BLE module (only in  A64-OLinuXino-1G4GW),
    HDMI output, LCD output and MIPI DSI,
    jack headphone output and microphone input,
    power jack for 5V external power. 50€ for 1G ram 4G emmc; 75€ for 2G
    ram, 16G emmc.

    This board has no SATA.
-   [A20-OLinuXino-LIME2
    ](https://www.olimex.com/Products/OLinuXino/A20/A20-OLinuXino-LIME2/)
    Allwinner A20/T2 dual core Cortex-A7 processor _same as bananapi M1/Pro_
    dual-core Mali 400 GPU,
    1GB DDR3 RAM memory,
    8GB NAND flash memory option,
    4GB or 16GB eMMC flash memory option,
    16MB SPI flash option,
    Native SATA support with connector and 5V SATA power jack,
    FullHD (1080p) video,
    HDMI support with connector,
    2 x USB High-speed host,
    USB-OTG,
    1000MBit Ethernet.

    Sold 40€ in 2022 on olimex site, 48€ with 4GB nand, 53€ with 16G emmc flash mem.,

    -   [FreedomBox A20-OLinuXino-Lime2
        ](https://wiki.debian.org/FreedomBox/Hardware/A20-OLinuXino-Lime2)
    -   [FreedomBox PioneerEdition
        ](https://wiki.debian.org/FreedomBox/Hardware/PioneerEdition)
        includes all the hardware needed for launching a FreedomBox home server on an
        Olimex A20-OLinuXino-LIME2 board.
        It is sold [on Olimex site
        ](https://www.olimex.com/Products/OLinuXino/Home-Server/Pioneer-FreedomBox-HSK/)
        at 69€. _2022_.

# SolidRun products
[SolidRun](https://www.solid-run.com/) produces many sbc based on
Marvell's Armada, NXP i.MX6 & i.MX8, and Intel Braswell (atom not ARM)

-   [ClearFog
    ](https://www.solid-run.com/marvell-armada-family/clearfog/clearfog-specifications/)
    are  based on [Marvell ARMADA 388
        ](https://www.marvell.com/embedded-processors/armada-38x/)
    -   Base Model has 1GB M.2, 8GB uSD/4GB eMMC (Optional), 1 x
        mPCIE, 1 x USB 3.0, 2 x Gigabit Ethernet, RTC Battery, Linux
        Kernel 4.x (OpenWRT/LEDE, Yocto) and cost 120$.
    -   Pro model has 1GB M.2, 8GB uSD/4GB eMMC (Optional), 2 x
        mSATA/mPCIE, 1 x USB 3.0 port, 1 x Port dedicated Ethernet, 5
        x Port switched Ethernet, 1 x SFP, RTC Battery, JTAG, Linux
        Kernel 4.x (OpenWRT/LEDE, Yocto), 180€
    -   An enclosure is available for 25€ for base model, 80$ for pro
        model.
    -   [OpenWRT - Clearfog
        ](https://openwrt.org/toh/solidrun/clearfog).
    -   [ClearFog GT 8K
        ](https://www.solid-run.com/marvell-armada-family/clearfog-gt-8k/)
        is a more powerfull platform based on ARMADA A8040 quad-core
        Cortex A72, up to 16GB DDR4 DIMM, MicroSD, eMMC, 4 x 1GbE switched LAN (RJ45)
        1 x 1GbE WAN (RJ45), 3 x mPCIe (USB 2.0 + PCIe), 1 x USB 3.0,
        1 x SFP+ (up to 10GbE).

        But the price is also higher from 200$ without memory to 620$
        with 16GB RAM and 128GB eMMC.

     -  In the same range of product than ClearFog GT 8K they produce
        also the [Cex7-A8040
        ](https://www.solid-run.com/marvell-armada-family/com-express-7-a8040/cex7-a8040-%20specifications/)

-  {{< wp "CuBox" >}} is a fan-less cube-shaped at 2 × 2 × 2 inches arm
   computer. It is produced by [Solid Run](https://imx.solid-run.com/),
   it is powered by an Freescale
   {{< wp "https://en.wikipedia.org/wiki/I.MX#i.MX_6_series"  "I.MX6" >}}
   Cortex A-9 processor.
   It is produced by [Solid Run](https://imx.solid-run.com/)
   where you find [Cubox-i Home page
    ](https://www.solid-run.com/freescale-imx6-family/cubox-i/)
    -   Cubox I2 model It has an [i.MX6 Freescale ARM Cortex-A9
        ](https://www.solid-run.com/nxp-family/imx6-som/imx6-som-specifications/)
        dual core cpu clocked at 800MHz, 1GByte DDR3, HDMI 1.4,
        S/PDIF, Gigabit Ethernet 2 x USB 2.0 host ports, IrDA
        receiver, MicroSD, optional WIFI.  Its power consumption is 1
        W + usb @ 5V/2A DC. It is sold at 110$ + VAT + shipping,
        including alimentation, and 8GB Micro SD with OS Android or
        Linux Kodi.
    -   I2ex hass also a dual core, but clocked at 1 GHz the same
        characteristics than i2 but adding a Gigabit ethernet, 1 x
        eSATA 3Gbps, RTC , MicroUSB to RS-232for console.  The i4 has
        same hardware but is a quad-core, and host 2GB DDR3. I2 ultra
        with power adaptor and 8GB microSD preloaded with linux Kodi
        or android.[Price on Newit
        ](https://www.newit.co.uk/shop/All-CuBox-i/Cubox-i's/)
        127$  _add  shipping (18$)_.
    -   The CuBox i4Pro model features 4 cores, 2Gb DDR3,
        1GB ethernet, 2 usb2, 1 eSata2, wifi, bluetooth,
        in a 2cmx2cmX2cm cube. 141€.
    -   CuBox  CuBox i4x4 features 4 cores, 4Gb DDR3,
        1GB ethernet, 2 usb2, 1 eSata2, wifi,  bluetooth.
        CuBox-i4x4 , Power Adapter ( 110V / 220V ) , 8GB Micro SD
        card preloaded with Kodi and an IR remote control.
        [Price on Newit
        ](https://www.newit.co.uk/shop/All-CuBox-i/Cubox-i's/) 144€.
    -   There is an [ArmBian](https://www.armbian.com/] distribution
        [for Cubox-i](https://www.armbian.com/cubox-i/Cubox),
        the [Xbian distribution](https://www.xbian.org/) which is a
        minimal distribution based on Debian support Cubox and provide
        the Kodi Media center.
        We find also an [ArchLinux support
        ](https://archlinuxarm.org/platforms/armv7/marvell/cubox)
    -   [NewIt: CuBox-i4Pro
        ](https://www.newit.co.uk/shop/All-CuBox-i/CuBox-i4Pro)

-   [HummingBoard
    ](https://www.solid-run.com/nxp-family/hummingboard/hummingboard-specifications/)
    are low cost [NXP i.MX6
    ](https://www.solid-run.com/nxp-family/imx6-som/imx6-som-specifications/)
    based platforms
    They feature [NXP i.MX6
    ](https://www.solid-run.com/nxp-family/imx6-som/imx6-som-specifications/)
    solo to quad core SOM, Up to 2GB DDR3, uSD,_for model Pro_ mSata,
    _for model Edge_ eMMC (8GB), M.2, 1xRJ-45 1000 Mbps link is
    limited to 470Mbp, _for Base_ 2 host USB 2.0, _for Gate and Edge_
    4xUSB 2.0, _for Pro Gate and Edge_ mPCIE, HDMI-Out, SPDIF, MIPI-
    CSI-2 Camera.
    -   [NewIt HummingBoard-i2eX
        ](https://www.newit.co.uk/shop/All-HummingBoard/Hummingboards/)
        i1 46€, ie2 67€, ie2x 88€,


# Misc Socs

-   [UDOO NEO](https://www.udoo.org/udoo-neo/) and
    [UDOO DUAL](https://www.udoo.org/udoo-quad-dual/)
    are single-board computers with a dual or quad core
    ARM Freescale {{< wp "Cortex-A9" >}}  and an {{< wp "Arduino" >}} board.
-   [UDOO X86 II ADVANCED PLUS](https://shop.udoo.org/en/udoo-x86-ii-advanced-plus.html)
    uses an CPU Intel Celeron N3160 2.24 Ghz 4 corzs, 4 GB DDR3L Dual Channel, 32GB eMMC
    storage, GPU Intel HD Graphics 400, 1x HDMI 2x miniDP++ connectors, Standard SATA
    connector, M.2 Key B SSD slot, Micro SD card slot, Gigabit Ethernet, 3 x USB 3.0
    type-A sockets. In 2022 it costs $242 + tva and shipping.
-   [UDOO X86 II ULTRA](https://shop.udoo.org/en/udoo-x86-ii-ultra.html) is similar to
    the advanced plus model but with a 4 cores CPU Intel Pentium N3710 2.56 GHz,
    and a RAM 8 GB DDR3L Dual Channel. In 2022 it costs $368 + tva and shipping.
-   [Unas](https://shop.udoo.org/en/projects/unas/) is a project of  creating a
    Network Attached Storage (NAS) with UDOO. It is also commented in this
    forum thread [x86 Used as NAS, Read Write Speeds
    ](https://www.udoo.org/forum/threads/x86-used-as-nas-read-write-speeds.6975/).
-   [MiraBox
    ](https://www.newit.co.uk/shop/All-MiraBox/MiraBox)
    1.2Ghz Marvell Armada CPU ARMADA 370 ARM v7, 1GB DDR3, 1 GB NAND
    Flash, 2 X 1GB ethernet, 2 x USB 3.0 host_ 122£.


# QNAP

[Debian is supported for Qnap orion TS109, TS-209, TS 409](https://www.cyrius.com/debian/orion/qnap/)
and [Qnap Kirkwood 11x, 12x, 21x, 22x, 41x, 42x](https://www.cyrius.com/debian/kirkwood/qnap/).

With a QNAP 109 you have first to check you have
[recovery mode](https://www.cyrius.com/debian/orion/qnap/ts-109/recovery.html)
then you will find the installation procedure in the page
[Installing Debian on the QNAP TS-109](https://www.cyrius.com/debian/orion/qnap/ts-109/install.html).
You can also look at some
[Debian installation screenshoots](https://wiki.qnap.com/wiki/Debian_Installation_On_QNAP)
on the Qnap wiki or in the
[Harryd's blog](https://harryd71.blogspot.com/2008/09/installing-debian-on-qnap-ts-209.htm).


Once we can ssh to the box we can continue following the
[Debian GNU/Linux Installation Guide for arm](https://www.debian.org/releases/lenny/arm/)
by using the orion5x build.

For my Qnap I use a lvm formatted disk. Lvm support is missing in the Qnap provided kernel.

# Debian on Buffalo Nas

Linkstation Pro and Live and KuroBox are based on an Orion chip, like are Qnap TS109, TS-209, TS 409.

-   [Intalling Debian on Buffalo KuroBox Pro
    ](https://www.cyrius.com/debian/orion/buffalo/kuroboxpro/)
    by Per Andersson and Martin Michlmayr .
-   [Install Debian on the Linkstation Pro/Live
    ](https://buffalo.nas-central.org/wiki/Install_Debian_on_the_Linkstation_Pro/Live)
    on *nas-central*.

Linkstation are now based on Marvell ARMADA 370 processor (1.2GH, 512M DDR3)
which is like a Kirkwood but with ARMv6/v7 (instead of ARMv5).Synology
use the same processor for its NAS, and we can at least
[run in a chroot
](https://www.rooot.net/fr/geek-stuff/synology/39-chroot-debian-sur-synology-avec-debootstrap.html).

# Excito Bubba

Excito Bubba line of NAS were running  Debian Squeeze

[Excito Bubba 3
](https://www.excito.com/bubba/products/technical-specifications.html)
features 1.2GHz ARM processor, 512MB RAM, 1 x internal 2"5 or 3"5 sata
drive bay, 2 Gigabit Ethernet, 2x USB2, 1 e-sata, optional wifi, 115 x
45 x 185 mm, 5-13W power consumption, fanless, run Debian Squeeze.

At _autumn 2013_ Excito changed focus to make hardware and software
platforms for the digital home, which they sell to operators. So the
Development of Bubba software is stalled to a squeeze release with a
2.6 Kernel;


[Excito wiki](https://wiki.excito.org/wiki/index.php/Main_Page)
is the primary source for Bubba related tutorials and how-tos.

The members of Excito that were developping this line of product have
moved to [OpenProduct](https://openproducts.se/) which is prepping a
tiny (105x105x25mm) Ubuntu-based private file and email server called
OPI ([technical specifications
](https://media.openproducts.com/tech_spec.pdf))
with Cortex A8 processor, 512MB RAM, LUKS-based microSD encryption,
and optional USB or cloud backup



# Software

-   {{< wp "Zephyr_(operating_system" "Zephyr" >}} (Apache2 License)
    is a real-time operating system (RTOS) for connected, resource-constrained and
    embedded devices like {{< wp  "microcontrollers" >}}.
    -   [Zephyr Project Documentation](https://docs.zephyrproject.org/latest/index.html).

## Monitoring
-   [rpi monitor](https://rpi-experiences.blogspot.fr/p/rpi-monitor.html)
    is a self monitoring application designed to run on Raspberry Pi.
    It gives the status: version, uptime, cpu, temperature, memory,
    swap, SD card usage, network traffic.
    -   [GitHub Rpi-monitor](https://github.com/XavierBerger/RPi-Monitor)
-   {{< iref "monitoring#conky" "conky" >}} can be used with raspberry.
-   {{< wp "Raspcontrol" >}}
    is a web control centre written in PHP for Raspberry Pi.
    It is no longer available but has numerous forks on GitHub.
    -   [harmon25/raspcontrol](https://github.com/harmon25/raspcontrol)
    -   [davidvuong/pyraspcontrol](https://github.com/davidvuong/pyraspcontrol)
        Python port of the original RaspControl by Bioshox
-   {{< iref "monitoring#monitorix" "monitorix" >}} can be used with
    raspberry, as explained in
    [How to set up a web-based lightweight system monitor on Linux
    ](https://www.xmodulo.com/web-based-lightweight-system-monitor-linux.html)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
