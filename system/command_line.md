---
title: Command Line
---

# refs
-   [Category:Commands - ArchWiki](https://wiki.archlinux.org/title/Category:Commands)


# readline
-   [The GNU Readline Library](https://tiswww.case.edu/php/chet/readline/rltop.html)
    is the official documentation, it contains three documents that are also available
    as info manual:
    -   [GNU Readline Library User Manual](https://tiswww.case.edu/php/chet/readline/rluserman.html)
        _rluserman_ describe the end user interface of the GNU Readline Library.
    -   [GNU Readline Library](https://tiswww.case.edu/php/chet/readline/readline.html),
        *readline*, the GNU Readline Library. It contains a copy of the previous user
        manual, followed by a chapter on *Programming with GNU Readline*.
    -   [GNU History Library](https://tiswww.case.edu/php/chet/readline/history.html)
-   [Readline - ArchWiki](https://wiki.archlinux.org/title/Readline)
-   {{< man "readline(3)" >}}


To see the default bindings in readline enter
``` sh
INPUTRC=~/dev/null bash -c 'bind -pm emacs' | \
grep -vE '^#|: (do-lowercase-version|self-insert)$'
```
for vi bindings replace `emacs` by `vi`.

Look also to the answer to
[What are readline's modes, keymaps and their default bindings?
](https://unix.stackexchange.com/questions/303479/what-are-readlines-modes-keymaps-and-their-default-bindings#303480)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
