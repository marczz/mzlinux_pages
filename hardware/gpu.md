---
title: Graphic Processing Unit
---

# References
-   <a class="WpRef" href="https://en.wikipedia.org/wiki/Graphic_Card"
    title="Wikipedia - Graphic_Card">Graphic Card</a>.
-   [Category:Graphics - ArchWiki](https://wiki.archlinux.org/title/Category:Graphics)
-   [GraphicsCard - Debian Wiki](https://wiki.debian.org/GraphicsCard).
-   <a class="WpRef" href="https://en.wikipedia.org/wiki/Video_Acceleration_API"
    title="Wikipedia - Video_Acceleration_API">Video Acceleration API</a>.
    makes it possible for the video card to decode/encode video.
-   [Hardware video acceleration - ArchWiki
    ](https://wiki.archlinux.org/title/Hardware_video_acceleration).
-   [HardwareVideoAcceleration - Debian Wiki
    ](https://wiki.debian.org/HardwareVideoAcceleration)

To detect the graphics hardware in your system, use this command:
``` sh
lspci -k | grep -EA3 'VGA|3D|Display'
```
You can have more information, like the card capabilities with
```sh
lshw -c video
```

The opengl capabilities can be queried with the utility `glxinfo`from the package
*mesa-utils*.
```sh
glxinfo -B
```

There are three API for hardware video acceleration:

-   VA-API:
    Supported on Intel, AMD, and NVIDIA, and by Kodi, VLC, MPV, Chromium, and Firefox.
    The [Debian Wiki](https://wiki.debian.org/HardwareVideoAcceleration#VA-API)
    list the package to install to get the proper drivers.
-   VDPAU:
    Supported on AMD and NVIDIA and by Kodi, VLC, and MPV, but has not in Chromium or
    Firefox.
    [Debian list of drivers](https://wiki.debian.org/HardwareVideoAcceleration#VDPAU)
-   NVENC/NVDEC:
    proprietary NVIDIA API supported only by FFmpeg and OBS Studio for encoding, FFmpeg
    and MPV for decoding. [Debian list of drivers
    ](https://wiki.debian.org/HardwareVideoAcceleration#NVENC.2FNVDEC).

# Intel Graphics
-   Wikipedia <a class="WpRef" href="https://en.wikipedia.org/wiki/Intel_Quick_Sync_Video"
    title="Wikipedia - Intel_Quick_Sync_Video">Intel Quick Sync Video</a> has a table of
    <a class="WpRef" href="https://en.wikipedia.org/wiki/Intel_Quick_Sync_Video#Hardware_decoding_and_encoding"
    title="Wikipedia - /ntel_Quick_Sync_Video#Hardware_decoding_and_encoding"">
    Hardware decoding and encoding</a> that you can also find in the following Intel.com pages.
-   [Intel graphics - ArchWiki](https://wiki.archlinux.org/title/Intel_graphics).
-   [Intel - Gentoo wiki](https://wiki.gentoo.org/wiki/Intel).
-   [VAAPI support on Intel GPU
    ](https://www.intel.com/content/www/us/en/developer/articles/technical/linuxmedia-vaapi.html)
-   [Quick Reference Guide for Intel Core Processor Graphics
    ](https://www.intel.com/content/www/us/en/developer/articles/guide/quick-reference-guide-to-intel-processor-graphics.html)
-   [intel/media-driver](https://github.com/intel/media-driver)
    Intel Graphics Media Driver to support hardware decode, encode and video processing.
    The supported platforms include: Broadwell, Skylake, Broxton, Apollo Lake,
    Kaby Lake, Coffee Lake, Whiskey Lake, Cannon Lake, Ice Lake,

    The debian package in the non-free section is *intel-media-va-driver-non-free*.

# Application support
## Firefox
See [Firefox Hardware Video Acceleration - ArchWiki
](https://wiki.archlinux.org/title/Firefox#Hardware_video_acceleration)


in `about:config` in address bar:
~~~ ini
media.ffmpeg.vaapi.enabled true
media.ffvpx.enabled false
~~~

The first line enable gpu acceleration for AVC/h.264 HEVC/h.265 work, the second
disables firefox internal software decoding of VP8/VP9 and forces hardware decoding, it
should be enabled only if your gpu can decode VP9.

To make YouTube use a codec supported by your gpu you may want to use the extension
[enhanced-h264ify](https://addons.mozilla.org/en-US/firefox/addon/enhanced-h264ify/).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
