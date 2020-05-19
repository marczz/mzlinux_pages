---
title: Documents management.
---


# References
-   [ArchWiki: list of applications - Documents
    ](https://wiki.archlinux.org/index.php/List_of_applications/Documents)
-   Wikipedia {{< wp "Comparison of reference management software" >}}

# Applications
-   {{< wp "Referencer" >}} is a GNOME application to organize documents or
    references, and generate a BibTeX file. It is tagetet to pdf
    papers more than books, so it uses
    {{< wp "Digital object identifier"  "DOI (Digital object identifier)" >}} rather than
    {{< wp "ISBN" >}}. It is in Debian.
-   [cb2Bib](http://www.molspaces.com/cb2bib/)
    is a open source application for extracting unformatted, or unstandardized
    bibliographic references from email alerts,
    journal Web pages, and PDF files.
-   [bibutils](http://sourceforge.net/p/bibutils/home/Bibutils/)
    is a set of script to convert between bibliographic data formats:
    BibTeX, COPAC, EndNote refer, EndNote XML, Pubmed XML, ISI web of
    science, US Library of Congress MODS XML, RIS, and Word 2007
    bibliography. It is in debian.
-   {{< wp "Bebop_(software)"  "Bebop (BibTeX Publisher)" >}} is an Ajax/PHP
    BibTeX front-end that allows browsing by author, year, document
    type, topic and keywords. It uses a single BibTeX file and don't
    uses a DBMS.<br/>
    Bibliographic entries can be exported as BibTeX through {{< wp "unAPI" >}},
    making it compatible with Zotero.
-   {{< wp "Zotero" >}} (AGPL)
    is a reference management software to manage bibliographic data
    and related research materials (such as PDF files).
    Features include web browser integration, online syncing,
    generation of in-text citations, footnotes and bibliographies,
    as well as integration with word processors.
    -   [Zotero Home](https://www.zotero.org/)
    -   [Zotero Bookmarklets](https://www.zotero.org/downloadbookmarklet)
        for desktop and mobile browsers.

# Read List {#read_list}
## Web services
There are some web service that use to keep a list of your read list
url, and transform and clean the articles such it can be easily read
offline on any device computer, smartphone or ebook readers.

-   {{< wp "Instapaper" >}} is a tool for saving web pages to read later on
    one's Android or iOS device, computer, ereader, or smartphone.

    You can save your article to epub, customize the article by
    choosing font, font size, line and paragraph spacing, colour,
    organize articles in folders.

    Articles can be [saved](https://www.instapaper.com/save/browser)
    with bookmarklets, email, IFTT with
    [many recipes](https://ifttt.com/instapaper), or dedicated app.

    The basic web service is free,
    some web advanced features are subscription based.
    The premium feature for 3$/mont offers illimited highlight, and
    full text search.

-   {{< wp "Pocket_(application)"  "Pocket" >}} is an application and service for
    managing a reading list of articles from the Internet. It is
    available for OS X, Windows, iOS, Android, Windows Phone,
    BlackBerry, Kobo eReaders, and web browsers.

    You can save the browsed page, with a dedicated application, a
    browser extension or bookmarklets.

    You can choose the font size, and tag articles.

    The web service is free the mobile application are
    advertissement-paid, there is also a paid subscription service
    called Pocket Premium which allows full text search, unlimited
    highlights, ad free in the web app, and allow to save the content
    of articles, so they stay available even if they are no more
    published on the web.

-   {{< wp "Readability_(service)"  "Readability" >}}
    which replaced {{< iref "#readability" "Readability Bookmarklet" >}}
    was closed on December 10, 2016 see {{< iref "#readability" "below" >}}

-   [Wallabag](https://wallabag.org/)
    extracts the article's content without artefacts, and save it for
    later reading. It allows also {{< wp "Web annotation" >}} of the saved
    pages. There are mobile applications for ios, android, pocketbook,
    kobo, kindle; and browsers plugins for Firefox, Chrome, Opera.
    It provides RSS feeds for each article status.

    You can import your reading list from other services Pocket,
    Readability, Instapaper, Pinboard, Firefox or Chrome; and export
    it to PDF, ePUB, .mobi, JSON, CSV, txt or HTML.

    You can install it on your server or shared hosting or on use a
    wallabag instance.
    -   [Wallabag Documentation](https://doc.wallabag.org/)
    -   [GitHub - Wallabag](https://github.com/wallabag/wallabag)
    -   [wallabag.it](https://www.wallabag.it/)
        is a wallabag service, you can register for 9€ / year
    -   [Framabag](https://framabag.org) is a free instance
        _with limited page number_ of wallabag proposed by
        [Framasoft](https://framasoft.org/).
    -   [Wallabag sur votre Kobo en un clic
        ](https://chabotsi.fr/blog/wallabag-sur-votre-kobo-en-un-clic.html).
        to use with this [script update
        ](https://san.heraut.eu/2016/09/29/wallabag-solution-libre-lecture-differee-web/).

## Readability Software {#readability_software}

Most browsers offer a _reader view_ that offer an uncluttered view of
the page like the builtin [Firefox Reader View
](https://support.mozilla.org/en-US/kb/firefox-reader-view-clutter-free-web-pages)
that you activate in clicking on the small book on the right end of
the URL form. When in Reader mode you can tweak the font, background
color, line width and column size with the __Aa__ button on the left
bar.

On Chrome there are many extensions to remove adds and distractions
from the web page, like
[Mercury Reader
](https://mercury.postlight.com/reader/)
 [Just Read
](https://github.com/ZachSaucier/Just-Read),
_EasyReader_, _Read Mode_, _Reader View_, _Chrome
Reader View_ (same then _Firefox Reader View_), _Purify_, _Outline_
and more ...

In Safari there is now a [builtin Reader Mode
](http://www.theregister.co.uk/2010/06/08/safari_reader_based_on_open_source_project/)
based on {{< iref "#readability" "Readability plugin" >}},
this buton is available as well on Mac OSX and on IOS.

There are also many open source libraries for cleaning feeds, or web
pages.

_Arc90 Labs_ produced the _Readability_ bookmarklet to remove the clutter around what
you're reading. They replaced it later with a whole web service at
http://www.readability.com, and five years latter abandoned it. They propose to switch
to _Mercury_ and the
[Mercury Reader Chrome plugin](https://mercury.postlight.com/reader/).

<a name="readability"></a>There are many forks of the _Readability_ bookmarklet.

-   [The original source of readability
    ](https://code.google.com/archive/p/arc90labs-readability/source/default/source)
    is still available on Google Code archive.
-   [ejucovy readability
    ](https://github.com/ejucovy/readability/tree/gh-pages)
    is a copy of the Readability bookmarklet from _Arc90 Labs_.
    on <http://ejucovy.github.io/readability/> you find the bookmarklet
    that you can add to your browser.

-   [bndr/node-read  npm](https://github.com/bndr/node-read)
    Based on Arc90's readability project using cheerio engine.
-   [luin/readability npm](https://github.com/luin/readability) (Apache Licence)
    a Node library to turn any web page into a clean view.  using jsdom to parse HTML
    instead of cheerio.
    There is an active fork
    [ruguoapp/readability - dev branch
    ](https://github.com/ruguoapp/readability/tree/dev).

FiveFilters first used a
[PHP Port of Arc90’s Readability](http://www.keyvan.net/2010/08/php-readability/)
to perform
[Content Extraction](http://www.keyvan.net/2011/03/content-extraction/)
they later produced a new tool
<a name="full-text_rss"></a>[Full-Text RSS](http://fivefilters.org/content-only/)
which is
[introduced in this help article
](http://help.fivefilters.org/customer/en/portal/articles/225363-introduction).

You can use the form at the Head of the
[Full-Text RSS page](http://fivefilters.org/content-only/),
it gives a limited use of Full-text RSS with 1-3 items per feed, no json output , and an
extra Link to FiveFilters.org. The self hosted app cost (one time payement) 35€ there
are also an FiveFilters hosted version from 4€ / month.
See also the [request parameters
](http://help.fivefilters.org/customer/en/portal/articles/226660-usage-and-request-parameters).



-   [fivefilters php-readability (Apache License)
    ](https://bitbucket.org/fivefilters/php-readability/src/master/)
    is a PHP port of Arc90's original Javascript version of
    Readability.
-   [fivefilter full-text-rss source on Bitbucket  (Apache License)
    ](https://bitbucket.org/fivefilters/full-text-rss/src/master/)
    this is the previous version of the software, the source of the
    latest which power the [FiveFilters Full-Text Rss page
    ](http://fivefilters.org/content-only/) are not available.


-   [j0k3r/php-readability  (Apache License)
    ](https://github.com/j0k3r/php-readability) is a fork of
    FiveFilters php-readability.
-   [andreskrey/readability.php
    ](https://github.com/andreskrey/readability.php).
    is a distinct port to php of Arc90 Readability.js.

FiveFilters also produce
[pdf-newspaper](http://fivefilters.org/pdf-newspaper/)
which can produce a 2-column A4/Letter PDF, a single-column A5 PDF, or
an editable HTML output with a print stylesheet from web articles and
news feeds. A alimited use with a max of 10 pages per feed and 4
full-text fetches per feed is available with the form at the top of
the [pdf-newspaper Home Page](http://fivefilters.org/pdf-newspaper/)
you can remove these limitation for 24€ / year or self-host it for
20€ one-shot .

An other application to grab the texts of feeds and make it readable is
[f43.me](https://f43.me/) (MIT License) it can use for uncluttering pages either a fork
of {{< iref "#full-text_rss" "Full-Text RSS" >}} named
[j0k3r/graby](https://github.com/j0k3r/graby) (MIT License) or the
[Mercury Web Parser API](https://github.com/postlight/mercury-parser).

As the author [Jérémy Benoist](https://github.com/j0k3r) is also a developper of
[Wallabag](https://github.com/wallabag/wallabag) the parsing of articles is similar in
the two products.

-   [GitHub - f43.me](https://github.com/j0k3r/f43.me).


[croqaz/clean-mark](https://github.com/croqaz/clean-mark) (MIT License)
is a Node package to convert a blog article into a clean Markdown text file.
-   [npm clean-mark](https://www.npmjs.com/package/clean-mark).


[Newspaper3k](http://newspaper.readthedocs.io/en/latest/) (MIT License)
is a python 3k module for article scraping & curation.
-   [GitHub - codelucas/newspaper](https://github.com/codelucas/newspaper)

<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
