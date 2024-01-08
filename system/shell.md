---
title: Shell
---

# Shell references
-   [Wikipedia: Unix shells](http://en.wikipedia.org/wiki/Unix_shell),
    [Comparison of computer shells
    ](http://en.wikipedia.org/wiki/Comparison_of_computer_shells),
    {{< wp "POSIX" >}}
-   [Command-line shell - ArchWiki](https://wiki.archlinux.org/title/Command-line_shell)
-   [uhub/awesome-shell](https://github.com/uhub/awesome-shell)
    long list of unclassified shell references. _so messy that is is unusable_.
-   [alebcay/awesome-shell](https://github.com/alebcay/awesome-shell)
    properly classified list of shell references, contains not only resources for shell
    development, but also  list of application written in shell.
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
-   [Shell development - awesome-shell
    ](https://github.com/alebcay/awesome-shell#shell-script-development).

-   [Argbash](https://argbash.readthedocs.io/en/latest/index.html)
    is a bash code generator that can assist you in writing scripts that accept
    arguments.
    -   [argbash · GitHub](https://github.com/matejak/argbash)
    -   [Argbash alternatives
        ](https://argbash.readthedocs.io/en/latest/others.html)
-   John Dubois who maintains [armory.com](http://www.armory.com/)
    has made available a huge number of
    [Ksh and awk scripts](http://www.armory.com/~ftp/) _2011_.
-   [bash-modules](https://github.com/vlisivka/bash-modules)
    A module system for bash which provide a set of bash subroutines,
-   [log4sh](https://sites.google.com/a/forestent.com/projects/log4sh) (LGPL)
    is a logging framework for shell scripts
-   Pádraig Brady has many command line references, in his
    [PixelBeat Site](http://www.pixelbeat.org) and scripts in
    [his GitHub repository](https://github.com/pixelb) (LGPL).
-   [pluginhook](https://github.com/progrium/pluginhook) (MIT)
-   [sh](https://pkg.go.dev/mvdan.cc/sh/v3)
    is a Go shell parser, formatter, and interpreter. Supports POSIX Shell, Bash, and mksh.
    -   [mvdan / sh - GitHub](https://github.com/mvdan/sh)
        (BSD 3-Clause revised license)
    -   `shfmt` formats shell programs, accoding to a [cannonical syntax
        ](https://github.com/mvdan/sh/blob/v3.3.1/syntax/canonical.sh)
    A plugin system for Bash. In Debian.
-   [Heiner's SHELLdorado](http://www.shelldorado.com/)
    see also the extensive
    [link page](http://www.shelldorado.com/links/index.html)
-   [shunit](http://shunit.sourceforge.net/)
    is the first unit testing framework for Bourne derived shells.
-   [shunit2](https://github.com/kward/shunit2)
    is an improved xUnit based unit testing for Unix shell scripts.
-   Nathaniel Landau [Boilerplate Shell Script Template
    ](https://natelandau.com/boilerplate-shell-script-template/)
    is a template for writing shell scripts.
-   [docopt](http://docopt.org/)
    is a command-line interface description language which allows you to define the
    interface for your command-line app, and automatically generate a parser for it.

    It has [implementations for many languages](https://github.com/docopt):
    {{< iref "python_libraries#docopt" "Docopt for Python" >}}, go, C, cpp, php, rust,
    nim, ruby, cofee script, clojure, lua,

    The [Shell interpreter for docopt](https://github.com/docopt/docopts) is a command
    line wrapper for bash written in go.
    [doctops.sh](https://github.com/docopt/docopts/blob/master/docs/README.md)
    is a library companion of doctops binary.

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

The [dash git repository](http://git.kernel.org/cgit/utils/dash/dash.git)
gives the source and a [changelog](http://git.kernel.org/cgit/utils/dash/dash.git)

The details of the [Ash (Almquist Shell) Variants
](http://www.in-ulm.de/~mascheck/various/ash/) is given in this page.


[Bashism - How to make bash scripts work in dash](http://mywiki.wooledge.org/Bashism)
list some of the most common bashisms, i.e. features not defined by
POSIX and how to translate them to POSIX shells.

[Ubuntu - Dash as /bin/sh](https://wiki.ubuntu.com/DashAsBinSh), has the same goal
than the previous reference
detail how to convert a bash script to a posix one, examining the bash specific
constructs, *the bashisms* and how to replace them by posix constructs.

[checkbashism.pl
](https://salsa.debian.org/debian/devscripts/-/blob/master/scripts/checkbashisms.pl)
is a script in the debian package *devscripts*, it comes with a manual
{{< man "checkbashisms(1)" >}}.

The purpose of *checkbashism* is to check what in a script is not posix. It is
used to convert your bash script to dash.

There is a [slightly different release in Sourceforge
](https://sourceforge.net/projects/checkbaskisms).

To work with portable posix shell you can also use
[Autoconf manual - Portable Shell Programming
](http://www.gnu.org/savannah-checkouts/gnu/autoconf/manual/autoconf-2.69/html_node/Portable-Shell.html)
and
[Rich’s sh (POSIX shell) tricks](http://www.etalabs.net/sh_tricks.html).

[Yash](https://yash.osdn.jp/) (GPL)
has a special status among the ash family. It is conceived to be the most
POSIX-compliant shell, Yash fully supports POSIX.1-2008 (IEEE Std 1003.1, 2013
Edition). Yash features exceed those of dash and busybox ash; and in contrast to dash it
can be used as an interactive shell.

It features global aliases, arrays, socket redirection, pipeline redirection, and
process redirection, brace expansion, extended globbing, fractional numbers in
arithmetic expansion, prompt command and command-not-found handler, command line
completion.

Yash is available in Debian, Ubuntu, Fedora.

The manual is also [available online](https://yash.osdn.jp/doc/).

All these shell are tiny on an amd64 dash is 1.6M resident / 1.4M
shared; yash 1.1M/1.0M; busybox 2.3M/2.1M.

Busybox seems a lot bigger but it includes all coreutils, awk, sed
.... in the same executable.

Bash (without my big init) is 3.8M/3.2M; zsh (without user init)
4.4M/3.6M.

:
# Bash

-   [awesome-bash](https://github.com/awesome-lists/awesome-bash)
    A curated list of Bash scripts and resources.
-   [Chet Ramey](https://tiswww.case.edu/php/chet):
    [Bash page](https://tiswww.case.edu/php/chet/bash/bashtop.html)
-   [Bash Reference Manual (gnu)](https://www.gnu.org/software/bash/manual/)
    or you find it also at
    [Bash Reference Manual (chet)](https://tiswww.case.edu/php/chet/bash/bashref.html),
    it should be also installed as an info file.
-   [BASH(1) Manual Page](https://tiswww.case.edu/php/chet/bash/bash.html)
-   [Chet Ramey official Bash FAQ](http://tiswww.case.edu/php/chet/bash/FAQ)
    is still useful but not updated since Bash version 5.1.
-   [Greg's Wiki Bash FAQ](http://mywiki.wooledge.org/BashFAQ)
    _other material from Greg's Wiki are {{< iref "#gregs_wiki" "below" >}}
-   [Greg's Wiki Bash Reference Sheet](http://mywiki.wooledge.org/BashSheet)
-   [Bash Guide for Beginners](http://www.tldp.org/LDP/Bash-Beginners-Guide/html/)
    _2008_.
-   [Bash Programming Introduction](http://tldp.org/HOWTO/Bash-Prog-Intro-HOWTO.html)
    _for this elementary guide being old (2000) is not challenging_.
-   [Advanced Bash Scripting Guide](http://tldp.org/LDP/abs/html/index.html) *2014*.
-   [Bash Hackers Wiki
    ](https://github.com/rawiriblundell/wiki.bash-hackers.org/blob/main/start.md)
    hold documentations about the GNU Bash. The first page is an index of pages on
    commands, builtins, and expressions of bash.
    the original site.

    `bash-hackers.org/wiki` went down but the last version from wayback machine has been
    downloaded on [this Github repository
    ](https://github.com/rawiriblundell/wiki.bash-hackers.org/).
-   <a name="gregs_wiki"></a>[Greg Wooledge's Wiki, in short Greg's Wiki
    ](https://mywiki.wooledge.org/)
    contains bash resources:
    -   [Bash Guide](http://mywiki.wooledge.org/BashGuide)
        more than a Tutorial, a guide to nearly all bash constructs.
    -   [Bash Reference Sheet](http://mywiki.wooledge.org/BashSheet)
        a shorter manual page.
    -   [BASH Frequently Asked Questions](http://mywiki.wooledge.org/BashFAQ)
    -   [Bash Pitfalls](http://mywiki.wooledge.org/BashPitfalls)
        a long list of common bash errors and how to mend them.
    -   [Bash Weaknesses](http://mywiki.wooledge.org/BashWeaknesses)
        or _don't use bash for large programs, they would be unreliable_.
    -   The [Shell category](http://mywiki.wooledge.org/CategoryShell)
        includes many interesting pages.
-   [Shell style guide](https://google.github.io/styleguide/shellguide.html)
    some additional explanations in this [Stack Overflow answer
    ](https://stackoverflow.com/a/45386798/965798).
-   Bash by example by Daniel Robbins:
    [Part 1](http://www.ibm.com/developerworks/linux/library/l-bash/index.html),
    [Part 2](http://www.ibm.com/developerworks/linux/library/l-bash2/index.html),
    [Part 3](http://www.ibm.com/developerworks/library/l-bash3/index.html).

    From the same author: [Tip: Prompt magic
    ](http://www.ibm.com/developerworks/linux/library/l-tip-prompt/index.html?dwzone=linux)
    Show how to customize the BASH prompt, and set the xterm title.
-   [Commandline Fu](http://www.commandlinefu.com/)
    is a repository for sharing shell commands. The
    [FAQ](http://www.commandlinefu.com/site/faq) gives other accesses to it like RSS
    feeds.
-   [bashdb](http://bashdb.sourceforge.net/) is a source code debugger for bash.
-   [Bashdoc](https://github.com/ajdiaz/bashdoc) (GPL-3.0)
    is a bash documentation processor similar to javadoc but use reStructuredText to
    provide the final document.
-   [Starship: Cross-Shell Prompt](https://starship.rs/) (ISC License)
    customizable prompt for any shell. A fast prompt written in Rust for many shells
    bash, fish, zsh
    -   [starship - GitHub](https://github.com/starship/starship)

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

Note that variable, and arithmetic expansion and command and process substitution are
done in the same pass from left to right.

A (double) quoted string and **a quoted command substitution** is not subject to word
splitting and pathname expansion

After an assignment only a subset of these expansions hold, namely: tilde expansion,
parameter expansion, command substitution, arithmetic expansion, and quote removal. (no
pathname and brace expansion, nor process substitution)

## Bash development tools

-   [explainshell](https://explainshell.com/)
    is a is a web online tool capable of parsing man pages, extracting options and
    explaining a given command-line by matching each argument to the relevant help text
    in the man page.
    -   [Github - explainshell](https://github.com/idank/explainshell) (GPL-3.0)
-   [shellcheck](https://github.com/koalaman/shellcheck) (GPL-3.0)
    A ssh/sh shell script static analysis tool written in haskell.


    *Shellchek* is a unix command and can be used from emacs *flycheck* or *flymake* and from (neo)vim with
     *ALE*, *Neomake*, or *Syntastic*.

     It can be used online on the site [shellcheck.net](https://www.shellcheck.net/).

    *shellcheck* is packaged in Debian.

    -   [shellcheck Wiki · GitHub](https://github.com/koalaman/shellcheck/wiki)

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

# Other shells
-   [Elvish Shell](https://elv.sh/)
     is an expressive programming language and a versatile interactive shell.
     Elvish uses Pipelines whish can carry structured data, not just text. You can
     stream lists, maps and even functions through the pipeline.
     _Elvish_ is in Debian and Alpine.
-   [Ion](https://gitlab.redox-os.org/redox-os/ion/)
    an unix shell written in rust.
-   [Nushell](https://www.nushell.sh/) (MIT License)
    _Nushell_ is in Alpine.
-   [Oil](https://www.oilshell.org/) (Apache License 2.0)
    is a new POSIX & bash compatible shell written in Python.
    While written in Python it is  translated to C++, so the  executable doesn't depend
    on Python.

    The bash compatible layer is
    [OSH Langage](https://www.oilshell.org/cross-ref.html#osh-language),
    which runs real shell programs while adding reliable error handling, safe processing
    of user-supplied data, lack of "quoting hell", and better error messages and tools.

    You can add some [Global Shell Options
    ](https://www.oilshell.org/release/latest/doc/options.html)
    to _OSH_, they allow more powerful langage constructs at the price of breaking bash
    compatibility. When you add all option to _OSH_ you get _OIL_.
    _Oil_ is in Alpine.

# Shell Utilities
-   [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/html_node/index.html)
-   [Shell and Utilities volume of POSIX.1-2017
    ](https://pubs.opengroup.org/onlinepubs/9699919799/utilities/contents.html)
-   [POSIX Shell and Utilities Quick Reference](http://shellhaters.org/)
    See also the [slides of Shell Hater's Handbook](http://shellhaters.org/deck/#1)
-   [Core utilities - ArchWiki](https://wiki.archlinux.org/title/Core_utilities)
    lists coreutils commands with link to their manual (man or info), and gives
    alternatives to the commands.

# Awk {#awk}

-   Wikipedia {{< wp "Awk" >}}
-   [Gawk: Effective AWK Programming
    ](http://www.gnu.org/software/gawk/manual/)
    (FDL) an online book by Arnold Robbins available in pdf and html.
    The [Regexp Chapter
    ](http://www.gnu.org/software/gawk/manual/html_node/Regexp.html)
    is a good reference on gnu Regexps.
-   [Awk Faq](http://www.faqs.org/faqs/computer-lang/awk/faq/)
-   [Awk in 20 Minutes](https://ferd.ca/awk-in-20-minutes.html) by Fred Hebert.
-   [Getting started with awk](http://www.cs.hmc.edu/tech_docs/qref/awk.html)
-   [Steve's Awk Acadamy](http://www.troubleshooters.com/codecorn/awk/index.htm)
    by Steve Litt is an awk tutorial.
-   Bruce Barnett [Grymoire: Awk](http://www.grymoire.com/Unix/Awk.html).
-   [awk cheat sheet (.pdf)](http://www.catonmat.net/download/awk.cheat.sheet.pdf) and
    [awk cheat sheet (.txt)](http://www.catonmat.net/download/awk.cheat.sheet.txt) by
    [Peteris Krumins](http: www.catonmat.net).
-   [Awk.Info](http://awk.info/) is the Portal of Awk community.
    It has many awk recipes [one liners](http://awk.info/?OneLiners),
    [ten liners](http://awk.info/?TenLiners),
    [Tips]([http://awk.info/?Tips),
    [real world Awk programs](http://awk.info/?awk100).

    The [lawker repository](https://code.google.com/p/lawker/) holds all the code
    (and web pages).
    The site seems sleeping, but may be not dead as there is a
    [GitHub Project new.awk.info](https://github.com/pjimenez-cl/new.awk.info).

# Sed
-   [Wikipedia: Sed](http://en.wikipedia.org/wiki/Sed),
    you may find there references to many tutorials.
-   [sed manual](http://www.gnu.org/software/sed/manual/html_node/)
-   [Sed by example, Part 1
    ](http://www.ibm.com/developerworks/linux/library/l-sed1.html),
    [Part 2](http://www.ibm.com/developerworks/linux/library/l-sed2.html),
    and [Part 3](http://www.ibm.com/developerworks/linux/library/l-sed3.html)
    by Daniel Robbins at IBM developerWorks is an excellent introduction by examples to
    sed.
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
    (GPL) is a very usefull sed debugger (and formatter) written in python.
    -   [original sedsed by E. Pement](http://www.pement.org/sed/sedsed.txt)
    -   [ksh version](http://www.pement.org/sed/sd.ksh.txt)
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
    a syntax and semantics derived from
    [Perl Regular Expressions](http://perldoc.perl.org/perlre.html).
    _PCRE_ are used in numerous languages and utilities.
    -   [PCRE2 HTML documentation
        ](https://pcre2project.github.io/pcre2/doc/html/index.html):
        -   [pcre2syntax - pcre2 expression syntax quick-reference
            ](https://pcre2project.github.io/pcre2/doc/html/pcre2syntax.html).
    -   The [Wikipedia:  PCRE](http://en.wikipedia.org/wiki/PCRE)
        page details the features of pcre expressions and the differences
        with perl re.
    -   [Search and replace tricks with ripgrep
        ](https://learnbyexample.github.io/substitution-with-ripgrep/).
    -   [ripgrep is faster than {grep, ag, git grep, ucg, pt, sift}
        ](https://blog.burntsushi.net/ripgrep/)
        in Andrew Gallant's Blog
    -   [Regular-Expressions.info](https://www.regular-expressions.info/)
        -   [Regex references](https://www.regular-expressions.info/refflavors.html)
            and [Replacement Strings Reference
            ](https://www.regular-expressions.info/refreplace.html)
            contain tables where you can select your regex variant among a large list.
        -   [Regex Tutorial](https://www.regular-expressions.info/tutorial.html) and
            [Replacement Strings Tutorial
            ](https://www.regular-expressions.info/replacetutorial.html)
    -   [Regular Expression HOWTO — Python documentation
        ](https://docs.python.org/dev/howto/regex.html)
        is for Python RE, which are close _but not identical_ to PCRE.
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
-   [ripgrep](https://github.com/BurntSushi/ripgrep) (Unlicense and MIT licenses)
    recursively searches directories for a regex pattern.  _In debian._
    -   [ripgrep User Guide](https://github.com/BurntSushi/ripgrep/blob/master/GUIDE.md)
    -   *Ripgep* by default uses
        [Crate regexps](https://docs.rs/regex/latest/regex/#syntax)
        which are similar to Perl-style regular expressions, but lacks look around and
        back-references.

        If you need pcre2 additional features you can use the PCRE2 regex engine instead
        of the default with the --pcre2 (-P for short) flag, but it will slow down
        ripgrep. More details are [explained in the faq
        ](https://github.com/BurntSushi/ripgrep/blob/master/FAQ.md#why-does-ripgrep-get-slower-when-i-enable-pcre2-regexes).
    -   [supplementary documentation
        ](https://github.com/BurntSushi/ripgrep/blob/master/README.md#documentation-quick-links).
    -   [ripgrep FAQ](https://github.com/BurntSushi/ripgrep/blob/master/FAQ.md)
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

# Change environment
-   [direnv](https://direnv.net/) (MIT License)
    unclutter your .profile by loading and unloading environment variables depending
    on the current directory.

    [emacs-direnv](https://github.com/wbolster/emacs-direnv) is direnv integration for
    emacs.

    _Direnv_is in Debian and Alpine.
-   [Ondir](http://swapoff.org/OnDir)
    from [Alex Thomas](http://swapoff.org/) is a program that automatically
    executes scripts as you traverse directories at a terminal.

# Bulk file renamers
-   [GPRename](http://gprename.sourceforge.net/) (GPL)
    is a perl/perl GTK2 GUI batch renamer. GPRename easily can replace, remove, insert,
    delete and number consecutively files and directorys.
-   _rename_ or [File-Rename](https://metacpan.org/dist/File-Rename)
    is a perl extension for renaming multiple files. Available n any distribution
    including Debian.
    -   a [rename tutorial
        ](https://www.howtogeek.com/423214/how-to-use-the-rename-command-on-linux/)
-   [renameutils](https://www.nongnu.org/renameutils/) (GPL)
    The file renaming utilities are a set of CLI programs designed to make renaming of
    files faster and less cumbersome.
    It  consists of five programs - qmv, qcp, imv, icp and deurlname..
    -   `qmv` ("quick move") allows file names to be edited in a text editor.
        The names of all files in a directory are written to a text file,
        which is then edited by the user. The text file is read and parsed,
        and the changes are applied to the files.
    -   `qcp` ("quick cp") program works like qmv, but copies files instead of moving
        them.
    -   `imv` ("interactive move") allows a file name to be edited in the terminal using
        the GNU Readline library.
    -   `icp` is similar but copies files.
    -    `deurlname` removes URL encoded characters (such as %20 representing space)
         from file names.
    _renameutils_ is in Debian.

The [Github topic _renamer_](ttps://github.com/topics/renamer) point out more renamer
software.

In emacs we can [rename file in Dired
](https://ftp.gnu.org/old-gnu/Manuals/emacs-21.2/html_chapter/emacs_31.html#SEC405)
the use of [dired editable buffer (WDired)](https://www.emacswiki.org/emacs/WDired)
is very convenient for renaming files in bulk.

## prefix files to put them in order
-   [autorenamer](https://marcin.owsiany.pl/autorenamer-page) (BSD License)
    A PyGTK2 GUI to rename files in order, by draging them at the wanted order.
    It is in Debian.
-   _mrename_ or Mass Rename is a simple pair of shell scripts giving an automatic and
    simple way to rename multiple files with a customizable prefix and a progressive
    number. It is in Debian.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
