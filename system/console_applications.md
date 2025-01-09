---
title: Console Applications
---

Console applications are also called _terminal applications_

{{< noteref "command_line" "See also Unix command Line" >}}

------

# Refs
- see Wikipedia: {{< wp "Console application" >}},
{{< wp "Text-based user interface" >}},
{{< wp "Command-line interface" >}}.

See also {{< iref "file_managers#console" "console file managers" >}}
{{< iref "text_editors#terminal_editors" "terminal text editors" >}}

The internet messaging clients are in the pages {{< iref "irc" "IRC" >}},
{{< iref "xmpp" "XMPP" >}},  {{< iref "social_networks" "Social Network" >}}.


-   [Core utilities - ArchWiki](https://wiki.archlinux.org/title/Core_utilities)
    list also the alternative to core utilities
-   [incosolation blog](http://inconsolation.wordpress.com) is devoted
    to console applications, it stopped in 2015.
-   [cli.fan — Showcasing the best command-line tools](https://cli.fan/posts/).
-   [suckless.org software that sucks less](https://suckless.org/rocks/)
    many cli among these applications.
-   [Awesome CLI Apps](https://github.com/agarrharr/awesome-cli-apps).
-   [awesome-browserless](https://github.com/koalagang/awesome-browserless)
    _awesome_ list of alternatives to apps traditionally used in the web browser.
    _not only console_.
-   [Modern Rust Alternatives of Command-Line Tools
    ](https://zaiste.net/posts/shell-commands-rust/)

# Command line WEB search

-   [YubNub](http://yubnub.org/) allows to query numerous sites
    -   [Yubnub - Wikibooks](https://en.wikibooks.org/wiki/Yubnub).
-   [Goosh](http://goosh.org/) is a google command line in your
    browser.  Goosh is written in javascript and the package is
    available in [Google Code](http://code.google.com/p/goosh/) under
    GPL copyleft. _not updated since 2008_
-   [Surfraw](http://surfraw.alioth.debian.org/) (GPL) is a unix
    command line interface to WWW search engines. Surfraw is written in
    shell.
    -   [ArchWiki: Surfraw
        ](https://wiki.archlinux.org/index.php/Surfraw)
    -   [list of Surfraw search scripts (elvi)
        ](http://surfraw.alioth.debian.org/#elvilist)

# List of applications
See also {{< iref "shell#grep" "Grep and other tools" >}}


The applications below are not cross-referenced with their main entry
in this site, you can make a search to find the appropriate page.

[abook](http://abook.sourceforge.net/)
: text-based ncurses address book application


{{< wp "alpine" >}}
: A mail user agent.

[axel](http://axel.alioth.debian.org)
: light download accelerator - console version
  Axel tries to accelerate the downloading process by using multiple connections
  for one file.  It can also use multiple mirrors for one download.

[bc](http://www.gnu.org/software/bc)
: arbitrary precision calculator language

[byobu](http://launchpad.net/byobu)
:  a set of useful profiles and a profile-switcher for GNU screen

[calcurse](http://calcurse.org/)
: a calendar and scheduling application for the command line.

{{< wp "cmus" >}}
: audio player

{{< wp "elinks" >}}
: web browser.See {{< iref "browsers" "Browsers" >}}.

[exa](https://github.com/ogham/exa)
: is a replacement for ls written in Rust.

[fd](https://github.com/sharkdp/fd)
: installed as _fdfind_ fast and user-friendly alternative to find.

[hyperfine](https://github.com/sharkdp/hyperfine)
:   A command-line benchmarking tool
    -   [hyperfine - cli.fan](https://cli.fan/posts/hyperfine/)    .

[iftop]( http://www.ex-parrot.com/~pdw/iftop/)
: displays bandwidth usage information on an network interface

{{< wp "Irssi" >}}
: IRC client

[htop](http://htop.dev)
: ncurses-based process viewer.  It is similar to top, but allows to scroll the list
  vertically and horizontally to see all processes and their full command lines.  Tasks
  related to processes (killing, renicing) can be done with keyboards shortcuts.

  See the {<< man "htop" "manual page" >}} or the help menu (F1 or h inside htop) for a
  list of supported key commands.

[links2](http://atrey.karlin.mff.cuni.cz/~clock/twibright/links/)
: browser that can work in text mode, or graphic mode with X11, fb or
  framebuffer. See {{< iref "browsers" "Browsers" >}}.

{{< wp "MidMidnight Commander" >}}
: file manager

[p3blaster](http://manpages.debian.org/cgi-bin/man.cgi?query=mp3blaster%281%29)
: an interactive text-console based mp3 player. See
  {{< iref "media_players#mp3blaster" "Media Players" >}}.

{{< wp "Mutt" >}}
: e-mail client

{{< wp "nano" >}}
: text editor

[ncdu](http://dev.yorhel.nl/ncdu)
: ncurses disk analyzer

{{< wp "newsbeuter" >}}
: RSS reader

{{< wp "Ranger_(file_manager)"  "ranger" >}}
: file manager

[progress](https://github.com/Xfennec/progress)
:   reports the progress of file read/write operations for processes that have entries
    in `/proc`.
    -   [progress - cli.fan](https://cli.fan/posts/progress/).

[reddio](https://gitlab.com/aaronNG/reddio)
: a command-line interface for Reddit written in POSIX sh.

[ripgrep](https://github.com/BurntSushi/ripgrep)
: installed as _rggrep_, a line-oriented search tool that recursively searches the
  current directory for a regex pattern. An alternative to _ack_ and _ag_.
  Emacs has a _ripgrep_ interface with the package
  [deadgrep](https://github.com/Wilfred/deadgrep).


{{< iref "browsers#surfraw" "Surfraw" >}}
: fast unix command line interface to  WWW search engines.

[yank](https://github.com/mptre/yank) (MIT License)
:   Select a field from a command output, and copy it to the clipboard.
    _Yank_ is in Debian.

{{< wp "w3m" >}}
: web browser

# Framebuffer applications {#framebuffer_applications}
See also {{< iref "xterminals#framebuffer_terminals" "Framebuffers Terminals" >}}

{{< iref "xorg#directvnc" "directvnc" >}}
:   VNC client on a linux framebuffer.

[fbff](http://repo.or.cz/w/fbff.git)
: A small ffmpeg or libmpeg3 based framebuffer media player.
  [GitHub mirror](https://github.com/aligrudi/fbff).

[fbfv](https://github.com/smokku/fvb)
is a simple program to view pictures on a linux framebuffer device.


[fbgrab](https://fbgrab.monells.se/)
: Grabs an image of a framebuffer device and store it as a png file.
  -   [GitHub mirror](https://github.com/MikeMayer/FBGrab), see also the forks.

{{< iref "images#fbida" "fbi" >}}
: image viewer for framebuffer console.
  part of the [fbida](http://linux.bytesex.org/fbida/) suite

{{< iref "ps_pdf_djvu#fbpdf" "fbpdf" >}}
: A small framebuffer pdf viewer based on MuPdf.

[fbutils](https://github.com/richinfante/fbutils)
: a framebuffer png, jpg, svg image display program.

[fbv](https://github.com/godspeed1989/fbv)
: framebuffer image viewer with png, jpeg, bmp support.
   -   [kfarnsworth /fbv](https://github.com/kfarnsworth/fbv)
       this fork support gif through giflib.
   -   The original [fbv-1.0](http://s-tech.elsat.net.pl/fbv/) is used in archlinux
       package.

[fim](http://www.autistici.org/dezperado/)
: Fbi IMproved image viewer {{< iref "images" "see Images" >}}.

[hovacui](http://sgerwk.altervista.org/hovacui/hovacui.html)
: is a pdf viewer for X11 and the Linux framebuffer, Its main feature is its autozoom to
  text. It is part of [pdftorof](https://github.com/sgerwk/pdftoroff) pdf viewer,
  scaler, converter (to text, html, etc.) by blocks of text.

[jfbview](https://github.com/jichu4n/jfbview)
: a PDF and image viewer for the Linux framebuffer.  There are Debian packages.

{{< iref "browsers#links2" "links2" >}}
: browser that can work in text mode, or graphic mode with X11, fb or
  framebuffer.

{{< iref "arm_sbc" "OMXPlayer" >}}
: Command line player for rapberry pi, plays video on the framebuffer.

[ppmtofb](https://github.com/kurt-vd/ppmtofb)
: get/put a ppm from/to a linux framebuffer.

{{< wp "Mpv_(media_player)"  "Mpv" >}}
: A mediaplayer with framebuffer support on rapberry pi, with the options

        --vo=gpu --gpu-api=opengl --gpu-context=mali-fbdev



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
