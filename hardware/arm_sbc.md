---
title: ARM Single Board Computers
---

{{% toc /%}}

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
-   ARMv7: provided by {{< wp "Cortex-M" >}}, {{< wp "Cortex-R" >}}, and {{< wp "Cortex-A" >}} 5
    to 17.
    -   Wikipedia: {{< wp "Comparison of ARMv7-A cores" >}}
    -   {{< wp "ARM_Cortex-A7" >}} is a popular processor that has many
        system-on-chips (SoC) by {{< wp "Allwinner_Technology"  "Allwinner" >}}
        (A20, A31, A83T ,H3, H8), {{< wp "Broadcom" >}},
        {{< wp "Freescale_Semiconductor"  "Freescale" >}},
        {{< wp "Marvell_Technology_Group"  "Marvell" >}}, Mediatek, Qualcomm,
        Samsung.
     -  {{< wp "ARM Cortex-A9 MPCore" >}} is a 32-bit multicore processor
        providing up to 4 cores, each implementing the ARM v7 instruction set.
        {{< wp "Cortex-A9" >}} is provided by [Texas Instrument OMAP4
        ](http://en.wikipedia.org/wiki/Texas_Instruments_OMAP#OMAP4),
        [Nvidia Tegra 2 series
        ](http://en.wikipedia.org/wiki/Nvidia_Tegra#Tegra_2_series)
        and
        [Freescale i.MX6x series (Wikipedia)
        ](http://en.wikipedia.org/wiki/I.MX#i.MX6x_series),
        [Freescale i.MX6x Home Page
        ](http://www.freescale.com/webapp/sps/site/taxonomy.jsp?code=IMX6X_SERIES).
    -   <a name=armada38x"></a>[Marvell ARMADA 38X
        ](https://www.marvell.com/embedded-processors/armada/armada-38x)
        is a family of ARMv7 multicore Socs with DDR3/DDR3L/DDR4 Ram
        (including ECC), PCI-e2.0, 2 or 3 Gigabits internets, 1 OSB
        3.0, 1 to 4 SATA, and a TDP of 3W to 4W.
-   ARMv8: provided by {{< wp "Cortex-A32" >}} _32 bits only_ and for
    32bits/64bits {{< wp "Cortex-A" >}} > 35 among which the most used in SBC
    is {{< wp "Cortex-A53" >}}, and Qualcom {{< wp "Snapdragon" >}}.
    -   ARMv8-A _2011_ also named ARMv8.0-A introduce 64 bits AArch64,
        ARMv8-A allows 32-bit applications to be executed in a 64-bit
        OS.
    -   Then it was improved in ARMv8.1-A _2014_, {{< wp "ARMv8.2-A" >}}_2016_
        supported by  {{< wp "Cortex-A55" >}} and {{< wp "Cortex-A75" >}} ,
        ARMv8.3-A _2016_.
    -   Wikipedia: {{< wp "Comparison of ARMv8-A cores" >}}
    -   {{< wp "Cortex-A53" >}} is the architecture of
        [Marvell’s ARMADA 3700
        ](https://www.marvell.com/embedded-processors/armada-3700/)
        found in EspressoBin,  and
        [Actions SOC S700
        ](http://www.actions-semi.com/en/productview.aspx?id=225)
        found in Cubieboard 7, and AllWinner
        [H64](http://linux-sunxi.org/H64),
        [H5](http://linux-sunxi.org/H5),
        [H6](http://linux-sunxi.org/H6).
-       [ArchWiki - Armv8 Platforms
        ](https://archlinuxarm.org/platforms/armv8)

## Linux Arm support

-   [Debian ARM port](http://www.debian.org/ports/arm/):
    -   [Intel IOP support](http://www.cyrius.com/debian/iop/)
        like the Thecus NAS,
    -   [Marvell's Kirkwood Debian Support
        ](http://www.cyrius.com/debian/kirkwood/)
        like {{< wp "SheevaPlug" >}}, {{< wp "Guruplug" >}}, [D2Plug
        ](http://www.globalscaletechnologies.com/p-43-d2-plug.aspx)
    -   [Marvell's Orion Debian Support
        ](http://www.cyrius.com/debian/orion/) like
        {{< iref "#qnap" "Debian on QNAP" >}},
-   [Debian Cheap ServerBox Hardware
    ](https://wiki.debian.org/CheapServerBoxHardware).
    is a list of arm small boxes that we can consider for open source
    project development.
-   [Ubuntu support ARM](https://wiki.ubuntu.com/ARM/),
    including [Ubuntu OMAP/OMAP4 support](https://wiki.ubuntu.com/ARM/OMAP).
    [Ubuntu ARM  device support](https://wiki.ubuntu.com/ARM/DeviceSupport).
-   [Arch Linux ARM](http://archlinuxarm.org/),
-   [Arm Platforms comparison](https://archlinuxarm.org/platforms).
-   [Bitkistl: Linux on ARM powered Devices](http://bitkistl.blogspot.fr/)
-   [elinux: RaspberryPi Comparison](http://elinux.org/RaspberryPi_Comparison)
    give a comparison of arm-linux development boards.
-   [Neil William](http://linux.codehelp.co.uk/) the previous leader
    of the project _Embedian_ has a
    [blog about ARMMP](http://linux.codehelp.co.uk/?s=armmp)
    the  Debian kernel for [armhf - Arm Hard Float
    ](https://wiki.debian.org/ArmHardFloatPort).
    Software are in [CodeHelp Github Repository
    ](https://github.com/codehelp).
-   [OmapPedia](http://www.omappedia.org/wiki/)
    reference the support across the miscellaneous distributions
    of the {{< wp "Omap" >}} arm processors developed by Texas Instruments

## Allwinner Technology

{{< wp "Allwinner_Technology"  "Allwinner" >}} is one of the more popular
manufacturer of arm SoC.

It produces the A1x serie of {{< wp "Cortex-A8" >}} ArmV7 SoC;
the A2x and A3x serie of {{< wp " Cortex-A7" >}} ArmV7 SoC; the A8x family
of  {{< wp " Cortex-A7" >}} and {{< wp "Cortex-A15" >}} ArmV7 SoC; The Hx family where
H2, H3, H8 are {{< wp " Cortex-A7" >}} ArmV7 SoCs and  AllWinner
[H64](http://linux-sunxi.org/H64), [H5](http://linux-sunxi.org/H5),
[H6](http://linux-sunxi.org/H6)are {{< wp "Cortex-A53" >}} armV8-A Socs.

-   Wikipedia: {{< wp "Allwinner_Technology"  "Allwinner" >}}
-   [AllWinner - A series
    ](http://www.allwinnertech.com/index.php?c=product&a=index&pid=2)
-   [AllWinner - H series
    ](http://www.allwinnertech.com/index.php?c=product&a=index&pid=6)
-   [Installing Debian On Allwinner
   ](https://wiki.debian.org/InstallingDebianOn/Allwinner)
-   [linux-sunxi](http://linux-sunxi.org/Main_Page)
    is an open source software community dedicated to Allwinner SoC
    based devices.
-   [ArchLinux AllWinner armv7 platform comparison
    ](http://archlinuxarm.org/platforms/armv7/allwinner)
-   {{< wp "Allwinner A1X" >}} can boot GNU/Linux distributions such as Debian,
    Ubuntu, Fedora, from an SD card, in addition to the Android OS
    installed on the flash memory.
-   [Allwinner A10 CPU](http://elinux.org/Allwinner_A1X)
    is an 1.5ghz ARM Cortex A8 with a MALI400 GPU,
    2160p Hardware-accelerated Video playback with  HDMI out up to
    1080p, USB 2.0 Host
    as well as a 2nd USB-OTG  Interface, 10/100
    Ethernet, SATA-II 3gb/sec., audio input and
    output, DDR3 512MB / 1GB, 4GB NAND storage,
    SDHC card slot supporting up to 32GB. <br />
    It run Linux or Android. It powers up
    [many tablets](http://elinux.org/A10_tablets) and
    [boards and minipc](http://elinux.org/A10_boards_and_minipc)
    on the Chinese market.
    The A10 can update the firmware from USB, so it can not be
    bricked, and it can be securely
    [hacked](http://elinux.org/Hack_A10_devices).
-   [Allwinner A20](http://elinux.org/Allwinner_A20)
    contains an {{< wp "Cortex-A7" >}} dual core, GPU – ARM Mali400 MP2, DDR3
    ram, 10/100 Ethernet, 4Gb Nand Flash, HDMI 1080p Output with
    3840×1080@30fps 3D decoding, 2 USB Host, 1 micro SD slot, 1 SATA,
    1 IR.


## Platform comparison.

-   [H2+/H3/H5 boards overview
    ](https://forum.armbian.com/topic/1351-h3-board-buyers-guide/?do=findComment&comment=44979).
    by [T Kaiser in armbian forum
    ](https://forum.armbian.com/profile/7-tkaiser/).
-   [Raspberry vs Banana vs A10-OLinuXino : powering and SATA performance
    ](http://hardware-libre.fr/2014/06/raspberry-vs-banana-vs-a10-olinuxino-powering-and-sata-performance/)
-   [OpenBenchmarking.org - ARM-SBC-Benchmark
    ](http://openbenchmarking.org/result/1408120-GLND-140706967&obr_sor%3Dy&obr_hgv%3DBanana%2BPi%2BSSD/)
    Comparison of Raspberry, Banana PI, Banana PI SSD
-   [Raspberry vs Banana : hardware duel | Hardware-Libre
    ](http://hardware-libre.fr/2014/06/raspberry-vs-banana-hardware-duel/) performance
-   [loverpi](https://www.loverpi.com/blogs/) comparisons
    -   [Raspberry Pi 3, Banana Pi M3, Orange Pi Plus 2, ODROID C2 Spec
        Comparison
        ](https://cdn.shopify.com/s/files/1/1098/4826/files/comparisonupdate.png),
    -   [CPU Performance Review of SBCs
        ](https://www.loverpi.com/blogs/news/95250433-cpu-performance-review-of-sbcs)
        includes banana pi (pi/m2/m3), odroid (odroid/c1+/c2/xu4), orange pi, orange
        pi/one/pc/plus, raspberry pi 2/pi 3, see also [the full test
        on openbenchmarking
        ](http://openbenchmarking.org/result/1604016-GA-MERGE757555)


#  Raspberry
{{< wp "Raspberry Pi" >}} is a single-board computer

-   version 1 had a  ArmV6 Broadcom BCM2835 ARM11 700Mhz cpu,
    512 Mb ram, SD Card Slot, USB 2.0, RCA video, HDMI socket,
    10/100 BaseT Ethernet socket
    power consumption of 3.5 W and a price of 45€.
-   version 2 uses a ArmV7 Broadcom BCM2836 SoC with a 900 MHz 32-bit
    quad-core ARM {{< wp "Cortex-A7" >}} processor, 1Gb RAM
-   version 3 uses a ArmV8-A Broadcom BCM2837 SoC with a 1.2 GHz
    64-bit quad-core ARMv8-A {{< wp "Cortex-A53" >}} processor, 1Gb RAM
-   The B-3+ launched in march 2018 has a Broadcom BCM2837B0 SoC with
    1.4 GHz 64-bit quad-core ARMv8-A {{< wp "Cortex-A53" >}}, 1Gb RAM,
    4xUSB-2.0, HDMI, analog audio I/O, MicroSDHC, 10/100/1000 Mbit/s
    Ethernet (real speed ~300 Mbit/s), 802.11ac dual band 2.4/5 GHz
    wireless, Bluetooth 4.2, 17× GPIO, power from 2.3W idle to 5.7w

## Refs
-   [raspberrypi.org](http://www.raspberrypi.org/).
-   [The Pi Hut](http://thepihut.com/) sells Raspberry and accessories.
-   [MagPi](http://www.themagpi.com/) is a magazine for Raspberry Pi
    users.
-   [The Embedded Linux Wiki (elinux.org)](http://elinux.org/Main_Page)
    host the Raspberry Pi wiki
    [RPi Hub](http://elinux.org/R-Pi_Hub).
    You find there
    [Tutorials](http://elinux.org/RPi_Tutorials),
    [liste of Guides](http://elinux.org/RPi_Guides),
    [RPi Troubleshooting](https://elinux.org/R-Pi_Troubleshooting),
    [Hardware specification](http://elinux.org/RPi_Hardware),
    [Expansion Boards](http://elinux.org/RPi_Expansion_Boards),
    [Cases](http://elinux.org/RPi_Cases),
    [VerifiedPeripherals](http://elinux.org/RPi_VerifiedPeripherals),
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
-   [RaspBerry Pi Stack Exchange](http://raspberrypi.stackexchange.com/)
-   [Raspbian](http://www.raspbian.org/) is a  Debian  variant optimized for
    the Raspberry Pi hardware. The [Raspbian FAQ](http://www.raspbian.org/RaspbianFAQ)
    and [Raspbian Documentation](http://www.raspbian.org/RaspbianDocumentation)
    give hints on package compiling.
-   <a name="omxplayer">[OMXPlayer](http://omxplayer.sconde.net/)
    is the command line OMX player for the Raspberry PI. Don't miss the keyboard
    shortcut listed on this page, ore in the [Github repository
    ](https://github.com/popcornmix/omxplayer).  There is no manual, and the command
    line options are in the usage string (from -h or missing arguments), but the
    keybindings are missing from the distribution.
    -   [GitHub - OMXPlayer](https://github.com/popcornmix/omxplayer).
    -   [OMXPlayer - Raspbian
        ](https://www.raspberrypi.org/documentation/raspbian/applications/omxplayer.md)
-   [Gentoo Wiki: Raspberry Pi Cross building
    ](http://wiki.gentoo.org/wiki/Raspberry_Pi_Cross_building)
-   There are many expansion boards for Raspberries most are listed
    in [RPIHub: Expansion Boards
    ](http://elinux.org/RPi_Expansion_Boards),
    you find also some sata expansion cards (by
    [SupTronics
    ](http://www.suptronics.com/Xseries.html),
    or [WDLabs
    ](http://wdlabs.wd.com/products/sata-adapter-board/))
    but they use an usb to sata bridge, so you cannot expect better
    performances than the usb provide.
-   [Ducky Pond Raspberry-pi tutorials
    ](http://www.ducky-pond.com/tag/raspberry-pi.html)
-   [HiFiBerry DAC/Digi/Amp products](https://www.hifiberry.com/) allow to build
    an high-quality and affordable audio distribution systems, based on RaspBerry.
    -   [DLNA/UPnP Server + Renderer – HiFiBerry
        ](https://support.hifiberry.com/hc/en-us/community/posts/115000045625-DLNA-UPnP-Server-Renderer/.

## Kodi on RaspBerry

{{< iref "media_players#kodi" "Kodi" >}}
[run on Raspberry](https://kodi.wiki/index.php?title=Raspberry_Pi)
either with a choice of specific distributions, like the minimal
[Xbian](http://wiki.xbmc.org/index.php?title=XBian),[osmc](https://osmc.tv/),
or on a modern Raspbian or following the
[Raspbian build recipe](http://www.raspbian.org/RaspbianXBMC).

-   [HOW-TO:Install Kodi on Raspberry Pi - Kodi Wiki
    ](https://kodi.wiki/view/HOW-TO:Install_Kodi_on_Raspberry_Pi),
    [On Raspbian](https://kodi.wiki/view/HOW-TO:Install_Kodi_on_Raspberry_Pi#Raspbian)
-   [Raspberry Pi FAQ - Kodi Wiki](https://kodi.wiki/view/Raspberry_Pi_FAQ)

# Banana Pi
the information on the bananapi devices are on Wikipedia {{< wp "Banana Pi" >}}
and on the [Banana Pi gitbook](https://www.gitbook.com/book/bananapi/).

-   Bananapi M1 has an ArmV7 {{< wp "Allwinner A20" >}} {{< wp "ARM Cortex-A7" >}}
    Dual-Core 1GB DDR3, 10/100/1000 Ethernet, HDMI, CVBS, LVDS/RGB
    Video output, 3.5mm jack and HDMI Audio output, SATA 2.0 (quite
    slow 36MB/s) , 2 x USB
    2.0 ports, the same GPIO headers as the Raspberry Pi 1 Model A &
    B.

    Note That the allwinner A20 was a nice improvement over the first
    single-core Raspberry Pis few years ago but is pretty slow by
    today’s standards. The native SATA is very slow, and the gigabit
    is not fully capable of 940 Mbits/sec in both directions.
    So Armbian suggest now to replace it with better alternatives like
    those listed in [This T. Kaiser post
    ](https://forum.armbian.com/topic/1351-h3-board-buyers-guide/?tab=comments#comment-28169).

-   Bananapi M2 improve CPU with an Allwinner A31S {{< wp "ARM Cortex-A7" >}}
    Quad-Core 1GHz, 4 x USB 2, but drop SATA.
-   Bananapi M2+ CPU is H3 Quad-core {{< wp "ARM Cortex-A7" >}} Quad-Core, one
    USB 2.0 HOST, NO SATA, Wifi,
-   [Bananapi M2 Ultra
    ](https://www.gitbook.com/book/bananapi/bpi-m2-ultra-open-source-single-board-computer/details)
    _November 2016_ has an [Allwinner R40
    ](https://en.wikipedia.org/wiki/Allwinner_Technology#R-Series)
    {{< wp "ARM Cortex-A7" >}} Quad-Core 2GHz, 2GB DDR3 SDRAM, 8G eMMC flash on
    board, bluetooth 4.0 and SATA interface. The Allwinner R40’s
    advantage over the H3 and A31 is the addition of eMMC flash and
    native SATA support.
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

-   [Banana Pi - Wikipedia](http://en.wikipedia.org/wiki/Banana_Pi)
-   [Banana Pro | Banana Pi - LeMaker](http://www.lemaker.org/):
    [Banana Pi Quick Start Guide
    ](http://www.lemaker.org/resources/9-39/banana_pi_quick_start_guide.html),
    [Banana Pi Wiki - lemaker.org](http://wiki.lemaker.org/Main_Page),
    [FAQ](http://wiki.lemaker.org/FAQ),
    [GitHub: LeMaker resources](https://github.com/LeMaker).
    Banana Pro is  an update version of Banana PiTM,
    designed by LeMaker Team.
-   [bananapi.org - Banana Pi](http://www.bananapi.org/): site officiel (?) du Banana Pi
    [Banana Pi specifications and layout diagrams
    ](http://www.bananapi.org/p/product.html),
-   [BananaPi - Google Groups
    ](https://groups.google.com/forum/#!forum/bananapien)
-   [Banana Pi - ArchWiki](https://wiki.archlinux.org/index.php/Banana_Pi)


## Banana Pi development
-   Banana dev - GitHub  allow to [Build Banana Pi Image
    ](https://github.com/bananapi-dev/BPi/blob/master/HowToBuild_BPi_image.en.txt)
-   Instruction to get a cross dev platform, build kernel and uboot
    and set the sdcard is in lemaker wiki at:
    [Building u-boot, script.bin and linux-kernel - Banana Pi
    ](http://wiki.lemaker.org/Building_u-boot,_script.bin_and_linux-kernel),
    [Setting up the bootable SD card - Banana Pi
    ](http://wiki.lemaker.org/Setting_up_the_bootable_SD_card)
-   The linux-sunxi site has also
    [Linux Kernel - linux-sunxi.org](http://linux-sunxi.org/Linux#A20), and
    [Toolchain - linux-sunxi.org](http://linux-sunxi.org/Toolchain)

## Vente du Banana Pi

-   [banana-pi.com](http://www.banana-pi.com/)
    a la [liste des revendeurs](http://www.banana-pi.com/egsjj.asp?id=12)
-   [lextronic.fr
    ](http://www.lextronic.fr/), principallement raspberry et
    alternatives mais a le  Banana Pi et nombreux modèles de modules.
-   [BananaPi.fr (vente)
    ](http://e.banana-pi.fr/) et [BananaPiFr | Facebook
    ](https://www.facebook.com/BananaPiFrance?ref%3Dhl)
    _Site assez cher avec peu d'accessoires, mais livraison bon marché._
-   [reichelt.de - Banana PI](http://www.reichelt.de/)
    un des meilleurs sites européens, a le BananaPi, RaspberryPi et
    beaucoup de materiels.
-   [Amazon.fr : banana-pi
    ](https://www.amazon.fr/s/ref=nb_sb_noss?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&url=search-alias%3Daps&field-keywords=bananapi)
    ](http://www.amazon.fr/Banana-Wireless-power-cable-Antenne/dp/B00MWUIA4Y/ref%3Dsr_1_5?ie%3DUTF8&qid%3D1419784076&sr%3D8-5&keywords%3Dbanana-pi)
-   [New It : Banana Pi
    ](https://www.newit.co.uk/shop/All-Banana-Pi/BananaPiBoard)
-   China banana PI, orange Pi, Suppliers  Aliexpress.com
    [banana Pi](http://www.aliexpress.com/wholesale?SearchText=banana+pi).

# ESPRESSObin

Specifications:

-   [Marvell’s ARMADA 3700
    ](https://www.marvell.com/embedded-processors/armada-3700/)
    {{< wp "Cortex-A53" >}} dual-core  up to 1.2 GHz.
-   1x [Topaz Networking Switch
    ](http://wiki.espressobin.net/tiki-index.php?page=Topaz+Switch)
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

-   [ESPRESSObin Wiki](http://wiki.espressobin.net/).
-   [I/O ports and connectors
    ](http://wiki.espressobin.net/tiki-index.php?page=Quick+User+Guide#I_O_ports_and_connectors),
    and [hardware brief outline
    ](http://espressobin.net/espressobin-hardware-brief-outline/)
-   [ESPRESSObin Quick User Guide
    ](http://wiki.espressobin.net/tiki-index.php?page=Quick+User+Guide).
-   [Software How To
    ](http://wiki.espressobin.net/tiki-index.php?page=Software+HowTo)
    many pages on building and bootin a kernel image and how to
    [update the bootloader
    ](http://wiki.espressobin.net/tiki-index.php?page=Update+the+Bootloader)
-   [Getting Started Tutorials
    ](http://wiki.espressobin.net/tiki-index.php?page=Getting+Started+Tutorials)
-   [Running OpenSSL speed test on ESPRESSObin
    ](http://wiki.espressobin.net/tiki-index.php?page=Running+OpenSSL+speed+test+on+ESPRESSObin).


The ESPRESSObin is unbrickable you can always do
[boot ESPRESSObin from SATA drive
](http://wiki.espressobin.net/tiki-index.php?page=Boot+ESPRESSObin+from+SATA+drive)


-   [Marvell ESPRESSObin Forum](http://espressobin.net/forums/)
-   [Debian Wiki - Installing debian on Marvell ESPRESSOBin
    ](https://wiki.debian.org/InstallingDebianOn/Marvell/ESPRESSOBin)


-   {{< iref "#armbian" "ArmBian" >}} supports the espressobin,
    -   [armbian - Espressobin](https://www.armbian.com/espressobin/)
    -   [Espressobin support development efforts
        ](https://forum.armbian.com/topic/4089-espressobin-support-development-efforts/)
    -   [ESPRESSObin Forum](http://espressobin.net/forums/) :
        [Armbian Ubuntu / Debian
        ](http://espressobin.net/forums/topic/armbian-ubuntu-debian/),
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
    ](http://indietech.rocks/howto/espressobin-home-router.html)
-   [My EspressoBIN board is up
    ](http://upon2020.com/blog/2017/05/my-espressobin-board-is-up/)
-   [Molex to SATA power adapter - Marvell ESPRESSObin
    ](http://espressobin.net/forums/topic/molex-to-sata-power-adapter/)

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
    ](http://www.cyrius.com/debian/kirkwood/sheevaplug/) and
    [Plug Computer models and how well they are supported in Debian
    ](http://www.cyrius.com/debian/kirkwood/sheevaplug/plugs.html)
-   [Martin Michlmayr review of SheevaPlug
    ](http://www.cyrius.com/journal/debian/kirkwood/sheevaplug/nslu2-killer)
-   Distributed by [globalscaletechnologies.com
    ](http://www.globalscaletechnologies.com/p-26-sheevaplug-dev-kit-europe.aspx)
    and [NewIt](https://www.newit.co.uk/shop/All-SheevaPlug/) (~120€)
-   [ArchLinux Platforms](https://archlinuxarm.org/platforms)
    support some plug computers.

[Tonido Plug 2](http://www.tonidoplug.com/tonido_plug.html)
is a variant of SheevaPlug, with 512 MB of DDR3, 512 MB of Flash, USB
2.0, Gigabit Ethernet, WiFi, 2.5 inch SATA.
It run Ubuntu to provide
a nas and media streaming. It costs 78€ now discounted 32€ at
[NewIT](https://www.newit.co.uk/shop/All-TonidoPlug/TonidoPlug2).

{{< wp "GuruPlug" >}} is the successor of Sheevaplug.  with 1.2 GHz ARM Marvell
Kirkwood 6281 (ARM9E i.e. ARM-v5), 512MB SDRAM, 512MB NAND, USB 2.0,
Gigabit Ethernet, JTAG, Bluetooth 2.1, Wi-Fi 802.11 b/g

[DreamPlug
](http://www.globalscaletechnologies.com/p-41-dreamplug-devkit.aspx)
is the successor of GuruPlug. Its specifications are: 71.2 GHz ARM
Marvell Kirkwood 88F6281 SoC (ARM9 i.e. ARM-v5), 2MB Flash for uboot, 2
GB Flash, 512MB SDRAM, 1xMicro-SD system + 1SD Slot,2xUSB 2.0
Microphone in, Headphone out, 2xgibabits Ethernet,1xeSata, SP/DIF out,
WiFi /BT, Jtag and Uart. It costs 176€ [at NewIt
](https://www.newit.co.uk/shop/All-DreamPlug/).

[D2Plug](http://www.globalscaletechnologies.com/p-43-d2-plug.aspx)
Specifications: a Marvell PXA510 – 800MHz, 1GB 1GB DDR3 Ram,
Powered eSATA, USB 2.0 Host and USB 2.0 device, SD card slot,
1 xGb ethernet, VGA and and HDMIoutput, mic in, audio out and s/pdif,
usb console, jtag.  200$.

[SmilePlug](http://www.globalscaletechnologies.com/p-57-smileplug.aspx)
specifications are:
Marvell ARMv7 ARMADA 370 CPU, WiFi, 2x USB 3.0, 2x Gigabit Ethernet
1x Microsd, 1GB NAND Flash / 512MB DDR3, TAG.
It run ArchLinux ARM and cost 200$.


#  BeagleBoard

[BeagleBoard](http://en.wikipedia.org/wiki/BeagleBoard) and BeagleBone
There is two _BeagleBones_
they both adhere to the same standard for expansion and interfacing.
[beagleboard.org](http://beagleboard.org/) is the Beagleboard Home
page where you can find technical and commercial information on
these boards.
-    BeagleBone has 720 MHz superscalar ARM Cortex-A8 AM3358/9,
     256 MB DDR2 RAM, MicroSD slot, USB 2.0 host, USB mini OTG,
     Storage-over-USB or Ethernet-over-USB on other USB device
     port, Power consumption of 300-500mA at 5V
-    BeagleBone Black is a 1 GHz superscalar ARM Cortex-A8 AM3359,
     with 512 MB DDR3 RAM, 2 GB eMMC flash, MicroSD slot,
     USB 2.0 host, mini-USB 2.0 client, HDMI output,
     power consumption of 210-460 mA at 5V
-    [Embedded Linux Wiki (elinux): BeagleBoard
    ](http://elinux.org/BeagleBoard)
     is related to BeagleBoard and BeagleBoard-xM that both use
     {{< wp "Texas instrument OMAP" >}} Single-board computer (ARM
     architecture). A distinct SoC is used for the following _BeagleBone]_.
-    [Embedded Linux Wiki (elinux): BeagleBone
    ](http://elinux.org/BeagleBone)
     gives a description of the two boards the original _BeagleBone_
     and the new _BeagleBone Black_ .
     The _BeagleBone_ has support in Angstrom,
     [Debian](http://elinux.org/BeagleBoardDebian), Ubuntu,
     [ArchLinux](http://archlinuxarm.org/platforms/armv7/beaglebone),
     Gentoo, and more ...
-    [digikey sell beagleboards and BeagleBones
     ](http://dkc1.digikey.com/us/mkt/beagleboard.html).
     A BeagleBone black card costs 45$ shipping from US and taxes not included.
-    [Adafruit](http://www.adafruit.com/) sell BeagleBones and
     accessories enclosure (20$), power supply _5VDC, 1A, 2.1mm,
     center positive_ (10$),..
-    [Farnel element14.com
     ](http://www.element14.com/community/community/knode/dev_platforms_kits/element14_dev_kits/next-gen_beaglebone)
     is a reseller network with numerous agents in many EU and asian countries.
-    [BeagleBoneBlack Wiki
     ](http://circuitco.com/support/index.php?title=BeagleBoneBlack)
     has also an [accessories page
     ](http://circuitco.com/support/index.php?title=BeagleBone_Black_Accessories).

# CubieBoard
{{< wp "Cubieboard" >}} is a single-board computer manufacured by
[cubietech.com](http://www.cubietech.com/).

The processors goes from  AllWinner A10 {{< wp "Cortex-A8" >}} for cubieboard
1,  AllWinner A20 2x{{< wp "Cortex-A7" >}} for CubieBoard 2 and 3, Allwinner A80
4x Cortex-A15 and 4x{{< wp "Cortex-A7" >}} {{< wp "ARM big.LITTLE" >}} for CubieBoard 4,
Allwinner H8 8x{{< wp "Cortex-A7" >}} CubieBoard 5, Actions SOC S500
4x{{< wp "Cortex-A9" >}}

The {{< wp "Cubieboard"  "Cubieboard Wikipedia Page" >}} lists the specifications
of the models. A lot of the actual platforms are on sell on
[NewIt](https://www.newit.co.uk/shop/All_Cubieboard).

-   [CubieBoard.org](http://cubieboard.org/)
-   [Cubie Forums](http://www.cubieforums.com/)
-   [Debian CubieBoard Page](https://wiki.debian.org/CubieBoard)
-   [Cubian](http://cubian.org/),
    [GitHub Cubian](https://github.com/cubieplayer/Cubian) is a
    Debian distribution for CubieBoard 1 and 2 based on Debian wheezy.
    _Not updated since 2014_
-   [sunxi: Cubieboard wiki](http://linux-sunxi.org/Cubieboard)
-   ArchLinux: [Cubieboard
    ](http://archlinuxarm.org/platforms/armv7/allwinner/cubieboard),
    [Cubieboard 2
    ](http://archlinuxarm.org/platforms/armv7/allwinner/cubieboard-2),
    [CubieBoard3 / Cubietruck
    ](https://archlinuxarm.org/platforms/armv7/allwinner/cubietruck);

-   [Cubieboard2 - Wikipedia
    ](http://en.wikipedia.org/wiki/Cubieboard#Cubieboard2)
    is based on the A20 board; the newer improved models are the
    _Cubieboard 3_ and _Cubieboard 6_.
    _Cubieboard 6_

-   [CubieBoard3 / CubieTruck](http://cubieboard.org/tag/cubietruck/)
    also called CubieBoard3 is an improvement of
    CubieBoard2 with VGA, SPDIF, Gigabit ethernet, and 2Gb
    RAM. It support an 2"5 sata disk or a
    [3"5 sata witn an HDD adon board
    ](http://cubieboard.org/2013/09/24/how-to-support-3-5-inch-hdd-on-cubieboard/)

-   [Cubieboard 4
    ](http://www.cubietech.com/product-detail/cubieboard4/)
    _8 cores, 2GB DDR3, HDMI&VGA, 1GB ethernet, wifi,
    4 x USB HOST, 1 x OTG_, [On NewIt
    ](https://www.newit.co.uk/shop/All_Cubieboard/Cubieboard4) 133€.

-   [Cubietruck Plus (Cubieboard 5)
    ](http://www.cubietech.com/product-detail/cubieboard5/)
    has the same PCB layout and almost the same features as the CubieTruck.
    Specifications: Allwinner H8 Cortex-A7 @ 2 GHz octa-core,
    GPU: PowerVR SGX544 @ 700 MHz, HDMI 1.4 1080p and DisplayPort,
    2 GiB DDR3,  8 GB EMMC, 1x microSD, 1x SATA 2.0 port
    (Hard Disk of 2,5") via USB bridge,  RJ45 Gigabit Ethernet,
    2x USB Host, 1x USB OTG,  S/PDIF, headphone, and HDMI audio out,
    Wi-Fi (dual-radio 2.4 and 5 GHz) and Bluetooth on board with PCB
    antenna

    In [this release note
    ](http://cubieboard.org/2016/03/15/cubietruck-pluscubieboard5-released-now/)
    CubieTruck Plus can be connected directly to the SATA hard disk,
    but also can be built to a dual hard disk array by HDD-RAID
    subboard which transformed from USB3.0/SATA III to Dual SATA III
    interfaces. HDD can be configured as  : RAID0, RAID1, JOBD, PM.

    [Sold On NewIt
    ](https://www.newit.co.uk/shop/All_Cubieboard/Cubieboard5) 133€

-   [CubieBoard 6
    ](http://www.cubietech.com/product-detail/cubieboard6/)
    is an enhencement of _CubieBoards 2 and 3_ with a distinct chip
    _S500_ instead of _A20_ and sata 3 instead of sata 2.

    Specifications: [Actions SOC S500
    ](http://www.actions-semi.com/en/productview.aspx?id=209)，
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
    ](http://www.cubietech.com/product-detail/cubieboard7/)
    Specifications: [Actions SOC S700
    ](http://www.actions-semi.com/en/productview.aspx?id=225)
    {{< wp "Cortex-A53" >}} Quad-Core CPU, Mali450 MP4 GPU, 2GB LPDDR3, 8GB
    eMMC, micro SD card slot, up to 32GB, Support 2.5 inch HDD/SSD up
    to 4TB, USB HOST Port x2, and USB Device port x1, HDMI V1.4a,
    1080P@60Hz, 10M/100M RJ45, Wifi, Bluetooth, IR, audio jack in and
    out, RTC.

    It costs 98€ on amazon.

-   They are many
    [CubieBoard Resellers](http://cubieboard.org/buy/)
    -   [NewIt](https://www.newit.co.uk/shop/All_Cubieboard)
        Cubieboard2 (53€ vat included), Cubieboard 3 / CubieTruck 91€,
        Cubieboard 4 133€, Cubieboard 5 137€, Cubieboard 6 86€.

# ODROID
-   [ODROID-XU4
    ](http://www.hardkernel.com/main/products/prdt_info.php)
    Samsung Exynos5422 Cortex™-A15 2Ghz and Cortex™-A7 Octa core CPUs,
    Mali-T628 MP6, 2Gbyte LPDDR3 RAM, eMMC5.0 HS400 Flash Storage,
    2 x USB 3.0 Host, 1 x USB 2.0 Host, Gigabit Ethernet, HDMI 1.4a,
    Power: 5V/4A input,
    -   [Sold on amazon
        ](https://www.amazon.fr/odroid-xu4/s?ie=UTF8&page=1&rh=i%3Aaps%2Ck%3Aodroid%20xu4).
        for 80€ including shipping.

# OLinuXino
{{< wp "OLinuXino" >}} is an open hardware single-board computer capable of
running Android or Linux designed by OLIMEX Ltd in Bulgaria.

There are products based on i.MX233 ARM926J, Allwinner A13, A10S
Cortex-A8, Allwinner A20, Allwinner A64 - 1.2 GHz Quad-Core ARM
Cortex-A53.

See {{< wp "Wikipedia OLinuXino" >}} for a list of all products

-   [OLimex OLinuxxino products
    ](https://www.olimex.com/Products/OLinuXino/)
-   [GitHub  OLIMEX / OLINUXINO](https://github.com/OLIMEX/OLINUXINO)

[OlinuXino A64
](https://www.olimex.com/Products/OLinuXino/A64/A64-OLinuXino/open-source-hardware)
CPU: Allwinner A64 - 1.2 GHz Quad-Core ARM Cortex-A53 64-bit,
Memory: 1GB or 2GB RAM DDR3L @ 672Mhz,
0/4/16GB eMMC flash memory,
MicroSD  up to 32GB,
serial UART debug header,
10/100/1000Mbps GbE Ethernet,
on-board WIFI and bluetooth 4.0 BLE module (only in  A64-OLinuXino-1G4GW),
HDMI output, LCD output and MIPI DSI,
jack headphone output and microphone input,
power jack for 5V exeternal power. 50€ for 1G ram 4G emmc; 75€ for 2G
ram, 16G emmc.


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
   computer. It is produced by [Solid Run](http://imx.solid-run.com/),
   it is powered by an Freescale
   {{< wp "https://en.wikipedia.org/wiki/I.MX#i.MX_6_series"  "I.MX6" >}}
   Cortex A-9 processor.
   It is produced by [Solid Run](http://imx.solid-run.com/)
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
        the [Xbian distribution](http://www.xbian.org/) which is a
        minimal distribution based on Debian support Cubox and provide
        the Kodi Media center.
        We find also an [ArchLinux support
        ](http://archlinuxarm.org/platforms/armv7/marvell/cubox)
    -   [NewIt: CuBox-i4Pro
        ](https://www.newit.co.uk/shop/All-CuBox-i/CuBox-i4Pro)

-   [HumminBoard
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

-   [UDOO](http://www.udoo.org/) is a single-board computer with a dual or quad core
    ARM Freescale {{< wp "Cortex-A9" >}}  and an {{< wp "Arduino" >}} board.
    The UDOO Quad
    features a Freescale i.MX 6 ARM Cortex-A9 Quad core 1GHz, GPU,
    Arduino compatible ARM Cortex-M3 CPU, RAM DDR3 1GB, HDMI and LVDS,
    2 Micro USB (1 OTG type a+b), 2 USB type A, analog audio/mic,
    micro SD card, RJ45 (10/100/1000 MBit), WiFi Module, SATA for
    135$ + taxes.<br />
    The first distribution provided are Ubuntu and Yocto.
-   [Utilite 2](http://www.compulab.co.il/utilite-computer/web/utilite2-models)
    is a Qualcomm Snapdragon 600 (APQ8064) ARMv7 quad-core @1.7GHz
    2GB DDR3, eMMC 4GB, mSATA socket, HDMI 1.4a, Gb Ethernet,
    WiFi 802.11b/g/n + Bluetooth 4.0, 4x USB2.0 host + USB OTG
    200$ + VAT + shipping.
    -   [Utilite run either Ubuntu or Android](http://utilite-computer.com/web/utilite-software).
-   [Trim-Slice](http://utilite-computer.com/web/models)
    is a fanless ARM desktop in an 0.6" thin metal
    case. It is based on NVIDIA {{< wp "Tegra" >}} 2 a dual-core ARM Cortex A9 at 1 GHz,
    it has 1 GB DDR2 RAM soldered on-board, either 32GB SSD
    or 2.5″ SATA hard disk, one Sd and one micro-SD both up to 32 GB.
    HDMI 1.3a 1080p and a DVI-D up to 1680 x 1050, stereo line-out and
    line-in, Gigabit Ethernet, 4 USB 2 ports, 2-6W power consumption.
    <br />
    The price of Trim-Slice range from 170€+VAT for a computer with
    Micro-SD 4 GB H costs, 250€+vat for H(arddisk) model with a 250GB
    sata, 300€+vat for a SATA SSD 32 GB. They are sold by
    [Tiny-Green store
    ](https://store.tinygreenpc.com/tiny-green-pcs/trim-slice.html)
    -   [TrimSlice on Debian](https://wiki.debian.org/TrimSlice)
-   [MiraBox
    ](https://www.newit.co.uk/shop/All-MiraBox/MiraBox)
    1.2Ghz Marvell Armada CPU ARMADA 370 ARM v7, 1GB DDR3, 1 GB NAND
    Flash, 2 X 1GB ethernet, 2 x USB 3.0 host_ 163€.


# QNAP

[Debian is supported for Qnap orion TS109, TS-209, TS 409](http://www.cyrius.com/debian/orion/qnap/)
and [Qnap Kirkwood 11x, 12x, 21x, 22x, 41x, 42x
](http://www.cyrius.com/debian/kirkwood/qnap/).

With a QNAP 109 you have first to check you have
[recovery mode](http://www.cyrius.com/debian/orion/qnap/ts-109/recovery.html) then you will find the installation procedure in the page
[Installing Debian on the QNAP TS-109](http://www.cyrius.com/debian/orion/qnap/ts-109/install.html).
You can also look at some
[Debian installation screenshoots](http://wiki.qnap.com/wiki/Debian_Installation_On_QNAP "wiki.qnap.com Debian_Installation_On_QNAP" )
on the Qnap wiki or in the
[Harryd's blog](http://harryd71.blogspot.com/2008/09/installing-debian-on-qnap-ts-209.htm "harryd71.blogspot.com installing-debian-on-qnap-ts-209.htm").


Once we can ssh to the box we can continue following the [Debian GNU/Linux Installation Guide for arm](http://www.debian.org/releases/lenny/arm/) by using the orion5x build.

For my Qnap I use a lvm formatted disk. Lvm support is missing in the Qnap provided kernel..

# Debian on Buffalo Nas

Linkstation Pro and Live and KuroBox are based on an Orion chip, like are Qnap TS109, TS-209, TS 409.

-   [Intalling Debian on Buffalo KuroBox Pro
    ](http://www.cyrius.com/debian/orion/buffalo/kuroboxpro/)
    by Per Andersson and Martin Michlmayr .
-   [Install Debian on the Linkstation Pro/Live
    ](http://buffalo.nas-central.org/wiki/Install_Debian_on_the_Linkstation_Pro/Live)
    on *nas-central*.

Linkstation are now based on Marvell ARMADA 370 processor (1.2GH, 512M DDR3)
which is like a Kirkwood but with ARMv6/v7 (instead of ARMv5).Synology
use the same processor for its NAS, and we can at least
[run in a chroot
](http://www.rooot.net/fr/geek-stuff/synology/39-chroot-debian-sur-synology-avec-debootstrap.html).

# Excito Bubba

Excito Bubba line of NAS were running  Debian Squeeze

[Excito Bubba 3
](http://www.excito.com/bubba/products/technical-specifications.html)
features 1.2GHz ARM processor, 512MB RAM, 1 x internal 2"5 or 3"5 sata
drive bay, 2 Gigabit Ethernet, 2x USB2, 1 e-sata, optional wifi, 115 x
45 x 185 mm, 5-13W power consumption, fanless, run Debian Squeeze.

At _autumn 2013_ Excito changed focus to make hardware and software
platforms for the digital home, which they sell to operators. So the
Development of Bubba software is stalled to a squeeze release with a
2.6 Kernel;


[Excito wiki](http://wiki.excito.org/wiki/index.php/Main_Page)
is the primary source for Bubba related tutorials and how-tos.

The members of Excito that were developping this line of product have
moved to [OpenProduct](http://openproducts.se/) which is prepping a
tiny (105x105x25mm) Ubuntu-based private file and email server called
OPI ([technical specifications
](http://media.openproducts.com/tech_spec.pdf))
with Cortex A8 processor, 512MB RAM, LUKS-based microSD encryption,
and optional USB or cloud backup


# Arm distributions
-   [Armbian](http://www.armbian.com/) by Igor Pečovnik is a
    lightweight Debian squeeze, Jessie or Ubuntu  based Linux
    distribution for arm platforms.

    It supports
    Banana Pi(M1, M2, M2+, Pro, Plus A20,), Orange Pi (One, 2, PC,
    PC2, PC plus, Plus 2E, Plus 1 & 2, mini A20, Lite, Prime, Win,
    A31S), NanoPi (M1, M1+, Neo, Neo2, Duo), Olimex ( Lime 1, Lime
    A10, Micro, Lime 2), Odroid C0/C1/C1+/C2/XU4/HC1, pcDuino2/3,
    Cubieboard 1/2, Roseapple Pi, Beelink X2, Le Potato, Espressobin,
    Pine64, soPine64, Pinebook A64, Hummingboard, Lamobo R1, pcDuino3
    nano, Udoo quad, Cubox-i, Cubietruck, Tinker Board, Miqi, Rock64.

    -   [Armbian on twitter](https://twitter.com/armbian)

-   [Bananian Linux](https://www.bananian.org/) distribution for
    Debian on Banana Pi; it stopped at Jessie and should now be
    replaced by Armbian
    -   [GitHub: Bananian Linux](https://github.com/Bananian) has
        development repositories,
    -   [bananian](https://github.com/Bananian/bananian)
        Bananian Linux tools and config files.


# Software

## Monitoring
-   [rpi monitor
    ](http://rpi-experiences.blogspot.fr/p/rpi-monitor.html)
    is a self monitoring application designed to run on Raspberry Pi.
    It gives the status: version, uptime, cpu, temperature, memory,
    swap, SD card usage, network traffic.
    -   [GitHub Rpi-monitor
        ](https://github.com/XavierBerger/RPi-Monitor)
    -   [my raspberry RPI Monitor](http://192.168.1.8:8888/)
    Rpimonitord uses 3 daemons processes in perl 7.6M/1.9M 6.8M/1.5M
    6.6M/1.2M ~ $7.6 + 6.8 - 1.5 + 6.6 - 1.2 => 18.3  $
-   {{< iref "monitoring#conky" "conky" >}} can be used with raspberry.
    [Conky for the Raspberry Pi
    ](http://jeffskinnerbox.me/posts/2012/Nov/02/conky-for-the-raspberry-pi/)
-   {{< wp "Raspcontrol" >}}
    is a web control centre written in PHP for Raspberry Pi.
    It has numerous forks on GitHub.
-   {{< iref "monitoring#monitorix" "monitorix" >}} can be used with
    raspberry, as explained in
    [How to set up a web-based lightweight system monitor on Linux
    ](http://xmodulo.com/2014/05/web-based-lightweight-system-monitor-linux.html)
-   I use {{< iref "monitoring#monit" "monit" >}} on bananapi.
-   [Banoffee Pi Server](http://banoffeepiserver.com/):
    [web based monitoring
    ](http://banoffeepiserver.com/server-monitoring/simple-web-based-monitoring-tools.html)
    with _linux-dash_, _phpsysinfo_, _Linfo_ or
    [Ganglia](http://banoffeepiserver.com/server-monitoring/ganglia/).

## Network monitoring.
-   [Monitor your LAN with Raspberry Pi
    ](https://sites.sas.upenn.edu/kleinkeane/blog/2013/07/monitor-your-lan-raspberry-pi)
-   [Network Monitoring with MRTG on Raspberry Pi
    ](http://resources.intenseschool.com/network-monitoring-with-mrtg-on-raspberry-pi/)


## Cluster

-   [Banoffee Pi Server](http://banoffeepiserver.com/): a Bananapi
    cluster with Mysql,
    [Glusterfs](http://banoffeepiserver.com/glusterfs/),
    [web based monitoring
    ](http://banoffeepiserver.com/server-monitoring/simple-web-based-monitoring-tools.html)
    with _linux-dash_, _phpsysinfo_, _Linfo_ or
    [Ganglia](http://banoffeepiserver.com/server-monitoring/ganglia/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
