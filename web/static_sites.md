---
title: Static Sites Generators
---

# References

-   GitLab [1. Static vs Dynamic Websites
    ](https://about.gitlab.com/2016/06/03/ssg-overview-gitlab-pages-part-1-dynamic-x-static/),
    [2. Modern Static Site Generators
    ](https://about.gitlab.com/2016/06/10/ssg-overview-gitlab-pages-part-2/),
    [3. Build any SSG site with GitLab Pages
    ](https://about.gitlab.com/2016/06/17/ssg-overview-gitlab-pages-part-3-examples-ci)
    the second part explore the benefits and the structure of modern
    static site generators.
-   Authentication is not easy with Static Sites, we can always rely
    on the server side authentication through basic HTTP authentication.
    We can also rely on external services like [Firebase
    ](https://www.firebase.com/) (look at the
    [Security & Authentication Examples
    ](https://www.firebase.com/docs/web/examples.html)),
    or [UserApp](https://www.userapp.io/).

# Alt Lists
The static site generators are so numerous, that I will not try to
list all of them, but some selection, excluding the software which
are only targeted to blogs. My selection may also be biased toward python.

You can find also some more complete and up to date lists:

-   [Top Open-Source Static Site Generators - StaticGen
    ](http://www.staticgen.com/)
-   [Awesome Static Generators](https://github.com/myles/awesome-static-generators)
-   [Static Website Generators For Your Site, Blog Or Wiki
    ](https://iwantmyname.com/blog/2014/05/the-updated-big-list-of-static-website-generators-for-your-site-blog-or-wiki)
    _(2014 post)_.
-   [Complete List of Static Site Generators for Python
    ](https://gistpages.com/posts/complete_list_of_static_site_generators_for_python)
-   Steve Kemp has put on GitHub a [review of static site generators
    ](https://github.com/skx/static-site-generators) including
    gostatic, hakyll,  jekyll, nanoc, pelican, poole, templer,
    webby, webgen, wintersmith. _dated 2013_
-   A very complete list *but limited to a list* is
    [Static Site Generators](http://staticsitegenerators.net/).
-   [{static is} The New Dynamic
    ](https://www.thenewdynamic.org/)
    list resources for static sites.
-   [Top Open-Source Static Documentation Generators
    ](http://www.docbuilds.com/)_no longer updated since february 2017_

# Lists by programming language
The site generators are written in various languages:

-   _python_: <a name="python_static_sites_list"></a>
    {{< iref "#acrylamid" "Acrylamid" >}},
    {{< iref "#chisel" "Chisel" >}},
    {{< iref "#cyrax" "Cyrax" >}},
    {{< iref "#elyse" "Elyse" >}},
    {{< iref "#growl" "Growl" >}},
    {{< iref "#hyde" "Hyde" >}},
    {{< iref "#liquidluck" "liquidluck" >}},
    {{< iref "#markdoc" "MarkDoc" >}},
    {{< iref "#mkdocs" "Mkdocs" >}},
    {{< iref "#nib" "Nib" >}},
    {{< iref "#nikola" "Nikola" >}},
    {{< iref "#pelican" "Pelican" >}},
    {{< iref "#mynt" "Mynt" >}},
    {{< iref "#poole" "Poole" >}},
    {{< iref "#simple" "simple-docs" >}},
    {{< iref "#stangecase" "StrangeCase" >}},
    {{< iref "#soho" "Soho" >}},
    {{< iref "#webber" "Webber" >}},
    {{< iref "#wok" "Wok" >}}.
-   _Ruby_:
    {{< iref "#awestruct" "Awestruct" >}},
    {{< iref "#bonsai" "Bonsai" >}},
    {{< iref "#jekyll" "Jekyll" >}},
    {{< iref "#gollum-site" "Gollum-site" >}},
    {{< iref "#middleman" "Middleman" >}},
    {{< iref "#nanoc" "Nanoc" >}},
    {{< iref "#ruhoh" "Ruho" >}},
    {{< iref "#shelob" "shelob" >}},
    [many more referenced in the ruby toolbox
    ](https://www.ruby-toolbox.com/categories/static_website_generation).
-   _Haskell_: {{< iref "#hakyll" "Hakyll" >}}
-   in _Php_:
    {{< iref "#couscous" "Couscous" >}},
    {{< iref "#dauxio" "Daux.io" >}},
    {{< iref "#ewiki" "Ewiki" >}},
-   _node.js_: {{< iref "#docpad" "docpad" >}},
    {{< iref "#blacksmith" "BlackSmith" >}},
    {{< iref "#codex" "Codex" >}},
    {{< iref "#docsify" "Docsify" >}},
    {{< iref "#flatdoc" "Flatdoc" >}},
    {{< iref "#hexo" "Hexo" >}},
    {{< iref "#gitbook" "GitBook" >}},
    {{< iref "#punch" "Punch" >}},
    {{< iref "#wintersmith" "Wintersmith" >}},
-   _shell_:  {{< iref "#simple_static" "simple-static" >}},
    {{< iref "#sw" "sw" >}}, {{< iref "#werc" "werc" >}}
-   emacs-lisp {{< iref "#o_blog" "o-blog" >}},
    {{< iref "#org" "org-page" >}},
    {{< iref "#org" "org-site" >}}
-   _go_:
    {{< iref "hugo" "Hugo" >}},

# List by page format
-   {{< iref "markdown" "Markdown" >}}:
    {{< iref "#acrylamid" "Acrylamid" >}},
    {{< iref "#awestruct" "Awestruct" >}},
    {{< iref "#blacksmith" "BlackSmith" >}},
    {{< iref "#bonsai" "Bonsai" >}},
    {{< iref "#couscous" "Couscous" >}},
    {{< iref "#dauxio" "Daux.io" >}},
    {{< iref "#docpad" "Docpad" >}}
    {{< iref "#chisel" "Chisel" >}},
    {{< iref "#codex" "Codex" >}},
    {{< iref "#elyse" "Elyse" >}},
    {{< iref "#flatdoc" "Flatdoc" >}},
    {{< iref "#gitbook" "GitBook" >}},
    {{< iref "#gollum-site" "Gollum-Site" >}},
    {{< iref "#hakyll" "Hakyll" >}},
    {{< iref "#hexo" "Hexo" >}},
    {{< iref "hugo" "Hugo" >}},
    {{< iref "#hyde" "Hyde" >}},
    {{< iref "#jekyll" "Jekyll" >}},
    {{< iref "#liquidluck" "liquidluck" >}},
    {{< iref "#markdoc" "MarkDoc" >}},
    {{< iref "#middleman" "Middleman" >}},
    {{< iref "#mkdocs" "Mkdocs" >}},
    {{< iref "#mynt" "Mynt" >}},
    {{< iref "#nanoc" "nanoc" >}},
    {{< iref "#nib" "Nib" >}},
    {{< iref "#nikola" "Nikola" >}},
    {{< iref "#pelican" "Pelican" >}},
    {{< iref "#poole" "Poole" >}},
    {{< iref "#punch" "Punch" >}},
    {{< iref "#ruhoh" "Ruho" >}},
    {{< iref "#simple" "simple-docs" >}},
    {{< iref "#simple_static" "simple-static" >}},
    {{< iref "#sw" "sw" >}},
    {{< iref "#werc" "werc" >}}
    {{< iref "#wintersmith" "Wintersmith" >}},
    {{< iref "#wok" "Wok" >}}.
-   _ReSTructured text_:
    {{< iref "#acrylamid" "Acrylamid" >}},
    {{< iref "#flask" "Flask-rst" >}},
    {{< iref "#gollum-site" "Gollum-Site" >}},
    {{< iref "#hyde" "Hyde" >}},
    {{< iref "#jekyll" "Jekyll" >}},
    {{< iref "#liquidluck" "liquidluck" >}},
    {{< iref "#nikola" "Nikola" >}},
    {{< iref "#pelican" "Pelican" >}},
    {{< iref "#soho" "Soho" >}},
    {{< iref "#wok" "Wok" >}},
-   _AsciiDoc_:
    {{< iref "#awestruct" "Awestruct" >}},
    {{< iref "#gitbook" "GitBook" >}},
    {{< iref "#gollum-site" "Gollum-Site" >}},
    {{< iref "#hexo" "Hexo" >}} through a plugin,
    {{< iref "hugo" "Hugo" >}} through a plugin,
    {{< iref "#hyde" "Hyde" >}},
    {{< iref "#pelican" "Pelican" >}},
-   _Org-mode_:
    {{< iref "#gollum-site" "Gollum-Site" >}},
    {{< iref "#hexo" "Hexo" >}} through a plugin,
    {{< iref "hugo" "Hugo" >}} through a plugin,
    {{< iref "#hyde" "Hyde" >}} through a plugin,
    {{< iref "#jekyll" "Jekyll" >}} through a plugin,
    {{< iref "#o_blog" "o-blog" >}},
    {{< iref "#org" "org-page" >}},
    {{< iref "#org" "org-site" >}}

# Site generators list
-   [Awestruct](http://awestruct.org/) (MIT License)
    <a name="awestruct"></a> is a ruby static website
    generator, that uses Asciidoc an Markdown (+Haml) formats.

-   <a name="chisel"></a>[Chisel
    ](http://github.com/dz/chisel/blob/master/chisel.py)
     is a minimal (100 lines) python static blog generation utility
     using _jinja2_ and _Markdown_.
-    <a name="docpad"></a>[Docpad](https://github.com/bevry/docpad)
    (MIT License) a node.js site generator for _MarkDown_ pages.
     -   [Docpad Documentation](http://docpad.org/docs/).
     -   _DocPad_ can be [deployed on many hosting solutions
         ](http://docpad.org/docs/deploy): _S3_, _Google Storage_,
         a _node.js_ provider, _GitHub_ pages, or as static pages on
         any server.
     -   [Docpad Sunny](https://github.com/bobobo1618/docpad-plugin-sunny)
         (MIT License) is a Docpad plugin using
         [Sunny](https://github.com/ryan-roemer/node-sunny)
         to publish your _DocPad_ site to _Amazon S3_ or _Google
         Storage_.
     -   Many pre-made
         [DocPad skeletons](http://docpad.org/docs/skeletons)
         are availables.
-   <a name="elyse"></a>[Elyse](https://github.com/FSX/elyse)
    is a very simple (450 SLOC) static site generator
    in python, using [misaka](http://misaka.61924.nl/) to generate documentation from
    mardown sources. _Obsolete 2012_
-   [Ewiki](http://soultcer.net/wiki/Code/eWiki)<a name="ewiki"></a>
    is a small Wiki written in PHP. It uses Git as backend and a
    [custom markup.](http://github.com/soult/ewiki/blob/master/doc/markup.txt)
-   {{< iref "python_web#flask" "Flask" >}}
    You can transfom your
    {{< iref "python_web#flask" "Flask" >}}
    application to a static site with <a name="frozen-flask"></a>
    [Frozen-Flask](https://github.com/SimonSapin/Frozen-Flask)
    (BSD License) by Simon Sapin.
    -   [Hosting static Flask sites for free on Github Pages
        ](http://www.stevenloria.com/hosting-static-flask-sites-for-free-on-github-pages/)
        is a tutorial by Steven Loria accompanied by an
        [example of  static Flask app on Github pages
        ](https://github.com/sloria/flask-ghpages-example),
        [_killtheyak_ - a larger example
        ](https://github.com/killtheyak/killtheyak.github.com/tree/master/killtheyak)
        is also available.
-   [Flask-rst](https://github.com/jarus/flask-rst) <a name="flask-rst">
    is a python tool to create a website from a source of
    reStructuredText that uses  {{< iref "python_web#flask" "Flask" >}}
-   <a name="gollum-site">[Gollum-Site](https://github.com/dreverri/gollum-site)
    is a static site generator for  {{< iref "content_management#gollum" "Gollum" >}}
    like _Gollum_ it is  written in Ruby with a git backend and accept pages written in
    _Asciidoc_, _Creole_, _Markdown_, _Org Mode_, _Pod_, _RDoc_,
    _ReStructuredText_, _Textile_, _MediaWiki_.
    -  Like _Gollum_ _Gollum-Site_ uses the
       [Liquid Templating System](https://github.com/tobi/liquid/wiki).
    -  [Riak](http://basho.com/) had previously its wiki written in Gollum and Gollum-site,
        you can still find the source of the
        [Riak-Wiki on GitHub](https://github.com/ghaskins/riak_wiki).
        But now Riak switched to {{< iref "#middleman" "middleman" >}}
    -   _Gollum-Site_ has not followed the _Gollum_ new release and is still linked to
        _Gollum_ 1.4.  and many sites either changed of static generator or upgraded to
        _Gollum_ 2, but dropped _Gollum-Site_
-   <a name="growl"></a>[Growl](http://github.com/xfire/growl/tree) (GPL)
    an other  python static site generator inspired by
    {{< iref "#jekyll" "Jekyll" >}}.
    It uses _MarkDown_ as markup language, and  has
    [Minimal dependencies](http://github.com/xfire/growl/blob/master/README.markdown)
    python python-yaml and a templating engine like jinja2.
    _It allows only a simple layout and has not changed since 2009._
-   <a name="hakyll"></a>[Hakyll](http://jaspervdj.be/hakyll/)
    is a Haskell library for generating static sites, aimed at
    small-to-medium sites and personal blogs. Integration with pandoc give
    _Markdown_ and TeX support.
-   [Hugo](https://gohugo.io/) is a static site
    generator written in go. It is in Debian. More on
    {{< iref "hugo" "Hugo section" >}}.
-   <a name="hexo"></a> [Hexo](https://hexo.io)
    (MIT License) a blog framework, powered by Node.js.
    -   [GitHub - Hexo](https://github.com/hexojs/hexo)
    -   [Hexo Documentation](https://hexo.io/docs/)
    -   [coldnew/hexo-renderer-org
        ](https://github.com/coldnew/hexo-renderer-org)) :
        Hexo renderer plugin for emacs org-mode
    -   [TheNewDynamic - list of Hexo links
        ](https://www.thenewdynamic.org/tool/hexo/).
    -   [awesome-hexo
        ](https://github.com/hexojs/awesome-hexo)
        resourcers, plugins and examples for hexo.
-   [Jekyll](http://wiki.github.com/mojombo/jekyll/wiki/)<a name="jekyll"></a> (MIT License)
    is a static site generator written in ruby that
    uses _Textile_, _Markdown_ or _HTML_ as markup.
    -   Jekyll is the engine behind
        [GitHub Pages](http://pages.github.com/)
        -   [GitHub Pages Help](https://help.github.com/categories/20/articles).
        -   [Using Jekyll with Pages](https://help.github.com/articles/using-jekyll-with-pages)
    -   [Jekyll Wiki pages](https://github.com/mojombo/jekyll/wiki)
    -   There is a huge [list of jekyll plugins](https://github.com/mojombo/jekyll/wiki/Plugins)
    -   [Jekyll-Bootstrap](http://jekyllbootstrap.com/)
        -   [Jekyll Introduction](http://jekyllbootstrap.com/lessons/jekyll-introduction.html)
        -   [Jekyll-Bootstrap - GitHub](http://github.com/plusjade/jekyll-bootstrap)
    -   There are many examples sites to help you to boostrap your
        Jekyll powered site:
        [Lukasz Grzegorz Maciak: Sample-Jekyll-Site
        ](https://github.com/maciakl/Sample-Jekyll-Site),
        [Hendrik Kleinwaechter - jekyll-quickstart
        ](https://github.com/hendricius/jekyll-quickstart) use
        [Slim template](http://rdoc.info/github/slim-template/slim)
    -   [jekyll Deployment](https://github.com/mojombo/jekyll/wiki/Deployment)
    -   [Org-jekyll](http://juanreyero.com/open/org-jekyll/)
         by Juan Reyero export jekyll blog posts from org-mode.
    -   There are number of
        [Jekyll powered sites](https://github.com/mojombo/jekyll/wiki/Sites)
        whose sources are available.
        The site [git-ready](http://gitready.com/) is built with Jekyll and the
        [source is available on GitHub](https://github.com/gitready/gitready).
        It is a good example of a simple Jekyll layout, .
-   <a name="metalsmith"></a>[Metalsmith](http://www.metalsmith.io/)
    a node.js plugable static site generator. It accepts documentation in Markdown and
    through plugin ReSTructured text, asciidoc, org-mode.
    -   [GitHub Metalsmith
        ](https://github.com/segmentio/metalsmith).
    -   [TheNewDynamic - list of Metalsmith links
        ](https://www.thenewdynamic.org/tool/metalsmith/)
    -   [awesome-metalsmith
        ](https://github.com/metalsmith/awesome-metalsmith)
        Resources and examples for Metalsmith.
-   <a name="middleman"></a>[Middleman](http://middlemanapp.com/)
    (MIT License) is a static site generator written in ruby. It uses
    Haml, Sass, Less & Coffee Script.  There is a huge
    [list of sites built with middleman
    ](http://middlemanapp.com/community/built-using-middleman/).
-   <a name="mynt"></a>[Mynt](http://mynt.uhnomoli.com/) (BSD License)
    a Python static site generator. It uses _Jinja_ templates,
    and _Markdown_. Even if the last commit is in 2014 there is a
    list of [many examples
    ](http://mynt.uhnomoli.com/community/powering/)
    which are alive in 2018.
    -   [GitHub: Mynt](https://github.com/Anomareh/mynt/)
    -   [Quick Start: A Static Site with Bootstrap and Mynt
        ](http://www.tummy.com/articles/static-sites-with-bootstrap-and-mynt/)
        a tutorial by Sean Reifschneider from tummy.com.
-   <a name="nanoc"></a>[Nanoc](https://nanoc.ws/)
    is a static site generator written in ruby
    that can use formats such as _Markdown_, _Textile_, _Haml_…
    There are many examples of nanoc sites, and
    [FOSDEM switched from Drupal to Nanoc
    ](https://archive.fosdem.org/2013/news/2012-11-16-new-website/)
-   <a name="nikola"></a>[Nikola](https://github.com/ralsina/nikola/)
    (MIT License) by Roberto Alsina is a Python static website
    generator.
    It is extensible via plugins, and uses Markdown or ReSTructured
    text.

    -   [Pypi: Nikola](https://pypi.python.org/pypi/Nikola/)
    -   [Nikola Home Page](http://nikola.ralsina.com.ar/)
    -   [Nikola Handbook](http://nikola.ralsina.com.ar/handbook.html)
    -   [Lateral Opinion - Roberto Alsina Blog
        ](http://ralsina.me/) itself published
        with Nikola, gives Nikola development news.
    -   [nikola-server](https://github.com/ralsina/nikola-server)
        allow to manage a remote Nikola site

-   <a name="o-blog"></a>[o-blog](http://renard.github.io/o-blog)
    (Licence: [WTFPL](http://sam.zoy.org/wtfpl/)) by Sébastien Gross _renard_,
    is a static site generator managed from emacs. The pages are written in
    {{< iref "org-mode" "org-mode" >}}. It allows blogs and static pages.
    [GitHub: o-blog](https://github.com/renard/o-blog).
-   <a name="org-page"></a>[org-page
    ](https://github.com/kelvinh/org-page) (GPL)
    by Kelvin Hu is a static site generator based on
    {{< iref "org-mode" "Emacs org-mode" >}}.
    the [Kevin's site](http://kelvinh.github.io/) (
    [source](https://github.com/kelvinh/kelvinh.github.com))
    and the [site of Standino](http://standino.github.io/) (
    [source](https://github.com/standino/standino.github.com))
    are examples of *org-page* sites.
-   <a name="org-site"></a>[org-site](http://xiaohanyu.github.io/org-site/about.html) (GPL)
    is a static site generator based on {{< iref "org-mode" "Emacs org-mode" >}}
    It includes theme with *Bootstrap* default,  *mustache* templating,
    index page generation, commenting using *Disqus*.
    [GitHub:org-site](https://github.com/xiaohanyu/org-site/).
-   <a name="pelican"></a>[Pelican](http://pelican.notmyidea.org/)
    (GNU Affero General Public License)
    is a static blog generator in python, that uses
    _ReSTructured text_, _Asciidoc_ or _Markdown_.
    Themes are done using _jinja2_.

    -   [Pelican GitHub repository](https://github.com/getpelican/pelican/).
    -   The [Not My Idea](http://blog.notmyidea.org)
        blog of Alexis Metaireau has its
        [source in GitHub](https://github.com/ametaireau/notmyidea), The
        [Pelican Blog](http://blog.getpelican.com) also has its
        [source in GitHub](https://github.com/getpelican/pelican-blog)
    -   [Pelican hosts a huge list of themes on GitHub
        ](https://github.com/getpelican/pelican-themes)
    -   [Pelican and Github Pages](http://martinbrochhaus.com/pelican2.html)
        by Martin Brochhaus.
    -   [Bootstrap 3 theme for Pelican
        ](https://github.com/DandyDev/pelican-bootstrap3)
    -   Gabe Weatherhead has written three blog pages on setting up a
        Pelican site, they focus on the site design:
        [Moving From WordPress and Initial Setup
        ](http://www.macdrifter.com/2012/08/pelican-guide-moving-from-wordpress-and-initial-setup.html),
        [Design Planning
        ](http://www.macdrifter.com/2012/08/moving-to-pelican-design-planning.html),
        [About Properly Formatted Blog Posts
        ](http://www.macdrifter.com/2012/09/things-ive-learned-about-properly-formatted-blog-posts.html)
    -   [Generate a Static Company Site and Blog with Pelican and Jinja
        ](http://stackful-dev.com/static-site-jinja-pelican-shared-templates.html)
        by Hristo Deshev,an
        [example site using these concepts
        ](https://github.com/hdeshev/pelican-site-example)
        is hosted in GitHub.
    -   [Creating A Pelican-Powered Site on GitHub Pages
        ](http://magically.us/2013-02-03/creating-a-pelican-powered-site-on-github-pages.html)
        by Kevin Richardson, explains how it generates his site
        [magically.us](http://magically.us/)
        whose [source is available on GitHub
        ](https://github.com/kfr2/kfr2.github.com).

    Pelican is a promising project, well maintained and with a very
    good documentation, both for the user and the developer. Alas, It
    is targeted to blogs and the support for pages is quite rudimentary.

-   <a name="punch"></a> [Punch
    ](http://laktek.github.io/punch/) (MIT License)
    is a node.js static site generator that uses
    {{< iref "python_web#mustache" "Mustache" >}} for
    templating _and mustache itself use Json for the data_ and
    _Markdown_ to write pages.
    -   [Punch GitHub repository](https://github.com/laktek/punch)
    -   [Generate Websites from JSON, Markdown, and Mustache Templates
        using Punch
        ](http://css.dzone.com/articles/generate-websites-json).
-   <a name="shelob"></a>[Shelob
    ](https://www.ruby-toolbox.com/categories/static_website_generation)
    (BSD License) is a ruby site generator extension for
    [Smeagol](https://github.com/rubyworks/smeagol) which is
    a server that can run a read-only version of a Gollum wiki.
-    <a name="vee"></a>[Vee](http://estrabd.github.io/vee/)
    command line shell microblogging tool.
    [Vee GitHub repository](https://github.com/estrabd/vee)
-   [WinterSmith](https://github.com/jnordberg/wintersmith)
    is a _node.js cofeescript_ static site generator for _MarkDown_ pages
    inspired by {{< iref "#blacksmith" "BlackSmith" >}}.
    It uses [marked](https://github.com/chjj/marked) to parse
    markdown and the [jade](https://github.com/visionmedia/jade)
    _node.js_ templating engine.


# Generators for documentation
Many of the previous generators can be used for documentaion, even if
most o them where primary aimed to blogging.
## All pupose generators used for documentation
-   {{< iref "#hexo" "Hexo" >}}
    -   [Project Documentation with Hexo Static Site Generator
        ](https://www.sitepoint.com/project-documentation-hexo/).
    -   The [exo site documentation](https://hexo.io/docs/)
        is an example of a simple flat documentation.
        The [source is on GitHub
        ](https://github.com/hexojs/site).
    -   [Meteor Api documentation
        ](https://docs.meteor.com/) -
        [GitHub](https://github.com/meteor/doc)
        and [Meteor Guide](https://guide.meteor.com/) -
        [GitHub](https://github.com/meteor/guide),
        are a fairly complete examples of documentaion.
-   {{< iref "#jekyll" "Jekyll" >}}
    -   [How GitHub uses GitHub to document GitHub · GitHub
        ](https://github.com/blog/1939-how-github-uses-github-to-document-github).
-   {{< iref "#metalsmith" "MetalSmith" >}}
    -   [Building a Static Documentation Site with Metalsmith
        ](https://gregleeds.com/building-a-static-documentation-site-with-metalsmith/).
    -   [Building Technical Documentation with Metalsmith
        ](https://segment.com/blog/building-technical-documentation-with-metalsmith/).

## generators mainly targeted to documentation

-   <a name="couscous"></a>[Couscous](http://couscous.io/)
    PHP documentation generator for Markdown _Extra_.
    -   [GitHub Couscous](https://github.com/CouscousPHP/Couscous)
-   <a name="crowbook">[CrowBook](https://github.com/lise-henry/crowbook)
    a ruby program yp convert books written in Markdown to html,
    latex/pdf and epub.
    -   [Mot-clé crowbook - Le blog de Lizzie Crowdagger
        ](https://crowdagger.fr/blog/index.php?tag/crowbook)
-   <a name="dauxio"></a>[Daux.io](https://dauxio.github.io/)
    (MIT License)is a static documentation generator written in PHP.
    I accept documentation in Markdown.
    -   [GitHubDaux.io](https://github.com/dauxio/daux.io).
-   <a name="docsify">[Docsify](https://github.com/QingWei-Li/docsify/)
    (MIT License) is a javascript dynamic _(not static site)_
    documentation generator for markdown.
-   <a name="gitbook"></a>[GitBook](https://github.com/GitbookIO/gitbook)
    is a javascript toolchain for documentation using Git and Markdown or AsciiDoc.
    -   [GitBook Toolchain](https://toolchain.gitbook.com/)
    -   [gitbook.com](https://www.gitbook.com) is a site offering free publication of
        free open source books, and paid service for private books.
-   <a name="flatdoc"></a>[Flatdoc](http://ricostacruz.com/flatdoc/)
    by [Rico Sta. Cruz](https://github.com/rstacruz) is a JavaScript program to render
    Markdown files.
    -   [GitHub - Flatdoc](https://github.com/rstacruz/flatdoc) _last commit 2015,
        numerous forks_.
-   <a name="mkdocs"></a>[MkDocs](http://www.mkdocs.org/)
    is  static site generator in python aimed to project
    documentation. It is used for markdown documentation with Yaml
    configuration.
-   <a name="simple-docs"></a>[simple-docs](http://simpledocs.co/)
    (MIT license) is a Python Flask website for
    viewing _Markdown_ documentation files online. It is not a static
    site generator, but can be used for this task with
    {{< iref "#frozen" "Frozen-Flask" >}}.
    -   [GitHub - simple-docs](https://github.com/chrislaskey/simple-docs)
-   <a name="simple_static"></a>[simple-static
    ](https://github.com/wlangstroth/simple-static)
    is a site generator, using _Markdown_ pages. It is mainly
    targeted to documentation.
    It is written in awk and shell using
    [md2html.awk](node/markdown/#md2html_awk "internal reference").
    It is based on {{< iref "#sw" "sw" >}}.
-   <a name="sw">[sw](https://github.com/jroimartin/sw)
    is a minimal static site generator for _Markdown_ pages using the
    shell and common utilities grep, sed, awk (with
    {{< iref "markdown" "md2html.awk" >}})...
    <br/>
    _sw_ is inspired by {{< iref "#werc" "werc" >}}, and
    {{< iref "#simple_static" "simple-static" >}} is a fork of
    _sw_.
-   <a name="werc"></a>[werc](http://werc.cat-v.org/)
    (Public domain or MIT license or ISC license)
    is a static site generator for html and _Markdown_ written with
    the Plan9 shell _rc_, cat, grep, sed, ... _last release 2010_.

# Obsolete or low developpement sofware
-   <a name="acrylamid"></a>
    [Acrylamid](https://posativ.org/acrylamid/) (BSD License)
    by Martin Zimmermann is a static blog (and articles) generator
    written in python and using Markdown, reStructuredText or textile.
    _Acrylamid is tagged unmaintained, no development since 2015_
    -   [GitHub: Acrylamid](https://github.com/posativ/acrylamid).
    -   Acrylamid includes a [search engine](https://posativ.org/acrylamid/static-search.html).
-   <a name="blacksmith"></a>
    [BlackSmith](ttps://github.com/flatiron/blacksmith) (MIT License)
    is a node.js static site generator for markdown pages. It was
    developed by {{< wp "Nodejitsu" >}} people and
    the _Nodejitsu_ site was built with _BlackSmith_.

    But _Nodejitsu_ was acquired in 2015 and _Blacksmith_ non longer
    developped since 2013 disappeared.

    -   _Nodejitsu Handbook_
        is an example of doc produced by _BlackSmith_, it's source
        is [available in GitHub](https://github.com/nodejitsu/handbook).
    -   [blacksmith-sites](https://github.com/flatiron/blacksmith-sites)
        is a collection of templates for  _BlackSmith_.
    -   {{< iref "#wintersmith" "winterSmith" >}} is derived from _BlackSmith_.

-   <a name="bonsai"></a>[Bonsai (GitHub)
    ](https://github.com/benschwarz/bonsai)
    (MIT License) is a ruby static site generator
    with _Liquid_ templates and _Markdown_ pages.
    -   [Bonsai Home (tinytree.info)](http://tinytree.info/)
    _last commit January 2014._
-   <a name="codex"></a>[Codex
    ](https://github.com/logicalparadox/codex) (MIT License)
    is a node.js static site generator from Markdown files. It uses
    _Jade_ for templating and
    [Stylus](https://github.com/learnboost/stylus) for the style
    (css).
    _Codex last commit is from beginning 2014._
-   <a name="chisel"></a>[Chisel
    ](http://github.com/dz/chisel/blob/master/chisel.py)
     is a minimal (100 lines) python static blog generation utility
     using _jinja2_ and _Markdown_.
     _16 commits in 9 years._
-    <a name="cyrax"></a>[Cyrax](http://cyrax.readthedocs.org/en/latest/)
     is a static site generator in python using Jinja2 template
     engine.
     _Only 13 commits between 2012 and 2018._
     -   [GitHub Cyrax](https://github.com/piranha/cyrax)
-   <a name="hyde"></a>[Hyde](http://hyde.github.com/) (MIT License)
    is a python static website generator.

    We can use blocks of text formatted in _Markdown_,
    _Textile_, _reStructuredText_, _AsciiDoc_ and use
    {{{< iref "source_code#pygments" "Pygments" >}} for source code.

    _Hyde has a very slow activity and no commit since beginning 2016._

    -   [Hyde Starter Kit
        ](http://merlin.rebrovic.net/hyde-starter-kit/)
        by Merlin Rebrović is a _Hyde_ tutorial and example site; also
        included in an _Hyde_ installation as a layout named
        _starter_.
        [merlin.rebrovic.net the website of Merlin Rebrović
        ](http://merlin.rebrovic.net) is also an
        [open source Hyde site
        ](https://github.com/merlinrebrovic/merlin.rebrovic.net)
    -   The [Documentation for Hyde](http://hyde.github.com/)
        is itself an
        [open source Hyde site](https://github.com/hyde/docs)
    -   [Org-Hyde](https://github.com/punchagan/org-hyde)
        allow to push org content under Hyde. It is a fork of
        [Org Jekyll](http://juanreyero.com/open/org-jekyll/)

    Among the many
    [open source examples of Hyde sites](https://github.com/hyde/hyde/wiki/Hyde-Powered):

    -   _RingCe_ from the author of _Hyde_
        Lakshmi Vyas, has its
        [source on GitHub](https://github.com/lakshmivyas/ringce)
        but is obsolete.
    -   Vincent Bernat has [switched to Hyde
        ](http://www.luffy.cx/en/blog/2011-new-website-with-hyde.html)
        his site [luffy.cx](http://www.luffy.cx/) and the
        [source is available at
        GitHub](https://github.com/vincentbernat/www.luffy.cx)
        _still active in 2018._
-   <a name="liquidluck"></a>[liquidluck
    ](https://github.com/avelino/liquidluck)
    (BSD License) aka _Felix Felicis_ is a static blog generator in
    python using _MarkDown_ and _ReSTructured Text_ as markup
    languages.
    _Only 19 commits between October 2013 and 2018._
-   <a name="nib"></a>[Nib](https://github.com/jreese/nib) (MIT license)
    is a static site generator, written in Python, geared toward
    creating a simple site or blog. It uses inja2 and _Markdown_ is
    inspired by
    {{< iref "#poole" "Poole" >}}.
    _slow activity 21 commits between 2014 an 2018_.
    -   An example is
        [John Reese (author of Nib) noswap site](http://noswap.com/)
        ([source at GitHub](https://github.com/jreese/noswap)).
-   <a name="poole"></a>[Poole](https://bitbucket.org/obensonne/poole) (GPL)
    a static site generator written in a single 800 lines python script.
    It uses _Markdown_ for page formatting.
    _No more commit between July 2015 and 2018._
    -   [Pimp your Poole site with a free CSS template
        ](http://obensonne.bitbucket.org/blog/20091122-using-a-free-css-templates-in-poole.html)
        a recipe by the author Oben Sonne.
    -   There is a [list of sites built with poole
        ](https://bitbucket.org/obensonne/poole/wiki/Home),
        but it is obsolete and most sites are either down or have
        changed for an other generator. The main example is the
        home page of the author, [Oben Sonne
        ](http://obensonne.bitbucket.org/) which seems now unavailable
        ar this URL, but for which he still provides the
        [poole source](https://bitbucket.org/obensonne/poole-obs/src),
        and [generated html
        ](https://bitbucket.org/obensonne/obensonne.bitbucket.org/src).
        <br/>
        [Prof Gra site](http://profgra.org/lycee/index.html)
        is also still available.
    -    See also the derived {{< iref "#nib" "Nib" >}}.
-   <a name="ruhoh"></a>[Ruhoh](https://github.com/ruhoh/ruhoh.rb)
    (MIT License)
    is a static site generator in ruby, using _mustache_ for templates
    and _MarkDown_ as text format. _last commit 2014_.
    -    [GitHub: Ruhoh](https://github.com/ruhoh/ruhoh.rb/)
    -    _Ruho_ is geared to blogs, but allow
         also pages, and the [Ruhoh.com Site](http://ruhoh.com/)
         _now unavailable ?_
         show that it is not limited to blogs.
         [GitHub: Ruhoh.com source](https://github.com/ruhoh/ruhoh.com).
-   <a name="soho"></a>[Soho](http://pypi.python.org/pypi/soho)
    is a python script to build a static web site from a set of
    reStructuredText source files and a layout template file.
    The [site of the author of Soho Damien Baty: noherring.com
    ](http://code.noherring.com/)
    is an example of use of Soho.
    _soho is obsolete, last release 2012_.
-    <a name="strangecase"></a>[StrangeCase
    ](http://colinta.com/projects/StrangeCase.html) (BSD Like license)
    is the equivalent of {{< iref "#nanoc" "Nanoc" >}}
    but written in Python.
    _StrangeCase is not updated since beginning 2014._
    -   [GitHub - StrangeCase
            ](https://github.com/colinta/StrangeCase)
-   <a name="wok"></a>[Wok](http://wok.mythmon.com/)
    a static site generator written in python
    using a _Jinja2_ based templating system and  syntax highlighting
    via _Pygments_.
    Pages can be written in _Markdown_ or reStructuredText.
    _Wok_ Source is [hosted on GitHub](https://github.com/mythmon/wok),
    and the package is available in pypi.
    _13 commits in 2 years 2016-2018__

# Static site search
## Javascript search

-   [Fuse.js](https://github.com/krisk/fuse)(Apache License)
    fuzzy-search, in JavaScript
-   <a name="lunr"></a>[lunr.js](https://lunrjs.com/) (MIT License)
    -   [GitHub - lun.js](https://github.com/olivernn/lunr.js)
    -   [hugo-lunr - npm](https://www.npmjs.com/package/hugo-lunr)
        generate lunr.js index files from
        {{< iref "hugo" "Hugo static sites" >}}.
    -   [hexo-generator-lunr](https://github.com/zllovesuki/hexo-generator-lunr)
        Lunr index generator plugin for Hexo.
    -   [metalsmith-lunr](https://github.com/CMClay/metalsmith-lunr)
        A Metalsmith plugin that integrates the Lunr.js client side
        search engine.
    -   [jekyll_pages_api_search](https://github.com/18F/jekyll_pages_api_search).
        Jekyll search plugin based on lunr.js and jekyll_pages_api
-   [list.js](http://listjs.com/) (MIT License)
    library for adding search, sort, filters and flexibility to
    tables, lists and various HTML elements.
    -   [GitHub - javve/list.js](https://github.com/javve/list.js)
-   <a name="pagefind"></a>[PageFind](https://github.com/cloudcannon/pagefind) (MIT License)
    is a static search library using as little of your users' bandwidth as possible.

    PageFind run after you build your static site. After indexing, Pagefind adds a
    static search bundle to your built files, which exposes a JavaScript search API that
    can be used anywhere on your site.

   -   [PageFind - GitHub](https://github.com/cloudcannon/pagefind)
   -   [PageFind documentation](https://pagefind.app/docs/)

## Google site search

-   [Google Custom Search Engine](http://www.google.com/cse/)
    is add-powered or paid site search.
-   [How to add search to your static site
    ](http://www.unleashnetworks.com/blog/?p=388)
    is a recipe to get _Google cse_ working.
-   If the paid plan is too expensive you may try to
    [Replace Google Site Search with Bing Site Search
    ](http://www.orangetreeweb.com/articles/installing-bing-site-search.html).

## Hosted search service
See also {{< iref "content_management#search_engines" "Search Engines" >}} where you can
find hosted search engines {{< iref "content_management#bonsai" "Bonsai" >}}, and
{{< iref "content_management#meilisearch" "Meilisearch" >}}.

-   <a name="algolia"></a>[Algolia](https://www.algolia.com/) (private)
    is a search service, there are free plans for opensource.
    -   Hexo has to plugins for algolia search
        [hexo-algoliasearch
        ](https://github.com/LouisBarranqueiro/hexo-algoliasearch) and
        [hexo-algolia](https://github.com/oncletom/hexo-algolia).
    -   [metalsmith-algolia](https://github.com/stafyniaksacha/metalsmith-algolia)
        is a metalsmith plugin for indexing content on Algolia.




<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
