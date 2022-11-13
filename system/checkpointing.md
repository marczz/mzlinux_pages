---
title: Checkpointing
---

Tmux is in it's {{< iref "tmux" "own page" >}}.

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
    It was abandonned in 2013, but is still
    [packaged in Debian](https://tracker.debian.org/pkg/blcr).
-   [CRIU](http://criu.org/) (GPL)
    is an userspace applications  to freeze a running application (or part of it)
    and checkpoint it to persistent storage. {{< wp "CRIU"  "Wikipedia: CRIU" >}} is in Debian
    and in active development in 2022. There are many HOW-TOs and uses cases references
    in the [CRIU Home Page](http://criu.org/). It is in Debian.
-   <a name="dtach"></a>[dtach](https://github.com/crigler/dtach) (GPL)
    emulates the detach feature of screen. Dtach is in Debian. The
    [repository README](https://raw.githubusercontent.com/crigler/dtach/master/README)
    provides examples of use.
    -   [ArchWiki: Dtach](https://wiki.archlinux.org/index.php/Dtach)
-   <a name="abduco"></a>[abduco](http://www.brain-dump.org/projects/abduco/) (ISC Licence)
    is a fork of {{< iref "#dtach" "dtach" >}} with some
    [improvements](http://www.brain-dump.org/projects/abduco/#dtach)
    [Git Repository](https://github.com/martanne/abduco)
-   [DMTCP: Distributed MultiThreaded CheckPointing](http://dmtcp.sourceforge.net/) (LGPL)
    checkpoint the state of multiple simultaneous applications, including multi-threaded
    and distributed applications.  It operates directly on the user binary executable.
    _Active in 2022 last release 2019_.
    [GitHub DMCTP](https://github.com/dmtcp/dmtcp)
-   <a name=reptyr></a>[reptyr](https://github.com/nelhage/reptyr) (MIT license)
    is a recent utility for taking an existing running program and
    attaching it to a new terminal.

    It is useful for moving a long-running process into a tmux session.

    It is in Debian.
    _Active development in 2022._

# Terminal multiplexors {#terminal_multiplexors}

-   [Gnu Screen documentation](http://aperiodic.net/screen/)
-   {{< iref "console#dvtm" "dvtm" >}} by itself does only console
    virtual terminal management, but it can be launched with
    {{< iref "#abucco" "abucco" >}} or
    {{< iref "#dtach" "dtach" >}} to provide session management.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
