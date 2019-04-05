---
title: Dictionary and Spell Checker Software
---

{{% toc /%}}

The {{< iref "français" "French and English Language Page" >}} has grammar and dictonaries references
related to these language.

See also Wikipedia {{< wp "Comparison of machine translation applications" >}}.

## Dict protocol software

-   The dict protocol is defined in the
    [RFC 2229](http://tools.ietf.org/html/rfc2229).
-   [links](http://www.dict.org/links.html) from
    [dict.org: The DICT Development Group](http://www.dict.org/)
-   John Goerzen has written
    a [Dictclient](http://darcs.complete.org/dictclient) -- Python
    Client API for Dict protocol, and
    a [dictlib](http://darcs.complete.org/dictclib) -- a pure
    Python API for writing dictd databases.
-   [Emacs package for talking to a dictionary server](http://www.myrkr.in-berlin.de/dictionary/index.html)
-   [curl](http://curl.haxx.se/docs/manual.html) can be used as a _dictd_ client

        curl dict://dict.org/d:grow:web1913

    use `d` for define, `f` for find
-   Other Dict servers and clients are listed in the {{< wp "Dict"  "Wikipedia Dict Page" >}}
    and in the
    [_dict.org:_ wiki](http://www.dict.org/w/software/start).

## Spell checkers
-   {{< wp "GNU Aspell" >}} is the standard GNU spell checker designed to replace Ispell  adding
    utf-8 support.
-   Emacs as numerous [spelling modes](http://www.emacswiki.org/emacs/CategorySpelling)
    including [Wcheck Mode](http://www.emacswiki.org/emacs/WcheckMode)
    that can use most of spelling software.
-   [Grammalecte](https://dicollecte.org/)(GPL)
    est un correcteur grammatical open source dédié à la
    langue française, pour Writer (LibreOffice, OpenOffice), Firefox,
    Thunderbird, {{< wp "Pluma_(editor)"  "Pluma" >}},VIM, Emacs and CLI.
    -   [linux.fr: Grammalecte, correcteur grammatical
        ](http://linuxfr.org/news/grammalecte-correcteur-grammatical)
        updated in [Grammalecte, correcteur grammatical II
        ](https://linuxfr.org/news/grammalecte-correcteur-grammatical-2).
        [Améliorer la correction orthographique et grammaticale sous
        Emacs
        ](http://linuxfr.org/users/jn/journaux/ameliorer-la-correction-orthographique-et-grammaticale-sous-emacs)
        is written before grammalecte was available.
    -   [flycheck-grammalecte
        ](https://gitlab.com/geeklhem/flycheck-grammalecte) and
        <!-- also minor fork for nix packages
        https://github.com/apeyroux/flycheck-grammalecte -->
        [yet-an-other-flycheck-grammalecte-fork
        ](https://github.com/thomasluquet/yet-an-other-flycheck-grammalecte-fork)
        are wrappers for Grammalecte with emacs flycheck emacs.
    -   [vim-Grammalecte](https://github.com/dpelle/vim-Grammalecte)
        A vim plugin for Grammalecte.

-   {{< wp " Hunspell" >}} (GPL) is the spell checker of LibreOffice,
    OpenOffice.org and Mozilla Firefox 3 & Thunderbird, Google
    Chrome. Hunspell is backward-compatible with MySpell dictionaries
    but can also use utf-8 encoded dictionaries.<br />


    To use hunspell in emacs you can put in your startup file:

        (if (file-exists-p "/usr/bin/hunspell")
          (progn
             (setq ispell-program-name "hunspell")
             (eval-after-load "ispell"
                '(progn (setq  ispell-extra-args '("-a" "-i" "utf-8"))))))

    -     [hunspell Home](http://hunspell.sourceforge.net/)
    -   [Les dictionnaires Français sous Hunspell
        ](https://www.dicollecte.org/documentation.php?prj=fr).


-   [LibreOffice Dictionaries extensions
    ](http://extensions.libreoffice.org/extension-center?getCategories=Dictionary)
-   [OpenOffice spell checkers
    ](http://www.openoffice.org/lingucomponent/)
    and hunspell [Dictionaries
    ](http://wiki.openoffice.org/wiki/Dictionaries).
-   [verbiste]( http://sarrazip.com/dev/verbiste.html) (GPL)
    is a french conjugation system, it has an emacs interface.

## Other desktop dictionary software
-   [Babiloo](https://code.google.com/p/babiloo/) (GPL) written in python
    supports dictionaries in SDictionary, and
    {{< iref "#stardict" "StarDict" >}}.
    There are Debian and Ubuntu Packages.</br >
    Babiloo is now inactive and they recommend using
    {{< iref "#goldendict" "GoldenDict" >}}
-   [Fantasdic](http://projects.gnome.org/fantasdic/)
    is a gnome dictionary application writen in ruby/gtk it supports DICT
    dictionary server, edict or cedict, Google Translate, Dictd files,
    {{< iref "#stardict" "StarDict" >}} files,
    EPWING dictionaries (popular format in Japan).
-   [GoldenDict](http://goldendict.org/) (GPL)
    <a name="goldendict"></a>
    is a dictionary reader in C/qt4/libwebkit4 with a very large
    support of formats (see
    [GoldenDict home page](http://goldendict.org/)).  It supports
    multiple dictionary file formats: Babylon (.bgl) files with images
    and resources, {{< iref "#stardict" "StarDict" >}}
    (.ifo / .dict / .idx / .syn) dictionaries,
    Dictd (.index / .dict / .dz) dictionary files, ABBYY Lingvo (.dsl)
    source files, together with abbreviation files, ABBYY Lingvo (.lsa
    /.dat) audio archives. It can also look up in remote Wikipedia,
    Wiktionary, or any other MediaWiki-based sites.<br /> The android
    application is not covered by the GPL and is proprietary.
    A GoldenDict package is in Debian.
    -   [GitHub: GoldenDict](https://github.com/goldendict).
    -   [gcl (goldendict command line)
        ](https://github.com/dohliam/gdcl)
        is a ruby  command-line interface for searching GoldenDict
        dictionaries.
-   [lightlang](https://github.com/mdevaev/lightlang)
    (GPL) is a program in python with interface either in PyGTK or
    PyQT, with its custom dictionary format.
-   [MDict](http://mdic.gnufolks.org/)
    (GPL) is a QT4 dictionary software. It has its own dictionary
    format but the dictionary formats
    {{< iref "#stardict" "StarDict" >}} (.ifo) , Freedict
    (.tei) and Sdictionary (.dct) can be converted via MDicConv
    convertor or PyGlossary tool. MDic is no more developed since
    2010.
-   [Penelope  (GitHub)](https://github.com/pettarin/penelope)
    (MIT License)
     is a python tool for creating, editing and converting
     dictionaries, especially for eReader devices.
     -   Penelope can convert from/to: Bookeen Cybook Odyssey (R/W),
         CSV (R/W), EPUB (W only), MOBI (Kindle, W only),
         Kobo (R index only, W unencrypted/unobfuscated only),
         StarDict (R/W), XML (R/W)
     -   [Projects page of Alberto Pettarin
         ](http://www.albertopettarin.it/projects.htmlhttp://www.albertopettarin.it/projects.html)
         the developer of Penelope, and his
         [blog](http://www.albertopettarin.it/blog/)
-   [ppdict](https://github.com/luohao-brian/ppdict)
    is a dictionary written in Python, it was previously
    [on google code](https://code.google.com/p/ppdict/)
    _but there is no ppdict source code on google code_
    PPdict uses stardict data format and use of Webkit for text
    representation; and GTK as UI representation.</br> The project is
    inactive since 2011. Some python class interfacing with stardict
    can still be usefull, like
    [stardict.py](https://github.com/luohao-brian/ppdict/blob/master/stardict.py)
    and others.
-   [PtkDic and GTKDict](http://swaj.net/ptkdic/)<a name="ptkdic"></a>
    are Perl/GTK+ and GTK+/Tk  Dictionary that store dictionaries in a MySQL
    server.
    -   [PtkDic dictionary's SQL tables structure
        (http://dict.nsu.ru/help-ptkdic-format.htmlhttp://dict.nsu.ru/help-ptkdic-format.html).
    -   [phpMyLingvo](https://gitlab.com/sergeygalin/phpMyLingvo)
        is a Web-based dictionary/glossary application.
        It is afront-end to PtkDicdictionaries.
-   [pyglossary](https://github.com/ilius/pyglossary)
    (GPL) is a python tool for creating and converting dictionary
    databases. It can use either PyGTK or TKinter for it's GUI.
    The [Pyglossary SourceForge Site
    ](http://sourceforge.net/projects/pyglossary/) is not updated
    since 2011, the [Pyglossary GiHub Repository
    ](https://github.com/ilius/pyglossary) is up-to-date.
-   [pystardict](https://github.com/lig/pystardict)
    is a Python library for manipulating StarDict dictionaries. _
    main code _2009_ last release _2010_.
-   [Sdictionary](http://swaj.net/sdict/index.html)
    is a Perl/TK dictionary project that uses own Sdict dictionary
    format.
-   {{< wp "StarDict"  "Stardict _Wikipedia_" >}} <a name="stardict"></a>
    developed by Hu Zheng (胡正) introduce a dictionary format that is much used, not only by the _Stardict_
    application but by numerous applications on all OS.
    Stardict has been removed from sourceforge and is now found on its
    developper site.
    It is packaged in debian with a GTK+ interface as weel as
    _qstardict_ which use a QT4 interface; _stardict-plugin-spell_ is
    a spell plugin that give spelling suggestion when looking for a
    word in Stardict.
    For dictionaries in stardict format look at the {{< iref "#stardict" "following section" >}}
    -   [Stardict Home](http://www.huzheng.org/stardict/).
    -   [Stardict Wiki](https://code.google.com/p/stardict-3/wiki/index)
        is still on google code.
    -   [sdcv](http://sdcv.sourceforge.net/)
        is the console version of StarDict program.
    -   [Stardict File Format
        ](http://www.huzheng.org/stardict/StarDictFileFormat)
        The file format has changed between 2.4 and 3.0 and some older
        applications can only read the old format.
    -   [Note on Stardict Tools in Ubuntu
        ](http://thanhsiang.org/faqing/node/181) by Hu Zheng
        _2007_.
    -   [Convert lingvo .dsl dictionaries for use in StarDict
        ](https://code.google.com/p/stardict-3/wiki/ConvertLingvo)
    -   [Verify and Repair broken StarDict dictionaries
        ](https://code.google.com/p/stardict-3/wiki/RepairStarDictDicts).

## e-dicts

-   [English Wiktionary in StarDict format
    ](http://www.dictinfo.com/)
-   [FreeDict - for free bilingual dictionaries
    ](http://www.freedict.org/) contains may GPL licensed
    dictionaries. The databases are available in XMLand support the
    conversion ro dictd format. They are available in debian with a
    name _dict-freedict-la1-la2_ where  _la1_ and _la2_ are the 3-letter
    language codes from ISO 639-2.
-   {{< wp "XDXF" >}} is an  universal XML-based format, convertible from and
    to other popular formats like
    {{< iref "#ptkdic" "PtkDic" >}},
    {{< iref "#stardict" "StarDict" >}}.
    -   [xdxf-makedict](https://github.com/soshial/xdxf_makedict)
        is for converting dictionary files many-to-many:
        dictd/dsl/sdict/stardict/xdxf → dictd/stardict/xdxf
    -   [Fora](http://ng-comp.com/fora/index.html)
         an android/linux/windows/OSX/iOs dictionary understand XDXF
         (and {{< iref "#stardict" "StarDict" >}}, DSL, and Dictd)
    -   [XDXF Format](https://github.com/soshial/xdxf_makedict/blob/master/format_standard/xdxf_description.md
    -   [XDXF sourceforge site
        ](http://sourceforge.net/projects/xdxf/files/)
        host XDXF coded dictionaries, there is no index of
        dictionaries and you may prefer the next site.
    -   [XDXF dictionary downloads](http://dicto.org.ru/xdxf.html)
        host all xdxf dictionaries, a lot of them from or to russian.
-   [Babylon free dictionaries
    ](http://www.babylon.com/free-dictionaries/), a large offer
    in `.bgl` format that is understood by numerous applications,
    or can be converted easily. Some dictionaries come with a `.exe`
    suffix it is a `7zip` compressed archive that contain the `.bgl` file.
-   {{< wp "Lingvo" >}} (private software) is a product of Russian software company ABBYY.
    It has a huge list of dictionnaries
    see [lingvo list of english monolingual dictionaries
    ](http://lingvodics.com/dics/view/English+Monolingual)
    and the extensive list of
    [lingvo dictionary languages](http://translate.google.com/translate?sl=ru&tl=en&js=n&prev=_t&hl=en&ie=UTF-8&layout=2&eotf=1&u=http%3A%2F%2Flingvodics.com%2Fpages%2Flanguages%2F).
    -   The [lingoes site](http://www.lingoes.net/) has also a
        [dictionary download page](http://www.lingoes.net/en/dictionary/).
    -   Lingvo dictionnaries can be read by _GoldenDict_
        and [converted to StarDict
        ](http://code.google.com/p/stardict-3/wiki/ConvertLingvo),
        it is even possible to
        [add sound to .dsl dictionaries
        ](http://code.google.com/p/stardict-3/wiki/DslSound).
-   [Stardict dictionaries from Hu Zheng (胡正) Site
    ](http://abloz.com/huzheng/stardict-dic/)
    <a name="stardict-dicts"></a>
    -   Dictionaries converted to
        {{< iref "#stardict" "StarDict" >}} from
        [dictd](http://abloz.com/huzheng/stardict-dic/dict.org/),
        [freedict](http://abloz.com/huzheng/stardict-dic/freedict.de/),
        [mova](http://abloz.com/huzheng/stardict-dic/mova.org/).
    -   [Babylon: Stardict dictionaries
        ](http://abloz.com/huzheng/stardict-dic/babylon/)
        are in {{< iref "#stardict" "StarDict" >}} 3.0 format.
    -   [Babylon: Stardict English dictionaries
        ](http://abloz.com/huzheng/stardict-dic/babylon/english/)
    -   [Babylon: Stardict French dictionaries
        ](http://abloz.com/huzheng/stardict-dic/babylon/french/)
    -   [lingvo dictionaries
        ](http://abloz.com/huzheng/stardict-dic/lingvo/)

For english two big free dictionaries available in many formats
[including Kobo](http://www.mobileread.com/forums/showthread.php?t=196925)
and originally in project Gutenberg are:

-   Chamber's Twentieth Century Dictionary of the English Language,
    Rev. Thomas Davidson (1908), London.
    Over 33,000 definitions; it is particularly good for
    British English and historical fiction, as it contains archaic
    words that are not in the more modern English dictionary supplied
    with the Kobo. But don't go looking up "twitter" or "facebook"!
    [Entry of the first part 1/4 on project Gutenberg
    ](http://www.gutenberg.org/ebooks/37683).

-   Webster's Unabridged Dictionary, various, (1913), This
    dictionary has over 110,000 definitions (compared to the 80,000 or
    so in the Kobo dictionary), many of them with lengthy descriptions
    (generally longer than in the Chambers). It is primarily focused
    on American English spellings; it has British English spellings
    too, but the definitions simply refer to the American
    equivalent. For more information about this dictionary, including
    pronunciation and abbreviation guides. See here the
    [Project Gutenberg record of Webster's Unabridged Dictionary
    ](http://www.gutenberg.org/ebooks/29765) or
    [an alternate download](http://www.gutenberg.org/ebooks/667)
    of the same book but with  distincts files.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
