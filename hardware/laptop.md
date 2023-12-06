---
title: Linux on Laptops
---

# References
-   [Laptop - ArchWiki](https://wiki.archlinux.org/title/Laptop)
-   [InstallingDebianOn - Debian Wiki](https://wiki.debian.org/InstallingDebianOn/)
-   [Certified laptops | Ubuntu](https://ubuntu.com/certified/laptops)

## Tablet PC

-   [Tablet PC - ArchWiki](https://wiki.archlinux.org/title/Tablet_PC)

-   The kernel sys-bus-iio is described in the [Kernel Documentation: sys-bus-iio
    ](https://git.kernel.org/pub/scm/linux/kernel/git/torvalds/linux.git/tree/Documentation/ABI/testing/sysfs-bus-iio),
    you find it in the sysfs entry `/sys/bus/iio/devices/iio:deviceX`.
-   [iio-sensor-proxy](https://gitlab.freedesktop.org/hadess/iio-sensor-proxy/)
    Proxies sensor devices (accelerometers, light sensors, compass) to applications
    through D-Bus.

    The [accelerometer orientation
    ](https://gitlab.freedesktop.org/hadess/iio-sensor-proxy/#accelerometer-orientation)
    may need to be calibrated.

    We can check that the proxy is running with:
    ``` sh
    systemctl status iio-sensor-proxy.service
    ```

    We van interact with the iio-sensors by using the command `monitor-sensor`which read
    from dbus the iio-sensors events and report them.

#### Rotate screen

There are many small projects to auto-rotate screen, which is necessary for tablet PC
and 2 in 1 pc.

You find in shell:
-   The gist [*midjomo* Script to rotate the screen
    ](https://gist.github.com/mildmojo/48e9025070a2ba40795c)
    is aimed to X11, it has numerous forks, most referred in the gist thread which is is
    quite long.
-   [*AcamposPT* Script to rotate the screen
    ](https://gist.github.com/ACamposPT/6794aa02a6e5e341f123d447b3645b93)a
    is a similar fork, which still use *xinput*.
-   [*undg* autorotate](https://github.com/undg/autorotate/) is a go program for
    rotation of X11.
-   [*tedk0n* autorotate\_sway\_script
    ](https://github.com/tedk0n/autorotate_sway_script)
    is a bash script aimed at wlroots composers, it uses the output of `monitor-sensor`.
-   [efernau/rot8: screen rotation daemon](https://github.com/efernau/rot8)
    is a rust daemon for auto screen rotation on X11 or wayland.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- eval: (org-link-minor-mode 1) -->
<!-- End: -->
