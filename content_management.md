<!--
.. description:
.. date: 2016-01-26
.. slug: content_management
.. tags:
.. link:
.. book: mzlinux
.. title: Content Management
-->

[TOC]

# content management system (CMS)

A **content management system (CMS)** is a computer software system
for organizing and facilitating collaborative creation of documents
and other content. We call **content management framework** an
application programming interface for creating a customized content
management system. I have only few links of general CMS.

Look also at
[Wiki section](#wikis "Internal reference"),
[Blogger](#bloggers "Internal reference")
and
[Web Frameworks](/node/python_web#web_frameworks "Internal reference").
For a broader view look at the following wikipedia pages.

- Wikipedia :
  [w:Content management system],
  [w:Content management framework],
  [w:Comparison of content management systems],
  [w:Web framework].
- [Drupal](http://www.drupal.org/) is a CMS with PHP +
  Mysql/Postgresql which include a lot of modules which provide a
  wide assortment of features. ref:
  [Drupal Wikipedia Page](http://en.wikipedia.org/wiki/Drupal)
- [PyLucid](http://www.pylucid.org) is a cms in python that uses django an allows
  text marked up in Textile, Markdown, ReStructuredText, creole, plain html
- [TextPattern](http://www.textpattern.com/ "textpattern.com Home")
  is a CMS in php+mysql that use the structured text language
  [Textile
  ](http://textbook.textpattern.net/wiki/index.php?title=Textile).
- [WOLFCMS](http://www.wolfcms.org/) (GPL)
  is a CMS written in PHP with storage in MySQL, PostgreSQL, or SQLite.
- Some popular CMS:
  [PhpNuke](http://phpnuke.org), [PostNuke](http://www.postnuke.com),
  [openphpnuke](http://www.openphpnuke.com/),
  [SPIP](http://www.spip.net/),
  [NPDS](http://www.npds.org/), [guppy](http://www.freeguppy.org/),
  [Xoops](http://www.frxoops.org/).

# Content Delivery network (CDN)
For content delivery an alternative is P2P content delivery in which
clients provide resources as well as use them.

-   Wikipedia: [w:Content delivery network] (CDN)

-   [w:Cloudflare] is a CDN with advanced DDoS protection.
    It works by reverse proxying your Site. _Cloudflare_ offer a
    [Free plan](https://www.cloudflare.com/plans/)
    for small personal websites or
    blogs, with Limited DDoS protection, and Shared SSL certificate.
    -   [CloudFlare Home](https://www.cloudflare.com/)
-   [CacheP2P](http://www.cachep2p.com/) is a P2P cache in javascript.

# Wikis {#wikis}
This page is about **Wikis** understood as
*simple, human readable, markup languages* this is not limited to
the websites an in
[strict definition of wikis](http://en.wikipedia.org/wiki/Wiki).

-   [Wiki](http://en.wikipedia.org/wiki/Wiki) page from wikipedia,
    they also provide a
    [Comparison of wiki software](http://en.wikipedia.org/wiki/Comparison_of_wiki_software)
    and [w:Comparison of wiki hosting services]
-   [WikiWikiWeb](http://c2.com/cgi/wiki?WikiWikiWeb) (perl) the
    first wiki, [WikiEngines](http://c2.com/cgi/wiki?WikiEngines)
-   [MediaWiki](http://www.mediawiki.org/ "mediawiki.org") (php, mysql)
-   [Wikka Wiki](http://wikkawiki.org/HomePage "wikkawiki.org") (php,
    mysql), Pmwiki has a markdown plugin.
-   [PmWiki](http://www.pmwiki.org/ "pmwiki.org") (php, flat-file).
-   [Dokuwiki](https://www.dokuwiki.org/dokuwiki) (GPL)
    is a php wiki aimed at creating documentation. It has his own syntax but
    there is a [plugin to use Creole](http://www.dokuwiki.org/plugin:creole)
    and [one for markdown](http://www.dokuwiki.org/plugin:markdownextra)
-   [TikiWiki](http://tikiwiki.org/) is a CMS (LGPL) developed in
    PHP and using the ADOdb database abstraction library which support
    all main DBMS.
    [Tiki Wiki (Wikipedia page)](http://en.wikipedia.org/wiki/TikiWiki)
    provides numerous components for content creation, organization,
    communication, and administration.

## Wiki with a Git/Mercurial backend
-   [Gitit](https://github.com/jgm/gitit) (GPL) by
    [John MacFarlane](http://johnmacfarlane.net/)
    is a wiki written in haskell, serving markdown,
    reStructuredText, LaTeX, or HTML pages thru pandoc, and using a
    git backend.
-   [git-wiki](http://atonie.org/2008/02/git-wiki)(public domain) is a
    ruby wiki using git as backend. It has a clone in python +
    Flask [gily](https://github.com/nyarla/gily) (public domain).
-   <a name="gollum"></a>[Gollum](https://github.com/gollum/gollum)
    (MIT License) is a Wiki written in Ruby with a git backend that
    accept pages written in Asciidoc, Creole, Markdown, Org Mode, Pod,
    RDoc, ReStructuredText, Textile, MediaWiki.  It is the software
    that powers up the GitHub wiki pages.
    -   [Gollum-Site
        ](/node/static_sites#gollumsite "internal reference")
        is a static site generator for Gollum.
    -   [code of Gollum GitHub Demo
        ](https://github.com/gollum/gollum-demo)
        and [generated wiki](https://github.com/gollum/gollum-demo/wiki).
    -   A less trival example is the
        [Radiant Wiki](https://github.com/radiant/radiant/wiki)
        for [Radiant CMS](http://radiantcms.org/).
-   [Hatta](http://hatta-wiki.org/) (no license but mercurial is GPL)
    uses Mecurial as backend and Creole as mark-up language.
-   [IkiWiki](http://ikiwiki.info/) (GPL): is a static wiki compiler
    that converts wiki pages into HTML developed by Joey Hess.
    Ikiwiki use a revision control system as backend. It supports Git,
    Subversion, mercurial, bzr, tla. Pages are written using many
    formats: MarkDown, WikiText, WikiCreole, ReStructured Text,
    Textile or plain Html.
-   [Nanoki](https://sourceforge.net/projects/nanoki/)
    (MIT license) is a lua wiki with markdown syntax.
-   [Sputnik](http://sputnik.freewisdom.org/)
    (MIT license) is a lua wiki with markdown or MediaWiki syntax.
    Sputnik stores its data as plain files or in a git repository, in a
    database or in subversion repository.
-   [wigit](https://el-tramo.be/wigit/) (BSD License)
    is a php wiki using Git as a backend and using
    of [Textile](http://textile.thresholdstate.com/) for marking up
    text.

## Python powered Wikis {#python_wikis}

[list of python wiki engines](https://wiki.python.org/moin/PythonWikiEngines)
at python.org.

_Gitology_, _gazest_, _Hatta_ are listed in the above section.

The static site generators
are in the [list of python powered static sites generators
](/node/static_sites#python_static_sites_list "internal reference") in the
[static generator section](/node/static_sites "internal reference")

-   The [Infogami](http://infogami.org/) wiki is powered
    up by web.py.
    [Infogami user tutorial](http://openlibrary.org/dev/docs/infogami).
-   [MoinMoin Wiki](http://moinmo.in/)(GPL) is a wiki
    written in python with easy integration of plugins, including
    formatters to render different source languages like
    Moins, ReST, MediaWiki and Markdown markups.
    -   [MoinMoin 2.0 documentation
        ](http://moin-20.readthedocs.io/en/latest/)



# Blog Software {#bloggers}
I give only few links to most known blogging software, you'll find them on
Wikipedia: [w:Weblog software], and focus on lightweight bloggers.

-   Main stream bloggers:
    [WordPress](http://wordpress.org/),
    [dotclear](http://www.dotclear.net/)
    [Blogger](http://www.blogger.com/) the google blog.
-   [Cherry Blossom](http://github.com/llimllib/cherry-blossom)
    is a blogging system written in Python, similar with pyblosxom but
    written on top of Cherrypy, _last commit 2011_. It is used to run
    [Bill Mill's blog](http://billmill.org).
-   [LnBlog](http://lnblog.skepticats.com/)
    (GPL) a php blogger with file based backend.
-   [nanoblogger](http://nanoblogger.sourceforge.net/) (GPL) a bash
    commandline blogger that only requires bash and base unix commands:
    cat, cp, cut, dirname, date\\*, expr, grep, mkdir, mv, read, rm,
    sed, sort, touch.
    [nanoblogger manual
    ](http://nanoblogger.sourceforge.net/docs/nanoblogger.html).
-   [PivotX](http://pivotx.net/) is a blogging tool and CMS written in PHP+Smarty with flat file or MySQL database.
-   [pybloxsom](http://pyblosxom.sourceforge.net/)
    a lightweight file-based weblog system written in python,
    is now abandoned.
-   [Vee](http://www.0x743.com/vee/) (BSD like license)
    is a command-line blog tool, it is a 600 lines shell
    script that uses only base unix commands cd, pwd, ls, sort, head,
    tail, cat, grep, groff, fold, expr.

# Web tools
-   Google: [Webmaster central](http://www.google.com/webmasters/)
    ([Centre pour les webmasters](http://www.google.fr/webmasters/)),
    [webmasters tools](https://www.google.com/webmasters/tools/)
-   [Sitemaps](http://www.sitemaps.org/) are an easy way for webmasters
    to inform search engines about pages on their sites that are
    available for crawling.
-   [Google alerts](https://www.google.com/alerts)
    Monitor the web for interesting new content, _en français_
    [Google alertes](https://www.google.fr/alerts)
-   [Talkwalker Alerts](https://www.talkwalker.com/alerts)
    an alternative to Google Alerts.

# Search engines
Wikipedia: [w:Category:Free search engine software]

-   [Lucene](http://lucene.apache.org/) (Apache License)
    is a java search engine supported by the Apache foundation.
    [elasticsearch](http://www.elasticsearch.org/) (Apache License)
    is a distributed, RESTful,  search server based on Apache Lucene.
    - Wikipedia: [w:Lucene] and [w:Elasticsearch]
    - A [collection of elasticsearch tutorials
      ](http://getelastomer.com/blog/category/elasticsearch-tutorials/)
    - [answers in stackoverflow: to Beginner's guide to
      ElasticSearch
      ](http://stackoverflow.com/questions/11593035/beginners-guide-to-elasticsearch/11767610)
-   [Sphider](http://www.sphider.eu/) (GPL) <a name="sphider"></a>
     is a lightweight web spider and search engine written in PHP,
    using MySQL as its back end database.
    it includes word autocompletion, spelling suggestions etc.
    _There is no more active development since 2009._
    - Sphider has two _very similar_ forks
      [Sphider plus](http://www.sphider-plus.eu/) and
      [SphiderPro](http://www.sphiderpro.eu/). But even if
      [Sphider pro announce it is GPL licensed
      ](http://www.sphiderpro.eu/license/)
      they both ask you to pay £25 before downloading, and I found no
      link to the source.
    - While there is no free download on
      [SphiderPro Home](http://www.sphiderpro.eu/)
      Since January 2013 there is a
     [google code sphiderpro](https://code.google.com/p/sphiderpro/)
      site, with an empty svn repository, but a rar archive to download.
-   [Sphinx](http://sphinxsearch.com/) (GPL)
    is a C++ search engine, running either as a stand alone service or
    interfaced with a DBMS; MySQL, MariaDB, PostgreSQL, ODBC
    - Wikipedia: [w:Sphinx]
-   [Xapian](http://www.xapian.org/)(GPL) is  a full text  search engine
    library  written in  C++, with  bindings to  allow use  from Perl,
    Python, PHP, Java, Tcl, C#, Ruby and Lua.
    [Recoll](http://www.lesbonscomptes.com/recoll/) (GPL) is a full text
    desktop search tool  based on xapian.
    - Wikipedia pages for [w:Xapian] and [w:recoll]
-   [Woosh](https://bitbucket.org/mchaput/whoosh/wiki/Home) (BSD License)
     is a searching library implemented in pure Python.
-   [Zend_Search_Lucene
    ](http://framework.zend.com/manual/1.12/en/zend.search.lucene.html)
    (BSD license)
    is search engine derived from the Apache Lucene project
    written entirely in PHP 5.



<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
