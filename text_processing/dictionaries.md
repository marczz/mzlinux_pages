---
title: Dictionary and Spell Checker Software
---

The {{< iref "français" "French and English Language Page" >}} has grammar and
dictonaries references related to these language.

See also Wikipedia {{< wp "Comparison of machine translation applications" >}}.

# Dict protocol software

-   The dict protocol is defined in the
    [RFC 2229](http://tools.ietf.org/html/rfc2229).
-   [links](http://www.dict.org/links.html) from
    [dict.org: The DICT Development Group](http://www.dict.org/)
-   [dictd - ArchWiki](https://wiki.archlinux.org/title/Dictd).
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

# Spell checkers
-   {{< wp "GNU Aspell" >}} is the standard GNU spell checker designed to replace Ispell
    adding utf-8 support.
-   Emacs as numerous [spelling modes](http://www.emacswiki.org/emacs/CategorySpelling)
    including [Wcheck Mode](http://www.emacswiki.org/emacs/WcheckMode)
    that can use most spelling software.
-   {{< wp " Hunspell" >}} (GPL) is the spell checker of LibreOffice,
    OpenOffice.org and Mozilla Firefox 3 & Thunderbird, Google
    Chrome. Hunspell is backward-compatible with MySpell dictionaries
    but can also use utf-8 encoded dictionaries.


    To use hunspell in emacs you can put in your startup file:

        (if (file-exists-p "/usr/bin/hunspell")
          (progn
             (setq ispell-program-name "hunspell")
             (eval-after-load "ispell"
                '(progn (setq  ispell-extra-args '("-a" "-i" "utf-8"))))))

    -   [hunspell Home](http://hunspell.sourceforge.net/)
    -   [Les dictionnaires Français sous Hunspell
        ](https://www.dicollecte.org/documentation.php?prj=fr).
-   [LibreOffice Dictionaries extensions
    ](http://extensions.libreoffice.org/extension-center?getCategories=Dictionary)
-   [OpenOffice spell checkers](http://www.openoffice.org/lingucomponent/)
    and hunspell [Dictionaries](http://wiki.openoffice.org/wiki/Dictionaries).
-   [verbiste]( http://sarrazip.com/dev/verbiste.html) (GPL)
    is a French conjugation system, it has an Emacs interface.

## Grammatical checkers
-   [Grammalecte](https://dicollecte.org/)(GPL)
    est un correcteur grammatical open source dédié à la
    langue française, pour Writer (LibreOffice, OpenOffice), Firefox,
    Thunderbird, {{< wp "Pluma_(editor)"  "Pluma" >}},VIM, Emacs and CLI.
    -   [linux.fr: Grammalecte, correcteur grammatical
        ](http://linuxfr.org/news/grammalecte-correcteur-grammatical)
        updated in [Grammalecte, correcteur grammatical II
        ](https://linuxfr.org/news/grammalecte-correcteur-grammatical-2).
        [Améliorer la correction orthographique et grammaticale sous Emacs
        ](http://linuxfr.org/users/jn/journaux/ameliorer-la-correction-orthographique-et-grammaticale-sous-emacs)
        is written before grammalecte was available.
    -   [flycheck-grammalecte](https://github.com/milouse/flycheck-grammalecte)
        is a wrappers for Grammalecte with emacs flycheck.
    -   [vim-Grammalecte](https://github.com/dpelle/vim-Grammalecte)
        A vim plugin for Grammalecte.
-   <a name="langagetool"></a>[LangageTool](https://languagetool.org/) (private license)
    LanguageTool offers spell and grammar checking. It is Free for 20,000 characters per
    check. A premium license cost 60€/year.

    It supports [numerous languages](https://languagetool.org/languages)
    like English, German, Italian, Portuguese, Esperanto, Breton, Japanese, Russian, and
    many other; see the [language table](https://languagetool.org/languages) for the
    level of support of each language.

    There are addons for Firefox, Chromium,
    LibreOffice, Google Docs, [Emacs](https://github.com/mhayashi1120/Emacs-langtool),
    [vim](http://www.vim.org/scripts/script.php?script_id=3223),
    [vim-grammarous](https://github.com/rhysd/vim-grammarous), Atom,
    [android](https://play.google.com/store/apps/details?id=org.softcatala.corrector)
    and [other software
    ](http://wiki.languagetool.org/software-that-supports-languagetool-as-a-plug-in-or-add-on).

# Other desktop dictionary software
-   [List of Dictionary and thesaurus applications - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Documents#Dictionary_and_thesaurus)

-   <a name="goldendict"></a>[GoldenDict](http://goldendict.org/) (GPL)
    is a dictionary reader in C/qt4/libwebkit4 with a very large support of formats (see
    [GoldenDict home page](http://goldendict.org/)).
    It supports multiple dictionary file formats: Babylon (.bgl) files with images and
    resources, {{< iref "#stardict" "StarDict" >}} (.ifo / .dict / .idx / .syn)
    dictionaries, Dictd (.index / .dict / .dz) dictionary files, ABBYY Lingvo (.dsl)
    source files, together with abbreviation files, ABBYY Lingvo (.lsa /.dat) audio
    archives. It can also look up in remote Wikipedia, Wiktionary, or any other
    MediaWiki-based sites.
    The android application is not covered by the GPL and is proprietary.
    A GoldenDict package is in Debian.
    -   [GitHub: GoldenDict](https://github.com/goldendict).
    -   [GoldenDict - ArchWiki](https://wiki.archlinux.org/title/GoldenDict)
    -   [gcl (goldendict command line)](https://github.com/dohliam/gdcl)
        is a ruby  command-line interface for searching GoldenDict
        dictionaries.
-   <a name="goldendict-ng"></a>[GoldenDict
    ](https://xiaoyifang.github.io/goldendict-ng/) (GPL)
    is a fork of {{< iref "#goldendict" "GoldenDict" >}}.
    It [supports many dictionary format
    ](https://xiaoyifang.github.io/goldendict-ng/dictformats/)

    local dictionaries:
    -   [MDict](https://www.mdict.cn/) (.mdx/.mdd)
    -   [StarDict](http://www.huzheng.org/stardict/) (.ifo/.dict./.idx/.syn)
    -   [DSL](https://lingvoboard.ru/store/html/DSLReference_HTML/index.html) (ABBYY Lingvo source files .dsl(.dz))
    -   [XDXF](https://github.com/soshial/xdxf_makedict) (.xdxf(.dz))
    -   [Zim](https://wiki.openzim.org/wiki/OpenZIM) (.zim)
    -   [Slob (Aard 2)](https://aarddict.org/) (.slob) and Aard (.aar)
    -   [DictD](https://en.wikipedia.org/wiki/DICT#Dict_file_format) (.index/.dict(.dz))
    -   [Epwing](https://ja.wikipedia.org/wiki/EPWING)
    -   [SDictionary](http://swaj.net/sdict/index.html) (.dct)
    -   [Babylon glossary builder](https://www.babylon-software.com/glossary-builder/) source files (.gls(.dz))
    -   Babylon dictionaries, complete support with images and resources (.BGL)
    -   ABBYY Lingvo sound archives (.lsa/.dat)
    -   Sound files in separate folders. File names are used as word
    -   Zipped sound pack. Sound files zipped, but with extension changed from .zip to (.zips)

    Network Sources:
    -   Wikipedia and Wiktionary
    -   [DICT](https://en.wikipedia.org/wiki/DICT) protocol
    -   LinguaLibre/Forvo pronunciations

    Compared to GoldenDict the GoldenDict-ng fork brings many enhancements: webengine
    with latest html/css feature support, >4GB dictionary, xapian as fulltext engine,
    Qt6, performance optimization,
    [anki integration](https://xiaoyifang.github.io/goldendict-ng/topic_anki/).

    A GoldenDict-ng package is in Debian.
-   [PtkDic and GTKDict](http://swaj.net/ptkdic/)<a name="ptkdic"></a>
    are Perl/GTK+ and GTK+/Tk  Dictionary that store dictionaries in a MySQL
    server.
    -   [PtkDic dictionary's SQL tables structure
        (http://dict.nsu.ru/help-ptkdic-format.htmlhttp://dict.nsu.ru/help-ptkdic-format.html).
    -   [phpMyLingvo](https://gitlab.com/sergeygalin/phpMyLingvo)
        is a Web-based dictionary/glossary application.
        It is afront-end to PtkDicdictionaries.
-   [pyglossary](https://github.com/ilius/pyglossary) (GPL-3.0)
    (GPL) is a python tool for creating and converting dictionary
    databases. It can use either PyGTK or TKinter for it's GUI.
    */Don't use the [Pyglossary SourceForge Site
        ](http://sourceforge.net/projects/pyglossary/) which not updated
        since 2011, but the [Pyglossary GiHub Repository
        ](https://github.com/ilius/pyglossary) which is up-to-date.*
-   [pystardict](https://github.com/lig/pystardict)
    is a Python library for manipulating StarDict dictionaries. _
    main code _2009_ last release _2010_.
-   [Sdictionary](http://swaj.net/sdict/index.html)
    is a Perl/TK dictionary project that uses own Sdict dictionary
    format.
-   <a name="stardict"></a> {{< wp "StarDict"  "Stardict _Wikipedia_" >}}
    developed by Hu Zheng (胡正) introduce a dictionary format that is much used, not
    only by the _Stardict_ application but by numerous applications on all OS.  Stardict
    has been removed from Sourceforge and is now found on its developper site.

    It is packaged in Debian with a GTK+ interface as well as
    _qstardict_ which use a QT4 interface; _stardict-plugin-spell_ is
    a spell plugin that give spelling suggestion when looking for a
    word in Stardict.
    For dictionaries in stardict format look at the
    {{< iref "#stardict-dicts" "following section" >}}
    -   [Stardict 3 - GitHub](https://github.com/huzheng001/stardict-3).
    -   [Stardict Wiki](https://code.google.com/p/stardict-3/wiki/index)
        is still on Google code.
    -   [stardict ubuntu french doc](http://doc.ubuntu-fr.org/stardict)
    -   [sdcv](https://github.com/Dushistov/sdcv) (GPL-2.0)
        is the console version of StarDict program.
    -   [Stardict File Format
        ](https://github.com/huzheng001/stardict-3/blob/master/dict/doc/StarDictFileFormat)
        The file format has changed between 2.4 and 3.0 and some older
        applications can only read the old format.
    -   [Convert lingvo .dsl dictionaries for use in StarDict
        ](https://code.google.com/p/stardict-3/wiki/ConvertLingvo)
    -   [Verify and Repair broken StarDict dictionaries
        ](https://code.google.com/p/stardict-3/wiki/RepairStarDictDicts).

# e-dicts {#edicts}

-   [English Wiktionary in StarDict format](http://www.dictinfo.com/)
-   [FreeDict - for free bilingual dictionaries](http://www.freedict.org/)
    contains many GPL licensed dictionaries. The databases are available in XMLand
    support the conversion to dictd format. They are available in debian with a name
    _dict-freedict-la1-la2_ where _la1_ and _la2_ are the three letters language codes from
    ISO 639-2.
-   {{< wp "XDXF" >}} is an universal XML-based format, convertible from and
    to other popular formats like
    {{< iref "#ptkdic" "PtkDic" >}},
    {{< iref "#stardict" "StarDict" >}}.
    -   [xdxf-makedict](https://github.com/soshial/xdxf_makedict)
        is for converting dictionary files many-to-many: dictd/dsl/sdict/stardict/xdxf →
        dictd/stardict/xdxf
    -   [Fora](http://ng-comp.com/fora/index.html) and
        [Alpus](https://alpusapp.com/)
        are two android/linux/windows/OSX/iOs dictionary software from *NG Computing*
        that understand XDXF and {{< iref "#stardict" "StarDict" >}}, DSL, and Dictd.
    -   [XDXF Format
        ](https://github.com/soshial/xdxf_makedict/tree/master/format_standard)
    -   [XDXF sourceforge site](https://sourceforge.net/projects/xdxf/files/)
        host XDXF coded dictionaries.

        The dictionaries are from year 2006 and
        there is no index of
        dictionaries, and you may prefer the next site.
    -   [XDXF dictionary downloads - dicto.org.ru](http://dicto.org.ru/xdxf.html)
        host all xdxf dictionaries, a lot of them from or to Russian.
-   [Babylon free dictionaries](http://www.babylon.com/free-dictionaries/),
    a large offer in `.bgl` format that is understood by numerous applications, or can
    be converted easily.

    Some dictionaries come with a `.exe` suffix it is a `7zip` compressed archive that
    contain the `.bgl` file.
-   {{< wp "Lingvo" >}} (private software) is a product of Russian software company ABBYY.
    It has a huge list of dictionnaries
    see [lingvo list of english monolingual dictionaries
    ](http://lingvodics.com/dics/view/English+Monolingual)
    -   The [lingoes site](http://www.lingoes.net/) has also a
        [dictionary download page](http://www.lingoes.net/en/dictionary/).
    -   Lingvo dictionnaries can be read by _GoldenDict_
        and [converted to StarDict
        ](http://code.google.com/p/stardict-3/wiki/ConvertLingvo),
        it is even possible to
        [add sound to .dsl dictionaries
        ](http://code.google.com/p/stardict-3/wiki/DslSound).
-   <a name="stardict-dicts"></a>Stardict Dicts:
    -   [Stardict dictionaries from Hu Zheng (胡正) Site](https://huzheng.sourceforge.io/)
        also available in [stardict-dic at SourceForge.net
        ](https://sourceforge.net/projects/huzheng/files/stardict-dic/)
    -   [Free StarDict dictionaries
        ](https://tuxor1337.frama.io/firedict/dictionaries.html)
        freely available dictionaries in StarDict format for offline use

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
    -   [GoldenDict. Logiciel et dictionnaires unilingues français
        ](https://archive.org/details/goldendict.logicieletdictionnairesunilinguesfrancais)
        Académie française de 1935, CD Universalis 3.0, Larousse Multidico,
        Le Grand Robert, Le Littré, Le petit Robert 2007,
        Le Trésor de la langue française
-   [ubuntu-fr Dictionnaires et encyclopédies
    ](https://doc.ubuntu-fr.org/dictionnaires_encyclopedies)
-   [XMLittre.dict directory listing](https://archive.org/download/XMLittre.dict)

For English, two big free dictionaries available in many formats
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

# Translation

-   [Translate Shell](https://www.soimort.org/translate-shell) (public domain)
    is a command-line translator powered by
    _[Google Translate](https://translate.google.com/)_,
    _[Bing Translator](https://www.bing.com/translator)_,
    _[Yandex.Translate](https://translate.yandex.com/)_, and
    _[Apertium](https://www.apertium.org/)_. It is in Debian.
    -  [Translate-shell - GitHub](https://github.com/soimort/translate-shell)
-   [Google Translate](http://translate.google.com/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
