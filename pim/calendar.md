---
title: Calendar and Address Book
---

See also {{< iref "task_management" "Tasks Management" >}}
and {{< iref "org-mode" "Org Mode" >}}

<!--
[[file:../../../../content-org/notes/pim_notes.org::#calendar_notes][Calendar Notes]]
-->

# Icalendar references

-   Wikipedia: {{< wp "Calendaring_software" >}},
    {{< wp "VCard"  "Wikipedia VCard" >}},
    {{< wp "ICalendar" >}},
    {{< wp "List of applications with iCalendar support" >}}
    {{< wp "CalDAV" >}},
    {{< wp "CardDAV" >}},
    {{< wp "Comparison of CalDAV and CardDAV implementations" >}}.
-   Guide to Internet Calendaring
    [RFC 3283](http://www.ietf.org/rfc/rfc3283.txt)
-   Internet Calendaring and Scheduling Core Object Specification
    (icalendar) [RFC2445](http://rfc.sunsite.dk/rfc/rfc2445.html) at
    [rfc.sunsite.dk](http://rfc.sunsite.dk), A nice xhtml excerpt is at
    [www.kanzaki.com/](http://www.kanzaki.com/docs/ical/)
-   iCalendar DTD Document:
    [xCal ietf draft](https://tools.ietf.org/html/draft-ietf-calsch-many-xcal-02)
-   iCalendar Transport-Independent Interoperability Protocol
    (iTIP) Scheduling Events, BusyTime, To-dos and Journal Entries
    [RFC 2446](http://www.ietf.org/rfc/rfc2446.txt)
-   [CalConnect](https://www.calconnect.org/) The Calendaring and Scheduling Consortium
    -   [Developer's Guide](https://devguide.calconnect.org/)
-   [CalDAV](http://caldav.calconnect.org/)
    is a calendaring and scheduling client/server protocol designed to allow users to
    access calendar data on a server, and to schedule meetings with other users on that
    server or other servers. -   The CalDAV Access protocol is an extension of
    the {{< iref "webdav" "WebDAV Protocol" >}},
    it has been published as
    [RFC 4791](http://tools.ietf.org/html/rfc4791).
-   [CardDAV](https://devguide.calconnect.org/CardDAV/) is an address book client/server
    protocol designed to allow users to access and share contact data on a server.

    It is published as [RFC 6352](); vCards is published as
    [RFC 6350](http://www.rfc-editor.org/rfc/rfc6350.txt),
    and the XML Representation of vCard (xCard) as
    [RFC 6351](http://www.rfc-editor.org/rfc/rfc6351.txt).
-   [microformats](http://microformats.org) is an HTML5 extension for marking up people,
    organizations, events, locations, blog posts, products, reviews, resumes, recipes
    etc.
    -   [Microformats | HTML5 Doctor](http://html5doctor.com/microformats/) an
        introduction _2010_.
    -   [microformats2 - Microformats Wiki](https://microformats.org/wiki/microformats2)
        is the latest version of microformats.
    -   [h-event](https://microformats.org/wiki/h-event) is open format for events on
        the It provides web.distributed calendaring and events and contact information
        formats, based on the iCalendar and Vcard standards. _h-event_ is the
        microformats2 update to [hCalendar](http://microformats.org/wiki/hcalendar).
    -   [h-card](https://microformats.org/wiki/h-card) open format for publishing
        people and organisations on the web.

-   [iCalShare](http://www.icalshare.com/) directory of shareable
    calendars on the web.
-   [Calendar FAQ](http://www.tondering.dk/claus/calendar.html),


# icalendar, CalDAV, CardDAV libraries

-   Wikipedia: {{< wp "CalDAV" >}}, {{< wp "CardDAV" >}},
    {{< wp "Comparison of CalDAV and CardDAV implementations" >}}.
-   [Calendar and Contacts Server](https://www.calendarserver.org/) (Apache 2 License)
    server implementing the CalDAV and CardDAV protocols
-   [caldav](https://github.com/python-caldav/caldav) (GPL-3.0 and Apache-2.0)
    is a calDAV python library. _active in 2023_.
-   [cardDAV PHP](https://github.com/graviox/CardDAV-PHP) (affero GPL)
    by Christian Putzke _last commit 2012_, is a simple CardDAV client library written
    in PHP + CURL. It is used in the
    [Roundcube CardDAV plugin](https://github.com/graviox/Roundcube-CardDAV).
    _last commit 2014_.
-   [FullCalendar](http://fullcalendar.io/) (MIT license or commercial)
    is a jQuery plugin that provides a full-sized, drag & drop calendar.

    _It is an active project in 2023._

    -   FullCalendar has a [scheduler](http://fullcalendar.io/scheduler/)
    -   [FullCalendar GitHub](https://github.com/fullcalendar)
        where you find the FullCalendar and the Scheduler repositories.
        plugin

    The author Adam Shaw has also produced
    [XDate](http://arshaw.com/xdate/) (GPL-2.0 and MIT)
    a JavaScript Date Library, which he no more develops.
    _last commit 2019, last release 2021_.

-   [libical](https://github.com/libical/libical/) (LPGL or MPL)
    implementation of the IETF's iCalendar Calendaring and Scheduling
    _active in 2023_
-   [moment](https://github.com/moment/moment/) (MIT License)
    Parse, validate, manipulate, and display dates in javascript.
    _active in 2022_.
-   [python icalendar](https://github.com/collective/icalendar)
    is a parser/generator of iCalendar files for use with Python.
    Debian package *python3-icalendar*, _active in 2023_.
-   [vcard](https://gitlab.com/engmark/vcard) (AGPL-3.0)
    by Victor Engmark, is a vCard validator, with a   python class and utility functions.
    _active in 2023_.
-   [vobject](https://eventable.github.io/vobject/) (Apache License)
    is a python icalendar library, intended to be a full featured Python package for
    parsing and generating vCard and vCalendar files. Debian package *python3-viobject*,
    _last version 2018_.
    -   [vobject - GitHub](https://github.com/eventable/vobject)
    -   [VObject - An iCalendar and vCard Library (presentation at PyCon 2006)
        ](http://www.python.org/pycon/2006/papers/53/)

# CalDAV protocol and servers

-   [Apple calendar server](https://github.com/apple/ccs-calendarserver) (Apache License)
    is a standards-compliant server implementing the CalDAV and CardDAV protocols.

    The project is no more longer developed and has been archived in 2020.
-   [Bedework](https://bedework.github.io/) (Apache 2.0 License)
    CalDav and CardDav java server.
    -  [bedework - GitHub](https://github.com/Bedework/bedework)
-   [Baïkal](https://sabre.io/baikal/) (GPL)
    a PHP+SQLite or MySQL CalDAV+CardDAV server.
    [Baikal GitHub](https://github.com/jeromeschneider/Baikal)
    _active in 2023._
-   [Chandler server](https://www.chandlerproject.org/project-wiki)
    (Apache License) is a CalDAV server written in java using Tomcat,
    and Derby an embedded database. Chandler also provides a client
    software: **Chandler Desktop** written in Python and C-based
    extensions.
-   [DAVIcal](http://davical.org/) (GPL)
    is a calDAV and cardDAV server.  DAVical is written in PHP and uses a PostgreSQL database.
-   [Radicale](http://radicale.org/) (GPL)
     is a CalDAV (calendar) and CardDAV (contact) server solution
     written in python.  It is in Debian.
    -    [Radicale online documentation](http://www.radicale.org/documentation)

## caldav synchronization

-   <a name="vdirsyncer"></a>[vdirsyncer](https://github.com/pimutils/vdirsyncer)
    (BSD License)
    is a python command-line tool for synchronizing calendars and addressbooks between
    a variety of CalDAV and CardDav servers and the local filesystem.

    _vdirsyncer is packaged in Debain. _active in 2023_.

    -   [vdirsyncer documentation](https://vdirsyncer.pimutils.org/en/stable/)

-   [ASynK](https://asynk.io/)
    is a contacts synchronization program that works with Microsoft Outlook, Microsoft
    Exchange Server, Google Contacts, Any standards compiant CardDAV server, and Emacs
    BBDB.

    The last release is from 2015, the development seem to be restricted to some quick
    fix commits since 2018, no issue is closed since 2020,
    -   [ASynK GitHub](https://github.com/skarra/ASynK)a
    -   [Async Wiki](https://github.com/skarra/ASynK/wiki)

## caldav/cardav client applications

-   [AgenDAV](https://github.com/adobo/agendav/) (GPL)
    a CalDAV web client in PHP+AJAX  with shared calendars support, similar to google
    calendar. _active in 2022_.
-   [khal](https://github.com/pimutils/khal) (MIT License)
    is a python calendar terminal program for viewing adding and editing events and
    calendars. Khal is build on the iCalendar and vdir (allowing the use of vdirsyncer
    for CalDAV compatibility) standards.

    Packaged in Debian, _and active in 2023_.

    -   [khal documentation](http://khal.readthedocs.org/)

-   [khard](https://github.com/lucc/khard) (GPL 3.0)
     is a python console vcard client. It creates, reads, modifies and removes vCard address book
     entries at your local machine. Khard is also compatible to the email clients mutt
     and alot and the SIP client twinkle.

     _khard_ can use {{< iref "#vdirsyncer" "vdirsyncer" >}} to synchronize with a
     CardDAV server.

     Khard is packaged in Debian,_and active in 2023_.

     -   [khard documentation](https://khard.readthedocs.io/en/latest/)

-   [PHP iCalendar](http://phpicalendar.net/) is a PHP-based iCal
    file viewer/parser.
    -   [Dreamhost Wiki: PhpIcalendar page
        ](http://wiki.dreamhost.com/PHPiCalendar)
-   [Lightning](https://www.thunderbird.net/en-US/calendar/) (	MPL 2.0)
    is a redesign of the {{< wp "Mozilla Sunbird" >}} cross platform standalone calendar
    application *obsolete since 2010* that integrates into Mozilla Thunderbird.

    Lightning uses a SQLite based storage. iCal standard files can be opened, imported,
    exported and subscribed to.

    -   {{< wp "Lightning_(software)" "Wikipedia: Lightening" >}}.

-   [todoman](https://github.com/pimutils/todoman) (ISC License)
     A simple python cli, standards-based, todo (aka: task) manager. Todos are stored
     into icalendar files, which means you can sync them via CalDAV using, for example,
     vdirsyncer.

     *todoman* is in Debian. _active in 2023_.

## Synchronization to org
-   [Worg: Google Calendar Synchronization
    ](http://orgmode.org/worg/org-tutorials/org-google-sync.html)
-   [ical2org.py](https://github.com/asoroa/ical2org.py) (GPL-3.0)
    converts an ical calendar (for instance, as exported from google calendar) into an
    org-mode document.
    It is a replacement of the awk script `ical2org.awk`.

    _It is maintained in 2023._
-   [org-gcal](https://github.com/kidd/org-gcal.el)
    allow to  Fetch google calendar event,  Post/edit org element,  Sync between Org
    and Gcal. _in elpa, active in 2023._
-   the script [vCard2org.rb](https://gist.github.com/simonthum/4145201)
    creates org-contacts entries from vCard input. Only telephone and name.
-   [org-caldav](https://github.com/dengste/org-caldav) (GPL-3.0)
    Caldav sync for Emacs Orgmode, work with owncloud, nextcloud, radicale, baikal,
    SOgo, colab and google with OAuth2 and a google application ID. It is in
    elpa. _active in 2023_.

    The main author is no longer able to maintain the repo since 2021 as stated in
    [issue #234](https://github.com/dengste/org-caldav/issues/234),
    but *jackkamm* accept to push from
    [his fork](https://github.com/jackkamm/org-caldav) and merge *some* bug fixes.

-   [org-vcard](https://github.com/flexibeast/org-vcard) (GPL-3.0)
    export and import vcards to org-mode. _in 2023 the project need a new maintainer._

## Google Calendar
-   [Google Calendar](https://www.google.com/calendar/),
    [google calendar (mobile)](https://support.google.com/calendar/answer/2465776),
    are web clients  which allow [exporting clendars as ics files
    ](ttps://support.google.com/calendar/answer/37111?hl=en) and [sharing your calendars
    ](https://support.google.com/calendar/answer/37082?hl=en).
    You can also [import](https://support.google.com/calendar/answer/37118?hl=en)
    icalendar `.ics` files in your google calendar.

# simple calendar applications
-   [List of Time Management  applications - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Other#Time_management)

-   [BORG](https://github.com/mikeberger/borg_calendar) (GPL)
    is a calendar and and scheduling application written in Java. There is an ical
    plugin.
    _active in 2023_.

    There is a [experimental CardDAV import only, an CalDAV synchronisation with _some_
    servers](https://github.com/mikeberger/borg_calendar/discussions/153) and
    an [experimental (partial) sync with google calendar / task
    ](https://github.com/mikeberger/borg_calendar/discussions/155] in borg 1.10
-   [calcurse](https://calcurse.org/) (BSD License)
    is a text-based calendar and scheduling application. It includes a
    configurable notification system and an online help system. It can import and export
    _Icalendar_ format, and export to _pcal_ appointments format.  It is an old project,
    but still actively maintained _in 2023_.
    -   [calcurse manual](http://calcurse.org/files/manual.html)
    -   [calcurse-caldav](https://calcurse.org/files/calcurse-caldav.html)
    -   [calcurse git repository](http://git.calcurse.org/calcurse.git/tree/)
    -   [calcurse - GitHub](https://github.com/lfos/calcurse) mirror of previous git
        repo, include the issue tracker and pull requests.
-   [DayPlanner](http://www.day-planner.org/) (GPL)
    a Perl program that uses Icalendar format. _DayPlanner_ last release in 2012.
    -   [DayPlanner Gitlab repository](https://gitlab.com/zerodogg/dayplanner)
.
-   <a name="etm"></a>[etm](https://github.com/dagraham/etm-dgraham)
    is a python event and task manager.

    -   [etm user manual](https://dagraham.github.io/etm-dgraham/)
-   [gcal](http://www.gnu.org/software/gcal/manual/html_node/index.html) (GPL)
    is a console-based utility that has many uses, as taught by
    [The many uses of gcal
    ](http://www.basicallytech.com/blog/index.php?/archives/97-The-many-uses-of-gcal.html)
    by Rob Newcater *2007*.

    It is quite complex but the resource file is in a custom format, and there is no
    import/export option.
    -   [gcal git repository](https://git.savannah.gnu.org/cgit/gcal.git)
-   [gcalcli](https://github.com/insanum/gcalcli) (MIT License)
    is a Python CLI application that allows you to access your Google Calendar from
    command line. _packaged in Debian; acttive in 2023._
    -   [Command-Line Cloud: gcalcli | Linux Journal
        ](https://www.linuxjournal.com/content/command-line-cloud-gcalcli)
    -   [how to use gcalcli with Conky to display the google calendar on your desktop
        ](http://www.tux-planet.fr/afficher-le-calendrier-google-sur-votre-bureau-linux/).
    -   The same subject is presented in
        [How to integrate Google Calendar in Linux desktop - Xmodulo
        ](https://xmodulo.com/integrate-google-calendar-linux-desktop.html)
-   [pal calendar](http://palcal.sourceforge.net/) (GPL-2.0)
    a command-line calendar program. It uses a custom event format (with no import or
    export), and can generate a latex and html calendar. Packaged in Debian. _last
    release 2011_
-   <a name="pcal"></a>[pcal and lcal](http://pcal.sourceforge.net/)
    (Artistic License) _pcal_ generate monthly-format an yearly-format postscript
    calendars with optional embedded text and images to mark special events.  _lcal_
    generates a postscript yearly _lunar phase_ postscript calendar. _lcal_ is no more
    developed since 2007, and _pcal_ since 2011. In 2033 _pcal_ is in Debian.

    The [Home Page](http://pcal.sourceforge.net/) list many third party programs.
-   [Pear: Date and Time packages](http://pear.php.net/manual/en/package.datetime.php)
    in [Pear manual](http://pear.php.net/manual/en/)
-   <a name="PHPIcalendar"></a>[PHPIcalendar
    ](https://sourceforge.net/projects/phpicalendar/) (GPL)
    is a PHP-based iCal file viewer/parser. The last release is in 2010 and the home
    site `phpicalendar.net` is no longer available.
    The [Dreamhost Wiki: PhpIcalendar page
    ](http://wiki.dreamhost.com/PHPiCalendar#Setting_up_a_WebDAV-enabled_Calendar_Directory)
    explains how use PhpIcalendar as webdav client.
-   [PyCalendarGen](https://github.com/jwarlander/pycalendargen) (GPL)
    is a python application that uses  uses ReportLab and mxDateTime
    to generate customizable calendar pages in PDF format. *updated in 2018*
-   [remind](https://dianne.skoll.ca/projects/remind/) (GPL-2.0)
    calendar and alarm program. It is an old project that is packaged in Debian from
    year 2000 until now, and it is still active in 2023.

    Remind is a C program with no dependencies,as well as the old postscipt converter
    *rem2ps* the companion programs *Rem2html* and
    *Rem2PDF* are written in perl and have perl dependencies; the GUI is a Tcl/TK program.

    There are many third party applications listed at the end of the
    [Home Page](https://dianne.skoll.ca/projects/remind/); some of them allow exporting
    and importing from/to icalendar and vcard.

    Debian ha s a *remind*, *reùmind-tools* and a *tkremind* package.

    -   [Remind Home Page](https://dianne.skoll.ca/projects/remind/)
    -   [Dianne Skoll / remind · Debian Salsa GitLab
        ](https://salsa.debian.org/dskoll/remind/)
    -   {{< man "remind(1)" >}}
    -   [Remind Wiki](https://dianne.skoll.ca/wiki/Remind)
    -   [Remind FAQ](https://dianne.skoll.ca/wiki/Remind_FAQ)
    -   [Remind - ArchWiki](https://wiki.archlinux.org/title/Remind)
    -   [Wyrd](https://gitlab.com/wyrd-calendar/wyrd) (GPL-2.0)
        is an ncurses-based frontend for remind written in ocaml.
        It is packaged in Debian. *active in 2023.*
        -   [Wyrd manual](https://wyrd-calendar.gitlab.io/wyrd/)
    -   [mail2rem](https://github.com/esovetkin/mail2rem)
         a small bash script for converting ics file inside your Maildir to Remind
         calendar.
-   [WebCalendar](http://www.k5n.us/webcalendar.php) is a PHP-based
    calendar which relies on a sql DBMS. _last release 2019 active in 2023_.
    -   [webcalendar - GitHub](https://github.com/craigk5n/webcalendar)

## graphical calendar applications
-   [etmtk -  event and task manager](http://people.duke.edu/~dgraham/etmtk/)
    is a python-tk application that use free-form text entries to store items in plain
    text files. It can import/export from icalendar ics format. _last release 2017_.
    See also {{< iref "#etm" "etm" >}} by the same author.

    The Debian package is *etm*.
    -   [etmtk - GitHub](https://github.com/dagraham/etm-tk),
    -   [etmtk Wiki](https://github.com/dagraham/etm-tk/wiki)
-   [gnome calendar](https://gitlab.gnome.org/GNOME/gnome-calendar)
    is a GTK4 application for gnome desktop. In Debian and Flathub.
-   [wmcalendar](http://wmcalendar.sourceforge.net/) (GPL)
    is a dockapp with monthly view and interface to iCal based calendars.
    _last release 2007_

# Address Books

-   Wikipedia {{< wp "Category:Personal information managers" >}},
    {{< wp "List of personal information managers" >}},
    {{< wp "Comparison of notetaking software" >}}, {{< wp "Outliner" >}},
    {{< wp "Outline Processor Markup Language" >}}
-   [List of Contact Management applications - ArchWiki
    ](https://wiki.archlinux.org/title/List_of_applications/Other#Contacts_management)

-   <a name="abook"></a>[abook](http://abook.sourceforge.net/) (GPL-3.0)
    text-based addressbook program designed to use with mutt mail client. Abook is
    written in C + Ncurses.  It can import/export to ldif, csv, palm csv and export to
    html, vcard, plain text.

    The [source forge git repository](https://sourceforge.net/p/abook/git/)
    has maintenance commits in December 2021 and a last release 0.6.1 in 2015.

    The github [hhirsh/abook](https://github.com/hhirsch/abook/)
    repository is forked from the previous at commit `5840fce` in 2014, and is active in
    2023.

    The patched abook from Debian in the
    [abook - Salsa.debian](https://salsa.debian.org/rhonda/abook/)
    repository is a debianized patched fork of the sourceforge repository, at time of
    writing this note in 2023, the upstream version is 0.6.1.

    -   [python-abook](https://github.com/jspricke/python-abook) (GPL-3.0)
        is a Python script to convert betwen vcard and abook. _active in 2022_.
-   [directory](http://geuz.org/directory/)
    is a macro package for LaTeX and BibTeX that facilitates the
    construction, the maintenance and the exploitation of an address
    book like database. _2004_
-   [Doneyet](https://github.com/gtaubman/doneyet) (MIT License) is an ncurses
    based hierarchical todo list manager written in C++. *commits in 2020*
-   [GooBook](https://gitlab.com/goobook/goobook) (GPL)
    is a python program to access Google contacts from the command-line
    or mutt.

    Gobook is packaged in Debian, *and active in 2023, looking for a new maintainer*
-   [hnb](http://hnb.sourceforge.net) _hierarchical notebook(hnb)_
    (GPL) is a curses program to structure in one
    place, addresses, to-do lists, ideas, ... hnb is no longer maintened since 2003, and
    do not support UTF-8.

    It is still available in debian/ubuntu but *though the current Debian maintainer
    tries to keep hnb in a usable and releasable state he does not plan to add many new
    features*.
-   [The Little Brother's Database (lbdb)](http://www.spinnaker.de/lbdb/) (GPL-2.0)
    is a client program written in shell that can query many information database on
    your computer.
    You can query your _passwd_ file or any password source accepting _getent_, your
    _pgp2_ or _gpg_ files, a _fido_ database, an _NIS_ server, _Tk addressbook_
    database, the mutt aliases, the pine address book, the palm address book _if you
    have the perl module Palm::PDB_, a _gnomecard_ database, the _emacs bbdb_, any _ldap
    server_, the _evolution_ address book, _vcf_ databases, the _abook_ database,
    _goobook_ .
    It can also extract addresses from your mails,
    -   [lbdb - Github](https://github.com/RolandRosenfeld/lbdb)
-   [Osmo](https://osmo-pim.sourceforge.net/)
    a GTK+ personal organizer, which
    includes calendar, tasks manager and address book modules. It requires
    only _GTK+_ and _LibXML 2_.

    To add more functionalities the Debian package add _libnotify_,
    *libwebkit2gtk*, _libical_, ...
    It is packaged in Debian, _active in 2023_

    -   [Osmo Documentation - Wikibooks](https://en.wikibooks.org/wiki/Osmo_Documentation)
-   [PHP Address Book](http://sourceforge.net/projects/php-addressbook/) (AGPL-3)
    web-based address & phone book, contact manager, organizer.  vCards, LDIF, Excel,
    iPhone, Gmail & Google-Maps supported. PHP / MySQL based.
    _last update 2016_.
    -   [GitHub - php-addressbook](https://github.com/chatelao/php-addressbook)

# BBdb {#bbdb}
The old BBDB 2.x changed from maintainer and atransition to BBDB-3 started in 2010.

Many scripts, importers, exporters for BBDB-2, have not been updated and are no longer
usable with BBDB-3.

-   [BBDB-3 Savannah Git repository
    ](https://git.savannah.nongnu.org/cgit/bbdb.git/tree/)
    _active in 2022_.
-   [GNU ELPA - bbdb](https://elpa.gnu.org/packages/bbdb.html)
    this page reproduce the current README of BBDB, there is not yet _in 2023_ a user
    manual for BBDB-3.
-   [BBDB-2 User Manual](http://bbdb.sourceforge.net/bbdb.html)
-   [EmacsWiki: Category Bbdb](https://www.emacswiki.org/emacs/CategoryBbdb)
    -   [EmacsWiki Bbdb Importers](http://www.emacswiki.org/emacs/BbdbImporters),
    -   [EmacsWiki Bbdb Exporters](http://www.emacswiki.org/emacs/BbdbExporters),
    -   [EmacsWiki: Bbdb Export Import Sync
        ](http://www.emacswiki.org/emacs/BbdbExportImportSync)
-   [tohojo/bbdb-vcard](https://github.com/tohojo/bbdb-vcard)
    vCard Import and Export for The Insidious Big Brother Database (BBDB)

    This is a fork works with BBDB-3, from a script for BBDB-2. _updates in 2021_.



<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
