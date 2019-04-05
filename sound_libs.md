---
title: Sound and Video Processing Libraries
---

{{% toc /%}}

# Sound Libraries
[audiofile](http://www.68k.org/~michael/audiofile/) <a name="audiofile"></a>
:   The Audio File library is an implementation of SGI's Audio File
    Library, which provides an API for accessing audio file formats
    like AIFF/AIFF-C, WAVE, and NeXT/Sun .snd/.au files. This library
    is used by the {{< iref "streaming#esound" "EsounD" >}} daemon,
    {{< iref "media_players#alsaplayer" "AlsaPlayer" >}},
    {{< iref "sound_edit#ecasound" "Ecasound" >}},
    {{< iref "media_players#glame" "Glame" >}}, brasero, ekiga,
    madplay, mplayer and a lot of gnome libraries ...
:   It provides {{< iref "sound_edit#sfconvert" "sfconvert" >}} to
    convert between the aiff, aifc, next, or wave formats and `sfinfo`
    to prints information regarding files from this format.


ladcca)<a name="ladcca"></a>
:   LADCCA stands for Linux Audio Developer's Configuration and
    Connection API. It is a session management system for audio
    applications on GNU/Linux. It understands the
    {{< iref "streaming#jack" "Jack" >}}
    low latency audio API and the {{< iref "sound_edit#alsa" "Alsa" >}} MIDI sequencer
    interface.
