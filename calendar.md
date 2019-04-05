---
title: Calendar and Address Book
---

{{% toc /%}}

See also {{< iref "app_tasks" "Tasks Management" >}}
and {{< iref "org" "Org Mode" >}}

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
-   [hCalendar](http://microformats.org/wiki/hcalendar) and
    [Hcard](http://microformats.org/wiki/hcard) are simple, open,
    distributed calendaring and events and contact information formats,
    based on the iCalendar and Vcard standards. There are parts of the
    HTML5 extension [microformats](http://microformats.org), see also
    [Microformats | HTML5 Doctor
    ](http://html5doctor.com/microformats/).
-   [X2V](http://suda.co.uk/projects/X2V/) is an implementation of an
    XSLT file to transform and hCard/hCalendar encoded XHTML file into
    the corresponding vCard/iCalendar file.
-   [iCalShare](http://www.icalshare.com/) directory of shareable
    calendars on the web.
-   [Calendar FAQ](http://www.tondering.dk/claus/calendar.html),
-   [Sources for Time Zone](http://www.twinsun.com/tz/tz-link.htm),
-   [éphémérides du bureau des longitudes](http://www.bdl.fr/ephemeride.html).



# icalendar, CalDAV, CardDAV libraries
-   Wikipedia:
    {{< wp "CalDAV" >}},
    {{< wp "CardDAV" >}},
    {{< wp "Comparison of CalDAV and CardDAV implementations" >}}.

-   [cardDAV PHP](https://github.com/graviox/CardDAV-PHP) (affero GPL)
    by Christian Putzke,
    is a simple CardDAV client library written in PHP + CURL. It is used
    in the
    [Roundcube CardDAV plugin](https://github.com/graviox/Roundcube-CardDAV).
    _last commit 2012_.
-   [libical](https://github.com/libical/libical/) Open Source
    implementation of the IETF's iCalendar Calendaring and Scheduling
    _active in 2015_
-   The [PyPi: icalendar package
    ](https://pypi.python.org/pypi/icalendar)
    is a parser/generator of iCalendar files for use with Python.
    [GitHub: Icalenda](https://github.com/collective/icalendar)).
    _active in 2015_.
-   [Apple's Calendar Library](http://www.apple.com/ical/library/)
    Apple's library of .ics files
-   [vobject](http://vobject.skyhouseconsulting.com/) (Apache
    License) is a python icalendar library, intended to be a full
    featured Python package for parsing and generating vCard and
    vCalendar files. It is reviewed in
    [VObject - An iCalendar and vCard Library (presentation at PyCon 2006)
    ](http://www.python.org/pycon/2006/papers/53/) _last version 2009_
-   [vcard](https://github.com/l0b0/vcard) (GPL)
    by Victor Engmark _l0b0_,
    is a vCard validator, with a   python class and utility functions.
    _active in 2015_.
-   [caldav](http://pythonhosted.org/caldav/) is a simple calDAV
    python library. [pypi: caldav](https://pypi.python.org/pypi/caldav)
-   [CalDAV Clieent Library
    ](http://trac.calendarserver.org/wiki/CalDAVClientLibrary)
    (​Apache License) from the Apple calendar Server.
-   [dhtmlxScheduler](http://www.dhtmlx.com/docs/products/dhtmlxScheduler/)
    (GPL, proprietary _PRO_ version) is a JavaScript event calendar
    that allows you to add a Google-like scheduler to your web app or
    website.
-   [FullCalendar](http://fullcalendar.io/) (MIT license)
    is a jQuery plugin that provides a full-sized, drag & drop
    calendar.
    The author Adam Shaw has also produced
    [XDate](http://arshaw.com/xdate/)
    a JavaScript Date Library.

    -   FullCalendar has a [scheduler](http://fullcalendar.io/scheduler/)
        plugin
    -   [FullCalendar GitHub](https://github.com/fullcalendar)
        where you find the FullCalendar and the Scheduler repositories.

## CalDAV protocol and servers

-   [CalDAV](http://caldav.calconnect.org/ "caldav.calconnect.org the CalDAV website")
    is a calendaring and scheduling client/server protocol designed to
    allow users to access calendar data on a server, and to schedule
    meetings with other users on that server or other servers.
-   The CalDAV Access protocol is an extension of
    the {{< iref "webdav" "WebDAV Protocol" >}},
    it has been published as
    [RFC 4791](http://tools.ietf.org/html/rfc4791 "ietf.org rfc4791").
-   [Apple calendar server](http://trac.calendarserver.org/)
    is a standards-compliant server implementing the CalDAV and CardDAV protocols.
    It is in Debian and has heavy python dependencies.
-   [Bedework](https://www.apereo.org/bedework) is
    an Open Source CalDav server written in java.
-   [Baïkal](http://baikal-server.com/) (GPL)
    a PHP+SQLite or MySQL CalDAV+CardDAV server.
    [Baikal GitHub](https://github.com/jeromeschneider/Baikal)
    _active in 2015_
-   [Dingo](http://andrew.triumf.ca/dingo/ "andrew.triumf.ca dingo")
    is a CalDAV compatible server using MySQL, written in Perl as a CGI
    script. *Dingo is not fully RFC 4791 compliant*.
-   [Chandler server](http://chandlerproject.org/ "chandlerproject.org")
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

# caldav client applications

-   [AgenDAV](http://agendav.org/) (GPL)
    a CalDAV web client in PHP+AJAX  with shared calendars support.
    [AgenDAV GitHub](https://github.com/adobo/agendav/),  _active in 2015_.
-   {{< iref "#asynk" "Asynk" >}} is a caldav client.
-   [CardDavMATE](http://www.inf-it.com/open-source/clients/carddavmate/)
    (Affero GPL)
    is a JavaScript+jQuery CardDAV web client.
-   [jqCalDAV](http://boxacle.net/jqcaldav/)
    a jquery calDAV client for html5 browsers. _2012_
-   [jquery-week-calendar
    ](https://github.com/themouette/jquery-week-calendar)
    A weekly calendar plugin based on jquery and jquery-ui. [Demo
    ](http://themouette.github.com/jquery-week-calendar/weekcalendar.html)
    [Google Group](http://groups.google.com/group/jquery-week-calendar).
    _2012_
-   [khal (GitHub)](https://github.com/geier/khal)
    is a calendar program for the terminal for viewing,
    adding and editing events and calendars. Khal is build on the
    iCalendar and vdir (allowing the use of vdirsyncer for CalDAV
    compatibility) standards.
    -   [khal documentation](http://lostpackets.de/khal/)
-   [PHP iCalendar](http://phpicalendar.net/) is a PHP-based iCal
    file viewer/parser.
    -   [Dreamhost Wiki: PhpIcalendar page
        ](http://wiki.dreamhost.com/PHPiCalendar)
-   [pycarddav (GitHub)](https://github.com/geier/pycarddav)
    is a cli __carddav__ client (for use with mutt etc.)
-   [Sunbird](http://www.mozilla.org/projects/calendar/sunbird/) is
    a cross platform standalone calendar application based on Mozilla's
    XUL user interface language;
    [Lightning](http://www.mozilla.org/projects/calendar/lightning/) is
    a redesign of the Sunbird that integrates into Mozilla Thunderbird.
    Sunbird/Lightning uses a SQLite based storage, iCal standard files
    can be opened, imported, exported and subscribed to.

## Synchronization to org
-   [Worg: Google Calendar Synchronization
    ](http://orgmode.org/worg/org-tutorials/org-google-sync.html)
-   [ical2org.py
    ](https://github.com/asoroa/ical2org.py) converts an ical calendar (for instance, as exported
    from google calendar) into an org-mode
    It is a replacement of the awk script
-   the script [vCard2org.rb
    ](https://gist.github.com/simonthum/4145201)
    creates org-contacts entries from vCard input.
    Only telephone and name.
-   [org-caldav](https://github.com/dengste/org-caldav)
    Caldav sync for Emacs Orgmode, work with owncloud (no longer
    Google), it is in elpa.
-   [org-vcard](https://github.com/flexibeast/org-vcard)
    export and import vcards to org-mode.



## Asynk {#asynk}
-   [ASynK: Awesome Sync (by Karra): ASynK User Manual
    ](http://karra-asynk.appspot.com/doc/asynk/asynk.html),
    [ASynK GitHub](https://github.com/skarra/ASynK)
-   I use the following profils gcbbfournisseurs, gcbbfriends,
    gcbbsante, gcbbdharma
-   To sync we do:

        ~/share/software/ASynK/asynk.py --op=sync \
        --name gcbbfournisseurs  --log debug

## Google Calendar
-   [Google Calendar](https://www.google.com/calendar/),
    [google calendar (mobile)](https://www.google.com/calendar/m?source%3Dmobileproducts&pli%3D1),
    are web clients with export/import to csv or vcard.

### ics import {#gcal_ics_import}

To import properly an icalendar ics file in google calendat, the
header should set the encoding, otherwise it is supposed to be
ascii and all UTF-8 characters are replaced by a question mark.

We check the header with

    curl -I http://url/to/icalendar.ics

And it should answer:

    Content-Type: text/calendar; charset=utf-8

Otherwise you should modify the header, in apache it is done by adding
in a `<Directory>` section or in the `.htaccess` file of the ical
repository.

    AddType 'text/calendar; charset=UTF-8' .ics

# simple calendar applications
-   [BORG](http://borg.mbcsoft.com) (GPL)
    is a calendar and and  scheduling application written in
    Java. There is an ical  plugin.
    _active in 2015_.
-   [calcurse](http://calcurse.org/)
    (BSD License) is a text-based calendar and scheduling
    application. It includes a configurable notification system and an
    online help system. It can import and export _Icalendar_ format,
    and export to _pcal_ appointments format.
    It is an old project, but still actively maintained _in 2017_.
    -   [calcurse manual](http://calcurse.org/files/manual.html)
    -   [calcurse git repository
        ](http://git.calcurse.org/calcurse.git/tree/)
-   [clcal](http://www.hyborian.demon.co.uk/clcal/)
    a basic command-line calendar written in C. The entries are in a custom format
    and there is no import/export option. _The last resource file is 2008_.
-   {{< wp "Chandler_(software)"  "Chandler" >}}
    a calendar sharing application  _dead since 2006_
-   [DayPlanner](http://www.day-planner.org/) (GPL)
    a Perl program that uses Icalendar format.
    [DayPlanner GitHub repository
    ](https://github.com/zerodogg/dayplanner)
    _DayPlanner_ slowed developement in 2012, and stopped in 2015.
-   [etmtk -  event and task manager
    ](http://people.duke.edu/~dgraham/etmtk/)
    is a python-tk application that use free-form text entries to
    store items in plain text files. It can import/export from
    icalendar ics format.
    [etmtk is stored in GitHub](https://github.com/dagraham/etm-tk),
    where you also find the [etmtk Wiki
    ](https://github.com/dagraham/etm-tk/wiki).
-   [gcal](http://www.gnu.org/software/gcal/manual/html_node/index.html) (GPL)
    is a console-based utility that has many uses, as taught by
    [The many uses of gcal
    ](http://www.basicallytech.com/blog/index.php?/archives/97-The-many-uses-of-gcal.html)
    by Rob Newcater.
    It is quite complex but the resource file is in a custom format, and there is no import/export option.
-   [gcalcli](https://github.com/insanum/gcalcli)
    (MIT License) is a Python application that allows you to access
    your Google Calendar from a command line.
    -   [Command-Line Cloud: gcalcli | Linux Journal
        ](http://www.linuxjournal.com/content/command-line-cloud-gcalcli?page%3D0,1)
    -   This [article teach you how to use gcalcli with Conky
        ](http://www.tux-planet.fr/afficher-le-calendrier-google-sur-votre-bureau-linux/).
        to display the google calendar on your desktop by using a provided
        configuration file.
    -   The same subject is presented in
        [How to integrate Google Calendar in Linux desktop - Xmodulo
        ](http://xmodulo.com/integrate-google-calendar-linux-desktop.html)
-   [pal calendar](http://palcal.sourceforge.net/) a command-line
    calendar program. It uses a custom event format (with no import),
    and can generate a latex and html calendar. _last release 2008_
-   <a name="pcal"></a>[pcal and lcal](http://pcal.sourceforge.net/)
    (Artistic License) _pcal_ generate monthly-format an yearly-format
    postscript calendars with optional embedded text and images to
    mark special events.  _lcal_ generates a postscript yearly _lunar
    phase_ postscript calendar. _lcal_ is no more developed since
    2007, and _pcal_ since 2011. _pal_ is in Debian.
-   [Pear: Date and Time packages](http://pear.php.net/manual/en/package.datetime.php)
    in [Pear manual](http://pear.php.net/manual/en/)
-   [PHPIcalendar](http://phpicalendar.net/documentation/index.php/Main_Page)
    <a name="PHPIcalendar"></a>(GPL) is a PHP-based iCal file viewer/parser.
    The [Dreamhost Wiki: PhpIcalendar page
    ](http://wiki.dreamhost.com/PHPiCalendar#Setting_up_a_WebDAV-enabled_Calendar_Directory)
    explains how use PhpIcalendar as webdav client.
-   [PyCalendarGen]](https://github.com/jwarlander/pycalendargen) (GPL)
    is a python application that uses  uses ReportLab and mxDateTime
    to generate customizable calendar pages in PDF format.
-   [remind](http://www.roaringpenguin.com/penguin/open_source_remind.php)
    calendar and alarm program.
-   [SimpleAgenda](http://coyote.octets.fr/simpleagenda/)
    is an objective-C Gnustep application, that can read Icalendar
    format. _not updated since 2012_.
-   [WebCalendar](http://www.k5n.us/webcalendar.php) is a PHP-based
    calendar which relies on a sql DBMS. _Minimal maintenance - last release in 2013_
-   [wmcalendar](http://wmcalendar.sourceforge.net/) (GPL)
     is a dockapp with monthly view and interface to iCal based
     calendars.

# Address Books

-   Wikipedia {{< wp "Category:Personal information managers" >}},
    {{< wp "List of personal information managers" >}},
    {{< wp "Comparison of notetaking software" >}}, {{< wp "Outliner" >}}, {{< wp "Outline Processor Markup Language" >}}
-   <a name="abook"></a>[abook](http://abook.sourceforge.net/) (GPL)
    text-based addressbook program
    designed to use with mutt mail client. Abook is written in C + Ncurses.
    It can import/export to ldif, csv,  palm csv
    and export to html, vcard, plain text. _active in 2015._
    - [gmail-abook-contact-converter](http://code.google.com/p/gmail-abook-contact-converter/)
      is a short python script to convert a vCard file (.vcf) of exported Gmail contacts
      into abook's addressbook format.
    -   [python-vcf2abook](https://github.com/frankhjung/python-vcard2abook)
        is a Python script to convert gmail addresses in vcard format to abook.
-   [directory](http://geuz.org/directory/)
    is a macro package for LaTeX and BibTeX that facilitates the
    construction, the maintenance and the exploitation of an address
    book like database. _2004_
-   [Doneyet](http://code.google.com/p/doneyet/) (GPL) is an ncurses
    based hierarchical todo list manager written in C++._not updated
    since 2009_
-   The [GPE Palmtop Environment](http://gpe.linuxtogo.org/) includes a
    PIM suite._It is no longer active_<br />
    There is a
    [Gpe synchronisation interface](http://www.handhelds.org/moin/moin.cgi/GpeSync)
    via [Multisync](http://multisync.sourceforge.net/) or
    [Opensync](http://www.opensync.org/).
-   [GooBook](http://pypi.python.org/pypi/goobook/) (GPL)
    is a python program to use Google contacts from the command-line
    or mutt.
    _A pypi release in 2014_.
-   [hnb](http://hnb.sourceforge.net) _hierarchical notebook(hnb)_
    (GPL) is a curses program to structure in one
    place, addresses, to-do lists, ideas, ... hnb is no longer maintened since 2003,
    but is still available in debian/ubuntu.
-   [The Little Brother's Database (lbdb)](http://www.spinnaker.de/lbdb/) is a client program
    written in shell that can query many information database on your computer.
    You can query your _passwd_ file or any password source accepting _getent_,
    your _pgp2_ or _gpg_ files, a _fido_ database,
    an _NIS_ server, _Tk addressbook_ database, the mutt aliases, the pine address book,
    the palm address book _if you have the perl module  Palm::PDB_, a _gnomecard_ datatbase,
    the _emacs bbdb_, any _ldap server_, the _evolution_  address book, _vcf_ databases,
    the _abook_ database.
    It can also extract addresses from your mails,
-   [Osmo](http://clayo.org/osmo/) a GTK+ personal organizer, which
    includes calendar, tasks manager and address book modules. It requires
    only _GTK+_ and _LibXML 2_. To add more functionalities you may need _libnotify_,
    _libgtkhtml2_, _libical_, _Libtar_, _libgringotts_,
    _libsyncml_. It is packaged in Debian, _active in 2015_
-   [PHP Address Book | SourceForge.net
    ](http://sourceforge.net/projects/php-addressbook/)
    web-based address & phone book, contact manager, organizer.
    vCards, LDIF, Excel, iPhone, Gmail & Google-Maps supported. PHP /
    MySQL based.
    [GitHub - php-addressbook](https://github.com/chatelao/php-addressbook)

# BBdb {#bbdb}
-   [Insidious Big Brother Database User Manual
    ](http://bbdb.sourceforge.net/bbdb.html)
-   [EmacsWiki Bbdb Importers
    ](http://www.emacswiki.org/emacs/BbdbImporters),
    [EmacsWiki Bbdb Exporters
    ](http://www.emacswiki.org/emacs/BbdbExporters),
    [EmacsWiki: Bbdb Export Import Sync
    ](http://www.emacswiki.org/emacs/BbdbExportImportSync)
-   [bbdb-vcard-import.el
    ](http://www-pu.informatik.uni-tuebingen.de/users/crestani/downloads/bbdb-vcard-import.el)
    imports all vCards that are in a file, just do
    `M-x bbdb-vcard-import RET <filename> RET`.
    It looks for vCards within `begin:vcard` and `end:vcard` tags in the
    file.
-   [Lisp:bbdb-vcard-export.el
    ](http://www.emacswiki.org/emacs/bbdb-vcard-export.el)
    write your entire BBDB into a directory, one entry per line. Per
    default `M-x bbdb-vcard-export-update-all` writes the data encoded
    in UTF-16, because that’s what the Apple Addressbook in OSX seems
    to expect. If you want to specify a different encoding, just use a
    prefix argument: `C-u M-x bbdb-vcard-export-update-all` and you
    will be asked for another encoding. The default BBDB file encoding,
    ISO 2022 JP is probably not what you want.



# Calendar Notes

## Google calendar
-   [About the 'Quick Add' feature - Calendar Help
    ](https://support.google.com/calendar/answer/36604?hl%3Den)
    Example:

        Language Class every Wednesday 7-8pm for 5 months
        Mom's birthday June 19 yearly
        Manicure on 9/1 every mont
        Running w/ Pat 2:15 tomorrow for 45 minutes
        Running w/ Pat 2:15 - 3 pm tomorro

    If you enter a time with no date, Quick Add will create the event
    on the earliest date that puts the event in the future; the present
    day if the time is later, or the next day if the time has already
    passed: `Volleyball at 5pm`


<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
