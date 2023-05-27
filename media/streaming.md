---
title: Streaming
---

See also {{< iref "ffmpeg" "FFmpeg section" >}},
{{< iref "media_players" "Media Players" >}} for the clients,
{{< iref "codecs" "Codecs" >}}, {{< iref "sound_edit" "Sound Edit" >}},
{{< iref "video_edit" "Video Encoders" >}}.

---

# References
-   Wikipedia {{< wp "Streaming media" >}} and
    {{< wp "List of streaming media systems" >}}.
-   [List of applications/Multimedia - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia) in the sections
    [Audio Players
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Audio),
    [Video players][https://wiki.archlinux.org/title/List_of_applications/Multimedia#Video),
    [Music streaming clients
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Music_streaming_clients),
    [Media Servers
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Media_servers)
-   [Streaming Media With Linux part 1
    ](http://www.linuxdevcenter.com/pub/a/linux/2001/03/23/streaming_media.html)
    and
    [part 2](http://www.linuxdevcenter.com/pub/a/linux/2001/03/30/streaming_linux2.html)
    tutorial on streaming _2001_
-   Music stream directories:
    [Shoutcast](http://www.shoutcast.com/),
    [live365](http://www.live365.com/),
    [Xiph.org](http://dir.xiph.org/),
    [basic.ch](http://www.basic.ch/).


# Sound Servers
-   <a name="esound"></a>{{< wp "ESound" >}}
    the Enlightened Sound Daemon, is a server process that mixes several audio streams
    for playback by a single audio device.  Now _esd_ is largely replaced by
    {{< iref "#pulseaudio" "PulseAudio" >}} or {{< iref "#pipewire" "PipeWire" >}}.
-   <a name="jack"><a>[Jack](http://jackit.sourceforge.net)
    JACK is a low-latency audio server. It can connect a number of different
    applications to an audio device, as well as allowing them to share audio between
    themselves.
    -   Wikipedia {{< wp "JACK Audio Connection Kit" >}}
    -   [ArchWiki: JACK Audio Connection Kit


## PulseAudio {#pulseaudio}
[PulseAudio](http://www.freedesktop.org/wiki/Software/PulseAudio/)
(LGPL library, GPL server) is a a networked sound server, that has support in audacious,
gst (gst-pulse), libao, {{< iref "media_players#mpd" "mpd" >}},
 mplayer, qmmp, xine.... There is an alsa bridge, with which alsa can be both a backend
and a frontend to PulseAudio, through it any alsa player can use PulseAudio.


Wikipedia has a {{< wp "Pulseaudio" >}} page.

-   [Freedesktop PulseAudio Home
    ](http://www.freedesktop.org/wiki/Software/PulseAudio/)
    -   [About PulseAudio
        ](http://www.freedesktop.org/wiki/Software/PulseAudio/About/)
    -   The pulseaudio server setup is described in the
        [PerfectSetup Page
        ](http://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/PerfectSetup/)
    -   [Server Strings
        ](http://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/ServerStrings/)
        to select the server.
    -   [list of modules
        ](http://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/Modules),
    -   [network setup
        ](https://www.freedesktop.org/wiki/Software/PulseAudio/Documentation/User/Network/)
    -   module-cli Command Line Language is described in
        the man page {{< man "pulse-cli-syntax(5)" >}}
-   Wikipedia {{< wp "PulseAudio" >}}
-   Ubuntu has a basic [PulseAudio page](https://wiki.ubuntu.com/PulseAudio),
    note there the importance of `/etc/asound.conf`.
-   [Debian Wiki PulseAudio](https://wiki.debian.org/PulseAudio).
-   [Gentoo Pulseausdio](http://wiki.gentoo.org/wiki/PulseAudio).
-   [ArchWiki: PulseAudio
    ](https://wiki.archlinux.org/index.php/PulseAudio),
    [PulseAudio/Configuration
    ](https://wiki.archlinux.org/index.php/PulseAudio/Configuration),
    [PulseAudio/Examples
    ](https://wiki.archlinux.org/index.php/PulseAudio/Examples),
    [PulseAudio/Troubleshooting
    ](https://wiki.archlinux.org/index.php/PulseAudio/Troubleshooting).
-   [mpd wiki: how to set mpd to use Pulseaudio](https://mpd.fandom.com/wiki/PulseAudio)
-   [Linux MAO PulseAudio
    ](http://www.linuxmao.org/tikiwiki/tiki-index.php?page=PulseAudio)
    (français) translated and adapted for gentoo in
    [proaudio.tuxfamily.org PulseAudio Howto
    ](http://proaudio.tuxfamily.org/wiki/index.php?title=PulseAudio).
-   The utilities in the package pulseaudio-utils are
    [paplay(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=paplay+1),
    [parecord(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=parecord+1),
    [padsp(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=padsp+1),
    [pactl(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pactl+1),
    [pacmd(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pacmd+1),
    [pacat(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pacat+1),
    [pamon(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pamon+1),
    [pax11publish(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pax11publish+1),
    [pasuspender(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pasuspender+1),
-   The gtk utilities are in separate packages:
    [pavucontrol(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pavucontrol+1)
    *PulseAudio Volume Control*,
    [paprefs(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=paprefs+1)
    *PulseAudio Preferences* ,
    [pavumeter(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=pavumeter+1)
    *PulseAudio Volume Meter*,
-   [pamixer](https://github.com/cdemoulins/pamixer)(GPL) and
    [ponymix](https://github.com/falconindy/ponymix) are
    two command line mixers for pulseaudio, but you can also use _amixer_.
-   When the server run in user mode it load the [default.pa - server module config file
    ](https://wiki.archlinux.org/index.php/PulseAudio/Configuration#default.pa)
    in `~/.config/pulse/default.pa`  and  when  that  file  doesn't  exist
    `/etc/pulse/default.pa` to configure modules.
    The same commands can also be entered during runtime  in  the  {{< man "pacmd(1)" >}}
    tool they follow {{< man "pulse-cli-syntax(5)" >}}.
-   [client.conf -  PulseAudio client applications configuration
    ](https://wiki.archlinux.org/index.php/PulseAudio/Configuration#client.conf)
    is used to configure runtime options for individual clients.  It can be used to set
    the configure the default sink and source statically as well as allowing (or
    disallowing) clients to automatically start the server if not currently
    running.<br/> Spanning pulse with the session is disabled by putting `autospawn =
    no`.

    The client read `~/config/pulse/client.conf` and if it does not exists
    `/etc/pulse/client.conf`.  See {{< man "pulse-client.conf(5)" >}} for more
    information
-   [daemon.conf - daemon configuration
    ](https://wiki.archlinux.org/index.php/PulseAudio/Configuration#daemon.conf)
    defines base settings like the default sample rates used by modules, resampling
    methods, realtime scheduling ... . These can not be changed at runtime without
    restarting the PulseAudio daemon.  See the {{< man "pulse-daemon.conf" >}} for
    information.
-   To start manually pulseaudio to debug it, first disable _as above_ and stop the
    autospawned session then start again with `pulseaudio -v` to get info messages,
    `pulseaudio -vv` to also get debugging messages.
-   [pa-applet](https://github.com/fernandotcl/pa-applet)
    is a systray-applet that allows you to control the volume level of the default sink
    and mute or unmute it.  pa-applet is not a replacement to padevchooser and
    pavucontrol, but offer basic functions for regular desktop usage.
-   Pulseaudio can stream to UPnP / DLNA with
    {{< iref "#pulseaudio" "pulseaudio-dlna" >}}.

## PipeWire {#pipewire}
-   [PipeWire / pipewire · GitLab](https://gitlab.freedesktop.org/pipewire/pipewire)
    contains the README top documentation.
-   [PipeWire Wiki - Freedesktop
    ](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/home)
    -   [Migrate PulseAudio
        ](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/Migrate-PulseAudio).
    -   [Virtual devices
        ](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/Virtual-Devices)
-   [PipeWire README
    ](https://gitlab.freedesktop.org/pipewire/pipewire/-/blob/master/README.md)
-   [PipeWire - Debian Wiki](https://wiki.debian.org/PipeWire)
-   [PipeWire - ArchWiki](https://wiki.archlinux.org/index.php/PipeWire),
    [PipeWire/Examples](https://wiki.archlinux.org/title/PipeWire/Examples)
-   [Pipewire - Gentoo Wiki](https://wiki.gentoo.org/wiki/Pipewire#Replacing_PulseAudio)
-   [Fedora Switch to Pipewire](https://fedoraproject.org/wiki/Changes/DefaultPipeWire).
-   [WirePlumber](https://pipewire.pages.freedesktop.org/wireplumber/index.html)
    is a modular session / policy manager for PipeWire and a GObject-based high-level
    library that wraps PipeWire’s API, providing convenience for writing the daemon’s
    modules as well as external tools for managing PipeWire.

The release 3.25 add pw-loopback tool and support module-loopback. pw-loopback
Sends the captured data from a source directly to a sink.

It uses an input and output stream so the source and sink can be moved in pavucontrol,
channel remixing is possible and the volume can be adjusted.

The module loopback and the command `pw-loopback` are
described in pipewire wiki [in the page Migrate-PulseAudio
](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/Migrate-PulseAudio#module-loopback).
Examples of use of pw-looback are in the page [coupled streams virtual devices
](https://gitlab.freedesktop.org/pipewire/pipewire/-/wikis/Virtual-Devices#loopback)

# Streaming renderers
-   [Cortado](http://theora.org/cortado/)   (GPL) is a java streaming applet.
-   [streamripper](http://streamripper.sourceforge.net/) is a
    command-line tool that record MPEG III and OGG  streams. _last
    commit 2010_.
-   <a name="tomahawk"></a>[TomaHawk](https://github.com/tomahawk-player/tomahawk) (GPL)
    _seems abandonned in 2020_
    is a multisource, multi-platform media player.  It can hook via plugins on numerous
    source API, including {{< iref "#ampache" "ampache" >}} and owncloud.


## Gstreamer {#gstreamer}
<a name="gstreamer"></a>[GStreamer (LGPL)](http://gstreamer.freedesktop.org/) is a
streaming-media framework, based on graphs of filters which operate
on media data. Applications using this library can do real-time
sound processing and playing videos. New data types or processing
capabilities can be added by installing new plugins.
The Debian package _gstreamer1.0-tools_ include the basic
command-line tools provided with GStreamer


_Gstreamer_ provides some [Command line tools
](https://gstreamer.freedesktop.org/documentation/tools/index.html)
gst-inspect
:   [gst-inspect-1.0
    ](https://gstreamer.freedesktop.org/documentation/tools/gst-inspect.html)
    print info about a GStreamer plugin. se also
    [using Gstreamer
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/faq/html/chapter-using.html).
ges-launch
:   [ges-launch-1.0
    ](https://gstreamer.freedesktop.org/documentation/tools/ges-launch.html)
    creates a multimedia timeline and plays it back, or renders it to the specified format.
gst-launch
:   [gst-launch(1)
    ](https://gstreamer.freedesktop.org/documentation/tools/gst-launch.html)
    is a tools that builds and runs basic {{< iref "#gstreamer" "GStreamer" >}}
    pipelines it allows playing and transforming sounds and images.
gst-stats
:   A terminal app that shows summary/running stats.
gst-typefind
:   uses  the  GStreamer type finding system to determine the relevant
    GStreamer plugin to parse or decode a file, and the corresponding media type.

They are many clients available, some listed below, but to
experiment with gstreamer you need a command line tool like
[gst123](http://space.twc.de/~stefan/gst123.php).

Gstreamer is appropriate for playing music and converting formats.
The plugins are in the package gstreamer-plugins.

Gstreamer is the basis of numerous applications the following are refered in these
pages:
{{< iref "media_players#audiopreview" "Audiopreview" >}},
{{< iref "media_players#auditive" "Auditive" >}},
{{< iref "media_players#banshee" "Banshee" >}},
{{< iref "media_players#bmpx" "Bmpx" >}} _obsolete_,
{{< iref "media_players#clementine" "Clementine" >}},
{{< iref "#dmapd" "dmapd" >}} DAAP server >}},
{{< iref "media_players#exaile" "Exaile" >}},
{{< iref "media_players#gnash" "gnash" >}},
{{< iref "media_players#guayadeque" "Guayadeque" >}},
{{< iref "sound_edit#jokosher" "Jokosher" >}},
{{< iref "media_players#juk" "Juk" >}},
{{< iref "media_players#kaffeine" "Kaffeine"  >}},
{{< iref "media_players#muine" "Muine" >}},
{{< iref "video_edit#oggconvert" "OggConvert" >}} _obsolete_,
{{< iref "media_players#parlatype" "Parlatype" >}},
{{< iref "video_edit#pitivi" "PiTiVi" >}},
{{< iref "media_players#quodlibet" "Quod Libet" >}},
{{< iref "media_players#rhytmnbox" "RhytmnBox" >}},
{{< iref "#rygel" "Rygel" >}},
{{< iref "sound_edit#soundconverter" "SoundConverter" >}},
{{< iref "media_players#sayonara" "Sayonara" >}},
{{< iref "media_players#strawberry" "Strawberry" >}},
{{< iref "video_edit#thoggen" "Thoggen" >}},
{{< iref "media_players#gnome_videos" "Gnome Videos" >}}

[GStreamer: Applications](https://gstreamer.freedesktop.org/apps/).
is a larger list, but contains some obsolete applications, in [ArchWiki list of
Multimedia applications](https://wiki.archlinux.org/title/List_of_applications/Multimedia)
you find also the [gsteamer based audio players
](https://wiki.archlinux.org/title/List_of_applications/Multimedia#GStreamer-based) and
[video players](https://wiki.archlinux.org/title/List_of_applications/Multimedia#GStreamer-based).

[Gstreamer Documentation](http://gstreamer.freedesktop.org/documentation/):
-   [Gstreamer tutorials
    ](https://gstreamer.freedesktop.org/documentation/tutorials/index.html)
-   [List of all Plug-ins
    ](https://gstreamer.freedesktop.org/documentation/plugins_doc.html),
    [GStreamer Core Plugins Reference
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gstreamer-plugins/html/),
    [GStreamer Base Plugins Reference
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-base-plugins/html/),
    [GStreamer Good Plugins Reference
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-good-plugins/html/),
    [GStreamer Ugly Plugins Reference
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-ugly-plugins/html/),
    [GStreamer Bad Plugins Reference
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-bad-plugins/html/)


# Stream servers {#streamservers}
-   [ArchWiki list of media servers
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Media_servers).

## Music only

-   [AmpJuke](http://www.ampjuke.org/) (GPL) is a PHP+MySQL streaming
    server. _Not updated since 2014_.
-   [Apache MusicIndex](http://www.parisc-linux.org/~varenet/musicindex/)
    is an apache module that allows to display and stream the directory tree of your
    music collection.
-   <a name="cherrymusic"></a>[CherryMusic](https://github.com/devsnd/cherrymusic) (GPL)
    is a music streaming server written in python. It lets you remotely stream, browse
    and manage your music collection. It is intended to be an alternative to streaming
    services like Last.fm, Spotify and Grooveshark.
    -   [ArchWiki - CherryMusic
        ](https://wiki.archlinux.org/index.php/CherryMusic)
-   <a name="groovebasin"></a>[GrooveBasin](https://github.com/andrewrk/groovebasin)
    is a music player server with a web-based user interface. Groove Basin runs on a
    server optionally connected to speakers. Guests can control the music player by
    connecting with a laptop, tablet, or smart phone. Further, users can stream their
    music libraries remotely.
    -   [ArchWiki - GrooveBasin](https://wiki.archlinux.org/index.php/Groovebasin)
-   [litestream](http://litestream.org/ "litestream.org Home") (BSD license)
    is a mp3 streaming server written in C. It is compatible with the shoutcast protocol
    and with muse.
-   {{< iref "media_players#mpd" "Music Player Daemon" >}} has a subsection.
    in the {{< iref "media_players#mpd" "Media Players" >}}.
-   <a name="mopidy"></a>[Mopidy](https://www.mopidy.com/)
    is a music server written in Python.  It can play music from local files, radio
    streams, and cloud services such as Spotify, Google Play Music, and SoundCloud.
    Mopidy is just a server that output Http streams or act as a MPD server.
    -   [Mopidy documentation](https://docs.mopidy.com/)
    -   [GitHub Mopidy](https://github.com/mopidy/mopidy)
-   [MuSE](https://www.dyne.org/software/muse/) <a name="muse"></a> (GPL)
    is a sound streaming server written in C++ that can mix multiple
    sources to stream to the net.  It can encode as mp3 or ogg and
    stream to {{<iref "#icecast" "Icecast" >}}, shoutcast, and darwin. _Last release 2005_
-   [Sonerezh](https://github.com/Sonerezh/sonerezh) (AGPL)
    a php+sql web music server.

### Ampache (AGPL-3.0) {#ampache}
{{< wp "Ampache" >}} is a PHP-based tool for managing, updating and playing
MP3/OGG/RM/FLAC/WMA/M4A files via a web interface. It is implemented with Apache (or any
web server), MySQL, and PHP. It includes a HTML5 Web Player, shoutcast streams; subsonic
(since 3.7), plex (since 3.7), daap(since 3.8), UPnP (since 3.8), webdav (since 3.8)
backends. Ampache can transcode music on the fly.  It can also stream music through a
shoutcast server.

-   [Ampache GitHub Wiki](https://github.com/ampache/ampache/wiki)
-   [Ampache page on wikipedia](http://en.wikipedia.org/wiki/Ampache).
-   [ArchWiki: Ampache](https://wiki.archlinux.org/index.php/Ampache).
-   Ampache web interface can play music by using the Adobe Flash plugin.
    This plugin is to play mp3 encoded sounds at 44 khz sample rate, other formats (ogg,
    or even mp3 48khz) need transcoding.
-   _Ampache_ can  control multiple mpd instances on the network, it is listed in the
    [MPD clients](https://mpd.fandom.com/wiki/Clients)
-   John Goerzen has written two Docker images for _Ampache_,
    [docker-ampache](https://github.com/jgoerzen/docker-ampache) which need an external
    mysql/mariadb server and
    [docker-ampache-mysql](https://github.com/jgoerzen/docker-ampache-mysql)
    which provides an internal an embedded MariaDB server.

#### Ampache clients.
-   By [enabling ampache API](https://github.com/ampache/ampache/wiki/API).
    you can also set Ampache as [UpNP/DLNA Server
    ](https://github.com/ampache/ampache/wiki/API#upnp--dlna-api)
    and use {{< iref "#upnp_media_clients" "any UpNP client" >}}.
-   [The DAAP API](https://github.com/ampache/ampache/wiki/API#daap-api)
    allow the use of {{< iref "#daap clients" "DAAP Clients" >}}.
-   [Subsonic API](https://github.com/ampache/ampache/wiki/subsonic)
    gives access to many clients, as there are many subsonic clients for android, ios,
    windows, MacOS, and Linux.
-   [Webdav API](https://github.com/ampache/ampache/wiki/API#webdav-api) gives acces to
    ampache through webdav, allowing to use potentially any music player, either by
    using webdav in the client, or mounting webdav with fuse.
-   [Ampache Wiki: Clients](https://github.com/ampache/ampache/wiki/Clients).
-   Some players can interface to ampache through the XML api you can find
    a [list on Ampache wiki](https://github.com/ampache/ampache/wiki/client-api), like:
    {{< iref "media_players#mpd" "mpd" >}},
    {{< iref "media_players#vlc" "VideoLan Client (VLC)" >}}
    _for playlist only, not the xml api_,
    {{< iref "media_players#amarok" "Amarok" >}} or
    {{< iref "media_players#clementine" "Clementine" >}},
    {{< iref "#tomahawk" "Tomahawk" >}},
    {{< iref "media_players#rhythmbox" "Rhythmbox" >}}
    can play ampache streams through a plugin,
-   [Viridian](http://viridian.daveeddy.com/) (BSD 3-clause license)
    is a python/pygtk ampache client.
-   [Ampyche](https://github.com/tych0/ampyche)
    ([Beerware License](http://people.freebsd.org/~phk/))
    by Tycho Andersen is a python "binding" for the ampache API.
-   [GitHub - ampache-xbmc-plugin](https://github.com/ampache/ampache-xbmc-plugin)
    KODI plugin for Ampache.

#### android clients for ampache
More on ampache wiki, you can also use android clients for subsonic, UpNP/DLNA, DAAP if
you have enabled these API.
_
-   [GitHub - meandor/ampdroid](https://github.com/meandor/ampdroid) (MIT license)
    by Daniel Schruhl, there is also an other repository:
    [4phun/ampdroid](https://github.com/4phun/amproid) (GPL-3.0) this last is on
    [Amproid on Google Play
    ](https://play.google.com/store/apps/details?id=com.pppphun.amproid),
-   [justplayer
    ](https://play.google.com/store/apps/details?id=jp.co.kayo.android.localplayer)
    last release 2015, no longer developped in the [Bitbucket repository
    ](https://bitbucket.org/yokmama/just-player/).
-   [reactive-ampache · GitLab](https://gitlab.com/antoniotari/reactive-ampache/) or
    (GPL v3.0) [named power-ampache on f-droid
    ](https://f-droid.org/en/packages/com.antoniotari.reactiveampacheapp/).


## Video and Music
### Icecast {#icecast}
{{< wp "Icecast" >}} (GPL)is a streaming server (audio/video) with support of Ogg/Vorbis
and Ogg/Theora, Opus, WebM and MP3 streams. Icecast is in Debian.
Icecast has tiny memory footprints.
-   [Icecast Home](http://www.icecast.org/)
-   [Icecast official documentation](http://icecast.org/docs/icecast-latest)
-   [Icecast 3rd Party Applications](http://icecast.org/apps/)
    Source Clients, Mediaplayers that support Icecast streams,
-   [ArchWiki - Icecast](https://wiki.archlinux.org/index.php/Icecast).
-   [tunapie](http://tunapie.sourceforge.net/documentation.html) (LGPL-2.0)
    is a GUI based program for displaying Shoutcast or Icecast video and radio
    streams. It gives information about streams including bitrate, IP and current
    number of listeners. Streams can then be played using a favorite media player,
    or recorded using streamripper. It is in Debian.

### Icecast source clients
-    [official list of source clients](http://icecast.org/apps/) contains approximately
    twenty five clients.
-   _Icecast_ can be used to [stream from MPD
    ](https://wiki.archlinux.org/index.php/Icecast#Streaming_with_MPD),
    but {{< iref "media_players#MPD" "MPD" >}}
    has its [own HTTP streaming server
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Tips_and_tricks#HTTP_streaming).
-   [Ezstream](https://icecast.org/ezstream/)
    is a command line source client for Icecast media streaming servers that streams
    files without reencoding. It supports mp3, WebM, and Matroska streams. _Ezstream_ is
    in Debian.
    It is tiny 1.5M resident on my armel nas.
-   [DarkIce](http://www.darkice.org/)
    is a  live audio streamer, It records audio from an audio interface
    (e.g. sound card), encodes it and sends it to a streaming server. It supports
    encoding in mp3, ogg vorbis, AAC, Opus.
    -   [DarkIce - GitHub](https://github.com/rafael2k/darkice)
    -   Darkice can be controlled from
        [darksnow](https://darksnow.radiolivre.org/index.en.html)
        GTK-2 gui interface.

    Darkice and Darksnow are packaged in Debian.
-   [GlassCoder](https://github.com/ElvishArtisan/GlassCoder) (GPL-2.0)
    is a minimalist audio encoder for IceCast and Shoutcast as well as HTTP Live
    Streaming (HLS). It can stream from ALSA, Jack, and files.
    It is in Debian as well as the gui _glassgui_.
    -{{< iref "#gstreamer" "Gstreamer" >}} with the plugin [shout2send
    ](https://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-good/html/gst-plugins-good-plugins-shout2send.html)
    pushes a media stream to an icecast server.

Some media players like  {{< iref "media_players#mpd" "MPD" >}},
{{< iref "media_players#qmmp" "Qmmp" >}}  can output to icecast.

### Jinzora {#jinzora}
<a name="jinzora"></a>[Jinzora](https://sourceforge.net/projects/jinzora/) (GPL)
is a Web-based media streamer and local Media Jukebox. It can play numerous audio and
video formats Jinzora is a quite powerful system, but the administrative interface is
not easy to use. _Jinzora last release was in 2011 with only maintenance commits in
2014._
-   [ArchWiki - Jinzora](https://wiki.archlinux.org/index.php/Jinzora)

## Live.com
[LIVE.COM](http://www.live555.com/mediaServer/) (LGPL)
is a source-code C++ library for standards-based RTP/RTCP/RTSP/SIP multimedia
streaming, suitable for embedded and/or low-cost streaming applications. It is used
by the following applications:
-   [openRTSP](http://www.live555.com/openRTSP/) a command-line RTSP client
-   [playSIP](http://www.live555.com/playSIP/) - a command-line SIP session
    recorder.
-   [live555 MediaServer](http://www.live555.com/mediaServer/)
    is a complete RTSP server application. It can stream mpeg 1, 2, 4
    or aac. You can use openRTSP, vlc, or mplayer as client.
-   [RTSP/RTP streaming support](http://www.live555.com/mplayer/)
    for the "MPlayer" media player
-   [vobStreamer](http://www.live555.com/vobStreamer/)
    A network DVD player that allows to stream your DVD content over a LAN.

## Red5
[Red5 Server](https://github.com/Red5/red5-server)
s an Open Source Flash Server written in Java that supports:

-   Streaming Video (FLV, F4V, MP4, 3GP)
-   Streaming Audio (MP3, F4A, M4A, AAC)
-   Recording Client Streams (FLV and AVC+AAC in FLV container)
-   Shared Objects
-   Live Stream Publishing
-   Remoting
-   Protocols: RTMP, RTMPT, RTMPS, and RTMPE


## Subsonic and forks {#subsonic}
[Subsonic](http://www.subsonic.org/) (closed source, previously GPL)
is a streaming server written in Java.  _Subsonic_ supports any streamable media
(including MP3, AAC, and Ogg) with on-the-fly media conversion. Subsonic was no
longer open source until version 6.  Some features like
DLNA/UPnP compatibility, are only available in the private source _Subsonic Premium_
that costs 12 $/year.
-   [ArchWiki: Subsonic](https://wiki.archlinux.org/index.php/Subsonic).
-   [Subsonic Apps](http://www.subsonic.org/pages/apps.jsp) list subsonic clients.
-   [SubFirePlayer](http://www.subfireplayer.net/)
    is a pure HTML5 audio player for SubSonic, implemented in JQueryMobile. It is
    available as a web application, as a Chrome hosted app, and as appli for devices
    including well as Android and the Kindle Fire HD.
-  [Jamstash](https://github.com/tsquillario/Jamstash)
   is an HTML5 Music Streamer for SubSonic.
    -   [Jamstash online site](http://jamstash.com/)

-   [madsonic](http://www.madsonic.org/) (closed source, previously GPL)
    a java fork of Subsonic that adds features and bug fixes over the main branch.

    Like _Subsonic_ _Madsonic_ was opensource until version 6.  It introduce some extra
    features listed in the comparison page.

    Madsonic has now introduced a private source _premium_ version. Only _Madsonic
    Premium_ has support for UPnP/DLNA and Chromecast.  There are Premium plans from 24
    $/y to 40 $/y. It is still flagged as open source under GPL, but the source code
    don't seem available.

-   [Airsonic](https://airsonic.github.io/) (GPL)
    is a java media server, fork of Subsonic and Libresonic. _Airsonic_
    streams any audio or video format that can stream over HTTP, for instance AAC
    and OGG, and can transcode other formats.
    -   [airsonic - GitHub](https://github.com/airsonic/airsonic/)
        active in 2021.
    -   [Documentation - Airsonic](https://airsonic.github.io/docs/)

-   [Supysonic](https://github.com/spl0k/supysonic) (GPL)
    a Python implementation of the Subsonic server API. _active in 2021_.

-   {{< iref "media_players#videolan" "VideoLan Client (VLC)" >}} is in the
    {{< iref "media_players#video_players" "Video Players section" >}}.


# UPnP / DLNA

This section is about {{< wp "Universal Plug and Play" >}} UPnP which allows
device-to-device networking of appliances, I uses the TCP/IP, UDP and
HTTP protocols and supports zero configuration networking see the
{{< wp "Universal Plug and Play"  "wikipedia page for more info" >}}.

When talking of UPnP we should distinguish, the
{{< wp "Internet Gateway Device Protocol" >}} (IGD) which is a method of
automatically configuring port forwarding to allow {{< wp "NAT traversal" >}};
and broadcasting of digital media which is used by {{< wp "DLNA" >}} devices.

-   Wikipedia: {{< wp "Universal Plug and Play" >}},
    {{< wp "Internet Gateway Device Protocol" >}}, {{< wp "DLNA" >}}.
-   [DLNA Home Page](https://www.dlna.org/)
-   [Complete Guide to wifi - UPnP DLNA Network Audio
    ](https://www.computeraudiophile.com/ca/ca-academy/the-complete-guide-to-hifi-upnp-dlna-network-audio/)
-   [Open Connectivity - UPnP standards & architecture
    ][https://openconnectivity.org/developer/specifications/upnp-resources/upnp)

## UPnP Media servers {#upnp_servers}
-   Wikipedia:
    {{< wp "Comparison of UPnP AV media servers" >}},
    {{< wp "List of UPnP AV media servers and clients" >}}
-   [BRisa](http://brisa.garage.maemo.org/) is an UPnP framework written
    in Python. It provides a Media Server and Media Renderer to play medias,
    and a Media Applet to start/stop media servers/renderers. _no
    longer active_
-   <a name="coherence"></a>[Coherence](https://github.com/coherence-project/Coherence)
    (MIT License) was an UPnP/DLNA Framework that provides a
    server. Coherence developper resigned, and the development ceased
    in 2014, but there are some maintenance commits in the repository that merge the
    change made by  {{< iref "#cohen" "Cohen" >}} a fork of
    _Coherence_
    -   [Github: Coherence
        ](https://github.com/coherence-project/Coherence)
        record the last state of the abandonned Coherence project.
-   <a name="cohen"></a>[Cohen](https://cohen.readthedocs.io/en/latest/) (MIT License).
    -   [Github: Cohen](https://github.com/unintended/Cohen).
    -   [Cohen manual](https://cohen.readthedocs.org/en/latest/)
    -   [Cohen](https://pypi.python.org/pypi/Cohen) is on Pypi.
-   <a name="emby"></a>[Emby](https://emby.media/) (GPL)
    is an personal media server written in C#. It has clients for many platforms like
    html5 server, android, ipad, windows and many more. It is used to organize personal
    home media, as well as play back on other devices. It supports DLNA and can send to
    chromecast.
    Emby provides Debian packages for amd64 and armhf.

    The [GitHub repository](https://github.com/MediaBrowser/Emby) is no more updated
    since 2018 version 3.5.2, As of version 3.5.3 Emby has been relicensed and is now
    closed-source, {{< iref "#jellyfin" "Jellyfin" >}} is an open source fork.
-   [FreeMi](http://freemiupnp.fr/) (Open Source License)
    FreeMi is an C#/Mono UPnP Media Server audio/video for the FreeBox.
    the CLI can be used on Linux.
-   [Fuppes](https://github.com/u-voelkel/fuppes) (GPL)
    is an UPnP A/V MediaServer (not yet fully UPnP compliant).  It supports on-the-fly
    transcoding from ogg/vorbis, musepack/mpc, FLAC and AAC/MP4 to mp3, mp2, wav or pcm,
    image conversion/rescaling and video transcoding.
    -   [Fuppes sourceforge Page](http://sourceforge.net/projects/fuppes/).
-   <a name="jellyfin"></a>[Jellyfin](https://jellyfin.org/) (GPL)
    is an open source fork of {{< iref "#emby " "Emby">}}.

    It is an personal media server written in C#. It has clients for many platforms like
    html5 server, android, ipad, windows and many more. It is used to organize personal
    home media, as well as play back on other devices. It supports DLNA and can send to
    chromecast. Jellyfin has clients for Desktop linux amd-64, MacOs, Windows; Android,
    ios, IpadOs, Webos, Kodi plugin, Roku plugin, {{< iref "#mopidy" "Mopidy" >}}
    extension. It has also a set of plugins listed below.

    -   Wikipedia: {{< wp "Jellyfin" >}}.
    -   [Jellyfin Documentation](https://jellyfin.org/docs/)
    -   [Plugins | Jellyfin
        ](https://jellyfin.org/docs/general/server/plugins/index.html)a
    -   [Jellyfin - GitHub](https://github.com/jellyfin/jellyfin)
-   <a name="gerbera"></a>[Gerbera](https://gerbera.io/)  (GPL)
    is an upnp media server written in C++, the continuation of
   [MediaTomb](https://sourceforge.net/projects/mediatomb/)
    which is no longer maintained since 2010. It allows transcoding via plugins and
    scripts.  It is active in 2021 and packaged in Debian.
    -   [Gerbera Documention](http://docs.gerbera.io/en/latest/).
    -   [GitHub - Gerbera](https://github.com/gerbera/gerbera).
-   {{< iref "media_players#mythtv" "MythTV" >}}
    has a [builtin UPnP server](https://www.mythtv.org/wiki/UPnP).
-   <a name="pulseaudio-dlna"></a>__Pulseaudio-DLNA__ (GPL-3.0)
    is a lightweight streaming server which brings DLNA / UPNP and Chromecast support to
    PulseAudio. It can stream your current PulseAudio playback to different UPNP devices
    (UPNP Media Renderers) or Chromecasts in your network.
    It is packaged in Debian.
    -   [GitHub - masmu/pulseaudio-dlna](https://github.com/masmu/pulseaudio-dlna)
        The repository of the author of pulseaudio DLNA, no longer maintained since 2018, still in
        python 2.
    -   [GitHub - joecksma/pulseaudio-dlna](https://github.com/joecksma/pulseaudio-dlna)
        python 3 fork on which are based the recent debian packages.
    -   [How to stream audio to chromecast or dlna / upnp device using pulseaudio-dnla
        ](http://www.webupd8.org/2016/03/how-to-stream-audio-to-chromecast-or.html)
    -   [How To Use pulseaudio-dlna To Stream Audio To Chromecast Devices
        ](https://www.linuxuprising.com/2020/10/how-to-use-pulseaudio-dlna-to-stream.html)
-   [ReadyMedia previously MiniDLNA](http://sourceforge.net/projects/minidlna/) (GPL)
    is server software with the aim of being fully compliant with DLNA/UPnP-AV
    clients. It is developed by a NETGEAR employee for the ReadyNAS product
    line. _active in 2020_
    -   [ReadyMedia git repository
        ](https://sourceforge.net/p/minidlna/git/ci/master/tree/)
    -   [ReadyMedia news
        ](http://sourceforge.net/p/minidlna/git/ci/master/tree/NEWS)
    -   [Webmin plugin for miniDLNA
        ](http://sourceforge.net/projects/minidlnawebmin/)

    _ReadyMedia_ is a tiny server on an arm v6 I have footprint of 2 MB and on an arm64 7MB
    resident / 3M shared.
-   [Universal Media Sever](http://www.universalmediaserver.com/) (GPL-2.0)
    is a  Java UpNP server which was forked and is the continuation of
    [PS3 Media Server]((https://github.com/ps3mediaserver/ps3mediaserver), which is not
    maintained since 2016.

    It allows transcoding using
    FFmpeg, MediaInfo, OpenSubtitles, Crowdin, MEncoder, tsMuxeR, AviSynth, VLC.
    It has support for Chromecast. The site gives a
    [comparaison of features](http://www.universalmediaserver.com/comparison/)
    with _PS3 Media server_, _Serviio_, _KooRaRoo_, _Plex_.

    _It is a very active project in 2021._
-   [uShare _GeexBox page_](http://ushare.geexbox.org/) (GPL)
    is an Upnp (TM) A/V Media Server based on <a name="gmediaserver"></a>[GMediaServer
    ](http://www.gnu.org/software/gmediaserver/) which is no longer maintained since
    2007.

    _uShare_ itself does not seem to be active since 2010.
-   {{< iref "media_players#kodi" >}}
    has a [builtin UPnP server](https://kodi.wiki/view/UPnP).

### Rygel {#rygel}
[Rygel](https://wiki.gnome.org/action/show/Projects/Rygel)
is an UPnP AV MediaServer, It stick to a strict conformance to DNLA, and provide on the
fly conversion of media.

Media players may use Rygel to become a MediaRenderer through the Playbin plugin.  It
can then be controlled remotely by a UPnP or DLNA Controller.

_Rygel_ is in debian, the renderer plugin is in _rygel-playbin_, `rygel-gst-launch` is a
gst-launch plugin that enables using a a DLNA service/UPnP device in a gst pipeline; and
a configuration gui in _rygel-preferences_.

_rygel_, _rygel-playbin_, and several plugins are in Debian.

Rygel with the playbin plugin takes on amd64 47M res / 17M shr on may 2018 for rygel
0.36.1, when playing a TV stream I got 56M / 26M.

-   [ArchWiki: Rygel](https://wiki.archlinux.org/index.php/Rygel)
-   [Rygel.conf man page
    ](http://rygel-project.org/doc/latest/rygel.conf.html)
-   [Rygel Wiki](https://wiki.gnome.org/Projects/Rygel)
-   [Rygel FAQ](https://wiki.gnome.org/Projects/Rygel/FAQ)
-   [Rygel Wiki -  stream audio to DLNA / UPnP devices using Rygel
    ](https://wiki.gnome.org/Projects/Rygel/Pulseaudio)

#### Rygel Features {#rygel_Features}
Taken from the [Rygel Wiki - features
](https://wiki.gnome.org/Projects/Rygel/Features)

-   Export of on-disk media via [Tracker](https://wiki.gnome.org/Projects/Tracker)
    or media-export
    [server plugins](https://wiki.gnome.org/Projects/Rygel/ServerPlugins).
-   Export of online media from
    [2nd German TV station](http://www.zdf.de/).
-   Export of media hierarchies provided by external applications
    through implementation of
    [D-Bus MediaServer spec](https://wiki.gnome.org/Projects/Rygel/MediaServer2Spec).
    Applications that utilize this feature are:

    -   [DVB Daemon](https://wiki.gnome.org/Projects/DVBDaemon):
        Provides live TV (DVB) channel streams.
    -   {{< iref "media_players#rythmbox" "Rhythmbox" >}}.
    -   {{< iref "#pulseaudio" "PulseAudio" >}}.
    -   [GRILO](https://wiki.gnome.org/Projects/Grilo)
        a framework focused on making media discovery and browsing easy, used with Rygel
        and  {{< iref "media_players#totem" "Totem" >}}.

-   Export of GStreamer pipelines as media items on the network, specified through
    gst-launch syntax in the user configuration.
-   Audio and Video Transcoding when using
    [Rygel's GStreamer media engine](https://wiki.gnome.org/Projects/Rygel/MediaEngines).
-   Standalone MediaRenderer plugin based on [GStreamer playbin
    ](http://gstreamer.freedesktop.org/data/doc/gstreamer/head/gst-plugins-base-plugins/html/gst-plugins-base-plugins-playbin.html){.http}
    element.
-   Export of media players that implement
    {{< iref "media_players#mpris" "Mpris specification" >}} D-Bus interface,
    as MediaRenderer devices.

## UPnP media renderers (clients): {#upnp_media_clients}

-   {{< wp "List_of_UPnP_AV_media_servers_and_clients#UPnP_AV_clients" "Wikipedia list of UPnP clients" >}}.
-   [djmount](http://djmount.sourceforge.net/) (GPL)
    is an UPnP AV client. It mounts as a Linux filesystem the media content of
    compatible UPnP AV devices. _djmount devellopement on sourceforge stopped in 2006,
    it was in debian until stretch._

    A newer fork of _djmount_ is [djmount - GitHub](https://github.com/mwilck/djmount/),
    this fork has several fixes including the transition from libupnp3 to libupnp6.
    _This fork has no commit since 2017 (checked in 2021)_.
-   [eezpnp](http://www.eezupnp.de/) (Free but not open source ?)
    is a control point written in Java.
-   [gmrender-resurrect](https://github.com/hzeller/gmrender-resurrect)  (GPL)
    is an UPnP media renderer for Linux, It provides UPnP controllers to render media
    content from a UPnP media server.  It is a fork of
    [GMediaRender](http://gmrender.nongnu.org/) which was no longer maintained
    since 2007.  _gmrender-resurrect_ is in the Debian package _gmediarender_, _it is
    active in 2021_.
-   _rygel-playbin_ is a media renderer par of the {{< iref "#rygel" "Rygel" >}}
    upnp media server.
-   [simple-dlna-browser
    ](https://github.com/javier-lopez/learn/blob/master/sh/tools/simple-dlna-browser)
    is a simple shell script to browse dlna servers.

## Media Players with Upnp support
These streaming server acts as  UPnP media renderers.

-   {{< iref "media_players#amarok" "Amarok" >}}
    can [play UPnP / DLNA streams
    ](https://userbase.kde.org/Amarok/Manual/Organization/Collection/RemoteCollections/UPnP)
    this feature is not shared by the Clementine or Exaile forks.
-   {{< iref "media_players#banshee" "Banshee" >}} a mono  player.
-   {{< iref "media_players#kodi" "Kodi (Xbmc)" >}}
    can [act as an UPnP client](https://kodi.wiki/view/UPnP)
    that can be controlled by an UPnP control point.
-   {{< iref "media_players#mpd" "MPD" >}} can natively read UPnP streams on the local
    network with the native upnp plugin but there is also a frontend to serve UPnP
    content _upmdcli_.  The difference between the two approaches are described in
    [Libupnpp, Upmpdcli and Sc2mpd Documentation
    ](https://www.lesbonscomptes.com/upmpdcli/pages/docs.html)
    -   [upmpdcli](https://www.lesbonscomptes.com/upmpdcli/) (GPL)
        is a UPnP Media Renderer front-end for MPD written in C++, It supports UPnP
        gapless track transitions and the OpenHome Media services (including a Radio
        service to listen to Internet streams).
    -   [Upmpdcli downloads](https://www.lesbonscomptes.com/upmpdcli/downloads.html).
-   {{< iref "media_players#rhythmbox" "Rhythmbox" >}} can play UPnP medias, and DAAP
    via a plugin which uses _libdmapsharing_.
-   {{< iref "media_players#totem" "Totem" >}} has a [DLNA plugins
    ](https://help.gnome.org/users/totem/stable/totem-plugins.html.en#totem-plugins-coherence)
    for {{< iref "#coherence" "coherence project" >}} or
    {{<  iref "#cohen"  "cohen" >}} which allows it to work as UPnP media client.
-   {{< iref "media_players#vlc" "VLC" >}} can play UPnP medias since 1.2.0 release.
-   {{< iref "media_players#kodi" "Kodi" >}} can play UPnP medias.

## Hardware including an UPNP renderer

-   [List of MythTV UPnP clients
    ](https://www.mythtv.org/wiki/UPnP_Client_Info) both hardware and
    software.


## UpNP control point
A control point, functions as a digital audio/video remote control. Control points
automatically detect UPnP servers on the network to browse content directories and
request the transfer or streaming of media. A UPnP media renderer performs the actual
audio or video rendering. Control points and media renderers most commonly run on
separate devices, the control point being for example a tablet, and the renderer a
television or a networked audio computer connected to an audio receiver. Some control
points integrate a media renderer and may function as a complete music playing
application.


-   <a name="gupnp"></a>[GUPnP](https://wiki.gnome.org/Projects/GUPnP)
    is a framework for creating UPnP devices and control points.  _GUPnP-Tools_ is a set
    of utilities to work with UPnP. It includes an AV control point `gupnp-av-cp`, a
    Generic Control Point `gnupnp-universal-cp` an uploader `gupnp-upload` and a
    {{< wp "Simple Service Discovery Protocol" >}} (SSDP) commandline client.
    `gssdp-discover`. _GUPnP-Tools is in Debian._

    On amd64 _gupnp-av-cp_ takes 25 res / 17M shr on may 2018 for gupnp-tools 0.8.14.

-   [upplay](https://www.lesbonscomptes.com/upplay/) (GPL)
    is a desktop UPnP audio Control Point written in C++ for Linux/Unix and MS
    Windows. A _Debian_ package repository is provided. On amd64 upplay takes 53M res /
    35M shr on may 2018 for 1.2.11, which is very heavy for a control point.

-   {{< iref "media_players#kodi" "Kodi" >}}
    can  [act as an UPnP Control Point](https://kodi.wiki/view/UPnP/Client).

### Android and IOS control points and renderers
More control points and server are in the
[Wikipedia page List of UPnP control points and player software
](https://en.wikipedia.org/wiki/List_of_UPnP_AV_media_servers_and_clients#UPnP_control_points_and_player_software).

-   _BubbleUPnP_ is a DLNA Server, Controller and Renderer for Android.
-   _Gizmoot_ is a free Android UPnP AV Control Point and Renderer.
-   _Kinsky_ is an open source UPnP control point for iPod/iPhone, iPad,
    Windows, macOS, Linux, Android and PocketPC.
-   _MediaSteersman_ is a free UPnP control point for Android tablets
    with included UPnP renderer and server functionality.
-   _Pixel Media Controller_ is a free DLNA compliant Digital Media
    Controller on Android.
-   [PlugPlayer](https://en.wikipedia.org/wiki/PlugPlayer)
    is a cross-platform UPnP client, Media Renderer, Media Server and
    control point available for iPod/iPhone, iPad, Android, Google TV
    and macOS.

## UPnP IGD client/server

-   [MiniUPnP Project](http://miniupnp.free.fr/) includes a UPnP IGD
    server and a library and client to control UPnP IGD devices.
    _active in 2018_
    -   [GitHub _ MiniUPnP](https://github.com/miniupnp/miniupnp).

## DAAP {#daap}
-   The {{< wp "Digital Audio Access Protocol" >}} (DAAP) is a proprietary
    protocol by Apple that does the same job than UPnP but being
    proprietary. As Itunes is quite popular, it is widespread, so
    there are also opensource software to play DAAP.  DAAP is also
    used by {{< wp "Roku" >}} products.

### DAAP Clients {#daap_clients}
-   a DAAP client _i.e. players_ os [on Wikipedia - DAAP Clients
    ](https://en.wikipedia.org/wiki/Digital_Audio_Access_Protocol#DAAP_clients).

    They include: {{< iref "media_players#rhythmbox" "Rhythmbox" >}},
    {{< iref "media_players#amarok" "Amarok" >}},
    {{< iref "media_players#exaile" "Exaile" >}}
    {{< iref "media_players#exaile" "Banshee" >}},
    {{< iref "media_players#kodi" "Kodi" >}}.

### DAAP Servers
-   [Wikipedia list of DAAP servers
    ](https://en.wikipedia.org/wiki/Digital_Audio_Access_Protocol#DAAP_servers)
-   <a name="owntone"></a>[owntone server](https://github.com/owntone/owntone-server)
    (GPL) previously __Forked-daapd__ is a fork by E.Jurgensen of the the _forked-daapd_
    originally written by Julien Blache whose development stopped in 2012, which was
    itself a fork of{{< iref "#firefly" "Firefly" >}}.

    _Owntone_ is a daemon which serve your music library with the DAAP protocol,
    the MPD protocol, and the RSP protocol used by {{< wp "Roku" >}} devices.

    _Owntone_ can output through DAAP clients, {{< wp "Itunes" >}} clients like
    _Apple Remote_, MPD Clients, Airplay or Chromecast devices _audio only_,
    the computer sound card with alsa, or PulseAudio, or to an http mp3 stream.

    _Owntone_ can transcode a stream with ffmpeg, when the format is not understood by
    the client. It also supports  M3U and PLS playlists.

    _forked-daapd_ is in Debian.

    -   [owntone server - Raspberry Pi Forums
        ](https://www.raspberrypi.org/forums/viewtopic.php?t=49928)
        E. Jurgensen proposes a Raspbian repository for _Owntone_.

-   [canary](http://code.woong.org/canary)
    is a DAAP server written in Node js.
    -   [canary - GitHub](https://github.com/mycoboco/canary)
_   <a name="dmapd"></a>[dmapd](https://www.flyn.org/projects/dmapd/)
    is a DAAP and DPAP server with realtime transcoding, it uses
    {{< iref "#gstreamer" "GStreamer" >}}, and as been used on small OpenWrt servers.
-   {{< iref "#ampache" "Ampache" >}} provides a
    [DAAP API](https://sourceforge.net/p/ampache4/wiki/API/)
    allowing it to be used as a DAAP server.
-   [spydaap](https://github.com/egh/spydaap)
    is a media server supporting the DAAP protocol written in Python
    that  uses the mutagen media metadata library. _not updated since 2011_
    _spydaap_ can stream mp3s, ogg, flac, and Quicktime videos. It is used in an
    {{< iref "media_players#exaile" "Exaile" >}} plugin.
-   <a name="firefly"></a> {{< wp "Firefly" >}} (GPL), previously _mnt-daap_
    is an open-source media server (or daemon) for the {{< wp "Roku" >}} Server Protocol
    (RSP) and Digital Audio Access Protocol (DAAP). It is abandoned since 2008.
    Two clients were targeted specifically to Firefly:
    -   [Firefly client](http://sourceforge.net/projects/fireflyclient/)
        was a java client and a java client applet to Firefly media
        server. _last release 2008_
    -   [FirePlay](https://sourceforge.net/projects/fireplay/)
        A flash based client. _Last release 2010._

# Chromecast {#chromecast}
{{< wp "Chromecast" >}} are digitals players by Google. They can display video
up to 1080p for second generation and 4K ultra HD for Chromecast
ultra.

They [support the following codecs
](https://developers.google.com/cast/docs/media):
-   Image formats, BMP, GIF, JPEG, PNG, WEBP
-   Media container formats: AAC, MP3, MP4, WAV, WebM
-   Video codecs (CCast 1st and 2nd Gen.): H.264 High Profile <= level
    4.1, VP8. (Ccast ultra) HEVC / H.265 Main and Main10 Profiles <=
    level 5.1 (2160p/60fps), VP9 Profile 0 and Profile 2 <= level 5.1
    (2160p/60fps)
-   Audio codecs: HE-AAC, LC-AAC, MP3, Vorbis, WAV (LPCM),
    FLAC (up to 96kHz/24-bit), Opus.

The cast protocol {{< wp "Google Cast" >}} is a proprietary protocol. There is
a SDK to allow applications to interract with Chromecat devices
and on  {{< wp "Google_Cast#Compatible_devices"  "Compatible devices" >}} which
include android TV and many sounbars and speakers.
A list of these devices is in the Google help page
[Chromecast built-in](https://www.google.com/chromecast/built-in).

On Wikipedia you find a {{< wp "List of apps with Google Cast support" >}}.

Google Chromecast Help
](https://support.google.com/chromecast/chromecast/).



## Casting a chrome tab or the desktop screen

In Chrome’s menu on the right side of the window and select “Cast”, or
right-click the current page and select “Cast”.

Then you can choose if you want to cast a tab or the fulldesktop, and
the chromecast receiver you want to use.

The Google Cast extension was only needed with older releases of
Chrome.


## Casting an audio or video file or url {#casting_apps}
-   [Mkchromecast](http://mkchromecast.com/)
    is a python application to cast a file to  Google Cast devices or Sonos speakers.
    It can play any sound that you can send to pulseaudio using
    _parec_, it can also use
    _ffmpeg_ or _avconv_ to play a file or an url.
    It has a Linux deb
    package, that you can find also in Debian.
    -   [GitHub - Mkchromecast
        ](https://github.com/muammar/mkchromecast)
    -   _pulsaudio_ can be replaced with alsa, see
        [Alsa support
        ](https://github.com/muammar/mkchromecast/wiki/ALSA)
-   [GitHub - gnomecast](https://github.com/keredson/gnomecast).
    is a GUI for casting a video file it can transcode any unsupported
    format that _ffmpeg_ accept, and has support for subtitle.
-   [GitHub - skorokithakis/catt](https://github.com/skorokithakis/catt)
    (BSD License)
    a python CLI to cast videos local or remote, or websites.
    It can cast any source [supported by youtube-dl
    ](http://rg3.github.io/youtube-dl/supportedsites.html).
    It has support for local or remote subtitle.
    There are commands to pause, resume, seek to some time, change
    volume of the current video played by chromecast.
-   [castnow](https://github.com/xat/castnow) (MIT Licence)
    is a node CLI to cast a local file or an URL.
    The author and maintainer step down in 2017 and is seeking a
    new maintainer.
-   Pulseaudio can stream to Chromecast ( and UPnP / DLNA) with
    {{< iref "#pulseaudio" "pulseaudio-dlna" >}}
    streaming server.
-   [Transformer votre Raspberry Pi en Chromecast
    ](https://www.supinfo.com/articles/single/7029--transformer-votre-raspberry-pi-chromecast).


## Chromecast libraries

-   [Pychromecast](https://github.com/balloob/pychromecast)
    (MIT License)
    is a Python 3 library communicate with the Google Chromecast.
    It is used by [Home Assistant](https://www.home-assistant.io/).
-   [lanceseidman/PiCAST](https://github.com/lanceseidman/PiCAST/)
    make a raspberry pi like Chromecast.
    -    [PiCast overview
        ](http://compulsivetech.biz/lance/2014/02/picast-2-0-make-a-raspberry-pi-like-chromecast-easier/).


## Chromecast support in media players
Some media players have built-in support for Chromecast like
{{< iref "media_players#vlc" "VLC" >}},
{{< iref "media_players#smplayer" "SMPlayer" >}},
{{< iref "media_players#emby" "Emby" >}}.

Other players that use pulseaudio as output device can use
{{< iref "#pulseaudio-dlna" "pulseaudio-dlna" >}} or
{{< iref "#mkchromecast" "mkchromecast" >}}
this can be used for instance with mpd, mpv, mplayer2, ffmpeg.

When a player can output to http we can also send this URL to
chromecast with many applications {{< iref "#casting_apps" "referenced above" >}}.
This can be used with mpd, or {{<iref "#icecast" "Icecast" >}}.

# Miracast {#miracast}
{{< wp "Miracast" >}} Miracast is a standard for wireless connections from sending
devices to display receivers launched by the  Wi-Fi Alliance. It can roughly be
described as "HDMI over Wi-Fi" using the peer-to-peer Wi-Fi Direct standard.

-   [MiracleCast](https://github.com/albfan/miraclecast) (LGPL)
    MiracleCast implements the Display-Source as well as Display-Sink side.

    The Display-Source side allows you to connect external displays to your system and
    stream local content to the device.

    The Display-Sink side allows you to create wifi-capable external displays
    yourself. You can use it on your embedded devices or even on full desktops to allow
    other systems to use your device as external display.


-   [gnome-network-displays](https://gitlab.gnome.org/GNOME/gnome-network-displays)
    is a miracast implementation for gnome.


<!--  Local Variables: -->
<!--  ispell-local-dictionary: "english" -->
<!--  mode: markdown -->
<!--  End: -->