:   [LASH](http://www.nongnu.org/lash/)
    stands for Linux Audio Session Handler. It is a session management
    system for audio applications on GNU/Linux. It understands the
    {{< iref "streaming#jack" "Jack" >}} low latency audio API and the
    {{< iref "sound_edit#alsa" "Alsa" >}} MIDI sequencer interface.

[Ladspa](http://www.ladspa.org/) (Linux Audio Developer's Simple Plugin API)<a name="ladspa"></a>
:   Ladspa plugins:
:   [CMT](http://www.ladspa.org/cmt)
    :   The Computer Music Toolkit (CMT) is a collection of LADSPA
        plugins for use with software synthesis and recording packages on
        Linux.

:   Ladspa is used by
    {{< iref "sound_edit#ardour" "Ardour" >}},
    {{< iref "sound_edit#ecasound" "Ecasound" >}}, *GNU Sound*,
    {{< iref "streaming#gstreamer" "GStreamer" >}},
    {{< iref "sound_edit#audacity" "audacity" >}},
    {{< iref "streaming#muse" "MusE" >}},
    {{< iref "sound_edit#rezound" "ReZound" >}},
    {{< iref "sound_edit#snd" "Snd" >}},
    {{< iref "sound_edit#sweep" "Sweep" >}}

[libao](http://www.xiph.org/ao/)<a name="libao"></a>
:   Libao is a cross-platform audio library that allows programs to
    output audio using a simple API on a wide variety of platforms. It
    supports: null output, wav, au, oss (Open Sound System), alsa,
    alsa09 (alsa version 0.9x or 1.x), polypaudio (next generation
    GNOME sound server), esd (Enlighten Sound Daemon), nas (Network
    Audio Server), irix and sun. The driver is given in
    `/etc/libao.conf` or `.libao` with the syntax `default_driver=x`

:   Libao is needed by
    {{< iref "media_players#mpg321" "mpg321" >}}, the python bindins
    are provided by the package pyao.

:   An interesting feature of the {{< iref "streaming#esound" "esd" >}} driver of
    libao is the possibility to send sound to networked computer by
    using the option `"host=hostname:port"`.

libfishsound
:   FishSound (libfishsound) provides a simple programming
    interface for decoding and encoding audio data using the codecs
    {{< iref "#vorbis" "Vorbis" >}}and{{< iref "#speex" "Speex" >}}.

:   Refs:[libfishsound api](http://www.annodex.net/software/libfishsound/html/)

[libmad](http://www.underbit.com/products/mad/) <a name="libmad"></a>
:   MAD (libmad) is a high-quality MPEG audio decoder available under GPL. It currently
    supports MPEG-1 and the MPEG-2 extension to Lower Sampling
    Frequencies, as well as the so-called MPEG 2.5 format. All three
    audio layers (Layer I, Layer II, and Layer III a.k.a. MP3) are
    fully implemented.
    {{< iref "sound_players#madplay" "madplay" >}}
    is a command line front-end to libmad.

    The [Mad home page](http://www.underbit.com/products/mad/) cite
    eighty applications using libmad. It is the most popular free mpeg
    decoding library.

[liboggz](https://xiph.org/oggz/doc/)<a name="liboggz"></a>
:   Oggz provides a simple programming interface for reading and
    writing Ogg (cf. {{< iref "#vorbis" "Vorbis" >}}, {{< iref "#libogg" "libogg" >}})
    files and streams.

[Ogg Vorbis](node/codecs#ogg_vorbis "Internal reference")
:   Ogg Vorbis is a GPLed compressed audio format for audio and
    music at fixed and variable bitrates from 16 to 128 kbps/channel.
    Look at [Technical Details in Wikipedia Vorbis page
    ](http://en.wikipedia.org/wiki/Vorbis#Technical_details).

    - Libogg is a library for manipulating Ogg bitstream. , the
    python bindins are provided by the package pyogg.
    - The {{< iref "#libogg" "libvorbis" >}} package contains runtime
    libraries for use in programs that support Ogg Vorbis.
    - See also {{< iref "#libfishsound" "libfishsound" >}} and
    {{< iref "#liboggz" "liboggz" >}}for a programming interface
    - [xiph.org  Ogg homepage](http://www.xiph.org/ogg/).
    _(in french:  [page francophone du format Ogg Vorbis](http://ptaff.ca/ogg/)
    )_.
   -  A list of ogg vorbis players is provided by the
    [PortablePlayers Wiki](http://wiki.xiph.org/index.php/PortablePlayers)

[libsndfile](http://www.mega-nerd.com/libsndfile/) <a name="libsndfile"></a>
:   Libsndfile is a C library for reading and writing files
    containing sampled sound (such as MS Windows WAV and the Apple/SGI
    AIFF format)
:   refs:
    [libsndfile API](http://www.mega-nerd.com/libsndfile/api.html),
    [sndfile-convert(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-convert(1))
    converts sound files from one format to another,
    [sndfile-info(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-info(1))

    [sndfile-play(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-play(1))
    ,
    [sndfile-resample
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-resample(1))
    is a sample rate converter.

:   libsndfile is required by {{< iref "media_players#alsaplayer" "alsaplayer" >}}
    {{< iref "#libsamplerate" "libsamplerate" >}} {{< iref "sound_edit#sweep" "sweep" >}}
    {{< iref "streaming#jack" "jack-audio-connection-kit-example-clients" >}}.

[libsamplerate](http://www.mega-nerd.com/SRC/))<a name="libsamplerate"></a>
:   Secret Rabbit Code (aka libsamplerate) is a Sample Rate
    Converter for audio.
:   refs: [sndfile-resample(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=sndfile-resample(1))



[SDL](http://www.libsdl.org/)
:   Simple DirectMedia Layer (SDL) is a cross-platform multimedia
    library designed to provide fast access to the graphics frame
    buffer and audio device.
:   SDL\_net is a portable network library for use with SDL.


# Alsa {#alsa}
Alsa is packaged as three packages, alsa-utils, alsa-lib,
alsa-driver

## Documentation on alsa
-   [ALSA project](http://www.alsa-project.org/)
    page, and
    [Documentation](http://www.alsa-project.org/main/index.php/Documentation),
    [Asoundrc](http://www.alsa-project.org/main/index.php/Asoundrc).
-   [Linux ALSA sound notes](http://www.sabi.co.uk/Notes/linuxSoundALSA.html)
    are notes about configuring ALSA. _2008_
-   [AlsaOpensrcOrg unofficial wiki](http://alsa.opensrc.org/)
-   [Gentoo Wiki: ALSA](https://wiki.gentoo.org/wiki/ALSA)
    [HOWTO ALSA Complete (includes dmix)](http://gentoo-wiki.com/HOWTO_ALSA_sound_mixer_aka_dmix).
-   [ArchLinux Alsa Guide
    ](http://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture),
    [Advanced Linux Sound Architecture/Example Configurations
    ](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture/Example_Configurations),
    [Advanced Linux Sound Architecture/Troubleshooting
    ](https://wiki.archlinux.org/index.php/Advanced_Linux_Sound_Architecture/Troubleshooting).
-   [Debian Wiki: Alsa
    ](https://wiki.debian.org/ALSA)
-   [Wikibook: Configuring Sound on Linux
    ](https://en.wikibooks.org/wiki/Configuring_Sound_on_Linux)

## Alsa components

Alsa pcm plugins
:   The configuration of alsa is done via the asoundrc file, it is
    documented at
    [alsa-project: asoundrc
    ](http://www.alsa-project.org/main/index.php/Asoundrc)
    a copy is in
    [alsa.opensrc wiki: asoundrc
    ](http://alsa.opensrc.org/Asoundrc).
:   [Alsa project pcm plugins page
    ](http://alsa-project.org/alsa-doc/alsa-lib/pcm_plugins.html)
:   [alsa.opensrc.org](http://alsa.opensrc.org/):
    [Plugin documentation](http://alsa.opensrc.org/Plugin_Documentation)
:   [HOWTO ALSA sound mixer aka dmix
    ](http://gentoo-wiki.com/HOWTO_ALSA_sound_mixer_aka_dmix)
    this how-to explains the old conf setting for dmix which is no
    longer necessary since v. 1.09
:   [alsa.opensrc.org: Dmix Plugin HowTo
    ](http://alsa.opensrc.org/DmixPlugin)

alsa-driver
:   Alsa drivers are a set of drivers compatible with OSS/Lite but
    with improved features.
:   Refs:
    [Alsa lib driver Documentation](http://alsa-project.org/alsa-doc/alsa-lib/),
    [alsa sound cards](http://alsa.opensrc.org/Sound_cards).

alsa-utils
:   offers the following programs:
:   alsactl
    :   [alsactl(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=alsactl(1))
        utility
        for store / restore of soundcard settings
    aplay/arecord
    :   [aplay(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=aplay(1))
        utility for  playback / record of `.wav`,`.voc`, `.au` files.
    amixer
    :   [amixer(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=amixer(1))
        a command line mixer
    alsamixer
    :   [alsamixer(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=alsamixer(1))
        ncurses mixer
    aconnect
    :   [aconnect(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=aconnect(1))
        utility to connect and disconnect two existing ports
        on ALSA sequencer system

alsa-lib
:   provides the libasound library. There is an api manual

## Alsa devices
Alsa put devices information and control in `/proc/asound`. The
layout of the alsa proc subsytem is explained in the
[Proc asound documentation
](https://alsa.opensrc.org/Proc_asound_documentation)
of the [Alsa Wiki](http://alsa.opensrc.org/).

The list of cards is in `/proc/asound/cards` so on one laptop I have:

    $ cat /proc/asound/cards
     0 [HDMI           ]: HDA-Intel - HDA Intel HDMI
                          HDA Intel HDMI at 0xb0610000 irq 47
     1 [PCH            ]: HDA-Intel - HDA Intel PCH
                          HDA Intel PCH at 0xb0614000 irq 45

Each card has a directory in `/proc/asound/` so if I want to have info on the playback
if the pcm in the card numer 1, I look in `cat /proc/asound/card1/pcm0p/info`.

But now the `/sys` filesystem is to be preferred and the alsa devices are in
`/sys/class/sound/` so the `car1` is a

     $ cat /sys/class/sound/card1/id
     PCH

And we find the directories for each device control, hw dvices, and pcm inthe directory
`/sys/class/sound`.

For the devices we look at:

    $ cat /proc/asound/devices
      2: [ 1]   : control
      3: [ 1- 0]: digital audio playback
      4: [ 1- 0]: digital audio capture
      5: [ 1- 0]: hardware dependent
      6: [ 0]   : control
      7: [ 0- 3]: digital audio playback
      8: [ 0- 7]: digital audio playback
      9: [ 0- 8]: digital audio playback
     10: [ 0- 0]: hardware dependent
     33:        : timer

The first number is the card number, the second the device number.

they appear as device in `/dev/snd` directory They are named in the form `aaaCxDy` where
`aaa` is the service name, `x` is the card number (0-7), and `y` the device number (0-?)

The service names can be `pcm`, `hw`, `seq` _sequencer_, `timer`, `control`
_mixer, etc._

For the previous example we hve two hardware cards that appear as devices as `hwC0D0`,
`hwC1D0`, with their respective control the devices `controlC0` and `controlC1`.

For the `pcm`s we have for the card number 1 (PCH)  one control,
one playback, and one capture which gives the devices
`controlC1`, `pcmC1D0p`, `pcmC1D0c`.

For the card number 0 (HDMI) we have one control,
and four playbacks  wich appear as device in `/dev/snd` as
`controlC0`, `pcmC0D3p`, `pcmC0D7p`, `pcmC0D8p`

The playback devices will also be listed by `aplay --list-devices` or `aplay -l` and
the record devices by `arecord --list-devices` or `arecord -l`.

If you loaded the `snd-pcm1-oss` module, you can also use
the OSS-compatibility to access your sound card. It provides mapping from
`/dev/snd/pcmCxD0` devices to `/dev/audiox`, `/dev/dspx` and
`/dev/snd/pcmCxD1` devices to `/dev/adspx`.

The `snd-mixer-oss` module as well, allows to use the
backwards compatible mixer.

You can use these hardware devices directly for recording or playing but the sound must
exactly fit the hardware. On my PCH card I can play

    $ aplay -D hw:1,0 -c 2 -f S16_LE -r 48000 /tmp/gong.snd

Because the hardware is set to two channels, signed 16 bits low endian 48000Hz, but any
sound that does not follow these norm will not be played. (For the rate 48000HZ and
44100Hz are allowed, for the format S16_LE and S32_LE)

To play an other file we can add software conversion with a virtual pcm predefined in
alsa which is `plughw`.

    $ aplay -D plughw:1,0  /tmp/train2.wav
    Playing WAVE '/tmp/train2.wav' : Float 32 bit Big Endian, Rate 11025 Hz, Stereo

Here the the encoding (float 32), the endianess, and the rate are converted before to be
directed to the hardware sound card.

Instead of giving devices numbers, I can select the device by name so the last command
can also be written:

    $ aplay -D plughw:PCH /tmp/train2.wav
    Playing WAVE '/tmp/train2.wav' : Signed 32 bit Big Endian, Rate 11025 Hz, Stereo

The conversion of format is done by using the `plug` conversion and a slave pcm; ici
`plughw:1,0` is an abbreviated form of `-D "plug:'hw:1,0'"`.

## Pulseaudio

Pulseaudio sound server is
{{< iref "streaming#pulseaudio" "in the streaming section" >}}

# Video Libraries

Theora<a name="theora"></a>
:   Theora is an open video codec being developed by the Xiph.org Foundation
    as part of their Ogg project.

    Refs: [Theora web site](http://www.theora.org/) and
    [FAQ](http://www.theora.org/theorafaq.html)


DVB and Video4Linux<a name="v4l"></a>
:   The [LinuxTV project](http://www.linuxtv.org/) develops and maintains
    the DVB driver subsystem which is included in the Linux 2.6.x kernel,
    DVB links are in the
    [DVB Wiki](http://www.linuxtv.org/wiki/index.php/Main_Page).
    [Video4Linux (V4L)](http://www.linuxtv.org/v4lwiki/index.php/Main_Page)
    is intended to provide a common programming interface for TV, capture cards,
    parallel port and USB video cameras.

SDL
:   see {{< iref "#sdl" "in sound libraries" >}}

General Graphic Interface (GGI))<a name="gci"></a>
: The {{< wp "General Graphics Interface" >}} project aims to
develop a reliable, stable and fast graphics system that works
everywhere.



<!--  Local Variables: -->
<!--  ispell-local-dictionary: "english" -->
<!--  mode: markdown -->
<!--  End: -->
