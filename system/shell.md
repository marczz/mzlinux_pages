---
title: Shell
---

# Shell references
-   [Wikipedia: Unix shells](http://en.wikipedia.org/wiki/Unix_shell),
    [Comparison of computer shells
    ](http://en.wikipedia.org/wiki/Comparison_of_computer_shells),
    {{< wp "POSIX" >}}
-   [Shell Features](http://tldp.org/LDP/intro-linux/html/app3.html)
    in [Introduction to Linux](http://tldp.org/LDP/intro-linux/html/) _2008_
    gives rough common and differing features between shells
-   The shell faq:
    [UNIX shell differences and how to change your shell
    ](http://www.faqs.org/faqs/unix-faq/shell/shell-differences/).
-   [The Open Group Base Specifications - §2 Shell Command Language
    ](http://pubs.opengroup.org/onlinepubs/9699919799/utilities/V3_chap02.html)
-   [Linux Shell Scripting Tutorial v2.0
    ](https://bash.cyberciti.biz/guide/Main_Page)
-   The page
    [The Traditional Bourne Shell Family
    ](http://www.in-ulm.de/~mascheck/bourne/)
    is about all the variants of the original Bourne shell.
-   [comp.unix.shell FAQ
    ](http://www.faqs.org/faqs/by-newsgroup/comp/comp.unix.shell.html)
-   [Ubuntu: Command Line Learning Resources
    ](https://help.ubuntu.com/community/CommandLineResources)
-   Bruce Barnett [Grymoire: Sh - the Bourne Shell
    ](http://www.grymoire.com/Unix/Sh.html#uh-14)


# Shell scripting libraries {#shell_libraries}
-   [Heiner's SHELLdorado](http://www.shelldorado.com/)
    see also the extensive
    [link page](http://www.shelldorado.com/links/index.html)
-   [shunit](http://shunit.sourceforge.net/)
    is the first unit testing framework for Bourne derived shells.
-   [shunit2](https://github.com/kward/shunit2)
    is an improved xUnit based unit testing for Unix shell scripts.
-   [log4sh](https://sites.google.com/a/forestent.com/projects/log4sh) (LGPL)
    is a logging framework for shell scripts
-   John Dubois who maintains [armory.com](http://www.armory.com/)
    has made available a huge number of
    [Ksh and awk scripts](http://www.armory.com/~ftp/) _2011_.
-   Pádraig Brady has many command line references, in his
    [PixelBeat Site](http://www.pixelbeat.org) and scripts in
    [his GitHub repository](https://github.com/pixelb) (LGPL).
-   A [list of bash shell-scripting libraries
    ](http://dberkholz.com/2011/04/07/bash-shell-scripting-libraries/)
    _2011_.
-   Nathaniel Landau [Boilerplate Shell Script Template
    ](https://natelandau.com/boilerplate-shell-script-template/)
    is a template for writing shell scripts.
-   [pluginhook](https://github.com/progrium/pluginhook) (MIT)
    A plugin system for Bash. In Debian.
-   [bash-modules](https://github.com/vlisivka/bash-modules)
    A module system for bash which provide a set of bash subroutines,
-   [Argbash](https://argbash.readthedocs.io/en/latest/index.html)
    is a bash code generator that can assist you in writing scripts that accept
    arguments.
    -   [argbash · GitHub](https://github.com/matejak/argbash)
    -   [Argbash alternatives
        ](https://argbash.readthedocs.io/en/latest/others.html)
-   {{< iref "python_libraries#docopt" "Docopt" >}}
    is a python utilities, that is also suited to parsing bash command line arguments.

# Ash

Ash is a light shell written in 1989 by Kenneth Almquist as
replacement to the "System V Release 4" Bourne shell.

Main differences with SysV4 shell:

-   implements "$(...)" command substitution
-   accepts "export VAR=value"
-   no command line editing and history (by intention)
-   parameter expansion doesn't know # and %
-   read doesn't know "-r"
-   no arithmetic expansion
-   traditional behaviour about
    [IFS vs. "$\*"](http://www.in-ulm.de/%7Emascheck/various/ifs/)

The more common flavour of ash are the
[netbsd ash](http://cvsweb.netbsd.org/bsdweb.cgi/src/bin/sh),
{{< man "dash" >}} used as **sh** in debian and ubuntu, the new **yash**
and the Busybox **ash**.

The [dash git repository
](http://git.kernel.org/cgit/utils/dash/dash.git)
gives the source and a [changelog
](http://git.kernel.org/cgit/utils/dash/dash.git)

The details of the [Ash (Almquist Shell) Variants
](http://www.in-ulm.de/~mascheck/various/ash/) is given in this page.


[Bashism - How to make bash scripts work in dash
](http://mywiki.wooledge.org/Bashism)
list some of the most common bashisms, i.e. features not defined by
POSIX and how to translate them to POSIX shells.

It is also detailled in [Ubuntu - Dash as /bin/sh
](https://wiki.ubuntu.com/DashAsBinSh).

[checkbashism.pl
](https://anonscm.debian.org/cgit/collab-maint/devscripts.git/plain/scripts/checkbashisms.pl)
is a script in debian devscripts, which comes with a manual
{{< man "checkbashisms(1)" >}} to check what in a script is not posix. It is
used to convert your bash script to dash.
There is a [slightly modified release in Sourceforge
](https://sourceforge.net/projects/checkbaskisms).

To work with portable posix shell you can also use
[Autoconf manual - Portable Shell Programming
](http://www.gnu.org/savannah-checkouts/gnu/autoconf/manual/autoconf-2.69/html_node/Portable-Shell.html)
and
[Rich’s sh (POSIX shell) tricks
](http://www.etalabs.net/sh_tricks.html).

[Yash](https://yash.osdn.jp/) (GPL)
has a special status among the ash family. It is conceived to be the
most POSIX-compliant shell, Yash fully supports POSIX.1-2008 (IEEE Std
1003.1, 2013 Edition). Yash features exceed those of dash and busybox
ash; and in contrast to dash it can be used as an interactive shell.

It features global aliases, arrays, socket redirection, pipeline
redirection, and process redirection, brace expansion, extended
globbing, fractional numbers in arithmetic expansion, prompt command
and command-not-found handler, command line completion.

Yash is available in Debian, Ubuntu, Fedora.

The manual is also [available online
](https://yash.osdn.jp/doc/)

All these shell are tiny on an amd64 dash is 1.6M resident / 1.4M
shared; yash 1.1M/1.0M; busybox 2.3M/2.1M.

Busybox seems a lot bigger but it includes all coreutils, awk, sed
.... in the same executable.

Bash (without my big init) is 3.8M/3.2M; zsh (without user init)
4.4M/3.6M.


# Bash

-   [Chet Ramey](http://cnswww.cns.cwru.edu/~chet):
    [Bash page](http://cnswww.cns.cwru.edu/~chet/bash/bashtop.html)
-   [Bash Reference Manual
    ](http://cnswww.cns.cwru.edu/~chet/bash/bashref.html)
-   [BASH(1) Manual Page
    ](http://cnswww.cns.cwru.edu/~chet/bash/bash.html)
-   [Chet Ramey official Bash FAQ
    ](http://tiswww.case.edu/php/chet/bash/FAQ)
-   [Greg's Wiki Bash FAQ
    ](http://mywiki.wooledge.org/BashFAQ)
    _other material from Greg's Wiki are {{< iref "#gregs_wiki" "below" >}}
-   [Bash Reference Sheet
    ](http://mywiki.wooledge.org/BashSheet)
-   [Bash Hackers Wiki](http://bash-hackers.org/wiki/doku.php/)
    hold documentations about the GNU Bash.
-   [Bash Guide for Beginners
    ](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
    _2008_.
-   [Bash Programming Introduction
    ](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
    _for this elementary guide being old (2000) is not challenging_.
-   [Advanced Bash Scripting Guide
    ](http://tldp.org/LDP/abs/html/index.html)
-   [Bash Hackers Wiki](http://wiki.bash-hackers.org/doku.php)
    hold documentations  about the GNU Bash. The first page is an
    index of pages on commands, builtins, and expressions of bash.
-   [Greg Wooledge's Wiki, in short Greg's Wiki
    ](http://mywiki.wooledge.org/) contains bash resources:
    -   [Bash Guide](http://mywiki.wooledge.org/BashGuide)
        more than a Tutorial, a guide to nearly all bash constructs.
    -   [Bash Reference Sheet](http://mywiki.wooledge.org/BashSheet)
        a shorter manual page.
    -   [BASH Frequently Asked Questions
        ](http://mywiki.wooledge.org/BashFAQ)
    -   [Bash Pitfalls](http://mywiki.wooledge.org/BashPitfalls)
        a long list of common bash errors and how to mend them.
    -   [Bash Weaknesses](http://mywiki.wooledge.org/BashWeaknesses)
        or _don't use bash for large programs, they would be unreliable_.
    -   The [Shell category](http://mywiki.wooledge.org/CategoryShell)
        includes many interesting pages.
-   [Bash by example, Part 1
    ](http://www.ibm.com/developerworks/linux/library/l-bash/index.html),
    [Part 2
    ](http://www.ibm.com/developerworks/linux/library/l-bash2/index.html),
    [Part 3](http://www.ibm.com/developerworks/library/l-bash3/index.html)
    by Daniel Robbins. From the same author:
    [Tip: Prompt magic
    ](http://www.ibm.com/developerworks/linux/library/l-tip-prompt/index.html?dwzone=linux)
    Show how to customize the BASH prompt, and set the xterm title.
-   [Commandline Fu](http://www.commandlinefu.com/)
    is a repository for  sharing shell commands. The
    [FAQ](http://www.commandlinefu.com/site/faq)
    gives other accesses to it like RSS feeds.
-   [bashdb](http://bashdb.sourceforge.net/)
    is a source code debugger for bash.
-   [Bashdoc
    ](https://github.com/ajdiaz/bashdoc)
    is a bash documentation processor similar to javadoc
    but use reStructuredText to provide the final document.

To proofread a bash script It is often very useful to remember how,
and in what order expansion is done. It is given in section
[3.7.1 Simple Command Expansion
](http://www.gnu.org/software/bash/manual/bashref.html#Simple-Command-Expansion)
of
[bash reference manual](http://www.gnu.org/software/bash/manual/bashref.html):

-   [3.5.1 Brace Expansion
    ](http://www.gnu.org/software/bash/manual/bashref.html#Brace-Expansion)
    Expansion of expressions within braces.
-   [3.5.2 Tilde Expansion
    ](http://www.gnu.org/software/bash/manual/bashref.html#Tilde-Expansion)
    Expansion of the \~ character.
-   [3.5.3 Shell Parameter Expansion
    ](http://www.gnu.org/software/bash/manual/bashref.html#Shell-Parameter-Expansion)
    How Bash expands variables to their values.
-   [3.5.4 Command Substitution
    ](http://www.gnu.org/software/bash/manual/bashref.html#Command-Substitution)
    Using the output of a command as an argument.
-   [3.5.5 Arithmetic Expansion](http://www.gnu.org/software/bash/manual/bashref.html#Arithmetic-Expansion)How
    to use arithmetic in shell expansions.
-   [3.5.6 Process Substitution
    ](http://www.gnu.org/software/bash/manual/bashref.html#Process-Substitution)
    A way to write and read to and from a command.
-   [3.5.7 Word Splitting](http://www.gnu.org/software/bash/manual/bashref.html#Word-Splitting)How
    the results of expansion are split into separate arguments.
-   [3.5.8 Filename Expansion](http://www.gnu.org/software/bash/manual/bashref.html#Filename-Expansion)A
    shorthand for specifying filenames matching patterns.
-   [3.5.9 Quote Removal
    ](http://www.gnu.org/software/bash/manual/bashref.html#Quote-Removal)
    How and when quote characters are removed from words.

Note that variable, and arithmetic expansion and command and
process substitution are done in the same pass from left to right.

A (double) quoted string and **a quoted command substitution** is
not subject to word splitting and pathname expansion

After an assignment only a subset of these expansions hold, namely:
tilde expansion, parameter expansion, command substitution,
arithmetic expansion, and quote removal. (no pathname and brace
expansion, nor process substitution)

# Zsh {#zsh}

-   Wikipedia {{< wp "Z shell" >}}
-   [Zsh Home at sourceforge](http://zsh.sourceforge.net/)
-   [Zsh Manual
    ](http://zsh.sourceforge.net/Doc/Release/index-frame.html), or
    without frames:
    [Zsh Manual](http://zsh.sourceforge.net/Doc/Release/zsh_toc.html).
-   [A User's Guide to the Z-Shell
    ](http://zsh.sourceforge.net/Guide/zshguide.html)
    by Peter Stephenson _2003_.
-   [Z-Shell Frequently-Asked Questions](http://zsh.sourceforge.net/FAQ/)
    with
    [differences between zsh and sh, ksh, csh, tcsh, bash.
    ](http://zsh.sourceforge.net/FAQ/zshfaq02.html).
-   [ArchWiki: Zsh](https://wiki.archlinux.org/index.php/Zsh)
    a tutorial and numerous references and links.
-   [Grml](http://grml.org/) use [zsh](http://grml.org/zsh/)
    They provide a complex zshrc which has a
    [grml: zshrc manpage](http://grml.org/zsh/grmlzshrc.html)
    and a page of zsh turorials and tips
    [zsh-lovers](http://grml.org/zsh/zsh-lovers.html).
-   [Zsh Wiki](http://zshwiki.org/home/)
-   [Zsh Wiki: Switching from Bash
    ](http://zshwiki.org/home/convert/bash).
-   [linux Magazine: Making the Transition to zsh
    ](http://www.linux-mag.com/id/1053/)
-   [Bash to Zsh refcard (pdf)
    ](http://www.bash2zsh.com/zsh_refcard/refcard.pdf)
-   [zplugin](https://github.com/zdharma/zplugin) (MIT License)
    A flexible Zsh plugin manager.

# Awk {#awk}

-   Wikipedia {{< wp "Akw" >}}
-   [Gawk: Effective AWK Programming
    ](http://www.gnu.org/software/gawk/manual/)
    (FDL) an online book by Arnold Robbins available in pdf and html.
    The [Regexp Chapter
    ](http://www.gnu.org/software/gawk/manual/html_node/Regexp.html)
    is a good reference on gnu Regexps.
-   [Awk Faq](http://www.faqs.org/faqs/computer-lang/awk/faq/)
-   [Getting started with awk
    ](http://www.cs.hmc.edu/tech_docs/qref/awk.html)
-   [Steve's Awk Acadamy
    ](http://www.troubleshooters.com/codecorn/awk/index.htm)
    by Steve Litt is an awk tutorial.
-   Bruce Barnett [Grymoire: Awk
    ](http://www.grymoire.com/Unix/Awk.html).
-   [awk cheat sheet (.pdf)
    ](http://www.catonmat.net/download/awk.cheat.sheet.pdf) and
    [awk cheat sheet (.txt)
    ](http://www.catonmat.net/download/awk.cheat.sheet.txt) by
    [Peteris Krumins](http: www.catonmat.net).
-   [Awk.Info](http://awk.info/) is the Portal of Awk community.
    It has many awk recipes [one liners](http://awk.info/?OneLiners),
    [ten liners](http://awk.info/?TenLiners),
    [Tips]([http://awk.info/?Tips),
    [real world Awk programs](http://awk.info/?awk100).<br />
    The [lawker repository](https://code.google.com/p/lawker/)
    holds all the code (and web pages).<br />
    The site seems sleeping, but may be not dead as there is a
    [GitHub Project new.awk.info
    ](https://github.com/pjimenez-cl/new.awk.info).

# Sed
-   [Wikipedia: Sed](http://en.wikipedia.org/wiki/Sed "en.wikipedia.org Sed"),
    you may find there references to many tutorials.
-   [sed manual
    ](http://www.gnu.org/software/sed/manual/html_node/index.htm")
-   [Sed by example, Part 1
    ](http://www.ibm.com/developerworks/linux/library/l-sed1.html),
    [Part 2
    ](http://www.ibm.com/developerworks/linux/library/l-sed2.html),
    and [Part 3
    ](http://www.ibm.com/developerworks/linux/library/l-sed3.html)
    by Daniel Robbins at IBM developerWorks is an excellent
    introduction by examples to sed.
-   Bruce Barnett [Grymoire: Sed - An Introduction and Tutorial
    ](http://www.grymoire.com/Unix/Sed.html)
-   [sed1line](http://sed.sourceforge.net/sed1line.txt)
    are handy sed one liners by Eric Pement.
    -   [Sed One-Liners Explained
        ](http://www.catonmat.net/blog/sed-one-liners-explained-part-one/)
-   [sed.sourceforge.net](http://sed.sourceforge.net/)
    host an extended collections of links to sed documentation programs
    and tools and a great collection of sed scripts.
-   [sedsed](http://sedsed.sourceforge.net/)
    (GPL) is a very usefull sed debugger (and formatter) written in
    python.
    -   [original sedsed by E. Pement
        ](http://www.pement.org/sed/sedsed.txt)
    -   [ksh version
        ](http://www.pement.org/sed/sd.ksh.txt
-   [Seder's grab bag](http://sed.sourceforge.net/grabbag/)
    is a collection of sed scripts and tutorials.

# Regexps {#regexps}
-   [Regular Expressions/POSIX-Extended Regular Expressions - Wikibook
    ](https://en.wikibooks.org/wiki/Regular_Expressions/POSIX-Extended_Regular_Expressions).
-   [Regexp Chapter of Gawk manual
    ](http://www.gnu.org/software/gawk/manual/html_node/Regexp.html)
    describes gnu Extended Regexps.
-   <a name="pcre"></a>[PCRE - Perl Compatible Regular Expressions](http://www.pcre.org/)
    is a set of C functions that implement regular expression pattern matching using the
    same syntax and semantics as
    [Perl Regular Expressions](http://perldoc.perl.org/perlre.html).
    _PCRE_ are used in numerous languages and utilities.
    -   [PCRE2 HTML documentation
        ](http://www.pcre.org/current/doc/html/):
        [pcre2syntax - pcre2 expression syntax quick-reference
        ](http://www.pcre.org/current/doc/html/pcre2syntax.html).
    -   The [Wikipedia:  PCRE](http://en.wikipedia.org/wiki/PCRE)
        page details the features of pcre expressions and the differences
        with perl re.
    -   There are many online pcre tester:
        [regexpal](http://www.regexpal.com/),
        [regex101](https://regex101.com/),
        [debuggex](https://www.debuggex.com/),
        [myregextester](https://www.myregextester.com/),
        [reg-exp](http://reg-exp.com/),
        [pythex](http://pythex.org/) _python regexp_.
-   See also the {{< iref "python_libraries#python_re" "Python _re_ references" >}},
    {{< iref "text_editors#vim_regexps" "Vim Regexps" >}}.


## Grep tools {#grep}
-   [ack](http://beyondgrep.com/)
    perl tool like grep, optimized for programmers. _In debian._
-   [ag](https://geoff.greer.fm/ag/)
    The silver searcher_ like grep and ack but written in C and a lot
    quicker. [Emacs package ag](https://github.com/Wilfred/ag.el) s a front end to ag.
     _In debian._
-   [BurntSushi/ripgrep](https://github.com/BurntSushi/ripgrep)
    recursively searches directories for a regex pattern.  _In debian._
    -   Ripgep_ use [Crate regexps](https://docs.rs/regex/1.4.2/regex/#syntax)
        which are similar to Perl-style regular expressions, but lacks look around and
        backreferences.
    -   [ripgrep User Guide](https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md)
    -   [supplementary documentation
        ](https://github.com/BurntSushi/ripgrep/blob/master/README.md#documentation-quick-links).
    -   [ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}
        ](https://blog.burntsushi.net/ripgrep/)
        by the author of _ripgrep_ Andrew Gallant
-   [txt2regex](http://txt2regex.sourceforge.net/) is a regular expression
    wizard written in bash that converts human sentences to regexps
    (gnu prce or more formats ...).

# Browse, bookmark and change directory {#dir_bookmarks}

-   [apparix](http://micans.org/apparix/)
    is a console-based bookmark tool for fast file system navigation inspired by
    _cdargs_. There are bash and zsh versions.
    It does not include a curse browser as cdargs does.
    You can combine it with _goto_ from Sitaram Chamarty.
-   [autojump](https://github.com/joelthelion/autojump) (GPL)
    is a directory tracker that _jump_ to the most used directory matching the argument.
    an alternative in pure shell is _z_.
-   [cdargs](http://www.skamphausen.de/cgi-bin/ska/CDargs) (GPL)
    _cdargs_ is a file system navigation tool;
    It plugs into the shell built-in cd-command and adds bookmarks and a browser to it.
    It includes an elisp interface, which allow to use it in emacs to go to a direcory.
    It is packaged in Debian.
    There is also elisp code for plugging cdargs in ido in
    [ido-jb-misc-extras.el](https://www.emacswiki.org/emacs/ido-jb-misc-extras.el).
-   [go2](http://savannah.nongnu.org/projects/go2/) (GPL)
     is a fast and simple directory finder for console and desktop
     on the style of the old Norton Change Directory for DOS, but designed specifically for bash.
     It is similar to _wcd_, but does not include the ncurses browser.
-   [goto](https://github.com/sitaramc)
    by Sitaram Chamarty combine cd and find and complements
    _apparix_.
-   [Ondir](http://swapoff.org/OnDir) from
    [Alex Thomas](http://swapoff.org/) s a program that automatically
    executes scripts as you traverse directories at a terminal.
-   [Wcd](http://waterlan.home.xs4all.nl) (GPL)
    is a command-line program to change directory fast
    modeled after Norton Change Directory (NCD)..
    One needs to type only a part of a directory name and wcd will jump to it.
    _wcd_ is packaged in Debian. It is similar to _go2_
-   [z](https://github.com/rupa/z) by [rupa](http://un.ix.io/)
    Tracks your most used directories, and after learning phase, z will take you to the
    most used directory that matches all of the regexes given on the command line.
    It is an [alternative to _autojump_](http://un.ix.io/bash%20directory%20jump)
    that avoids to launch python on every call.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
