---
title: Git & alt. SCM
---


# General References on Source Conf Management
-   {{< wp "Revision_control"  "Wikipedia: Revision Control" >}}
    and {{< wp "Comparison of revision control software" >}}
-   [Better SCM Initiative](http://better-scm.shlomifish.org/)
    compares the SCMs: Aegis, Arch, Bazzaar, BitKeeper, Darcs, Git,
    Mercurial, Monotone, Perforce, Subversion, Vesta.
-   [Version Control System Comparison
    ](http://better-scm.shlomifish.org/comparison/comparison.html)
-   [Happenings in the VCS world
    ](http://blogs.gnome.org/newren/2008/03/01/happenings-in-the-vcs-world/)
    paper by David A. Wheeler
-   [Making Sense of Revision-control Systems
    ](http://queue.acm.org/detail.cfm?id=1595636) by Bryan O'Sullivan
-   comparison of vcs:  [Why Choose Mercurial?
    ](http://hgbook.red-bean.com/read/how-did-we-get-here.html),
    [Why Git is Better Than X
    ](http://whygitisbetterthanx.com/),
    [Why Switch to Bazaar?
    ](http://doc.bazaar.canonical.com/migration/en/why-switch-to-bazaar.html)
-   [Semantic Versioning](http://semver.org/)
    is a simple set of rules and requirements that dictate how version
    numbers are assigned and incremented.  Under this scheme, version
    numbers and the way they change convey meaning about the
    underlying code and what has been modified from one version to the
    next.

# Information by system
_Git is below!_

-   [The CVS Book](http://cvsbook.red-bean.com/)
-   [cvsup](http://www.cvsup.org/) general-purpose mirroring tool
    tailored to CVS repositories.
-   {{< wp "GNU_arch"  "Arch" >}} (GPL) is a distributed revision control system
    also known as __tla__ from the name of the main Arch command.
    Tla author Tom Lord seems  stopped developping tla in 2006 to
    start implementing revc (kind of arch 2.0) whose development is
    now discontinued.
-   {{< wp "Bazaar_(software)"  "Bazaar" >}} GPL is a distributed revision control
    system written in python. _Bazaar_ is was previously nammed
    _Bazaar-ng_ and is a fork from the previous _Bazaar_ also known as _Baz_
    itself a fork from _Arch_.
-   [Subversion](http://subversion.tigris.org/),
    [Version Control with Subversion](http://svnbook.red-bean.com/)
    (subversion reference manual), and
    [Subversion FAQ](http://subversion.apache.org/faq.html).
-   [Rapidsvn](http://rapidsvn.org/) is a gui for Subversion.
-   Tools for statistical reports:
    [mpy-svn-stats](http://mpy-svn-stats.berlios.de/),
    [CVSAnalY](http://tools.libresoft.es/cvsanaly) (GPL). For git there is
    [GitStats](http://gitstats.sourceforge.net/) (GPL) and
    [Pepper](http://scm-pepper.sourceforge.net/) (GPL)
    supports git, mercurial and Subversion.
-   {{< wp "Darcs" >}} is a revision control system written in Haskell,
    along the lines of CVS or arch. Darcs has two distinctive
    features: 1) each copy of the source is a fully functional branch,
    and 2) underlying darcs is a powerful theory of patches.
    [Darcs Home](http://darcs.net/)
    [Darcs Manual](http://darcs.net/manual/)
-   [Mercurial (hg)](http://mercurial.selenic.com/)
    (GPL) is a fast lightweight distributed Source Control Management
    system written in python. Mercurial is used for some big open
    source projects like alsa, xine, e2fsprogs, mutt, xen, moinmoin
    ....
    -   [Mercurial: The Definitive Guide](http://hgbook.red-bean.com/read/)
    -   [Mercurial for Git users](http://mercurial.selenic.com/wiki/GitConcepts)
-   [src](https://gitlab.com/esr/src)
    from Eric Raymond is a *RCS reloaded* with a modern UI, designed
    to manage single-file solo projects. It features sequential
    revision numbers, lockless operation, embedded command help, and a
    command set that familiar to users of Subversion, Mercurial, and
    Git.



# Git
I have also set a [git-memo](http://git-memo.mzlinux.org/)
which gives some reminders and explanations on git use.

-   [Git](http://git-scm.com) is a
    GPL distributed source code management tool.
    Git is born following the withdraw of free use of
    BitKeeper for free software, it has been developped by the Linux
    Kernel team to replace BitKeeper for the kernel source Management,
    this and more is explained in the very detailled
    [Wikipedia: Git](http://en.wikipedia.org/wiki/Git_%28software%29)
    article.
-   [Git Home page](http://git-scm.com/) at [git-scm.com
    ](http://git-scm.com/).
-   [Git Wiki](http://git.wiki.kernel.org/index.php) cross-reference
    Main Git resources.
    -   [Git FAQ](https://git.wiki.kernel.org/index.php/GitFaq)
    -   [Git Documentation
        ](https://git.wiki.kernel.org/index.php/GitDocumentation)
    -   [Interfaces Frontends And Tools
        ](https://git.wiki.kernel.org/index.php/Interfaces,_frontends,_and_tools)
    -   [Git Links
        ](https://git.wiki.kernel.org/index.php/GitLinks);
    -   [
-   [Awesome Git](https://github.com/dictcp/awesome-git)
    list of Git resources
    -   [Git Add-ons](https://github.com/stevemao/awesome-git-addons)
        to enhance the `git` CLI.
    -   [Awesome GitHub](https://github.com/Kikobeats/awesome-github)
        -   [Browser extensions for GitHub
            xs](https://github.com/stefanbuck/awesome-browser-extensions-for-github)
        -   [Toolkits for Github
            ](https://github.com/xohozu/awesome-toolkit)

# Git Documentation
Git includes a live version of it's documentation. You can access each
manual with ``git <command> --help`` or ``git help <command>`` the
list of available command by  ``git help -a``
you can also get the guides
with ``git help <concept>`` where concept is one of
[attributes
](https://www.kernel.org/pub/software/scm/git/docs/gitattributes)
, [everyday
](https://www.kernel.org/pub/software/scm/git/docs/giteveryday.html)
, [glossary
](https://www.kernel.org/pub/software/scm/git/docs/gitglossary.html)
, [ignore
](https://www.kernel.org/pub/software/scm/git/docs/gitignore.html)
, [modules
](https://www.kernel.org/pub/software/scm/git/docs/gitmodules.html)
, [revisions
](https://www.kernel.org/pub/software/scm/git/docs/gitrevisions.html)
, [tutorial
](https://www.kernel.org/pub/software/scm/git/docs/gittutorial.html)
, [workflows
](https://www.kernel.org/pub/software/scm/git/docs/gitworflows.html).

## Documentation references
-   [git wiki - Git Documentation
    ](https://git.wiki.kernel.org/index.php/GitDocumentation)
    is a complete source of documentation but is not always up-to-date
    and some links are broken.
-   [git wiki - Git Links
    ](https://git.wiki.kernel.org/index.php/GitLinks)
    references articles, blogs, mailing lists, talks, git
    comparisons...
-   [git-scm - External Links](https://git-scm.com/doc/ext)
-   [Git FAQ](https://git.wiki.kernel.org/index.php/GitFaq)
-   And to get a fresh view of what is coming up, you can search
    the web for Git
    [tutorials](http://www.google.com/search?q=git+tutorial),
    [guides](http://www.google.com/search?q=git+guide),
    [howto](http://www.google.com/search?q=git+howto), and
    [comparisons](http://www.google.com/search?q=git+comparison)
-   The mailing list is `comp.version-control.git` archived at:
    -   You find it archived at:
        [gmame  (search form)](http://search.gmame.org) with a choice of formats:
        [gmame.news: git](http://news.gmane.org/gmane.comp.version-control.git)
        [gmame blog-like interface : git
        ](http://blog.gmane.org/gmane.comp.version-control.git),
        [gmame rss feeds](http://rss.gmane.org/topics/excerpts/gmane.comp.version-control.git)
    -   It is also mirrored at [marc: git](http://marc.info/?l=git)
        *(search form)*.
-   [users mailing list on google groups
    ](http://groups.google.com/group/git-users)
-   IRC  #git ([log](http://colabti.org/irclogger/irclogger_logs/git))
    or #git-devel ([log
    ](http://colabti.org/irclogger/irclogger_logs/git-devel))
    channels on irc.freenode.net. #github #bitbucket and #gitlab have
    also their channel.
-   You can have a fresh view of the latest official git
    documentation at
    [Gitweb access to the Documentation folder of the git *git* repository
    ](http://git.kernel.org/?p=git/git.git;a=tree;f=Documentation;hb=HEAD).


## manuals

-   [Git User Manual
    ](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html)
-   [Git manual page
    ](https://www.kernel.org/pub/software/scm/git/docs/)
    which reference all other manual pages.
-   [Git Reference index](https://git-scm.com/docs)
    at [git-scm.com](https://git-scm.com/)
-   [git-scm.com](https://git-scm.com/) also host
    [Git User Manual](https://git-scm.com/docs/git)
    along with the
    [Git manual page](https://git-scm.com/docs/git)
    with a different formatting than the kernel.org raw layout.
-   [Git magic](http://www-cs-students.stanford.edu/~blynn/gitmagic/)
    by Ben Lynn is a Git Manual, lighter than the official manual. The
    [asciidoc source is available in GitHub
    ](https://github.com/blynn/gitmagic) or
    [repo.or.cz](http://repo.or.cz/w/gitmagic.git)
-   [Pro Git](http://git-scm.com/book) by Scott Schacon and als
    is a very complete book. It covers many new features of git.
    The previous _Git Community Book_ has been merged with
    _Pro Git_ in 2012, and is now deprecated..
    -   [source repository](https://github.com/progit/progit).
    -   [Scott Schacon GitHub Repositories](https://github.com/schacon)
    -   [Scott Schacon Home Page](http://schacon.github.io/).
-   [Git in a Nutshell](http://jonas.iki.fi/git_guides/HTML/git_guide/)
    by Jonas Jusélius summarize most of git tasks including branch
    management with remote directory and merge conflict solving. _last
    update 2008_ the html version seems non longer available but the
    [source is on GitHub](https://github.com/bakerjonas/git-guides).

## Tutorials, recipes, tips
### Official Tutorials

-   [git tutorial
    ](https://www.kernel.org/pub/software/scm/git/docs/gittutorial.html)
    covers the basics.
-   [Everyday Git
    ](https://www.kernel.org/pub/software/scm/git/docs/everyday.html)
    handbook gives set of commands and the workflow for any developer.
-   [A tutorial introduction to git: part two
    ](https://www.kernel.org/pub/software/scm/git/docs/gittutorial-2.html)
    introduce to the structure of a git repository.
-   [Gitcore-tutorial
    ](https://www.kernel.org/pub/software/scm/git/docs/gitcore-tutorial.html)
    explains how to use the "core" git programs to set up and work with
    a git repository.
-   [Git Tips](https://git.wiki.kernel.org/index.php/GitTips)
-   [Git FAQ](https://git.wiki.kernel.org/index.php/GitFaq)

### Git internals
-   [Git from the bottom up (pdf)
    ](http://ftp.newartisans.com/pub/git.from.bottom.up.pdf)
    by John Wiegley _2009_ explain git starting from the repository
    structure.
-   [Tommi Virtanen (Tv)](http://eagain.net/)
    has  written an introduction to git internals
    [Git for Computer Scientists
    ](http://eagain.net/articles/git-for-computer-scientists/)
-   Sitaram Chamarty version
    [git for computer scientists](http://gitolite.com/gcs.html)
    is an expanded version (detached heads, reflog ...) of the
    one from Tommi Virtanen.

### Other tutorials
-   Some other resources are in the the
    [Git documentation](http://git-scm.com/documentation).
-   GitHub [Git reference](http://git.github.io/git-reference/)
    ([source](https://github.com/git/git-reference)).
-   [GitHub Help](https://help.github.com/en)
    give many guides on either Git topics under the section
    [using Git](https://help.github.com/en/github/using-git) or the GitHub use.
-   [Ry’s Git Tutorial
    ](https://web.archive.org/web/20161121145226/http://rypress.com:80/tutorials/git/index)
    a detailed introduction to the entire Git porcelain _2012_.
-   [A tour of git: the basics](http://cworth.org/hgbook-git/tour/)
    a complete tutorial, more verbose and aimed at beginners,
    _2007_ by  Bryan O'Sullivan and Carl D. Worth.
-   Lars Vogel has many git tutorials, including:
    -   [Git
        ](http://www.vogella.com/tutorials/Git/article.html) _2018_
    -   [Using submodules
        ](http://www.vogella.com/tutorials/GitSubmodules/article.html)
        _2015_
    -   [Git typical workflows
        ](http://www.vogella.com/tutorials/GitWorkflows/article.html)
        _2016_.
-   [Kernel Hackers' Guide to git](http://linux.yyz.us/git-howto.html)
    by Jeff Garzik is a short and easy *but not over-easy*, tutorial.
    _2008_.
-   Denx [Basic git Commands
    ](http://www.denx.de/en/Documents/GitBasicCommands),
    and [Using git (advanced commands)
    ](http://www.denx.de/en/Documents/GitAdvancedUse),
    are tutorials coverring complex branch management
    (*They are related to a previous state of git (2005)
    so they use more plumbing commands that it would be necessary today*).
-   [GitCasts](http://www.gitcasts.com) present is a
    repository of git podcasts.
-   [git ready](http://gitready.com/) is a collection of short git tips.
-   [A Visual Git Reference
    ](http://marklodato.github.com/visual-git-guide/index-en.html)
    for the most common commands in git, by Mark Lodato _2010_.
    _[French translation
    ](http://marklodato.github.com/visual-git-guide/index-fr.html)_
    -   [visual-git-guide GitHub Repository
        ](https://github.com/MarkLodato/visual-git-guide)
        is an interesting use-case of latex-TkiZ.
-   [Seth Robertson's tutorials](http://sethrobertson.github.io/):
    -   [Git Best Practices
        ](http://sethrobertson.github.io/GitBestPractices/)
        followed by
        [Post-Production Editing using Git
        ](http://sethrobertson.github.io/GitPostProduction/gpp.html)
        _2012_
    -   [On undoing, fixing, or removing commits
        ](http://sethrobertson.github.io/GitFixUm/fixup.html) _2012_.

### Blogs and notes
-   [Junio C. Hamano old blog](http://gitster.livejournal.com/) _until 2011_
    and [new blog](http://git-blame.blogspot.fr/) _2011-2016_.
-   [Git Notes](http://gitolite.com/index2.html)
    ( [GitHub repository](https://github.com/sitaramc/git-notes) )
    by Sitaram Chamarty, a set of various notes
    with a useful not so common documentation on
    commands like _reflog_, _grafting_, __pull --rebase__, ...
    <br />
    It includes a very useful [git as a deployment tool
    ](http://gitolite.com/deploy.html).
    He is also author of a version of
    [git for computer scientists](http://gitolite.com/gcs.html).
-   [Git cookbook](https://git.seveas.net/) by Dennis Kaarsemaker is a collection of
    recipes for using git.
-   Martin f. Krafft *(madduck)* has written
    [Packaging with Git](http://madduck.net/blog/2007.10.03:packaging-with-git/)
    followed by
    [Converting a package to Git
    ](http://madduck.net/blog/2007.10.07:converting-a-package-to-git/)
    _The madduck blog seems no longer available, while his
    [git.madduck.net](https://git.madduck.net/) and
    [GitHub Repository](https://github.com/madduck)_ are still active._
-   [Packaging With Git - Debian Wiki](https://wiki.debian.org/PackagingWithGit)
-   [Git Developer Pages](https://git.github.io/)

## Git cheatsheets
-   [Git Cheat Sheet & Git Flow
    ](https://github.com/arslanbilal/git-cheat-sheet)
-   [Git Tips](https://github.com/git-tips/tips)
-   Zack Rusin's [git cheat sheet
    ](http://zrusin.blogspot.com/2007/09/git-cheat-sheet.html)
    [available in svg
    ](http://byte.kde.org/~zrusin/git/git-cheat-sheet.svg)
    ([saved copy
    ](http://www.cheat-sheets.org/saved-copy/git-cheat-sheet.svg)),
    [pdf](http://www.cheat-sheets.org/saved-copy/git-cheat-sheet.pdf),
    [medium png
    ](http://byte.kde.org/~zrusin/git/git-cheat-sheet-medium.png)
    and
    [large png
    ](http://byte.kde.org/~zrusin/git/git-cheat-sheet-large.png)
    ([saved copy
    ](http://www.cheat-sheets.org/saved-copy/git-cheat-sheet-large.png));
    -   Zack Rusin Git Cheat Sheet
        [expanded version by Pierre-Alexandre St-Jean (svg)
        ](https://rawgit.com/pastjean/git-cheat-sheet/master/git-cheat-sheet.svg)
        ([source](https://github.com/pastjean/git-cheat-sheet))
    -   Zack Rusin Git Cheat Sheet [extended edition by Jan Krueger
        ](http://jan-krueger.net/development/git-cheat-sheet-extended-edition).
-   [GitHub : Git cheat sheet
    ](https://github.github.com/training-kit/downloads/github-git-cheat-sheet/),
    [Github : git cheat sheet (pdf)
    ](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf)
    reference some other cheat sheets and give a git memo.
-   [Magit Cheatsheet](http://daemianmack.com/magit-cheatsheet.html)
    has its'
    [org source in GitHub
    ](https://github.com/daemianmack/magit-cheatsheet).
-   [Alvin  Alexander: A Git cheat sheet
    ](http://alvinalexander.com/git/git-cheat-sheet-git-reference-commands)
    elementary cheatsheet
-   [Bilal Arslan -  git and git flow cheat sheet
    ](https://github.com/arslanbilal/git-cheat-sheet)  written in Markdown.
-   [git-tips - Most commonly used git tips and tricks
    ](https://github.com/git-tips/tips)

# Language bindings
-   [Git Wiki - Interfaces to other programming languages
    ](https://git.wiki.kernel.org/index.php/Interfaces,_frontends,_and_tools#Interfaces_to_other_programming_languages)

-   [Dulwich](http://samba.org/~jelmer/dulwich/) is a pure-Python
    read-write implementation of the Git file formats and protocols.
    _active in 2018._
    [Dulwich Tutorial](http://samba.org/~jelmer/dulwich/tutorial).
-   [GitPython](http://gitpython.readthedocs.io/en/stable/) (BSD License)
    is a python (2 or 3) library used to interact with git
    repositories, high-level like git-porcelain, or low-level like
    git-plumbing.  It provides object model access to your git
    repository. _active in 2018_.
    -   [GitPython tutorial
        ](http://gitpython.readthedocs.io/en/stable/tutorial.html)
        is part of the documentation.
   -   [GitHub: GitPython
       ](https://github.com/gitpython-developers/GitPython).
-   [libgit2](http://libgit2.github.com/)
    is a portable, pure C implementation of the Git core methods provided
    as a re-entrant linkable library. It has
    [Binding to a lot of languages
    ](http://libgit2.github.com/#bindings) python, lua, node, go,
    erlang, gobject, ruby, objective-c .... and gives
    [many code samples
    ](https://libgit2.github.com/docs/guides/101-samples/)
    _active in 2018;_
    -   [GitHub: libgit2
        ](https://github.com/libgit2/libgit2)
    -   [Pygit2](http://www.pygit2.org/) ([GitHub
    ](https://github.com/libgit2/pygit2)) is the python binding
    (with py3k support).

# Repository management
-   First you can set your own server, it is the simpler when you have
    few users and not to manage authentication protocol, it is the
    subject of
    [Pro Git: Git on the server
    ](https://git-scm.com/book/en/v2/Git-on-the-Server-The-Protocols)
-   [gitdir](https://github.com/belak/gitdir) (MIT Licence)
    by Kaleb Elwert _belak_, a secure git server written in Go.
-   [Gitosis](http://eagain.net/gitweb/?p=gitosis.git)
    by Tommi 'Tv' Virtanen is a Python tool to manage git repositories,
    provide access to them over SSH, with tight access control and not
    needing shell accounts. It is discussed in
    [Hosting Git repositories, The Easy (and Secure) Way
    ](http://scie.nti.st/2007/11/14/hosting-git-repositories-the-easy-and-secure-way),
    2007 with a 2010 comment:
    >> For additional features not present in gitosis, check out gitolite.
    -   [Arch Linux: Gitosis
    ](https://wiki.archlinux.org/index.php/Gitosis),
    -   [Pro Git v1: Gitosis
        ](https://git-scm.com/book/en/v1/Git-on-the-Server-Gitosis).
-   <a name="gitolite"></a>[Gitolite
    ](https://github.com/sitaramc/gitolite) (GPL)
    by Sitaram Chamarty is an enhancement of Gitosis. It add per-branch permissions.
    It is written entirely in perl, and doesn't require root access.<br />
    Tutorials:
    -   [Pro Git v1: Gitolite
    ](https://git-scm.com/book/en/v1/Git-on-the-Server-Gitolite),
    -   [Gitolite Tutorial
    ](http://sites.google.com/site/senawario/home/gitolite-tutorial)
    by Sena Wario,
-   [Gitlab](https://github.com/gitlabhq/gitlabhq) (MIT)
    is a git repository management application based on Ruby on Rails.
    It uses ruby, redis and a sgbd either MySQL, MariaDB or
    PostgreSQL. It needs at least 1GB Memory for up to 100 users.
    -   [Pro Git: Gitlab
        ]( https://git-scm.com/book/en/v2/Git-on-the-Server-GitLab)
    -   [ArchWiki: Gitlab](https://wiki.archlinux.org/index.php/gitlab)
    -   [Gentoo Wiki:Gitlab](http://wiki.gentoo.org/wiki/GitLab)
-   [Gogs](https://gogs.io/) (MIT)
    is a self-hosted Git service written in Go.
    -   [GitHub - Gogs](https://github.com/gogits/gogs).
    -   Demo site [try.gogs](https://try.gogs.io/).
    -   [ArchWiki - Gogs](https://wiki.archlinux.org/index.php/Gogs).
-   [Gitea](https://gitea.io/) (MIT)
    is a community managed fork of Gogs.
    -   [GitHub - Gitea](https://github.com/go-gitea/gitea)
    -   [ArchWiki: Gitea](https://wiki.archlinux.org/index.php/Gitea)

# front-end layers
## Git extensions
The {{< iref "backup#git_backup" "git backup tools" >}} are in the
{{< iref "backup" "Backup Page" >}}.

-   [EtcKeeper](http://etckeeper.branchable.com/) (GPL)
    is a collection of tools to let /etc be stored in a git repository. It hooks into
    apt to automatically commit changes made to /etc during package upgrades.
-   [IsiSetup](http://sourceforge.net/projects/isisetup/) is an
    utility for managing configuration files using git as backend
    _last activity 2006_.
-   [etcgit](http://git.debian.org/?p=users/jo-guest/etcgit.git)
    from Jörg Sommer is an alternative to etckeeper that records the
    original package configuration in one branch and your changes in
    another one _not updated since 2009_.
-   _Git_cache_meta_ is a shell script to register the file mode that is not handled by
    Git _except the execution bit_. There is many version of this script like
    [arno01 git_cache_meta.sh
    ](https://gist.github.com/andris9/1978266#gistcomment-1599650)
    or [danny0838 git_cache_meta.sh
    ](https://gist.github.com/danny0838/fb475658c73be6fe51a2) and a perl version
    [danny0838/git-store-meta](https://github.com/danny0838/git-store-meta)
    (MIT License).
-   [przemoc/metastore](https://github.com/przemoc/metastore) (GPL)
    Store and restore metadata from a filesystem.
-   [zit](http://git.oblomov.eu/zit/blob/HEAD:/zit)
    is a bash script used to track single files within a directory
    like RCS does but using git.

## Git LFS {#git_lfs}
[Git LFS (large file systems)](https://git-lfs.github.com/) Is a git extension for
versioning large files developped by GitHub and also Available on Bitbucket and GitLab.
-   [GitHub Git-lfs repository](https://github.com/github/git-lfs)
    Every account using Git Large File Storage receives 1 GB of free storage and 1 GB a
    month of free bandwidth.

    You can purchase [additionnal data packs
    ](https://help.github.com/en/articles/upgrading-git-large-file-storage#purchasing-additional-storage-and-bandwidth-for-a-personal-account)
    for 5$/month for 50 GB of bandwidth and 50 GB for storage.

-   [BitBucket Git-lfs
    ](https://confluence.atlassian.com/bitbucket/git-large-file-storage-in-bitbucket-829078514.html)
    is available with 1GB free for free personnal account, and 10$/month for 100 GB.
-   [GitLab Git LFS
    ](https://docs.gitlab.com/ee/workflow/lfs/manage_large_binaries_with_git_lfs.html),
    [GitLab Git LFS Administration
    ](https://docs.gitlab.com/ee/workflow/lfs/lfs_administration.html#storing-lfs-objects-in-remote-object-storage)
    allow storing lfs objects on external resources. If you use the hosted Gitlab.com
    the [global repository size limit
    ](https://docs.gitlab.com/ee/user/gitlab_com/index.html#repository-size-limit)
    includes lfs and is 10 GB.
-   There is an official [list of git-lfs implementation
    ](https://github.com/git-lfs/git-lfs/wiki/Implementations), but most of them are
    unmaintained or speak the deprecated v1 protocol. Among recent servers
    [The reference LFS Test Server](https://github.com/git-lfs/lfs-test-server) in go
    language, and [rudolfs](https://github.com/jasonwhite/rudolfs) a high-performance,
    caching Git LFS server with an AWS S3 back-end, with a tiny (<10MB) Docker image.
-   Alternatives to git-lfs: {{< iref "#git-annex" >}}, git-bigfiles _unmaintained_,
        [git-fat](https://github.com/jedbrown/git-fat), git-media _unmaintained_,
        [git-bigstore](https://github.com/lionheart/git-bigstore),
        [git-sym](https://github.com/cdunn2001/git-sym).
-   <a name="git-annex"></a>[git-annex](http://git-annex.branchable.com/) by Joey Hess
    manage files with git, without checking their contents into git.
    -   [GitHub: git-annex](https://github.com/joeyh/git-annex)
    -   [sharebox](https://github.com/chmduquesne/sharebox-fs)
        is a distributed FUSE filesystem for sharing
        files across several machines based on git-annex.
    -   [git annex walkthrough
        ](http://git-annex.branchable.com/walkthrough/)
    -   [NeuroDebian git-annex standalone packages
        ](http://neuro.debian.net/pkgs/git-annex-standalone.html)
        package a very recent version of git-annex.

## Emacs Interfaces {#emacs_git}
Many Emacs modes are available for Git; For a detailed review of the
emacs front ends, look at
[Work with Git from Emacs](http://alexott.net/en/writings/emacs-vcs/EmacsGit.html)
from Alex Ott; and the
[Emacs Wiki Git page](http://www.emacswiki.org/emacs/Git).<br />
[Work with Git from Emacs](http://alexott.net/en/writings/emacs-vcs/EmacsGit.html)
provides a detailled description of the use of the following packages.

-   __vc-git.el__ hich is the Emacs VC backend, is now part of the emacs distribution (since emacs-22).
    The use of _vc_ is described in the
    [Version Control chapter of the Emacs manual](http://www.gnu.org/software/emacs/manual/html_node/emacs/Version-Control.html)
-   [git.el](http://www.kernel.org/git/?p=git/git.git;a=blob;hb=HEAD;f=contrib/emacs/git.el)
    from Alexandre Julliard is distributed with _git-core_ and part of emacs.
    The entry point is the command 'git-status'.<br />
    The package
    [egit.el](http://github.com/jimhourihan/egit)
    gives an interface to git commands which are not
    part of git.el. Primarily, this is a view of the git commit
    history with the ability to mark ranges and/or single commits and
    operate on them..
-   [git-emacs](http://files.taesoo.org/git-emacs/git-emacs.html) has almost the same functionality, as the git.el package, and it add some improvements.<br />
    [git-emacs repository](https://github.com/tsgates/git-emacs) at [github](https://github.com/)
-   <a name="magit"></a>[Magit](http://philjackson.github.com/magit)
    by Marius Voller and Phil Jackson has an online
    -   [Magit Manual](http://magit.github.io/master/magit.html),
    -   [Magit Cheatsheet](http://daemianmack.com/magit-cheatsheet.html)
        has its'
        [org source in GitHub](https://github.com/daemianmack/magit-cheatsheet).
-   [Egg](http://github.com/byplayer/egg) is a fork of magit. An
    [introduction to Egg](http://bogolisk.blogspot.com/2009/01/introduction-to-egg.html)
-   <a name="git-wip"></a>[git-wip](https://github.com/bartman/git-wip) (GPL)
    by Bart Trojanowski  is a script that will manage Work
    In Progress (or WIP) branches. It includes hooks for vim and
    emacs.
-   [magit-wip
    ](https://github.com/magit/magit/blob/master/magit-wip.el)
    is a magit plugin included in {{< iref "#magit" "magit distribution" >}} which add two modes to emacs.
    The global mode _magit-wip-mode_ provides highlighting of wip refs in
    Magit buffers while the local mode _magit-wip-save-mode_
    commits to such a ref when saving a file-visiting buffer.
-   <a name="ediff"></a>[Ediff (UserManual)
    ](http://www.gnu.org/software/emacs/manual/html_node/ediff/)
    is an emacs visual interface to Unix diff and patch utilities.
    It is an improvement of the emerge package.
-   <a name="emerge"></a>[Emerge
    ](https://www.gnu.org/software/emacs/manual/html_node/emacs/Emerge.html)
    is the emacs merge utility. The Emerge commands compare two files
    or buffers, but in contrast to ediff use a third buffer. In ediff
    it is also provided by the command ediff-merge.
    (the merge buffer) where merging takes place.
-   <a name="vdiff"></a>[vdiff](https://github.com/justbur/emacs-vdiff)
    by Justin Burkett, is a diff tool that display diff information in
    buffers as you edit them, like vimdiff does.
    It has also a magit interface which replace ediff by vdiff in
    magit: [vdiff-magit](https://github.com/justbur/emacs-vdiff-magit).
    vdiff and vdiff-magit are in melpa.

## Git Fuse filesystems

-   [Git Wiki -  Filesystem interfaces
    ](https://git.wiki.kernel.org/index.php/Interfaces,_frontends,_and_tools#Filesystem_interfaces)

-   [figfs](http://www.qotw.net/~reillyeon/projects/figfs/) (GPL)
    from Reilly Grant. _last update 2009_. A fuse fs written in Ocaml/sqlite3,
    _figfs_ allows to browse branchs, tags, and revisions.
    [GitHub Repository](https://github.com/reillyeon/figfs).
-   [pygitfs (GitHub)](https://github.com/tv42/pygitfs) (MIT License)
    by Tommi Virtanen is a pythonic filesystem API to Git, allowing
    you to access contents of bare git repositories, including
    creating new commits.
    It is a python library, exposing an API, with no command line frontend
    included, the last release is from 2009.  [pygitfs is in Pypi
    ](https://pypi.python.org/pypi/gitfs).
-   [legitfs (GitHub)](https://github.com/mbr/legitfs) (MIT License)
    a read-only fuse filesystem written in python.
    [legitfs is on pypi](https://pypi.python.org/pypi/legitfs/).

## Patch management
-   [Quilt](http://savannah.nongnu.org/projects/quilt "savannah.nongnu.org quilt")
    scripts allow to manage a series of patches by keeping track of the
    changes each patch makes. It is described in this
    [Introduction to Quilt](http://www.suse.de/~agruen/quilt.pdf) by
    Andreas Grünbacher.
-   [Stacked Git - Stgit](http://www.procode.org/stgit/)
    provides a *Quilt*-like patch management functionality in the Git
    environment.
-   [TopGit](https://github.com/greenrd/topgit)
    aims to make handling of large amounts of interdependent topic
    branches easier. It is designed for the case where
    you maintain a queue of third-party patches on top of another (perhaps
    Git-controlled) project. Topgit can be used from
    {{< iref "#magit" "Magit" >}}.

## Graphic Interfaces

I don't list all of them here, find them with a feature matrix at
[GitWiki: Graphical Interfaces
](https://git.wiki.kernel.org/index.php/InterfacesFrontendsAndTools#Graphical_Interfaces).
the Git Wiki [list also the Web interfaces
](https://git.wiki.kernel.org/index.php/Interfaces,_frontends,_and_tools#Web_Interfaces).

-   [gitk](https://www.kernel.org/pub/software/scm/git/docs/gitk.html) and
    [git gui](http://www.kernel.org/pub/software/scm/git/docs/git-gui.html)
    are Tcl/Tk GUI for git distributed with git. _gitk_ is useful for
    browsing history, diff, and trees; while _git_gui_ is mainly a
    commit tool.
    -   [The missing gitk documentation
         ](http://gitolite.com/gitk.html).
-   [tig](http://jonas.nitro.dk/tig/) is a git repository browser
    written using
    ncurses. [tig-manual](http://jonas.nitro.dk/tig/manual.html),
    [GitHub: tig](https://github.com/jonas/tig).
    [tig user manual](http://jonas.nitro.dk/tig/manual.html)
-   [QGit](http://digilander.libero.it/mcostalba/) (GPL) uses Qt toolkit
-   [Giggle](https://wiki.gnome.org/Apps/giggle) (GPL)  uses GTK+/Gnome toolkit
-   [git-cola](http://cola.tuxfamily.org/) (GPL) uses PyQt4.
    [git-cola documentation
    ](http://git-cola.github.io/share/doc/git-cola/html/index.html)
-   [gitg](http://git.gnome.org/cgit/gitg/) (GPL) GTK+/Gnome clone of
    the mac/OS gui _GitX_.
-   [GitForce](https://sites.google.com/site/gitforcetool/home) (GPL)
    written in C#.
-   [GitWeb](https://git.wiki.kernel.org/index.php/Gitweb) distributed with Git,
    is a web interface written in Perl.
-   [Klaus](https://github.com/jonashaag/klaus) (BSD License)
    by Jonas Haag is a Git web viewer written in python.
    [Pypi Klaus](https://pypi.python.org/pypi/klaus/).
-   [Agit](https://github.com/rtyley/agit/wiki) (GPL) is a 'read-only'  android client for git.
    It can clone a repository and explore history, presently you cannot commit or push.
-   [Git Extensions](http://gitextensions.github.io/)
    is a graphical user interface for Git that allows you control Git without using the commandline.
    _what a big Deal!_

# Tools
-   [Git Wiki - Tools
    ](https://git.wiki.kernel.org/index.php/Interfaces,_frontends,_and_tools#Tools)

## Commit
-   See {{< iref "#git-wip" "git-wip" >}} above.
-   [gitwatch](https://github.com/gitwatch/gitwatch) (GPL)
    A bash script to watch a file or folder and commit changes to a git repo.
    I uses _inotify_ to watch for changes.

## Sensitive information
-   [git-remote-gcrypt
    ](https://spwhitton.name/tech/code/git-remote-gcrypt/)
    is a git remote helper to push and pull from repositories
    encrypted with GnuPG. It works with the standard git transports,
    including repository hosting services like GitHub. There is a
    Debian package.

    Supported locations are `local`, `rsync://` and `sftp://`, where
    the repository is stored as a set of files, or instead any
    `<giturl>` where gcrypt will store the same representation in a
    git repository, bridged over arbitrary git transport.

    Using an arbitrary `<giturl>` or an `sftp://` URI requires
    uploading the entire repository history with each push.  The
    `rsync://` transport _(not git rsync!)_, performs incremental
    pushes.
    -   [source mirror on GitHub
        ](https://github.com/spwhitton/git-remote-gcrypt)
-   [git-crypt](https://www.agwa.name/projects/git-crypt/)
    is a C++ program that enables transparent encryption and decryption
    of files in a git repository. You can choose files which are
    encrypted when committed, and decrypted when checked out.  This
    lets you store your secret material (such as keys or passwords) in
    the same repository as your code, without requiring you to lock
    down your entire repository.
-   [git secret](http://git-secret.io/)
    is a bash script which stores gpg encrypted credential inside
    source code git repository.

    _git secret_ is similar to _git-crypt_, but written as a script
    while git-crypt is a binary program. _git-crypt_ also has an has
    an option to export a symmetric key, that is not available in
    _git-secret_.  With _git-secre_t you can simply encrypt/decrypt
    files with gpg commands which is [harder with git-crypt
    ](https://github.com/AGWA/git-crypt/issues/99#issuecomment-270179200).

-   [Blackbox](https://github.com/StackExchange/blackbox) (MIT)
    is a bash suite of utilities to gpg encrypt secrets in a VCS repo
    (i.e. Git, Mercurial, Subversion or Perforce). Blackbox allow
    collaboration by allowing to retreive the secrets files with the
    gpg key of each registered user.
-   [transcrypt](https://github.com/elasticdog/transcrypt) (MIT)
    is a bash script to provide transparent encryption of sensitive
    files stored in a git directory. Sensitive files are recognized by
    a  `.gitattributes` filter pattern.
-   [Keyringer](https://keyringer.pw/) (GPL)
    lets you manage and share secrets using GnuPG and Git in
    a distributed fashion. It has custom commands to encrypt, decrypt
    and recrypt secrets as well as create key pairs and supports
    encryption to multiple recipients and groups of different
    recipients. Keyringer is in Debian.
    -   [keyringer source](https://git.fluxo.info/keyringer/)


## File systems synchronization {#fs_synch}
See also {{< iref "backup#synchronization" "Synchronization" >}} in the
{{< iref "backup" "Backup Section" >}}.

-   [SparkleShare](http://www.sparkleshare.org/) is a collaboration and sharing tool
    that uses a git repository backend.  It is written in mono and uses libnotify (with
    python and dbus services) to monitor files so it has quite heavy dependencies.
    [Source code](http://github.com/SparkleShare/),
    [SparkleShare Wiki](http://github.com/hbons/SparkleShare/wiki/).
-   [DVCS-Autosync](http://mayrhofer.eu.org/dvcs-autosync)
    is a lighter alternative to SparkleShare.  It watch files and folders in specified
    paths and sync them in a git or mercurial repository.  It needs pynotify (python),
    xmppy and a provided patched JabberBot. The project has a very low activity _last
    release november 2019_, nevertheless the maintainer indicates it can accept pull
    requests.
    -   [dvdautosync - GitHub](https://github.com/rmayr/dvcs-autosync).
-   [git-sync](https://github.com/ianb/git-sync)
    by Ian Bicking is a git deployement script.
-   Tychoish _Sam Kleinman_ uses [a script to synchronize git repositories
    ](https://gist.github.com/tychoish/f73efe9825dd691369b9), he explained its
    [use in his blog](https://tychoish.com/post/git-sync/).

## Diff
-   The diffutils package provides the diff, diff3, sdiff, and cmp
    programs.  These utilities are explained in
    [GNU Diffutils Manual - Comparing and Merging Files
    ](http://www.gnu.org/software/diffutils/manual/diffutils.html)
-   [wdiff](http://www.gnu.org/software/wdiff/)
    is a front end to diff for comparing files on a word
    per word basis. It defines a word as anything between whitespace.
    It is  useful for comparing two texts in which a few words have
    been changed and for which paragraphs have been refilled. In
    Debian it is in its own wdiff package.
-   [dwdiff](http://os.ghalkes.nl/dwdiff.html)
    is an a compatible alternative to wdiff that allows to specify
    what characters should be considered delimiters.
-   The Perl script [colordiff](http://www.colordiff.org/)
    is a wrapper for 'diff' and produces pretty syntax highlighting.
-   [diffstat](http://invisible-island.net/diffstat/diffstat.html)
    reads the output of diff and displays a histogram of the
    insertions, deletions, and modifications per-file.  It is
    incorporated in git but the standalone version is still very
    useful for reviewing large, complex patch files.
-   [Git - git-difftool](http://git-scm.com/docs/git-difftool/)
    allows you to compare and edit files between revisions
    using common diff tools.

## Visual diff utilities
See {{< iref "#ediff" "above for emacs frontends" >}}:
{{< iref "#ediff" "ediff" >}},
{{< iref "#emerge" "emerge" >}},
{{< iref "#vdiff" "vdiff" >}}.

-   [Diffoscope](https://diffoscope.org/) (GPLv3)
    is a files or directories python comparison tools, it can
    recursively unpack archives of many kinds and transform various
    binary formats into  human readable form. It can compare two
    tarballs, ISO images, or PDF. The differences can be shown in a
    text or HTML report. There is also a command line client to the
    hosted version of diffscope
    [trydiscope](https://github.com/lamby/trydiffoscope)
    both diffscope and trydiffscope are in Debian.
-   [Diffuse](http://diffuse.sourceforge.net/) (GPL)
    is a diff GUI tool written in python. Diffuse can
    retrieve revisions of files from Bazaar, CVS, Darcs, Git,
    Mercurial, Monotone, RCS, Subversion, and SVK repositories
    for comparison and merging. Diffuse is in Debian.
    [Diffuse Manual](http://diffuse.sourceforge.net/manual.html)
-   [Meld](http://meldmerge.org/) is a visual diff and merge tool
    that supports Git, Bazaar, Mercurial, Subversion, etc and can be
    used with git mergetool.
    -   [Meld Manual](http://meldmerge.org/help/)
    -   [Meld keyboard Shortcuts
        ](http://meldmerge.org/help/keyboard-shortcuts.html)
-   [Pretty Diff](https://github.com/prettydiff/prettydiff/)
    (Creative Commons Zero License)
    is a language aware javascript comparison tool. It also beautifies,
    minifies. It can run as a stand alone node.js application or
    in Atom code editor with the [atom-beautify
    ](https://atom.io/packages/atom-beautify)
    package inside the browser.
    -   [Pretty Diff Online Interface](http://prettydiff.com/)
    -   [Pretty Diff Documentation
        ](http://prettydiff.com/documentation.xhtml)
-   [tkdiff](http://sourceforge.net/projects/tkdiff/)
    is a gui for diff written in TK that provides a
    side-by-side diff view.
-   [xxdiff](http://furius.ca/xxdiff/) (GPL)
    is a graphical file and directories comparator and merge tool.
    It is in the Debian package xxdiff.
    There is also a set of [helper scripts
    http://furius.ca/xxdiff/doc/xxdiff-scripts.html)
    in the package xxdiff-scripts.

### vimdiff
-   [vimdiff manual](http://vimdoc.sourceforge.net/htmldoc/diff.html)
-   [Use vimdiff as git mergetool
    ](http://www.rosipov.com/blog/use-vimdiff-as-git-mergetool/)


To open files and diff:

    vimdiff file1 file2

or

    vim -d file1 file2

vertical splits is the default or can be given explicitely:

    vimdiff -O file1 file2

horizontal splits with

    vimdiff -o file1 file2

You can compare two, three or four versions:

    vimdiff file1 file2 [file3 [file4]]

or

    vim -d file1 file2 [file3 [file4]]

Keyboard Shortcuts

-   do - Get changes from other window into the current window.
-   dp - Put the changes from current window into the other window.
-   ]c, [c   - Jump to the next/previous change.
-   Ctrl W + Ctrl W - Switch to the other split window.
-   Ctrl Wh, Ctrl Wj, Ctrl Wk, Ctrl Wl switch to window left, down, up, right
-   :diffupdate - diff update
-   :syntax off - syntax off
-   zo, zc - open/ce folded text
-   :ls - window info

When used as a git mergetool you get the following windows:

-   Upper-Left - The local/target branch
-   Upper-Center -  The most common ancestor
-   Upper-Right - The remote/merge branch
-   Bottom - The product of this merge operation


## Misc
-   [GitStats](http://gitstats.sourceforge.net/) (GPL)
    generates statistics for git,
-   [Pepper](http://scm-pepper.sourceforge.net/) (GPL)
    generates statistics for git, mercurial and Subversion.
-   [octogit](https://github.com/myusuf3/octogit/) (MIT License)
    by Mahdi Yusuf
    is a python command line interface to github.
-   [reposurgeon](https://gitlab.com/esr/reposurgeon)
    by Eric S. Raymond is a tool for editing version-control
    repositories and translating among different systems. Supports
    git, bzr, Subversion, darcs, and fossil directly, also hg, CVS,
    and RCS through plugins.


# Git Workflow {#git_worflow}
## What are git workflows
There are a great number of species of git workflows with their
varieties each one having multiple forms. To have a taste of if you
can begin with the [Chapter 5 of Pro Git: Distributed Git
](http://git-scm.com/book/en/Distributed-Git).

In the same way than the {{< wp "Species problem" >}} in biology git workflows
is a controversial subject, with his proponents of eugenics an genetic
diversity defensors.

A lot of people publish on the web their git workflow.
 But all of them don't use git in the same context.
Some are individual developers, some other maintain
a big project with many contributors....

In any case it is useful to read about experimented people practice.
They met traps, either by themselves, or have observed pitfalls
in other practices and their advice can avoid to expose
ourself or our friends to the same traps.

## Basis of git worflow
A good introduction is the [previously cited chapter
](http://git-scm.com/book/en/Distributed-Git)
of the book of Scott Chacon, then
the secure basis for our workflow seems to lie in the git documentation: the
[Git Manual](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html),
[Everyday GIT](https://www.kernel.org/pub/software/scm/git/docs/everyday.html)
and [gitworflows](https://www.kernel.org/pub/software/scm/git/docs/gitworkflows.html)
based on the understanding of
[git-merge](https://www.kernel.org/pub/software/scm/git/docs/git-merge.html)
and [git-rebase](https://www.kernel.org/pub/software/scm/git/docs/git-rebase.html).
The [git wiki: GitWorkflows
](https://git.wiki.kernel.org/articles/g/i/t/GitWorkflows_d0c8.html)
gives useful tips.
Personally I have to refer to them again and again to them when I feel
to switch to a more fashionable workflow.

## Git-Flow
[A successful Git branching model
](http://nvie.com/posts/a-successful-git-branching-model/)
is Vincent Driessen's branching model. He has written
[git-flow](https://github.com/nvie/gitflow)
a git extensions to provide high-level repository operations along this model.

Benjamin Sandofsky in
[Understanding the Git Workflow](http://sandofsky.com/blog/git-workflow.html)
warn us against the overuse of non fast forward merges used in Vincent
Driessen's model _because it breaks bisect and blame_ mainly when
merging raw checkpoints, and advise to prefer a squash merge for short
developments or a rebase of the topic branch before merge.

Scott Chacon
[GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
points out the advantages of *git-flow*
> A flexible workflow that works for lots of developers in a fairly straightforward manner

He speaks also some of its issues and why GitHub uses a much simpler
Git workflow.

This GitFlow has also been tweaked for GitHub with
[HubFlow](http://datasift.github.io/gitflow/)
this topic is also discussed by Pedro Melo in
[Flow setups for git
](http://www.simplicidade.org/notes/archives/2012/09/flow_setups_for.html).

## Merge or rebase
Vincent Driessen's git-flow use heavily merges at many levels.

The [Git Manual
](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html)
explains
[why bisecting merge commits can be harder than bisecting linear history
](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html#bisect-merges)
and concludes:

> many experienced git users, even when working on an otherwise
> merge-heavy project, keep the history linear by rebasing against the
> latest upstream version before publishing.

The [Git Workflow for Agile Teams
](http://reinh.com/blog/2009/03/02/a-git-workflow-for-agile-teams.html)
show also how to rebase before merge. Randy Fay take the same approach with
[A Rebase Workflow for Git](http://randyfay.com/node/91) this two posts are from 2009
and 2011.

As Randy Fay noted later the present way of acting is with
[pull requests](https://help.github.com/articles/about-pull-requests/)
used in [GitHub workflow
](https://help.github.com/articles/github-flow/)
and detailed in the pages from
[Proposing changes to your work with pull requests
](https://help.github.com/articles/proposing-changes-to-your-work-with-pull-requests/)

Kumar McMillan's
[Using topic branches and interactive rebasing effectively
](http://blog.mozilla.com/webdev/2011/11/21/git-using-topic-branches-and-interactive-rebasing-effectively/)
shows also when fast forwarding and when avoiding it.

When your head is spinning and you are like a Buridan’s Ass between a
rebased stack of hay and a merged pail of water, you can read this
[post from Linus Torvald
](http://article.gmane.org/gmane.linux.kernel/681763)
([thread view
](http://thread.gmane.org/gmane.linux.kernel/681712/focus=681763))

> Rebasing branches is absolutely not a bad thing for individual developers.
But it *is* a bad thing for a subsystem maintainer....

In short it may be wise to follow the
[manual](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html)
and apply your topic branches by
[creating the perfect patch series
](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html#patch-series).

Read also [Fun with various workflows (1)
](http://git-blame.blogspot.fr/2013/06/fun-with-various-workflows-1.html)
and
[Fun with various workflows (2)
](http://git-blame.blogspot.fr/2013/06/fun-with-various-workflows-2.html)
by Junio C Hamano.

# Submodules and Subtrees
In git, there are  three main techniques for providing subproject
support: submodules, subtrees, and wrappers they are compared in
[Git Wiki: SubprojectSupport
](https://git.wiki.kernel.org/index.php/SubprojectSupport).

-   [Git Subrepo](https://github.com/ingydotnet/git-subrepo/)
    is an improvement from git-submodule and git-subtree,
    -   [Git Subrepo
        Wiki](https://github.com/ingydotnet/git-subrepo/wiki/)
-   an older alternative to subtree and submodule was
    {{< iref "#gitslave" "GitSlave" >}}
    but it is no longer developped since 2012.


## git-submodule
-   [Git Submodule Tutorial](https://git.wiki.kernel.org/index.php/GitSubmoduleTutorial)
    _2012_.
-   [git-submodules(1)
    ](https://www.kernel.org/pub/software/scm/git/docs/git-submodule.html)
-   [Git user manual: submodules
    ](http://www.kernel.org/pub/software/scm/git/docs/user-manual.html#submodules)
-   [Pro Git: Submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules)
-   [Lars Vogel: Using submodules in Git
    ](https://www.vogella.com/tutorials/GitSubmodules/article.html)
-   [GitHub Help: Working with submodules](http://help.github.com/submodules/)
-   [Mastering Git submodules – Christophe Porteneuve – Medium
    ](https://medium.com/@porteneuve/mastering-git-submodules-34c65e940407)
-   [Working with submodules - The GitHub Blog
    ](https://github.blog/2016-02-01-working-with-submodules/)

We need to avoid [Submodules Gotchas
](https://git.wiki.kernel.org/index.php/GitSubmoduleTutorial#Gotchas)
the main being yhe need to publish the submodule change before
publishing the change to the superproject that references it or you
won’t be able to clone the repository as shown in
[Pitfalls with submodules
](https://www.kernel.org/pub/software/scm/git/docs/user-manual.html#_pitfalls_with_submodules)
and [Pro Git: Issues with Submodules
](https://git-scm.com/book/en/v2/Git-Tools-Submodules_issues_with_submodules)

## Subtree merge
A subtree merge is used to contain a repository in a folder within a
repository.

-   In the Git distribution documentation you will find
    [How to use the subtree merge strategy
    ](https://www.kernel.org/pub/software/scm/git/docs/howto/using-merge-subtree.html).
-   [GitHub Help: Subtree Merge](http://help.github.com/subtree-merge/)
-   [ProGit: Subtree Merging
    ](https://git-scm.com/book/en/v1/Git-Tools-Subtree-Merging)
    _not yet in ProGit v2 at time of writing._
-   [GitHub: About Git subtree merges
    ](https://help.github.com/articles/about-git-subtree-merges/)
-   [Markus Prinz: Subtree merging and you
    ](http://nuclearsquid.com/writings/subtree-merging-and-you/)
-   If you want only to combine two git repositories into a new
    high-level repository, you don't need any extra tool, but just
    follow
    [Scott W. Bradley: Merge Git Repositories and Preseve Commit History
    ](http://scottwb.com/blog/2012/07/14/merge-git-repositories-and-preseve-commit-history/).

## git-subtree
See also my
[Git Subtree — Git Memo](https://git-memo.readthedocs.io/en/latest/subtree.html).

-   [git-subtree
    ](https://git.kernel.org/pub/scm/git/git.git/plain/contrib/subtree/git-subtree.txt)
    was first developed by Avery Pennarun and since april 2012 merged
    in git mainline and available in the contrib directory.
-   [Understanding Git Subtree
    ](https://hpc.uni.lu/blog/2014/understanding-git-subtree/) _2014_.
-   Jakub Suder's [Sharing code between projects with git subtree
    ](http://psionides.eu/2010/02/04/sharing-code-between-projects-with-git-subtree/)
     is a tutorial to git-subtree _2010_.
-   Nicola Paolucci wrote [Alternatives To Git Submodule: Git Subtree
    ](https://www.atlassian.com/blog/git/alternatives-to-git-submodule-git-subtree)
    _2013 updated 2017_ a git-subtree tutorial and [The power of Git subtree
    ](https://developer.atlassian.com/blog/2015/05/the-power-of-git-subtree/)
    _2015_.
-   [git subtrees: a tutorial – Vinícius Baggio Fuentes – Medium
    ](https://medium.com/@v/git-subtrees-a-tutorial-6ff568381844)
-   [Mastering Git subtrees – Christophe Porteneuve – Medium
    ](https://medium.com/@porteneuve/mastering-git-subtrees-943d29a798ec)
-   [When to use git subtree? - Stack Overflow
    ](https://stackoverflow.com/questions/32407634/when-to-use-git-subtree)
-   [Understanding Git Subtree - HPC @ Uni.lu
    ](https://hpc.uni.lu/blog/2014/understanding-git-subtree/)
    includes a comparison with git submodules.
-   [Using Git subtrees for repository separation – Making Software
    ](https://makingsoftware.wordpress.com/2013/02/16/using-git-subtrees-for-repository-separation/)
    _2013_

### comparisons with submodules
-   [Handling Dependencies with Submodules and Subtrees - GitHub Cheatsheets
    ](https://github.github.com/training-kit/downloads/submodule-vs-subtree-cheat-sheet/)
-   [Git: submodules vs. subtrees - Andrey Nering
    ](https://andrey.nering.com.br/2016/git-submodules-vs-subtrees/)
-   [Differences between git submodule and subtree - Stack Overflow
    ](https://stackoverflow.com/questions/31769820/differences-between-git-submodule-and-subtree)
-   [Git Submodules vs Git Subtrees | Code Wins Arguments
    ](https://codewinsarguments.co/2016/05/01/git-submodules-vs-git-subtrees/)

## Other tools
Some other tools to act on a group of repositories

-   <a name="gitslave"></a>[GitSlave](http://gitslave.sourceforge.net/)
    manage a superproject repository and a number of slave
    repositories all of which are concurrently developed on and on
    which all git operations should normally operate; Gitslave has no
    new commit since 2012.
-   [mr alias _myrepos_](https://github.com/joeyh/myrepos) (GPL)
    by Joey Hess is a perl script that can checkout, update, or
    perform other actions on a set of repositories. _mr_ is a Debian
    Package.
-   [fgit (Folder Git)](https://github.com/l0b0/fgit) (GPL)
    by Victor Engmark is a small shell script that run a Git command
    in several repositories.
-   [metagit (GitHub)](https://github.com/stettberger/metagit) (GPL)
    is a python tool for defining sets of git (or whatever scm)
    repositories and perform actions like clone/pull/push on them.

# Git repositories
There are some git free or *adware* or *{{< wp "Freeware"  "freemium" >}}*
repositories they are [listed in the Git Wiki
](https://git.wiki.kernel.org/index.php/GitHosting)
and in the Wikipedia
{{< wp "Comparison of open-source software hosting facilities" >}}.

## GitHub
[GitHub](http://github.com/) gives you a free git
repository for public _and now private_ projects.

-   [GitHub Full workflow inside the browser
    ](https://github.com/blog/1557-github-flow-in-the-browser)

### Gist
GitHub  host a pastebin-style site called
[Gist](https://gist.github.com/) for hosting code snippets.

You can write any block of text in the space provided,
You can choose to have a secret Gist that will not be visible to
search engines but only to those who know the URL.

All changed to a gist are recorded and you can compare the releases.

Your gist can be in GitHub Markdown and previewed in the browser.

[Roughdraft](http://www.roughdraft.io/) allow to serve your page
written in GitHub-flavored Markdown, Textile, Haml, and plain text on
the web.

[Bl.ocks](https://bl.ocks.org) is a simple viewer for sharing code examples hosted on GitHub Gist.
You put in your gist an html document with relative links to other
files in your Gist, such as images, scripts or stylesheets; a
Readme.md in markdown a `.block` YAML configuration, and _Bl.ocks_
serve your page. Look at
this [example source](https://gist.github.com/mbostock/1353700),
and [Bl.ocks rendering](https://bl.ocks.org/mbostock/1353700).


## Free for open source software
-   [repo.or.cz](http://repo.or.cz/) offer free git hosting
    for open-source projects, you find
    there mirrors of numerous projects (\~250): cogito, dia, darcs2git,
    django, elinks, fast-export, findutils, gajim, git,
    git-\<something\>, guile, moodle, qemu, rox-filer,...
-   {{< wp "Gitorious" >}} (AGPL) was hosting
    freely your open source git repository. It is now acquired by
    GitLab, and closed, an archive is at
    [Gitorous read-only mirror ](http://gitorious.org)


## Project specific open source software
-   Debian has for its projects a
    [git.debian.org](http://git.debian.org/) gitweb
    repository. At
    [Alioth](http://wiki.debian.org/Alioth) you
    will find a
    [notice to use it](http://wiki.debian.org/Alioth/Git).
-   [Savanah](http://savannah.gnu.org/) the Gnu
    software repository has a
    [gitweb access](http://git.sv.gnu.org/gitweb/).

## Free open-source and private repositories
-   [CloudHost](http://git.cloudhost.io/) free open sources, and up to
    1000 private repositories.
-   [GitLab Cloud](http://www.gitlab.com/) unlimited private repositories,
    unlimited collaborators, max 1G per repository. It is based on the
    [GitLab Web frontend](http://gitlab.org/) (MIT License).
    [Framagit](https://framagit.org/) is an other free instance of
    GitLab Community.
    -   [ArchWiki: Gitlab](https://wiki.archlinux.org/index.php/Gitlab).
-   [BitBucket](https://bitbucket.org/) gives unlimited private code
    repositories for at most 5 users.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
