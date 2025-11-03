---
title: Tag, playlist, lyrics Management
---

<!-- [[file:../../../../content-org/notes/media_notes/sound_notes.org::#tags][Tags Notes]] -->

# References

-   [id3.org - ID3 tags Home](http://id3.org/) has references for the
    id3 format, and its implementation. There is a complete
    [list of ID3 implementations](http://id3.org/Implementations)
    containing library bindings in each language and softwares for all OSes.
-   [ArchWiki: ID3 Tag Problems
    ](https://wiki.archlinux.org/index.php/ID3_Tag_Problems)
    deals with problem with multiple versions of id3 tags.

# Tag Management Software
-   [List of audio tag editors - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Audio_tag_editors)

[amded](https://github.com/ft/amded).
:    _amded_ by Niels Giesen is a command line tagging program based
     on {{< iref "#taglib" "taglib" >}}.
     It can be used from Emacs with
     [tagit.el](https://github.com/pft/elisp-assorted/blob/master/taggit.el)
     Taggit.el has support for Dired mode and Mingus.

[Cowbell](http://www.more-cowbell.org/cowbell/)(GPL)
:   _Cowbell_ is a music organizer and tag graphic editor. It allows viewing and editing
    of the mp3, flac, ogg, MusePack, tags, It can guess information with the help of
    Amazon Web Services and has a gtk2 interface or alternatively a command-line based
    batch tagger. Cowbell is written in _mono_ and is in Debian.

[Demlo](https://gitlab.com/ambrevar/demlo) (MIT license)
:   is a music library organizer and batch music tagger powered by Lua and FFmpeg.

    It can transcode, fix case, generate cue sheets, onl tag with MusicBrainz, manual
    edit tags with your favorite editor, download cover, change folder hierarchy
    according to tags or file properties.

    _Since 2018 the project is no longer active (as far as 2023)._

    -   [Demlo - ArchWiki](https://wiki.archlinux.org/title/Demlo)

<a name="easytag"></a>[EasyTag](https://wiki.gnome.org/Apps/EasyTAG/)
:   EasyTAG is an GUI utility for viewing, editing and writing tags of MP3, MP2 files
    (ID3 tag), FLAC files (FLAC Vorbis tag), Ogg Opus, Ogg Speex and Ogg Vorbis files
    (Ogg Vorbis tag), MP4/M4A/AAC files (MPEG-4 Part 10 tag), and MusePack, Monkey's
    Audio files (APE tag).  _in Debian_

    -   [EasyTag manual](https://help.gnome.org/users/easytag/stable/)
    -   [easytag(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=easytag)

[eyeD3](http://eyed3.nicfit.net/)<a name="eyed3"></a>
:   EyeD3 (GPL) is a Python module and command line tag editor for processing ID3 tags
    v1.0/v1.1 and v2.3/v2.4. _only id3 no ogg vorbis/opus comment_. It can also retrieve
    information such as length and bit rate from an MP3 file.

    -   [Command Line Tool documentation
        ](http://eyed3.nicfit.net/cli.html)

<a name="exfalso"></a>[ExFalso](https://github.com/quodlibet/quodlibet)
:   ExFalso is part of
    {{< iref "media_players#quodlibet" "quodlibet" >}}
    media player, and a python/GTK+ frontend to {{< iref "#mutagen" "mutagen" >}}.

    With the ExFalso gui, a command line _oberon_ is also provided.

    In Debian _exfalso_ and {{< iref "media_players#quodlibet" "quodlibet" >}} are two
    distinct packages.

    -   [ExFalso/Quodlibet manual
        ](https://quodlibet.readthedocs.org/en/latest/)

<a name="hachoir-metadata"></a>
[hachoir-metadata](http://bitbucket.org/haypo/hachoir/wiki/hachoir-metadata)
:   _hachoir-metadata_ is a python program to extract metadata using
    Hachoir library _so it is a tag viewer not a tag editor_.
    _hachoir-metadata_ extracts metadata from multimedia files: music,
    picture, video, but also archives.<br /> It supports most common
    file formats:

    -   Archives: bzip2, gzip, zip, tar;
    -   Audio: MPEG audio ("MP3"), WAV, Sun/NeXT audio, Ogg/Vorbis (OGG), MIDI, AIFF, AIFC, Real audio (RA);
    -   Image: BMP, CUR, EMF, ICO, GIF, JPEG, PCX, PNG, TGA, TIFF, WMF, XCF
    -   Video: ASF format (WMV video), AVI, Matroska (MKV), Quicktime (MOV), Ogg/Theora, Real media (RM)

id3ren
:   _id3ren_ is an id3 tagger and renamer that can be used for batch processing mpeg3 files.
     The id3 fields can be set on the command line, entered interactively,
    or “guessed” from the path and the filename. _in Debian_

<a name='kid3'></a>[Kid3](http://kid3.sourceforge.net/) (GPL)
:    Kid3 is a Qt interface to {{< iref "#taglib" "taglib" >}} It can process MP3,
     Ogg/Vorbis, Opus, DSF, FLAC, MPC, APE, MP4/AAC, MP2, Speex, TrueAudio, WavPack,
     WMA, WAV, AIFF.  Kid3 allow easy mass tagging. It can be compiled with or without
     KDE, and can be used in any desktop environment.

    -   [The Kid3 Handbook](http://kid3.sourceforge.net/kid3_en.html)
    -   [kid3-cli](http://kid3.sourceforge.net/kid3_en.html#kid3-cli)
        offers a command-line-interface for Kid3. It is packaged
        separatly in Debian, and does not require any QT/KDE library.

[lltag](http://home.gna.org/lltag/) (GPL)
:   _lltag_ is a perl frontend to tag (and rename) mp3/ogg/flac files automagically. It
    uses mp3info, vorbiscomment and metaflac.  It may be used to tag multiples files at
    once by comparing their filename or pathname against a configurable list of formats,
    or by getting tags from the CDDB database. lltag may also rename files according to
    a configurable filename format.

    Because it is a script calling command tools, it can be slow when tagging a great
    number of files.

<a name="puddletag">[puddletag](https://docs.puddletag.net/) (GPL-3.0)
:   _puddletag_ is a Linux tag editor similar to the Windows program _Mp3tag_. It uses a
    spreadsheet-like layout to provide quick access to any tag. Supported formats:
    ID3v1, ID3v2 (mp3), MP4 (mp4, m4a, etc.), VorbisComments (ogg, flac), Musepack
    (mpc), Monkey’s Audio (.ape) and WavPack (wv).

    _puddletag_ is written in python/QT and uses the {{< iref "#mutagen" "mutagen" >}}
    library. It is in Debian.

    -   [puddletag GitHub repository](https://github.com/keithgg/puddletag).
    -   [puddletag documentation](https://docs.puddletag.net/docs.html)

[pyrenamer](http://www.infinicode.org/code/pyrenamer/) (MIT License)
:   mass file renamer _not a tag editor_ written in PyGTK that can use
    {{< iref "#hachoir" "hachoir-metadata" >}} or {{< iref "#eyed3" "eyed3" >}} You can
    rename files using patterns, search and replace, substitutions, insert or delete
    text. You can also rename images using their EXIF tags and music using their
    metadata tags.

    It seems to be a short lived project from 2017, it is no more packaged in Debian.
    Many othr tag editor like {{< iref "#puddletag" "Puddletag" >}} alow also renaming
    based on tags.
<a name="pytagsfs"></a>[pytagsfs](https://github.com/david-morris/pytagfs) (AGPL-3.0)
:   pytagsfs is a FUSE filesystem that arranges media files in a virtual directory
    structure based on the file tags. It is in Debian.

:   File tags can be changed by moving and renaming virtual files and directories.

:   The command line utility [pytags(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=pytags&apropos=0&sektion=0&manpath=Debian+unstable+sid&format=html&locale=en)
    set and remove tags on media files from filename and options .

:   The mount command is named [pytagsfs(1)
    ](http://manpages.debian.org/cgi-bin/man.cgi?query=pytagsfs&sektion=1&apropos=0&manpath=Debian+unstable+sid&locale=en)

<a name="tagtool">[Tagtool](http://sourceforge.net/projects/tagtool/)</a> (GPL-2.0)
:   Audio Tag Tool (GPL)is a program to manage the information fields in MP3 and Ogg
    Vorbis files.

    The most useful features are the ability to easily tag or rename hundreds of files
    at once, in any desired format.

    _Tagtool is no longer in Debian, sources from 2008._
[getID3](http://getid3.sourceforge.net/) (GPLv3, LGPL, MPL)
:   A PHP5 script that extracts useful information from MP3s & other multimedia file
    formats

[Thunar](http://docs.xfce.org/xfce/thunar/)
:   Thunar, the xfce file mnager, has a _media tag plugin_ that allows to rename
    multiple media files at once using the tags and edit media tags (i.e. ID3 tags) from
    within Thunars file properties dialog.

# Libraries
<a name="id3lib"></a>id3lib (LGPL)
:   [id3lib](http://id3lib.sourceforge.net/)  provides a software library for
    manipulating ID3v1 and ID3v2 tags. It provides a convenient interface for software
    developers to include standards-compliant ID3v1/2 tagging capabilities in their
    applications. Features include identification of valid tags, automatic size
    conversions, (re)synchronisation of tag frames, seamless tag (de)compression, and
    optional padding facilities.  The code date from 2003 and seems no longer updated.

:   Id3lib (alias id3lib) is used by grip, {{< iref "#easytag" "easytag" >}} and
    {{< iref "#tagtool" "tagtool" >}}

:   It has some small utilities `id3cp`, `id3info`, `id3convert`, id3tag, which are in
    the _debian_ package _libid3-tools_; and a separate package
    [id3v2](http://sourceforge.net/projects/id3v2/ "sourceforge.net id3v2") (LGPL) gives
    a command-line tool to add, modify, remove, or view ID3v2 tags, as well as convert
    or list ID3v1 tags.

:   Refs:
    [id3lib.sourceforge.net](http://sourceforge.net/projects/id3lib),
    [id3V2 standard](http://sourceforge.net/projects/id3),
    [ID3v2.3 Programming Guidelines](http://id3lib.sourceforge.net/id3guide.html)

libid3tag (GPL)
:   libid3tag is a a library for reading and (eventually)
    writing ID3 tags. libid3tag is coming with the
    [mad](http://www.underbit.com/products/mad/) project. both ID3v1
    and the various versions of ID3v2.

mp4v2 (Mozilla public license)
:   [mp4v2](https://github.com/enzo1982/mp4v2) is a C/C++ library to create, modify and
    read MP4 files.

<a name="mutagen"></a>[mutagen](https://bitbucket.org/lazka/mutagen) (GPL)
:   Mutagen is a Python module to handle audio metadata it comes with a GTK frontend
    named {{< iref "#exfalso" "ExFalso" >}}.  It supports AIFF, AAC, ASF, FLAC, MP4,
    MP3, Ogg FLAC, Ogg Speex, Ogg Theora, Ogg Vorbis, Monkey audio, True Audio,
    OptimFROG, and WavPack audio files, since v1.21 (2013) Ogg opus. All versions of
    ID3v2 are supported, and all standard ID3v2.4 frames are parsed.

:   [Mutagen Documentation](https://mutagen.readthedocs.org/en/latest/)

:   Mutagen is used in the players {{< iref "media_players#quodlibet" "quodlibet" >}},
    and {{< iref "media_players#exaile" "Exaile" >}} thru the __ExFalso__ plugin.

    It is also used in the tag editing frontends {{< iref "#exfalso" "ExFalso" >}} which
    is the reference implementation of mutagen, and part of the
    {{< iref "media_players#quodlibet" "quodlibet" >}} software,
    {{< iref "#pytagsfs" "pytagsfs" >}} and {{< iref "#puddletag" "puddletag" >}}.

:   [The Building Coder: MP3 Manipulation Using Python, Mutagen and Ffmpeg
    ](http://thebuildingcoder.typepad.com/blog/2013/02/mp3-manipulation-using-python-mutagen-and-ffmpeg.html)
    is a mutagen usecase.

<a name="taglib"></a> [Taglib](http://developer.kde.org/~wheeler/taglib.html) (GPL)
:   Taglib is a library for reading and editing the meta-data
    of audio formats, the library is usually _libtag1_ and C bindings
    are found in _libtagc0_. It supports both ID3v1 and ID3v2 and/or Ogg
    Opus/Vorbis comments in MP3, FLAC, MPC, Opus, Speex, Vorbis, WavPack and TrueAudio
    files. Taglib page says it is times faster than id3lib, it is
    written in C++ and while part of KDE it has no dependency to KDE or
    QT. It is used in numerous applications including
    audacious-plugins,
    {{< iref "media_players#amarok" "amarok" >}},
    {{< iref "#cowbell" "cowbell" >}},
    emms, forked-daapd, gmediaserver,
    {{< iref "streaming#gstreamer" "gstreamer-plugins" >}},
    {{< iref "#kid3" "kid3" >}} and
    {{< iref "#kid3" "kid3-cli" >}},
    {{< iref "streaming#gerbera" "Gerbera" >}},
    {{< iref "media_players#moc" "moc" >}},
    {{< iref "media_players#ncmpcpp" "ncmpcpp" >}}, ...

    -   [tagpy](http://mathema.tician.de/software/tagpy)
        provides python bindings to Taglib

# Cue, bookmarks, Audiobooks
## Cue sheet {#cuesheet}
A {{< wp "Cue_sheet_(computing)"  "Cue sheet" >}} is a metadata file which
describes how the tracks of a CD or DVD are laid out. For audio files
they are usefull when a big record contain many titles. Quite few
Linux music players support Cue sheets: {{< iref "media_players#amarok" "Amarok" >}},
{{< iref "media_players#audacious" "Audacious" >}} through the .cue plugin,
{{< iref "media_players#clementine" "Clementine" >}},
{{< iref "media_players#deadbeef" "DeaDBeef" >}},
{{< iref "media_players#cmus" "cmus" >}}*partial support*,
{{< iref "media_players#guayadeque" "Guayadeque" >}},
{{< iref "media_players#kodi" "Kodi" >}},
{{< iref "media_players#mpd" "MPD" >}},
{{< iref "media_players#mplayer" "Mplayer" >}},
{{< iref "media_players#qmmp" "Qmmp" >}},
{{< iref "media_players#strawberry" "Strawberry" >}}
{{< iref "media_players#xmms2" "xmms2" >}} with the cue plugin, _and other, I have not
checked!_.

FLAC, Monkey's audio and Wavpack support embedded cuesheet by using a `CUESHEET` tag,
but the effective support depend on the player, some may even support the `CUESHEET` mp3
tag.

-   [Audacity Wiki: Cue sheets](http://wiki.audacityteam.org/wiki/Cue_sheets)
-   [Hydrogenaudio.org Cue Sheet wiki
    ](http://wiki.hydrogenaudio.org/index.php?title=Cue_sheet)
-   [Kodi Wiki - Cue sheets](https://kodi.wiki/view/Cue_sheets),
    [Useful Cue Sheet Editing Applications
    ](https://kodi.wiki/view/Cue_sheets#Useful_Cue_Sheet_Editing_Applications)
-   [The Mixing Bowl](http://wiki.themixingbowl.org/Main_Page):
    [Cue Sheets](http://wiki.themixingbowl.org/Cue-Sheets)
-   [ArchWiki: Cue Splitting
    ](https://wiki.archlinux.org/index.php/CUE_Splitting)
-   [cuetools](https://github.com/svend/cuetools)
    is a set of programs for manipulating CUE sheet (cue) files and Table of Contents
    (toc) files. It contains the following utilities: cueconvert, cuebreakpoints,
    cueprint, cuetag.
-   [Label2Cue Convertor](http://sourceforge.net/projects/label2cue/)
    is a java tool to convert Audacity label files to .cue files.
-   [lbl2cue / cue2lbl](http://grimblefritz.com/audacity/)
    are two php script scripts to convert audacity label files to .cue files and .cue
    files to label files. They are available online at the previous address.
-   [labelcue](http://forum.audacityteam.org/download/file.php?id=3489)
    is a bash script to convet labe to cue. It needs some
    [bc functions (from pixelbeat)](http://www.pixelbeat.org/scripts/bc).
    _DJ Kaboodle_ the author explain how he use it in
    [Burning Mixes to CD How To
    ](http://www.djkaboodle.co.uk/blog/2011/may/29/burning-mixes-cd-how)
-   [split2flac](https://github.com/ftrvxmtrx/split2flac)
    Is a bash script to split flac/ape/wv/wav + cue sheet into separate tracks .
-   [cuesplit.sh](tps://bbs.archlinux.org/viewtopic.php?id=75774)
    is very simple shell script that use shntool and cuetools to split ape flac mp3 ogg
    tta wv wav files using a cue sheet.
-   [Flacon](https://flacon.github.io/) (GPL)
    extracts individual tracks from one big WAV, FLAC, APE, WavPack, True Audio (TTA)
    audio, using a CUE sheet and save them in FLAC, WAV, WavPack, AAC, ogg/vorbis, Opus
    or MP3. Flacon has an unofficial debian package, and a flatpack.
    -   [flacon Wiki · GitHub](https://github.com/flacon/flacon/wiki)
-   [ytbtocue](https://github.com/trialuser02/ytbtocue) (BSD License)
    _YouTube to CUE Converter_, a C++ program to download audio file using _youtube-dl_
    and generates Cue Sheet with metadata.


{{< iref "media_players#mpd" "mpd" >}} support cuesheets with an integrated parser which
works with both external and embedded cuesheets.

The command

    mpc load albumx/x.cue

loads the file `music_directory/albumx/x.cue` as playlist.

The cuesheet shoulf have the `FILE` value relative to the cueesheet
directory, usually the same directory where is placed the `.cue` file.
_It should not be relative to the music directory, as it is the case
for playlists._

In the case of an CUESHEET tag you can issue

    mpc load albumx/x.flac.


Few clients have cue sheet support, you can use cantata and ncmpcpp.


-   [cuetools](http://developer.berlios.de/projects/cuetools) is a set of
    utilities to manipulate cue files.

## Bookmarks {#bookmark}
The following players have bookmarks: amarok, banshee, exaile thru plugin, quodlibet,
{{< iref "media_player#moc" "Moc" >}},
{{< iref "media_player#vlc" "VLC" >}}, {{< iref "media_player#smplayer" "Smplayer" >}}.

Exaile has only one bookmark list, no export, no edit, clementine has none.

VlC has one active bookmark list that can be [saved and loaded with the playlist
](https://wiki.videolan.org/How_to_save_bookmarks).
You can edit the bookmark file from the play list, the
bookmark GUI interface allow only to add and delete them.

There is also a [VLC extension: Resume Media
](http://addons.videolan.org/content/show.php/Resume+Media+V3.40+%28Win%2BLin%29?content=165231)
that offer an extended bookmarking. _not tested_

VLC has also the possibility to play parts of media by using playlist
with the following structure:

    #EXTVLCOPT:start-time=28
    #EXTVLCOPT:stop-time=36
    video.mp4
    #EXTVLCOPT:start-time=500
    #EXTVLCOPT:stop-time=550
    video.mp4
    #EXTVLCOPT:start-time=900
    #EXTVLCOPT:stop-time=1100
    video2.mp4

{{< iref "media_player#smplayer" "Smplayer" >}} can add bookmark with a key shortcut
Ctrl-A by default, or the menu under the *Browse" section, this menu allows also to edit bookmarks.

You may prefer to use {{< iref "#chapter" "Chapters" >}} which is a portable
bookmarking solution with a format which depend on the container, but stable across
players with chapter support.

But bookmark are used for short term tasks, and have usually a life cycle a lot shorter
than chapter.

All the previous bookmarking solutions are specific to a software piece and not
shareable, with an other media player.

## Chapters {#chapter}
Chapters record navigation points for a media file. They are used for
[enhanced podcasts](https://en.wikipedia.org/wiki/Podcast#Enhanced_podcasts)
or
[podcasts novels or podcast audiobooks
](https://en.wikipedia.org/wiki/Podcast#Podcast_novels)

Chapters are available in many containers MP4, Matroska (MKV), Ogg.

A chapter is only a comment like:

    CHAPTER001=00:00:00.000
    CHAPTER001NAME=Chapter 1
    CHAPTER002=01:00:00.000
    CHAPTER002NAME=Chapter 2

-   [Chapter Marks for MP3, MP4 Audio and Vorbis Comment (Enhanced Podcasts)
    ](https://auphonic.com/blog/2013/07/03/chapter-marks-and-enhanced-podcasts/)
     from [auphonic.com](https://auphonic.com/).
    this post contains example files to demonstrate chapters in MP4 (M4A), MP3, Ogg
    Vorbis, Opus.
-   [matroska chapter extension
    ](http://savvyadmin.com/adding-chapters-to-videos-using-mkv-containers/)
-   [Ogg chapter extension ](https://wiki.xiph.org/Chapter_Extension)
-   [Podcast Comparison, Part 3: Ogg Vorbis Metadata (Vorbis Comment)
    ](https://auphonic.com/blog/2012/01/22/podcast-comparison-part-3-ogg-vorbis-metadata-vorbis-comment/).
-   [Auphonic Blog: Automatically generate Shownotes, Summaries and Chapters from
    Recordings
    ](https://auphonic.com/blog/2023/06/12/auto-generate-shownotes-summaries-and-chapters-from-recordings/)
    uses AI to add chapters and shownotes.

The name {{< wp "Vorbis Comment" >}} may be misleading, it is the format of comments
{{used in Ogg containers for vorbis, opus, speex theora. In ogg containers the chapters
are embedded in vorbis comments.

On Linux chapters are recognized by {{< iref "media_players#vlc" "VLC" >}},
{{< iref "media_players#qmmp" "Qmmp" >}},
{{< iref  "media_players#mpv" "mpv" >}} with a plugin.

They are not used by exaile, smplayer, clementine, strawberry, sayonara, Rhythmbox.

Nevertheless with the players that support cue file and no chapter you can extract the
metadata with:
```sh
ffmpeg -i audio_file.m4b -f ffmetadata audio_file.meta
```
and generate a cue file based on these metadata.

On Android you can use the open source
[Voice Audiobook Player](https://f-droid.org/en/packages/de.ph1b.audiobook/)
to read audiobooks and navigate by chapters.

[AntennaPod](https://f-droid.org/en/packages/de.danoeh.antennapod/)
is a podcast client which displays chapter marks with URLs.

## Podcasts
See also [Podcast Client Feature Comparison Matrix
](https://docs.google.com/spreadsheets/d/1c2L14UVH1xtN4iDG4awheLbMgPCQgaKEamUauWs1gps/edit).
where it is said that neither amarok, banshee, gpodder, miro,
rythmnbox, hpodder (_obsolete_) support chapters; and gpodder is the
only one to support bookmarks. Most IOS clients have support for
chapters.

-   [gPodder](http://gpodder.org/) (GPL) is a python software
    that downloads and manages, and play audio and video podcasts.
    It is available for Linux, FreeBSD, Windows, Mac OS X, Sailfish
    OS, Android, and some devices. gpodder is in Debian.
    -   [gPodder Wiki](http://wiki.gpodder.org/wiki/Main_Page)
    -   [gPodder GitHub repository
        ](https://github.com/gpodder/gpodder)
    -   [How to run the latest git development version of gPodder
        ](http://wiki.gpodder.org/wiki/Git)
-   [awesome-mpv - Playback](https://github.com/stax76/awesome-mpv#playback)
    list many chapter scripts for mpv.

## Audiobook
Audiobooks use often the {{< wp "MPEG-4" >}} part 14 {{< wp "MP4 file format" >}}.

Audiobooks can also use an other format and a {{< iref "#cuesheet" "cue sheet" >}}.

For encoding we may use {{< iref "ffmpeg" "ffmpeg" >}} or
{{ iref "sound_edit#faac" "ffac" >}}.

-   [ArchWiki: audiobook](https://wiki.archlinux.org/index.php/Audiobook)
    present how to create ios compatible audiobooks, that is, how to
    convert to AAC and {{< wp "MP4_file_format"  "mp4b" >}} using command line tools like
    [MP4Box](https://wiki.gpac.io/MP4Box/MP4Box/) _from the GPAC package_,
    faac encoder and the tools in the package mp4v2-utils.
-   [Audio Book Creator - abc](http://www.ausge.de/ausge-download/abc-info-english)
    creates iPod compatible audiobooks including chapters. The licence is not given in
    the home page nor a link to the source code. The maintenance is unknown.
-   [GPAC - Open Source multimedia framework](https://gpac.io/) (LGPL)
    provide [MP4Box multimedia packager](https://wiki.gpac.io/MP4Box/MP4Box/).
    It is in the Debian Package _gpac_.
    -   [GPAC Wiki](https://wiki.gpac.io/)
-   [Libation](https://github.com/rmcrackan/Libation/) (GPL-3.0)
    an open source Audible audiobook manager that can download audiobooks and remove
    DRM. œ:w
-   [m4b-tool](https://github.com/sandreas/m4b-tool) (MIT license)
    is a command line utility to merge, split and chapterize audiobook files such as
    mp3, ogg, flac, m4a or m4b.
-   [m4b-merge](https://github.com/djdembeck/m4b-merge) (GPL-3.0)
    A python CLI tool which outputs consistently sorted, tagged, single m4b files.
-   [inAudible-NG/tables](https://github.com/inAudible-NG/tables)
    a rainbow table password cracker with tables suited to audible activation bytes.
-   [m4b-tool](https://github.com/sandreas/m4b-tool) (MIT license)
    command line utility to merge, split and chapterize audiobook files such as mp3,
    ogg, flac, m4a or m4b

## WebVTT
[WebVTT: The Web Video Text Tracks Format](https://w3c.github.io/webvtt) support
inclusions of cue files. WebVTT cues allow to include hierarchical chapters.

Xiph.org plan to add support for included WebVTT comments in the ogg format.

-   Wikipedia: {{< wp "WebVTT" >}}
-   [caniuse browser support for WebVTT ](http://caniuse.com/#feat=webvtt)
-   [jwplayer: browser support for various features of the WebVTT format
    ](http://www.jwplayer.com/html5/webvtt/)
-   VLC support WebVTT.

# playlists

A {{< wp "Playlist" >}} is a list of songs there are many popular playlist formats:

-   {{< wp "M3U" >}}, a simple text-based list of the locations of the items, with each
    item on a new line, consisting of either an absolute local pathname, a pathname
    relative to the the m3u file directory, or an URL.

    the file can contain comments, prefaced by the "#" character.

    _Extended M3U_ allow to include in comments line [extended M3U directives
    ](https://en.wikipedia.org/wiki/M3U#Extended_M3U).
-   {{< wp "PLS" >}}, a text playlist in .ini format It can store (cache)
    information on the song title and length (this is supported in
    extended M3U only).
-   {{< wp "XML_Shareable_Playlist_Format"  "XML Shareable Playlist Format" >}}
    (XSPF) is an XML-based playlist format for digital media created and
    supported by the the Xiph.Org Foundation at
    [xspf.org](https://xspf.org/). It is supported by
    {{< iref "media_players#mpd" "mpd" >}},
    {{< iref "media_players#amarok" "amarok" >}},
    {{< iref "streaming#ampache" "ampache" >}},
    {{< iref "media_players#audacious" "audacious" >}},
    {{< iref "media_players#bmpx" "bmpx" >}},
    {{< iref "media_players#totem" "totem" >}},
    {{< iref "media_players#vlc" "Vlc" >}},
    {{< iref "media_players#xmms2" "xmms2" >}} (via a plugin).

    In XSPF the file names are URIs, meaning that you could pass them to a web browser,
    it also support metadata like the name of the artist and title of the album.
-   [xhippo](https://www.gnu.org/software/xhippo/)
    is a simple GTK-based playlist manager


# Lyrics {#lyrics}

To synchronizes song lyrics with an audio file we use lyrics
-   Wikipedia: {{< wp "LRC_(file_format)" >}}
-   [List of applications/Lyrics - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Multimedia#Lyrics).

-   [lrc format](https://en.wikipedia.org/wiki/LRC_(file_format) "en.wikipedia.org LRC_(file_format)")
    is used for the lyric files.
-   [Lyrics3 v2.00 tag](https://www.id3.org/Lyrics3v2) which replaces the older
    [Lyrics3 tag](https://id3.org/Lyrics3)
    is a tag from [id3v2](https://www.id3.org/) which can store the lyrics.
-   [lyrics ID3](http://kde-apps.org/content/show.php?content=49274) (
    [lyrics ID3 README](http://www.gansinger.net/lyricsID3/README.fr.xhtml) )
    is composed of two scripts to retrieve and store lyrics to id3v2.  They are written
    in python using python-mutagen and aimed at amarok media player.
-   [lyric mode for emacs](https://www.emacswiki.org/emacs/LyricMode) is a major
    mode for editing lyric (.lrc) files.

Some media player have support for lyric display, like
    -   {{< iref "media_players#clementine" "Clementine" >}}.
    -   {{< iref "media_players#amarok" "Amarok" >}}.
    -   {{< iref "media_players#qmmp" "Qmmp" >}}.
    -   {{< iref "media_players#lollylop" "Lollylop" >}}.
    -   {{< iref "media_players#rythmbox" "Rhythmbox" >}} displays lyrics through
        plugins like the [official lyric plugin
        ](https://wiki.gnome.org/Apps/Rhythmbox/Plugins) or
        [lLyrics](https://github.com/dmo60/lLyrics).
    -   {{< iref "media_players#trawberry" "Strawberry" >}}.
-   {{< iref "media_players#mpd" "mpd" >}} has [several hacks
    ](https://web.archive.org/web/20160414023836/http://mpd.wikia.com/wiki/Hacks)
    _(archive of the page which has not be transferred to new fandom wiki.)_
    to display lyrics,

    Some mpd clients have support for lyrics:
    -   [ncmpcpp](http://unkart.ovh.org/ncmpcpp/),
    -   [py-lyrics](https://github.com/tremby/py-lyrics) (GPL-3.0)
        Python CLI script making use of [LyricWiki](lyrics.wikia.com) to pull lyrics
        from the web.
    -   {{< iref "media_players#mympd" "myMPD"a >}}.
-   [emms-lyrics](https://www.gnu.org/software/emms/manual/Lyrics.html)
    allows to display lyrics with
    {{< iref "media_players#emms" "Emms The Emacs Multimedia System" >}}.

-   [lrcShow-X](https://launchpad.net/lrcshow-x)
    is a python / pyqt4 application to add synchronized lyrics visualization
    functionality to the most used Linux media players, using existing LRC files,
    embedded lyrics like ID3 Sylt, Uslt, Lyrics3 and ApeTag. It also searches for lyrics
    using 12 different engines among which MiniLyrics, EvilLyrics, LrcDB and TTPlayer.

    It supports linux players using a dbus interface, like Amarok2, Qmmp, Audacious and
    many other.

    The last release is in 2012 but the  [Ubuntu PPA](https://launchpad.net/lrcshow-x)
    gives package for recent Ubuntu releases.
-   [GitHub - naaando/lyrics](https://github.com/naaando/lyrics) (GPL-3.0)
    Display lyrics on media players with MPRIS-2 interface. It is written in vala
    language.
-   [GitHub - muriloventuroso/givemelyrics
    ](https://github.com/muriloventuroso/givemelyrics) (GPL-3.0)
    Display lyrics _from any application_, but seems need MPRIS to synchronize lyrics.
    It is written in vala language.
-   [GitHub - osdlyrics/osdlyrics](https://github.com/osdlyrics/osdlyrics) (GPL-3.0)
    Standalone lyrics fetcher/displayer (windowed and OSD mode).
-   [GitHub - Jugran/lyrics-in-terminal](https://github.com/Jugran/lyrics-in-terminal)
    (MIT License)
    Python curses application to view lyrics in terminal of a song played in an MPRIS
    compatible player.
-   [GitHub - timxx/lyricsx](https://github.com/timxx/lyricsx) (MIT License)
    A C++/QT lyrics editor.

<!--  Local Variables: -->
<!--  ispell-local-dictionary: "english" -->
<!--  mode: markdown -->
<!--  End: -->
