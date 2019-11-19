---
title: Linux Kernel
---

# Kernel references

-   [The Linux Kernel documentation](https://www.kernel.org/doc/html/latest/)
    and other [documentation at kernel.org](https://www.kernel.org/doc/)
    including
    [text files in the kernel's Documentation directory
    ](http://www.kernel.org/doc/Documentation/).
-   [Linux Kernel Newbies](https://kernelnewbies.org/) :
    [KernelBuild](https://kernelnewbies.org/KernelBuild),
    [Documents](https://kernelnewbies.org/Documents),
    [FAQ](https://kernelnewbies.org/FAQ).
-   [Linux Kernel in a Nutshell](http://www.kroah.com/lkn/)
    *(pdf with html toc Creative Commons Attribution-ShareAlike license)*
    an up to date book by Greg Kroah-Hartman. The reference chapters
    are usefull.
-   [The Linux Kernel Archive](http://www.kernel.org/pub/)
    contains the kernel sources.
-   Ubuntu Wiki:  [Index of Kernel pages](https://wiki.ubuntu.com/Kernel),
    and index of [Kernel/Dev](https://wiki.ubuntu.com/Kernel/Dev).
-   Gentoo Wiki : [Gentoo Kernel Configuration Guide
    ](https://wiki.gentoo.org/wiki/Kernel/Gentoo_Kernel_Configuration_Guide),
    [Kernel/Configuration
    ](https://wiki.gentoo.org/wiki/Kernel/Configuration),
    [Kernel modules](https://wiki.gentoo.org/wiki/Kernel_Modules)

# Kernel Build

-   [KernelBuild - Linux Kernel Newbies](https://kernelnewbies.org/KernelBuild)
-   [Linux Kernel Build HOWTO](http://www.tedfelix.com/linux/kernel-build.html)
    by Ted Felix _July 2018_.
-   [How To CrossBuildAn Official Debian Kernel Package - Debian Wiki
    ](https://wiki.debian.org/HowToCrossBuildAnOfficialDebianKernelPackage)
-   [Creating custom kernels with Debian's kernel-package system
    ](http://newbiedoc.sourceforge.net/system/kernel-pkg.html)
    _kernel-package_ provides the capability to create a Debian kernel image package by just
    running make-kpkg kernel_image in a kernel source directory tree.
    This document is also in  the directory `/usr/share/doc/kernel-package/`.
    a tutorial is
    [Creating a Custom Linux Kernel in Debian GNU/Linux by Steve Powell
    ](http://www.stevesdebianstuff.org/Kernel.htm)
    which uses the *kernel-package*



## naming the kernel with a version

When compiling the kernel, the kernel built is identified by the
variables:
`VERSION PATCHLEVEL SUBLEVEL EXTRAVERSION NAME LOCALVERSION` so
when I compile a kernel with different configs ( what I do very
often to test my configs, I change `LOCALVERSION` in order to have
a new name for my module tree, otherwise all the build of a same
kernel will find the modules generated during the last build.

`LOCALVERSION` can be set in many ways : a file named
`localversion*`, a config variable `CONFIG_LOCALVERSION` or it can
be passed to `Make` as variable

The appropriate make order is:
`make LOCALVERSION=my_config_version`

If you give a local version all your modules in the `/lib/modules`
tree are identified by the full
`VERSION PATCHLEVEL SUBLEVEL EXTRAVERSION LOCALVERSION` so your
different kernels don't get mixed.

## Cross Compiling Kernel

The kernel Makefile say in the section
*Cross compiling and selecting different set of gcc/bin-utils*:

> When performing cross compilation for other architectures ARCH shall be set
> to the target architecture. (See arch/\* for the possibilities).

`ARCH` can be set during invocation of make:

    make ARCH=ia64

Another way is to have ARCH set in the environment.
The default ARCH is the host where make is executed.

`CROSS_COMPILE` specify the prefix used for all executables used
during compilation. Only gcc and related bin-utils executables
are prefixed with `$(CROSS_COMPILE)`.

`CROSS_COMPILE` can be set on the command line

    make CROSS_COMPILE=ia64-linux-

Alternatively `CROSS_COMPILE` can be set in the environment.
A third alternative is to store a setting in `.config` so that plain
"make" in the configured kernel build directory always uses that.
Default value for `CROSS_COMPILE` is not to prefix executables
Note: Some architectures assign `CROSS_COMPILE` in their `arch/\*/Makefile`.


# compiling a single kernel module

-   [Kernel.org : Building External Modules
    ](https://www.kernel.org/doc/Documentation/kbuild/modules.txt)
    is the base documentation
-   [Rebuilding a single kernel module - Debian Administration
    ](https://debian-administration.org/article/640/Rebuilding_a_single_kernel_module)
    is an exemple of using the previous recipe.
-   [Compile kernel module - ArchWiki
    ](https://wiki.archlinux.org/index.php/Compile_kernel_module)
    is an other tutorial on the same recipe
-   [KernelDKMS - Debian Wiki](https://wiki.debian.org/KernelDKMS)
-   A more complex description in
    [How to recompile just a single kernel module? - Stack Overflow
    ](https://stackoverflow.com/a/44204152/965798)
-   See also [14.04 - How (recipe) to build only one kernel module? - Ask Ubuntu
    ](https://askubuntu.com/questions/515407/how-recipe-to-build-only-one-kernel-module?noredirect=1&lq=1)
-   Partially obsolete but a complete example workout:
    [Compiling Kernel Modules -  The Linux Kernel Module Programming Guide
    ](https://www.tldp.org/LDP/lkmpg/2.6/html/x181.html)



## Example of module

    #include <linux/module.h>
    #include <linux/kernel.h>
    #include <linux/init.h>

    MODULE_LICENSE("GPL");
    MODULE_AUTHOR("M.Z.");
    MODULE_DESCRIPTION("a simple test module");
    MODULE_VERSION("1.0");


    static int __init
    start(void) {
      printk(KERN_INFO "\nHello from test module!\n\n");
      return 0;
    }


    static void __exit
    end(void) {
      printk(KERN_INFO "\nBye from test module!\n\n");

    }


    module_init(start);
    module_exit(end);

with makefile

    obj-m+=foo.o

    KVERSION=$(shell uname -r)

    all:
        make -C /lib/modules/$(KVERSION)/build M=$(PWD) modules

    clean:
        make -C /lib/modules/$(KVERSION)/build M=$(PWD) clean


<a id="org874ebab"></a>

## module-assistant tool** (alias m-a)

helps managing external Linux kernel modules it is packaged for Debian. It can do:

-   automated preparation of build environment for module compilation (e.g. automatic
    detection and installation of required kernel source/headers);
-   automated module source downloads;
-   configuration and tracking of external and locally built modules packages;
-   semi-automated multiple builds for multiple kernel versions;

It is used in [Chapter 4. Common kernel-related tasks - Debian Kernel Team
](https://kernel-team.pages.debian.net/kernel-handbook/ch-common-tasks.html#s-common-out-of-tree)

You find documentation in:

-   [ModuleAssistant - Debian Wiki](https://wiki.debian.org/ModuleAssistant)
-   [module-assistant(8)
    ](https://manpages.debian.org/buster/module-assistant/module-assistant.8.en.html)
