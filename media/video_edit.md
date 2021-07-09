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
    [screencasting software
    ](https://wiki.archlinux.org/title/Screen_capture#Screencast_software),
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
    _Active in 2021_.

    It is not in Debian but in deb-multimedia.

[dvdauthor](http://dvdauthor.sourceforge.net/) (GPL)
:   `dvdauthor` is simple set of tools to help author a DVD. The idea
    is to be able to create menus, buttons, chapters, etc. It is an old tool but still
    maintained _in 2021_. It is packaged in Debian.
    -   [DVDAuthor documentation](http://dvdauthor.sourceforge.net/doc/index.html)
    -   [qdvdauthor](http://qdvdauthor.sourceforge.net/) was a frontend for
        _dvdauthor_. Last commit 2011.
    -   [GitHub: dvdauthor](https://github.com/ldo/dvdauthor)

[Flowblade](https://github.com/jliljebl/flowblade) (GPL)
:   is a multitrack non-linear video editor to compose movies from video clips, audio
    clips and graphics files. Clips can be cut at the desired frames, filters can be
    added to clips, and you can create multilayer composite images using compositor
    objects. _Flowblade is packaged in Debian._


<a name="handbrake"></a>[HandBrake](https://handbrake.fr/) (GPL)
:   is a tool for converting video from nearly any format to videos in H.265 (x265 and
    QuickSync), H.264(x264 and QuickSync), H.265 MPEG-4 and MPEG-2, VP8, VP9 and Theora;
    and audio in AAC / HE-AAC, MP3, Flac, AC3, Opus, or Vorbis.As such it can be used
    for for converting DVDs or making videos that are compatible with portable video
    devices. _In Debian and deb-multimedia_

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
    a CLI client, it's called shRip. _Latest release 2015, last commit 2018_.
    -   [OGMRip source repository](https://sourceforge.net/p/ogmrip/code/ci/master/tree/)

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
    GTK+ that uses the {{< iref "streaming#gstreamer" "gstreamer" >}}
    framework and integrates with _Gnome_. Packaged in Debian._
    -   Wikipedia: {{< wp "PiTiVi" >}}.
    -   [PiTiVi Home](http://www.pitivi.org/)
    -   [Pitivi Manual](http://www.pitivi.org/manual/)

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
    {{< iref "#handbrake" "Handbrake" >}} for video are  alternatives to
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

See also {{< iref "#webcam" "Webcam" >}}.

-   Wikipedia {{< wp "Screencast" >}} and
    {{< wp "Comparison of screencasting software" >}}.
-   [ArchWiki: list of screencasting software
    ](https://wiki.archlinux.org/title/Screen_capture#Screencast_software)

-   {{< iref "ffmpeg" "ffmpeg" >}} or {{< iref "ffmpeg" "libav" >}}
    can be used for screencasting as described in
    [Screencasts in Ubuntu, part 2: FFmpeg
    ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-2/)
    by Marcin Seredyński and [FFmpeg screen capture- ArchWiki
    ](https://wiki.archlinux.org/title/FFmpeg#Screen_capture).
-   {{< iref "media_players#vlc" "VLC" >}} allows screen capture.

-   [istanbul](https://wiki.gnome.org/Projects/Istanbul)
    (GPL) is a gnome project written in python. It is a desktop
    session recorder for the Free Desktop. It records your session
    into an Ogg Theora .
-   [recordMyDesktop - Github](https://github.com/Enselic/recordmydesktop/)
    is a CLI desktop session recorder written in C. It records theora video, and
    ogg vorbis audio.

    The project was stalled at 3.8.1 december 2008. But Martin Nordholts who is the
    maintainer of recordMyDesktop moved it to Github and relaunched development and a
    new release 4.0. in march 2021.  recordMyDesktop had a gtk and a qt front-end, but at
    time of release 4.0, they have not yet been ported to the new code base.

    recordMyDesktop is in Debian.
    -   [Screencasts in Ubuntu, part 1: recordmydesktop
        ](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-1/)
        by Marcin Seredyński is a recordmydesktop tutorial.
    -   [recordMyDesktop - Sourceforge](http://recordmydesktop.sourceforge.net/)
        was the home of recordmydesktop until 3.8.1.
    -   [RecordMyDesktop - ArchWiki](https://wiki.archlinux.org/title/RecordMyDesktop).
-   [SimpleScreenRecorder](https://en.wikipedia.org/wiki/SimpleScreenRecorder) (GPL-3.0)
    is a Qt-based screencast software thar can record the entire screen or part of it,
    or record OpenGL applications directly. It uses libav/ffmpeg libraries for encoding,
    so it supports many different codecs and file formats. _packaged in Debian_.
    -   [SimpleScreenRecorder Home](https://www.maartenbaert.be/simplescreenrecorder/)
-   [vokoscreenNG](https://linuxecke.volkoh.de/vokoscreen/vokoscreen.html) (GPL-2.0)
    vokoscreenNG is a QT5 screencasting software, to record the screen, an area or a
    window; and audio from multiple sources. It has also built-in camera support.
    _packaged in Debian_
    -   [vokoscreenNG - GitHub](https://github.com/vkohaupt/vokoscreenNG)
-   [vnc2flv](http://www.unixuser.org/~euske/python/vnc2flv/index.html)
    is a screen recorder  build in python. The old 2010 Python 2 is obsolete, but
    [matthayes / vnc2flv - Github](https://github.com/matthayes/vnc2flv) is a port to
    Python 3.
-   [xvidcap](http://xvidcap.sourceforge.net/)
    (GPL) is a screen recording utility using FFMPEG's libavcodec/libavformat.
    _Obsolete, last release 2006._

# Video recording

## Television (DVB) and cameras
### DVB

DVB systems distribute data using a variety of standards:
-   Satellite: DVB-S, DVB-S2, DVB-S3, DVB-SH _Satellite Handhelds_.
-   Cable: DVB-C, DVB-C2
-   Terrestrial television: DVB-T, DVB-T2, DVB-H _Handhelds_.

The DVB card support for linux is given by the entries in
[Hardware device information - LinuxTVWiki
](https://www.linuxtv.org/wiki/index.php/Hardware_device_information)
which are classified by standard _cf above_ and card interface pci, pcie, pcmia,
IEEE1394 / Firewire, usb device.

### DVB and Video4Linux {#v4l}
[LinuxTV.org - Television with Linux](https://www.linuxtv.org/)
develops and maintains the Linux Kernel Media Subsystems, provide support for
devices like webcams, streaming capture and output, analog TV, digital TV, AM/FM
radio, Sofware Digital Radio (SDR), remote controllers and encoders/decoders for
compressed video formats. It offers native support for a large number of drivers for
commonly available PCI cards and USB devices

The DVB driver subsystem is included in the Linux kernel ≥ 2.6.

Video4Linux (V4L) is intended to provide a common programming interface for TV,
capture cards, parallel port and USB video cameras.
-   Wikipedia: {{< wp "Digital Video Broadcasting" >}}
-   [LinuxTV.org - Projects](https://www.linuxtv.org/projects.php).
-   DVB links are in the
    [V4L - DVB Wiki](http://www.linuxtv.org/wiki/index.php/Main_Page).
-   [Video for Linux resources](http://www.exploits.org/v4l/)
-   [Radio Listening Software](https://www.linuxtv.org/wiki/index.php/Radio_Listening_Software)
-   [DVB-T - ArchWiki](https://wiki.archlinux.org/title/DVB-T)
-   [DVB-S - ArchWiki](https://wiki.archlinux.org/title/DVB-S)
-   [RTL-SDR - ArchWiki](https://wiki.archlinux.org/title/RTL-SDR)
-   [GNU Radio - ArchWiki](https://wiki.archlinux.org/title/GNU_Radio)

-   [v4l2ucp](http://v4l2ucp.sourceforge.net) is an universal control
    panel for V4L and V4L2 devices. it is in Debian until _buster_ but
    [the source repository is no longer available
    ](https://tracker.debian.org/pkg/v4l2ucp).
-   [V4l-utils](https://linuxtv.org/wiki/index.php/V4l-utils)
    are a series of programs for handling media devices.
    It is packaged in the Debian package _dvb-tools_.
    v4l-utils  contains the following video4linux command line utilities:
    -   decode_tm6000: decodes tm6000 proprietary format streams
    -   v4l2-compliance: tool to test v4l2 API compliance of drivers
    -   v4l2-ctl, cx18-ctl, ivtv-ctl: tools to control v4l2 controls from the cmdline
    -   v4l2-dbg: tool to directly get and set registers of v4l2 devices
    -   v4l2-sysfs-path: sysfs helper tool
-   [LinuxTV dvb-apps](https://www.linuxtv.org/wiki/index.php/LinuxTV_dvb-apps)
    are a set of libraries, applications and utilities geared towards the initial setup,
    testing and operation of an DVB device supporting the DVB-S, DVB-C, DVB-T,
    and ATSC standards. It is packaged in the Debian package _dvb-apps_
-   [VDR](http://www.tvdr.de/software.htm)
    The Video Disk Recorder Software, is a digital sat-receiver program to record MPEG2
    streams, as well as output the stream to TV. It is also possible to watch DVDs and
    use an IR remote control. It is packaged in Debian.
-   [Xawtv](https://www.linuxtv.org/wiki/index.php/Xawtv)
    is a set of software for watching and recording television channels and webcams.
    In Debian distribution it is in the following packages:

    -   alevtd : HTTP daemon for teletext pages
    -   fbtv : television viewer - Linux framebuffer application
    -   pia : movie player for xawtv
    -   radio : ncurses-based radio application
    -   scantv : television channel-scanner
    -   streamer : television and webcams capture tool (images/movies)
    -   ttv : television viewer - console application
    -   v4l-conf : tool to configure video4linux drivers
    -   webcam : image grabber and uploader
    -   xawtv, xawtv-plugins, xawtv-plugin-qt : television viewer - X11 application
    -   xawtv-tools : television viewer - tools

### Gnome DVB Daemon {#dvb_daemon}

[DVBDaemon](https://wiki.gnome.org/action/show/Projects/DVBDaemon)
is a GStreamer based daemon to setup your DVB devices, record and/or watch TV shows and
browse EPG. It supports DVB-C, DVB-S, DVB-S2 and DVB-T devices (DVBv5 API), is
controlled via its D-Bus interface by any application, allow to watch live TV using
{{< iref "#gnome_videos" "Gnome Videos" >}}, and acces UPnP / DLNA through
{{< iref "streaming#rygel" "Rygel" >}}.

gnome-dvb-client Python GTK+ client, which speaks to the daemon via DBUS.

### Camera applications {#webcam}
-   [Webcam setup - ArchWiki](https://wiki.archlinux.org/title/Webcam_setup)
-   [List of applications Webcam - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Webcam)
-   Wikipedia {{< wp "Comparison of webcam software" >}}
-   [Webcam HOWTO](http://en.tldp.org/HOWTO/Webcam-HOWTO) _2005_
-   {{< iref "ffmpeg" "FFMPEG" >}} can [record your webcam
    ](https://wiki.archlinux.org/title/FFmpeg#Recording_webcam)
-   {{< iref "#mpv" "mpv" >}} can take a [v4l source as input
    ](https://github.com/mpv-player/mpv/wiki/Video4Linux2-Input).
-   You can take snapshots from your webcam
    [with mplayer](https://wiki.archlinux.org/title/Webcam_setup#MPlayer)
    or
    [with mpv](https://wiki.archlinux.org/title/Webcam_setup#mpv).

-   [Cheese](https://wiki.gnome.org/Apps/Cheese)
    is a Gnome webcam application that supports image and video capture, it has features
    such as Multi-Burst mode, Countdown timer for photos. It is in Debian.
-   [deepin-camera](https://github.com/linuxdeepin/deepin-camera) (GPL-3.0)
    a QT5 software to view camera, take photo and video.
-   [FFmpeg recoding webcam - ArchWiki
    ](https://wiki.archlinux.org/title/FFmpeg#Recording_webcam)
-   [fswebcam](http://www.sanslogic.co.uk/fswebcam/) (GPL-2.0)
    _fswebcam_ is a CLI program which captures images from a V4L1/V4L2 compatible device
    or file, averages them to reduce noise and draws a caption, compress the image to
    PNG or JPEG using the GD Graphics Library and save it to a file or send to stdio
    where it can be piped to something like ncftpput or scp.

     _fswebcam_ is in Debian but as far than 2021, the 2020 release us not packaged, but
     only the 2014 release.

     -   [fswebcam - GitHub](https://github.com/fsphil/fswebcam).
     -   [Raspberrypi fswebcam tutorial
         ](https://www.raspberrypi.org/documentation/usage/webcams/)
-   [Kamoso](https://apps.kde.org/kamoso/) (GPL-2.0)
    Webcam KDE recorder.
-   [Motion](https://motion-project.github.io/index.html)
    Motion is a highly configurable program that monitors video signals from many types
    of cameras. Features include
    -   Create mpeg/mp4/swf/flv/mov/ogg videos or save jpg/ppm pictures of the activity.
    -   Passthrough recording from many IP cameras
    -   View live stream of cameras
    -   Invoke scripts when activities occur
    -   Log activity into multiple types of databases
    -   Fully customizable masks for privacy or motion detection
    -   Full tls(https) support with authentication for webcontrol and streams
    -   Can use Network cameras via RTSP, RTMP and HTTP; PI cameras; V4L2 webcams;
        Video capture cards

    Motion is a command line based tool with options setup via the command line or via
    configuration files. It has also minimalistic web server allowing to access the
    webcam output via a browser.

    Motion is packaged in Debian.

    There is also a  package gmotionlive  for a GTK  viewer
    for streaming webcams that use multipart/x-mixed-replace streams, originally
    targeted to motion, but this program does not seem anymore maintained.

    -   [Motion Documentation](https://motion-project.github.io/motion_guide.html)
    -   [Motion - Github](https://github.com/Motion-Project/motion)

-   [Qtcam
    ](https://www.e-consystems.com/opensource-linux-webcam-software-application.asp)
    (GPL 3.0) C++/QT webcam software provides easier user interface for capturing and
    viewing video from devices supported by Linux UVC driver, and any V4L2 compatible
    device. An ubuntu package is provded on a Launchpad PPA.
    -   [Qtcam - Github](https://github.com/econsysQtCAM/QtCAM)
    -   [list of supported cameras
        ](https://www.e-consystems.com/opensource-linux-webcam-software-application.asp#Supported-Cameras)
-   _uvcdynctrl_ (GPL) from [libwecam](https://sourceforge.net/projects/libwebcam/)
    is a command line tool to control v4l2 devices. It is in Debian until _buster_,
    [look here for more recent support](https://tracker.debian.org/pkg/libwebcam).
-   [vgrabbj](http://vgrabbj.gecius.de/) grabs a image from a camera
    (any v4l compatible device) and puts it in jpg/png format. It is
    in debian.
-   _Webcam_ from {{< iref "#xawtv" "Xawtv software suite" >}}
    provides an utility that captures images from a video4linux device such as bttv,
    annotates them and uploads them to a webserver in an endless loop using FTP or SSH.
    It is a Debian package. From  {{< iref "#xawtv" "Xawtv " >}} you can also use
    _streamer_, also packaged in Debian.
-   [Webcamoid](http://webcamoid.github.io/) ( GPL-3.0 )
    a C++, QT application to capture, save and view a video stream. In Debian.
    -   [Webcamoid - GitHub](https://github.com/webcamoid/webcamoid)
-   [ZoneMinder](https://zoneminder.com/)
    is intended for use in single or multi-camera video security applications,
    It supports capture, analysis, recording, and monitoring of video data coming from
    one or more video or network cameras. It needs a mysql/mariadb database.
    There is _an heavy_ package on Debian _with a lot of Perl dependencies_.
    _For a lighter software look at motion above_.

### USB video device class, UVC  {#uvc}
{{< wp "UVC" >}}is a USB device class that describes devices capable of streaming video
like webcams, digital camcorders, transcoders, analog video converters and still-image
cameras.

The support of UVC in linux is done by the
[Linux UVC project](http://www.ideasonboard.org/uvc/)
which includes a V4L2 kernel device driver.

-   Wikipedia {{< wp "List of USB video class devices" >}}.
-   [Linux UVC list of supported devices](http://www.ideasonboard.org/uvc/#devices).
-   [Linux UVC driver & tools – FAQ](http://www.ideasonboard.org/uvc/faq/).

-   [guvview GTK+ UVC Viewer](http://guvcview.sourceforge.net/)
    Gtk3 or Qt5  interface for capturing and viewing video from UVC devices.
    The GTK3 build is available in Debian.



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
