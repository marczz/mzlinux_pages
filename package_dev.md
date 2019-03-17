<!--
.. description:
.. date: 2015-09-30
.. slug: package_dev
.. tags:
.. link:
.. book: mzlinux
.. title: Debian package Developement
-->

[TOC]

See also [Debian administration
](/node/debian_admin "internal reference") subsections:
[Package management
](/node/debian_admin#package_management "internal reference"),
[Package Repositories
](/node/debian_admin#package_repository "internal reference"),
[Apt Pinning
](/node/debian_admin#apt_pinning "internal reference").


# Package Building

## Tutorials
-   [Debian Wiki: Packaging](https://wiki.debian.org/Packaging) references other pages
    on packaging in Debian Wiki.
    -   [Packaging Intro](https://wiki.debian.org/Packaging/Intro),
    -   [How To Package For Debian
        ](https://wiki.debian.org/HowToPackageForDebian).
-   [Debian Wiki: BuildingTutorial](https://wiki.debian.org/BuildingTutorial),
    [Building a Package](https://wiki.debian.org/BuildingAPackage) uses fakeroot on
    _/debian/rules_ (a make command).
-   Raphael Herzog: [Howto to rebuild Debian packages
    ](https://raphaelhertzog.com/2010/12/15/howto-to-rebuild-debian-packages/)
-   There is a package with packaging tutorials: [packaging-tutorial
    ](https://packages.debian.org/search?keywords=packaging-tutorial)
    or read the [on line - packaging tutorial (pdf)
    ](https://www.debian.org/doc/manuals/packaging-tutorial/packaging-tutorial.en.pdf),
    in french [Tutoriel : la construction de paquets Debian (pdf)
    ](https://www.debian.org/doc/manuals/packaging-tutorial/packaging-tutorial.fr.pdf).
-   [Debian Package Customization HOWTO
    ](http://people.connexer.com/~roberto/howtos/debcustomize)

## Building Tools
-   The documentation for all the _dh_xxx_ commands are in man pages and referenced in
    [debhelper(7)](https://manpages.debian.org/stretch/debhelper/debhelper.7.en.html),
    [dh(1)](https://manpages.debian.org/stretch/debhelper/dh.1.en.html)
    you find a tutorial for their use in the _Debian Maintainers'_ guide referenced
    below.
-   The package _dh-make_ allows you to take a standard (or upstream) source package and
    convert it into a format that will allow you to build Debian packages.

## Debian References

-   [Debian New Maintainers' Guide
    ](http://www.debian.org/doc/manuals/maint-guide/)
    is the main reference on package building.
    In  [Debian New Maintainers' Guide (HTML)
    ](https://www.debian.org/doc/manuals/maint-guide/index.en.html)
    you find:
    -   [Modifying the source
        ](https://www.debian.org/doc/manuals/maint-guide/modify.en.html)
    -   [Required files (control, rules, ...)
        ](https://www.debian.org/doc/manuals/maint-guide/dreq.en.html)
    -   [Building the package
        ](https://www.debian.org/doc/manuals/maint-guide/build.en.html)
        with _debuild_, _pbuilder_, _git-buildpackage_,
    -   [Checking the package
        ](https://www.debian.org/doc/manuals/maint-guide/checkit.en.html)
    -   [updating the package
        ](https://www.debian.org/doc/manuals/maint-guide/update.en.html)
    -   [uploading the package
        ](https://www.debian.org/doc/manuals/maint-guide/upload.en.html)
-   [Guide for Debian Maintainers
    ](https://www.debian.org/doc/manuals/debmake-doc/index.en.html)
    which is focused on the use of [debmake(1)
    ](https://manpages.debian.org/stretch/debmake/debmake.1.en.html)
    complete the previous manual dealing with same subjects like _debian/control_ and
    _debian/rules_. It is maily focused on
    [debmake](https://www.debian.org/doc/manuals/debmake-doc/ch06.en.html).
-   [Debian Developer's Reference
    ](http://www.debian.org/doc/manuals/developers-reference/)
    is intended to debian developers but chapter 5,6,7 deal with
    packages and are of interest for package builders:
    - [Managing Pakages
      ](http://www.debian.org/doc/packaging-manuals/developers-reference/pkgs.html)
      deals with creating, uploading, maintaining, and porting
      packages.
    -   [Best Packaging Practices
        ](https://www.debian.org/doc/manuals/developers-reference/best-pkging-practices.html)
    -   [overview of debian packaging tools
        ](http://www.debian.org/doc/packaging-manuals/developers-reference/tools.html) _only a short overview_
-   [Debian Policy Manual](http://www.debian.org/doc/debian-policy/)
    includes technical requirements that each package must satisfy to
    be included in the debian distribution.
-   [mentors.debian.net](http://mentors.debian.net/) is a site for
    non-official debian mainteners, they can upload their packages on
    the site repository.
-   Joey Hess [The Debconf Programmer's Tutorial
    ](http://www.fifi.org/doc/debconf-doc/tutorial.html)


# Pbuilder
-   [Pbuilder](http://www.debian.org/doc/maint-guide/ch-build.en.html#pbuilder)
    in [Debian Maintainers' Guide](http://www.debian.org/doc/maint-guide/)
-   [pbuilder User's Manual
    ](http://www.netfort.gr.jp/~dancer/software/pbuilder-doc/pbuilder-doc.html)
    is the reference manual by Junichi Uekawa.
-   [Ubuntu Pbuilder Howto](https://wiki.ubuntu.com/PbuilderHowto)
-   [Debian Wiki: Pbuilder Tricks](http://wiki.debian.org/PbuilderTricks)
-   [Backporting Debian packages with pbuilder
    ](http://www.tolaris.com/2009/03/31/backporting-debian-packages-with-pbuilder/)
-   [cowbuilder(8)](https://manpages.debian.org/stretch/cowbuilder/cowbuilder.8.en.html)
    is a wrapper for pbuilder which allows using pbuilder-like
    interface over _cowdancer_ environment.
    -   [Debian Wiki: Cowbuilder](https://wiki.debian.org/cowbuilder).
    -   [Ubuntu Help: Cowdancer HowTo](https://wiki.ubuntu.com/CowdancerHowto).

# Sbuild
_sbuild_ compined with _schroot_ are used on the Debian build daemons, they are  not as
simple as _pbuilder_, but allows LVM snapshots.

-   [Debian Wiki: Sbuild](https://wiki.debian.org/sbuild).
-   [Ubuntu Help - Sbuild Lvm HowTo](https://help.ubuntu.com/community/SbuildLVMHowto).

# cdbs _common build system_
-   The [CDBS tool](http://cdbs-doc.duckcorp.org/en/cdbs-doc.xhtml)
    is a wrapper system over  _debhelper_. Along the (maintenairers' guide
    ](https://www.debian.org/doc/manuals/debmake-doc/ch07.en.html#cdbs)
    _For simple packages, the dh command alone allows us to make a simple and clean
    debian/rules file_  and should be preferred to  CDBS, which is used for complex
    packages like the gnome suite. The _packaging-tutorial_ also tell that for new
    packages we should use _dh_ that is know, from far, the most used build system for
    Debian packages.
-   [Debian packaging with CDBS
    ](http://debathena.mit.edu/packaging/)
    an introduction to Debian development
-   Joey criticisms [ship in a bottle
    ](http://joey.kitenet.net/blog/entry/ship_in_a_bottle/),
    [cdbs killer (design phase)
    ](http://joey.kitenet.net/blog/entry/cdbs_killer___40__design_phase__41__/)

# Equivs
[equivs](https://packages.debian.org/sid/equivs) is a tool
to create trivial Debian packages which contain mainly dependency
information, but they can also include normal installed files like
other packages do.

One use for this is to create a metapackage: a package whose sole
purpose is to declare dependencies and conflicts on other packages;
or to circumvent dependency checking

# git-buildpackage

git-buildpackage is a tool suite to help with Debian packages in Git repositories.

-   [git-buildpackage manual: Building Debian Packages with git-buildpackage
    ](http://honk.sigxcpu.org/projects/git-buildpackage/manual-html/gbp.html)
    by Guido Guenther.
-   [sigxcpu.org wiki](https://honk.sigxcpu.org/piki/):
    -   [git-buildpackage](https://honk.sigxcpu.org/piki/projects/git-buildpackage//manual-html/gbp.html)
        is a _git-buildpackage_ workflow,
        it includes backporting instructions.
    -   [debian packages in git at  sigxcpu.org](https://honk.sigxcpu.org/piki/development/debian_packages_in_git/)
    -   [cl2vcs](https://honk.sigxcpu.org/piki/projects/cl2vcs/)
    -   [colors of noise](https://honk.sigxcpu.org/con/) is the blog of Guido Guenther.
-   [Using Git for Debian Packaging](http://www.eyrie.org/~eagle/notes/debian/git.html) by Russ Allbery
    is a general debian-git tutorial, with a section on _git-buildpackage_.
-   [git-dpm _(manpage)_](http://git-dpm.alioth.debian.org/manpage.htm)
    or _debian packages in git manager_ is a tool to handle a debian
    source package in a git repository.
    [git-dpm: debian packages in git manager](http://git-dpm.alioth.debian.org/)
    is a presentation of git-dpm.
-   [TopGit](http://repo.or.cz/w/topgit.git?a=blob;f=README)
    is a tool to maintain a large amount of interdependent topics
    branches in git.
    _Tg2Quilt_ facilitates generation of the quilt series from
    _TopGit_ branches it is explained in the
    [Tg2Quilt HowTo
    ](http://git.debian.org/?p=collab-maint/topgit.git;a=blob_plain;f=debian/HOWTO-tg2quilt;hb=HEAD)
    you find _TopGit_ in it's [git repository](http://repo.or.cz/w/topgit.git).


# Setting up a Package Repository
-   [How To Setup A Debian Repository ](http://wiki.debian.org/HowToSetupADebianRepository)
    in debian wiki, lists the known tools to maintain an apt
    repository.
-   [Automatic Debian Package Repository HOWTO
    ](http://people.connexer.com/~roberto/howtos/debrepository)
    is replaced by the following
    _Setting up your own APT repository with upload support_
    but it still have informations on directory structure
-   [Setting up your own APT repository with upload support
    ](https://www.debian-administration.org/article/286/Setting_up_your_own_APT_repository_with_upload_support)
    use the reprepro package
-   [HOWTO: Create your own local Debian repository
    ](http://blogs.koolwal.net/2009/09/21/howto-create-your-own-local-debian-repository/)
    is a short tutorial for a small personnal repository.

# Backporting

See main section [Debian administration
](/node/debian_admin "internal reference") :
[Backports](/node/debian_admin#backports  "internal reference").


-   [Debian Wiki: Simple Backport creation
    ](https://wiki.debian.org/SimpleBackportCreation)
-   [Backports](http://doc.cliss21.com/index.php?title=Backports)
    from [cliss 21](http://www.cliss21.com/) decribe how to backport a package.
-   ref manual:
    [Updates and Backports
    ](https://www.debian.org/doc/manuals/debian-reference/ch02.en.html#_updates_and_backports),
    [Port a package to the stable system
    ](https://www.debian.org/doc/manuals/debian-reference/ch02.en.html#_porting_a_package_to_the_stable_system)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
