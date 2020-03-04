---
title: Checkpointing
---

{{% toc /%}}

See also {{< iref "xorg#xpra" "Xpra" >}},
{{< iref "xorg#winswitch" "Winswitch" >}},
{{< iref "xterminals" "Terminal emulators" >}}, .

{{< wp "Application_checkpointing"  "Checkpointing" >}}
consists of storing a snapshot of the current application state,
and later on, uses it for restarting the execution in case of failure.

We also put under this header application to detach and reattach processes

{{< iref "xorg#xpra" "Xpra" >}} and
{{< iref "xorg#winswitch" "Winswitch" >}} also detach and reattach a
process, but from an Xorg session to another, they are put in the
{{< iref "xorg#winswitch" "Xorg section" >}}.

-   [Berkeley Lab Checkpoint/Restart (BLCR)
    ](http://crd.lbl.gov/departments/computer-science/CLaSS/research/BLCR/)
    (LGPL and GPL)
    can checkpoint both single- and multithreaded (pthreads) programs linked with
    the NPTL implementation of pthreads. It is  is implemented within kernel modules.
    It is in active development in 2013 (but nothing in 2014, 2015)
    and packaged in debian.
-   [CRIU](http://criu.org/) (GPL)
    is an userspace applications  to freeze a running application (or part of it)
    and checkpoint it to persistent storage. {{< wp "CRIU"  "Wikipedia: CRIU" >}} is in Debian
    and in active development in 2019. There are many HOW-TOs and uses cases rreferences
    in the [CRIU Home Page](http://criu.org/). It is in Debian.
-   [cryopid](http://sourceforge.net/projects/cryopid2/) (BSD license)
    allows you to capture the state of a running process in Linux and
    save it to a file that can then be used to resume the process
    later on after a reboot or even on another machine.  _Last release
    2009_.
-   <a name="dtach"></a>[dtach](https://github.com/crigler/dtach) (GPL)
    emulates the detach feature of screen. Dtach is in Debian. The
    [repository README](https://raw.githubusercontent.com/crigler/dtach/master/README)
    provides examples of use.
    -   [ArchWiki: Dtach](https://wiki.archlinux.org/index.php/Dtach)
-   <a name="abduco"></a>[abduco](http://www.brain-dump.org/projects/abduco/) (ISC Licence)
    is a fork of {{< iref "#dtach" "dtach" >}} with some
    [improvements](http://www.brain-dump.org/projects/abduco/#dtach)
    [Git Repository](https://github.com/martanne/abduco)
-   [DMTCP: Distributed MultiThreaded CheckPointing
    ](http://dmtcp.sourceforge.net/) (LGPL)
    checkpoint the state of multiple simultaneous applications,
    including multi-threaded and distributed applications.
    It operates directly on the user binary executable.
    _Active development in 2019_.
-   [reptyr](https://github.com/nelhage/reptyr) (BSD like license)
    is a recent utility for taking an existing running program and
    attaching it to a new terminal. It is in Debian.
    Active development in 2019.
-   [ITP: retty](http://pasky.or.cz/~pasky/dev/retty/) (GPL)
    by Petr Baudiš lets you attach processes running on other terminals]
    [retty git repo](http://repo.or.cz/w/retty.git) _developed in
    2006, last change 2012_ It is in Debian.

# Terminal multiplexors {#terminal_multiplexors}

-   [Gnu Screen documentation](http://aperiodic.net/screen/)
-   {{< iref "console#dvtm" "dvtm" >}} by itself does only console
    virtual terminal management, but it can be launched with
    {{< iref "#abucco" "abucco" >}} or
    {{< iref "#dtach" "dtach" >}} to provide session management.

## Tmux {#tmux}
[tmux](https://github.com/tmux/tmux) (BSD License)
is an alternative to screen. It uses a client-server model. Windows may be linked
simultaneously to multiple sessions and moved freely between sessions; and a client
may be switched between sessions.

-   [GitHub - tmux](https://github.com/tmux/tmux)
-   [tmux FAQ](https://github.com/tmux/tmux/wiki/FAQ)
-   [tmux crash course](https://robots.thoughtbot.com/a-tmux-crash-course)
-   [Quick and easy guide to tmux](http://www.hamvocke.com/blog/a-quick-and-easy-guide-to-tmux/)) and a few books
-   [The Tao of Tmux](https://leanpub.com/the-tao-of-tmux/read))
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
-   [tmux in practice
    ](https://medium.com/free-code-camp/tmux-in-practice-series-of-posts-ae34f16cfab0)
    a series of tutorials by Alexey Samoshkin. He also give his
    [tmux configuration](https://github.com/samoshkin/tmux-config).
-   [Tmuxinator](https://github.com/aziz/tmuxinator) (BSD like
    Licence)
    [Teamocil](https://github.com/remiprev/teamocil) (MIT license)
    are sessions managers for tmux written in ruby with YAML
    configuration.
    _tmuxinator is in Debian_.
-   [tmuxp](https://tmuxp.git-pull.com/en/latest/)
    is a _tmux_ session manager written in python with JSON or
    YAML configuration. It is _in Debian_.
    -   [ArchWiki: tmuxp](https://wiki.archlinux.org/index.php/Tmuxp).
-   <a name="powerline"></a>[Powerline (GitHub)](https://github.com/powerline/powerline)
    is a statusline plugin for vim, zsh, bash, _tmux_, IPython,
    Awesome and Qtile.
    [Powerline manual](https://powerline.readthedocs.org/en/latest/).
    -   Emacs has a powerline compatible package
        [telephone line](https://github.com/dbordak/telephone-line).

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

### Tmux addons
-   [Battery](https://github.com/Goles/Battery) by Nicolas Goles
    is a little bash script that uses
    [Spark](http://zachholman.com/spark/)
    to display the battery status on your tmux sessions or the terminal.
-   [RainBarf](https://github.com/creaktive/rainbarf) (GPL)
    by Stanislaw Pusep is a perl script that give a CPU/RAM/battery
    stats chart bar for tmux (and GNU screen)
-   [vim-tmux-navigator](https://github.com/christoomey/vim-tmux-navigator)
    allow seamless navigation between tmux panes and vim splits.

### Tmux and emacs
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
    tmux manipulation from Emacs inspired by tslime.vim and vimux. _in elpa_.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
