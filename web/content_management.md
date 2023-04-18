---
title: Content Management
---


# content management system (CMS)

A **content management system (CMS)** is a computer software system
for organizing and facilitating collaborative creation of documents
and other content. We call **content management framework** an
application programming interface for creating a customized content
management system. I no longer use CMS and replaced them by static site generators so I
list only few links of general CMS.

Look also at {{< iref "static_sites" "Static Sites" >}},
{{< iref "python_web#web_frameworks" "Web Frameworks" >}}.
For a broader view look at the following wikipedia pages.

- Wikipedia :
  {{< wp "Content management system" >}},
  {{< wp "Content management framework" >}},
  {{< wp "Comparison of content management systems" >}},
  {{< wp "Web framework" >}}.
- [Drupal](http://www.drupal.org/) is a CMS with PHP +
  Mysql/Postgresql which include a lot of modules which provide a
  wide assortment of features. ref:
  [Drupal Wikipedia Page](http://en.wikipedia.org/wiki/Drupal)

# Content Delivery network (CDN)
For content delivery an alternative is P2P content delivery in which
clients provide resources as well as use them.

-   Wikipedia: {{< wp "Content delivery network" >}} (CDN)

-   {{< wp "Cloudflare" >}} is a CDN with advanced DDoS protection.
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
    and {{< wp "Comparison of wiki hosting services" >}}
-   [MediaWiki](http://www.mediawiki.org/ "mediawiki.org") (php, mysql)
-   [ ] [PmWiki](http://www.pmwiki.org/ "pmwiki.org") (php, flat-file).
-   [Dokuwiki](https://www.dokuwiki.org/dokuwiki) (GPL)
    is a php wiki aimed at creating documentation. It has his own syntax but
    there is a [plugin to use Creole](http://www.dokuwiki.org/plugin:creole)
    and [one for markdown](http://www.dokuwiki.org/plugin:markdownextra)
-   [TikiWiki](https://tiki.org/HomePage) is a CMS (LGPL) developed in
    PHP and using the ADOdb database abstraction library which support
    all main DBMS.
    [Tiki Wiki (Wikipedia page)](http://en.wikipedia.org/wiki/TikiWiki)
    provides numerous components for content creation, organization,
    communication, and administration.

## Wiki with a Git/Mercurial backend
-   [Gitit](https://github.com/jgm/gitit) (GPL) by
    [John MacFarlane](http://johnmacfarlane.net/)
    is a wiki written in haskell, serving markdown, reStructuredText, LaTeX, or HTML
    pages thru pandoc, and using a git backend.
-   [git-wiki](http://atonie.org/2008/02/git-wiki)(public domain) is a
    ruby wiki using git as backend. It has a clone in python +
    Flask [gily](https://github.com/nyarla/gily) (public domain).
-   <a name="gollum"></a>[Gollum](https://github.com/gollum/gollum) (MIT License) is a
    Wiki written in Ruby with a git backend that accept pages written in Asciidoc,
    Creole, Markdown, Org Mode, Pod, RDoc, ReStructuredText, Textile, MediaWiki.  It is
    the software that powers up the GitHub wiki pages.
    -   {{< iref "static_sites#gollumsite" "Gollum-Site" >}}
        is a static site generator for Gollum.
    -   [code of Gollum GitHub Demo
        ](https://github.com/gollum/gollum-demo)
        and [generated wiki](https://github.com/gollum/gollum-demo/wiki).
    -   A less trival example is the
        [Radiant Wiki](https://github.com/radiant/radiant/wiki)
        for [Radiant CMS](http://radiantcms.org/).
-   [IkiWiki](http://ikiwiki.info/) (GPL): is a static wiki compiler that converts wiki
    pages into HTML developed by Joey Hess.  Ikiwiki use a revision control system as
    backend. It supports Git, Subversion, mercurial, bzr, tla. Pages are written using
    many formats: MarkDown, WikiText, WikiCreole, ReStructured Text, Textile or plain
    Html.

## Python powered Wikis {#python_wikis}

[list of python wiki engines](https://wiki.python.org/moin/PythonWikiEngines)
at python.org.

The static site generators
are in the {{< iref "static_sites#python_static_sites_list" "list of python powered static sites generators" >}}
in the {{< iref "static_sites" "static generator section" >}}.

-   The [Infogami](http://infogami.org/) wiki is powered
    up by web.py.
    [Infogami user tutorial](http://openlibrary.org/dev/docs/infogami).
-   [MoinMoin Wiki](http://moinmo.in/)(GPL) is a wiki
    written in python with easy integration of plugins, including
    formatters to render different source languages like
    Moins, ReST, MediaWiki and Markdown markups.
    -   [MoinMoin 2.0 documentation
        ](http://moin-20.readthedocs.io/en/latest/)



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

# Search engines {#search-engines}
Wikipedia: {{< wp "Category:Free search engine software" >}}

-   <a name="lucene"></a>[Lucene](http://lucene.apache.org/) (Apache License)
    is a java search engine supported by the Apache foundation.
    -   <a name="elasticsearch"></a>[elasticsearch](http://www.elasticsearch.org/) (Apache License)
    is a distributed, RESTful,  search server based on Apache Lucene.
    -   <a name="bonsai"></a>[Bonsai](https://bonsai.io/) (commercial)
       hosted Elasticsearch-as-a-service. There is a free plan for testing with 125M ssd
       and 125 Memory, thefirst _true_ plan is 20$/month for 1GB Memory and 250M SSD.
    -   Wikipedia: {{< wp "Lucene" >}} and {{< wp "Elasticsearch" >}}
-   [Sphinx Search](http://sphinxsearch.com/) (GPL)
    is a C++ search engine, running either as a stand alone service or interfaced with a
    DBMS; MySQL, MariaDB, PostgreSQL, ODBC.

    _sphinxsearch_ is packaged in Debian.
    - Wikipedia: {{< wp "Sphinx" >}}
-   [Xapian](http://www.xapian.org/)(GPL)
    is a full text search engine library written in C++, with bindings to allow use from
    Perl, Python, PHP, Java, Tcl, C#, Ruby and Lua.

    _libxapian_ is available as Debain opackage as well as _xapian-tools_ and binding
    for java, python3, ruby,
    -   [Recoll](http://www.lesbonscomptes.com/recoll/) (GPL)
        is a full text desktop search tool  based on xapian.

        _recollgui_ the QT5 frontend tpo recoll is available in Debian, as well as the CLI
        _recoll-cmd_.
    -   [Xapers](https://finestructure.net/xapers/)
        is a personal journal article management system based on xapian.
        _xapers_ is in Debian.
    -   Wikipedia pages for {{< wp "Xapian" >}} and {{< wp "recoll" >}}.
-   <a name="meilisearch"></a>[GitHub - meilisearch
    ](https://github.com/meilisearch/meilisearch) (MIT License)
    a rust powered search engine.
    -   [Quick start
        ](https://docs.meilisearch.com/learn/getting_started/quick_start.html#setup-and-installation).
    -   [Official SDKs](https://docs.meilisearch.com/learn/what_is_meilisearch/sdks.html).
    -   [docs-scraper](https://github.com/meilisearch/docs-scraper) (MIT License)
        scrape your documentation into Meilisearch.
    -   [docs-searchbar.js](https://github.com/meilisearch/docs-searchbar.js) (MIT License)
        a front-end search bar for documentation with Meilisearch.
    There is also a commercial cloud hosted [Meilisearch](https://www.meilisearch.com/).
    In 2023 first 100k documents and 10K searches/month are free then  $0.25 for every
    1k documents and 1k searches.
-   <a name="orama"></a>[orama](https://github.com/oramasearch/orama) (Apache License)
    is a fast, in-memory, typo-tolerant, full-text search engine written in TypeScript.

    Orama was previously named _Lyra_
-   [YaCy](http://www.yacy.net/en/index.html) (GPL)
    is a distributed Peer-to-Peer Web Search Engine and Intranet Search Appliance _Yaci_
    is community hosted, you need to run a java server component on your machine.
    -   [YaCy - GitHub](https://github.com/yacy/yacy_search_server)

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
