---
title: Color Themes
---

See also {{< iref "emacs#emacs_themes" "Emacs Themes" >}},
{{< iref "desktop" "Desktop" >}}.

 <!-- see also [[file:../../../../content-org/notes/system_notes/themes_notes.org::+hugo_front_matter_format: yaml][Themes Notes]] -->

# Color Themes
-   [arc-theme](https://github.com/jnsh/arc-theme)a (GPL-3.0)
:   A flat theme with transparent element, designed for GTK based desktop environments.
    -   [sachahjkl/wofi-arc-dark](https://github.com/sachahjkl/wofi-arc-dark)
        A stylesheet recreating the arc-dark theme for wofi.
-   <a name="base16"></a>[base16](https://github.com/chriskempson/base16)
    by Chris Kempson is the improvement of his own
    [tomorrow-theme](https://github.com/chriskempson/tomorrow-theme)
    it is very actively maintained It has color schemes for: _Xressources_, _i3_, _XFCE4
    Terminal_, _mate terminal_, _termite_, _gnome terminal_, _alacritty_, _shell_
    (_bash_, _zsh_), _vim_, _emacs_, _gimp_, _{{< iref "dbus#dunst" "dunst" >}}_,
    _zathura_, _rofi_, _st_, and _mac os_ apps.

    See also {{< iref "#tinted-theming" "Tinted Theming" >}} which is a community fork
    of Base16.
-   <a name="dracula"></a>[Dracula](https://draculatheme.com/) is a dark theme
    for a lot of apps (135!) including vim, zsh, emacs, gnome-terminal, alacritty,
    chrome, gitk, firefox, i3, rofi, termite, gtk, zathura, and many windows or OS X
    applications.
    -   [dracula/i3](https://github.com/dracula/i3)  Dark Dracula theme for i3.
    -   [dracula/wofi](https://github.com/dracula/wofi) (MIT License)
        Dark Dracula theme for wofi.
-   <a name="gruvbox"></a>[Gruvbox](https://github.com/morhetz/gruvbox-contrib)
    group ports on many application of the original
    [gruvbox vim theme](https://github.com/morhetz/gruvbox); a theme inspired by
    badwolf, jellybeans and solarized. It has a dark and light mode and covers many apps
    including xresources, shell, awesome wm, i3 wm, i3 status, conky,rofi,
    {{< iref "checkpointing#tmux_themes" "tmux" >}}  st, alacritty, emacs.
    -   [a-schaefers/i3-wm-gruvbox-theme
        ](https://github.com/a-schaefers/i3-wm-gruvbox-theme)
        An i3-wm gruvbox theme implementation.
-   [lighthaus](https://github.com/lighthaus-theme/lighthaus)
    A focused dark color lighthouse inspired color scheme.  It supports alacritty,
    {{< iref "dbus#Dunst" "Dunst" >}}, bottom system monitor, gnome-terminal, i3, iTerm,
    Kitty, Konsole, rofi, terminator, termite, termux, tilix, vim, vim-airline status
    bar, xfce-terminal, xresources, zathura, zsh.
    -   [lighthaus-theme/i3](https://github.com/lighthaus-theme/i3),
        A Lighthaus theme for i3.
-   <a name="nord-theme"></a>[nord](https://github.com/arcticicestudio/nord)
    is an arctic, north-bluish color palette. It provides four palettes,
    but it seems that all port are using a dark one, and the light one
    is [delayed to a far future
    ](https://github.com/arcticicestudio/nord/issues/46#issuecomment-661675957).
    -   [Nord Home](https://www.nordtheme.com)
    -   [nord vim](https://github.com/arcticicestudio/nord-vim)
    -   [nord tmux](https://github.com/arcticicestudio/nord-tmux)
    -   [nord emacs](https://github.com/arcticicestudio/nord-emacs)
    -   {{< iref "xterminals#st" "st" >}} color patch
        [nordtheme](https://st.suckless.org/patches/nordtheme/).
    -   [mtyn/polar](https://github.com/mtyn/polar)
        is a light colour scheme based on Nord.
-   [Solarized](http://ethanschoonover.com/solarized)
    is a sixteen color palette. The same palette is used for dark or light themes. There
    are ports to vim, Xresources, emacs,  mutt,
    {{< iref "checkpointing#tmux_themes" "tmux" >}}, GIMP Palette; and some Mac OS
    apps. It is also [ported to gnome-terminal
    ](https://github.com/Anthony25/gnome-terminal-colors-solarized).
-   [Smyck](https://github.com/hukl/Smyck-Color-Scheme),
    [Smyck Home](http://color.smyck.org/)
    is mainly aimed to OS X apps, it is no longer updated since 2017, but has many forks.
-   <a name="tinted-theming">[tinted-theming](https://github.com/tinted-theming/home)
    Style systems and tooling for crafting color schemes and using them in many apps.

    Tinted-Theming is a community fork of
    {{< iref "#base16" "Base16 from Chris Kempson" >}}.
    -   [Base16 Gallery](https://tinted-theming.github.io/base16-gallery/)
    -   [base16 styling guideline
        ](https://github.com/chriskempson/base16/blob/main/styling.md)
    -   Tinted Theming has many schemes templates for applications like
        [shell](https://github.com/tinted-theming/base16-shell),
        [rofi](https://github.com/tinted-theming/base16-rofi),
        [hexchat](https://github.com/tinted-theming/base16-hexchat),
        [polybar](https://github.com/tinted-theming/base16-polybar),
        [qutebrowser](https://github.com/tinted-theming/base16-qutebrowser),
        [foot](https://github.com/tinted-theming/base16-foot),
        [xresources](https://github.com/tinted-theming/base16-xresources),
        [fzf](https://github.com/tinted-theming/base16-fzf),
        [i3](https://github.com/tinted-theming/base16-i3),
        [tmux](https://github.com/tinted-theming/base16-tmux),
        [dunst](https://github.com/tinted-theming/base16-dunst),
        [emacs](https://github.com/tinted-theming/base16-emacs),
        [helix](https://github.com/tinted-theming/base16-helix),
        [vim](https://github.com/tinted-theming/base16-vim),
        kakoune,
    -   Tinted theming or Base16 have some builders like
        [base16-builder-go](https://github.com/tinted-theming/base16-builder-go),
        {{< iref "#flavours" flavour" >>}, {{< "#pywal16" "Pywal 16" >}}.

-   [Zenburn vim theme](https://github.com/jnurmine/Zenburn) (GPL)
    is original Zenburn theme.

    It has been ported to multiple applications.
    -    [zenburn-emacs](https://github.com/bbatsov/zenburn-emacs) (GPL-3.0)
         by Bozhidar Batsov a port of ZenBurn to emacs.
    -   [phha/zenburn.nvim](https://github.com/phha/zenburn.nvim) (MIT License)
        improves the original Zenburn for vim, by including support for TreeSitter and
        many other plugins.
    -    [anrxc](http://sysphere.org/~anrxc/) gives [in his blog
        ](http://sysphere.org/~anrxc/j/articles/zenburn/index.html)
        gives ZenBurn schemes for [awsome](http://awesome.naquadah.org/wiki/Zenburn_Theme),
        console, _Gajim_, _pidgin_, _emacs_, X apps thru _.Xdefaults _.
-   There are many web applications to help to configure color themes
    -   [256 colors - cheat sheet](https://jonasjacek.github.io/colors/),
    -   [4bit Terminal Color Scheme Designer](http://ciembor.github.io/4bit/)
        can export to Xresources, gnome terminal, and many other terminals.
    -   [colorschemedesigner](http://colorschemedesigner.com/csd-3.5/), Export to
        text, HTML+CSS, XML.
    -   [terminal sexy](http://terminal.sexy/) ,
        [terminal sexy GitHub repository](https://github.com/stayradiated/terminal.sexy)
        can export to many formats using the
        [termcolor library](https://github.com/stayradiated/termcolors) including
        Xresources, st, linux console, gnome ...
    -   [The 28 best tools for choosing a colour scheme (2014)
        ](http://www.creativebloq.com/colour/tools-colour-schemes-12121430).
-   For bash you can look at [ArchLinux: Color Bash Prompt
    ](https://wiki.archlinux.org/index.php/Color_Bash_Prompt)

## Theme switchers.
-   [base16-universal-manager](https://github.com/pinpox/base16-universal-manager)
    (MIT License). A manager to set base16 themes for any [supported application
    ](https://github.com/chriskempson/base16-templates-source/blob/master/list.yaml).
    -   [Configuration examples
        ](https://github.com/pinpox/base16-universal-manager/wiki/Configuration-examples)
-   [flavours](https://github.com/Misterio77/flavours)(MIT License).
    a base16 scheme manager written in rust. You can apply your theme to any application
    with a template, there is a [list of base16 predefined templates
    ](https://github.com/chriskempson/base16-templates-source/blob/master/list.yaml).

    It is inspired by *base16 universal manager*, with similar features; but is
    compatible with {{< iref "#tinted-theming" "Tinted Theming" >}}.
-   [pywal](https://github.com/dylanaraps/pywal) (MIT License).
    Pywal generates a color palette from the dominant colors in an image.
    It then applies the colors system-wide and on-the-fly in supported programs.
    It has also a library of 250 predefined themes.(

    Pywal supports a [wide range of programs and applications
    ](https://github.com/dylanaraps/pywal/wiki/Customization)
    -   [Pywal Wiki](https://github.com/dylanaraps/pywal/wiki)
    -   [Pywal cheatsheet](https://www.schotty.com/Cheatsheets/Pywal_cheatsheet/)
    -   [ewal](https://github.com/cyruseuros/ewal)(GPL-3.0)
        is a pywal based Emacs color-picker and theme generator.
-   [pywal16](https://github.com/eylles/pywal16) (MIT License).
    16 colors fork of pywal.
-   [wal-theme-picker](https://github.com/drybalka/wal-theme-picker) (MIT License).
    script to pick the best suited predefined themes for wal based on the colors
    in the image. *instead of generating a new theme*.
-   [wallust](https://codeberg.org/explosion-mental/wallust) (MIT License).
    A rust program which intends to be a better pywal.

### Theme switchers for i3
The previous programs manage *also* i3, but these seem to be only targeted to i3.

-   [Online i3wm Theme Maker](http://i3designer.aoeu.xyz/)
-   [Online Colorscheme Configurator for i3, i3status, dmenu
    ](https://thomashunter.name/i3-configurator/)

-   [j4-make-config](https://github.com/okraits/j4-make-config)
    is python a theme switcher and config generator for i3.
    It has a fork
    [D-Vaillant/j4-make-config](https://github.com/D-Vaillant/j4-make-config)
-   [i3-style](https://github.com/altdesktop/i3-style)
    a rust program which applies a theme to your i3 config file to change the
    colorscheme of the window decorations and the different parts of {{< iref "#i3bar" "i3bar" >}}.
-   [i3wm-themer](https://github.com/unix121/i3wm-themer)
    Theme collection manager for i3-wm.
-   [raven](https://git.sr.ht/~nicohman/raven) (GPL 3.0)
    A rust theme manager for linux, currently focusing on i3. Supports multiple different
    configuration files. *no commit between 2019 and 2023*
    -   [raven wiki](https://man.sr.ht/~nicohman/raven).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
