---
title: Sound and Video Players
---

See also  {{< iref "codecs" "Codecs" >}} and it's subsection
{{< iref "codecs#media_info" "Media Info" >}},
{{< iref "tag_management" "Tag Management" >}},
{{< iref "streaming" "Streaming" >}}, {{< iref "ffmpeg" "FFmpeg section" >}},
{{< iref "sound_edit" "Sound Edit" >}},
{{< iref "video_edit" "Video Edit" >}},

-----

# References
## Sound
-   [Sound-Playing-HOWTO
    ](http://www.tldp.org/HOWTO/Sound-Playing-HOWTO.html)
    lists applications for Linux that play various sound formats, but
    is outdated *1998*.
-   [Wikipedia list of Linux audio software
    ](http://en.wikipedia.org/wiki/Linux_audio_software),
    {{< wp "Comparison of audio player software" >}},
    [Comparison of media players
    ](http://en.wikipedia.org/wiki/Comparison_of_media_players)
    including many features,
    [Category: Linux Media Players
    ](https://en.wikipedia.org/wiki/Category:Linux_media_players)
    and {{< wp "List of Linux audio software" >}}.
-   [linux-sound.org](http://linux-sound.org/).
-   [ArchWiki list of audio applications
    ](https://wiki.archlinux.org/index.php/List_of_applications/Multimedia#Audio).
-   [Music software written in Python
    ](http://wiki.python.org/moin/PythonInMusic)
-   The [Free Software Directory](http://directory.fsf.org/)
    [Audio section
    ](http://directory.fsf.org/audio/)
    gives a list of GPL sound applications.

## DVD/CD
See also {{< iref "dvd_cd_recording" "DVD and CD recording" >}}

-   ArchWiki:
    -   [Optical disc drive
        ](https://wiki.archlinux.org/index.php/Optical_disc_drive)
        burning, playback, ripping, troubleshooting.
    -   [DVD Backup
        ](https://wiki.archlinux.org/index.php/Dvdbackup),
-   Ubuntu Help:
    -   [Cd/Dvd Burning
        ](https://help.ubuntu.com/community/CdDvd/Burning)
    -   [How do I enable restricted codecs to play DVDs?
        ](https://help.ubuntu.com/stable/ubuntu-help/video-dvd-restricted.html)
    -   [RestrictedFormats/PlayingDVDs - Community Help Wiki
        ](https://help.ubuntu.com/community/RestrictedFormats/PlayingDVDs)
-   [DVD FAQ](http://dvddemystified.com/dvdfaq.html) from
    dvddemystified.com _updated each month_
-   [imdb : internet movie database](http://www.imdb.com)

# Sound Players {#sound_players}

Most Video players can handle both video and audio, the following
players are refered to in the
{{< iref "#video_players" "Video players section" >}}:
{{< iref "#gnash" "Gnash" >}}
{{< iref "#mplayer" "Mplayer" >}},
{{< iref "#mpv" "mpv" >}},
{{< iref "#xine" "Xine" >}},
{{< iref "#videolan" "Videolan Client (VLC)" >}}

Wikipedia: {{< wp "Comparison of audio player software" >}},
[Comparison of free software for audio - Players
](https://en.wikipedia.org/wiki/Comparison_of_free_software_for_audio#Players)

## Gstreamer based sound players
<a name="banshee"></a>{{< wp "Banshee_(music_player)"  "Banshee" >}}
:   An other music player using {{< iref "Streaming#Gstreamer" "GStreamer" >}} framework, but built
    upon Mono and Gtk#.

<a name="bmpx"></a>[Bmpx](https://sourceforge.net/projects/beepmp/) (GPL)
:   Bmpx is based on {{< iref "streaming#gstreamer" "GStreamer" >}},
    and can be considered as a gstreamer gui. The old *Bmp* was based on xmms, but
    *Bmpx* was rewritten from scratch in C++ and no longer share code with
    xmms. Bmpx can play every format for which you have a gst plugin. It supports also
    MusicBrainz, Last.fm radio/scrobbling, HAL, DBus. It is an obsolete software
    abandoned since 2006.

<a name="clementine"></a>[Clementine](https://www.clementine-player.org/)
:   Clementine is a QT5 fork of {{< iref "#amarok" "amarok 1.4" >}} but using
    {{< iref "Streaming#Gstreamer" "GStreamer" >}} .
    {{< wp "Clementine_(software)" "Wikipedia: Clementine" >}}.  Clementine can play
    internet streams, transcode music into MP3, Ogg Vorbis, speex, FLAC or AAC, manage
    tags, use {{< iref "tag_management#cuesheet" "Cue Sheets" >}}, display lyrics,
    be controlled from android phone, and many
    [features](http://www.clementine-player.org/about), playing
    main formats included opus, and can read all playlists including
    {{< iref "tag_management#cuesheet" "Cue Sheets" >}} but has no bookmark nor access
    to chapters. With one ogg file loaded it uses 85M resident / 60M shared.

    {{< iref "#strawberry" "Strawberry" >}} is a fork of clementine written in C++, QT5
    or QT6.

    -   [Controlling Clementine from the commandline with DBus and MPRIS
        ](https://github.com/clementine-player/Clementine/wiki/Controlling-Clementine-from-the-commandline-with-DBus-and-MPRIS)

<a name="exaile"></a>[Exaile](https://www.exaile.org/)
:   [Exaile](http://en.wikipedia.org/wiki/Exaile)
    (GPL) is an audio player written in python using pygtk and using
    {{< iref "streaming#gstreamer" "GStreamer" >}}
    aiming to be similar to KDE's AmaroK, but for GTK+. It has a plugin system that
    allow: {{< iref "#mpris" "MPRIS" >}} control
    ([mpris plugin](https://github.com/exaile/exaile/tree/master/plugins/mpris)),
    bidirectional last.fm support, a shoutcast directory browser, tag
    editing thru an
    {{< iref "tag_management#mutagen" "ExFalso" >}}
    plugin, {{< iref "streaming#daap" "DAAP protocol" >}}
    _client and server_ support.  As a PyGTK player you can expect a memory footprint of
    81M/39M shared (one ogg file loaded). Exaile is no longer in Debian since _jessie_.

    -   [GitHub - Exaile](https://github.com/exaile/exaile)
    -   [Exaile Documentation](http://exaile.readthedocs.io/en/stable/)
    -   [ArchWiki - Exaile](https://wiki.archlinux.org/index.php/Exaile)

<a name="guayadeque"></a>[Guayadeque](http://guayadeque.org/) (GPL)
:   Guayadeque is an audio player with database written in C++. It uses
    {{< iref "streaming#gstreamer" "GStreamer" >}}
    and _wxWidgets_ for the UI. It can play Ogg Vorbis, FLAC, MP3 or anything supported
    by _gstreamer_.  It can be interfaced through {{< iref "#mpris" "MPRIS" >}} D-Bus interface.  _in Debian_.

    -   Wikipedia: {{< wp "Guayadeque Music Player" >}}.

<a name="muine"></a>{{< wp "Muine" >}}
:   An other music player using {{< iref "streaming#Gstreamer" "GStreamer" >}}
    framework, but built upon Mono and Gtk# (like _Banshee_), not used on my systems.

<a name="juk"></a>[Juk](https://juk.kde.org/) (GPL-2.0)
is a KDE audio jukebox application, supporting collections of MP3, Ogg Vorbis, and FLAC
audio files. It's main focus, is on music management.

For playing media it uses {{< iref "streaming#Gstreamer" "GStreamer" >}}.

_Juk_ has many KDE libraries dependencies, making it heavy to use on non KDE Desktop.

-   [JuK · GitLab](https://invent.kde.org/multimedia/juk)

<a name="lollylop"></a>[Lollypop](https://wiki.gnome.org/Apps/Lollypop) (GPL-3.0)
:   is a Python / GTK3, {{< iref "streaming#Gstreamer" "GStreamer" >}} music player for
    Gnome.  It supports downloading of lyrics and cover art, syncing music with MTP
    devices (android), and has a kiosk mode view.

    Lollylop has no other Gnome dependencies that the GObject libraries (_gir1.2-xxx_),
    it is in Debian.

    As most python/GTK players it has heavy footprints, even with a small music library
    I get 430M resident / 84M shared without even playing anything.

    -   [lollypop · GitLab](https://gitlab.gnome.org/World/lollypop)

<a name="parlatype"><a>[Parlatype](https://www.parlatype.org/)
:   A  GNOME audio player for transcription using
    {{< iref "streaming#Gstreamer" "GStreamer" >}}

    It is packaged in Debian.

<a name=quodlibet></a>[QuodLibet](http://code.google.com/p/quodlibet/)
:   Quod Libet (GPL) is a GTK+-based audio player written in
    Python. It uses {{< iref "streaming#gstreamer" "gstreamer" >}}
    and supports Ogg Vorbis, FLAC, MP3, Musepack/Wavepack, MOD, MP4, TrueAudio, WMA.

    _QuodLibet_ uses playlists based on regular expressions and can display and edit
    tags.

    As other PyGTK players _like {{< iref "#exaile" "Exaile" >}}
    __QuodLibet__ is quite memory hungry (52M resident when playing mp3) as is ExFalso
    and if you are not using a full gnome desktop, you need to avoid _python-gnome2_
    otherwise you pull all the libraries and daemons.

    Even if we can find _QuodLibet_ too big as a background player, it is a nice tool
    for the _listen then tag_ game _like its brother _{{< iref "#exaile" "Exaile" >}}_.

    __Quodlibet__ use the python library {{< iref "tag_management#mutagen" "mutagen" >}}
    and share code with the {{< iref "tag_management#exfalso" "ExFalso" >}} tag editor.

    -   [ExFalso/Quodlibet manual](https://quodlibet.readthedocs.org/en/latest/)

<a name="rhythmbox"></a>[Rhythmbox](http://en.wikipedia.org/wiki/Rhythmbox) (GPL)
:   Rhythmbox is a gnome audio player using the
    {{< iref "streaming#gstreamer" "GStreamer" >}} media framework.

    Main features:
    -   Numerous [plugins
        ](https://en.wikipedia.org/wiki/Rhythmbox#Plug-ins), given also in
        [Rhythmbox/Plugins - GNOME Wiki!](https://wiki.gnome.org/Apps/Rhythmbox/Plugins)
        including [Third party plugins
        ](https://wiki.gnome.org/Apps/Rhythmbox/Plugins/ThirdParty).
    -   play streamed Internet radio and podcasts
    -   playlist
    -   gapless playback
    -   Audio CD ripping
    -   Album cover display
    -   Song lyrics display
    -   Scrobbling
    -   DAAP  server via DAAP sharing plugin which uses libdmapsharing.
    -   UpNP, DAAP, shoutcast,... client through
        [Grilo](https://developer.gnome.org/grilo/) plugin. _On Debian the package
        grilo-plugin is needed_.
    -   can subscribe to podcasts
    -   Web Remote Control.
    -   Plays ampache streams through a plugin.
    -   {{< iref "#mpris" "MPRIS" >}} plugin.

    Rhythmbox playing a single small mp3 take 90M res / 50M shr (on
    amd64 in may 2018)

    -   [Apps/Rhythmbox - GNOME Wiki!](https://wiki.gnome.org/Apps/Rhythmbox/)
    -   [Rhythmbox · GitLab](https://gitlab.gnome.org/GNOME/rhythmbox/-/tree/master)
    -   [ArchWiki - Rhythmbox
        ](https://wiki.archlinux.org/index.php/Rhythmbox)

<a name="sayonara"></a>[Sayonara](https://sayonara-player.com/index.php) (GPL-3.O)
:   is a small C++/QT music player,using {{< iref "streaming#gstreamer" "GStreamer" >}}.

    Sayonara supports {{< iref "#mpris" "MPRIS" >}}, lyrics and allow streaming from
    soundcloud, last.fm, Soma.fm, internet streams, radio broadcasting.


    Sayonara is in Debian since bullseye. for previous releases there is a
    [PPA repository for Sayonara
    ](https://launchpad.net/~lucioc/+archive/ubuntu/sayonara).
    with i386 and amd64 packages.

    On amd64 _Sayonara_ consume 68M res / 51M shr for _Sayonara
    1.0.0 in may 2018.

    -   [Sayonara Player · GitLab](https://gitlab.com/luciocarreras/sayonara-player)

<a name="strawberry"></a>[Strawberry](https://www.strawberrymusicplayer.org/) (GPL-3.0)
:   _Strawberry_ is a fork of  {{< iref "#clementine" "Clementine" >}} written in C++
    using the Qt toolkit QT5 or QT6 and {{< iref "streaming#gstreamer" "GStreamer" >}}.

    The features are essentially the same than {{< iref "#clementine" "Clementine" >}}
    Plays internet streams and interface with subsonic, Tidal, Qobuz.
    Supports WAV, FLAC, WavPack, Ogg FLAC, Ogg Vorbis, Ogg Opus,
    Ogg Speex, MPC, TrueAudio, AIFF, MP4, MP3, ASF and Monkey's Audio.  manage tags, use
    {{< iref "tag_management#cuesheet" "Cue Sheets" >}}, display lyrics,
    {{< iref "#mpris" "MPRIS control" >}},
    be controlled from android phone, and many
    [features](https://www.strawberrymusicplayer.org/#features), playing all formats
    recopgnized by {{< iref "streaming#gstreamer" "GStreamer" >}},
    and can read all playlists including cue sheet.

    Strawberry is not yet in Debian, but the project provides Debian packages, and
    Appimages built with QT5 or Qt6.

    -   [GitHub - Strawberry](https://github.com/strawberrymusicplayer/strawberry)

    On AMD64 in 2021 the memory footprints of _strawberry v0.9.3_ idle is 146M resident /
    100M shared.

## Other music players
[alsaplayer](http://www.alsaplayer.org/)
:   AlsaPlayer (GPL v3) <a name="alsaplayer"></a> is a PCM player. The Input Plugins include:
    MP2, MP3, WAV, CDDA, OGG, MPEG, MAD, CDDA, MikMod, and audiofile.
    The Output Plugins include: Alsa, OSS and OSS/Lite, Esound, Sparc,
    SGI, and JACK. Alsaplayer development stopped in 2004 with version
    0.99.75, but seem to begin again in 2007 with a new gtk2 interface,
    and has slept again the next year

<a href="amarok"></a>{{< wp "Amarok_(software)"  "Amarok" >}} (GPL)
:   said to be a very good audio player with a QT user interface,
    but is quite heavy and targeted to KDE. Amarok has been redesigned
    between v1.4 and v2.0, and many forks from previous version 1.4
    where done. The development stalled at 2.8 and marok was bound to QT4, as it was not
    updated it was [dropped from Debian](https://tracker.debian.org/pkg/amarok).
    But the development is kicking up again, and the release 3.0 should be using QT5 (or
    QT6?).

    -   _Amarok_ requires _KDE runtime_, which is a very heavy
        dependency, if your desktop is not KDE.
    -   {{< iref "#clementine" "Clementine" >}}
        is a fork of the version 1.4
        wich also uses Qt ( but QT5) and replaced the use of ffmpeg libraries by
        {{< iref "streaming#gstreamer" "GStreamer" >}}, and dropped the KDE
        dependencies. {{< iref "#strawberry" "Strawberry" >}} is a further fork of
        Clementine and share many features with it.
    -   {{< iref "#exaile" "Exaile" >}} is a GTK+ clone of amarok.
    -   _Amarok_ is the primary client for {{< iref "streaming#ampache" "Ampache" >}}
        this feature is not shared by the above derivatives.
    -   _Amarok_ can [play UPnP / DLNA streams
        ](https://userbase.kde.org/Amarok/Manual/Organization/Collection/RemoteCollections/UPnP)
        this feature is not shared by Clementine or Exaile.
    -   [ArchWiki - Amarok](https://wiki.archlinux.org/index.php/Amarok)
    -   [Amarok · GitLab](https://invent.kde.org/multimedia/amarok/-/tree/master)

     Main features:
     -   Play many formats including FLAC, Ogg, Opus, MP3, AAC, WAV,
         Windows Media Audio, Apple Lossless, WavPack, TTA and
         Musepack.
     -   Tag digital music files
     -   Search Covers and artist informations
     -   Playlist editing
     -   Display lyrics
     -   Podcast
     -   Play UPnP / DLNA streams

[Aqualung](http://aqualung.factorial.hu/home.html)
:   Aqualung (GPL) is a Gtk music player.
    Features:
    -   Play all sample-based, uncompressed formats, mod, mp3, Ogg
        Vorbis, Ogg Speex, flac, Musepack, Monkey's Audio, WavPack,
        and via ffmpeg AC3, AAC, WMA.
    -   Output on oss, jack, alsa, pulseaudio and can resample
    -   Audio CD play and ripping  with on-the-fly conversion to WAV,
        FLAC, Ogg Vorbis or CBR/VBR MP3 and tagging of the created files
    -   LADSPA plugin support.
    -   Tag editing
    -   Remote control through CLI commands

    If Aqualung has many dependancies upon sound libraries, it has
    none to desktop but Gtk. It is no longer in Debian since wheezy.

    -   [GitHub - Aqualung](https://github.com/jeremyevans/aqualung)
    -   [Aqualung Documentation
        ](http://aqualung.jeremyevans.net/manual/aqualung-doc.html).

[aRts](http://arts-project.org)
:   aRts (Analog Real-Time Synthesizer) is a sound system for KDE.
    aRts creates and processes sound using small modules that do
    certain tasks. aRts modules can create waveforms (oscillators),
    play samples, filter data, add signals, perform effects like
    delay/flanger/chorus, or output the data to a soundcard.

<a name="audacious"></a>[Audacious](http://audacious-media-player.org/)
:   Audacious is an GPL, XMMS like app written in QT5 or GTK 2, that
    support nearly the same plugins. It is a fork of BMP, like are
    {{< iref "#xmms2" "xmms2" >}} and

    Other forks are build in a client-server model, but
    Audacious was first a single player, but now can be controlled
    through DBUS.
    Features:

    -   codecs support thru plugins: mp3, aac, vorbis, flac, monkey's
        audio (ape), wavpack, shorten, musepack, tta, wma, sid, alac,
        wav, midi, CD audio;
    -   output to oss4, alsa, esound, jack, pulseaudio, sndio, sdl
    -   support for transcoding and streaming.
    -   Controlled through DBUS, accept {{< iref "#mpris" "MPRIS" >}} protocol.
    -   Can be controlled with Conky.
    -   Includes the client {{< man "audtool" >}}_ to sends commands to a running
        instance of Audacious.
    -   curses clients like [Audtty](http://audtty.alioth.debian.org/) _packaged in
        debian but the source code can no longer be accessed in 2021_.


    <!-- Audacious has a light memory footprint but seems somewhat processor
    demanding, I have no measure but I see my load average climbing
    each time I use it, more than other players.
    -->
    Audacious is in Debian some newer _audacious_ and _audacious_plugins_ are in
    the [ppa](https://launchpad.net/~ubuntuhandbook1/+archive/ubuntu/apps) maintained by
    [UbuntuHandbook](https://ubuntuhandbook.org/).

    The development seems to have slow down, at the end of version 3.x which was based
    by default on GTK2 and was developed during the years 2011-2019, but become again
    active in 2020 with the release of version 4.0 which is now based on QT5 with GTK2
    optional fallback.

    -   [Audacious Home page](http://audacious-media-player.org/),
    -   [audacious-plugins · GitHub
        ](https://github.com/audacious-media-player/audacious-plugins/tree/master/src)
    -   [GitHub - Audacious
        ](https://github.com/audacious-media-player/audacious).
    -   [ArchWiki - Audacious
        ](https://wiki.archlinux.org/index.php/Audacious)


<a name="deadbeef"></a>[DeaDBeeF](https://deadbeef.sourceforge.io/) (GPL v2)
:   is a C lang maudio player for Mp3, ogg vorbis,  flac, ape, wv/iso.wv, wav,
    m4a/m4b/mp4 (aac and alac), mpc, tta, cd audio, and  more.

    It reads and write tags in any format,  supports Shoutcast/Icecast and MMS, and
    {{< iref "tag_management#cuesheet" "cuesheet" >}}. _Deadbeef_ is not in Debian, but provides Debian packages for amd64.

    There are plugins for Pulseaudio, Jack, Mpris2.

    -   [Deadbeef - GitHub](https://github.com/DeaDBeeF-Player/deadbeef)
    -   Wikipedia:  {{< wp "Deadbeef" >}}


[Gradio](https://github.com/haecker-felix/gradio)
:   Gradio is a GTK3 app for finding and listening to internet radio stations.
    [ArchWiki - Gradio](https://wiki.archlinux.org/index.php/Gradio)


[Goggles Music Manager](https://gogglesmm.github.io/) ( GPL-3.0 License )
:   is a music collection manager and player. It is written in C++, and uses a sqlite
    database, the xine library for playback and the
    [FOX Toolkit](http://www.fox-toolkit.org/) for the interface.

    It categorizes your music files based on genre, artist, album, and song.  It
    supports gapless playback and tag editing.  It supports Ogg Vorbis , FLAC, MP3 ,
    MP4, ASF and Musepack music files.

    As it uses a desktop agnostic UI it has limited dependencies.

    -   [GitHub: goglesmm](https://github.com/gogglesmm/gogglesmm)
    -   [Goglesmm Ubuntu PPA package](https://launchpad.net/~s.jansen/+archive/ubuntu/gogglesmm)

{{< iref "#mpd" "Music Player Daemon" >}}
:   has a subsection.

<a name="qmmp"></a>[Qmmp](http://qmmp.ylsoftware.com/) (GPL)
:   _Qmmp_ is a C++/QT audio player. Qmmp is in Debian.

    Features:

    -   Codecs:  any formats provided by libsndfile, or ffmpeg
    -   Codecs list: MPEG1 layer 2/3, Ogg Vorbis, Ogg Opus,
        Native FLAC/Ogg FLAC, Musepack, WavePack,
        tracker modules (mod, s3m, it, xm, etc), ADTS AAC, CD Audio,
        WMA, Monkey's Audio, PCM WAVE, Midi, SID, Chiptune formats.
    -   DSP effects with LADSPA
    -   Output to OSS4, Alsa, {{< iref "streaming#pulseaudio" Pulse Audio >}},
        {{<iref "streaming#pipewire" "Pipewire" >}},
        {{<iref "streaming#jack" "Jack" >}}, QtMultimedia,
        {{<iref "streaming#icecast" "Icecast" >}}
    -   {{< iref "#mpris" "MPRIS" >}} (1.0 and 2.0)
    -   Cue sheet
    -   Lyrics
    -   [Extra plugins](http://qmmp.ylsoftware.com/links.php)

    On amd64 _Qmmp v1.4.4 (2021)_ memory footprints are 100M res / 83M shr idle
    or playing an opus file. It incrase whan you play more files, and is dependent of
    the enabled plugins.

[RealPlayer](http://www.real.com/linux) and [Helix Player](https://helixcommunity.org/)
:   Helix player is an open source media player, with support for the proprietary format
    `RealAudio` and `RealVideo` it is known as the proprietary RealPlayer. Mplayer is
    also known to play real audio and video with the appropriate codec. A test page for
    real audio and video streams is the
    [RealAudio and RealVideo Test Clips](http://service.real.com/realplayer/test/)

[TranscriberAG](http://transag.sourceforge.net/)
:   assists the manual annotation of speech signals. It
    provides a GUI for segmenting speech recordings, transcribing them,
    labeling speech turns, topic changes and acoustic conditions.

    See also {{< iref "#parlatype" "Parlatype" >}}
    -   [eroux/transcriberAG](https://github.com/eroux/transcriber-ag)

[xmcd & cda](http://www.amb.org/xmcd/)
:   Xmcd is a full-featured CD Player and Ripper, cda is a shell
    command-line utility which also features a curses-based,
    screen-oriented mode. xmcd is an alsa compatible application

<a name="xmms2"></a>[Xmms2](https://github.com/xmms2/wiki/wiki)
:   XMMS2 (GPL) is a music player developped using the
    client-server model which will provide kde, gtk, and command-line
    interface.
    It replaces the old _Xmms_ which was unmaintained and is sticked to gtk-1,
    It can play mp3, vorbis, aac, alac, wma, mac, sid, mod,
    wav, flac, mpc, speex files. _No support for opus in the stable release_.
    It is provided as a daemon with numerous plugin packages and client.

    The documentation for Xmms2 is in the
    [Xmms2 Wiki](https://github.com/xmms2/wiki/wiki)

    __xmms2__ has numerous clients
    graphic ones for gtk or kde, command line and ncurses clients, and
    also webclient that allow to control the daemon from a remote
    device. They are listed on the
    [Client page of xmms2 wiki](https://github.com/xmms2/wiki/wiki/Clients).

    The daemon itself is small.
    <!-- , and clients are 11M for gxmms2,
    14M for xmms2tray, wmxmms2 is only 1.7M and is the great winner
    among the graphic clients. -->

    We can also dispense with graphic gadgets
    and use the [console or command line client
    ](https://github.com/xmms2/wiki/wiki/Clients#console-clients) starting with _nyxmms2_
    the standard console application coming with XMMS2 and use no permanent resource at
    all when you use it only to launch, pause or stop the daemon, and only up to 1M is
    you let the status run on a permanent basis. In the same way a web client will use
    very few resources if running as a cgi script.

    Support for music formats/protocols is done through
    [plugins](https://github.com/xmms2/wiki/wiki/Plugins). There is a transport
    plugin for DAAP protocol, it is packaged in Debian as
    _xmms2-plugin-daap_.

    The stable version of Xmms2 is dated 2011, this 0.8 version is still proposed in the
    Debian package. The development version is no
    longer active.

    There are few forks of Xmms2: {{< iref "#bmpx" "Bmpx" >}},
    {{< iref "#audacious" "Audacious" >}}.


## Command Line Players {#CLI_players}

<a name="audiopreview"></a> [audiopreview](http://audiopreview.codealpha.net/audiopreview/)
:   is a simple command line tool based on
    {{< iref "streaming#gstreamer" "gstreamer" >}}
    to play previews of audio and video files, and internet streams. It can also be used
    as a regular media player. It is no longer in Debian since jessie, and the home page
    went away.
__
[cdtool](https://hinterhof.net/cdtool/)
:   _cdtool_ contains several programs for playing audio CDs and controlling a CD-ROM
    drive from the command line:
    -   [cdtool(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=cdtool%281%29)
    -   [cdplay](http://www.x-paste.de/cdplay/) is an interactive
        text-mode program for playing audio CDs. ref:
        [cdplay(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=cdplay%281%29)
    -   The _cdinfo_ command, with no option used, will print out the
        audiostatus.
    -   The _cdstop_ command stops the compact disc.
    -   The _cdpause_ command pauses the currently playing compact disc.
        Resume by using cdplay with no arguments.
    -   The _cdvolume_ command sets the output volume level (an integer
        from 0 to 255) of the CD player.
    -   The _cdir_ command lists information about the currently loaded
        audio compact disc. It lists the lengths of all tracks. It can also
        references a database files to find title, artist, and track name
        information.
    -   The _cdeject_ command ejects the current compact disc and the
        cdclose command closes the CDROM tray.

[cdparanoia](http://www.xiph.org/paranoia/)
:   Cdparanoia (Paranoia III) reads digital audio directly from a
    CD, then writes the data to a file or pipe in WAV, AIFC or raw 16
    bit linear PCM format. Cdparanoia does various extra checks and
    should be preferred to cdda2wav used when a perfect copy is
    necessary, or when the disk media or drive is damaged. cdparanoia
    can find if the paranoid tests are necessary or if the plain
    [cdda2wav can work with the cdrom](http://www.xiph.org/paranoia/faq.html#ok).
    refs: [cdparanoia(1)](http://www.xiph.org/paranoia/manual.html),
    [cdparanoia FAQ](http://www.xiph.org/paranoia/faq.html),
    [cdparanoia troubleshooting](http://www.xiph.org/paranoia/trouble.html)

icedax
:   [icedax(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdda2wav%281%29)
    also known as _ccda2wav_ is a sampling utility for CD-ROM (see
    {{< iref "sound_edit#icedax" "icedax entry in the Sound Editors, recorders section" >}}),
    it can also be used as a CD player.


<a name="gst123"></a>[gst123](http://space.twc.de/~stefan/gst123.php) (LGPL)
:   flexible command line player in the spirit of ogg123 and mpg123, based on
    {{< iref "#gstreamer" "Gstreamer" >}}. It plays all file formats gstreamer
    understands. Since gst123-0.1.0 support for watching videos has been added.

    _gst123_ is packaged in Debian.
    -   [gst123 - GitHub](https://github.com/swesterfeld/gst123).

<a name="madplay"></a>[madplay(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=madplay)
:   madplay is a command-line MPEG audio decoder and player based
    on the  MAD library {{< iref "sound_libs#item_libmad" "libmad" >}} and the
    [Mad audio decoder](http://www.underbit.com/products/mad/).
    madplay reads and decodes one or more input files containing MPEG audio data and
    plays them on the native audio device. It can also output a sound file in cdda,
    aiff, wave, snd, esd, raw formats. _see
    [madplay(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=madplay(1))

<a name="mpg123"></a>{{< wp "Mpg123" >}}
:   Mpg123 (LGPL) is a very fast decoder and player for mp3 _or any
    MPEG 1.0/2.0/2.5 stream (layers 1, 2 and 3)_ running on
    unix and w32 it support a lot aof audio interfaces including alsa,
    coreaudio, esound, jack, nas, oss, portaudio, pulseaudio, SDL.
    It  can also play MPEG audio files from a WWW server.
    _[mpg123(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=mpg123(1))

    [Mpg321](http://sourceforge.net/projects/mpg321)<a name="mpg321"></a>
    is a GPL replacement
    for Mpg123 which aimed at a truly free software mp3 player, while
    previous versions of mpg123 did not have a clear free opensource license.
    [mpg321(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=mpg321(1))

    There are some controversies about the respective performance of mpg123
    and mpg321. I have even read that mpg123 is twenty time faster. I made
    some test on an  Intel Core 2 Duo CPU  @ 2.00GHz, and found that
    mpg321 _(mpg321  0.2.10)_ is 16% slower than mpg123 _(mpg123 1.4.3)_.
    Of course it does not presume what it could be on other platforms.

    One other aspect of comparing both decoders is on memory footprint.
    when decoding a 42mn mp3 stream _(32kHz 128b/s)_ the resident size of
    mpg321 climbed progressively up to 36M, while mpg123 staid at 1M
    resident.

    Of course {{< iref "#madplay" "madplay" >}} that is based on the same libmad library
    has analogous performance in term of speed and memory fottprints, than mpg321.
    _It should be slower because doing only fixed arithmetic,
    but I found it 10% faster on an intel dual core._

{{< iref "#mplayer" "mplayer" >}}
:   MPlayer is a movie player. It plays most video and **audio**
    formats. He is described in the
    {{< iref "#mplayer" "Video Players section" >}} MPlayer can be used to
    record streaming audio with a command line like:

        mplayer -playlist playlist.txt -ao pcm -aofile mystream.wav -vc dummy -vo null

    It can be used from a cron tab like:

        0 11 * * 1-5 /home/username/scripts/streamrecorder >& /dev/null 0 14 * * 1-5  killall -9 mplayer

    You can also use in the same way {{< iref "#mpv" "mpv" >}}

## Ncurses sound players
<a name="auditive"></a>auditive
:   [auditive](http://www.rillion.net/auditive/)
    is a ncurses {{< iref "streaming#gstreamer" "GStreamer" >}} player written in vala.
    _last release 2013_.

[Cjukebox](http://muth.org/Robert/Cjukebox/)
:   is a GPL Python/Curses based management system for audio files
    and playlists, it uses [Musicus](http://muth.org/Robert/Musicus/)
    that uses xmms plugins in a non X environment. Development stalled
    since 2005

<a name="cmus"></a>[cmus](https://cmus.github.io/) (GPL)
:   cmus (GPL) is a ncurses text player.

    Main Features:
    -   Can play mp3, ogg/vorbis, FLAC, Opus, Musepack, WavPack, WAV,
        AAC, MP4, audio CD, and everything supported by ffmpeg (WMA, APE,
        MKA, TTA, SHN, ...) and libmodplug.
    -   configurable colorscheme, filters, album/artists sorting and a vi-like
        configuration interface.
    -   Play MP3 and Ogg streaming from SHOUTcast or Icecast.
    -   [support detaching natively](https://github.com/cmus/cmus/wiki/detachable-cmus).
    -   It can be controlled with an UNIX socket, and has many
        [remote controls](https://github.com/cmus/cmus/wiki/remote-control) from web,
        android, command line
    -   {{< iref "#mpris" "MPRIS" >}} support.
    -   Tiny: cmus 2.7.0 is 24M res. / 17 shr on amd64 (may 2018)

    Debian has a _cmus_ and a _cmus-plugin-ffmpeg_ package.

    Cmus has uncommon key binding and unusual help system: you have to type 7 to get
    help on key-bindings, to know you have to type 7, you just need hit the 7 key! Of
    course q does not quit, h or ?  does not give help. But to be fair I must say that
    you are free to configure key-bindings as you want.

    It is in active development in 2021 and packaged in Debian.
    -   [GitHub cmus repository](https://github.com/cmus/cmus)
    -   [cmus wiki](https://github.com/cmus/cmus/wiki)
    -   [Extensions and useful scripts](https://github.com/cmus/cmus/wiki)
    -   [cmus - C* Music Player](https://cmus.github.io/#documentation)
    -   Manual pages (last source):
        [cmus-tutorial](https://github.com/cmus/cmus/blob/master/Doc/cmus-tutorial.txt),
        [cmus](https://github.com/cmus/cmus/blob/master/Doc/cmus.txt) and
        [cmus-remote](https://github.com/cmus/cmus/blob/master/Doc/cmus-remote.txt).
    -   Manual pages  {{< man "cmus" >}}, {{< man "cmus-tutorial" >}},
        {{< man "cmus-remote" >}}.
    -   Wikipedia {{< wp "Cmus" >}}
    -   Cmus supports [remote control](https://github.com/cmus/cmus/wiki/remote-control)
        through a WEB interface or Android, and using {{< iref "#mpris" "MPRIS" >}}
    -   [ArchWiki - Cmus](https://wiki.archlinux.org/index.php/Cmus)
    -   [Articles about cmus](https://github.com/cmus/cmus/wiki/reviews)

[MikMod](http://mikmod.sourceforge.net/)
:   _MikMod_ is a [MOD](https://en.wikipedia.org/wiki/MOD_(file_format))
    music file players for UNIX-like systems. Mikmod is a module player and library
    supporting many formats, including mod, s3m, it, and xm.  MikMod uses the OSS
    /dev/dsp driver included in all recent kernels for output, and will also write .wav
    files.

    The player uses ncurses for console output and supports transparent loading from
    gzip/pkzip/zoo archives and the loading/saving of playlists.
    -   [mikmod(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=mikmod))
    -   [mikmod - GitHub](https://github.com/sezero/mikmod)

<a name="moc"></a>[Moc](http://moc.daper.net/) (GPL)
:   _Moc_ is an ncurses-based console audio player with ALSA, OSS, SNDIO or JACK
    outputs.  Supported file formats are: mp3, Ogg Vorbis, FLAC, Musepack (mpc), Speex,
    Opus, WAVE, AIFF, AU, SVX, Sphere Nist WAV, IRCAM SF, Creative VOC,SID, wavpack,
    MIDI and modplug.  With the FFmpeg plugin we add (WMA, RealAudio, AAC, MP4).

    _Moc_ works as a daemon and can be controlled by a command line or via conky, or the
    gui client mentioned below but it is not usable through the network like the music
    servers {{< iref "#mpd" "Mpd" >}} or {{< iref "#xmms2" "Xmms2" >}}.

    In 2021 there is no new release since MOC 2.5.2 and 2.6-alpha3 Released in 2016.
    Moc uses 6M resident.

    -   [Moc wikipedia page](http://en.wikipedia.org/wiki/Music_On_Console)
    -   [MOC Home page](http://moc.daper.net/)
    -   [Documentation | MOC](http://moc.daper.net/documentation)
    -   [MOC Readme](http://moc.daper.net/node/87)
    -   [MOC Scripts](http://moc.daper.net/contrib)
    -   [ArchWiki - Moc](https://wiki.archlinux.org/index.php/Moc).
    -   [MocIcon](http://mocicon.sourceforge.net/) is a simple GTK+ Music On Console tray
        icon. _Last release 2010._
    -   [moc-pris](https://github.com/progwolff/moc-mpris) is a mpris bridge for moc.
    -   [Exo](https://github.com/loimu/exo) (GPL-3.0) is a C++ QT frontend for MOC
        and {{< iref "#cmus" "Cmus" >}}.
        it supports Lyrics from web, {{< iref "#mpris" "MPRISv2" >}}, bookmarks, OSD with
        an additional Python script.

<a name="mp3blaster"></a>[mp3blaster](http://mp3blaster.sourceforge.net/) (GPL 2.0)
:   An interactive text-console based ogg, mp3, sid and wav player, with playlist
    management. As a ncurses application his memory requirements are low 3.5M resident.
    _mp3blaster_ last release was in 2014, and the development seems stopped since 2017.

    -   [GitHub - mp3blaster](https://github.com/stragulus/mp3blaster)
    -   manpages:
        [mp3blaster(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3blaster%281%29),
        [splay](http://manpages.debian.org/cgi-bin/man.cgi?query=splay%281%29),
        [nmixer(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=nmixer%281%29).

mpd text clients
:  {{< iref "#mpd" "mpd" >}} can be controlled by text clients like mpc, ncmpc, bash mp;
   they are referenced in the {{< iref "#mpd" "mpd section" >}}.

__ogg123__, __oggdec__
:  both GPL,  are part of the _vorbis tools_ which are the command lines utility
   of the {{< wp "Vorbis" >}} reference implementation, other decoders for
   ogg-vorbis are [Tremor](http://wiki.xiph.org/Tremor "wiki.xiph.org Tremor"),
   [Tremolo](http://wss.co.uk/pinknoise/tremolo/ "wss.co.uk pinknoise/tremolo")
   (GPL) _for arm platforms_ and ffmpeg _(see
   {{< iref "video_edit" "Video Encoders" >}}_.

   Performance of compression and quality  of _vorbis_ and mp3 are
   available in quantity and number, _(look on
   {{< wp "Vobis"  "Wikipedia:   Vorbis page" >}})_ but we compare less often
   speed and memory footprint. I compared _oggdec_ ,_mpg123_ and
   _mpg321_ on an intel dual core 2GHz, for the same wave file encoded
   at similar compression rate. I found _oggdec_ 20% slower than the
   mp3 decoders, a result not so significative, considered that I
   tried only on one stream. More interesting _oggdec_ and _mpg123_ stayed
   at 1.2Mb and 1Mb of resident memory, while _mpg321_ went up to 36Mb.

<a name="musikcube"></a>[MusikCube](https://musikcube.com/) (BSD-3-Clause License)
:   A terminal-based audio engine, library, player and server written in c++.
    Plug-ins provide core functionality for audio decoding, data streaming, output
    device handling, metadata parsing, digital signal processing.

    MusikCube is capable of streaming audio via an integrated server, and can be
    controlled by an android client. It supports also {{< iref "#mpris" "Mpris" >}}.

    Debian packages for amd64 are provided in the
    [releases page](https://github.com/clangen/musikcube/releases).

    -   [musikcube - GitHub](https://github.com/clangen/musikcube) .
    -   [MusikCube user guide](https://github.com/clangen/musikcube/wiki/user-guide)
    -   [MusikCube wiki](https://github.com/clangen/musikcube/wiki)

[play]( http://git.sysphere.org/play/)
:   A curses front-end written in python for various audio players based
    on cplay. _last commit 2013._

[Orpheus](http://thekonst.net/en/orpheus)
:   is a GPL text mode menu- and window-driven audio player application for CDs,
    internet stream broadcasts and files in MP3 and Vorbis OGG format. It is in debian.

[Radiotray-NG](https://github.com/ebruck/radiotray-ng) (GPL-3.0)
:   is a simple music streaming player that lives on the system tray. By clicking on the
    RadioTray icon, you'll be presented with a list of pre-configured online radios. By
    selecting one of those radios, it will start playing.

    This project is the continuation of
    [Radiotray](https://sourceforge.net/projects/radiotray/files/releases/).

## Emacs controlled Players {#emacs_players}

All these packages are in Melpa.

See also [EmacsWiki: MusicPlayers](http://www.emacswiki.org/emacs/MusicPlayers)

[Bongo](https://github.com/dbrock/bongo/) (GPL)
:   Bongo is a music player for emacs that was developped in parallel
    with EMMS. Bongo can use VLC,
    mpg321, ogg123, speexdec. Bongo has an
    [emacswiki page](http://www.emacswiki.org/emacs/Bongo).

<a name="emms"></a>[EMMS](http://www.emacswiki.org/cgi-bin/emacs.pl/EMMS) (GPL)
:   EMMS (GPLv3) is the Emacs Multi-Media System, a small application to play multimedia
    files from Emacs using external players. It can use mpg321, ogg123, mplayer, xine or
    {{< iref "#mpd" "mpd" >}}, {{< iref "streaming#mpv" "mpv" >}} with the help of the
    [mpv extension of emms](https://github.com/momomo5717/emms-player-simple-mpv),
    or any simple player available as unix command line client.

[ffmpeg-mplayer](https://github.com/jcs-elpa/ffmpeg-player) (GPL-3.0)
:   Play video from emacs using ffmpeg.

[playerctl.el](https://github.com/thomasluquet/playerctl.el)
:   Use {{< iref "#playerctl" "playerctl" >}} from emacs to control any
     {{< iref "#mpris" "MPRIS"  >}} enabled player.

[vlc.el](https://github.com/xuchunyang/vlc.el)
:   control VLC through VLC HTTP interface.


#### mpd control from emacs

<a name="libmpdee"></a>[libmpdee](https://github.com/andyetitmoves/libmpdee) (GPL)
:   LMibmpdee    is a client library for  {{< iref "#mpd" "mpd" >}}
    in emacslisp, packaged in MELPA.

[simple-mpc](https://github.com/jorenvo/simple-mpc) (GPL)
:   A GNU Emacs frontend to mpc, packaged in MELPA.

[Mingus](http://github.com/pft/mingus) (GPL).
:   Mingus is an extension of {{< iref "#libmpdee" "LMibmpdee" >}}
    by Niels Giesen, packaged in MELPA.  The interface resembles that of
    {{< iref "#ncmpc" "ncmpc"  >}}, and it provides extensive playlist editing
    facilities. It can be interfaced from emacs-w3m an dired.  _mingus stays home_ is
    used to play any local sound files, it provides a cd-burning tool
    and tag editing with [taggit]( https://github.com/ft/taggit).

__MPC__
:   is major mode providing an interface to MPD bundled with Emacs >= 23.2 .

[mpdel](https://gitea.petton.fr/mpdel/mpdel) (GPL)
:   Emacs user interface for Music Player Daemon, Available from melpa.
    It provides an Emacs user interface including playlists, navigation in
    the database and playback control. It can be controlled by ivy with
    [ivy-mpdel](https://gitea.petton.fr/mpdel/ivy-mpdel).

[simple-mpc](https://github.com/jorenvo/simple-mpc) (GPL)
:   A GNU Emacs major mode that acts as a front end to mpc.
    it is in Elpa.

# Music Player Daemon {#mpd}
## MPD Server

[Music Player Daemon](http://en.wikipedia.org/wiki/Music_Player_Daemon)
Music Player Daemon or MPD (GPL)allows remote access for
playing music  and managing playlists.

-   MPD can play MP3, Ogg Vorbis, Opus,FLAC, AAC, Mod, Musepack,
    Wavepack, wave files or anything produced by FFmpeg. More
    precisely it can play anything decoded with a [decoder plugin
    ](https://www.musicpd.org/doc/user/decoder_plugins.html): adplug,
    audiofile, faad, ffmpeg, flac, dsdiff, dsf, fluidsynth, mad,
    mikmod, modplug, mpcdec, mpg123, opus, pcm, sidplay, sndfile,
    vorbis, wavpack, wildmidi.
-   The input are not limited to files but can also come from any
    [input plugin
    ](https://www.musicpd.org/doc/user/input_plugins.html):
    alsa input from a soundcard, CD audio, HTTP stream with curl; rtp
    / rtsp / rtmp / rtmpt / rtmps with ffmpeg; unmounted smb or nfs,
    upnp servers on the local network, some commercial streaming services.
-   MPD can resample the input with a [resampler plugin
    ](https://www.musicpd.org/doc/user/resampler_plugins.html) i.e.
    either the internal resampler of low quality, but low cpu load; or
    better with libsamplerate or soxr.
-   MPD can then reencode the stream with an [encoder plugin
    ](https://www.musicpd.org/doc/user/encoder_plugins.html)
    null _i.e. no rencoding_, flac, mp3 with lame or shine, mp2 with
    twolame, opus, or vorbis for ogg vorbis, wave.
-   MPD can use any type of playlist with the [playlist plugins
    ](https://www.musicpd.org/doc/user/playlist_plugins.html)
    .asx, .cue,  embedded {{< iref "tag_management#cuesheet" "Cue Sheets" >}} from the "CUESHEET" tag with the
    embcue plugin, .m3u, extm3u, cuesheet metablock from a FLAC file
    with the flac plugin, .pls, .rss, playlist from SoundCloud,  XSPF
    playlists.
-   Mpd can output to alsa, or Jack and can send
    it's output thru network by using the {{< iref "sound_libs#libao" "libao" >}}
    and {{< iref "streaming#item_esound" "esound" >}} or
    {{< iref "streaming#pulseaudio" "use PulseAudio" >}}.
    The choice is down by setting
    [configuration options](https://www.musicpd.org/doc/user/config.html).
-   By using {{< iref "streaming#pulseaudio" "pulseaudio-dlna" >}}
    MPD can act as a UPnP / DLNA server.
-   MPD has its own [HTTP streaming server
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Tips_and_tricks#HTTP_streaming)
    capable of producing Ogg Vorbis and MP3 HTTP streams.
-   Mpd can output to an icecast or shoutcast server with the
    [shout ouput plugin
    ](https://www.musicpd.org/doc/user/output_plugins.html#shout_output)
    as described in
    [ArchWiki - Icecast: Streaming with MPD
    ](https://wiki.archlinux.org/index.php/Icecast#Streaming_with_MPD).
    but the native MPD streaming server can be preferred.

-   [Music Player Daemon documentation](https://mpd.readthedocs.io/en/latest/index.html),
    [MPD User Manual](https://mpd.readthedocs.io/en/stable/user.html)
-   [mpd(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpd%281%29)
-   [MPD configuration example
    ](https://github.com/MusicPlayerDaemon/MPD/blob/master/doc/mpdconf.example)
-   [GitHub - MPD](https://github.com/MusicPlayerDaemon/MPD)
-   [Music Player Daemon Wiki | Fandom
    ](https://mpd.fandom.com/wiki/Music_Player_Daemon_Wiki).
-   [ArchWiki: Music Player Daemon](https://wiki.archlinux.org/index.php/Mpd)
-   [ArchWiki: MPD Tips and tricks
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Tips_and_tricks)
-   [ArchWiki - Music Player Daemon/Troubleshooting
    ](https://wiki.archlinux.org/index.php/Music_Player_Daemon/Troubleshooting)
-   [Gentoo Wiki- MPD](https://wiki.gentoo.org/wiki/MPD)
    gives the configuration for a Bluetooh headset.
    See also
    [Gentoo Wiki - Bluetooth Headset](https://wiki.gentoo.org/wiki/Bluetooth_Headset).
    and the {{< iref "bluetooth" "Bluetooth section" >}}.

-   xmms2 team has published a
    [comparison of xmms2 and mpd](https://github.com/xmms2/wiki/wiki/XMMS2-vs-MPD),
    may be slightly biased in favor of {{< iref "#xmms2" "xmms2" >}},
    it omits that _mpd_ is lighter in memory and cpu than xmms2, and also that if the
    client development effort of {{< iref "#xmms2" "xmms2" >}} is presently greater than
    the older _mpd_, _mpd_ has still more language bindings and clients. In any case
    both server are worthwhile to try.
-   mpd can be controlled by a {{< iref "#mpris" "MPRIS" >}} with
    {{< iref "#mpdris2" "mpdris2" >}}.



## Clients
Mpd has some client libraries
in C/C++, Java, lisp/scheme, haskell, perl, php, python, Ruby.
-   [libmpdclient](https://www.musicpd.org/doc/libmpdclient/)
    is a client library for the Music Player Daemon, written in C.

For python you fin two main libraries:

-   [python-mpd](http://pypi.python.org/pypi/python-mpd/)
    is the older recommended library.
-   [python-mpd2](https://pypi.python.org/pypi/python-mpd2/)
    is an improvement of python-mpd.


The [MPD Manual](http://www.musicpd.org/doc/user/) has a a
[Configuration chapter](http://www.musicpd.org/doc/user/ch03.html).

You find a [long list of MPD clients in the mpd wiki
](https://mpd.fandom.com/wiki/Clients), most of
them are in the [mpd git repository](http://git.musicpd.org/),
the list is not always up-to date and some software are obsoletes.

Some scripts are also in the page  [MPD Hacks
](https://web.archive.org/web/20160414023836/http://mpd.wikia.com/wiki/Hacks)
_(archive of the page which has not be transferred to new fandom wiki.)_


A selection of clients:

-   {{< iref "streaming#ampache" "Ampache" >}}
    A  stream server for (see the {{< iref "streaming#ampache" "Ampache entry" >}})
    That can control many mpd instances for local play.
-   [Ario](http://ario-player.sourceforge.net/) a GTK2 client for _mpd_
    and {{< iref "#xmms2" "xmms2" >}}  inspired by Rhythmbox.
    _17M resident 10M shared_.
-   {{< iref "monitoring#conky" "Conky" >}}
    the monitoring daemon has a plugin to display the mpd state.
-   [emms](http://www.gnu.org/software/emms)
    the emacs multimedia player, can control mpd.
-   [fookebox](https://github.com/cockroach/fookebox/)
    is a jukebox-style web-frontend to mpd written in python
    with the pylons framework. It is in debian.
-   [Gimmix](https://github.com/cmende/gimmix) (GPL-2.0)
    is a graphical client written in C using GTK+2. It supports playlist management and
    ID3v2 Tag editing. _20M resident including 12M shared. The source repository has
    only few bug fixes since 2012 (checked in 2021)_
-   [Guimup](http://www.coonsden.com/) a client
    written in C++ and GTKmm.
-   [glurp](http://sourceforge.net/projects/glurp/)
    Graphical interface written in GTK+ (10M resident, 8.5M shared
    ).  [GitHub: glurp](http://git.musicpd.org/cgit/master/glurp.git/)
-   [gmpc](https://gmpc.fandom.com/wiki/Gnome_Music_Player_Client) (GPL-2.0)
    Gnome Music Player Client with playlist and tag management. It is
    a GTK client with light gnome dependencies (13M resident,10M, 3M
    added on my sys. ).
    -   [Github- gmpc](https://github.com/DaveDavenport/gmpc)
-   {{< iref "streaming#jinzora" "Jinzora" >}}
    A web based streaming and media management system.
-   _mpc_ the reference (Scriptable) command
    line client provided with _mpd_.
    Refs: [mpc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mpc%281%29)
-   __MPC.el__ is major emacs mode providing an interface to MPD.
-   [MPDCon](http://www.nongnu.org/gap/mpdcon/index.html) - A
    Graphical interface built with GNUstep SQLClient library.
-   [mpd remote](https://iprog.com/projects)  very basic PHP client
    designed for a mobile phone's browser.
-   [Mpd WebAmp](http://cseickel.googlepages.com/mpdwebamp)
    (GPL) is a web client for mpd based on turbogears.
-   <a name="mpdris2"></a>[mpDris2](https://github.com/eonpatapon/mpDris2) (GPL-3.0)
    is a {{< iref "#mpris" "MPRIS" >}} client daemon that is run in the user session and
    monitors a local or distant mpd server.
-   [musicpm](http://code.google.com/p/musicpm/)
    is a firefox extension written with the xul library it communicates
    with MPD over TCP sockets.
-   [ncmpc](http://git.musicpd.org/cgit/master/ncmpc.git/) -
    ncurses console client (1.6M resident, 1.2 shared) Refs:
    [ncmpc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ncmpc%281%29)
-   [ncmpcpp](http://ncmpcpp.rybczak.net/) is a rewrite in C++ and  of
    ncmpc, with some added features. It is _in 2018_ a very actively
    maintained, and updated project.
    -   [ArchWiki: Ncmpcpp
        ](https://wiki.archlinux.org/index.php/ncmpcpp)
    -   [GitHub - jelly/ncmpcpp-cheatsheet
        ](https://github.com/jelly/ncmpcpp-cheatsheet)
-   [phpMpReloaded](http://phpmpreloaded.sourceforge.net/) Group four
    Web interfaces  written in PHP with or without javascript:
    _PhpMp_ a simple web interface,  _PhpMp2_ add themes,
    _phpMp+_ is an enhanced PHP web
    interface with javascript that fit in your web browser's sidebar,
    _phpMp3_ is totally in JavaScript,
    driven by XMLHTTPRequest (AJAX) with a small php-backend, _iPodMp_ a
    php/ajax client, optimized for Apple's iPhone & iPod,
    _MPD-Web-Remote_  a mobile client for iPhone/iPad.
-   [Pitchfork MPD client](http://sourceforge.net/projects/pitchforkmpd/)
    is an ajax/php webinterface to mpd with optional streaming with
    icecast. _last release 2009_. There are some fork _patchfork_ that
    is no longer developed since 2010, and _web-mpd_.
-   [Pympd](http://pympd.sourceforge.net/) a frontend for mpd in
    the style of rhythmbox and itunes, written in python, with pygtk.
    (18M resident, 11M shared, on my system 7M truly
    added). _Unmaintained since 2007_.
-   [RDMPD](https://github.com/desfrenes/RMPDC) a simple PHP client
    targeted to smartphone with a basic browser (no javascript).
    _Last update 2010_
-   [Sonata](https://github.com/multani/sonata) is a e
    GTK+ client, a continuation of the unmaintened *Pygmy* client with
    playlist, tagediting, stream and Audioscrobbler (last.fm) support.
    (21M resident, 11M shared)
-   [Theory](http://theory.steelbreeze.org/)
    web based MPD client based on Python, pylons, and python-mpd.
-   [vimpc](https://github.com/boysetsfrog/vimpc) (GPL)
    A curses based client with vi like key bindings .
-   [WMmp](http://git.musicpd.org/cgit/master/wmmp.git/) - Window Maker
    dockapp
-   [wymypy](http://manatlan.infogami.com/wymypy)
    an http wsgi server written in python featuring a mpd client.
    It is an old unmaintained client with a fork in
    [GitHub: 02strich/wymypy
    ](https://github.com/02strich/wymypy).
-   [ympd
    ](https://github.com/notandy/ympd)
    is a tiny web client written in C with no other dependency than
    libmpdclient 2.

## Mpd bookmarks

To use bookmarks in mpd we can use

-   Joey Hess has set
    [mpdtoys](https://git.kitenet.net/index.cgi/mpdtoys.git/tree/), which is a
    collections of perl scripts for mpd. He
    [explains how he use them](https://joeyh.name/blog/entry/my_mpd_setup/).  _mpstore_,
    and _mpdload_ which dumps and restore the mpd daemon state can be used with
    audiobooks.
-   [MPD Bookmark](https://github.com/RaoulChartreuse/mpd_bookmark) is a simple script
    witch monitor MPD and keep a trace of where the listening of a file ended.
-   [mpdmark](https://github.com/Mic92/mpdtools) by Jörg Thalheim is a python script to
    bookmark songs, The author has also written
    [mpstated](https://github.com/Mic92/mpdstated) a vala program which restore recent
    position for each podcast in mpd.


# Video Players {#video_players}

All {{< iref "streaming#upnp_media_clients" "UPnP media clients" >}},
all {{< iref "#media_centers" "media centers" >}},
and many of the {{< iref "streaming" "Music Streamers" >}}
can also stream video, so you can also look around in these sections.

Of course video players allow also to play music, for other sound
players see the {{< iref "#sound_players" "Music Players section" >}}.

Wikipedia has a big
[Comparison of media players
](http://en.wikipedia.org/wiki/Comparison_of_media_players)
including many features,
a [Category: Linux Media Players
](https://en.wikipedia.org/wiki/Category:Linux_media_players)
and a page {{< wp "List of Linux audio software" >}}.

## Gstreamer based video players {#gstreamer_video_apps}

### Gstreamer

{{< iref "streaming#gstreamer" "GStreamer" >}} (LGPL) is a streaming-media framework,
based on graphs of filters which operate on media data. Applications using this library
can do anything from real-time sound processing to playing videos.it is
{{< iref "streaming#gstreamer" "referenced in the Music Streamer section" >}}


### Gnash {#gnash}

[Gnash](https://www.gnu.org/software/gnash/) (GPLv3) is the GNU Flash movie player which
can be run standalone, as well as as a plugin for several browsers. Gnash can use either
{{< iref "streaming#gstreamer" "GStreamer" >}} or ffmpeg as codec support library.

### Gnome Videos {#gnome_videos}
{{< wp "GNOME_Videos" >}} (GPL) previously named <a name="totem"></a> _Totem_ is a GTK+
media player (audio and video) for GNOME based on
{{< iref "streaming#gstreamer" "GStreamer" >}}, it can play all mainstream media formats
supported by {{< iref "streaming#gstreamer" "GStreamer" >}}.

It also understands numerous playlist formats, including SHOUTcast, M3U, XML Shareable
Playlist Format (XSPF), SMIL, Windows Media Player playlists and RealAudio playlists.

While _Videos_ offers a gnome desktop integration, it's gnome dependencies are moderate,
wich allow to install it in lighter GTK environments. _Videos_ is in the Debian package
_Totem_.

On an Amd64 in may 2018 Totem take 82M res / 46shr for a single ogg
track; 116M res / 57M shr for a tv broadcast on DLNA.

-   [Videos -  Gnome Home](https://wiki.gnome.org/Apps/Videos)
-   [Totem Manual](https://help.gnome.org/users/totem/stable/index.html.en)
-   [Totem Plugins](https://help.gnome.org/users/totem/stable/totem-plugins.html.en) :
    [YouTube Browser
    ](https://help.gnome.org/users/totem/stable/totem-plugins.html.en#totem-plugins-youtube)
    allows you to search and browse YouTube, and play YouTube videos directly in Totem
    Movie Player.
-   [Totem Gitlab repository](https://gitlab.gnome.org/GNOME/totem).

Totem can play UpNP, DAAP, Jamendo, Youtube, vimeo and more through the
[Grilo](https://developer.gnome.org/grilo/) plugin.

### Kaffeine {#kaffeine}
[Kaffeine](https://apps.kde.org/kaffeine/) (GPL-2.0+)
is a media player for KDE with support of digital TV (DVB). Kaffene uses
{{< iref "streaming#gstreamer" "GStreamer" >}}.

Its KDE dependencies are moderate, and it can be installed
in an other QT desktop.
-   [Multimedia / Kaffeine · GitLab](https://invent.kde.org/multimedia/kaffeine)


## Other Video players
### Lightspark {#lightspark}
[Lightspark](https://github.com/lightspark/lightspark) (GPL) is a Flash player
implementation that run as a web browser plugin or as a standalone application.
_LightSpark_ is in Debian.

-   [Lightspark GitHub repository](https://github.com/lightspark/lightspark)
-   [Lightspark Wiki](https://github.com/lightspark/lightspark/wiki/)
-   [Lightspark Support for various websites
    ](https://github.com/lightspark/lightspark/wiki/Site-Support)

### MPlayer  {#mplayer}

[Mplayer](http://www.mplayerhq.hu/) (GPL) is a movie player. It plays most video formats
as well as DVDs.  Its big feature is the wide range of supported output drivers.

The supported codecs are:

-   libavcodec: This codec package is capable of decoding
    H263/MJPEG/RV10/DivX3/DivX4/DivX5/MP41/ MP42/WMV1/WMV2/SVQ1/SVQ3
    encoded video streams and WMA (Windows Media Audio) v1/v2 audio. It
    is also known to be the fastest for this task.
-   Win32 codecs:
-   QuickTime codecs
-   XviD
-   XAnim: are the best codecs (full screen, hardware YUV zoom)
    fordecoding 3ivx and Indeo 3/4/5 movies

**gmplayer** is MPlayer with a graphical user interface;

{{< iref "#smplayer" "SMPlayer" >}} (GPL) is a GUI for mplayer or {{< iref "#mpv" "mpv" >}}.

{{< iref "video_edit#mencoder" "mencoder" >}}
is the encoder included in the mplayer distribution.

**References:**

-   [MPlayer Home page](http://www.MPlayerHQ.hu/),
-   [Mplayer documentation](http://www.mplayerhq.hu/DOCS/HTML/en/),
-   [MPlayer Features](http://www.mplayerhq.hu/design7/info.html).
-   [mplayer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mplayer(1))
-   Wikipedia {{< wp "MPlayer" >}}
-   [ArchWiki: Mplayer](https://wiki.archlinux.org/index.php/MPlayer)


### Mpv {#mpv}

[Mpv](https://mpv.io/) (LGPLv2.1+ and GPLv2+)
is a media player based on MPlayer and MPlayer2.

_MPlayer2_ was a fork of mplayer, that  the internal gui
_gmplayer_ and the encoder _mencoder_; and use shared libratries
instead of embedding {{< iref "ffmpeg" "ffmpeg" >}}.
It is dead and replaced with mpv.

Mpv also drop _mencoder_, but replace it with internal
[encoding](https://mpv.io/manual/stable/#encoding) facilities.
There are numerous other
[differences of mpv with mplayer and mplayer2
](https://github.com/mpv-player/mpv/blob/master/DOCS/mplayer-changes.rst).

-   [Mpv source (GitHub)](https://github.com/mpv-player/mpv)
-   [Mpv manual](https://mpv.io/manual/stable/),
    [FAQ](https://github.com/mpv-player/mpv/wiki/FAQ) and
    [Wiki](https://github.com/mpv-player/mpv/wiki).
-   Wikipedia: {{< wp "Mpv_(media_player)"  "MPV" >}}
-   [Archwiki -  Mpv](https://wiki.archlinux.org/index.php/Mpv)
-   [Gentoo Wiki - Mpv](https://wiki.gentoo.org/wiki/Mpv)

There is a Debian package _mpv_, but mpv developpers
[recommand to use a newer version](https://mpv.io/installation/)
in deb-multimedia.

_Mpv_ can be used in Wayland for hardware video acceleration under Wayland use
`--gpu-context=wayland`. If you compile it specifically for wayland use:
~~~
./configure --disable-x11 --disable-sdl --enable-wayland --disable-libass
make
sudo make install
~~~

#### Mpv frontends

Mpv itself has a rudimentary {{< iref "#mpv_pseudo" "pseudo-gui" >}}
and many
[third party frontends
](https://github.com/mpv-player/mpv/wiki/Applications-using-mpv#gui-frontends)
see also the [list on Wikipedia
](https://en.wikipedia.org/wiki/Mpv_(media_player)#Interface_and_graphical_front-ends).

<a name="smplayer"></a>[SMPlayer](http://www.smplayer.info/)
:   (GPL) is a GUI for {{< iref "#mplayer" "mplayer" >}} or mpv
    written in C++ with Qt4/Qt5. It supports [numerous formats and codecs
    ](http://www.smplayer.info/en/supported-formats-and-codecs), it can
    play YouTube videos. And support [chromecast
    ](https://blog.smplayer.info/category/chromecast/) since v17.1
    this need you have Chrome or Chromium installed. SMPlayer is in Debian.
-   [SMPlayer Blog](https://blog.smplayer.info/)
-   [Wikipedia: SMPlayer](https://en.wikipedia.org/wiki/SMPlayer).

[celluloid](https://celluloid-player.github.io/) (GPL-3.0)
:   is a  GTK+ frontend for mpv.
    -   [GitHub - celluloid](https://github.com/celluloid-player/celluloid)

<a name="mpv_pseudo-gui"></a>pseudo-gui mode
:   Mpv provides a _pseudo-gui mode_ that you get by starting it
    with:

        $ mpv  --player-operation-mode=pseudo-gui

    or by using the `mpv.desktop` file


### Streamlink {#streamlink}
[Streamlink](https://streamlink.github.io/index.html) ( BSD-2-Clause License )
is a command-line utility written in Python which allows you to watch online video
streams in video players, such as {{< iref "#vlc" "VLC" >}},
{{< iref "#mplayer" "Mplayer" >}}, {{< iref "arm_sbc#omxplayer" "OMXPlayer" >}} or
{{< iref  "#mpv" "Mpv" >}}.

Most of the big streaming services are supported, such as: Twitch, YouTube, Livestream,
Dailymotion, facebook, pluzz, vimeo, and a [huge list of site supporting plugins
](https://streamlink.github.io/plugin_matrix.html).

Streamlink is in Debian.

_Streamlink_ was forked from the now dead _Livestreamer_ project.

-   [Streamlink - GitHub](https://github.com/streamlink/streamlink)
-   [Streamlink documentation](https://streamlink.github.io/index.html)
-   [Streamlink - ArchWiki](https://wiki.archlinux.org/title/Streamlink)

## VideoLAN {#vlc}

[VideoLAN](http://www.videolan.org/) (GPL) targets streaming of MPEG-1,
MPEG-2,MPEG-4 and DivX files, DVDs, digital satellite and terrestial
television channels, and live videos on IP network

[VLC](http://www.videolan.org/vlc/) media player is a cross-platform media player, and
streamin server. Supported video formats and streaming protocols are given in the
[VLC features list](http://www.videolan.org/vlc/features.html)

Since version 3.0.1 VLC support {{< iref "streaming#chromecast" "Chromecast" >}}.

**Refs:**

-   {{< wp "Wikipedia VLC media player" >}}
-   [VideoLan Wiki](https://wiki.videolan.org/)
-   [VLC Documentation](https://wiki.videolan.org/Documentation).
-   [VLC playback documentation](https://wiki.videolan.org/Documentation:Play_HowTo)
-   [VLC Streaming documentation](https://wiki.videolan.org/Documentation:Streaming_HowTo),
    [HowTo/Receive and Save a Stream - VideoLAN Wiki
    ](https://wiki.videolan.org/Documentation:Streaming_HowTo/Receive_and_Save_a_Stream/)
-   [VLC FAQ](https://wiki.videolan.org/Frequently_Asked_Questions/)
-   [VLC Extensions](https://addons.videolan.org/)
-   [ArchWiki - VLC](https://wiki.archlinux.org/index.php/VLC_media_player)

### VLC memory footprints.

In june 2021 _vlc_ 3.0.12 loaded without playing anything takes on an AMD64 103M
resident / 80M shared.

Playing a simple opus file on DLNA don't change much the memory footprint going to 110M /
83M.

When playing a DLNA streamed film I get 173M / 98M, as usual the memory is not
automatically reclaimed, and after closing the film we have still 153M / 93M.

The qvlc i.e. vlc-qt interface is similar with 110M / 88M without playing.

The Ncurses interface launched with `vlc  -I ncurses` get 71M / 56M without playing,

### Xine {#xine}
[Xine](http://www.xine-project.org/) (GPL) is a free multimedia player which plays back
CDs, DVDs, and VCDs, decodes AVI, MOV, WMV, and MP3 from local disk drives, and displays
multimedia streamed over the Internet.

It is an old project, but still maintained and packaged in Debian.

-   {{< wp "xine" "Wikipedia: Xine" >}}
-   [Xine FAQ](http://xinehq.de/index.php/faq),
-   [Xine HowTo](http://dvd.sourceforge.net/xine-howto/),
-   [xine(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=xine(1)),
    [aaxine(1)](http://man.cx/aaxine(1)),
    [xine-remote(1)](http://manpages.debian.org/cgi-bin/man.cgi?query=xine-remote(1)).

# MPRIS {#mpris}

The [Media Player Remote Interfacing Specification (MPRIS)
](http://specifications.freedesktop.org/mpris-spec/latest/)is a standard D-Bus
interface which aims to provide a common programmatic API for
controlling media players.

-   [Features for MPRIS 3.0 - KDE Wiki
    ](https://community.kde.org/MPRIS#Features_for_MPRIS_3.0)

The players supporting MPRIS include
{{< iref "#amarok" "Amarok" >}},
{{< iref "#audacious" "Audacious" >}},
{{< iref "#banshee" "Banshee" >}},
{{< iref "#bmpx" "BMPx" >}},
{{< iref "#clementine" "Clementine" >}},
{{< iref "#cmus" "Cmus" >}},
{{< iref "#deadbeef" "Deadbeef" >}}with the
[DeaDBeeF-MPRIS-plugin](https://kernelhcy.github.io/DeaDBeeF-MPRIS-plugin/),
, Dragon Player,
{{< iref "#exaile" "Exaile" >}},
{{< iref "#guayadeque" "Guayadeque" >}},
{{< iref "#juk" "Juk" >}},
{{< iref "#moc" "Moc" >}} via [moc-pris](https://github.com/progwolff/moc-mpris),
{{< iref "streaming#mopidy" "Mopidy" >}}
via [mopidy-mpris](https://github.com/mopidy/mopidy-mpris),
{{< iref "#mpd" "MPD" >}} via {{< iref "#mpdris2" "mpDris2" >}},
{{< iref "#mpv" "mpv" >}} with the help of
[lua-mpris](https://github.com/dodo/lua-mpris#mpv)
or [mpv-mpris](https://github.com/hoyon/mpv-mpris),
{{< iref "#musikcube" "MusikCube" >}},
{{< iref "#qmmp" "Qmmp" >}},
{{< iref "#rhythmbox" "RhythmBox" >}},
{{< iref "#totem" "Totem" >}},
{{< iref "#vlc" "VLC" >}} when launched with
`vlc --control dbus`,
{{< iref "#xmms2" "Xmms2" >}} via xmms2-mpris-bridge.

This [shell script](https://gist.github.com/exic/1d051e3a15f61e06caf4), is an example of
MPRIS control of a player.

Other control tools are:

<a name="playerctl"></a>[playerctl](https://github.com/altdesktop/playerctl) (LGPL-3.0)
:   is an mpris command-line controller and library for vlc, mpv, RhythmBox, web
    browsers, cmus, mpd, spotify and others. _In Debian and active in 2021_.

    -   [playerctl.el](https://github.com/thomasluquet/playerctl.el) uses _playerctl_ from emacs
    -   [tmux-plugin-playerctl](https://github.com/richin13/tmux-plugin-playerctl) (MIT
        License) a tmux plugin or using playerctl to display MPRIS meta-data about the
        music currently playing.
    -   Inside [Waybar](https://github.com/Alexays/Waybar/) _playerctl_ is used in the python script
        [mediaplayer.py
        ](https://github.com/Alexays/Waybar/blob/master/resources/custom_modules/mediaplayer.py).

[mpris-remote](http://incise.org/mpris-remote.html)
:   is a utility that controls an MPRIS-capable music player.
    [GitHub: mpris-remote](http://github.com/mackstann/mpris-remote/).
    mpris-remote is in Debian.

[mpris-ctl](https://git.sr.ht/~mariusor/mpris-ctl) (MIT License)
:   by Marius Orcsik is a C lang cli mpris control for keyboard music control. Its only
    dependency is on the C dbus library.

[mpris-scrobbler](https://git.sr.ht/~mariusor/mpris-scrobbler)
:   by Marius Orcsik is a C lang user daemon which submits the currently playing song to
    libre.fm, listenbrainz, and compatible services.

[GitHub - un-def/i3blocks-mpris](https://github.com/un-def/i3blocks-mpris)
:   A persistent i3blocks blocklet for the MPRIS D-Bus interface.

# Mixers
[aumix](http://jpj.net/~trevor/aumix.html)
:   Aumix is a tty-based, interactive method of controlling a sound card
    mixer. It lets you adjust the input levels from the CD, microphone,
    and board synthesizers, as well as the output volume. Aumix can
    adjust audio mixers from the command line, from a script, or
    interactively at the console or terminal with an ncurses-based
    interface, or with a X11 interface named **aumix-X11**.

__amixer__
:   _amixer_ from {{< iref "sound_libs#alsa" "alsa" >}} utilities is the alsa text based mixer

    refs: [amixer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=amixer(1))

__alsamixer__
:   _alsamixer_ is a curse text mixer tool  from {{< iref "sound_libs#alsa" "alsa" >}}
    utilities.

    refs:  [alsamixer(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=alsamixer(1))

[SDL mixer](http://www.libsdl.org/projects/SDL_mixer/) (zlib license)
:   A simple multi-channel audio mixer for SDL. It supports 4 channels
    of 16 bit stereo audio, plus a single channel of music, mixed by
    {{< iref "#item_mikmod" "MikMod" >}} MOD, Timidity MIDI and SMPEG MP3 libraries.
    The command line utilities are **playmus** and **playwave**
    -   [SDL Mixer documentation
        ](https://www.libsdl.org/projects/SDL_mixer/docs/index.html)
    -   [SDL mixer - Github](https://github.com/libsdl-org/SDL_mixer)


# Media centers and distributions {#media_centers}

[freevo](http://freevo.sourceforge.net/)
:   A linux distribution for multimedia either on a standalone PVR
    computer with a TV+remote, as well as on a regular desktop computer
    using the monitor and keyboard. Freevo is developped using the
    Python Language.

    -   [Freevo Wiki](http://freevo.sourceforge.net/cgi-bin/doc)


[geexbox](http://www.geexbox.org/en/index.html)
:   is a live cd distribution aimed at media playing. GeeXboX runs on
    x86, PowerPC and ARM devices.


<a name="mythtv"></a>[MythTV](http://www.mythtv.org/) (GPLv2)
:   _MythTV_ is a digital video recorder. Through a plugins system it
    can record and play back scheduled programs, schedule recordings
    automatically in advance, play external video, show photos, play
    music files, use your TV and a web camera as a video-telephone over
    the Internet, retrieve weather forecasts, and many other functions.

    -   [MythTV main page](http://www.mythtv.org/)
    -   [MythTV HowTo](http://www.mythtv.org/wiki/MythTV-HOWTO)
    -   [MythTV User Manual](http://www.mythtv.org/wiki/User_Manual:Index)
    -   [MythTV UPnP](http://www.mythtv.org/wiki/UPnP):
        MythTV has a built-in UPnP server.
    -   [ArchWiki: MythTV](https://wiki.archlinux.org/index.php/MythTV)
    -   Wikipedia: {{< wp "MythTV" >}}

    No prepackaged _MythTV_ exists for Debian (_in 2021_) you have to build
    your package from the source as described in
    [Installing MythTV on Debian
    ](https://www.mythtv.org/wiki/Installing_MythTV_on_Debian).
    But there are Debian packages _kodi-pvr-mythtv_ a MythTV PVR Addon for Kodi,
    _mythtv-status_ status of a MythTV backend.

[rockbox](http://www.rockbox.org/)
:   is an open source replacement firmware for mp3 players. It runs on
    some models from Apple ipod, Archos, Cowon iaudio,Ipod, Iriver,
    MPIO, Olympus, Philips, Samsung, Sandisk, Sony, Toshiba.  _a
    release in 2017_

## Kodi {#kodi}
<a name="xbmc"></a>{{< wp "Kodi" >}} Kodi (formerly XBMC) (GPL)
is a cross-platform digital media hub and HTPC (Home theater PC)
software designed to be a    media player for the living-room TV.<br />

-   [Kodi Home](http://kodi.tv)
-   [Kodi Wiki](http://kodi.wiki/)
    -   [List of Kodi Devices
        ](https://kodi.wiki/view/Devices)
    -   [Raspberry Pi](https://kodi.wiki/view/Raspberry_Pi)
    -   [XBMC built-in UPnP A/V media server](http://kodi.wiki/view/UPnP/Server)
    -   [Kodi UPnP client](https://kodi.wiki/view/UPnP/Client)
    -   [Kodi as UPnP Control Point
        ](https://kodi.wiki/view/UPnP/Client#Sending_video_to_other_UPnP_targets).
    -   [PulseAudio](https://kodi.wiki/view/PulseAudio)
        s used when Kodi is installed in a desktop-environment rather than a
        dedicated/direct boot setup. PulseAudio allows normal video & audio playback in
        XBMC while at the same time allowing the user to get audio in their browser or
        other applications.
    -   [NFO FIles](https://kodi.wiki/view/NFO_files) can be used to provide metadata to
        the library for video and a music files.
    -   [Cue sheets](https://kodi.wiki/view/Cue_sheets)
    -   [UPnP server]](http://kodi.wiki/view/UPnP/Server).
    -   [List of built-in functions](https://kodi.wiki/view/List_of_built-in_functions).
    -   [External players](https://kodi.wiki/view/External_players)
-   [List of software based on Kodi - Wikipedia
    ](https://en.wikipedia.org/wiki/List_of_software_based_on_Kodi_and_XBMC).
-   [ArchWiki: Kodi](https://wiki.archlinux.org/index.php/Kodi)

On amd64 I have experienced Kodi playing a TV stream taking
98M res / 46M shr in may 2018 for kodi 2:17.6.

On raspberry PI 1 osmc distribution I have Kodi multiple threads
109M / 55 M shared.

Kodi can be used in wayland, _kodi-wayland is packaged in Debian_.

-   `kodi-send`  is used for sending actions to a kodi server in the lan.
    It is in the Debian Package _kodi-eventclients-kodi-send_; Of course you don't need
    to have a kodi server on the machine where you install `kodi-send`. The
    actions you can send are listed in the [List of built-in functions
    ](https://kodi.wiki/view/List_of_built-in_functions)
-   There are many Firefox plugins to send content to Kodi, among them:
    [Send to Kodi](https://addons.mozilla.org/en-US/firefox/addon/send-to-xbmc-kodi/)
    ( [GitHub Repository](https://github.com/dirkjanm/firefox-send-to-xbmc)) and its
    fork [send to Kodi2](https://addons.mozilla.org/en-US/firefox/addon/send-to-kodi-2/)
    (  [GitHub Repository](https://github.com/WPettersson/firefox-send-to-xbmc))
    [kodi-control](https://addons.mozilla.org/en-US/firefox/addon/kodi-control/)
    ( [GitHub Repository](https://github.com/LendoK/kodi-control)),
    [Play to Kodi](https://addons.mozilla.org/en-US/firefox/addon/play-to-kodi4/)
    ( [GitHub Repository](https://github.com/maciex/play-to-kodi) with numerous forks
    and a [Chrome Version](https://chrome.google.com/webstore/detail/play-to-kodi/)),
    [goldenratio/xbmc-web-remote](https://github.com/goldenratio/xbmc-web-remote) can be
    used with Firefox, Chrome or Opera,
-   [send2kodi](http://kodi.dnmx.ch/) is a javascript page to send an url to kodi
    Fabio Rämi (dnmx)
    [describes it in his blog](https://dnmx.ch/blog/2016/03/send2kodi.html).
-   There are also some shell scripts to send an url to kodi
    [allejok96/send-to-kodi](https://github.com/allejok96/send-to-kodi/),
    [facmachado/send2kodi](https://github.com/facmachado/send2kodi/),
    [nawar/kodi-cli](https://github.com/nawar/kodi-cli) and its fork
    [/WPettersson/kodi-cli](https://github.com/WPettersson/kodi-cli).
-   [osmc](https://osmc.tv/) is a distribution of Kodi based on Debian.
    All resources are on the [OSMC Wiki](https://osmc.tv/wiki/).
    It can be installed on Raspberry Pi, Apple TV first generation, and a their own
    platform [Vero](https://osmc.tv/vero/), an ARM64 platform with 2G DDR3, USB2, Gigabit
    ethernet, IR and RF receiver, with a price ~ 100€.
    -   [Github - osmc](https://github.com/osmc/osmc)

-   [xbev](https://github.com/bobo1on1/xbev/wiki) (GPL)
    is a simple desktop eventclient for Kodi, written in Python, it creates a window on
    using gtk and sends any keypresses received on that window to Kodi's eventserver.
-   [MediaElch](https://www.kvibes.de/mediaelch/) (LGPL)
    ([GitHub Repository](https://github.com/komet/mediaelch)) is a MediaManager for Kodi,
    which manage the ``nfo`` files used by Kodi. It is a C++ application, an appimage is
    provided (no package).

-   <a name="omxplayer">[OMXPlayer](https://github.com/popcornmix/omxplayer/)
    is the command line OMX player for the Raspberry PI.

    Omxplayer is deprecated and should be replaced by vlc , his is due to: omxplayer
    uses openvg for OSD and subtitles which isn't supported on Pi4. omxplayer uses
    openmax which has been deprecated for a long time and isn't supported with 64-bit
    kernels. omxplayer does not support software decode omxplayer does not support
    advanced subtitles omxplayer does not support playback from ISO files. omxplayer
    does not integrate with the X desktop.

<!--  Local Variables: -->
<!--  ispell-local-dictionary: "english" -->
<!--  mode: markdown -->
<!--  End: -->
