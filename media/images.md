---
title: Images
---

Among {{< wp " image file formats" >}}.
this section deals with _raster_ or _bitmap_ file formats, the _vector_
file formats are in the
{{< iref "svg" "SVG section" >}},
and the {{< iref "ps_pdf_djvu" "PDF and Postscript section" >}}. They are
compared in the Wikipedia page {{< wp "Comparison of graphics file formats" >}}.

<a class="iref" href="{{< relref "ps_pdf_djvu" >}}" title="internal reference">PDF Section</a>

# Image formats

Wikipedia: {{< wp "Image_file_formats#Raster_formats" "Raster File Formats" >}},
{{< wp "Raster graphics" >}}, {{< wp "Comparison of graphics file formats" >}}
which includes
{{< wp "Comparison_of_graphics_file_formats#Technical_details" "technical details" >}}.

The most popular formats for bitmap are:

Uncompressed lossless formats
:

-   [BMP](http://en.wikipedia.org/wiki/BMP_file_format), [BMP format file structure
    ](http://www.fileformat.info/format/bmp/egff.htm). 1, 4, 8, 16, 24, and 32-bits
    bitmaps format from microsoft
-   <a name="pnm"></a>[PPM, PGM, PBM, PNM](http://en.wikipedia.org/wiki/Netpbm_format),
    [netpbm: PPM](http://netpbm.sourceforge.net/doc/ppm.html) pixmap,
    [PGM](http://netpbm.sourceforge.net/doc/pgm.html) graymap,
    [PBM](http://netpbm.sourceforge.net/doc/pbm.html) bitmap,
    [PAM](http://netpbm.sourceforge.net/doc/pam.html) _Portable Arbitrary Map_ can

    replace  PBM,  PPM, PGM, PPM.
    [PNM](http://netpbm.sourceforge.net/doc/pam.html) anymap, not a true format but any
    of PBM,  PPM, PGM, PPM.

Compressed lossless formats
:

-   [GIF](http://en.wikipedia.org/wiki/Graphics_Interchange_Format),
    is a LZW lossless data compression bit image format, LZW was covered by patents, but
    they expired in 2004. PNG developped to overcome the LZW patents largely replace GIF
    but [Animated GIF](https://en.wikipedia.org/wiki/GIF#Animated_GIF)
    are still widely used.
-   {{< iref "#jxr" "JPEG XR" >}}  can do lossless or lossy compression.
-   {{< iref "#openexr" "openEXR" >}}  can do lossless or lossy compression.
-   [PNG](http://en.wikipedia.org/wiki/Portable_Network_Graphics),
    [Portable Network Graphics (PNG) Specification
    ](https://www.w3.org/TR/2003/REC-PNG-20031110),
    [Portable Network Graphics Home Page](http://www.libpng.org/pub/png/)
-   [ ] <a name="tiff"></a>[TIFF](http://en.wikipedia.org/wiki/TIFF)
    The TIFF image format is widely used for scanning, faxing, word processing, optical
    character recognition.  It can save multi-page documents to a single TIFF file.

    Tiff allows different [compression schemes
    ](https://en.wikipedia.org/wiki/TIFF#TIFF_Compression_Tag)
    CCITT T.4 (i.e group3) and T.6 (i.e group4), JBIG, JBIG2 bi-level encodings; LZW,
    {{< wp "Deflate" >}} (i.e. Zip), JPEG2000 . JPEG is also allowed making in this case
    a lossy format.

    Multiple  images tiff files can be splited or combined with
    {{< iref "#libtiff" "libtiff-tools" >}}, or even by
    {{< iref "#graphicsmagick" "GraphicsMagick" >}}/{{< iref "#imagemagick" "ImageMagic" >}}
    but these two last will use a lot of memory by loading all pages.

    Multiple  images tiff can be displayed only by some viewers like
    {{< iref "#imview" "imview" >}} and  {{< iref "ps_pdf_djvu#evince" "evince"  >}} .

-   [Multiple-image Network Graphics (MNG)
    ](http://www.libmng.com/pub/mng/index.html)
    A PNG-like Image Format Supporting Animation and Transparent JPEG

-  <a name="sixel"></a><a class="WpRef" href="https://en.wikipedia.org/wiki/Sixel"
   title="Wikipedia - Sixel">Sixel</a>
   is a bitmap graphics format supported by terminals and printers from DEC. It consists
   of a pattern six pixels high and one wide, resulting in 64 possible patterns. Each
   possible pattern is assigned an ASCII character. (more
   <a class="WpRef" href="https://en.wikipedia.org/wiki/Sixel"
   title="Wikipedia - Sixel">on Wikipedia</a>).

   Sixel was the format
   [used in the dec vt320](https://www.vt100.net/dec/vt320/soft_characters)
   to transmit glyphs.

   Many terminal applications are supporting sixel, like blackbox, eat, foot, mlterm, st
   with a patch, xfce-terminal, xterm (in vt340 mode since aout 2020), any web terminal
   built upon xterm.js with the image add-on, wezterm, yaft (framebuffer terminal),
   yakuake.

   See [sixel for terminal graphics](https://konfou.xyz/posts/sixel-for-terminal-graphics/)
   for how to set *xterm* and display sixel graphics.

   In 2024 all the vte based terminals, i.e gnome-terminal and sisters, are not sixel
   compatible, neither some popular terminals like alacrity, kitty, konsole, urxvt, ...

   An up to date list is in the page
   [Are We Sixel Yet?](https://www.arewesixelyet.com/).

Lossy Formats
:

-   [JPEG](http://en.wikipedia.org/wiki/JPEG ),
    {{< wp "JPEG" >}} is a method of compression for images, __jpeg/exif__ is
    the most common image format used by digital cameras.
-   {{< wp "JPEG 2000" >}} an enhancement of JPEG with the same level of compression
    but a greater flexibility allowing to lower the resolution without transcoding; at
    the price of additional computing complexity.
    -   [OpenJPEG](http://www.openjpeg.org/) is a BSD licence JPEG 2000 codec written in
        C.
        _ libopenjp2-tools_ is in Debian.
-   <a name="jxr"> {{< wp "JPEG XR" >}} (BSD License) a lossy or lossless format for
    photographic images. Computation can be done using only integer computations.
    The Compression is better than JPEG, and lossless compression is available. There is
    also a better color support, and the container is TIFF compatible.
    _libjxr-tools_ is packaged in Debian.
-   <a name="openEXR">{{< wp "OpenEXR" >}} a BSD licenced high dynamic range raster file
    format. It can do lossless or lossy compression.
    -   [OpenEXR Home](https://www.openexr.com/)
    -   Debian provides _openexr_ tools.
-   {{< iref "#tiff" "TIFF"  >}} when used with jpeg compression is a lossy format.
-   {{< wp "WebP" >}} is an open image format developped by Google
    both with lossless and lossy compression. Google tests show an
    improvement in size of roughly 25% both in lossless format tested
    against _png_ and lossy format compared to _jpeg_.
    -   [Google WebP page](https://developers.google.com/speed/webp/)
    -   _WebP_ is supported by
        browsers as _Chromium_, _Opera_, and an implementation is going on for
        _WebKit_ and _Mozilla_ based browsers.
    -   Image editors as _Gimp_ and
        _{{< iref "#imagemagick" "ImageMagic" >}}_, _but not yet GraphicsMagick_
        have also support for _WebP_
    -   Among viewers _Gthumb_ supports _WebP_. There is a
        [WebP plugin for imlib2](https://github.com/gawen947/imlib2-webp)
        so _imlib2_ based software
        like {{< iref "#feh" "feh" >}} or
        {{< iref "#sxiv" "sxiv" >}}
        should display the _WebP_ format.

Bi-levels Formats
:

    These are formats to encode binary images, or Black and White images. These are
    efficients algorithms which are allowed to embed images in pdf or djvu.

    -   {{< wp "Group_4_compression" "CCITT Group 4 compression" >}} or G4
        is a lossless compression used in Group 4 fax machines, or for PDF image
        embedding.  {{< iref "#imagemagick" "ImageMagick" >}} or
         {{< iref "#graphicmagick" "GraphicMagick" >}} can produce G4 images.
    -   {{< wp "JBIG2"  >}} is a lossless or lossy compression used for PDF embedding.
        It allows a lossless compression  3–5 times smaller than Group 4.
        It is similar to the JB2 compression used in
        {{< iref "ps_pdf_djvu#djvu" "DjVu" >}}.
        More {{< iref "ps_pdf_djvu#jbig2" "references on JBig2 in the PDF section" >}}.

# Color Management

An [ICC profile](https://en.wikipedia.org/wiki/ICC_profile) is describe the color
attributes of a particular device or viewing requirement by defining a bidirectional
mapping between the device source or target color space and a profile connection space
(PCS).

You can find exemple of ICC profiles in the [ICC profiles provided by
Adobe](https://supportdownloads.adobe.com/detail.jsp?ftpID=4075), if you have installed
the colord package many profiles are installed under `/usr/share/color/icc/`.


-   Wikipedia: {{< wp "Linux color management" >}}, {{< wp "ICC profile" >}}
-   [ICC profiles - ArchWiki
    ](https://wiki.archlinux.org/index.php/ICC_profiles#Gnome_Color_Manager)


# Image metadata

{{< wp "Exchangeable_image_file_format"  "EXIF" >}} or _Exchangeable image file format_
is a specification for the image file format used by digital cameras.
The unofficial site of EXIF is [EXIF.org](http://www.exif.org/).

{{< wp "EXtensible Metadata Platform" >}} (XMP) is a standard, created by Adobe,
for processing and storing standardized and proprietary
information relating to the contents of a file.  XMP can be used in
several file formats such as PDF, JPEG, JPEG 2000, JPEG XR, GIF, PNG,
HTML, TIFF, Adobe Illustrator, PSD, MP3, MP4, Audio Video Interleave,
WAV, RF64, Audio Interchange File Format, PostScript, Encapsulated
PostScript, and proposed for DjVu. In a typical edited JPEG file, XMP
information is typically included alongside Exif and IPTC Information
Interchange Model data.

The [IPTC core schema for XMP](http://www.iptc.org/IPTC4XMP/)
can store in XMP header information originally part of
{{< wp "IPTC Information Interchange Model" >}}.
The [IPTC core shema specification
](http://www.iptc.org/std/photometadata/specification/IPTC-PhotoMetadata-201007_1.pdf)
describe the name and role of tags used in IPTC.

## Metatada manipulation programs

Some general image manipulation program can access the exif data stored in jpeg images,
like GIMP, ImageMagic and GraphicksMagic. Number of viewers can also display exif data:
geekie, eog, fbi, gtkam, gphoto2, ristretto.... .

But  only few program that can __write exif__ , among them GIMP,
{{< iref "#imagemagick" "ImageMagic" >}},
{{< iref "#graphicsmagick" "GraphicsMagic" >}}, {{< iref "#exif" "exif" >}},
{{< iref "#gexif" "gexif" >}}, {{< iref "#exiv2" "exiv2" >}},
and {{< iref "#exiftool" "exiftool" >}}.

-   <a name="exif"></a>[Exif](https://github.com/libexif/exif) (LGPL-2.1)
    is the command-line utility from the [libexif](https://libexif.github.io/) library,
    to show and writes EXIF metainformation in JPEG files. exif is in Debian
-   [Exiftags](http://johnst.org/sw/exiftags/) (BSD Licence)
    shows exif metadata in jpeg files.
-   <a name="exiftrans"></a></a>[exiftrans](http://linux.bytesex.org/fbida/)
    is an utility  part of the [fbida project](http://linux.bytesex.org/fbida/)
    which provides also fbi viewer for the linux framebuffer console and da - This is a
    Motif application for viewing images.

    _exiftrans_ allows to rotate jpeg images without re-encoding and
    without losing exif information, in contrast to jpegtran.
-   <a name="exiftool"></a>[ExifTool](http://www.sno.phy.queensu.ca/~phil/exiftool/)
    (Perl License)
    is a perl library plus a command-line application for reading,
    and writing many metadata  in  image, audio and video files.

    The Debian package is _libimage-exiftool-perl_.

    The [Supported file types](https://exiftool.org/#supported) give the huge list of
    format supported with support levels for EXIF, IPTC, XMP, ICC_Profile and other
    metadata types for each file format.

    The [wikimedia commons: Exif
    ](http://commons.wikimedia.org/wiki/Commons:EXIF)
    page contains information of use of exif at Commons with exemple
    showing how to set a copyright and licensing information
    with _exiftool_.
-   <a name="exiv2"></a>[Exiv2](http://www.exiv2.org/) (GPL)
    is a C++ library and a command line utility to manage image
    metadata. It can read and __write__ Exif,
    IPTC and XMP metadata.
    -   [Exiv2 examples](http://www.exiv2.org/sample.html),
    -   [Exiv2 metadata reference tables](http://www.exiv2.org/metadata.html).
-   <a name="gexif"></a>[gexif](https://github.com/libexif/exif) (LGPL-2.1)
    gexif is a GTK3 GUI application which shows the EXIF tags contained in JPG
    and TIFF files. It is packaged in Debian.
-   [Jhead](http://www.sentex.net/~mwandel/jhead/)
    (public domain)  is a command line driven program for
    manipulating the non image parts of Exif flavour
    JPEG files that most digital cameras produce. It is in Debian.
-   [libexif](https://libexif.github.io/) (LGPL-2.1)
    has one command line utilities {{< iref "#exif" "exif" >}}, and a GTK3 gui
    {{< iref "#gexif" "gexif" >}}.
-   [Metacam](http://www.cheeseplant.org/~daniel/pages/metacam.html) (GPL)
    extract EXIF information from digital camera files. It is packaged in Debian.


# Image display

-   [xwd(1)](http://man.cx/xwd(1)) dump an image of an X window
-   [xloadimage(1)](http://man.cx/xloadimage(1))
    load images into an X11 window or onto the root window
-   {{< man "edisplay" >}} is the viewer provided by
    {{< iref "#exactimage" "Exact Image" >}}
-   <a name="fbida"></a>[fbida](http://linux.bytesex.org/fbida/)
    contains __fbi__ an image viewer for framebuffer console, _ida_ a
    small motif-based image viewer. _fbgs_ is a wrapper script to
    display PostScript or pdf using _fbi_ on a framebuffer
    console. {{< iref "#exiftran" "Exiftran" >}} does lossless transformations of JPEG
    images, preserving exif data.  (`jpegtran` instead ignore them)
-   <a name="feh"></a>[feh](http://feh.finalrewind.org/)
    is a CLI-based X11 image viewer using the imlib2 library.  It is
    controlled via command-line arguments and keyboard/mouse actions.
    _feh_ can also be used as an image browser or to set the
    background wallpaper.
    Feh is one of the leaner image viewers 10.5M resident/ 8.7M shared
    for a small png thumbnail.
    Less than even the standard lxde _Gpicview._ Even on my image test
    directory it takes only 19M/9M, you can compare with _geeqie_,
    _gthumb_, or even the _pqiv_ command line. It's only contender is
    {{< iref "#sxiv" "sxiv" >}}.

    -   A summary of feh capacities is given on the
        [Feh page of the previous maintener
        ](http://linuxbrit.co.uk/software/feh/).
    -   [ArchWiki: Feh](https://wiki.archlinux.org/index.php/Feh)
    -   [Feh GitHub repository](https://github.com/derf/feh)
    -   [Feh manual](https://man.finalrewind.org/1/feh/).

-   [Fim](http://www.autistici.org/dezperado/fim/) _(GPL)_
    display images on framebuffer, it can resize, zoom, rotate and
    scroll your images.
-   <a name="geekie"></a>[Geeqie](http://geeqie.org/) (GPL)
    is a fork of the older [gqview](http://gqview.sourceforge.net/),
    It is a gtk3 based image viewer, it does not requires gnome as many of
    its concurrent gtk browsers like **eog**. It is
    suited for photo collection maintenance: it allows viewing tags Exif/IPTC/XMP, it is
    feature we harly find in other image viewers, for which you have to rely on an
    external tool to view tags.

    It has a medium footprint less than {{< iref "#gthumb" "Gthumb" >}}
    and above the lighter {{< iref "#feh" "feh" >}} or
    _Gpicview_.  30 M resident/25 M shared at start moving to 93M/27M
    on my image test directory. Like gthumb it does not garbage
    collect and the footprints are always increasing during a session.

    It seems than on wayland, it does not autodetect the gdk backend, so you have to
    make sure that the environment variable `GDK_BACKEND=wayland` is set.
    -   [Geeqie github repository](https://github.com/BestImageViewer/geeqie)
    -   [The Geeqie User Manual](https://www.geeqie.org/help/GuideIndex.html)
-   [Gpicview](http://wiki.lxde.org/en/GPicView) (GPL)
    was a lightweight and fast image viewer for GTK+ 2.x.
    GpicView is no longer developped since 2013, has several bugs, and uses obsolete

-   <a name="gthumb"></a>{{< wp "Gthumb" >}} (GPL)
    is an image viewer and organizer. It belongs to gnome but it has very mild gnome
    dependencies and is more a GTK+ software. Its features include filesystem browsing,
    slide show, image catalogs, web album creation, camera import, image CD burning,
    batch file operations and quick image editing features like metadata display and
    edition, transformation and color manipulationColor Adjustments, resizing and
    cropping, rotations and flips.
    -   [Gthumb Home](https://wiki.gnome.org/action/show/Apps/gthumb)
    -   [Gthumb Help](https://help.gnome.org/users/gthumb/stable/)
    -   [gThumb - Ubuntu Community Help Wiki](https://help.ubuntu.com/community/gThumb)
    -   Gthumb start at 70M resident / 49M like geeqie, it grows fast depending of the
        images displayed, but I have observed a better garbage collection than in the
        case of geeqie, for the same image directory gthumb grow to 151M/70M and it
        doesn't seem to shrink when moving to small or even empty directory.
        _I noticed garbage collection on a previous version, but with the new one tested
        3.4.4 it does no more happen._
-   {{< iref "#graphickmagick" "Graphics Magick" >}}
    provide a command to display images. `gm display`.
-   {{< iref "#imagemagick" "ImageMagick" >}} display images
    with its command `display`.
-   <a name="imview"></a>[imview](http://hugues.zahlt.info/software_imview.html)
    is an X11 image viewer, with limited editing capabilities.  It can
    display multiple pages tiff files. It uses no desktop environment,
    only bare X. The 1.1.9h version is from 2009, Debian use 1.1.9C
    from 2008, it is now minimally maintained. It has small memory
    footprints 9.5M resident / 8.5M shared. When loading all files from
    my test directory the memory footprint is 43M / 14M
-   {{< wp "libjpeg"  "LibJpeg" >}} contains the following utilities: `cjpeg` and
    `djpeg`, for performing file formats conversions, `rdjpgcom` and
    `wrjpgcom`, for inserting and extracting textual comments in JFIF
    files, `jpegtran` for lossless transcoding between different JPEG
    formats.
-   [lsix](https://github.com/hackerb9/lsix)
    Shows thumbnails of images in a directory in terminal using {{< wp "Sixel" >}}
    graphics.  It is a bash script that uses {{< iref "#imagemagick" "ImageMagick" >}}
    for displaying images.
-   [lximage-qt](https://github.com/lxqt/lximage-qt) (GPL-2.0)
    is the image viewer and screenshot tool for lxqt. Its features include:
    Zoom, rotate, flip and resize images
    -   Slideshow
    -   Thumbnail bar (left, top or bottom); different thumbnail sizes
    -   Exif data bar
    -   Inline image renaming
    -   Custom shortcuts
    -   Image annotations (arrow, rectangle, circle, numbers)
    -   Take screenshots
-   [Mirage](http://mirageiv.sourceforge.net/)
    was a Python/GTK  image viewer, no longer maintained since 2011.
    -   [Mirage Documentation](http://mirageiv.sourceforge.net/docs.html)
-   <a name="pqiv"></a>[PQIV](https://github.com/phillipberndt/pqiv)
    is the continuation of {{< iref "#qiv" "QIV" >}}.  It is an image viewer written in
    C using GTK 3 and GLIB 2. It is actively maintained in 2024, and is in
    Debian.  It start at 26M resident / 21M shared on a small thumbnail, and browsing my
    image test directory 64M / 21M.
-   <a name="qiv"></a>[QIV - Quick Image Viewer](http://spiegl.de/qiv/)
    (GPL) is a gdk/Imlib2 image viewer. it is in Debian.  Development of _qiv_ stopped
    in 2013, but it continues in {{< iref "#pqiv" "PQIV" >}}.
-   [Ristretto](http://goodies.xfce.org/projects/applications/ristretto)
    is a fast and lightweight picture-viewer for the Xfce desktop environment.
-   <a name="sxiv"></a>[sxiv](https://github.com/muennich/sxiv)
    is a lightweight and scriptable image viewer written in C.  Its only dependency
    besides xlib is imlib2. It is in Debian.  Iis an alternative to {{< iref "#feh"
    "feh" >}},
    {{< iref "#qiv" "qiv" >}} or
    {{< iref "#pqiv" "pqiv" >}}.

    It start at 5.7M / 4.7M on a small png thumbnail and 20M /5M browsing my test image
    directory (34M / 5M when also making thumbnails). For those who want a very lean
    image viewer, it is the only contender to {{< iref "#feh" "feh" >}} among the viewer
    I tested.

    -   [ArchWiki: sxiv](https://wiki.archlinux.org/index.php/Sxiv)


_Notes_
:   _The memory footprints comparisons in this section are done by loading in the viewer
    a 4K png icon (emblem-debian.png 128x128)_

:   _The test image directory contains 23 jpegs of around 1MB for a
    total of 19MB_

### Wayland image viewers {#wayland_image_viewers}
See also  {{< iref "desktop#wayland_desktop_components" "Wayland Desktop Components" >}}

-   [imv](https://sr.ht/~exec64/imv/)  (MIT License)
    is an image viewer for X11/Wayland.
    [![packaging](https://repology.org/badge/tiny-repos/imv.svg?header=packages)
    ](https://repology.org/project/imv/versions)
    including Debian which provides the wayland and X11 binaries.
-   [mpv-image-viewer](https://github.com/occivink/mpv-image-viewer) (Unlicense license)
    or _miv_ Configuration, scripts and tips for using mpv as an image viewer.
    -   [eugenesvk/mpv-image-viewer fork
        ](https://github.com/eugenesvk/mpv-image-viewer)
        has some improvements.
-   [swappy](https://github.com/jtheoof/swappy) (MIT license)
    A Wayland native snapshot editing tool, inspired by Snappy on macOS,
    it is used with {{< iref "desktop#grim" "grim" >}} and
    {{< iref "desktop#slurp" "slurp" >}}.
    [![packaging](https://repology.org/badge/tiny-repos/swappy.svg?header=packages)
    ](https://repology.org/project/swappy/versions)repos
-   [swayimg](https://github.com/artemsen/swayimg) (MIT license)
    image viewer for Sway/Wayland.
    [![Packaging status](https://repology.org/badge/tiny-repos/swayimg.svg)
    ](https://repology.org/project/swayimg/versions)
-   [ueberzugpp](https://github.com/jstkdng/ueberzugpp) (GPL-3.0)
    is a command line utility which draws images on terminals using child windows.
    [![packaging](https://repology.org/badge/tiny-repos/ueberzugpp.svg?header=packages)
    ](https://repology.org/project/ueberzugpp/versions).
-   [vimiv-qt](https://github.com/karlch/vimiv-qt) (GPL-3.0)
    a QT image viewer with vim-like keybindings.

## Terminal image display
On a <a class="iref" href="#sixel" title="internal reference">sixel enabled terminal</a>
you can display sixel images by just using `cat img.six`.


Terminal like Kitty, iTerm2, wezterm, konsole and vscode, offer high resolution
images in 24bit colors.you will use an appropriate viewer. These terminal use each their
own custom image protocol, and offer their own viewer.

The MacOs terminal iterm2 implement a custom [Inline Images Protocol
](https://iterm2.com/documentation-images.html) which extends the xterm protocol with a
set of proprietary escape sequences. This specific protocol is also available on wezterm
and konsole. Using this protocol we can display an image by
```sh
(printf "\e]1337;File=inline=1:" ; base64 -w0 image.jpg  ; printf "\a\n")
```

Kitty has also adopted a custom {Kitty terminal graphics protocol
](https://sw.kovidgoyal.net/kitty/graphics-protocol/)
which can also be used in wezterm, konsole, wayst.
Many programs can use this protocol like timg, chafa, ranger, mpv, viu, some neovim
plugins ect *see the list on the [protocol page
](https://sw.kovidgoyal.net/kitty/graphics-protocol/)*.


Some viewer like timg work with many protocol.

-   [catimg](https://github.com/posva/catimg/) (MIT License)
    is a C program that display jpeg, png, gif images in the terminal using ascii or
    unicode characters.

    The repository include also the [catimg bash script
    ](https://github.com/posva/catimg/blob/master/catimg)
    that use imagemagick convert to display the image. The script is more accurate
    concerning colors but considerably slower, than the C version which is very fast.

    The work of catimg is explained [in the author blog
    ](https://posva.net/shell/retro/bash/2013/05/27/catimg).

    I have not done a careful benchmark, but for some examples I found catimg 7.7 faster
    than timg.

-   [Chafa](https://hpjansson.org/chafa/) (LGPL-3.0)
    is a terminal image viewer. It has support for the Sixels, Kitty, iTerm2 protocols,
    and most popular image formats, including animated GIFs.
    -   [Man page for Chafa](https://hpjansson.org/chafa/man/)
    -   [chafa - GitHub](https://github.com/hpjansson/chafa)

-   [timg](https://github.com/hzeller/timg) (GPL-2.0)
    A C++ terminal image and video viewer.

    It has support for half block characters, quarter block, sixel, kitty-protocol,
    iTerm2 protocol

    It uses sixel when it is available, but it I have noted that on *foot terminal*
    timg do not use sixel by default and you have to use it with:
    ```sh
    timg -p sixel <image>
    ```

    On terminals with high resolution display like Kitty, iTerm2, konsole timg can use
    the high res format.

    timg can display animated gif, but not webp animations.

    It can also display a pdf page, the result on a sixel enabled terminal, or kitty, is
    very nice with a pdf containing images.

    It can also display videos.

    timg has many options to control the image display.

## Image Libraries

-   [libmng](http://gjuyn.xs4all.nl/libmng/) The MNG reference
    library
-   [netpbm](http://netpbm.sourceforge.net/)
    Netpbm is a package of graphics programs and a programming library, for the
    Netpbm {{< iref "#pnm" "PNM format family" >}} including for tools for transforming and
    converting to other formats.
    The _huge_ list of Netpbm programs is on the manpage
    {{< man "netpbm(1)" >}}
-   [SDL image](http://www.libsdl.org/projects/SDL_image/docs/index.html) (GPL),
    also named _libsdl-image_ is a library used with the command
    __showimage__ for displaying image via the SDL library. It is used
    in numerous console games and also by the _Python Imaging Library
    (PIL)_


# Images Transforming


## Raster software

*see also Dia, Ditaa, Gnuplot, ivtools, xfig, veusz in the*
{{< iref "svg#svg_software" "SVG Software section" >}}.

-   [Aafigure](http://packages.python.org/aafigure/)
    is a python utility that convert diagrams drawn using ascii art into bitmap graphics
    in _png_ format.  Aafigure can be used with _asciidoc_, _Restructured Text_,
    _MoinMoin_, _Sphinx_
-   [Converseen](http://converseen.fasterland.net/) (GPL-3.0)
    Converseen is a batch image processor for Windows and Linux written in C++ with Qt5
    libraries using ImageMagick through the  Magick++ library.
    It allows you to convert, resize, rotate and flip an infinite number of images with a
    mouse click. It can also convert a pdf into a set of images.

    Converseen is packaged in Debian.
    -   [Converseen - GitHub](https://github.com/Faster3ck/Converseen)
-   [CoolText online graphics generator](http://www.cooltext.com/)
-   [drawing](https://github.com/maoschanz/drawing)
    python3 GTK simple image editor for Linux similar to MS Paint.
    It is in many distributions including Debian, Alpine and on Flathub.
-   <a name="exactimage"></a>[ExactImage](https://exactcode.com/opensource/exactimage/)
    is a fork of {{< iref "#imagemagick" "ImageMagic" >}}, coded for speed in C++.
    It supports BMP, Digital Camera RAW, GIF, JPEG, JPEG2000, OpenEXR, PNG, PBM, RAW,
    TIFF, XPM, SVG PDF, PS, EPS, PCX, Targa, TGA. More formats are planed. It has
    utilities similar to those of {{< iref "#imagemagick" "ImageMagic" >}}:
    `econvert`, `edisplay`, `edentify`.

    It has also {{< man "hocr2pdf" >}} to create a searchable PDF from hOCR input.
    and barcode recognition with {{< man "bardecode" >}}.

-   <a name="gimp"></a>[Gimp](http://www.gimp.org)
    is an image manipulation and paint program.
    -   The [Gimp site](http://www.gimp.org ) references the
        [Gimp documentation](http://www.gimp.org/docs/) with
        [tutorials](http://www.gimp.org/tutorials/),
        and [books](http://www.gimp.org/books/).
    -   The main references are the
        [Gimp User Manual](http://docs.gimp.org/en/) and
        [FAQ](http://www.gimp.org/docs/userfaq.html).
    -   [Grokking the GIMP](http://gimp-savvy.com/BOOK/index.html)
        is an online book and Gimp manual.
    -   _SOS GIMP_ (french lang) _The original site has been eaten by
        the commercial monster, the  book is yet [available here
        ](http://www.scribd.com/doc/3181597/SOS-GIMP)._
-   [Google Chart Tools](http://code.google.com/apis/chart/)
    or _Google Chart API_ lets you dynamically generate charts with a
    URL string.  You can embed these charts on your web page, or
    download the image for local or offline use
    -   [Graphy](http://graphy.googlecode.com/)
        is a  Python library for generating charts with _Google Chart API_.
-   <a name="graphicsmagick"></a>[Graphics Magick](http://www.graphicsmagick.org/)
    ([bunch of MIT like licenses](http://www.graphicsmagick.org/Copyright.html))
    is a fork of {{< iref "#imagemagick" "ImageMagick" >}}
    with roughly the same capabilities and supporting also [many formats
    ](http://www.graphicsmagick.org/formats.html)

    GraphicsMagick provides a
    [command line utility](http://www.graphicsmagick.org/utilities.html)
    which may be used to access all GraphicsMagick functions.
    -   [display](http://www.graphicsmagick.org/display.html)
        display an image on an X window.
        Used as an image viewer _display_ has tiny footprints
        10M resident/ 8M shared both for for the the _Image Magick_ and
        _Graphics Magick_ versions. In the same range than the winner
        {{< iref "#feh" "feh" >}}.
        But the user interface of display is more limited.
    -   [convert](http://www.graphicsmagick.org/convert.html)
        convert an image from one format
        to an other one
    -   see also: [animate](http://www.graphicsmagick.org/animate.html),
        [identify](http://www.graphicsmagick.org/identify.html),
        [montage](http://www.graphicsmagick.org/montage.html),
        [mogrify](http://www.graphicsmagick.org/mogrify.html),
        [composite](http://www.graphicsmagick.org/composite.html)
-   <a name="imagemagick"></a> [Image Magick](http://www.imagemagick.org/)
    (Open Source free [custom license](http://www.imagemagick.org/script/license.php))
    is an image display and manipulation tool for the X Window System.

    In 2025 it seems that neither Image Magick, nor Graphics Magick can use wayland,
    which means that *display* uses XWayland, and import cannot import wayland windows.

    Image Magick can read and write
    [many format](https://imagemagick.org/script/formats.php#supported) among which:
    BPM, EPS, EXR, FAX (G3, G4), GIF, JBIG, JPEG, JPEG-2000 (PGX), JXR i.e. _JPEG-XR_,
    MPEG (M2V, M4V, MKV, MOV, MPG, WMV), Photo CD (PCD), PDF, PNG, PNM (PBM, PPM, PGM,
    PAM), PS (level II and III), RGB, SVG, TIFF, XPM, WEBP, YUV image formats.

    It can resize, rotate, sharpen, color reduce, add special effects, convert an image,
    and creates animated or transparent .gifs, composite images, or thumbnail images.

    _ImageMagick_ includes the following command line tools:

    [animate](http://www.imagemagick.org/script/animate.php)
    :   animate an image sequence on an X server.

    [compare](http://www.imagemagick.org/script/compare.php)
    :   annotate the difference between an image and its reconstruction.

    [composite](http://www.imagemagick.org/script/composite.php)
    :   overlap one image over another.

    [conjure](http://www.imagemagick.org/script/conjure.php)
    :   interpret and execute scripts written in the Magick Scripting Language (MSL).

    [convert](http://www.imagemagick.org/script/convert.php)
    :   convert between image formats as well as resize an image, blur, crop, despeckle,
        dither, draw on, flip, join, re-sample, and more.

    [display](http://www.imagemagick.org/script/display.php)
    :   display an image or image sequence on an X server.

    [identify](http://www.imagemagick.org/script/identify.php)
    :   describe the format and characteristics of one or more image files.

    [import](http://www.imagemagick.org/script/import.php)
    :   save any visible window on an X server as an image file. You can capture a
        single window, the entire screen, or any rectangular portion of the screen.

    [mogrify](http://www.imagemagick.org/script/mogrify.php)
    :   resize an image, blur, crop, despeckle, dither, draw on, flip, join, re-sample,
        and much more. Mogrify overwrites the original image file, whereas _convert_
        writes to a different image file.

    [montage](http://www.imagemagick.org/script/montage.php)
    :   create a composite image by combining several separate images.  The images are
        tiled on the composite image optionally adorned with a border, frame, image
        name, and more.

    [stream](http://www.imagemagick.org/script/stream.php)
    :   stream one or more pixel components of the image or portion of the image to your
        choice of storage formats. It writes the pixel components as they are read from
        the input image a row at a time making `stream` desirable when working with
        large images or when you require raw pixel components.

    -   _ImageMagick_ API is
        [available for numerous languages](https://imagemagick.org/script/develop.php)
        C, C++, [GO](https://github.com/gographics/imagick), Java, javascript,
        lisp, node, lua, perl, PHP, Python, R, Ruby, Rust, TCL/TK .....

        The C++, node, php, perl, java, ruby, the python  _PythonMagick_ are availables
        in Debian.
    -   [ImageMagick Common Image Formats](http://www.imagemagick.org/Usage/formats/)
        describe how ImageMagick works with different image formats, and what are the
        options.

-   [Hugin](http://hugin.sourceforge.net/)
    is a panorama photo stitching program.  Stitching is accomplished by using several
    overlapping photos taken from the same location, and using control points to align
    and transform the photos so that they can be blended together to form a larger
    image.
-   <a name="libtiff-tools"></a> [libtiff-tools](http://libtiff.maptools.org)
    includes command line tools for converting TIFF images to and from
    other formats and tools for doing simple manipulations of TIFF
    images.
-   [ImageJ](https://en.wikipedia.org/wiki/ImageJ)
    (public domain see [license details](http://imagej.net/Licensing))
    is an image processing program written in Java.  It isinspired by NIH Image for the
    Macintosh.  It can display, edit, analyze, process, save and print 8-bit, 16-bit and
    32-bit images. It can read many image formats including TIFF, GIF, JPEG, BMP, DICOM,
    FITS and "raw".

    -   [ImageJ Home](https://imagej.nih.gov/)
    -   [ImageJ Wiki](http://imagej.net/)
    -   [ImageJ repository on GitHub](https://github.com/imagej/imagej)

-   [img2pdf](https://gitlab.mister-muffin.de/josch/img2pdf) (GPL-3.0)
    Lossless conversion of raster images to PDF.
   [![packaging](https://repology.org/badge/tiny-repos/img2pdf.svg?header=packages)
   ](https://repology.org/project/img2pdf/versions).

    If we use<a class="iref" href="#imagemagick" title="internal reference">
    ImageMagick</a> to convert a raster to pdf conversion is:
    -   lossy re-encoding to JPEG
    -   using wasteful flate encoding of raw pixel data
    -   slow because input data gets re-encoded
-   [mermaid](https://github.com/mermaid-js/mermaid) (MIT License)
    A _node.js_ tool for generation of sequence diagrams, class diagrams,
    state diagrams, Gantt diagrams, pie charts, and flowchart from text in a similar
    manner as markdown.
-   [Pinta](https://github.com/PintaProject/Pinta) (MIT License)
    is a Gtk# clone of Paint.Net 3.0 for drawing and image editing.
-   [sam2p](https://github.com/pts/sam2p) (GPL)
    is a command line utility that converts many raster (bitmap) image formats like GIF,
    JPG/JPEG, and PNG into PostScript or PDF files.

    It was [removed from Debian](https://tracker.debian.org/pkg/sam2p) in 2016,
    but there is a request to reintroduce it.
-   [tgif(1)](http://man.cx/tgif(1)) interactive 2-D drawing
    facility under X11.

    It supports PostScript formats suitable for LaTeX, as well as X11 bitmap or (version
    1) pixmap formats. Other vector and raster image formats such as SVG and PNG can be
    handled via filters.
-   [Trimage](http://trimage.org/) (MIT License)
    is a tool for losslessly
    optimizing PNG and JPG files. Trimage is in Debian.

    -   [Trimage - GitHub](https://github.com/Kilian/Trimage)

    It is a frontend to three tools:
    -   [Optipng](http://optipng.sourceforge.net/) (zlib license)
         a PNG optimizer and BMP, GIF, PNM and TIFFconverter.
    -   [AdvanceCOMP](http://advancemame.sourceforge.net/comp-readme.html)
        a set of recompression utilities for your .ZIP archives,
        .PNG snapshots, .MNG video clips and .GZ files.
    -   [jpegoptim](http://www.kokkonen.net/tjko/projects.html) (GPL)
        lossless optimization and "lossy" optimization based on setting
        maximum quality factor for jpeg files.

-   [Guy Rutenberg – Separating Colors
    ](https://www.guyrutenberg.com/2012/10/12/scanning-lecture-notes-separating-colors/)
    deals with generating 1bit depth image from coloured images.

## Wayland Screenshot {#wayland-screenshot}

-   [Screen capture in wayland - Archwiki](https://wiki.archlinux.org/title/Screen_capture#Wayland)
-   [grimshot](https://github.com/OctopusET/sway-contrib/blob/master/grimshot) -
    script to grab regions from the window, by using *grim*, *slurp*, *wl-copy* and *jq*.

    *Packaged in Debian*
-   [screenshot-bash
    ](https://codeberg.org/Scrumplex/screenshot-bash/src/branch/master/screenshot-bash) (GPL)
    screenshot - upload - copy-url pipeline using *grim*, *slurp*, *wl_copy*.
-   [snag](https://github.com/b0o/snag) (MIT License)
    bash script to snag screenshots and screencasts with Rofi
-   [swappy](https://github.com/jtheoof/swappy) (MIT Licence)
    A Wayland native snapshot and editor tool, works grim, slurp and sway.
-   [swayshot](https://gitlab.com/vitalijr2/swayshot) (GPL-3.0)
    adds sway keyboard shortcuts for screenshots of the full screen, focused window,
    or selected region. Optionally upload them to 0x0.st.

    It uses *grim*, *slurp*, *jq* and *wl-clipboard*.
-   [shotman](https://git.sr.ht/~whynothugo/shotman) (ISC License)
    rust program to take a screenshot and shows a small thumbnail with actions to copy,
    delete, dismiss.
-   [taiga](https://hg.sr.ht/~scoopta/taiga) (GPL-3.0)
    an animated waylan screenshot program written in C.
-   [wayshot](https://git.sr.ht/~shinyzenith/wayshot)
    A native screenshot tool for wlroots based compositors such as sway
    and river written in Rust.
-   [flameshot](https://github.com/flameshot-org/flameshot) (GPL-3.0)
    screenshot software, with customizable appearance, in-app screenshot editing, D-Bus
    interface, experimental GNOME/KDE Wayland support, integration with Imgur and
    support for both GUI and CLI interface.

    *Packaged in Debian*
-   [sway-screenshot](https://github.com/Gustash/sway-screenshot) (GPL-3.0)
    bash script to take screenshot in swaywm using your mouse, using
    *grim*, *slurp*, *wl_clipboard*, *jq*, *imagemacick*.

# Static Images gallery
-   [Sigal](http://sigal.saimon.org/en/latest/) (MIT License)
    a python static gallery generator that uses the for theming a javascript library, either
    [colorbox](http://www.jacklmoore.com/colorbox),
    [galleria](http://galleria.io/) or [photoswipe ](http://photoswipe.com/)

    Sigal process directories recursively, generate HTML pages using Jinja2 templates,
    use relative links, and support themes, videos, EXIF tags, zip download.

    Dependencies: Blinker, Click, Jinja2, natsort, Pilkit, Pillow, Python Markdown

    Sigal is actively maintained in 2025.

    -   [GitHub - sigal](https://github.com/saimn/sigal/)
-   [lazygal](https://sml.zincube.net/~niol/repositories.git/lazygal/about/) (GPL)
    is a static web gallery generator written in Python. It is in Debian.
-   [Gallery](https://github.com/horgh/gallery) (GPL)
    is a go language program to create a static photo gallery website.
    *Gallery is no longer updated since 2018.*
-   __Pictor__ [github](https://github.com/dustinkirkland/pictor),
    [launchpad](https://launchpad.net/pictor) is a web application for viewing and
    sharing your pictures online. Pictures are organized hierarchically in folders and
    sub-folders.

    **Pictor** still have release updates to keep it compatible to ubuntu development,
    but it has no new features since 2015.

# Image Recovery

-   [PhotoRec - Digital Picture and File Recovery
    ](https://www.cgsecurity.org/wiki/PhotoRec),
    [Digital Photos Recovery Using PhotoRec - CGSecurity
    ](https://www.cgsecurity.org/wiki/Digital_Photos_Recovery_Using_PhotoRec)
<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
