---
title: Xorg
---

See also {{< iref "input_methods" "Input method" >}} where you find
{{< iref "input_methods#xkb" "Xkb" >}},
{{< iref "console" "Console section" >}}, {{< iref "desktop" "Desktop" >}} where is found the
{{< iref "desktop#clipboard" "Clipboard managers" >}}.

---

# References

-   [Debian X Strike Force’s documentation](http://x.debian.net/)
    -   [X Strike Force’s General FAQ
        ](http://x.debian.net/faq/general.html)
    -   The [obsolete XStrikeForce site
        ](http://wiki.debian.org/XStrikeForce/)
        and it's [Debian X Window System Frequently Asked Questions
        ](http://wiki.debian.org/XStrikeForce/FAQ)  may have still more
        _sometime obsolete_ content.
-   [Debian Reference Chapter 7. The X Window System
    ](https://www.debian.org/doc/manuals/debian-reference/ch07.en.html)
-   [ArchWiki - Xorg](http://wiki.archlinux.org/index.php/Xorg)
-   [Gentoo Xorg Guide](https://wiki.gentoo.org/wiki/Xorg/Guide),
    [Hardware 3D acceleration guide
    ](https://wiki.gentoo.org/wiki/Xorg/Hardware_3D_acceleration_guide)
-   [FreeBSD Handbook -  Xorg Configuration
    ](https://www.freebsd.org/doc/handbook/x-config.html)
-   [Xephyr](http://freedesktop.org/wiki/Software/Xephyr)
    is a kdrive based X Server which targets a window on a host X
    Server as its framebuffer.
-   [freedesktop DRI Wiki](https://dri.freedesktop.org/wiki/)
-   [sxhkd](https://github.com/baskerville/sxhkd)
    is an X daemon that reacts to input events by executing commands.
-   [xannotate](http://furius.ca/xannotate/) opens a screen-size window
    over whatever is present and allows you to scribble over it.
    This is useful when you are doing a demo and you need to annotate
    parts of what is on-screen.

# xrandr {#randr}

{{< wp "RandR" >}} is an extension to the X11. With Randr you can set the
screen refresh rate, choose a monitor output, resize, rotate and
reflect the root window of a screen.

It supports Multi-monitor panning, and output border adjustment.

-   [Xorg Xrandr home page
    ](https://www.x.org/wiki/Projects/XRandR/).
-    ArchWiki :[xrandr](https://wiki.archlinux.org/index.php/xrandr),
    [Multihead](https://wiki.archlinux.org/index.php/Multihead).
-   [Thinkwiki: Xorg RandR 1.2 - xrandr manual
    ](http://www.thinkwiki.org/wiki/Xorg_RandR_1.2)
-   [Debian X Strike Force - HowTo RandR12
    ](http://wiki.debian.org/XStrikeForce/HowToRandR12)
    The RandR 1.2 extension provides automatic discovery of modes
    (resolutions, refresh rates, ...) together with the ability to
    configure outputs dynamically (resize, rotate, move, ...).

    This page is partially obsolete _2012_ but still contains useful information like
    [Use xrandr to enable/disable/move/resize multiple outputs
    ](https://wiki.debian.org/XStrikeForce/HowToRandR12#II._Use_xrandr_to_enable.2Fdisable.2Fmove.2Fresize_multiple_outputs).
-   [X Strike Force - How to use xrandr
    ](https://xorg-team.pages.debian.net/xorg/howto/use-xrandr.html)
-   [Ubuntu Wiki: resolution](https://wiki.ubuntu.com/X/Config/Resolution)
-   [xrasengan](https://github.com/geyslan/xrasengan) (Apache License)
    is a shell script that act as a xrandr wrapper, aimed to make
    multi-monitor setup easier.

xrandr has some gui interfaces:

-   [LXrandR](https://wiki.lxde.org/en/LXRandR) from lxde is a  basic
    monitor config tool. It is in Debian.
-   [aRandr](http://christian.amsuess.com/tools/arandr/) (GPL)
    is a more powerfull tool written in python / PyGTK. It allows full
    control over output positioning with edge snapping, and saving
    configurations as executable shell scripts.

# Wayland {#wayland}

See also
{{< iref "xterminals#wayland_terminals" "Wayland Terminals" >}},
{{< iref "desktop#wayland_compositors" "Wayland Compositors" >}}.

{{< wp "Wayland_(display_server_protocol)"  "Wayland" >}} is a protocol between a
compositor and its clients. The compositor sends input events to the
clients. The clients render locally and then communicate video memory
buffers and information about updates to those buffers back to the
compositor.

It can replace X as the native Linux graphics server or collaborate
with X. Wayland is a graphics multiplexer for a number of X servers,

-   Wikipedia {{< wp "Wayland_(display_server_protocol)"  "Wayland" >}},
    {{< wp "List_of_display_servers#Wayland"  "List of Wayland compositors" >}}
-   [Freedesktop Wayland Home](http://wayland.freedesktop.org/):
    [Wayland FAQ](http://wayland.freedesktop.org/faq.html)
-   <a name='weston"></a>{{< wp "Wayland_(display_server_protocol)#Weston"  "weston" >}}
    is the reference C implementation of a Wayland compositor.
    It is in debian.
-   [Xwayland](http://wayland.freedesktop.org/xserver.html)
    is an Xorg server modified to use wayland input devices for input
    and forward either the root window or individual top-level windows
    as wayland surfaces. The server still runs the same 2D driver with
    the same acceleration code as it does when it runs natively. The
    main difference is that wayland handles presentation of the
    windows instead of KMS. xwayland is in debian.

# Framebuffer
See also {{< iref "xterminals#framebuffer_terminals" "Framebuffer terminals" >}},
{{< iref "console_applications#framebuffer_applications" "Framebuffer Applications" >}}.

X.org _xf86-video-fbdev_ driver module provides framebuffer under
Xorg. It is in the package _xserver-xorg-video-fbdev_.

# Synaptics Touchpad

-   [Ubuntu: Synaptics Touchpad
    ](https://help.ubuntu.com/community/SynapticsTouchpad)
-   [ArchLinux: Touchpad Synaptics
    ](https://wiki.archlinux.org/index.php/Touchpad_Synaptics)

# Display Managers
See also the {{< iref "#xdmcp" "XDMCP section" >}}

-   Wikipedia: {{< wp "X display manager" >}}
-   [ArchWiki: Display Manager
    ](https://wiki.archlinux.org/index.php/display_manager)
    has a list of display managers for console and Xorg.
-   [CDM](https://github.com/evertiro/cdm/) (GPL)
    is a miminimal display manager for the console, written in bash.
    -   [CDM - ArchWiki](https://wiki.archlinux.org/index.php/CDM).
-   [Gnome Display Manager
    ](http://en.wikipedia.org/wiki/GNOME_Display_Manager)
    (GPL) is an alternative to {{< iref "#xdm" "XDM" >}}
    and newer implementation using gtk libraries.
    GDM has numerous added features, but is dependent of gtk. Despite
    his name, you can use it without a full gnome environment, and he is
    appropriate with any gtk desktop. GDM has a nice configuration tool,
    that make its use a lot less painful than xdm. Although his virtual
    memory size is three or four time the xdm one *(14M against 4 on one
    of my desktop)* its resident size is quite close *(1.6M/1.1M)*.
    -   [GDM Home Page](https://wiki.gnome.org/Projects/GDM)
    -   [GDM Reference Manual
        ](https://help.gnome.org/admin/gdm/stable/)
    -   [ArchWiki: GDM](https://wiki.archlinux.org/index.php/GDM).
-   <a name="lightdm"></a>[LightDM](http://en.wikipedia.org/wiki/LightDM) (GPL)
    is a window manager with same functionalities than _GDM_ but without Gnome
    dependencies.  LightDM is the default display manager for LXDE including lxubuntu,
    and many minimal distributions. The memory footprint of lightdm are 3.6M resident /
    3M shared for each session mother and children (3 on my desktop).  It is truly light
    since we can think that shared memory is actually shared among the session children.
    The lightdm GTK+ greeter is 14M / 10M for the gtk greater but it vanishes once
    connected.
    -   [Lightdm - GitHub](https://github.com/canonical/lightdm)
    -   [ArchWiki Lightdm](https://wiki.archlinux.org/index.php/LightDM)
    -   [LightDM - Debian Wiki](https://wiki.debian.org/LightDM)
    -   [Ubuntu Lightdm](https://wiki.ubuntu.com/LightDM),

    The guest account is setup by a script, the
    [guest-account provided in the distribution
    ](https://github.com/canonical/lightdm/blob/master/debian/guest-account.sh),
    that may be [patched to provide autologin
    ](https://aur.archlinux.org/cgit/aur.git/tree/0002-guest-account-Enable-autologin-guest-account-command.patch)
    or [ArchWiki simpler script
    ](https://aur.archlinux.org/cgit/aur.git/tree/guest-account.sh).

    -   [How to customize guest session - Ubuntu Help
        ](https://help.ubuntu.com/community/CustomizeGuestSession)

-   <a name="ldm"></a>[ldm
    ](http://wiki.ltsp.org/wiki/LTSPManual#The_LDM_display_manager)
    is the {{< iref "#ltsp" "LTSP" >}} display manager, it is written in python
    and connect through an ssh tunnelconnect through an ssh tunnel instead of XDMCP. _It
    is in Debian with two packages ldm and ldm-server_.
-   [Qingy](http://qingy.sourceforge.net/) (GPL)
    is a replacement for getty written in C, it uses DirectFB and allow
    to choose a login session (X or fb text). _Qingy is no more developped since 2010_.
    -   [Ubuntu Qingy tutorial
        ](https://help.ubuntu.com/community/qingy)
    -   [Gentoo Wiki: Qingy](https://wiki.gentoo.org/wiki/Qingy)
-   _Slim_ was a
    Desktop-independent graphical login manager for X11.
    The memory footprint for slim is 18M resident / 4M shared. Not so slim compared with
    lightdm. _It is abandonned since 2013 but still in Debian as far of 2019 buster_.
    -   [ArchWiki: SLIM](https://wiki.archlinux.org/index.php/Slim)
-   [Xdm (Wikipedia)
    ](http://en.wikipedia.org/wiki/XDM_(display_manager)) (MIT License)
    manages a collection of X displays, which may be on the local host
    or remote servers. It implements
    {{< iref "#xdmcp" "XDMCP, the X Display Manager Control Protocol" >}}.
    -   The configuration and options are described in the man page:
        [xdm(1)](https://www.x.org/releases/X11R7.6/doc/man/man1/xdm.1.xhtml)
    -   [ArchWiki: XDM](https://wiki.archlinux.org/index.php/XDM)
    -   [Ubuntu: Custom Xsession tutorial
        ](https://wiki.ubuntu.com/CustomXSession)


# Remote Deskstop {#remote_desktop}
-   Wikipedia: {{< wp "Remote desktop software" >}},
    {{< wp "Comparison of remote desktop software" >}},
    {{< wp "SPICE (protocol)"  "SPICE" >}},
    {{< wp "RFB protocol" >}},
    {{< wp "Xrdp" >}},
    {{< wp "NX technology" >}},
    [XDMCP
    ](https://en.wikipedia.org/wiki/X_display_manager_(program_type)#X_Display_Manager_Control_Protocol)

-   [rdesktop](http://www.rdesktop.org/) (GPL)
    is an UNIX client implementing RDP protocol for connecting to Windows Remote
    Desktop Services. It is in Debian, with also [grdesktop
    ](http://www.nongnu.org/grdesktop/) the gnome frontend.
    -   [Rdesktop - ArchWiki](https://wiki.archlinux.org/index.php/Rdesktop).
-   [xrdp remote desktop protocol(rdp) server](http://www.xrdp.org/) (Apache Licence)
    Based on the work of FreeRDP and rdesktop, xrdp uses the remote desktop protocol
    to present a GUI to the user. xrdp accepts connections from a variety of RDP
    clients: FreeRDP, rdesktop, Remina, NeutrinoRDP and Microsoft Remote Desktop
    Client.
    -   [xrdp - GitHub](https://github.com/neutrinolabs/xrdp) (Apache Licence)
    -   [XorgXrdp](https://github.com/neutrinolabs/xorgxrdp) (Apache Licence)
        is a collection of modules to be used with a pre-existing X.Org install to make
        the X server act like X11rdp.
    -   [Xrdp - ArchWiki](https://wiki.archlinux.org/index.php/Xrdp).

-   <a name="spice"></a>[Spice](http://www.spice-space.org/) (GPL)
    is a solution for interaction with virtualized desktop devices.  It provides remote
    access to {{< iref "virtualization#qemu" "Qemu" >}} virtual machine.  There are
    clients for linux, windows, android, a plugin for browsers like Firefox or Chromium;
    a Server for Qemu and a server for Xorg _Xspice_.
    You find in Debian _xserver-xspice_, _spice-client_, _spice-client-gtk_,
    _browser-plugin-spice_, _spice-html5_.
    -   Wikipedia {{< wp "SPICE (protocol)" >}}
-   [TeamViewer](http://www.teamviewer.com/) is a private source free
    software for remote control, desktop sharing, online meetings, web
    conferencing and file transfer between computers.
    TeamViewer is available for Microsoft Windows, Mac OS X,
    Linux, Chrome OS, iOS, Android, Windows RT, Windows Phone 8 and
    BlackBerry operating systems.
    -   Wikipedia {{< wp "Teamviewer" >}}

## XDMCP {#xdmcp}
[XDMCP
](https://en.wikipedia.org/wiki/X_display_manager_(program_type)#X_Display_Manager_Control_Protocol)
In X Window System a server can connect, using the XDMCP protocol, to a display
manager running on another computer, requesting it to start the session.  Users
start programs from the computer running the display manager, while their input and
output take place on the computer where the server (and the user) sits.

XDM, GDM, LightDM, SLiM can be configured to accept XDMCP.

-   [Xorg - X Display Manager Control Protocol (Xdmcp)
    ](https://www.x.org/releases/X11R7.6/doc/libXdmcp/xdmcp.html)
-   [Linux XDMCP HOWTO](https://www.tldp.org/HOWTO/html_single/XDMCP-HOWTO/)
-   [XDMCP - ArchWiki](https://wiki.archlinux.org/index.php/XDMCP)
-   [xdmcp - Ubuntu Wiki](https://wiki.ubuntu.com/xdmcp)

## XPRA {#xpra}
[Xpra](http://xpra.org/) (GPL)
is a multi-platform (linux, windows, OS-X) persistent remote
display server and client for forwarding applications and desktop
screens.

It gives you remote access to individual applications or full
desktops.  On X11 it allows you to run programs, usually on a
remote host, direct their display to your local machine, and then
to disconnect from these programs and reconnect from the same or
another machine, without losing any state. Unlike VNC, these
applications are "rootless".  They appear as individual windows
inside your window manager rather than being contained within
a single window.

It can also be used to forward full desktops, from X11 servers,
MS Windows, or Mac OS X.

Xpra also allows forwarding of sound, clipboard and printing
services.  Sessions can be accessed over SSH, or password
protected over plain TCP sockets.

Xpra can be used with  {{< iref "#winswitch" "winswitch" >}}.

Xpra is in Debian, and also a Debian repository is also
[available on the Xpra site](http://xpra.org/trac/wiki/Download#Linux).

-   [ArchWiki: Xpra](https://wiki.archlinux.org/index.php/Xpra)
-   [Xpra HTML5 Client](http://xpra.org/trac/wiki/Clients/HTML5)

## VNC {#vnc}
-   Wikipedia: {{< wp "Virtual_Network_Computing" >}} (VNC),
    {{< wp "Comparison of remote desktop software" >}}.
-   [vnc susefaq how-to](http://susefaq.sourceforge.net/howto/vnc.html)
-   Ubuntu Help: [VNC](https://help.ubuntu.com/community/VNC),
    [VNC/Servers](https://help.ubuntu.com/community/VNC/Servers).


## VNC Servers/client software

### Libvncserver based
[libvncserver](https://github.com/LibVNC/libvncserver) (GPL)
LibVNCServer/LibVNCClient are cross-platform C libraries.
there are an old project, but it is actively maintained in 2017.
It is the base of many clients and servers. The most known being
X11vnc.

[x11vnc](https://github.com/LibVNC/x11vnc)
is the VNC server, build
with LibVNCServer, previously part of the libvnc project, but now
in a separate repository since the version 0.9.14.

It has built-in SSL encryption and authentication, UNIX account
and password support, server-side scaling, single port HTTPS and
VNC, mDNS service advertising, and TightVNC and UltraVNC
file-transfer.

This is an old project, the core of the project comes from 0.9.13
year 2010 which is is packaged in Debian for version up to _buster_.

LibVNC and the GitHub community have taken over the development since 0.9.14.  on Jan 5,
2019 0.9.16 was released and is available in Debian _bullseye_. You can find
[the latest release on GitHub](https://github.com/LibVNC/x11vnc/releases/latest).

It can use as X display either the virtual framebuffer X server
[Xvfb](https://manpages.debian.org/unstable/xvfb/Xvfb.1.en.html)
which is available on most platforms and does not require root; or
Xdummy a wrapper script which until 9.13 was
[part of the x11vnc source code
](https://github.com/LibVNC/x11vnc/blob/187cb9f70d71353827ff2c01f9e0d65b767be071/misc/Xdummy) and
since 9.14 is a C program. An advantage of Xdummy over Xvfb is that
Xdummy supports {{< iref "#xrandr" "RANDR" >}} dynamic screen resizing.

-   [x11vnc documentation
    ](http://www.karlrunge.com/x11vnc/index.html)
    the documentation for the old project, but still actual.
-   [X11vnc - ArchWiki](https://wiki.archlinux.org/index.php/X11vnc)
-   [VNCpp](https://github.com/ocrespo/VNCpp) (GPL)
    is a VNC viewer to Android powered by LibVNCServer.
-   [vncterm](https://github.com/LibVNC/vncterm) (GPL)
    contains two programs; LinuxVNC
    exports a virtual console sessions to any VNC client; and VNCommand
    executes a command redirecting stdin from a vncviewer and stdout &
    stderr to the vnc clients. _vncterm_ is a client
    splitted out from libvncserver. It is in Debian.

### TightVNC
[TightVNC](http://www.tightvnc.com/). (previously GPL)
is a VNC server, the data encoding is optimized for low
bandwidth connections. It was an improvement over vncserver, but
now is present in both servers. This server does not need a
display on the server machine. It is in the debian package
_tightvncserver_ for version 1.3.9.

The Linux version stopped at 1.3.10 in 2009; it is now only
developped for windows with version 2.8.5 in 2016 with a private
licence.
You can replace it by the {{< iref "#tigervnc" "TigerVnc" >}} fork.

-   Van Emery has
    [VNC over SSH2 - A TightVNC Tutorial
    ](http://www.vanemery.com/Linux/VNC/vnc-over-ssh.html) _2003,
    the site seems no longer available_
-   Gentoo wiki:
    [TightVNC](https://wiki.gentoo.org/wiki/TightVNC).
-   _tightvnc-java_ is a java aplet for a browser vnc client. It is in
    Debian.
-   [ssvnc](http://www.karlrunge.com/x11vnc/ssvnc.html)
    is an enhanced version of the TightVNC client with
    support for x11vnc and UltraVNC extensions. It support the
    connection to x11vnc using using stunnel  or SSH tunnel,
    as well as forwarding of ports for audio, SMB, CUPS etc.
    It is in Debian.

### TigerVnc {#tigervnc}
[TigerVnc](http://tigervnc.org/) is a fork of TightVNC in 2009.

-   [TigerVnc GitHub Repository](https://github.com/TigerVNC/tigervnc)
-   [TigerVnc Wiki](https://github.com/TigerVNC/tigervnc/wiki)
-   [ TigerVNC - ArchWiki](https://wiki.archlinux.org/index.php/TigerVNC)
-   [TigerVNC - Gentoo Wiki](https://wiki.gentoo.org/wiki/TigerVNC)
-   Manuals:
    -   [vncconfig](http://tigervnc.org/doc/vncconfig.html)
    -   [vncpasswd](http://tigervnc.org/doc/vncpasswd.html)
    -   [vncserver](http://tigervnc.org/doc/vncserver.html)
    -   [vncviewer](http://tigervnc.org/doc/vncviewer.html)
    -   [x0vncserver](http://tigervnc.org/doc/x0vncserver.html)
    -   [Xvnc](http://tigervnc.org/doc/Xvnc.html)


Debian has TigerVnc package since _stretch_.

_TigerVnc_ can expose directly the X server like does {{< iref "#x11vnc" "X11VNC" >}}
through an Xorg extension _libvnc.so_, which is in Debian in a separate package
_tigervnc-xorg-extension_. You will use
[x0vncserver](http://tigervnc.org/doc/x0vncserver.html) to share the X display connected
to the physical screen remotely. Unlike [Xvnc](http://tigervnc.org/doc/Xvnc.html)  it
does not create a virtual display.

TigerVnc can be used with {{< iref "#virtualgl" "VirtualGL" >}} to acelerate
OpenGl rendering.

### Vino
[Vino](https://wiki.gnome.org/Projects/Vino) (GPL) is the GNOME VNC Server.

- [Vino - ArchWiki](https://wiki.archlinux.org/index.php/Vino).

### TurboVNC {#turbovnc}
[TurboVNC](https://www.turbovnc.org/) (GPL)

is a VNC server tuned to provide peak performance for 3D and video workloads. It is a
fork of of TightVNC.  2D and 3D TurboVNC's encoding methods have been adopted by
TigerVNC and libvncserver.  TurboVNC is compatible with other VNC distributions,
particularly with those that also support Tight encoding (such as TigerVNC, TightVNC,
and UltraVNC.)  TurboVnc can be used with {{< iref "#virtualgl" "VirtualGL" >}} to
provides a highly performant display of 3D applications.

-   [Sourceforge TurboVnc downloads](https://sourceforge.net/projects/turbovnc/files/)
    provide packages for TurboVnc, for Debian there are i386 and amd64 packages.

### RealVNC {#realvnc}
[RealVNC](http://www.realvnc.com/)
(previously GPL, now Private license) Is a VNC server that runs on
Windows, Mac OS X, Linux and other Unixes.  It provides also many VNC
client that run on the Java platform for Chrome and Linux, Mac,
Windoze, Ios (iPhone, iPod touch and iPad) and Google Android.

As the GPL License stopped with 4.1.1 in 2012, this version is still
the one available as client xvnc4viewer and server xvnc4server in
Debian Jessie under the name vnc4server, but in strech it is replaced
by tigervnc.

In 2017 RealVNC server download is 6.0.2, it proposes a .deb
package.

-   Wikipedia {{< wp "RealVNC" >}},
-   [FAQ](http://www.realvnc.com/faq.html)

## Other clients and software

-   <a name="directvnc">[directvnc](http://drinkmilk.github.com/directvnc/) (GPL)
    VNC client on a linux framebuffer. It is in Debian.
-   [Vnc2flv
    ](http://www.unixuser.org/~euske/python/vnc2flv/index.html)
    is a cross-platform screen recording tool for UNIX,
    Windows or Mac. It captures a VNC desktop session either your own
    screen or a remote computer and saves as a Flash Video (FLV)
    file.
    -   [vnc2flv GitHub repository](https://github.com/baijum/vnc2flv).
-   [Remina](https://remmina.org) (GPL)
     is a Gnome remote desktop client written in GTK+, which supports multiple network
     protocols, Currently RDP, {{< iref "#vnc" "VNC" >}}, {{< iref "#spice" "SPICE" >}},
     {{< iref "x2go" "NX" >}}, {{< iref "#xdmcp" "XDMCP" >}},  {{< iref "ssh" "SSH" >}}
     and EXEC. It is in Debian and also provided as _Flatpak_ or _Snap_ package.
     -   [Remmina GitLab repository](https://gitlab.com/Remmina/Remmina)
     -   [Remmina Wiki](https://gitlab.com/Remmina/Remmina/wikis/home)
     -   [Remmina - ArchWiki](https://wiki.archlinux.org/index.php/Remmina)
-   [Veyon](https://veyon.io/) (GPL) previously _ITALC_
    is a vnc based software that lets you view and control other
    computers in your network. It is aimed to pupils computer control
    and viewing by a teacher. the
    [Veyon Documentation](https://docs.veyon.io/en/latest/)
    is the main documentation source for the veyon software.
-   [Gitso](http://code.google.com/p/gitso/) (GPL)
    is a frontend to reverse VNC connections. It connects one person which need support
    to another's screen of a person that offer support. It is
    available in windows, linux, OSX. The project is no longer active since _2010_ but it
    is still in Debian.
-   [noVNC](https://novnc.com/info.html) (Mozilla Public License)
    is a HTML5 VNC client that runs well in any modern browser
    including mobile browsers (iOS and Android).
    It supports WebSocket SSL/TLS encryption (i.e. "wss://").

    _noVNC_ should work on any browser with reasonable HTML5 support:
    Chrome 49, Firefox 44, Safari 11, Opera 36, IE 11, Edge 12

    _noVNC_ does require WebSockets support, which is included in servers like
    {{< iref "#x11vnc" "X11vnc" >}} or in {{< iref "virtualization#qemu" "Qemu" >}},
    and [MobileVNC](http://www.smartlab.at/mobilevnc/). For others servers you need to
    use a WebSockets to TCP socket proxy like
    [websockify](https://github.com/novnc/websockify).


    -   [noVNC GitHub](https://github.com/novnc/noVNC).

-   <a name="virtualgl">[VirtualGL](https://virtualgl.org/Main/HomePage) (GPL)
    gives any Linux or Unix remote display software the ability to run OpenGL
    applications with full hardware acceleration.

    It can be used with X11 forwarding, or vnc,
    {{< iref "#turbovnc" "Turbovnc" >}}
    and {{< iref "#tigervnc" "Tigervnc" >}} openGl rendering van benefit from
    VirtualGL

    -   [VirtualGL - ArchWiki](https://wiki.archlinux.org/index.php/VirtualGL).
-   VNC can be used with {{< iref "#winswitch" "winswitch" >}}.

## NX and X2Go {#x2go}

-   [Wikipedia: NX technology
    ](http://en.wikipedia.org/wiki/NX_technology).
    Prior to version 4.0, NoMachine used the GNU General Public
    License for the core NX technology, and offered a free client and
    server products for Linux.  Since December 2010, NoMachine
    releases >= NX 4.0 are closed-source only.
-   [Debian Wiki: Freenx](https://wiki.debian.org/freenx) obsolete
    software, using the older NX release. No longer provided in Debian.
-   [ArchWiki: FreeNx](https://wiki.archlinux.org/index.php/FreeNX).
-   [X2Go](http://wiki.x2go.org/) (GPL and AGPL)
    uses the NX3 technology, and replaces FreeNx. Debian has packages for x2goserver,
    x2goclient, and many x2go addon packages.
-   [X2Go - ArchWiki](https://wiki.archlinux.org/index.php/X2Go)

## Winswitch {#winswitch}

[winswitch](http://winswitch.org/) (GPL) is a tool which allows you to display running
applications on other computers than the one you start them on.

WinSwitch supports many different protocols for accessing remote applications and desktops:
NX, {{< iref "#vnc" "VNC" >}}, {{< iref "#xpra" "Xpra" >}}, SSH, RDP,  and
GStreamer ( read-only screencasting).

It is in Debian,  a Debian repository is also
[available on the winswitch site](http://winswitch.org/downloads/debian-repository.html).

# Thin Clients
## References
-   Wikipedia {{< wp "Thin client" >}}

## LTSP {#ltsp}
-   [Wikipedia: LTSP](http://en.wikipedia.org/wiki/Linux_Terminal_Server_Project)
-   [Linux Terminal Server Project](http://www.ltsp.org/) (GPL),
-   [LTSP wiki](http://wiki.ltsp.org/) :
    [LTSP Documentation  (LTSPedia)
    ](http://wiki.ltsp.org/wiki/LTSPedia)
-   [Gentoo Wiki - LTSP Guide
    ](https://wiki.gentoo.org/wiki/LTSP),
-   [Edubuntu](http://www.edubuntu.org)  is a distribution based on
    {{< iref "distributions#distrib_ubuntu" "Ubuntu" >}}
    organized around LTSP servers running education customized Ubuntu
    and LTSP clients.  You find a collection of
    [LTSP documentation at help.ubuntu.com
    ](https://help.ubuntu.com/community/UbuntuLTSP/).
-   _LTSP_ use {{< iref "#ldm" "ldm" >}} window manager to connect to the display
    through an ssh tunnel.
-   Linux Journal howtos: [Linux Terminal Servers for Any
    Business](http://www.linuxjournal.com/article/8822) by Mark Rais
    _2006_;
    [MILLE-XTERM and LTSP](http://www.linuxjournal.com/article/9097) by
    F. Giraldeau, J.M. Dault and B. des Ligneris  _2006_.

## Other thin clients

-   {{< wp "Thinstation" >}} (GPL)
    is a _thin client_ operating system.
    -   [Thinstation Home](http://thinstation.github.io/thinstation/)
    -   [Thinstation Wiki
        ](https://github.com/Thinstation/thinstation/wiki)
    -   [Thinstation sourceforge project
        ](https://sourceforge.net/projects/thinstation/)
    -   [thinstation-general mailing list
        ](http://dir.gmane.org/gmane.network.thinstation.general)
-   [Gentoo Wiki - Diskless Nodes
    ](https://wiki.gentoo.org/wiki/Diskless_nodes)
-   [Diskless Remote Boot in Linux (DRBL)
    ](http://drbl.sourceforge.net/)
    provides a diskless environment for client machines. It is
    compatible with all main linux distribution. _active in 2019_
-   [PiNet](http://pinet.org.uk/)
    allows to managie a classroom set of Raspberry Pis.
-   [Raspberry Pi Thin Client project](http://rpitc.blogspot.com/)
    low price thin client over Raspberry Pi board! Microsoft RDC, Citrix ICA, VMWare
    View, OpenNX & SPICE.
-   [thinclient.org](http://www.thinclient.org/) news
    about thin clients products.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
