---
title: Input Methods
---

The keyboard input methods are in the
{{< iref "keyboard_input" "Keyboard Input Page" >}}.

See also
{{< iref "i18n" "Localisation (I18N)" >}}, {{< iref "xorg" "Xorg" >}}.

<!-- [[file:../../../../content-org/notes/system_notes/input_methods_notes.org][Input methods notes]] -->

# References
-   Wikipedia: {{< wp "Unicode input" >}}, {{< wp "Input Method" >}},
    {{< wp "List of input methods for Unix platforms" >}},
    {{< wp "Intelligent Input Bus" >}}, {{< wp "SCIM" >}}, {{< wp "Uim" >}},
    {{< wp "Help%3AMultilingual%5Fsupport%5F%28Indic%29#Linux"  "Linux Indic Languages support" >}},
-   [Linux Internationalization HOWTO](http://01101001.net/i18n.php)
    by David Oftedal deals with input methods.
-   [Debian Refernce: I18N and L10N
    ](http://www.debian.org/doc/manuals/debian-reference/ch08.en.html)
-   [Using UTF-8 in Debian](http://fruit.je/utf-8)
-   [Ubuntu iki: Language and Text
    ](https://wiki.ubuntu.com/LanguageAndText)
    gives details on how switch input methods.
-   <a name="iso-14655"></a> Without using extra input method the
    [ISO 14655 input method
    ](http://www.cl.cam.ac.uk/~mgk25/volatile/ISO-14755.pdf)
    you can use `CTRL+SHIFT u` then
    the hexadecimal code, then `SPACE`.Alternatively you hold
    `CTRL+SHIFT` while typing `U`+_hexadecimal sequence_, then release
    `CTRL+SHIFT`.
-   In emacs the previous method is still valid. In addition
    you can  type `C-x 8 RET` _Hexadecimal codepoint_
    or `C-x 8 RET` _Name_ or
-   In the Vim insert mode, type `Ctrl+V u` + _hexadecimal number_.

# m17n
[m17n library](http://www.nongnu.org/m17n/)
supports functions to handle multilingual texts, it is compatible
with ibus, SCIM and uim.

-   [m17n Library Documentation](http://www.nongnu.org/m17n/manual-en/index.html).
-   [How to create a new IME on Linux in about 15 minutes with SCIM and m17n
    ](http://www.freedesktop.org/wiki/Software/ScimSupportLanguageNewM17n/)
    _not scim specific_ from freedesktop pages.

The different input method are [described in the m17n database
](https://www.nongnu.org/m17n/manual-en/m17nDBData.html#mim-list).
Among them:<a name="tibetan_m17n"></a>

-   bo-tcrc: Tibetan input method using the  [TCRC keyboard layout
    ](http://tibetonline.tv/tibetan/tcrckbd.pdf).
-   bo-ewts Tibetan input method based on [EWTS version 2.0
    ](http://www.thlib.org/reference/transliteration/#!essay=/thl/ewts).
-   bo-wylie: Tibetan input method based on the {{< wp "Wylie" >}}
    transliteration.
-   fr-azerty: Simulating Azerty keyboard on English keyboard.
-   latn-post: Latin script with postfix modifiers.
-   latn-pre: Latin script with prefix modifiers.
-   rfc1345: [RFC1345](https://tools.ietf.org/html/rfc1345)
    mnemonics. You type `&`+_two characters code_.

    Exemple: `&!=` to obtain `≠`

-   unicode: Unicode BMP characters using hexadigits.
    with `CTRL-U` + __hexadecimal sequence_, you can rather use the
    above mentioned
    {{< iref "#iso" "ISO 14655 input method" >}}

# XIM
The X Input Method (XIM) was the original input method framework for the X Window
System. It predates IBus, SCIM, uim and IIIMF.

-   [XIM Specification
    ](http://www.x.org/releases/X11R7.6/doc/libX11/specs/XIM/xim.html).


# Ibus {#ibus}
-   [Ibus Home](https://github.com/ibus/ibus/wiki)
-   [ArchWiki: Ibus](https://wiki.archlinux.org/index.php/IBus)
-   [ArchWiki: Input Methods](https://wiki.archlinux.org/title/Input_method)
-   [Gentoo: Ibus](https://wiki.gentoo.org/wiki/IBus)
-   [EmacsWiki: IBus Mode](http://www.emacswiki.org/emacs/IBusMode)
-   [I18n/ibus - Debian Wiki](https://wiki.debian.org/I18n/ibus)
-   [Ibus Github Repository](https://github.com/ibus) has the
    source for _ibus_, _ibus-m17n_, _ibus-qt_, _ibus-xkb_, .....
-   [ibus-table](https://github.com/ibus/ibus/wiki/TableReadme)
    input methods.
    Most (but not all) methods are for chinese, vietnamese.
    -   Source package
        [Caius "kaio" repository](https://github.com/kaio/ibus-table).
        (other fork  [Mike Fabian repository
        ](https://github.com/mike-fabian/ibus-table/) )
    -   to create a new method:
        -   Ibus official [How To Create A Table For IBus Table
            ](https://github.com/ibus/ibus/wiki/HowToCreateATableForIBusTable).
        -   [How to Create a Custom Input Method Editor in Linux
            ](http://www.studymongolian.net/technical/how-to-create-linux-input-method-editor/)
            creates a table method for Mongolian IPA.
    -   An other multipurpose method is _table compose_ that input
        special letter by compose letter and diacritical mark.
    -   There is also Emoji and IPA-X-SAMPA.


To activate ibus, press control + Shift + space /it can be
configured/. You should now see a floating menu, where you can choose
between several input methods, you can use the same key combination
multiple times to cycle through available input methods, oe either
choose one with with left mouse click or using the left and right keys
.

 *Use system keyboard layout* remaps input methods to match (some)
non-US-English keyboard layouts.

{{< noteref "ibus_table_latex" "See also the memo ibus-table LaTeX" >}}

## using ibus for tibetan
There is a choice of input method for tibetan in ibus.

Among the [methods provided by m17n
](http://www.nongnu.org/m17n/manual-en/m17nDBData.html#mim-list) we find

-   `bo-ewts.mim`: Tibetan input method based on [EWTS version 2.0
    ](http://www.thlib.org/reference/transliteration/#!essay=/thl/ewts).
-   `bo-wylie.mim` Tibetan input method using the Wylie input method. It
    is a re-implementation of Emacs' tibetan-wylie input method, and is
    slightly different from Extended Wylie Transliteration Scheme
    (EWTS).
-   `bo-tcrc`: Tibetan input method using the
    [TCRC keyboard layout](http://tibetonline.tv/tibetan/tcrckbd.pdf).
    _It is not the same than {{< iref "#cns_keyboard" >}}.


# UIM
UIM _universal input method_ is an input method framework that uses
_bridges_ plugins to interract with applications.

UIM supports XIM the uim-xim bridge, GTK+ an Qt applications, console
input through _uim-fep_, Emacs with _uim.el_.
-   [WikiBook: UIM](http://en.wikibooks.org/wiki/Uim)
-   [Uim multilingual input method library - repository
    ](https://github.com/uim),
    [uim wiki pages](https://github.com/uim/uim/wiki)
    [uim official user document
    ](https://github.com/uim/uim/wiki/OfficialUserDocument).


# SCIM
-   [Smart Common Input Method platform SCIM](https://github.com/scim-im/scim) (LGPL)
    input method user interface for Unix. It has bindings to uim and m17n library
    and has support for covering more than 30 languages. It is an old project with only
    few maintenance commits.
    -   [Arch Linux SCIM](https://wiki.archlinux.org/index.php/SCIM)

# Other input method engines
-   [FriBidi](https://github.com/fribidi/fribidi) (LGPL)
    Implementation of the [Unicode Bidirectional Algorithm. (tr9 report)
    ](http://www.unicode.org/reports/tr9/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
