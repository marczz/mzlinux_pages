<!--
.. description:
.. date: 2015-06-12
.. slug: images
.. tags:
.. link:
.. book: mzlinux
.. title: Images
-->

[TOC]

Among [w: image file formats].
this section deals with _raster_ or _bitmap_ file format, the _vector_
file format are in the
[SVG section](#svg "internal reference"),
and the [PDF and Postscript section
](/node/ps_pdf_djvu "internal reference"). They are
compared in the Wikipedia page [w:Comparison of graphics file formats].


# Image formats

The most popular formats for bitmap are:

Uncompressed lossless formats
:   [BMP](http://en.wikipedia.org/wiki/BMP_file_format),
    [PPM, PGM, PBM, PNM](http://en.wikipedia.org/wiki/Netpbm_format).

Compressed lossless formats
:

-   [GIF](http://en.wikipedia.org/wiki/Graphics_Interchange_Format),
-   [PNG](http://en.wikipedia.org/wiki/Portable_Network_Graphics),
    [Portable Network Graphics Home Site](http://www.libpng.org/pub/png/)
-   [TIFF](http://en.wikipedia.org/wiki/TIFF "en.wikipedia.org TIFF")
    The TIFF format can save multi-page documents to a single TIFF file,
    it is user on scanner, and for fax servers
-   [Multiple-image Network Graphics (MNG)
    ](http://www.libmng.com/pub/mng/index.html)
    A PNG-like Image Format Supporting Animation and Transparent JPEG
-   [w:Exchangeable_image_file_format|EXIF]
    or _Exchangeable image file format_ is a specification for the
    image file format used by digital cameras.

Lossy Formats
:

-   [JPEG](http://en.wikipedia.org/wiki/JPEG ),
    [w:JPEG] is a method of compression for images, __jpeg/exif__ is
    the most common image format used by digital cameras.
-   [TIFF](http://en.wikipedia.org/wiki/TIFF) a lossy or losseless
    image format widely used for scanning, faxing, word processing, optical character recognition.
    It supports multiple images in one file, even if fiew viewers can display them
    _(but [imview](#imview "internal reference") does)_.
    Multiple  images tiff files can be splited or combined with
    [libtiff-tools](#libtiff-tools "internal reference"), or even by
    [GraphicsMagick](#graphicsmagick "internal reference")/ImageMagick
    but these two last will use a lot of memory by loading all pages.
-   [w:WebP] is an open image format developped by Google
    both with lossless and lossy compression. Google tests show an
    improvement in size of roughly 25% both in lossless format tested
    against _png_ and lossy format compared to _jpeg_.
    -   [Google WebP page](https://developers.google.com/speed/webp/)
    -   _WebP_ is supported by
        browsers as _Chromium_, _Opera_, and an implementation is going on for
        _WebKit_ and _Mozilla_ based browsers.
    -   Image editors as _Gimp_ and
        _ImageMagick_, _but not yet GraphicsMagick_ have also support for
        _WebP_
    -   Among viewers _Gthumb_ supports _WebP_. There is a
        [WebP plugin for imlib2](https://github.com/gawen947/imlib2-webp)
        so _imlib2_ based software
        like [feh](#feh "internal reference") or
        [sxiv](#sxiv "internal reference")
        should display the _WebP_ format.

# Image metadata

[w:Exchangeable_image_file_format|EXIF]
or _Exchangeable image file format_
is a specification for the image file format used by digital cameras.
The unofficial site of EXIF is [EXIF.org](http://www.exif.org/).

[w:EXtensible Metadata Platform] (XMP) is a standard, created by Adobe
Systems Inc., for processing and storing standardized and proprietary
information relating to the contents of a file.  XMP can be used in
several file formats such as PDF, JPEG, JPEG 2000, JPEG XR, GIF, PNG,
HTML, TIFF, Adobe Illustrator, PSD, MP3, MP4, Audio Video Interleave,
WAV, RF64, Audio Interchange File Format, PostScript, Encapsulated
PostScript, and proposed for DjVu. In a typical edited JPEG file, XMP
information is typically included alongside Exif and IPTC Information
Interchange Model data.

The [IPTC core schema for XMP](http://www.iptc.org/IPTC4XMP/)
can store in XMP header information originally part of
[w:IPTC Information Interchange Model].
The [IPTC core shema specification
](http://www.iptc.org/std/photometadata/specification/IPTC-PhotoMetadata-201007_1.pdf)
describe the name and role of tags used in IPTC.

## Metatada manipulation programs Some general image manipulation
program can access the exif data stored in jpeg images, like GIMP,
ImageMagic and GraphicksMagic. Number of viewers can also display exif
data: geekie, eog, fbi, gtkam, gphoto2, ristretto.... .

But  only few program that can __write exif__ , among them GIMP,
[ImageMagic](#imagemagick "internal reference"),
[GraphicsMagic](#graphicsmagick "internal reference"),
exif, gexif,  exiv2, and exiftools.

-   [Exiftags](http://johnst.org/sw/exiftags/) (BSD Licence)
-   [exiftran](http://linux.bytesex.org/fbida/)
    is aN utility to rotate jpeg images without re-encoding and
    without losing exif information.
-   [Exiftool](http://www.sno.phy.queensu.ca/~phil/exiftool/)
    is a perl library plus a command-line application for reading,
    and writing many metadata  in  image, audio and video files.
    The [wikimedia commons: Exif
    ](http://commons.wikimedia.org/wiki/Commons:EXIF)
    page contains information of use of exif at Commons with exemple
    showing how to set a copyright and licensing information
    with _exiftools_.
-   [Exiv2](http://www.exiv2.org/) (GPL)
    is a C++ library and a command line utility to manage image
    metadata. It can read and __write__ Exif,
    IPTC and XMP metadata.<br />
    [Exiv2 examples](http://www.exiv2.org/sample.html),
    [Exiv2 metadata reference tables
    ](http://www.exiv2.org/metadata.html).
-   [Jhead](http://www.sentex.net/~mwandel/jhead/)
    (public domain)  is a command line driven program for
    manipulating the non image parts of Exif flavour
    JPEG files that most digital cameras produce.
-   [libexif](http://libexif.sourceforge.net/)
    has one command line utilities  __exif__, and a GTK gui
    __gexif__.
-   [Metacam](http://www.cheeseplant.org/~daniel/pages/metacam.html)


# Image display

-   [xwd(1)](http://man.cx/xwd(1)) dump an image of an X window
-   [xloadimage(1)](http://man.cx/xloadimage(1))
    load images into an X11 window or onto the root window
-   [man:edisplay] is the viewer provided by
    [Exact Image](#exactimage "internal reference")
-   <a name="fbida"></a>[fbida](http://linux.bytesex.org/fbida/)
    contains __fbi__ an image viewer for framebuffer console, _ida_ a
    small motif-based image viewer. _fbgs_ is a wrapper script to
    display PostScript or pdf using _fbi_ on a framebuffer
    console. __Exiftran__ does lossless transformations of JPEG
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
    [sxiv](#sxiv "internal reference").

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
    is a fork of the older
    [gqview](http://gqview.sourceforge.net/),
    is a gtk (2 or 3) based image viewer, it does not requires gnome as many of
    its concurrent gtk browsers like **eog**. It is
    suited for photo collection maintenance: raw format, Exif/IPTC/XMP
    metadata (info from jpeg files), and integration with programs
    like UFraw, ImageMagick, Gimp, gPhoto or ExifTool.<br /> Geeqie
    has a medium footprint less than
    [Gthumb](#gthumb "internal reference") and above the lighter
    [feh](#feh "internal reference") or
    _Gpicview_.  30 M resident/25 M shared at start moving to 93M/27M
    on my image test directory. Like gthumb it does not garbage
    collect and the footprints are always increasing during a session.
    -   [Geeqie github repository
        ](https://github.com/BestImageViewer/geeqie)
-   [Gpicview](http://wiki.lxde.org/en/GPicView) (GPL)
    is a lightweight and fast image viewer for GTK+ 2.x. It has
    minimal dependencies and is quite lean 16M resident / 14M shared
    (without loaded image), it has no directory browsing capability
    and the version tested (0.2.5) has a bug that prevent to load all the jpeg
    of my test directory, so I cannot compare on my image directory, displaying
    only one jpeg of this directory it takes 32M/19M. By its
    footprints it is in the top range of GTK viewers, of course with
    an interface less user friendly than bigger viewer software.
    It is the standard picture viewer of LXDE, but has minimal
    dependencies using only GTK2 and glib2, and is desktop independant.
-   <a name="gthumb"></a>[w:Gthumb] (GPL) is an image viewer and
    organizer. It belongs to gnome but it has very mild gnome
    dependencies and is more a GTK+ software. Its features include
    filesystem browsing, slide show, image catalogs, web album
    creation, camera import, image CD burning, batch file operations
    and quick image editing features like metadata display and
    edition, transformation and color manipulationColor Adjustments,
    resizing and cropping, rotations and flips.
    -   [Gthumb Home](https://wiki.gnome.org/action/show/Apps/gthumb)
    -   [Gthumb Help](https://help.gnome.org/users/gthumb/stable/)
    -   Gthumb start at 70M resident / 49M like geeqie, it grows fast
        depending of the images displayed, but I have observed a
        better garbage collection than in the case of geeqie, for the
        same image directory gthumb grow to 151M/70M and it doesn't
        seem to shrink when moving to small or even empty directory.
        _I noticed garbage collection on a previous version, but with
        the new one tested 3.4.4 it does no more happen._
-   [Graphics Magick](#graphickmagick "internal reference)
    provide a command to display images. `gm display`.
-   [ImageMagick](#imagemagick "internal reference) display images
    with its command `display`.
-   <a name="imview"></a>[imview
    ](http://hugues.zahlt.info/software_imview.html)
    is an X11 image viewer, with limited editing capabilities.  It can
    display multiple pages tiff files. It uses no desktop environment,
    only bare X. The 1.1.9h version is from 2009, Debian use 1.1.9C
    from 2008, it is now minimally maintained. It has small memory
    footprints 9.5M resident / 8.5M shared. When loading all files from
    my test directory the memory footprint is 43M / 14M
-   [w:libjpeg|LibJpeg] contains the following utilities: `cjpeg` and
    `djpeg`, for performing file formats conversions, `rdjpgcom` and
    `wrjpgcom`, for inserting and extracting textual comments in JFIF
    files, `jpegtran` for lossless transcoding between different JPEG
    formats.
-   [Mirage](http://mirageiv.sourceforge.net/)
    is a Python/GTK  image viewer. It allow also simple image
    manipulation: rotating at 90-degree, flipping
    horizontally/vertically, resizing, cropping, and saturation.
    We can also define custom actions using shell commands and
    external executables.

    As every interpreted software the
    footprints are including the interpreter load so it
    weight 43M resident / 28M shared. This is still mild requirement
    compared to gthumb, on my test image directory it grows to
    100M/31M.

    -   [Mirage Documentation
        ](http://mirageiv.sourceforge.net/docs.html)

-   <a name="pqiv"></a>[PQIV](https://github.com/phillipberndt/pqiv)
    is the continuation of [QIV](#qiv "internal reference).
    It is an image viewer written in C using GTK 2 or GTK 3 and
    GLIB 2. It is actively maintained in 2017, and is in Debian.
    It start at 26M resident / 21M shared on a small thumbnail,
    and browsing my image test directory 64M / 21M.
-   <a name="qiv"></a>[QIV - Quick Image Viewer](http://spiegl.de/qiv/)
    (GPL) is a gdk/Imlib2 image viewer. it is in Debian.
    Development of _qiv_ stopped in 2013, but it continues in
    [PQIV](#pqiv "internal reference).
-   [Ristretto
    ](http://goodies.xfce.org/projects/applications/ristretto)
    is a fast and lightweight picture-viewer for the Xfce desktop environment.
-   <a name="sxiv"></a>[sxiv](https://github.com/muennich/sxiv)
    is a lightweight and scriptable image viewer written in C.
    Its only dependency besides xlib is imlib2. It is in Debian.
    Iis an alternative to [feh](#feh "internal reference"),
    [qiv](#qiv  "internal reference") or
    [pqiv](#pqiv  "internal reference").

    It start at 5.7M / 4.7M on a small png thumbnail and 20M /5M
    browsing my test image directory (34M / 5M when also making
    thumbnails). For those who want a very lean image viewer, it is
    the only contender to [feh](#feh "internal reference") among the
    viewer I tested.

    -   [ArchWiki: sxiv](https://wiki.archlinux.org/index.php/Sxiv)


_Notes_
:   _The memory footprints comparisons in this section are done by
    loading in the viewer a 4K png icon (emblem-debian.png 128x128)_

:   _The test image directory contains 23 jpegs of around 1MB for a
    total of 19MB_

## Image Libraries

-   [libmng](http://gjuyn.xs4all.nl/libmng/) The MNG reference
    library
-   [SDL image](http://www.libsdl.org/projects/SDL_image/docs/index.html) (GPL),
    also named _libsdl-image_ is a library used with the command
    __showimage__ for displaying image via the SDL library. It is used
    in numerous console games and also by the _Python Imaging Library
    (PIL)_


# Images Transforming


## Raster software

-   [Aafigure](http://packages.python.org/aafigure/)
    is a python utility that convert diagrams drawn using ascii
    art into bitmap graphics in _png_ format.
    Aafigure can be used with _asciidoc_, _Restructured Text_,
    _MoinMoin_, _Sphinx_
-   [CoolText online graphics generator](http://www.cooltext.com/)
-   [Ditaa](http://ditaa.sourceforge.net/)
    is a command-line utility written in Java, that convert diagrams
    drawn using ascii art into bitmap graphics in _png_ format.
    _Ditaa_ can be used with _asciidoc_, _dokuwiki_, _org mode_.
-   <a name="exactimage"></a>
    [ExactImage](https://exactcode.com/opensource/exactimage/)
    is a fork of ImageMagick, coded for speed in C++.
    It supports BMP, Digital Camera RAW, GIF, JPEG, JPEG2000, OpenEXR,
    PNG, PBM, RAW, TIFF, XPM, SVG PDF, PS, EPS, PCX, Targa, TGA. More
    formats are planed. It has utilities similar to ImageMagick ones
    `econvert`, `edisplay`, `edentify`,

    It has also [man:hocr2pdf] to create a searchable PDF from hOCR input.
    and barcode recognition with [man:bardecode]

-   <a name="gimp"></a>[Gimp](http://www.gimp.org)
    is an image manipulation and paint program.
    -   The [Gimp site](http://www.gimp.org ) references the
        [Gimp documentation](http://www.gimp.org/docs/) with
        [tutorials](http://www.gimp.org/tutorials/),
        and [books](http://www.gimp.org/books/).<br />
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
    download the image for local or offline use.<br />
    [Graphy](http://graphy.googlecode.com/)
    is a  Python library for generating charts with _Google Chart API_.
-   <a name="graphicsmagick"></a>
    [Graphics Magick](http://www.graphicsmagick.org/)
    ([bunch of MIT like licenses](http://www.graphicsmagick.org/Copyright.html))
    is a fork of [ImageMagick](#imagamagick "internal reference")
    with roughly the same capabilities. GraphicsMagick provides a
    [command line utility
    ](http://www.graphicsmagick.org/utilities.html)
    which may be used to access all GraphicsMagick functions.
    -   [display](http://www.graphicsmagick.org/display.html)
        display an image on an X window.
        Used as an image viewer _display_ has tiny footprints
        10M resident/ 8M shared both for for the the _Image Magick_ and
        _Graphics Magick_ versions. In the same range than the winner
        [feh](#feh "internal reference").
        But the user interface of display is more limited.
    -   [convert](http://www.graphicsmagick.org/convert.html)
        convert an image from one format
        to an other one
    -   see also: [animate](http://www.graphicsmagick.org/animate.html),
        [identify](http://www.graphicsmagick.org/identify.html),
        [montage](http://www.graphicsmagick.org/montage.html),
        [mogrify](http://www.graphicsmagick.org/mogrify.html),
        [composite](http://www.graphicsmagick.org/composite.html)
-   <a name="imagemagick"></a> [Image Magick
    ](http://www.imagemagick.org/)
    (Open Source free
    [custom license](http://www.imagemagick.org/script/license.php))
    is an image display and manipulation tool for the
    X Window System.

    ImageMagick can read and write JPEG, TIFF, PNM,
    GIF, and Photo CD image formats. It can resize, rotate, sharpen,
    color reduce, add special effects, convert an image, and creates
    animated or transparent .gifs, composite images, or thumbnail
    images.

    _ImageMagick_ includes the following command line tools:
    [animate](http://www.imagemagick.org/script/animate.php)
    :   animate an image sequence on an X server.
    [compare](http://www.imagemagick.org/script/compare.php)
    :   annotate the difference between an image
        and its reconstruction.
    [composite](http://www.imagemagick.org/script/composite.php)
    :   overlap one image over another.
    [conjure](http://www.imagemagick.org/script/conjure.php)
    :   interpret and execute scripts written in the Magick Scripting
        Language (MSL).
    [convert](http://www.imagemagick.org/script/convert.php)
    :   convert between image formats as well as resize an image, blur,
        crop, despeckle, dither, draw on, flip, join, re-sample, and
        more.
    [display](http://www.imagemagick.org/script/display.php)
    :   display an image or image sequence on an X server.
    [identify](http://www.imagemagick.org/script/identify.php)
    :   describe the format and characteristics of one or more
        image files.
    [import](http://www.imagemagick.org/script/import.php)
    :   save any visible window on an X server as an image file. You can
        capture a single window, the entire screen, or any rectangular
        portion of the screen.
    [mogrify](http://www.imagemagick.org/script/mogrify.php)
    :   resize an image, blur, crop, despeckle, dither, draw on, flip, join,
        re-sample, and much more. Mogrify overwrites the original image
        file, whereas _convert_ writes to a different image file.
    [montage](http://www.imagemagick.org/script/montage.php)
    :   create a composite image by combining several separate images.
        The images are tiled on the composite image optionally adorned
        with a border, frame, image name, and more.
    [stream](http://www.imagemagick.org/script/stream.php)
    :   stream one or more pixel components of the image or portion of
        the image to your choice of storage formats. It writes the
        pixel components as they are read from the input image a row
        at a time making `stream` desirable when working with large
        images or when you require raw pixel components.

    -   [ImageMagick Common Image Formats
        ](http://www.imagemagick.org/Usage/formats/)
        describe how ImageMagick works with different image formats,
        and what are the options.

-   [Hugin](http://hugin.sourceforge.net/)
    is a panorama photo stitching program.  Stitching is
    accomplished by using several overlapping photos taken from the
    same location, and using control points to align and transform
    the photos so that they can be blended together to form a larger
    image.
-   <a name="libtiff-tools"></a> [libtiff-tools
    ](http://libtiff.maptools.org)
    includes command line tools for converting TIFF images to and from
    other formats and tools for doing simple manipulations of TIFF
    images.
-   [ImageJ](https://en.wikipedia.org/wiki/ImageJ)
    (public domain see [license details](http://imagej.net/Licensing))
    is an image processing program written in Java.
    It isinspired by NIH Image for the Macintosh.
    It can display, edit, analyze, process, save and print
    8-bit, 16-bit and 32-bit images. It can read many image formats
    including TIFF, GIF, JPEG, BMP, DICOM, FITS and "raw".

    -   [ImageJ Home](https://imagej.nih.gov/)
    -   [ImageJ Wiki](http://imagej.net/)
    -   [ImageJ repository on GitHub](https://github.com/imagej/imagej)

-   [sam2p](https://code.google.com/archive/p/sam2p/) (GPL)
    is a command line utility that converts many raster (bitmap)
    image formats like GIF, JPG/JPEG, and PNG into PostScript or PDF
    files.
-   [tgif(1)](http://man.cx/tgif(1)) interactive 2-D drawing
    facility under X11.
-   [Trimage](http://trimage.org/) is a tool for losslessly
    optimizing PNG and JPG files. Trimage is in Debian.</br />
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

# Vector Graphic software {#svg}

See also the [postscript, pdf, djvu Page](/node/ps_pdf_djvu/).

## Documentation
-   Wikipedia: [w:Scalable Vector Graphics]
    an detailed review including support in browsers and software.
-   [Scalable Vector Graphics (SVG)](http://www.w3.org/Graphics/SVG/)
    from W3C
-   [Vector Markup Language (VML)
    ](http://www.w3.org/TR/1998/NOTE-VML-19980513)
    from W3C
-   [svg wiki](http://wiki.svg.org/)
-   [jan.kollhof.net svg pages](http://jan.kollhof.net/projects/svg/)

## Software
-   [Aafigure](http://packages.python.org/aafigure/)
    is used to convert drawings in plain text documents to HTML, PDF,
    SVG,png. It can be integrated with
    [docutils](/node/rest#docutils "internal reference"),
    [Sphinx](/node/rest#sphinx "internal reference"),
    [MoinMoin](http://moinmo.in/).
-   [Autotrace](http://autotrace.sourceforge.net/) (GPL) is a bitmaps
    to vector graphics converter. It was and may be still the more
    achieved open source vectorisation program. but don't seem any
    longer developped since 2004. [potracegui](http://potracegui.sourceforge.net)
    is a gui frontend that support potrace and autotrace.
-   [Blockdiag](http://blockdiag.com/en/index.html) is a set of graph generators
    from text source similar to [graphviz](#graphviz "internal reference")’s `dot` format.
    It includes  block diagrams, sequence diagrams,  activity diagrams, and network diagrams.<br />
    In the [sphinx contribs](https://bitbucket.org/birkenfeld/sphinx-contrib)
    there is a [Sphinx](/node/rest#sphinx "internal reference") extension for _Blockdiag_.
-   [Dia](http://live.gnome.org/Dia) (GPL) a GTK+ based diagram
    creation program that save diagrams to a custom XML format and can
    export them to EPS, SVG, XFIG, WMF and PNG, ...
-   [Ditaa](http://ditaa.sourceforge.net/)
    is a java tool that convert ascii art to bitmap diagram (or EPS
    with a plugin), _no vector graphic presently_. It can be used
    within DocuWiki, [Org Mode](/node/org-mode "internal reference").
-   [Gnuplot](http://www.gnuplot.info/)
    [ad-hoc Open Source License
    ](http://gnuplot.cvs.sourceforge.net/gnuplot/gnuplot/Copyright)
    is a
    portable command-line driven interactive data and function plotting
    utility Gnuplot supports plots in either 2D and 3D, Gnuplot can
    output to many file formats (eps, fig, jpeg, LaTeX, metafont, pbm,
    pdf, png, postscript, svg, ...).
    -   [gnuplot development at sourceforge](http://gnuplot.sourceforge.net/)
         best site to find recent documentation, tutorials, demo.
    -   [gnuplot documentation](http://www.gnuplot.info/documentation.html):
        [gnuplot v4.6 manual](http://www.gnuplot.info/docs_4.6/gnuplot.pdf)
    -   [GNUPLOT 4.2 - A Brief Manual and Tutorial
        ](http://www.duke.edu/~hpgavin/gnuplot.html)
    -   [gnuplot demos](http://gnuplot.sourceforge.net/screenshots/)
-   <a name="inkscape"></a>[inkscape](http://www.inkscape.org/)
    is a SVG based generic vector-drawing program.
    -   Wikipedia [w:Inskcape]
    -   Documentation:
        [inskape manual
        ](http://tavmjong.free.fr/INKSCAPE/MANUAL/html/index.php)
        by Tavmjong Bah in french or spanish
        _(Documenting Inkscape versions 0.47 and 0.48)_,
        [Inkscape User Manual
        ](http://www.angelfire.com/mi/kevincharles/inkscape/index.html)
        by Kevin Wixson,
    -   [Keys and Mouse Reference](http://www.inkscape.org/doc/keys.html),
    -   [TutorialsAndHelp
        ](http://wiki.inkscape.org/wiki/index.php/TutorialsAndHelp).
    -   When you install the _inskape package it places in the
        directory `/usr/share/inkscape` a directory of `examples` and
        `tutorials`
-   [ivtools](http://www.ivtools.org/ivtools/) drawing editors for
    PostScript, TeX, and web graphics and vector graphic shell
    _no longer developed, since 2009_.
-   [w:libsrvg]
    is the gnome SVG rendering library  The  command-line _rsvg_
    part of the package _librsvg2-bin_ convert SVG files into
    raster images.
-   [Mscgen](http://www.mcternan.me.uk/mscgen/) is a  program that
    parses Message Sequence Chart descriptions and produces PNG, SVG, EPS
    or server side image maps (as the output.
    Mscgen integrates with _Asciidoc_, _Doxygen_, _Sphinx_, _Org Mode_, _Latex_.
-   [OpenClipArt](http://www.openclipart.org/) is a library of public domain clipart in vector format.
-   [potrace](http://potrace.sourceforge.net/) (GPL) is a vector conversion program
    that can transform bitmaps in PBM, PGM, PPM, or BMP format to vector
    graphics in EPS, PostScript, PDF, SVG, Xfig, Gimppath, and PGM.
    potrace is now embedded in inkscape, you find it in the menu
    `Path/Trace Bitmap` see also the
    [inkscape wiki](http://wiki.inkscape.org/wiki/index.php/Potrace "/wiki.inkscape.org Potrace").<br />
    [potracegui](http://potracegui.sourceforge.net) (GPL) is a gui frontend
    for potrace and autotrace.
-   [pstoedit](http://www.pstoedit.net/pstoedit "pstoedit.net")
    (GPL) translates PostScript and PDF graphics into other vector
    formats: tgif, xfig, pdf, gnuplot, dxf-cad, hpgl, wmf, pic (troff),
    latex picture, kontour, plotutils, skencil, swf, svg, ...
    [pstoedit manual](http://www.helga-glunz.homepage.t-online.de/pstoedit/pstoedit.htm)
-   [Skencil](http://www.skencil.org/) (LGPL)
    is a vector drawing program. The development of Skencil stopped in
    2010, but the sK1 team gave a new start to the project, you find
    the new 1.x release on
    [sK1 page for Skencil
    ](http://sk1project.org/viewpage.php?page_id=21).
-   [sK1](http://sk1project.org/)
    is an open source vector graphics editor similar to CorelDRAW.  It
    is a fork of Sketch/Skencil, but while Skencil is developped
    against GTK+, sK1 uses TK. It also aim to be compatible with Corel
    Draw and Adobe Illustrator. It is packaged for main distributions.
-   [tgif](http://bourbon.usc.edu:8001/tgif/) (Q public license
    *trolltech*) drawing Program for the X Window System.
-   [Uniconvertor](http://sk1project.org/modules.php?name=Products&product=uniconvertor)
    is a universal vector graphics translator.<br />
    It can convert from:
    CorelDRAW, Adobe Illustrator, Postscript, Encapsulated Postscript,
    Computer Graphics Metafile, Windows Metafile (WMF), XFIG,
    Scalable Vector Graphics, Skencil/Sketch/sK1, Acorn Draw;
    to:
    Adobe Illustrator, Postscript, Computer Graphics Metafile, Windows Metafile,
    PDF, Sketch/Skencil, sK1, SVG.<br />
    It is available in Debian as _python-uniconvertor_.
-   [VectorMagic](http://vectormagic.com "/vectormagic.com")
    (proprietary closed license), convert bitmap images in
    JPEGs, GIFs and PNGs formats to EPS, SVG, and PDF
    It is a piece software  expensive to purchase, they also propose
    a 3 month subscription to online conversion, with a free trial.
-   [Veusz](http://home.gna.org/veusz/) (GPL)
    is a scientific plotting package written in python, PyQt and NumPy.
    Veusz produces plots in PNG, PDF, Encapsulated PostScript and SVG.
-   [XFig](http://www.xfig.org/ "xfig.org") A menu-driven tool to
    draw and manipulate objects interactively in an X window, with
    output to latex graphic formats or raster files thru *transfig.*

## Online Web software
-   [draw.io](https://www.draw.io/) is an onlinr free tool to edit
    diagrams. They can be saved in xml and exported as svg, or
    numerous raster formats.
-   [Gravit.io](http://gravit.io)
    is a web based drawing editor including Vector
    Illustration that can be exported as SVG.
-   [Inker](http://www.graphics.com/resource/inker)
    Is a free web based svg editor, that ca save in SVG and EPS.
    There is also an android app.
    -    [Inker web app](http://app.inker.co/)
-   [Vector Paint](http://vectorpaint.yaks.co.nz/)
    is an online Web SVG Editor, with svg download and optional export
    to png/speg.



## Graphviz {#graphviz}

[Graphviz](http://www.graphviz.org/) (Common Public License) is a
graph Visualization Software. It includes _dot_ for drawing directed
graphs, and _neato_ for drawing undirected graphs.

-   [An Introduction to GraphViz](http://www.linuxjournal.com/article/7275)
    by Mihalis Tsoukalos in _linux journal_.
-   [Graphviz Resources](http://www.graphviz.org/Resources.php)
-   Many python modules generate dot files and use them with
    graphviz:
    -   [python-graph](http://code.google.com/p/python-graph/)
        (MIT license) is a library for working with graphs in
        Python. It is in Debian.
    -   [GvGen](http://www.picviz.com/en/community/gvgen/gvgen.html)
        python class to produce dot language for easy scripting.
    -   [pydot](http://code.google.com/p/pydot/)(MIT License)
        allows to easily create both directed and non directed
        graphs from Python.
        It has Python 3 support.
    -   [yapgvb](http://code.google.com/p/yapgvb/) (BSD License)
        Python bindings to Graphviz,
    -   [NetworkX](http://networkx.lanl.gov/) package for the
        creation, manipulation, and study of the structure,
        dynamics, and functions of complex networks. It can output
        to Graphviz with[pygraphviz
        ](http://networkx.github.io/documentation/latest/examples/pygraphviz/)
    -   [dot2tex](https://pypi.python.org/pypi/dot2tex) (MIT
        License) by  Kjell Magne Fauske convert dot language to
        tex + PSTricks or PGF/TikZ.  [dot2tex source repository
        ](http://code.google.com/p/dot2tex/).
-   Some modules output a representaion of SQL Databases.
    -   [PostgreSQL Autodoc](http://www.rbt.ca/autodoc/index.html)
        run through PostgreSQL system tables and returns HTML, Dot,
        Dia and DocBook XML which describes the database.
    -   [SQLpp](http://www.codeproject.com/Articles/4603/A-scripted-SQL-query-generation-framework-with-IDEA)
        is a query generation framework with output to Dot.
    -   [SQLFairy](http://sqlfairy.sourceforge.net/)
        is a group of Perl modules that manipulate
        database schemas. It can convert among different dialects
        of CREATE syntax, visualizations of schemas with GraphViz
        or GD, automatic code generation, and more.
    -   [Sql2Dot](http://www.graphviz.org/Misc/sql2dot/)
        is a java parser to transform PostgreSQL sql into dot.
-   [Sphinx](/node/rest#sphinx "internal reference")
    has the extension [sphinx.ext.graphviz
    ](http://sphinx-doc.org/ext/graphviz.html)
    to embed Graphviz graphs in Sphinx Rest.
    source.
-   [MediaWiki Extension: GraphViz
    ](http://www.mediawiki.org/wiki/GraphViz)
    uses Graphviz and Mscgen  to create and
    display graphs as inline images.
-   [Graphviz filter for AsciiDoc
    ](http://asciidoc.org/asciidoc-graphviz-sample.html)
    allow to draw graphs via graphviz in
    [Asciidoc](/node/asciidoc "internal reference").
-   [gitit plugin Dot.hs
    ](https://github.com/jgm/gitit/blob/master/plugins/Dot.hs)
    allows you to include a graphviz dot diagram in a _gitit_ page.
-   [Xdot](http://code.google.com/p/jrfonseca/wiki/XDot) (LGPL) is an
    interactive viewer for Graphviz dot files written in python
    with PyGTK and Cairo.
-   [graph-easy](http://search.cpan.org/~tels/Graph-Easy/bin/graph-easy) (GPL)
    is a Perl module which can convert between many formats including
    _dot_ and render graphs.  You can use it to output to formats not
    supported by the graphviz suite, such as ASCII art.

# Static Images gallery
-   [Sigal](http://sigal.saimon.org/en/latest/)
    a python static gallery generator taht uses the javascript libraries
    [colorbox](http://www.jacklmoore.com/colorbox),
    [galleria](http://galleria.io/) and [photoswipe ](http://photoswipe.com/)
-   [lazygal](https://sml.zincube.net/~niol/repositories.git/lazygal/about/) (GPL)
    is a static web gallery generator written in Python. It is in Debian.
-   [Gallery](https://github.com/horgh/gallery) (GPL)
    is a go language program to create a static photo gallery website.
    _don't confuse with the dead php program [Gallery](http://galleryproject.org/)._kee
-   [photon](https://www.saillard.org/programs/photon/) (GPL)
    A python 2 image gallery generator. It is in Debian, I have not found the source
    repository.
<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
