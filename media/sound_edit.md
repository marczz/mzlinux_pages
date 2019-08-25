---
title: Sound encoders and editors
---

{{% toc /%}}

# Low level encoders
The {{< iref "video_edit" "Video Encoders" >}}
are often also audio encoders. In the
{{< iref "video_edit" "Video Encoders" >}}
page you find
{{< iref "video_edit#libav" "libav" >}},
{{< iref "video_edit#ffmpeg" "ffmpeg" >}},
{{< iref "video_edit#mencoder" "Mencoder" >}},
which are also audio  audio encoders.

## encoder list
lame
:   LAME create mp3 compressed audio files.

:   In variable bit rate (`--vbr-old` or `--vbr-new` the quality
    (set by the `-V` switch) range from 9 (lowest quality/biggest
    distortion) to 0 (highest quality/lowest distortion).

:   To use it with variable bit rate and the preset `standard`
    which should generally be transparent to most people on most music
    and is already quite high in quality, use this command.
    `lame --vbr --preset standard infile.wav outfile.mp3` The resulting
    bitrate should be in the 170-210kbps range, according to music
    complexity.

:   preset `medium` provide near transparency to most people on
    most music. The resulting bitrate should be in the 150-180kbps
    range, according to music complexity.

:   preset `extreme`, if you have extremely good hearing and
    similar equipment, will generally provide slightly higher quality
    than the standard mode. The resulting bitrate should be in the
    200-240kbps range, according to music complexity.

:   refs: [lame(1)
](http://manpages.debian.org/cgi-bin/man.cgi?query=lame(1))


bladeenc
:   BladeEnc is a freeware MP3 encoder. It is based on the same ISO
    compression routines as mpegEnc, but it is more than three times
    faster, and it works with several popular front-end graphical user
    interfaces .

Mp3Wrap
:   is a command-line utility that wraps quickly two or more mp3
    files in one single large playable mp3, without losing filenames
    and ID3 informations (and without need of decoding/encoding). Also
    with the possibility of including other non mp3 files inside the
    mp3.
:   Refs: [Mp3Wrap Homepage](http://mp3wrap.sourceforge.net/),
    [mp3wrap(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3wrap(1))

:   __Mp3Splt__ is a command line utility to split mp3 and ogg files
    selecting a begin and an end time position, without decoding.
:   Refs: [mp3splt Home Page](http://mp3splt.sourceforge.net),
    [mp3splt(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3splt(1))


<a name="vorbistools"></a>Vorbis tools
:   The {{< iref "codecs#ogg_vorbis" "vorbis" >}} package contains
    runtime libraries for use in programs that support Ogg Vorbis, as
    well as an encoder `oggenc`, a decoder `oggdec`, a tool to split
    vorbis files `vcut`, a playback tool `ogg123`, and a comment editor
    `vorbiscomment`.

:   refs: [ogg123(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogg123(1))
    ,
    [oggenc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=oggenc(1))
    ,
    [oggdec(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=oggdec(1))
    ,
    [vcut(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=vcut(1))
    ,
    [ogginfo(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogginfo(1))
    ,
    [vorbiscomment(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=vorbiscomment(1))
    .

<a name="ogmtools"></a>ogmtools
:   These tools allow information about (ogminfo) or extraction
    from (ogmdemux) or creation of (ogmmerge) OGG media streams. Note
    that OGM is used for "OGG media streams" .They can be used for
    video as for sound.

:   Refs [ogmdemux(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogmdemux(1))
    ,
    [ogminfo(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogminfo(1))
    ,
    [ogmmerge(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogmmerge(1))

    [ogmsplit(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=ogmsplit(1))
    .

 <a name="flac"></a>FLAC
:   FLAC stands for Free Lossless Audio Codec. The FLAC project
    consists of the stream format, reference encoders and decoders in
    library form, flac, a command-line program to encode and decode
    FLAC files, metaflac, a command-line metadata editor for FLAC files
    and input plugins for various music players

:   refs:[flac.sourceforge.net](http://flac.sourceforge.net/),
    [Flac Documentation](http://flac.sourceforge.net/documentation.html)
    (including man pages), [flac(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=flac(1))
    ,
    [metaflac(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=metaflac(1))


<a name="speex"></a>[Speex](http://www.speex.org/)
:   Speex is a patent-free audio codec designed especially for
    voice.

:   See also {{< iref "sound_libs#libfishsound" "libfishsound" >}} for a
    programming interface

:   refs:[speex.org](http://www.speex.org/),
    [speex manual](http://www.speex.org/docs/manual/speex-manual/),
    [speexenc(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=speexenc(1))
    ,
    [speexdec(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=speexdec(1))

faac
:   is the abbreviation for "Freeware Advanced Audio Coder" the
    program and options is described in the
    [Faac page of the AudioCoding.com knowledge base
    ](http://www.audiocoding.com/modules/wiki/?page=FAAC)

faad2
:   FAAD 2 is a GPL AAC audio encoder.

:   Refs [audiocoding.com](http://www.audiocoding.com/)


## encoders frontends
[audio convert](https://savannah.nongnu.org/projects/audio-convert/)
:   audio convert is a a script to convert wav, ogg, mp3, mpc, flac, ape
    or wma format. It uses MPlayer to decode WMA files, musepack-tools
    to manipulate MPC audio files, and flac. It is mainly a command line
    utility, but uses zenity to provide a GUI. audio convert is packaged
    in ubuntu as *nautilus-script-audio-convert*.*audio convert is
    unchanged since 2005*

[Asunder](http://littlesvr.ca/asunder/index.php)
:   Asunder (GPL) is a graphical Audio CD ripper and
    encoder for Linux. It can encode tracks from an Audio CD as WAV,
    MP3, OGG, FLAC and/or WavPack. Precompiled packages for Asunder are
    available for main distributions including Debian and Ubuntu.

[dir2ogg](http://jak-linux.org/projects/dir2ogg/)
:   dir2ogg (GPL) is a python script which converts mp3, m4a, wma, and
    wav files into ogg-vorbis format.

[Grip](http://nostatic.org/grip/) <a name="grip"></a>
:   Grip is a GTK+ based front-end for CD rippers (such as
    {{< iref "#cdparanoia" "cdparanoia" >}} and {{< iref "#cdda2wav" "cdda2wav" >}}) and
    MP3 encoders as {{< iref "#bladeenc" "bladeenc" >}}, {{< iref "#vorbisyools" "oggenc" >}}
    , lame , ... Grip allows you to rip entire tracks or just a section
    of a track. Grip supports the CDDB protocol for accessing track
    information on disc database servers. Gcd is the included cd
    player.

:   refs:[Grip Home Page](http://nostatic.org/grip/),
    [grip(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=grip(1))
    ,
    [Grip sourceforge project](http://sourceforge.net/projects/grip/Grip),
    [Grip User's Guide](http://nostatic.org/grip/doc/index.html)

[ripit](http://www.suwald.com/ripit/ripit.html)
:  RipIT can create
   mp3, flac, Ogg Vorbis, or Faac (m4a) from wav audio files extracted
   from an audio CD. It is a console based front-end written in Perl.
   It uses the following backends:

   * dagrab, cdparanoia or cdda2wav for ripping the audio CD tracks.
   * Lame, OggVorbis, Flac or Faac for encoding the wav files to mp3,
   ogg, flac or m4a
   * Perl module CDDB\_get >= 2.25 for CDDB retrieval

   It can add id3tags, create a m3u playlist, and generate a toc (cue)
   sheet for DAO burning.

[RipperX](http://sourceforge.net/projects/ripperx/)
:   A GTK-based audio CD ripper/encoder that can encoding
    into the OGG, FLAC, or MP2/3 formats using the vorbis tools, FLAC,
    toolame, mpg123.

[RippOff](http://ripoffc.sourceforge.net)
:   RippOff is a GTK+ based CD Ripper for
    Linux it can rip to ogg-vorbis, flac, and mp3 (with an extra mp3
    plugin)

[Serpentine](http://irrepupavel.com/projects/serpentine/)
:   *Serpentine* (
    [Serpentine project page](http://developer.berlios.de/projects/serpentine/)
    is a light cd audio recording
    application for Gnome. that is written in python and uses
    gstreamer. It supports the same codecs than gstreamer such as WAV,
    MP3, OGG, FLAC. Serpentine requires gnome2.

# High Level sound editors
## Desktop editors
<a name="audacity"></a>[audacity](http://audacity.sourceforge.net/)
:   {{< wp "Audacity" >}} (GPL) is a free audio editor. You can record sounds, play
    sounds, import and export wav, aiff, Vorbis, and MP3 files, mix
    tracks together, or apply effects to your recordings. It also has a
    built-in amplitude envelope editor, a customizable spectrogram mode
    and a frequency analysis window for audio analysis applications.

    [Audacity manual, Quick Reference Guide and FAQ
    ](http://audacity.sourceforge.net/help/documentation) are available on the main site
    [Audacity Wiki](http://wiki.audacityteam.org/)
    propose many [Tutorials
    ](http://wiki.audacityteam.org/index.php?title=Tutorials) and
    [Tips](http://wiki.audacityteam.org/index.php?title=Tips),
    mainly recording tips.

    [LibriVox Wiki](http://wiki.librivox.org/index.php/Main_Page) has many
    [Audacity Tutorials](http://wiki.librivox.org/index.php/Audacity_Tutorials)

    Audacity allow to do noise removal also called
    {{< wp "Audio_restoration" >}}, it is explained in
    [Audacity Documentation: Noise Reduction](http://wiki.audacityteam.org/wiki/Noise_Reduction)
    and further detailled in [Detailed Audacity Noise Removal
    ](http://wiki.librivox.org/index.php/Detailed_Audacity_Noise_Removal)
    in the pages of
    [LibriVox Wiki](http://wiki.librivox.org/index.php/Main_Page)
    on [Noise Cleaning](http://wiki.librivox.org/index.php/Noise_Cleaning)

<a name="ardour">[Ardour](http://ardour.org/)
:   {{< wp "Ardour" >}} (GPL) is a powerful multitrack Hard-Disk Recording system by
    Paul Davis and others. It supports
    {{< iref "sound_libs#ladspa" "LADSPA" >}} audio filter
    plugins.
:   [Ardour sourceforge page](http://ardour.sourceforge.net),
    [LAU doc on ardour](http://www.djcj.org/LAU/ardour).

 <a name="ceres"></a> __Ceres__(BSD like license)
:   _Ceres_  is a spectral domain editor for audio files.
    Ceres is originally developed by Oyvind Hammer, and later
    by Kjetil S. Matheussen ([Ceres3](http://www.music.lumbia.edu/%7Estanko/About_Ceres3.html)).
    [Ceres4](https://github.com/jeremysalwen/Ceres4) from Jeremy Salwen
    currently consists of Ceres ported to the gtk2 platform.

 <a name="dir2ogg">[dir2ogg](http://jak-linux.org/projects/dir2ogg/) (GPL)
:   _dir2ogg_ is a python script which converts mp3, m4a, wma,
    and wav files into ogg-vorbis format. It uses _mplayer_, _mpg123_
    or _lame_, _faad_, _flac_, _mpcdec_, _cdparanoia_ or _cedax_ or
    _cdda2wav_.<br /> {{< iref "#xcfa" "XCJA" >}} is an
    alternative to _dir2ogg_.

{{< wp "Ecasound" >}}<a name="ecasound"></a>
:   [ecasound (__Home__)](http://nosignal.fi/ecasound/)
    (GPL) is a sound processing application designed for basic
    effect processing, mixing, multitrack recording and signal
    recycling. It supports OSS and {{< iref "sound_libs#alsa" "ALSA" >}} sound drivers,
    wav, mp3, aiff, cdda, au, snd, raw and standard file streams

<a name="gnac">[gnac](http://gnac.sourceforge.net/) (GPL)
:   _Gnac_ is an audio conversion program for GTK3 using Gstreamer,
    like {{< iref "video_edit#oggconvert" "OggConvert" >}}
    and {{< iref "#soundconverter" "SoundConverter" >}}.
    But _gnac_ and _oggconvert_ have less gnome dependencies than
    SoundConverter.

[GNU Sound](http://www.gnu.org/software/gnusound/)
:   __Gnu sound__ (GPL) is a multitrack sound editor for Gnome.

{{< wp "Jokosher" >}}
:   __Jokosher__ (GPL) is a non-linear multi-track digital audio
    editor,it is being developed in Python,
    using the GTK+ interface and GStreamer as an audio back-end.

{{< iref "video_edit#oggconvert" "OggConvert" >}}
:   __0ggconvert__ (LGPL) convert audio and video files of various
    types into  Ogg Vorbis audio format, and video formats. It uses _GStreamer_<br />
    {{< iref "#soundconverter" "SoundConverter" >}},
    and {{< iref "#gnac" "gnac" >}},
    {{< iref "video_edit#pitivi" "PiTiVi" >}}
    are  alternatives to
    _OggConvert_.


{{< iref "video_edit#pitivi" "PiTiVi" >}}
:   __PiTivi__ (LGPL) is an audio/video editing software written
    in python CTK+ that uses the gstreamer framework.

<a name="rezound"></a>[Rezound](http://rezound.sourceforge.net)
:   {{< wp "ReZound" >}} (GPL) is a graphical audio file editor. It supports
    {{< iref "sound_libs#ladspa" "LADSPA" >}} audio filter
    plugins. It can use the formats: wave, aiff/aiff/-c, next
    berkeley/ircam/carl, raw, ogg vorbis, mpeg layer 3,2,1, flac, midi
    sample dump. It interfaces with OSS, portaudio, JACK.
    The software has only maintenance releases since long time.

<a name="soundconverter">[SoundConverter](http://soundconverter.org/) (GPL)
:   SoundConverter is a sound converter to ogg/vorbis for Gnome
    using gstreamer, it is similar to
    {{< iref "#gnac" "gnac" >}} and {{< iref "video_edit#oggconvert" "OggConvert" >}},
    but while _oggconvert_ deal both with video and sound formats,
    _soundconverter_ and _gnac_ focus only on sounds.<br />
    _soundconverter_ as more gnome dependencies than _oggconvert_
    or _gnac_, that make it an heavy package if you don't run a
    full gnome desktop.

    SoundConverter reads anything the GStreamer
    library can read (Ogg Vorbis, AAC, MP3, FLAC, WAV, AVI, MPEG, MOV,
    M4A, AC3, DTS, ALAC, MPC, Shorten, APE, SID, etc...), and writes
    WAV, FLAC, MP3, and Ogg Vorbis files.

<a name="snd"></a>[Snd](https://ccrma.stanford.edu/software/snd/)
:   __Snd__  (Artistic License) is a sound editor. It can accommodate any number of sounds
    each with any number of channels, and can be customized and
    extended using either Guile or Ruby.

    __Snd__ is a
    [Center for Computer Research in Music and Acoustics (CCRMA) Software
    ](https://ccrma.stanford.edu/software)

:   Notes:
    For using an other soundcard than `hw:0,0` we have to use the
    environment variables: SNDLIB\_ALSA\_PLAYBACK\_DEVICE,
    SNDLIB\_ALSA\_CAPTURE\_DEVICE, SNDLIB\_ALSA\_DEVICE.
    <br/> example:

        SNDLIB_ALSA_DEVICE="usb-audio" snd

<a name="sox"></a>[SoX](http://sox.sourceforge.net)
:   {{< wp "SoX" >}} _Sound eXchange_ (GPL) is a sound file format converter SoX can
    convert between many different digitized sound formats and perform
    simple sound manipulation functions, including sound effects.
    :   refs:
    -   [SoX Home]((http://sox.sourceforge.net/),
        [sox features](http://sox.sourceforge.net/Docs/Features).
    -   Wikipedia: {{< wp "SoX" >}}
    -   [SoX Documentation](http://sox.sourceforge.net/Docs/Documentation)
    -   manpages: [sox(1)
        ](http://sox.sourceforge.net/sox.html)
        _sox_, can also used with the name _play_ or _rec_ ,
        [soxi(1)
        ](http://sox.sourceforge.net/soxi.html),
    -   [SoX supported formats and devices](http://sox.sourceforge.net/soxformat.html)
    -   [examples scripts
        ](http://sox.sourceforge.net/Docs/Scripts)


<a name="sweep"></a>[Sweep](http://www.metadecks.org/software/sweep/)
:   {{< wp "Sweep_(software)"  "Sweep" >}} (GPL) is an editor for sound samples.
    It operates on `.wav`, `.aiff` and `.au` formats, and has
    multiple undo/redo levels and filters. It supports
    {{< iref "sound_libs#ladspa" "LADSPA" >}} audio filter
    plugins.<br />
   _The last release was in 2008, but it is still in Debian._
:   refs: [sweep(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sweep%281%29),
    [using sweep tutorial](http://www.metadecks.org/software/sweep/tutorials/using_sweep/)

 <a name="xcfa"></a>[X Convert File Audio - XCFA](http://www.xcfa.tuxfamily.org/static2/xcfa) (GPL)
:   XCFA is a tool to extract the content of
    Audio-CDs and convert musical audio files conversion to FLAC, WAV,
    OGG, M4A, MPC, MP3, WavPack, ... _Xcfa_ uses _libasound2_,
    _cdparanoia_, _icedax_ and a choice among many tools to perform
    the re-encoding: _mplayer_, _vorbis-tools_, _lame_, _mppen_c,
    _sox_, etc.<br />
    {{< iref "#dir2org" "dir2org" >}} is
    similar to _Xcfa_ , but has ogg-vorbis as only target format.

## Command line tools

:   [cdda2wav(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdda2wav%281%29)
    is a sampling
    utility for CD-ROM drives that are capable of providing a CD's
    audio data in digital form to your host. Audio data read from the
    CD can be saved as .wav or .sun format sound files. Recording
    formats include stereo/mono, 8/12/16 bits and different rates.
    Cdda2wav can also be used as a CD player.
:   [cdda2ogg(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=cdda2ogg%281%29)
    is a simple script that uses the cdda2wav and ogg123
    to encode audio tracks.
:   cddawav and cdda2ogg are part of the
    {{< iref "189#item_cdrecord" "cdrecord" >}} package

gst-tools
:   This is the basic command-line tools used for
    {{< iref "188#item_gstreamer" "GStreamer" >}}

[mp3diags](http://mp3diags.sourceforge.net/)
:   _mp3diags_ is a program to diagnostic and repair mp3 files.
    It comes with a QT GUI.

[mp3splt
](http://mp3splt.sourceforge.net/mp3splt_page/home.php)
and [Mp3Wrap](http://mp3wrap.sourceforge.net/)
:   mp3splt (Gpl) is an utility for mp3/ogg splitting without
    decoding refs:[mp3splt(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3splt%281%29)
    , it now comes with a gui **Mp3splt-gtk**.

:   Mp3Wrap (Gpl) wraps two or more mp3 files in one single large
    playable mp3, without decoding/encoding and without losing
    filenames and ID3 informations.

## Replay gain

[aacgain]()
:   is a fork and replacement of
    [mp3gain](http://mp3gain.sourceforge.net/)
    that is no longer updated since _2009_ and no longer in Debian.
    It supports AAC (mp4/m4a/QuickTime) audio files in addition
    to mp3 files. _aacgain_ is [available in debian-multimedia
    ](https://www.deb-multimedia.org/dists/testing/main/binary-amd64/package/aacgain)

[normalize](http://normalize.nongnu.org/)
:   normalize is a tool for adjusting the volume of audio files to
    a standard level.
    It is in the Debian package _normalize-audio_
:   refs: {{< man "normalize-audio" >}},
    {{< man "normalize-mp3" >}} (for mp3 __and__ ogg-vorbis)

[Gnormalize](http://gnormalize.sourceforge.net/)
:   Gnormalize is a perl-Gtk2 program that decodes the
    MP3/MP4/MPC/OGG/APE/FLAC file to WAV, then normalizes the WAV to a
    targeted volume level and re-encodes it, optionally in a different
    format.Gnormalize can also extract Audio CD tracks. It uses LAME,
    FAAC, OGGENC, MPPENC, FLAC and MAC encoders/decoders and mpg321,
    mpg123, madplay, MPlayer, mppdec, ogg123, flac123 to play sounds.
    You need only to install the programs needed for the task you
    perform.

[rgain](https://bitbucket.org/fk/rgain/)
:   provides modules to read, write and calculate Replay Gain as
    well as 2 scripts that utilize these modules to do Replay Gain.
    It is in Debian as _python-rgain_

{{< man "vorbisgain" >}}
:   calculate the replay gain for Ogg Vorbis files. _in Debian_.

# Speech synthesis and recognition
{{< wp "Speech_synthesis"  "Wikipedia: Speech synthesis" >}}, {{< wp "Comparison of speech synthesizers" >}},
{{< wp "Speech recognition" >}}, {{< wp "List of speech recognition software" >}},
{{< wp "Speech recognition in Linux" >}}.

[Festival](http://www.cstr.ed.ac.uk/projects/festival/) (BSD License)
:   {{< wp "Festival Speech Synthesis System" >}} is a multi-lingual speech synthesis
    system developed at Centre for Speech Technology Research (CSTR) at the
    University of Edinburgh and Carnegie Mellon University.

    -   [Festival Manual](http://www.cstr.ed.ac.uk/projects/festival/manual/).
    -   [Festvox](http://www.festvox.org/) (MIT License) is a suite of tools
        for building synthetic voices for Festival.
    -   [festlang.berlios.de](http://festlang.berlios.de/docu/doku.php)
        maintain a list of supported languages for Festival.
    -   [Flite](http://www.speech.cs.cmu.edu/flite/) is a small run-time speech
        synthesis engine developed at Carnegie Mellon University.
        Flite is designed as an alternative synthesis engine to Festival
        for voices built using FestVox.
    -   [Multilanguage FLite (ML-FLite)
        ](http://visilab.unime.it/~filippo/MLFLite/MLFLite.htm)
        is able to use both italian and english voices with Flite.
    -   [Mbrola](http://en.wikipedia.org/wiki/MBROLA) (proprietary, closed source,
        distributed at no cost) is a phonemizer for multilingual speech synthesis.
        [Mbrola can be used with the Festival system
        ](http://www.cstr.ed.ac.uk/projects/festival/mbrola.html)

[Espeak](http://espeak.sourceforge.net/) (GPL)
:   Espeak is a compact open source software speech synthesizer written in C++.

    -   Espeak can be used as a
        [front-end to Mbrola](http://espeak.sourceforge.net/mbrola.html)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
