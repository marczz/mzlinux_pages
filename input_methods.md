---
title: Input Methods
---

{{% toc /%}}

See also
{{< iref "i18n" "Localisation (I18N)" >}}

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
](http://www.nongnu.org/m17n/manual-en/m17nDBData.html#mim-list).
Among them:

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

# XKB {#xkb}

-   Wikipedia: {{< wp "X keyboard extension" >}}
-   [Xorg - X Keyboard Extension](http://www.x.org/wiki/XKB/)
-   [The XKB Configuration Guide
    ](http://www.x.org/releases/current/doc/xorg-docs/input/XKB-Config.html)
-   [How to further Enhance XKB Configuration
    ](http://www.x.org/releases/current/doc/xorg-docs/input/XKB-Enhancing.html)
-   The main reference site is Ivan Pascal [X Keyboard Extension
    ](http://pascal.tsu.ru/en/xkb/).
    -   [Some words about XKB internals
        ](http://pascal.tsu.ru/en/xkb/internals.html) by Yvan Pascal.
-   [Xorg - XKB protocol specification (pdf)
    ](http://www.x.org/releases/current/doc/kbproto/xkbproto.pdf)
-   [ArchWiki - X KeyBoard extension
    ](https://wiki.archlinux.org/index.php/X_KeyBoard_extension)
-   [ArchWiki: Keyboard Configuration in Xorg
    ](https://wiki.archlinux.org/index.php/Keyboard_Configuration_in_Xorg),
    -   [Extra Keyboard Keys (multimedia keys)
        ](https://wiki.archlinux.org/index.php/Extra_Keyboard_Keys),
    -   [Keyboard Configuration in Console
        ](https://wiki.archlinux.org/index.php/Keyboard_Configuration_in_Console)
-   [ArchWiki: Xmodmap
    ](https://wiki.archlinux.org/index.php/Xmodmap)
-   [RMLVO keyboard configuration
    ](http://who-t.blogspot.com/2008/09/rmlvo-keyboard-configuration.html)
    (rules, models, layouts, variants and options)
-   [Creating custom keyboard layouts for X11 using XKB
    ](http://hektor.umcs.lublin.pl/~mikosmul/computing/articles/custom-keyboard-layouts-xkb.html)
-   [An Unreliable Guide to XKB Configuration
    ](http://www.charvolant.org/~doug/xkb/html/index.html) _2004_.
-   [XKB Layout Creation Notes
    ](http://www.x.org/wiki/XKBLayoutCreationNotes/)
-   [Debian XStrikeForce -  How to configure input
    ](https://xorg-team.pages.debian.net/xorg/howto/configure-input.html)
-   [Debian XstrikeForce old FAQ: How does the keyboard work in the X Window System?
    ](http://wiki.debian.org/XStrikeForce/FAQ#keyboard)
-   [Extending the X keyboard map with xkb
    ](http://madduck.net/docs/extending-xkb/) by Martin F. Krafft is
    probably the best advanced tutorial on xkb.
-   For kdrive there is an old _2003_
    [kdrive with xkb Howto?
    ](http://lists.hellug.gr/pipermail/rule-list/2003/002759.html),
    and a [forum page showing examples of kdrive keyboard conf
    ](http://blog.gmane.org/gmane.comp.handhelds.openembedded/month=20080901/page=9)

## Input configuration
-   [Debian Wiki - Keayboard](https://wiki.debian.org/Keyboard)
    explains input configuration for the whole Debian system (X and console).
-   [How to configure input
    ](https://xorg-team.pages.debian.net/xorg/howto/configure-input.html)
    for an X server, keyboard, mouse,
-   [Keyboard input - ArchWiki
    ](https://wiki.archlinux.org/index.php/Keyboard_input#Identifying_keycodes_in_Xorg)
-   [Xorg/Keyboard configuration - ArchWiki
    ](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration)
    for Xorg and Wayland. With a section on using setxkbmap.

### Configuration notes
-   The setxkbmap {{< man "setxkbmap(1)" >}} command configures the keyboard to
    use the layout determined by the parameters

        setxkbmap [...](option)  [[variant [xkboption ...](layout) ] ]

-   The xkbcomp {{< man "xkbcomp(1)" >}} keymap compiler converts a description
    of an XKB keymap into a compiled keymap file or C header files or
    XKB source files.
-   xkbsel - select keyboard layout {{< man "xkbsel(1)" >}}

        xkbsel [-v] [--debug] [-s] MAP

-   xkbsel-aw {{< man "xkbsel-aw(1)" >}} is a simple GUI for selecting the
    keyboards and indicating the current selection.

## Compose key
-   [ArchWiki Keyboard configuration - Configuring compose key
    ](https://wiki.archlinux.org/index.php/Keyboard_configuration_in_Xorg#Configuring_compose_key).
-   [Ubuntu Help: Gtk Compose Table](https://help.ubuntu.com/community/GtkComposeTable)
    and [Compose Key](https://help.ubuntu.com/community/ComposeKey).

## Mouse control with keyboard
-   Ivan Pascal:
    [Xkb internal: accessX
    ](http://pascal.tsu.ru/en/xkb/internals.html#accessx) and
    [Xkb internal: Mouse Emulation
    ](http://pascal.tsu.ru/en/xkb/internals.html#mouse)
-   [Mapping the Mouse Buttons onto the Keyboard in XFree86
    ](http://www.geocities.jp/fred_b_maciel/kbd/kbd-e.html)



# XIM
The X Input Method (XIM) was the original input method framework for the X Window
System. It predates IBus, SCIM, uim and IIIMF.

-   [XIM Specification
    ](http://www.x.org/releases/X11R7.6/doc/libX11/specs/XIM/xim.html).


# Ibus {#ibus}
-   [Ibus Home](https://github.com/ibus/ibus/wiki)
-   [ArchWiki: Ibus](https://wiki.archlinux.org/index.php/IBus)
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
    -   See the page {{< iref "ibus_table_latex" "ibus-table LaTeX" >}}
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


# Other input method engines
-   [Smart Common Input Method platform project, SCIM
    ](http://sourceforge.net/projects/scim/)
    _older_ input method user interface for Unix
    -   [Arch Linux SCIM](https://wiki.archlinux.org/index.php/SCIM)
-   [FriBidi](http://fribidi.sf.net/) Free Implementation of the
    [Unicode Bidirectional Algorithm. (tr9 report)
    ](http://www.unicode.org/reports/tr9/)


# Keyboard Layout {#keyboard_layout}
-   Wikipedia {{< wp "Keyboard layout" >}}, {{< wp "QWERTY" >}}, {{< wp "AZERTY" >}},
    {{< wp "Dvorak_Simplified_Keyboard"  "DVORAK" >}},
    {{< wp "Dvorak_Simplified_Keyboard#One-handed_versions"  "DVORAK One Handed" >}}
-   Keyboard images: [QWERTY
    ](https://upload.wikimedia.org/wikipedia/commons/3/3a/Qwerty.svg),
    [AZERTY
    ](https://upload.wikimedia.org/wikipedia/commons/c/ca/Azerty_fr.svg),
    [DVORAK
    ](https://upload.wikimedia.org/wikipedia/commons/2/25/KB_United_States_Dvorak.svg),
    [Bépo
    ](https://upload.wikimedia.org/wikipedia/commons/0/05/KB_French_Dvorak_b%C3%A9po_simplifi%C3%A9.svg).
-   [Keyboard Layout Editor](http://www.keyboard-layout-editor.com/)
    is a  web application that enables the editing of
    keyboard-layouts, i.e., the position and appearance of each
    physical key.
    It is written in javascript and available
    [in GitHub](https://github.com/ijprest/keyboard-layout-editor).
-   [Simos Xenitellis: Keyboard Layout Editor
    ](https://github.com/simos/keyboardlayouteditor) is a python/gtk keyboard
    layout editor. _The code is mainly written in 2008._
-   [Ubuntu Forums - create your own keyboard layout tutorial
    ](http://ubuntuforums.org/showthread.php?t=188761&p=1092145#post1092145)

## One Handed Keyboard layout

-   [One-Handed Touch-Typing on a QWERTY Keyboard](http://edgarmatias.com/papers/hci96/)
-   [Mirrorboard: A one-handed keyboard layout for the lazy | xkcd
    ](http://blog.xkcd.com/2007/08/14/mirrorboard-a-one-handed-keyboard-layout-for-the-lazy/)
-   [How to Set Up a Virtual Keyboard in Linux - Make Tech Easier
    ](http://www.maketecheasier.com/setup-virtual-keyboard-linux/)

##  Tibetan keyboard layout {#tibetan_keyboard}
-   Wikipedia: {{< wp "Dzongkha_keyboard_layout" >}}.
    Images:
    -   [Dzongkha - regular
        ](https://upload.wikimedia.org/wikipedia/commons/c/c4/Dzongkha_Keyboard_layout_Main.svg),
    -   [Dzonkha shift
        ](https://upload.wikimedia.org/wikipedia/commons/9/91/Dzongkha_Keyboard_layout_Shift.svg),
    -   [Dzongkha Alt Gr
        ](https://upload.wikimedia.org/wikipedia/commons/7/78/Dzongkha_Keyboard_layout_AltGr.svg),
    -   [Dzongkha Shift Alt Gr
        ](https://upload.wikimedia.org/wikipedia/commons/7/7f/Dzongkha_Keyboard_layout_Shift_AltGr.svg).
    -   [All states in a pdf document
        ](http://www.dzongkha.gov.bt/IT/download/Dzongkha-Keyboard-2009.pdf).
-       [DzType 2 - Rigsum Institute of IT & Management
        ](http://www.rigsum-it.com/research/projects/dztype2) is a
        Dzongkha Typing Tutor,
        that we can use online or download.
-   CNS Tibetan keyboard images:
    -   [CNS Tibetan keyboard as supported by Windows Vista
        ](https://upload.wikimedia.org/wikipedia/commons/5/5a/Tibetan_Keyboard.png),
    -   [CNS Tibetan version 2
        ](https://upload.wikimedia.org/wikipedia/commons/5/5a/Tibetan_Keyboard.png)
    -   [How to Use CNS Keyboard
        ](http://www.yalasoo.com/English/docs/yalasoo_en_MStbKb.html)
    -   [regular keyboard
        ](http://www.yalasoo.com/images/MSTibKb/TibetanRegular.jpg),
    -   [m keyboard
        ](http://www.yalasoo.com/images/MSTibKb/Tibetan_m+.jpg),
    -   [shift keyboard
        ](http://www.yalasoo.com/images/MSTibKb/TibetanShift.jpg),
    -   [Alt Ctrl Shift keyboard
        ](http://www.yalasoo.com/images/MSTibKb/TibetanAltCtrlShift.jpg),
    -   [M keyboard
        ](http://www.yalasoo.com/images/MSTibKb/Tibetan_CapitalM+.jpg).
-   [keymanweb.com](https://keymanweb.com/) offer  javascript web
    keyboards [in tibetan
    ](https://keymanweb.com/#bod,Keyboard_tibetan_unicode_direct_input)
    ([help
    ](https://help.keyman.com/keyboard/tibetan_unicode_direct_input/1.0/tibetan_unicode_direct_input.php))
    or [in wylie
    ](https://keymanweb.com/#bod,Keyboard_tibetan_ewts_to_unicode)
    ([help
    ](https://help.keyman.com/keyboard/tibetan_unicode_ewts/1.0/tibetan_unicode_ewts.php))
    [Keyman](https://help.keyman.com/) has also keyboards for android,
    ipad, Mac OS, Windows
-   [a script to install tcrc xkb keyboard and fonts on linux
    ](https://github.com/scratch/Tibetan-keyboard)

# Virtual Keyboard
-   [xvkbd](http://homepage3.nifty.com/tsato/xvkbd/)
    is a virtual (graphical) keyboard program. This program
    also has facility to send characters specified as the command line
    option to another client.
-   [Sending Key Events
    ](http://homepage3.nifty.com/tsato/xvkbd/events.html)
    uses the API of the [XTEST extension
    ]http://www.x.org/releases/X11R7.7-RC1/doc/xextproto/xtest.html)
-   [Input Pad
    ](https://github.com/fujiwarat/input-pad/wiki)
    is a tool to send characters to text applications by clicking
    various buttons. The command input-pad is a standalone application
    and ibus-input-pad provides input-pad on
    {{< iref "#ibus" "IBus input method" >}}.
-   [Florence](http://florence.sourceforge.net) is a virtual
    keyboard,
    [Florence documentation](http://florence.sourceforge.net/english/),
    [How to Set Up a Virtual Keyboard in Linux - Make Tech Easier
    ](http://www.maketecheasier.com/setup-virtual-keyboard-linux/)
    (a Florence tutorial)

## Web keyboard
-   The [QWAZERTY online keyboard mapper](http://chezphil.org/qwazerty/)
    is an online application that converts the letters and symbols
    that you actually type into the ones in the same places on the
    keyboard that you are more used to.
-   [keymanweb.com](https://keymanweb.com/) offer a javascript web
    keyboard with hundreds of languages. You can add a bookmark in
    your browser or add the keyboard to your site.
    [Keyman](https://help.keyman.com/) has also keyboards for android,
    ipad, Mac OS, Windows.
    -   [Keyman Keyboard Layouts Help Index
        ](https://help.keyman.com/keyboard/).
    -   [Wikipedia help for Keyman Wikipedia plugin
        ](https://en.wikipedia.org/wiki/User:Keymanweb/Keymanweb)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
