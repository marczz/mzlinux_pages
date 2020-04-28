---
title: FFmpeg and Libav
---

See also {{< iref "codecs" "Codecs" >}} and it's subsection
{{< iref "codecs#media_info" "Media Info" >}},
{{< iref "sound_edit" "Sound Edit" >}},  {{< iref "media_players" "Media Players">}},
{{< iref "streaming" "Streaming" >}}.

------

# References

There are two forks of {{< wp "FFmpeg" >}}, {{< wp "FFmpeg" >}} itself and and
{{< wp "Libav" >}}. Most distributions like _Debian_ and _Ubuntu_ after the fork
switched to _libav_ before comming back in july 2015 to _ffmeg_; while
_Gentoo_ offer both and _Archlinux_ never adopted _libav_ and stick to _FFmpeg_.


[FFmpeg](http://www.ffmpeg.org/) documentation:

-   Official
    [FFmpeg documentation](http://www.ffmpeg.org/documentation.html):
    [FFmpeg general documentation](http://ffmpeg.org/general.html)
    including [list of supported File Formats, Codecs or Features
    ](http://ffmpeg.org/general.html#Supported-File-Formats_002c-Codecs-or-Features),
    [FFMPEG FAQ](http://ffmpeg.org/faq.html),
    [ffmpeg](http://www.ffmpeg.org/ffmpeg.html),
    [ffplay(1)](http://www.ffmpeg.org/ffplay.html),
    [ffprobe](http://www.ffmpeg.org/ffprobe.html),
    [ffserver](http://www.ffmpeg.org/ffserver.html)
-   [ffmpeg wiki](http://trac.ffmpeg.org/wiki)
    -   [Encoding pages](https://trac.ffmpeg.org/wiki#Encoding)
    -   [Encode/YouTube](https://trac.ffmpeg.org/wiki/Encode/YouTube)
    -   [Encode/H.264](https://trac.ffmpeg.org/wiki/Encode/H.264)
    -   [Encode/H.265](https://trac.ffmpeg.org/wiki/Encode/H.265)
    -   [Encode/VP8](https://trac.ffmpeg.org/wiki/Encode/VP8)
    -   [Encode/VP9](https://trac.ffmpeg.org/wiki/Encode/VP9)
    -   [Encode/AV1](https://trac.ffmpeg.org/wiki/Encode/AV1)
        {{< wp "AV1" >}} can save about 30% bitrate compared to VP9 and H.265 / HEVC,
        and about 50% over H.264, while retaining the same visual quality.
    -   [compilation guide for  FFmpeg on Ubuntu, Debian, or Mint
        ](https://trac.ffmpeg.org/wiki/CompilationGuide/Ubuntu)
    -   [Guidelines for high quality lossy audio encoding
        ](http://trac.ffmpeg.org/wiki/Encode/HighQualityAudio)
    -   [AudioChannelManipulation
        ](https://trac.ffmpeg.org/wiki/AudioChannelManipulation)
        gives the options for downmixing audio.


[libav](http://libav.org/) documentation:

-   [libav documentation](http://libav.org/documentation.html):
-   [libav general documentation](http://libav.org/general.html)
    including [list of supported File Formats, Codecs or Features
    ](http://libav.org/general.html#Supported-File-Formats-and-Codecs)
-   [libav FAQ](http://libav.org/faq.html),
-   [avconv](http://libav.org/avconv.html),
-   [avplay](http://libav.org/avplay.html),
-   [avprobe](http://libav.org/avprobe.html),
-   [avserver](http://libav.org/avserver.html)

The following references can be used for both projects.

-   [Debian Wiki: FFMPEG](https://wiki.debian.org/ffmpeg/).
-   [ArchWiki: FFmpeg](https://wiki.archlinux.org/index.php/FFmpeg)
-   [Ubuntu Help: FFmpeg](https://help.ubuntu.com/community/FFmpeg)
-   [Using FFmpeg to manipulate audio and video files
    ](http://howto-pages.org/ffmpeg/) by Howard Pritchett _2012_.
-   [HOWTO Convert video files](http://en.linuxreviews.org/HOWTO_Convert_video_files)
    using ffmpeg.

# Debian packages

The _libavcodecs56_ from official distribution support supports most
existing codecs (MPEG, MPEG2, MPEG4, AC3, DV...), but not some
non-free codecs.
The _libavcodecs56-extras_ __replace__  _libavcodecs56_ by adding AMR
encoders/decoders and AAC encoder. There is an alternative version in debian-multimedia

It seems support more encoders like for _aac_: _libfdk-aac1_ and
_libfaac0_  add to _ibvo-aacenc0_ _aac_ android encoder also present
in Debian.

This is dealed with in the Debian Wiki page:
[MultimediaCodecs](https://wiki.debian.org/MultimediaCodecs).

# ffmpeg Memo

## ffmpeg informations

To know available formats and codecs
~~~
$ ffmpeg  -hide_banner -formats
$ ffmpeg  -hide_banner -codecs
~~~

## Identify a stream:

    $ ffprobe -hide_banner "/path/to/input"
    $ avprobe /path/to/input

## Transcode audio

-   to transcode from mp3 to ogg, and resample to 32k Hz

        /usr/bin/ffmpeg -y -i "/path/to/input.mp3" \
          -acodec libvorbis -aq 3 -vn -ac 2 -ar 32000 \
          "/path/to/output.org"

    -   `-i input`: give input file
    -   `-acodec libvorbis`: tells to use the codec libvorbis for
        encoding.
    -   `-aq 3`: Set the audio quality, here 3 as libvorbis (VBR)
        quality. This is an alias for `-q:a 5`?
    -   `-ac 2`: Set the number of channels.
    -   `-ar 32000`: Set the audio resampling frequency.

-   to transcode from mp3 to opus, and resample to 64k mono

        avconv -i input.mp3 -codec:a libopus \
          -ac:a 1 -b:a 64k output.opus

    but it seems (in 2015) that the opus support is not perfect and
    opusinfo gives warnings in the output file.

    Better use:

        avconv -i input.mp3 -f wav | \
          opusenc --bitrate 64 --downmix-mono -  output.opus

    This method can be used for any format understood by `avconv`
    when there is an other known decoder we can prefer it like:

        mpg123 --quiet --wav - input.mp3  | \
          opusenc --bitrate 64 --downmix-mono - output.opus

    Note that `opusenc` default for >=44.1kHz mono input is 64kbps, so
    you can also omit the bitrate parameter.

## lower quality of audio

`input.webm` is a 1h21 speech,stereo opus encoded stream at at 105 kb/s, giving a file
of 62M, we downmix to mono, reencode in vbr at 32kb/s, and change container to ogg with:

    $ ffmpeg -i input.webm -c:a libopus -vbr on -ac 1 -b:a 32k ouput.ogg

-   `-c:a libopus` give the audio codec encoder.
-   `-ac 1` number of channel, here in output.
-   `-b:a 32k` bitrate

The result is a 19M file.

## change container

To change container  without transcoding an opus file from a webm container to an ogg
one.

~~~
ffmpeg -i input.webm -acodec copy output.ogg
~~~

In the same way to change a video from a webm container to a mkv one without transcoding

~~~
ffmpeg -i  input.webm -acodec copy -vcodec copy output.mkv
~~~

# screencasting with ffmpeg
 * Distribution version does not support many format
   and you may have to compile ffmpeg.
 * [Archlinux: FFmpeg screencast example
   ](https://wiki.archlinux.org/index.php/FFmpeg#Screen_cast)
 * Record high quality screencasts with:
~~~~~~~~~~~~~~~
ffmpeg -f oss -i /dev/dsp -f x11grab -s 1024x768 -r ntsc  -sameq -i :0.0 foo.avi
~~~~~~~~~~~~~~~
 * an other command with bitrate 1000 (increase it to get better quality, but larger files); x11:0,0 tells FFmpeg to
 record from the top-left cornet of the screen.. 1280x1024" is your screen resolution, or that of the window you want to
 record. In that case, you can use xwininfo -frame
~~~~~~~~~~~~~~~
./ffmpeg -vcodec mpeg4 -b 1000 -r 10 -g 300 -vd x11:0,0 -s 1280x1024 test.avi
~~~~~~~~~~~~~~~
 * third with further postprocessing with libx264 from
 [Screencasts in Ubuntu, part 2: FFmpeg](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-2/). It uses the options
 -an to turn the sound recording off, <width>x<height> +<ox>,<oy>  - the size of the recorded area plus the upper left corner,
 <fps> is the number of frames per second, for example: 15, <quality-bps> is in bits/seconds you can add a k to have kbits/sec,
 -sameq  use the same quality as in the input so in the case of x11grab it is the maximal value,
~~~~~~~~~~~~~~~
# The recording of the screen into a video
ffmpeg [-an] -s <width>x<height> -r <fps> -f x11grab -i \
:0.0[+<ox,oy>] -codec mpeg4 -sameq -y <temporary-file>.mp4
# The first processing into H.264
ffmpeg -i <temporary-file i> -vcodec libx264 -pass 1 \
[<quality-bps>](-b) -f mp4 -y /dev/null
# The second processing into H.264
ffmpeg -i <temporary-file> -vcodec libx264 -pass 2 \
[<quality-bps>](-b) -f mp4 -y <final-file>.mp4
~~~~~~~~~~~~~~~

~~~~~~~~~~~~~~~
ffmpeg -an -s 800x600 -r 15 -f x11grab -i :0.0+0,25 \
-vcodec mpeg4 -sameq -y scast-temp.mp4
ffmpeg -i scast-temp.mp4 -vcodec libx264 -pass 1 -b 240000 \
-f mp4 -y /dev/null
ffmpeg -i scast-temp.mp4 -vcodec libx264 -pass 2 -b 240000 \
-f mp4 -y scast.mp4
~~~~~~~~~~~~~~~

 * to Convert other video format to FLV (ar: audio samping rate in Hz , ab: audio bit rate in kbit/s, f: output format) _the influence on size of dividing by 2 default ar and ab seems minor_ but addin a video rate of -r 10 (def 25) gain 1/3 of size.
~~~~~~~~~~~~~~~
 ffmpeg -i video.avi -ar 22050 -ab 32 -f flv -s 320x240 video.flv
~~~~~~~~~~~~~~~
 * idem with metadata
~~~~~~~~~~~~~~~
ffmpeg -i video.avi -ar 22050 -ab 32 -f flv -s 320x240 - | flvtool2 -U stdin video.flv
~~~~~~~~~~~~~~~
 * or this one has a slow frame rate 6 (def 30) and high bitrate 300 (def 25)
~~~~~~~~~~~~~~~
ffmpeg -i video.ogg -y -vcodec flv -b 300k -s 320x240 -r 6 -croptop 6 -cropbottom 6 -f flv video.flv
~~~~~~~~~~~~~~~
 * Return one particular jpeg image of the frame based on start (ss)
~~~~~~~~~~~~~~~
    ffmpeg -i video.flv -an -ss 00:00:03  -vframes 1 -an -f rawvideo- -s 320×240 video.jpg
~~~~~~~~~~~~~~~
 * Return first frame of video as jpeg image, you can replace -s by  -sameq
~~~~~~~~~~~~~~~
    ffmpeg -i video.flv -vcodec png -vframes 1 -an -f rawvideo -s 320×240 video.jpg
~~~~~~~~~~~~~~~

 * We can easily transcode mpeg to flv or swf using ffmpeg. On mozilla the flash player (adobe) give a result not clear with the produced swf, we have a better one with mplayer


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
