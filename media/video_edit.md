---
title: Video Encoders / Editors
---

See also {{< iref "codecs" "Codecs" >}} and it's subsection
{{< iref "codecs#media_info" "Media Info" >}},
{{< iref "sound_edit" "Sound Edit" >}},  {{< iref "media_players" "Media Players">}},
{{< iref "streaming" "Streaming" >}}.

The main utility
{{< iref "ffmpeg" "ffmpeg alias libav" >}}
has its own page.

----------------------------

# Guides

-   [DVD-HOWTO](http://en.tldp.org/HOWTO/DVD-HOWTO.html) provides
    step by step instructions on getting DVD movies to play in Linux. _2000_
-   The new Gentoo Wiki:
    [MPlayer](http://wiki.gentoo.org/wiki/MPlayer),
    [CD/DVD/BD Writing](http://wiki.gentoo.org/wiki/CD/DVD/BD_Writing),
-   [DVD Frequently Asked Questions](http://dvddemystified.com/dvdfaq.html) _(uptodate 2013)_
-   [ArchWiki: Convert any Movie to DVD Video
    ](https://wiki.archlinux.org/index.php/Convert_any_Movie_to_DVD_Video)
-   [Optical disc drive - ArchWiki
    ](https://wiki.archlinux.org/index.php/Optical_disc_drive)
    contains also a [list of ripping tools
    ](https://wiki.archlinux.org/index.php/Optical_disc_drive#Ripping).
-   [Convert any Movie to DVD Video - ArchWiki
    ](https://wiki.archlinux.org/index.php/Convert_any_Movie_to_DVD_Video#Video2dvdiso).
-   [Debian Multimedia Video packages
    ](https://blends.debian.org/multimedia/tasks/video).
-   [ArchWiki: list of video editors
    ](https://wiki.archlinux.org/index.php/List_of_applications#Video_editors),
    [video converters
    ](https://wiki.archlinux.org/index.php/List_of_applications#Video_converters),
    [subtitles
    ](https://wiki.archlinux.org/index.php/List_of_applications#Subtitles),
    [subtitles editors
    ](https://wiki.archlinux.org/index.php/List_of_applications#Subtitle_editors),
    [screecast
    ](https://wiki.archlinux.org/index.php/List_of_applications#Screencast),
    [webcam
    ](https://wiki.archlinux.org/index.php/List_of_applications#Webcam),
    [DVD authoring
    ](https://wiki.archlinux.org/index.php/List_of_applications#DVD_authoring),
    [DVD ripping
    ](https://wiki.archlinux.org/index.php/List_of_applications#DVD_ripping).


# Video Encoding

[Avidemux](http://avidemux.sourceforge.net/) (GPL)
:   [Avidemux](http://avidemux.sourceforge.net/)
    is a video editing and encoding tool. It can encode video
    in the following codecs: dvd, FFV1, H.263, H.264, x264, HuffYUV,
    MJPEG, MJPEG-4, Snow, SVCD, VCD, XVCD, Xvid. For audio the
    following codecs are available: mp3 (with lame), vorbis (with
    libvorbis), AAC (with FAAC), MP2 and AC-3 (with libavcodecs), MP2
    (with TwoLame), WAV PCM and WAV LPCM. The documentation is in the
    [Avidemux wiki](http://www.avidemux.org/admWiki/index.php).

    It is not in Debian but in deb-multimedia.

[dvdauthor](http://dvdauthor.sourceforge.net/) (GPL)
:   `dvdauthor` is simple set of tools to help author a DVD. The idea
    is to be able to create menus, buttons, chapters, etc. It is
    packaged in Debian.

    [tutorial on dvdauthor](http://gecius.de/linux/dvd.html) by Jens
    Gecius

    [qdvdauthor](http://qdvdauthor.sourceforge.net/) is a frontend for
    _dvdauthor_

    [GitHub: dvdauthor](https://github.com/ldo/dvdauthor)

[Flowblade](https://github.com/jliljebl/flowblade) (GPL)
:   is a multitrack non-linear video editor to compose movies from video clips, audio
    clips and graphics files. Clips can be cut at the desired frames, filters can be
    added to clips, and you can create multilayer composite images using compositor
    objects. _Flowblade is packaged in Debian._


[HandBrake](https://handbrake.fr/) (GPL)
:   is a tool for converting video from nearly any format to videos in H.265 (x265 and
    QuickSync), H.264(x264 and QuickSync), H.265 MPEG-4 and MPEG-2, VP8, VP9 and Theora;
    and audio in AAC / HE-AAC, MP3, Flac, AC3, Opus, or Vorbis._In Debian and
    deb-multimedia_

    -   [HandBrake Documentation](https://handbrake.fr/docs/en/latest/)
    -   [HandBrake - GitHub](https://github.com/HandBrake/HandBrake)

[LiVES](http://lives-video.com)  (GPL)
:   _LiVES_ is a Video Editing System that use mplayer2 or mpv, ffmpeg, imagemagick,
    perl and gtk+. _packaged in Debian_.
    -   [LiVES - GitHub](https://github.com/salsaman/LiVES)

[ogmrip](http://ogmrip.sourceforge.net/) (LGPL)
:   _ogmrip_ is an application and a set of libraries for ripping and encoding DVD into
    AVI, OGM MP4 or Matroska files using a wide variety of codecs (vorbis, mp3, pcm,
    ac3, dts, aac, xvid, lavc, x264, theora). OgmRip relies on mplayer, mencoder,
    ogmtools, mkvtoolnix, mp4box, oggenc, lame, and faac to perform its tasks.  There is
    a CLI client, it's called shRip. _Latest release 2015.  In Debian and
    deb-multimedia._

[OpenShot](https://www.openshot.org/) (GPL)
:   a video editor using _ffmpeg_ and supporting all it's codecs. It allows
    clip resizing, scaling, trimming, snapping, rotation, and cutting,
    video transitions with real-time previews, compositing, title creation, speed up and
    slow down clips, audio editing, ...
    _Openshot-qt is packaged in Debian._
    -   [Openshot-qt - GitHub](https://github.com/OpenShot/openshot-qt)

<a name="mencoder"></a>[Mencoder](http://www.mplayerhq.hu/) (GPL)
:   [Mencoder](http://www.mplayerhq.hu/) is a simple movie encoder, associated with
    {{< iref "media_players#mplayer" "Mplayer" >}} and designed to encode
    MPlayer-playable movies. It encodes to DivX4, XviD, one of the
    libavcodec codecs and pcm/mp3/vbrmp3 audio in 1, 2 or 3 passes.

    -   [Mplayer Home Page](http://www.mplayerhq.hu/design7/info.html),
    -   [Basic usage of MEncoder
        ](http://www.mplayerhq.hu/DOCS/HTML/en/mencoder.html)
    -   [Encoding with MEncoder
        ](http://www.mplayerhq.hu/DOCS/HTML/en/encoding-guide.html)
        from
        [Mplayer Documentation](http://www.mplayerhq.hu/DOCS/HTML/en/).
    -   [MEncoder - ArchWiki
        ](https://wiki.archlinux.org/index.php/MEncoder)
    -   [HOWTO Convert video files](http://en.linuxreviews.org/HOWTO_Convert_video_files)
        using mencoder.


<a name="pitivi"></a>[PiTiVi](http://www.pitivi.org/)

:   __PiTivi__ (LGPL) is an audio/video editing software written in python
    GTK+ that uses the gstreamer framework and integrates with _Gnome_.
    -   Wikipedia: {{< wp "PiTiVi" >}}.
    -   [PiTiVi Home](http://www.pitivi.org/)

[Shotcut](https://www.shotcut.org/) (GPL)
:   QT video editor, based on ffmpeg, with features like 4k resolution support, network
    stream playback, audio/webcam captures ... _Packaged in Debian._
    -   [Shotcut - GitHub](https://github.com/mltframework/shotcut)

[TEncoder](http://tencoder.sourceforge.net/)
:   is a multithreaded video and audio converter that uses MEncoder,
    MPlayer and FFMpeg. It uses
    {{< iref "#youtube" "youtube-dl" >}} to download
    video/audio from video sites like youtube.  It can also rip
    unprotected DVDs. It can convert video and audio type to each
    other.  Subtitles with same name as video can be hard-coded into
    video.

<a name="thoggen"></a>[Thoggen](http://thoggen.net/) (GPL)
:   _Thoggen_ is a DVD backup utility for Linux, based on GStreamer
    and Gtk+ which encodes into Ogg/Theora video. features: GUI,
    resizing, cropping, language Selection for audio track.
    _No longer in debian_

{{< iref "media_players#vlc" "VLC" >}}
:   _VLC_ plays and  transcode videos as explained in the
    [VLC wiki: Transcode](https://wiki.videolan.org/Transcode/).

[x264 H.264/MPEG-4 AVC encoder](http://www.videolan.org/developers/x264.html)
:   commandline encoder for creating H.264 (MPEG-4 AVC) video streams.
    _X264_ is in Debian.

[x265 HEVC Encoder](http://x265.org/)
:   is a commandline encoder for creating H.265/High Efficiency Video Coding (HEVC)
    video streams. _X265_ is in Debian.

## Obsolete software
_low activity or obsolete projects._

[acidrip](https://sourceforge.net/projects/acidrip/) (GPL)
:   _aciprip_ is a Gtk2::Perl frontend for mencoder and mplayer. It
    has an introductory
    [article in linux journal](http://www.linuxjournal.com/article/9124)
    _last release 2004_.

[dvd::rip](http://www.exit1.org/dvdrip/)
:   _dvd::rip_ is a Perl Gtk+ based DVD copy program built on top of
    {{< iref "#transcode" "Transcode" >}}. _Last release 2010._

[iso2mkv](http://5ko.free.fr/en/iso2mkv.html) (MIT license)
:   _iso2mkv_ is a bash script based on mplayer, mencoder, oggenc
    or lame, and mkvmerge for automated DVD to XviD/vorbis MKV video
    conversion. _Last release 2011._

[lxdvdrip](http://sourceforge.net/projects/lxdvdrip/) (GPL)
:   _lxdvdrip_ is a command line tool to rip and burn a video DVD. It uses
    {{< iref "#mencode" "mencoder" >}}, {{< iref "#transcode" "transcode" >}},`dvdbackup`
    _Last release 2011_


<a name="oggconvert"></a>{{< wp "OggConvert" >}} (LGPL)
:   __Oggconvert__  _discontinued_ convert audio and video files of various types
    into Ogg Vorbis audio format, and the Theora, VP8 and Dirac video
    formats. It supports Ogg, Matroska and WebM containers for
    output. __0ggconvert__ is written in Python - GTK+ and depends only on
    the {{< iref "Streaming#Gstreamer" "GStreamer framework" >}}.

    {{< iref "sound_edit#soundconverter" "SoundConverter" >}} for audio,
    {{< iref "#pitivi" "PiTiVi" >}} for video are  alternatives to
    _OggConvert_.
    _Oggconvert is no more packaged in Debian since jessie._

[Transcode](https://bitbucket.org/france/transcode-tcforge)
:   _Transcode_ is an _ obsolete  text-console utility for video stream processing.
    It is discontinued and no more packaged in Debian since jessie.

[vcdimager](http://www.gnu.org/software/vcdimager/) (GPL)
:   VCDImager is a full-featured mastering suite for Video CD's and
    Super Video CD's. _Old tool main developement from years 200O-2005
    but still packaged in Debian_

[vobcopy](http://vobcopy.org/) (LGPL)
:   _vobcopy_ copy (and decrypt) vob files. The development stopped in 2008.

[WinFF](http://winff.org/)
:   is a GUI for _FFmpeg_ or _avconv_ to convert video and audio files.
    It is packaged in DEbian as _winff-gtk2_ and _winff-qt_.

# Slide show video

[Imagination](http://imagination.sourceforge.net/) (GPL)
:   is a  slide show maker, which only requires the ffmpeg encoder and libsox.
    _Imagination_ is packaged in Debian.

[PhotoFilmStrip](http://www.photofilmstrip.org/en/) (GPL)
:   is a Python software to creates movies out of your pictures. It is packaged in
    Debian.
    -   [Photo Film Strip GitHub repository](https://github.com/PhotoFilmStrip/PFS).

[ffDiaporama](http://ffdiaporama.tuxfamily.org/ffdiaporama/) (GPL)
:   is a movie creator from photos and video clips. It is packaged in Debian._Last
    version 2014._

# SWF tools
[swftools (GPL)](http://www.swftools.org/)
:   SWF Tools is a collection of SWF manipulation and creation
    utilities. It can convert from jpeg, png, gif, pdf, avi, wav, ttf
    fonts to swf. It allows also to combine swf files and to extract
    sound, movies, data from swf. _active in 2013_

{{< wp "Google Swiffy" >}}
:   is a web-based tool developed by Google that converts SWF files to
    HTML5. Its main goal is to display Flash contents on devices that
    do not support Flash. You can upload your swf to
    [Swiffy](https://developers.google.com/swiffy/) and get a
    it converted to html5.

    -   [Swiffy Home](https://developers.google.com/swiffy/)

# Subtitles editors

-   [Sam Hocevar: DVD Subtitles](http://sam.zoy.org/doc/dvd/subtitles/)
    explains the subtitle stream.
-   [Aegisub](http://www.aegisub.org/)
    _Aegisub - Advanced Subtitle Editor_ is a tool for creating and modifying
    subtitles. It allows to time subtitles to audio, styling them, typesetting, editing
    and translating subtitles, as well as a powerful scripting environment. It includes
    a built-in real-time video preview. _Aegisub is packaged in Debian_.
-   [gaupol](https://github.com/otsaloma/gaupol) (GPL)
    is a gtk subtitle editor for text based files. _Gaupol is in Debian._
-   [gnome-subtitle](http://gnomesubtitles.org/about/) (GPL)
    is a subtitle editor for gnome, written in mono. It supports the most common
    text-based subtitle formats, video previewing, timings synchronization and subtitle
    translation, _and is in Debian._
    -   [Gnome Subtitle Gitlab repository
        ](https://gitlab.gnome.org/GNOME/gnome-subtitles/)
-   [Subtitle Editor](https://kitone.github.io/subtitleeditor/) (GPL)
    is a C++-GTK+3 tool to edit subtitles. It can be used for new subtitles or to transform,
    edit, correct and refine existing subtitle.
    It  also shows sound waves, which makes it easier to synchronise subtitles to
    voices._It is in Debian._
    -   [Subtitle Editor - GitHub](https://github.com/kitone/subtitleeditor).

# Screencasting {#screencast}
-   Wikipedia {{< wp "Screencast" >}} and
    {{< wp "Comparison of screencasting software" >}}
-   [ArchWiki: list of screencasting software
    ](https://wiki.archlinux.org/index.php/List_of_applications/Multimedia#Screencast)
-   [xvidcap](http://xvidcap.sourceforge.net/)
    (GPL) is a screen recording utility using FFMPEG's
    libavcodec/libavformat. _2006_
-   [recordMyDesktop](http://recordmydesktop.sourceforge.net/)
    is a desktop session recorder it records theora video with
    ogg vorbis audio. recordMyDesktop has a gtk and a qt frontend.
    -   [Screencasts in Ubuntu, part 1: recordmydesktop
        ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-1/)
        by Marcin Seredyński is a recordmydesktop tutorial.
-   [istanbul](https://wiki.gnome.org/Projects/Istanbul)
    (GPL) is a gnome project written in python. It is a desktop
    session recorder for the Free Desktop. It records your session
    into an Ogg Theora .
-   [vnc2swf](http://www.unixuser.org/~euske/python/vnc2flv/index.html)
    is a screen recorder either build in python
-   {{< iref "ffmpeg" "ffmpeg" >}} or
    {{< iref "ffmpeg" "libav" >}}
    can be used for screencasting as described in
    [Screencasts in Ubuntu, part 2: FFmpeg
    ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-2/)
    by Marcin Seredyński.

# Video download helpers {#video_download_helpers}
-   Wikipedia {{< wp "Comparison of YouTube downloaders" >}},
    they are also listed in
    {{< wp "Comparison of download managers" >}}

## Command line
-   [telecharger-streaming - Documentation Ubuntu Francophone
    ](http://doc.ubuntu-fr.org/telecharger_streaming)
-   [clive](http://clive.sourceforge.net/)
    written in perl _2012_ and it's c++ clone
    [cclive](http://cclive.sourceforge.net/) _2013_ are command line
    utilities for extracting videos from video sharing Web sites like
    YouTube. It can background and work while the user is
    not logged on.
-   <a name="youtube-dl"></a>[youtube-dl
    ](http://rg3.github.io/youtube-dl/)
    is a python (2 or 3) script to dowload videos from [many sites
    ](http://rg3.github.io/youtube-dl/supportedsites.html).
    Youtube-dl can use the following external downloaders: aria2c,
    avconv, axel, curl, ffmpeg, httpie, wget
    It is in debian.
    -   [GitHub: youtube-dl](https://github.com/rg3/youtube-dl)
    -   [youtube-dl/README
        ](https://github.com/ytdl-org/youtube-dl/blob/master/README.md)
        is the manual.
    -   [Youtube-dl Tutorial With Examples
        ](https://www.ostechnix.com/youtube-dl-tutorial-with-examples-for-beginners/)
-   [Pafy](http://pythonhosted.org/pafy/)
    is a Python library and cli to download YouTube content and
    retrieve metadata.  It is in the debian package _python-pafy_.
    -   [GitHub: pafy](https://github.com/mps-youtube/pafy)
-   [get-flash-videos](http://code.google.com/p/get-flash-videos/)
    a perl program to download videos from various Flash-based video
    hosting sites, without having to use the Flash player, which allow
    to download without having the last version of the player. It is
    in debian.
    -   [get-flash-videos GitHub repo
        ](https://github.com/monsieurvideo/get-flash-videos),
        [Nigel Taylor get-flash-video Github repo
        ](https://github.com/njtaylor/get-flash-videos/).
-   [Quvi](http://quvi.sourceforge.net/)
    contains a command line program to extract and download video
    files using libquvi, a library to parse Adobe flash video download
    links. It supports Youtube and other similar video websites. It
    provides access to functionality and data through an API, and does
    not enable or require the use of the flash technology. Quvi is in
    Debian.
-   [Streamlink](https://streamlink.github.io/index.html)
    Streamlink is a command-line utility which pipes video streams from [various services
    ](https://streamlink.github.io/plugin_matrix.html) into a video player, such as VLC.
    -   [Streamlink - GitHub](https://github.com/streamlink/streamlink).

## browser extensions
-   [video bookmarlets
    ](http://1024k.de/bookmarklets/video-bookmarklets.html)
    to integrate with a javascript able browser
-   {{< wp "Video DownloadHelper" >}}  is an extension for Firefox  to
    download videos from sites that stream videos through HTTP, such as
    YouTube.   [Video DownloadHelper addon page
    ](https://addons.mozilla.org/fr/firefox/addon/video-downloadhelper/)
-   [YouTube Downloader for Android
    ](http://sourceforge.net/projects/ytdownloader/)
    download YouTube video and extract/convert audio to mp3. For
    Android4+

## Download sites
-   There are also dome download site to help the flv downloading:
    [Keepvid](http://keepvid.com/) and
    [DownloadFlv](http://www.downloadflv.com/)
-   The [Wikimedia Commons](http://commons.wikimedia.org/wiki/Main_Page)
    is a project that provides a central repository for free
    images, music, sound & video clips and, possibly, texts and spoken
    texts.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
