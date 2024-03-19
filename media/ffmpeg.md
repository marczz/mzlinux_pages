---
title: FFmpeg
---

See also {{< iref "codecs" "Codecs" >}} and it's subsection
{{< iref "codecs#media_info" "Media Info" >}},
{{< iref "sound_edit" "Sound Edit" >}},  {{< iref "media_players" "Media Players">}},
{{< iref "streaming" "Streaming" >}}.

------

# References

*{{< wp "FFmpeg" >}}  was forked in 2011 as
{{< wp "Libav" >}}. Many distributions like _Debian_ and _Ubuntu_ after the fork
switched to _libav_ before comming back in july 2015 to _ffmeg. The _libav fork was
abandoned after a last version in 2018.*

## FFmpeg Documentation

-   [FFmpeg Home](http://www.ffmpeg.org/).
-   [FFmpeg documentation](http://www.ffmpeg.org/documentation.html):
-   [FFmpeg general documentation](http://ffmpeg.org/general.html)
-   [list of supported File Formats, Codecs or Features
    ](http://ffmpeg.org/general.html#Supported-File-Formats_002c-Codecs-or-Features),
-   [FFMPEG FAQ](http://ffmpeg.org/faq.html),
-   [ffmpeg](http://www.ffmpeg.org/ffmpeg.html),
-   [ffplay(1)](http://www.ffmpeg.org/ffplay.html),
-   [ffprobe](http://www.ffmpeg.org/ffprobe.html),
-   [ffserver](http://www.ffmpeg.org/ffserver.html)
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
    -   [How To Burn Subtitles Into Video
        ](http://trac.ffmpeg.org/wiki/HowToBurnSubtitlesIntoVideo).


## Other references
-   [Debian Wiki: FFMPEG](https://wiki.debian.org/ffmpeg/).
-   [ArchWiki: FFmpeg](https://wiki.archlinux.org/index.php/FFmpeg)
-   [Ubuntu Help: FFmpeg](https://help.ubuntu.com/community/FFmpeg)
-   [Using FFmpeg to manipulate audio and video files
    ](http://howto-pages.org/ffmpeg/) by Howard Pritchett _2012_.
-   [HOWTO Convert video files](http://en.linuxreviews.org/HOWTO_Convert_video_files)
    using ffmpeg.
-   [20+ FFmpeg Commands For Beginners](https://ostechnix.com/20-ffmpeg-commands-beginners/)
-   [Corpie write](https://write.corbpie.com/) has a lot of
    [ffmpeg posts](https://write.corbpie.com/tag/ffmpeg/) incuding:
    -   H264 encoding comparison of `preset` and `crf`
        [part 1](https://write.corbpie.com/ffmpeg-h264-preset-crf-comparison-2020-pt1/),
        [2](https://write.corbpie.com/ffmpeg-h264-preset-crf-comparison-2020-pt2/),
        [3](https://write.corbpie.com/ffmpeg-h264-preset-crf-comparison-2020-pt3/) and
        [4](https://write.corbpie.com/ffmpeg-h264-preset-crf-comparison-2020-pt4/);
    -   H265 encoding comparison of `preset` and `crf`
        [Part 1](https://write.corbpie.com/ffmpeg-h265-preset-crf-comparison-2020-pt1/),
        [part 2](https://write.corbpie.com/ffmpeg-h265-preset-crf-comparison-2020-pt2/),
        [part 3](https://write.corbpie.com/ffmpeg-h265-preset-crf-comparison-2020-pt3/).
    -   FFmpeg h265 to WebM VP9 encoding comparison:
        [Part 1 h264 `-deadline good`
        ](https://write.corbpie.com/ffmpeg-h264-to-webm-vp9-encoding-comparison-part-1/),
        [Part 2  h264 `-deadline realtime`](https://write.corbpie.com/ffmpeg-h264-to-webm-vp9-encoding-comparison-part-2/),
        [Part 3 h264  `-deadline good` compared to `-deadline realtime`
        ](https://write.corbpie.com/ffmpeg-h264-to-webm-vp9-encoding-comparison-part-3/),
        [part 4 `-deadline good` with `-crf` values 15-30 and `-cpu-used` 0-5
        ](https://write.corbpie.com/ffmpeg-hevc-to-webm-vp9-encoding-comparison-part-4/).

# Debian packages

The _libavcodecs58_ from official distribution support supports most
existing codecs (MPEG, MPEG2, MPEG4, AC3, DV...), but not some
non-free codecs.
The _libavcodecs58-extras_ __replace__  _libavcodecs58_ by adding AMR
encoders/decoders and AAC encoder. There is an alternative version in debian-multimedia

It seems support more encoders like for _aac_: _libfdk-aac2_ add to _ibvo-aacenc0_ _aac_
android encoder also present in Debian; _libkvazaar6_ an HEVC encoder, _libdav1d4_ the
videolan av1 decoder. Also the version of some encoder like x264 or x265 may be more
recent.

So _ffmpeg_ compiled against these libraries support more codecs than the Debian one.

This is dealed with in the Debian Wiki page:
[MultimediaCodecs](https://wiki.debian.org/MultimediaCodecs)
which warn again poluting your source list with a foreign apt reository, but this risk
can be mitigated by using the _preferences_ for apt.

# ffmpeg Memo

## ffmpeg informations

To know available formats and codecs
~~~
$ ffmpeg  -hide_banner -formats
$ ffmpeg  -hide_banner -codecs
~~~

## Identify a stream:

    $ ffprobe -hide_banner "/path/to/input"

## Transcode audio

-   to transcode from mp3 to aac, and resample to 64k Hz
    ``` sh
    ffmpeg -y -i "/path/to/input.mp3" -c:a aac -ac 2 -ar 64k \
      "/path/to/output.ogg"
    ```
    -   `-y` overwrite output without asking
    -   `-i input`: give input file
    -   `-c:a aac`: tells to use the audio codec `aac` for encoding.
    -   `-ac 2`: Set the number of channels.
    -   `-ar 64k`: Set the audio resampling frequency.

-   to transcode from mp3 to ogg opus, and resample to 64k mono
    ``` sh
    ffmpeg -i input.mp3 -c:a libopus -ac:a 1 -b:a 64k output.opus
    ```
    -   `-c:a libopus`: tells to use the audio codec `libopus` for encoding.
    -   `-ac:a 1`: Set the number of channels for the audio stream, here `:a` is
        optional, since the only stream is audio.
    -   `-b:a 64k`: Gives the bitrate for the audio stream.

    We can also use `opusenc` with
    ``` sh
    ffmpeg -i input.mp3 -f wav | \
      opusenc --bitrate 64 --downmix-mono - output.opus
    ```

    This method can be used for any format understood by `ffmpeg`
    when there is an other known decoder we can prefer it like
    for transcoding mp3 to opus:
    ``` sh
    mpg123 --quiet --wav - input.mp3  | \
      opusenc --bitrate 64 --downmix-mono - output.opus
    ```

    Note that `opusenc` default for >=44.1kHz mono input is 64kbps, so
    you can also omit the bitrate parameter.

## lower quality of audio

`input.webm` is a 1h21 speech,stereo opus encoded stream at at 105 kb/s, giving a file
of 62M, we downmix to mono, reencode in vbr at 32kb/s, and change container to ogg with:

    ffmpeg -i input.webm -c:a libopus -vbr on -ac:a 1 -b:a 32k ouput.ogg

-   `-c:a libopus` : the audio codec encoder.
-   `-ac;a 1` : number of audio channels, here in output.
-   `-b:a 32k`: audio bitrate

The result is a 19M file.

## change container

To change container  without transcoding an opus file from a webm container to an ogg
one.

~~~
ffmpeg -i input.webm -c:a copy output.ogg
~~~

In the same way to change a video from a webm container to a mkv one without transcoding

~~~
ffmpeg -i  input.webm -c:a copy -c:v copy output.mkv
~~~

In the two previous examples as we copy all the streams, we may use

~~~
ffmpeg -i  input.webm -c copy output.mkv
~~~

## Keep only audio stream
Without re-encoding:

```sh
ffmpeg -i video.mp4 -map 0:a:0 -c:a copy audio.aac_
```
Note than some software, like apple Ipod, do not recognize the suffix `.aac`, and to
make it usable you have to use the apple preferred `.m4a`, as it is a mp4 container you
can also usem `.mp4`; but it does not show that it is an audio stream.


Here the video stream in both the video and the audio has the same format, say a stereo
48kHZ, 189 kb/s audio stream.

Now we want to mix the channels in a mono audio, reduce the bitrate to 64k, and encode
in opus rather than aac.

```ssh
ffmpeg -i video.mp4 -map 0:a:0 -c:a libopus -vbr on -ac:a 1 -b:a 64k audio.ogg
```



# Extracting some part of streams


Extract the first 10 minutes of a container

~~~
ffmpeg -i input.webm -c copy -t 600 output.webm
~~~

Here 600 is 600 seconds.

The `-time` option can appear both on input or output, to stop the input or output after
this time so:

~~~
ffmpeg -i -t 600 input.webm -c copy -t 600 output.webm
~~~

Will extract the the stream from 10mn to 20mn.

We can use also `-to` to give a position in the stream

~~~
ffmpeg -to 1:00:00 -i input.webm -c copy -to 10:00 output.ogg
~~~

Will extract the portion between 1h and 1h10mn of the webm container and put it in an
ogg container.

## Combining audio and Video

~~~
ffmpeg -i video_file -i audio_file -c:v copy -c:a copy out_file.mp4
~~~

If the video file contains also an audio track we have to tell ffmpeg which stream to
use using the [Map Option](https://trac.ffmpeg.org/wiki/Map).

~~~
ffmpeg -i video.mp4 -i audio.wav -c:v copy -c:a aac -map 0:v:0 -map 1:a:0 output.mp4
~~~


# reducing video size
There are many way of reducing video size, we can change resolution, we can use a more
lossy encoding, at the price of degrading quality, and we can try a more efficient
ancoding scheme.

# Using a sample to test our reencoding
There are number parameters for reencoding, you can change the audio and video codec,
ach codec has numerous parameters, that influence the video quality when this is a lossy
encoding, the size of the file and the transcoding time. Some of these parameter are
better tested visually or audibly, to check if the degradation due to lossy encoding is
perceptible, or even satisfy your needs.

As it would be too long to reencode multiple time a whole movie, it is better to test
your encoding on a sample, you can rxtract it with:
~~~
ffmpeg -ss 00:30:00 -t 00:02:00 -i movie.mp4 -acodec copy -vcodec copy sample.mp4
~~~

Which extract without reencoding a sample of the movie beginning at 30mn and a lenght of
2mn; which make a test file of 3000 frames.

But you may want to experiment separately the video and the audio, you can extract them
with command like:
~~~
ffmpeg -ss 00:30:00 -t 00:02:00 -i movie.mp4 -map 0:a -c:a copy sample.aac
ffmpeg -ss 00:30:00 -t 00:02:00 -i movie.mp4 -map 0:v -c:v copy sample_muted.mp4
~~~

# reencoding video in av1
The `av1` encoding is known to be the most efficient but also the most cpu demanding,
and so the longer, we can use it with:
~~~
ffmpeg -i h264_movie.mp4 -c:v libaom-av1 -crf 30 -b:v 0 av1_movie.mp4
~~~
`crf` is for constant quality, it implies `-b:v 0`, `-crf` is the quality from the
lossless 0 to 63. More details on the page
[Encode/AV1](https://trac.ffmpeg.org/wiki/Encode/AV1).

But if you have not a powerfull CPU it may take days, for only one movie.

# reencoding in H265/H264

{{< wp "High_Efficiency_Video_Coding" "H265" >}} is more efficient than `H264`. But H265 is
enencumbered with patents and not so widely available, neither firefox nor chrome
support it, but VLC or mpv do support it as android and ios, safari.

You have to choose a `CRF` quality from the lossless 0 to the worst 51, 18 is visually
lossless. You double or lower the bitrate by augmenting or lowering CRF of +6/-6.

The quality 28 of x265 correspond to quality 23 of x264

I have benchmarked a 2mn sample of pure video (no sound) encoded in H264 tht
|   size | CRF | speed     |   time |      |
|-------:|----:|-----------|-------:|------|
|  6364k |   - | -         |      - | 514  |
| 49408k |   0 | medium    | 15mn35 | 3367 |
|  2612k |  23 | medium    |  3mn33 | 177  |
|   672k |  29 | ultrafast |  1mn05 | 45   |
|   836k |  29 | superfast |  1mn14 | 56   |
|   944k |  29 | veryfast  |  1mn60 | 64   |
|   944k |  29 | faster    |  2mn02 | 64   |
|  1076k |  29 | fast      |  4mn02 | 73   |
|  1080k |  29 | medium    |  2mn26 | 73   |
|   1288 |  29 | slow      |  7mn16 | 87   |
|   412k |  35 | ultrafast |  0mn57 | 27   |
|   500k |  35 | superfast |  1mn04 | 34   |
|   492k |  35 | veryfast  |  1mn53 | 33   |
|   496k |  35 | faster    |  1mn41 | 33   |
|   580k |  35 | fast      |  3mn08 | 39   |
|   544k |  35 | medium    |  2mn09 | 36   |
|   624k |  35 | slow      |  6mn30 | 42   |
|   644k |  35 | slower    | 26mn52 | 43   |
|        |     |           |        |      |


# Reencoding in VP9
{{< wp "VP9" >}} is royalty free (but not completely patent free) and has an
encoding efficiency comparable to H265 _see wikipedia for comparison_.

It has a wider opensource support than H265. all browsers chromium, firefox, safari,
opera, microoft dge support it. VP9 is supported open source media playesr, including
VLC, MPlayer/MPlayer2/MPV, Kodi, FFplay. It is supported by android.
It has also a good hadware support  in CPUs, see {{< wp "VP9" "wikipedia VP9" >}}
for a list.


# screencasting with ffmpeg
-   Distribution version does not support many format
   and you may have to compile ffmpeg.
-   [Archlinux: FFmpeg screencast example
   ](https://wiki.archlinux.org/index.php/FFmpeg#Screen_cast)
-   Record high quality screencasts with:
    ~~~ sh
    ffmpeg -f oss -i /dev/dsp -f x11grab -s 1024x768 -r ntsc  -sameq -i :0.0 foo.avi
    ~~~

-   an other command with bitrate 1000 (increase it to get better quality,
    but larger files).
    ~~~ sh
    ffmpeg -vcodec mpeg4 -b 1000 -r 10 -g 300 -vd x11:0,0 -s 1280x1024 test.avi
    ~~~
   -   `x11:0,0` tells FFmpeg to record from the top-left cornet of the screen.
   -   `s 1280x1024` is your screen resolution, or that of the window you want to
         record. In that case, you can use `xwininfo -frame`

 * third with further postprocessing with libx264 from
 [Screencasts in Ubuntu, part 2: FFmpeg](http://polishlinux.org/linux/ubuntu/screencasts-in-ubuntu-part-2/). It uses the options
 -an to turn the sound recording off, <width>x<height> +<ox>,<oy>  - the size of the recorded area plus the upper left corner,
 <fps> is the` number of frames per second, for example: 15, <quality-bps> is in bits/seconds you can add a k to have kbits/sec,
 -sameq  use the same quality as in the input so in the case of x11grab it is the maximal value,

~~~
# The recording of the screen into a video
ffmpeg [-an] -s <width>x<height> -r <fps> -f x11grab -i \
:0.0[+<ox,oy>] -codec mpeg4 -sameq -y <temporary-file>.mp4
# The first processing into H.264
ffmpeg -i <temporary-file i> -vcodec libx264 -pass 1 \
[<quality-bps>](-b) -f mp4 -y /dev/null
# The second processing into H.264
ffmpeg -i <temporary-file> -vcodec libx264 -pass 2 \
[<quality-bps>](-b) -f mp4 -y <final-file>.mp4
~~~

~~~
ffmpeg -an -s 800x600 -r 15 -f x11grab -i :0.0+0,25 \
-vcodec mpeg4 -sameq -y scast-temp.mp4
ffmpeg -i scast-temp.mp4 -vcodec libx264 -pass 1 -b 240000 \
-f mp4 -y /dev/null
ffmpeg -i scast-temp.mp4 -vcodec libx264 -pass 2 -b 240000 \
-f mp4 -y scast.mp4
~~~

 * to Convert other video format to FLV (`ar`: audio samping rate in Hz ,
   `ab`: audio bit rate in kbit/s, f: output format) _the influence on size of dividing
   by 2 default `ar` and `ab` seems minor_ but addinG a video rate of -r 10 (def 25)
   gain 1/3 of size.
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

 * We can easily transcode mpeg to flv or swf using ffmpeg. On mozilla the flash player
   (adobe) give a result not clear with the produced swf, we have a better one with
   mplayer



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
