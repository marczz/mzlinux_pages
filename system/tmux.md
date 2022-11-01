---
title: Tmux
---
See also {{< iref "checkpointing" "Checkpointing" >}},

# Tmux References {#tmux_references}
[tmux](https://github.com/tmux/tmux) (BSD License)
is an alternative to screen. It uses a client-server model. Windows may be linked
simultaneously to multiple sessions and moved freely between sessions; and a client
may be switched between sessions.

-   [GitHub - tmux](https://github.com/tmux/tmux)
-   [tmux FAQ](https://github.com/tmux/tmux/wiki/FAQ)
-   [Tactical tmux: The 10 Most Important Commands
    ](https://danielmiessler.com/study/tmux/) by  Daniel Miessler.
-   [Quick and easy guide to tmux
    ](http://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)
    by Ham Vocke.
-   [The Tao of Tmux](https://leanpub.com/the-tao-of-tmux/read) a book
-   [Awesome tmux](https://github.com/rothgar/awesome-tmux)
    a list of helpful tmux links for various tutorials, plugins, and configuration
    settings.
-   [ArchWiki: Tmux](https://wiki.archlinux.org/index.php/Tmux)
    is a good introduction with references to complementary articles.
-   [Gentoo Wiki - Tmux](https://wiki.gentoo.org/wiki/Tmux).
-   [Tmux cheatsheet](https://gist.github.com/MohamedAlaa/2961058).
-   [Tmux Tutorial part I
    ](http://blog.hawkhost.com/2010/06/28/tmux-the-terminal-multiplexer/),
    [Part II
    ](http://blog.hawkhost.com/2010/07/02/tmux-%E2%80%93-the-terminal-multiplexer-part-2/)
-   [TMUX: My Getting Started Guide](http://howardism.org/Technical/Linux/tmux.html)
    by {{< iref "emacs#howardism" "Howard Abrams" >}}.
-   [tmux in practice
    ](https://medium.com/free-code-camp/tmux-in-practice-series-of-posts-ae34f16cfab0)
    a series of tutorials by Alexey Samoshkin. He also give his
    [tmux configuration](https://github.com/samoshkin/tmux-config).
-   <a name="powerline"></a>[Powerline (GitHub)](https://github.com/powerline/powerline)
    is a statusline plugin for vim, zsh, bash, _tmux_, IPython,
    Awesome and Qtile.
    -   [Powerline manual](https://powerline.readthedocs.org/en/latest/).
    -   Emacs has some powerline compatible packages
        [milkypostman/powerline](https://github.com/milkypostman/powerline)
        is the more cent fork of [many forks of vim powerline
        ](https://www.emacswiki.org/emacs/PowerLine).
        [telephone line](https://github.com/dbordak/telephone-line) was a new
        implementation.
-   [Byobu](http://byobu.co) is a wrapper script for launching either screen or tmux
    with an improved configuration.
    -   [GitHub - byobu](http://github.com/dustinkirkland/byobu)
    -   Dustin Kirkland the author of Byobu *and ecryptfs*
        gives a tutorial in his [presentation of byobu release 5
        ](http://blog.dustinkirkland.com/2011/12/byobu-5-released.html),
        in his [byobu blogs](http://blog.dustinkirkland.com/search/label/Byobu).
    -   Wikipedia: {{< wp "Byobu_(software)" "Byobu" >}}
    -   [byobu(1)
        ](http://manpages.debian.org/cgi-bin/man.cgi?query=byobu&format=html&locale=en).

# Tmux themes {#tmux_themes}
See also {{< iref "desktop#color_themes" Deskto color themes >}}

-   [awesome-tmux: Themes]https://github.com/rothgar/awesome-tmux#themes)
-   [Dr. Bunsen / The Text Triumvirate (archive)
    ](https://web.archive.org/web/20200414221857/https://www.drbunsen.org/the-text-triumvirate/)
-   [tmux themes - awesome-tmux
    ](https://github.com/rothgar/awesome-tmux#themes)
-   [tmux-gruvbox](https://github.com/egel/tmux-gruvbox)
    Gruvbox colorscheme for tmux.
-   [tmux-powerline-gruvbox-colorscheme
    ](https://github.com/PetrusZ/tmux-powerline-gruvbox-colorscheme)
    A gruvbox colorscheme for tmux powerline.
-   [Nord tmux](https://www.nordtheme.com/ports/tmux) for the
    {{< iref "desktop#nord-theme" "Nord theme" >}}.
-   <a name="tmux-solarized"></a>[seebi/tmux-colors-solarized
    ](https://github.com/seebi/tmux-colors-solarized)
    theme for tmux using Ethan Schoonover’s Solarized color scheme. It is compatible
    with tmux plugin manager.
-   [dracula/tmux](https://github.com/dracula/tmux)
     the official  {{< iref "desktop#dracula" "Dracula theme" >}} dark theme for tmux.
-   [tmux-tomorrow](https://github.com/edouard-lopez/tmux-tomorrow)
    5 flavors of Tomorrow theme _now {{< iref "desktop#base16" "base16" >}}_
    (i.e. dark/blue and light).
-   [jimeh/tmux-themepack](https://github.com/jimeh/tmux-themepack)
    A pack of various Tmux themes.
-   [odedlaz/tmux-onedark-theme](https://github.com/odedlaz/tmux-onedark-theme)
    dark tmux color scheme inspired by Atom's One Dark syntax theme.
-   [charlietag/tmux-themes](https://github.com/charlietag/tmux-themes)
    an plugin that applying the tmux themes maintened by the author.

# Tmux session managers

-   [Tmuxinator](https://github.com/aziz/tmuxinator) (BSD like Licence)
    [Teamocil](https://github.com/remiprev/teamocil) (MIT license)
    are sessions managers for tmux written in ruby with YAML
    configuration.
    _tmuxinator is in Debian_.
-   [tmuxp](https://github.com/tmux-python/tmuxp) (MIT License)
    is a _tmux_ session manager written in python with JSON or
    YAML configuration. It is _in Debian_.
    -   [tmuxp documentation](https://tmuxp.git-pull.com/)
    -   [ArchWiki: tmuxp](https://wiki.archlinux.org/index.php/Tmuxp).
-   [tmux-resurrect](https://github.com/tmux-plugins/tmux-resurrect) (MIT License)
    restore tmux environment after system restart. It is compatible
    with tmux plugin manager.

    It is a bash script that is an alternative to the ruby program _tmuxinator_.

    _tmux-resurrect_ can [save and restore tmux pane contents
    ](https://github.com/tmux-plugins/tmux-resurrect/blob/master/docs/restoring_pane_contents.md).
    It can also save vim/neovim session using
    [vim-obsession](https://github.com/tpope/vim-obsession).

    The list of [programs to be restored with the session
    ](https://github.com/tmux-plugins/tmux-resurrect/blob/master/docs/restoring_programs.md)
    can be configured to extend the minimal default program list.

    The default key bindings are `<prefix> + Ctrl-s` to save and
    `<prefix> + Ctrl-r` to restore the session.

    The last session is restored by default but the last 5 [older session can be restored
    ](https://github.com/tmux-plugins/tmux-resurrect/blob/master/docs/restoring_previously_saved_environment.md)
    or any session of the last 30 days.

# Tmux addons
-   [Tmux plugin  (TPM)](https://github.com/tmux-plugins/tpm) (MIT License)
    installs and loads tmux plugins.
    [Making a plugin tpm compatible
    ](https://github.com/tmux-plugins/tpm/blob/master/docs/how_to_create_plugin.md)
    is easy.
-   [tmux plugins repository](https://github.com/tmux-plugins)
-   [Battery](https://github.com/Goles/Battery) by Nicolas Goles
    is a little bash script that uses
    [Spark](http://zachholman.com/spark/)
    to display the battery status on your tmux sessions or the terminal.
-   [RainBarf](https://github.com/creaktive/rainbarf) (GPL)
    by Stanislaw Pusep is a perl script that give a CPU/RAM/battery
    stats chart bar for tmux (and GNU screen)
-   [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)
    allow seamless navigation between tmux panes and vim splits.

# Tmux and emacs
-   [EmacsWiki: tmux for collaborative editing
    ](https://www.emacswiki.org/emacs/tmux_for_collaborative_editing)
-   [EmacsWiki: Collaborative Editing
    ](https://www.emacswiki.org/emacs/CollaborativeEditing)
    [EmacsWiki: Rudel](https://www.emacswiki.org/emacs/Rudel)
    a collaborative editing environment for Emacs. Its purpose is to share buffers with
    other users in order to edit the contents of those buffers collaboratively.
-   [laishulu/emacs-tmux-pane](https://github.com/laishulu/emacs-tmux-pane)
    is a port of vim-tmux-navigator. It provide integration between emacs
    windows and tmux panes. _in elpa_
-   [syohex/emacs-emamux](https://github.com/syohex/emacs-emamux/)
    tmux manipulation from Emacs inspired by tslime.vim and vimux. _in elpa.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
