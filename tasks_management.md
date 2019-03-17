<!--
.. description:
.. date: 2011-05-29
.. slug: tasks_management
.. tags:
.. link:
.. book: mzlinux
.. title: Tasks Management
-->

[TOC]

----

See also [Documents management](/node/documents "internal reference")
and the section
[Read List](/node/documents#read-list "internal reference").

# GTD

-   [Toward a New Vision of Productivity, Part 3: The Trouble with GTD
    ](http://www.lifehack.org/articles/productivity/toward-a-new-vision-of-productivity-part-3-the-trouble-with-gtd.html)
-   [Total, Relaxed Organization (TRO)
    ](http://www.priacta.com/Training/),
    [TRO FAQs](http://www.priacta.com/Training/Training_FAQ.shtml),
    [TRO and GTD (pdf)](http://www.priacta.com/Articles/TRO-and-GTD.pdf)
-   [GTD Software Comparison, 164 Researched Apps - priacta
    ](http://www.priacta.com/Articles/Comparison_of_GTD_Software.php)
-   [Getting Things Done - Wikipedia
    ](http://en.wikipedia.org/wiki/Getting_Things_Done)

# Online tasks

## Toodledo

[Toodledo](http://www.toodledo.com/) is an online to-do list with
[org-toodledoo](https://github.com/christopherjwhite/org-toodledo)
syncing to emacs.

-   [handyman5/poodledo](https://github.com/handyman5/poodledo)
    python + toodledo
-   [Envoyer un SMS depuis Gmail via Freemobile
    ](http://webinventif.com/envoyer-sms-depuis-gmail-via-freemobile/)
    Peut servir pour les notification
-   [Toodledo : Bookmarklet
    ](https://www.toodledo.com/tools/bookmarklet.php)


## [Remember The Milk](https://www.rememberthemilk.com)

Remember the milk has the best notification applications but for
synchronization you need to have a paid plan to be able to synchronize
between the Android application and the main site. Remember the milk is
not connected with ifttt. The premium plan is 25€ a year.

-   numerous applications see the [RTM Help
    ](https://www.rememberthemilk.com/help/).
-   [orgmode.org Git - org-sync. os-rtm.el
    ](http://orgmode.org/w/?p=org-sync.git;a=blob;f=os-rtm.el;h=f9aa51c8a3f927fb4c88c174aa66e3d5a1585a35;hb=d3df7452c5968d85054518a887fbea70fd0f4de4)
    Remember The Milk backend for org-sync. also at
    [emacsmirror](https://github.com/emacsmirror/org-sync/blob/master/os-rtm.el)
-   [moloko, a RTM synchronized task application
    ](https://f-droid.org/wiki/page/dev.drsoran.moloko) allow
    to have an android a local database ansd sync with RTM, but it is in
    alpha quality, and the french translation is unusable.


## Other online services

-   [w:evernote] is a proprietary service/application to store notes,
    images and all kind of information. The basic plan is of free use.
    It supports search and tagging and you can sync everything between
    computers. Evernote supports mobile devices too like Android It has
    two opensources application for linux
    [NeverNote](http://nevernote.sourceforge.net/) and
    [Geeknote](http://www.geeknote.me/) console client whose deb
    packages are available on [notesalexp deb
    repo](http://notesalexp.org/).
-   [w:Todoist] is a project management application for personal and
    professional productivity.  Todoist is available in Web, Windows
    (PC and Windows 10 Mobile), macOS, Android, Android Wear, iOS
    (iPhone and iPad), watchOS (Apple Watch), Google Chrome, Firefox,
    Outlook, Gmail. Todoist Premium cost 45$/year and features include
    unlimited automatic synchronization across devices, platforms and
    computers; mobile and email reminders; unlimited note and file
    attachments; SSL encryption; task search; iCalendar task access;
    the ability to add emails as tasks; project templates; and
    automatic backups.
    -   [Todoist Home](https://todoist.com/).
    -   [Todoist, my new productivity tool
        ](https://www.osomac.com/2014/10/26/todoist-new-productivity-tool/)
        by Cesare Tagliaferri compares Todoist with Asana, Toodledo,
    -   [org-todoist](https://github.com/ttakamura/org-todoist)
        is a ruby script to sync TODOs between emacs org-mode files
        and Todoist, but you need a premium subscription to have
        access to Todoist API.

# Tasks on linux desktop

See also the sections [Org Mode](file:///node/org-mode/) and
[Calendar and Address Book](file:///node/calendar)

-   Wikipedia: [Comparison of note taking software
    ](https://en.wikipedia.org/wiki/Comparison_of_notetaking_software)
    [Category:Task management software
    ](https://en.wikipedia.org/wiki/Category:Task_management_software).
-   [VimOrganizer - An Emacs' Org-mode clone for Vim
    ](http://www.vim.org/scripts/script.php?script_id%3D3342),
    [GitHub VimOrganizer](https://github.com/hsitz/VimOrganizer)
-   [t](http://stevelosh.com/projects/t/) a **simple** todo in python
-   [task](http://taskwarrior.org/) or **taskwarrior** is a complet e
    task management system from command line, vim friendly,
    [task source repo - git.tasktools.org
    ](https://git.tasktools.org/projects/TM/repos/task/browse)
    -   [orgmode - task comparison
        ](http://taskextras.org/boards/8/topics/208%253Fr%253D941)
    -   [Mirakel android todo sync with taskwarrior and CALDAV
        ](https://f-droid.org/repository/browse/?fdfilter=caldav&fdid=de.azapps.mirakelandroid)
        but the project is hardly maintained and the synchronisation
        with taskwarrior is buggy *(in September 2016)*
-   [Nitro](http://nitrotasks.com/) BSD licence written in Coffee
    javascript [Github: CaffeinatedCode/nitro
    ](https://github.com/CaffeinatedCode/nitro)
-   [Tasque](https://wiki.gnome.org/Apps/Tasque) (GPL) is a gnome
    application *in Debian* written in mono/gtk with no extra
    dependencies. it takes [Remember the milk as backend
    ](https://wiki.gnome.org/Apps/Tasque/Backends)
-   [ReminderFox- The simple reminder application for Firefox
    ](http://www.reminderfox.org/)
-   [Todo.txt](http://todotxt.com/)
    (GPL) is a text only todo list. with management scripts in shell.
    A [todo.py python script]
    (http://msls.net/archive/2008/02/24/gittodo.htm) with git
    backend is also available and can be found in a
    [Gitorious repository](http://gitorious.org/git-todo-py/).
    Beside the [todo.txt Google code dir
    ](http://code.google.com/p/todotxt) *not updated
    since 2007* from Graham Daviez there is also a
    [github repository](http://github.com/ginatrapani/todo.txt-cli)
    maintained by the original author Gina Trapani.
    -   [Todo.txt CLI](https://github.com/ginatrapani/todo.txt-cli/wiki)
    -   [The Todo.txt format
        ](https://github.com/ginatrapani/todo.txt-cli/wiki/The-Todo.txt-Format)
    -   [Other todo.txt projects
        ](https://github.com/ginatrapani/todo.txt-cli/wiki/Other-Todo.txt-Projects)
        list all known projects.
    -   [Android Todo.txt
        ](https://play.google.com/store/apps/details?id=com.todotxt.todotxttouch)
        the oficial client.
    -   [Simpletask
        ](https://play.google.com/store/apps/details?id=nl.mpcjanssen.todotxtholo)
        is also using the same todo.txt format
-   [w:WikidPad] (BSD License) is a python-based wiki-like outliner
    for storing thoughts, ideas, to-do lists, contacts, and other notes
    with Wiki-like linking between pages.
-   [Yokadi](http://yokadi.github.com/) is a command-line oriented,
    SQLite powered, TODO list tool written in python. *release in 2014*


# Note taking software {#note_taking}

-   [w:Note-taking],
    [w:Comparison of notetaking software]



-   [w:Workflowy] freemium note taking software.
    Work mainly on web, but there are apps in ios, android, windows,
    Linux.
    -   [WorkFlowy Site](https://workflowy.com/)
        and [blog](https://blog.workflowy.com/)

## [SimpleNote](https://simplenote.com/)

is a free web service. It has applications for windows, OS-X, Linux,
Android, ios, Kindle Fire. Notes are versionned and can be shared.
Simplenote client apps are GPLv2 licensed, and are available in
[GitHub Automattic Repository](https://github.com/automattic).

-   [SimpleNote Help](https://simplenote.com/help/)
-   [SimpleNote Blog](https://simplenote.com/blog/)
-   [SimpleNote for Windows and Linux
    ](https://github.com/automattic/simplenote-electron) is written
    using [Electron](http://electron.atom.io/) a framework to build
    cross platform desktop apps with JavaScript, HTML, and CSS.
-   [Simplenote2.el](https://github.com/alpha22jp/simplenote2.el) is an
    Emacs lisp package that can assist your interaction with Simplenote,
    it is in Melpa.

[Turtl](https://turtlapp.com/)
is a place to keep your documents. They are protected by an end-to-end
encryption. It allows editing notes in markdown and  sharing.

The core interface and server are built in javascript; there is also a
core version in Rust, used by mobile applications. The desktop
application for windows, OS X and linux is in javascript.

In all the previous versions the core was in common
lisp.

-   [GitHub: Turtl](https://github.com/turtl)
-   [Turtl developers documentation](https://turtlapp.com/docs/)
-   ýou can run your [own instance of Turtl
    ](https://turtlapp.com/docs/server/)
    there are also docker images.
-   [turtlapp.com]](https://turtlapp.com/) is the main instance of
    turtl, the service is free until some limit.
-   [Framanote](https://framanotes.org/) free instance of Turtl.


# Notifications

-   [Bringing ETL to the Masses with APIs
    ](http://apievangelist.com/2013/02/10/bringing-etl-to-the-masses-with-apis/)
    zapier, ifttt znd friends
-   [Instapush - Instant Notifications for Important Transactions
    ](https://instapush.im/) accept an http post request to
    send a notification
-   [Pushover](https://pushover.net/) allow to receive notifications,
    from some enabled applications (including IFTT), or your own
    application using the API. There are client applications for
    Android, iPhone/iPad, and Desktop Browser. The service is one time
    payement of 5$ per device.
-   [Pushbullet](https://www.pushbullet.com/).
    -   [Pushbullet - Android Apps on Google Play
        ](https://play.google.com/store/apps/details?id=com.pushbullet.android)
        (5.7M)
    -   [GitHub - GustavoKatel/pushbullet-cli
        ](https://github.com/GustavoKatel/pushbullet-cli)
        (MIT License)
        is a Python Pushbullet CLI interface. It is in Pypi.
    -   [GitHub - randomchars/pushbullet.py
        ](https://github.com/randomchars/pushbullet.py)
        (MIT License)
        a python library for the Pushbullet service.
    -   [GitHub - rharder/asyncpushbullet
        ](https://github.com/rharder/asyncpushbullet)
        (MIT License) a python library for synchronous and
        asyncio-based communication with Pushbullet service. It is a
        fork of of the synchronous-only randomchars/pushbullet.py and
        is in Pypi.
-   [theanalyst/revolver](https://github.com/theanalyst/revolver)
    is an emacs client for pushbullet. It is in elpa under the name
    _pushbullet_.
-   <a name="IFTT">[IFTTT](https://ifttt.com/)
    is a service that lets you create
    connections between internet service providers.
-   [BipIO - For People and Robots](https://bip.io/) open source
    alternative of IFTTT.
-   [DERI Pipes](http://pipes.deri.org/) open source clone of
    [yahoo pipes](https://pipes.yahoo.com/pipes/)

remind
======

-   [remind home
    ](http://www.roaringpenguin.com/penguin/open_source_remind.php)
-   [wiki.43folders.com](http://wiki.43folders.com/):
    [Remind FAQ](http://wiki.43folders.com/index.php/Remind_FAQ),
    [Remind Helpers](http://wiki.43folders.com/index.php/Remind_Helpers),
    [ICal2Rem](http://wiki.43folders.com/index.php/ICal2Rem),
    [Remind use case II]
    (http://wiki.43folders.com/index.php/Remind_use_case_2),
    [Remind/wyrd use case 1
    ](http://wiki.43folders.com/index.php/Remind_use_case_1)
-   [rem2ics](http://mark.atwood.name/code/rem2ics)
    (see also [Remind Scripts
    ](http://wiki.grahamenglish.net/index.php/Remind_Scripts))
-   [wyrd](http://pessimization.com/software/wyrd/) a ncurses front end
    for remind. [Remind/wyrd use case
    ](http://wiki.43folders.com/index.php/Remind_use_case_1),



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
