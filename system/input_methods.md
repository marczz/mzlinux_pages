---
title: Input Methods
---

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
-   ArchWiki pages:
    -   [Xorg/Keyboard configuration - ArchWiki
        ](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration)
        for Xorg and Wayland. With a section on using setxkbmap.
    -   [X KeyBoard extension
        ](https://wiki.archlinux.org/index.php/X_KeyBoard_extension)
    -   [Xorg/Keyboard Configuration
        ](https://wiki.archlinux.org/index.php/Xorg/Keyboard_configuration)
        for Xorg and Wayland. With a section on using setxkbmap.
    -   [Extra Keyboard Keys (multimedia keys)
        ](https://wiki.archlinux.org/index.php/Extra_keyboard_keys),
    -   [Linux console/Keyboard configuration
        ](https://wiki.archlinux.org/index.php/Linux_console/Keyboard_configuration)
    -   [Xmodmap
        ](https://wiki.archlinux.org/index.php/Xmodmap)
    -   [Xbindkeys](https://wiki.archlinux.org/index.php/Xbindkeys)
    -   [Keyboard shortcuts](https://wiki.archlinux.org/index.php/Keyboard_shortcuts)

-   [MultimediaKeys - Ubuntu Help](https://help.ubuntu.com/community/MultimediaKeys)
-   [RMLVO keyboard configuration
    ](http://who-t.blogspot.com/2008/09/rmlvo-keyboard-configuration.html)
    (rules, models, layouts, variants and options)
-   [Creating custom keyboard layouts for X11 using XKB
    ](http://hektor.umcs.lublin.pl/~mikosmul/computing/articles/custom-keyboard-layouts-xkb.html)
-   [An Unreliable Guide to XKB Configuration
    ](http://www.charvolant.org/~doug/xkb/html/index.html) _2004_.
-   [XKB Layout Creation Notes
    ](http://www.x.org/wiki/XKBLayoutCreationNotes/)
-   [Extending the X keyboard map with xkb](http://madduck.net/docs/extending-xkb/)
    by Martin F. Krafft is probably the best advanced tutorial on xkb.

## Input configuration
_most entries target both console and Xorg_

-   [Debian Wiki - Keyboard](https://wiki.debian.org/Keyboard)
    explains input configuration for the whole Debian system (X and console).
-   [DebianWiki - Keyboard](https://wiki.debian.org/Keyboard)
-   [Debian XStrikeForce -  How to configure input
    ](https://xorg-team.pages.debian.net/xorg/howto/configure-input.html)
-   [Debian XStrikeForce -  InputHotplugGuide
    ](https://wiki.debian.org/XStrikeForce/InputHotplugGuide)
-   [Debian XstrikeForce old FAQ: How does the keyboard work in the X Window System?
    ](http://wiki.debian.org/XStrikeForce/FAQ#keyboard)
-   [How to configure input
    ](https://xorg-team.pages.debian.net/xorg/howto/configure-input.html)
    for an X server, keyboard, mouse,
-   [Keyboard input - ArchWiki
    ](https://wiki.archlinux.org/index.php/Keyboard_input)
-   [libinput documentation
    ](https://wayland.freedesktop.org/libinput/doc/latest/index.html)
    libinput is a library that provides a full input stack for display servers and other
    applications that need to handle input devices provided by the kernel.
-   [Peter Hutterer blog on libinput - Who-T](http://who-t.blogspot.com/)
-   [Xbindkeys](https://wiki.archlinux.org/index.php/Xbindkeys)
    is a program that allows to bind commands to certain keys or key combinations on the
    keyboard. Xbindkeys is independent of the window manager and desktop environment.
-   [GitHub - key-mapper](https://github.com/sezanzeb/key-mapper)
    A tool to change the mapping of your input device buttons.
    Supports mice, keyboards, gamepads, X11, Wayland, combined buttons and programmable
    macros.

    There is a Debian package in the
    [releases](https://github.com/sezanzeb/key-mapper/releases).

    -   [How to Remap Keyboard / Gamepad  Easily with key-mapper | UbuntuHandbook
        ](https://ubuntuhandbook.org/index.php/2021/07/remap-keyboard-gamepad-ubuntu/)

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


# Keyboard Layout {#keyboard_layout}
-   Wikipedia {{< wp "Keyboard layout" >}}, {{< wp "QWERTY" >}}, {{< wp "AZERTY" >}},
    {{< wp "Dvorak_Simplified_Keyboard"  "DVORAK" >}},
    {{< wp "Dvorak_Simplified_Keyboard#One-handed_versions"  "DVORAK One Handed" >}},
   {{< wp "Colemak" >}}.
    [Bépo](https://fr.wikipedia.org/wiki/B%C3%A9po)
-   Keyboard images: [QWERTY
    ](https://upload.wikimedia.org/wikipedia/commons/3/3a/Qwerty.svg),
    [AZERTY
    ](https://upload.wikimedia.org/wikipedia/commons/c/ca/Azerty_fr.svg),
    [DVORAK
    ](https://upload.wikimedia.org/wikipedia/commons/2/25/KB_United_States_Dvorak.svg),
    [Colemak](https://en.wikipedia.org/wiki/Colemak#/media/File:KB_US-Colemak.svg),
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

See above in the {{< iref "#tibetan_m17n" "ibus-m17n section" >}}
for ibus tibetan input methods.

-   [Tibetan and Himalayan Library (THL) - Tibetan Input System Principles
    ](http://www.thlib.org/tools/scripts/wiki/Tibetan%20Input%20System%20Principles.html)
-   [Rich Felker - Tibetan Keyboards / བོད་ཡིག་མཐེབ་གཞོང་སྐོར༎
    ](http://www.aerifal.cx/~dalias/bodyig/keyboards/)
-    [Tibetan Input Method for Linux - Digital Tibetan
    ](http://digitaltibetan.org/index.php/Tibetan_Input_Method_for_Linux).

### CNS Keyboard {#cns_keyboard}
Chinese National Standard of Tibetan Keyboard Layout named here CNS Keyboard was
designed by Tibet University at Lhasa. It is the base of the Tibetan keyboard on Windows

-   [CNS detailled description, and how to use it
    ](http://www.yalasoo.com/English/docs/yalasoo_en_MStbKb.html).
-   CNS Tibetan keyboard images, by level _the four image are ambedded in previous
    page_:
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
-   CNS Tibetan keyboard images on Wikipedia showing the 4 levels on a single image:
    -   [CNS Tibetan keyboard as supported by Windows Vista
        ](https://upload.wikimedia.org/wikipedia/commons/5/5a/Tibetan_Keyboard.png),
    -   [CNS Tibetan version 2
        ](https://upload.wikimedia.org/wikipedia/commons/5/5a/Tibetan_Keyboard.png)
-   In Xorg linux you can use the [XKB layout for CNS keyboard
    ](http://www.aerifal.cx/~dalias/bodyig/keyboards/bo_xkb.txt)
    by Rich Felker, which is included in Xorg with name `cn` or `cn(tib)`.
    You find it in `/usr/share/X11/xkb/symbols/cn`
-   In Linux console in an unicode able terminal you can use
    [LoadKey layout for CNS Keyboard
    ](http://www.aerifal.cx/~dalias/bodyig/keyboards/bo_linux.txt)
    by Rich Felker; but if you use the recent `console-setup` as explained in
    {{< iref "console#console_setup" "Console setup" >}} then =setupcon=  convert the
    xkb description to a `loadkey` keymap; which is loaded by =loadkey=. So you can use
    also your xkb rules in the console if the console or a console terminal has unicode
    support.

### Dzongkha Keyboard
-   Wikipedia: {{< wp "Dzongkha_keyboard_layout" >}} gives detailled description of
    Dzongkha keyboard, as images:
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
-   [XKB keyboard map for Dzongkha
    ](https://collab.its.virginia.edu/access/content/group/26a34146-33a6-48ce-001e-f16ce7908a6a/Tibetan%20Input%20Tools/Dzongkha%20Keyboard%20Resources/dzkeymap.html)
    can be used on Linux, it is included in xorg distribution.
    You find it in `/usr/share/X11/xkb/symbols/bt`

_In this keyboard U+0F0B (TSHEG) is located on the space bar at level 1 since it is the
most frequent character in Tibetan._

### Keyman Keyboards

-   [Keyman](https://keyman.com/) is available in Windoze, Mac OS, android, IOS, and
    [Linux](https://keyman.com/linux/)
-   [Keyman - THL page](http://www.thlib.org/tools/scripts/wiki/Keyman.html)
-   [keymanweb.com](https://keymanweb.com/) offer  javascript web
    keyboards [in tibetan
    ](https://keymanweb.com/#bod,Keyboard_tibetan_unicode_direct_input)
    ([help
    ](https://help.keyman.com/keyboard/tibetan_unicode_direct_input/1.0/tibetan_unicode_direct_input.php))
    or [in wylie
    ](https://keymanweb.com/#bod,Keyboard_tibetan_ewts_to_unicode)
    ([help
    ](https://help.keyman.com/keyboard/tibetan_unicode_ewts/1.0/tibetan_unicode_ewts.php))

Keyman support many keyboards including for Tibetan:
-   [Tibetan Unicode Direct Input Keyboard
    ](https://help.keyman.com/keyboard/tibetan_unicode_direct_input/1.1/tibetan_unicode_direct_input.php)
    _this keyboard is similar to the CNS keyboard in Windows but with some difference,
    you can see that the second letter in the second row is ཅ in the keyman keyboard
    while being ཆ in The CNS Keyboard, also the third and fourth levels of CNS are not
    implemented here._
-   [Tibetan Unicode EWTS Keyboard
    ](https://help.keyman.com/keyboard/tibetan_unicode_ewts/1.1/tibetan_unicode_ewts.php)
-   [Dzongkha (SIL)](https://help.keyman.com/keyboard/sil_dzongkha/1.1/sil_dzongkha.php).

These three keyboard seems to be the [Tibetan Keyman Keyboards from Peter Hauer
referenced in THL Page](http://www.thlib.org/tools/scripts/wiki/Keyman.html);
this page gives also downloads for the Sambhota Keyboard from Chris Walker.


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

# Virtual Keyboard
-   [Input Pad](https://github.com/fujiwarat/input-pad/wiki)
    is a tool to send characters to text applications by clicking
    various buttons. The command input-pad is a standalone application
    and ibus-input-pad provides input-pad on
    {{< iref "#ibus" "IBus input method" >}}.
-   [Florence](http://florence.sourceforge.net) is a virtual keyboard for Xorg.
    It was in Debian buster, and still packaged in sid in 2023; but no more in stable
    and testing.
    -   [Florence documentation](http://florence.sourceforge.net/english/),
    -   [How to Set Up a Virtual Keyboard in Linux - Make Tech Easier
        ](http://www.maketecheasier.com/setup-virtual-keyboard-linux/)
        (a Florence tutorial)
-   [matchbox-keyboard · GitLab](https://gitlab.com/matchbox-ui/matchbox-keyboard)
    an on-screen X11 virtual keyboard, designed for touch-screen devices running X.
    _matchbox-keyboard_ is packaged in Debian.
-   [Onboard](https://launchpad.net/onboard)
    An onscreen keyboard for X11 with macros, easy layout creation and word suggestion,
    useful for tablet PC users and for mobility impaired users. The last revision is
    from 2017.
    _onboard_ is packaged in debian.
-   [Phosh/squeekboard · GitLab](https://gitlab.gnome.org/World/Phosh/squeekboard)
    a keyboard-shaped input method supporting Wayland, built primarily for the Librem 5
    phone.
-   [wvkbd](https://git.sr.ht/~proycon/wvkbd) (GPL-3.0)
    On-screen virtual keyboard for wlroots.
-   [xvkbd](http://t-sato.in.coocan.jp/xvkbd)
    is a virtual (graphical) keyboard for X11. This program
    also has facility to send characters specified at the command line
    option to another client. _xvkb_ is in Debian.
    -   [Linux: xvkbd tutorial](http://xahlee.info/linux/linux_xvkbd_tutorial.html),
        by Xah Lee.
    -   [Sending Key Events](http://t-sato.in.coocan.jp/xvkbd/events.html)

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
