---
title: Dbus
---


# Dbus References
-   Wikipedia: {{< wp "D-Bus" >}}
-   [freedesktop.org - Software - dbus
    ](http://www.freedesktop.org/wiki/Software/dbus/):
    [dbus documentation
    ](http://www.freedesktop.org/wiki/Software/dbus/#index4h1),
    [D-Bus Tutorial](http://dbus.freedesktop.org/doc/dbus-tutorial.html),
-   [Dbus FAQ](http://dbus.freedesktop.org/doc/dbus-faq.html)
    gives a very comprehensive comparison between `Dbus` and
    other interprocess communication `IPC`: `CORBA`, `XML-RPC`, `SOAP`,
    Distributed Computing Environment (`DCE`), ZeroC's Internet
    Communications Engine (`Ice`), `DCOP`.
-   [Using of D-Bus - D-Bus integration in Emacs
    ](http://www.gnu.org/software/emacs/manual/html_node/dbus/index.html#Top)
        [Inspection - Using of D-Bus
        ](http://www.gnu.org/software/emacs/manual/html_node/dbus/Inspection.html#Inspection)
        [Introspection - Using of D-Bus
        ](http://www.gnu.org/software/emacs/manual/html_node/dbus/Introspection.html)
-   [Ian's TechBlog: Dbus Tutorial
    ](http://cheesehead-techblog.blogspot.fr/2012/07/dbus-tutorial-intro-and-resources.html) :
    [Introspection
    ](http://cheesehead-techblog.blogspot.fr/2012/08/dbus-tutorial-introspection-figuring.html)

-   Dbus Cli tools: {{< man "dbus-send+1" >}}, {{< man "gdbus+1" >}},
    {{< man "mdbus2+1" >}}, {{< man "dfeet+1" >}}

# Dbus API
In the {{< iref "python_libraries" "Python Libraries Page" >}} you find the
{{< iref "python_libraries#dbus_python_api" "Dbus Python API" >}}.


-   [FreeDesktop: Software/DBusBindings](http://www.freedesktop.org/wiki/Software/DBusBindings)
    give the bindings available in many languages.
-   [gdbus](https://developer.gnome.org/gio/stable/gdbus.html)
    is an implementation of D-Bus based on GIO streams included in GLib.

# Dbus use from shell

-   To suspend:

    ```sh
    dbus-send --print-reply  --system  \
    --dest=org.freedesktop.login1 /org/freedesktop/login1 \
    org.freedesktop.login1.Manager.Suspend boolean:true
    ```

    Instead of `Suspend` you can use `Reboot`, `PowerOff`, `Hibernate`.


-   To  list the services available on the system bus:

    ```sh
    dbus-send --print-reply  --system  \
    --dest=org.freedesktop.DBus --type=method_call --print-reply \
    /org/freedesktop/DBus org.freedesktop.DBus.ListNames
    ```

    Replace `--system` by `--session` to get the answer for the session bus.

-   To find the methods:

    ```sh
    dbus-send --print-reply  --system \
    --dest=org.freedesktop.login1 \
    /org/freedesktop/login1 \
    org.freedesktop.DBus.Introspectable.Introspect
    ```

Now using {{< man "gdbus+1"  "gdbus" >}}:

-   list methods, signal and properties:

    ```sh
    gdbus introspect --system --dest=org.freedesktop.login1 \
    --object-path="/org/freedesktop/login1" --recurse
    ```

With {{< man "qdbus+1"  "qdbus" >}}

-   list methods, signal and properties:

        qdbus --system org.freedesktop.login1 /org/freedesktop/login1


# Dbus monitoring tools

-   {{< man "dbus-monitor+1" >}}
-   [DFeet
    ](https://wiki.gnome.org/action/show/Apps/DFeet?action%3Dshow&redirect%3DDFeet),
    {{< lman "dfeet+1" >}}
-   [Bustle
    ](http://www.willthompson.co.uk/bustle/)

# Dbus Notification
-   [ArchWiki Desktop notifications
    ](https://wiki.archlinux.org/index.php/Desktop_notifications)
    explain how to display desktop notifications and information, with
    _libnotify_, in each programming language.
-   [Desktop Notifications Specification
    ](https://developer.gnome.org/notification-spec/)
    gives all the components, you will find here the markup,
    hyperlinks, url, image, categories (in the `category=` parameter
    of `inotify-send`), urgency levels, hints, the dbus-protocol.
-   The icons used in notifications must follow the
    [Icon Naming Specification
    ](http://standards.freedesktop.org/icon-naming-spec/icon-naming-spec-latest.html)

-   _notification daemon_ is the standard gnome a daemon to display
    passive notifications, it binds to gtk3 libraries and takes 14.6M
    resident/9.6M shared
-   [dunst](http://www.knopwob.org/dunst/) (BSD License) is a
    lightweight notification daemons for desktop notifications.  Dunst
    is designed to fit nicely into minimalistic windowmanagers, and
    has minimal dependencies. It takes only 3.3M resident with 2.7M
    shared in my desktop.  It is in Debian.
-   [notify-osd](https://launchpad.net/notify-osd) is the Canonical's
    on-screen-display notification agent, implementing the Desktop
    Notifications Specification with semi-transparent click-through
    bubbles. It has a smart non-obtrusive look.
    It is programmed in c/gtk2 but requires also many
    libraries, and so is heavier than _dunst_ or _statnot_ 23M res. :
    18M shr. It is in Debian.
-   [statnot](https://github.com/halhen/statnot) (GPL)
    is a notification-daemon replacement for lightweight window
    managers written in python/gtk.
-   [twmn](https://github.com/sboli/twmn)
    is a notification system for tiling window managers build in
    C++/QT.  Notifications are shown in a one-line bar called the
    notification slide. They can be navigated through and activated
    with shortcuts.

-   [Galago](http://www.galago-project.org/)
    is a desktop presence framework for UNIX systems. It transmits
    "presence" information on people between applications thru the dbus
    system  following the
    [Galago Desktop Notifications Specification
    ](http://www.galago-project.org/specs/notification/0.9/index.html)..

## notification history

-   On _dunst_ a configurable key shortcut, display the recent history
    of notification.
-   We can monitor notifications with

        dbus-monitor "interface='org.freedesktop.Notifications'" |\
        grep --line-buffered "member=Notify\|string"

-   There is also a package in PPA:
    [recent notification / indicator-notifications
    ](https://launchpad.net/~jconti/+archive/ubuntu/recent-notifications).
