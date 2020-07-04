---
title: Python Web Programming
---

{{% toc /%}}

----

The {{< iref "templating" "Templating libraries" >}}
are in their own section.

# General references

-   [awesome python - web
    ](https://github.com/vinta/awesome-python#wsgi-servers)
    list of resources for Web Content Extracting, Web Crawling,
    Web Frameworks, WebSocket, WSGI Servers.
-   [pythonidae - server
    ](https://github.com/svaksha/pythonidae/blob/master/Server.md)
    *awesome list* for python crawlers, browser, Network, ftp,
    web-frameworks,  Django, web-server.
-   [pycrumbs - web](https://github.com/kirang89/pycrumbs#web)
    *awesome list* for web, Frameworks, Web Servers, API and Web
    Services.

# HTTP Libraries {#http_libraries}
## standard library modules
The standard library provides the following modules:

-   [http.client](http://docs.python.org/3/library/http.client.html)
    implement the client side of the HTTP and HTTPS protocols.
    It is normally  used though the
    {{< iref "#urllib" "utllib module" >}}.
    in python 2 it is called [httplib
    ](http://docs.python.org/2/library/httplib.html)
-   [http.cookies](http://docs.python.org/3/library/http.cookies.html)
    <a name="http_cookies"></a>
    abstract the concept of cookies, an HTTP state management mechanism.
    It supports both simple string-only cookies, and also any
    serializable data-type as cookie value, it is principally useful
    for server-side code see following
    [http.cookiesjar]{{< iref "#urllib" "#http_cookiesjar "internal reference") for     client side processing. [urllib.request" >}}
    also handle cookies with the class _HTTPCookieProcessor_.
    -   In python 2 this module was named [cookie
        ](http://docs.python.org/2/library/cookie.html).Doug Hellmann
    -   [PyMOTW: Cookie](https://pymotw.com/3/Cookie/).
-   [http.cookiesjar](http://docs.python.org/3/library/http.cookiejar.html)
    <a name="http_cookiesjar"></a>
    handle reading of HTTP cookies.
    -  In python2 it was named
       [cookielib](http://docs.python.org/2/library/cookielib.html).
    -  [cookielib and ClientCookie
       ](http://www.voidspace.org.uk/python/articles/cookielib.shtml)
       tutorial by Michael Foord .
-   [urllib module](http://docs.python.org/3/library/urllib.html)
    <a name="urllib"></a> provides
    a simple interface for network resource access. In python 3 it is
    split in several submodules:
    -   [urllib.request
        ](https://docs.python.org/3/library/urllib.request.html)
        <a name="urllib_request"></a>for opening and reading URLs
        using basic and digest  authentication, redirections, cookies,
        etc.,
        _The {{< iref "#request" "Requests package" >}}
        is recommended for a higher-level http client interface._
    -   _urllib.error_ containing the exceptions raised by urllib.request,
    -   [urllib.parse]
        ](https://docs.python.org/3/library/urllib.parse.html)
        for parsing URLs,
    -   _urllib.robotparser_ for parsing robots.txt files.

    -   [HOWTO Fetch Internet Resources Using The urllib Package
        ](http://docs.python.org/3/howto/urllib2.html)
        by Michael Foord.
-   In python 2 the [urllib module
    ](http://docs.python.org/2/library/urllib.html#module-urllib)
    helped by [urlparse module
    ](http://docs.python.org/2/library/urlparse.html#module-urlparse)
    provided the interface for fetching data across the Web.
    It has been improved in [urllib2
    ](http://docs.python.org/2/library/urllib2.html)
    which help in opening URLs (mostly HTTP) using basic and digest
    authentication, redirections, cookies to
    provide facilities close to the new
    {{< iref "#urllib" "python3 urlllib module" >}}.
    -   [urllib/urllib2 porting from Python2 to Python3
        ](http://docs.pythonsprints.com/python3_porting/py-porting.html#url-related-modules).
    -   [HOWTO Fetch Internet Resources Using The urllib2 Package
        ](http://docs.python.org/2/howto/urllib2.html)
        by Michael Foord. Previously named: *urllib2 - The Missing Manual*
    -   Doug Hellmann PyMOW examples: [urllib
        ](https://pymotw.com/3/urllib/) ),
    -   [urllib2](https://pymotw.com/3/urllib2/),
    -   [urlparse](http://pymotw.com/2/urlparse/index.html#module-urlparse).
    -   [urllib2 - The Missing Manual
        ](http://www.voidspace.org.uk/python/articles/urllib2.shtml)


## Third party modules

-   [httplib2](https://github.com/jcgregorio/httplib2)(MIT License)
     is an HTTP/HTTPS client library with support for authentication
     basic digest or [WS-Security](http://en.wikipedia.org/wiki/WS-Security),
     redirects, compression.
     It has a python2 and python3 version.
-   [Requests](http://docs.python-requests.org/en/latest/) (Apache2 License)
    <a name="request"></a>
    is an improvement of _urllib2_ powered by  httplib and
    {{< iref "#urllib3" "urllib3" >}}.
    allow you to send HTTP/1.1 requests. You can add headers,
    form data, multipart files,
    and parameters with simple Python dictionaries, and access the response data
    in the same way.
-   [urllib3](https://pypi.python.org/pypi/urllib3) (MIT License)
    <a name="urllib3"></a>
    is an HTTP library with thread-safe connection pooling, file post,
    compresion. It works with python2 and python3. An upper layer is
    provided by the {{< iref "#request" "request library" >}}.
    [urllib3 documentation](http://urllib3.readthedocs.org/en/latest/).
# CGI
See also the [CGI protocol references
](internet_application#web_protocols "internal reference")

See also the {{< iref "#http_libraries" "http libraries section" >}},
{{< iref "#urllib_request" "urllib.request" >}},
{{< iref "#http_cookies" "http.cookies" >}},
{{< iref "#http_cookiesjar" "http.cookiesjar" >}},
and the third party modules {{< iref "#urllib3" "urllib3" >}},
{{< iref "#request" "request" >}}.

-   [CGI scripts references](http://wiki.python.org/moin/CgiScripts)
-   [cgitb module](http://docs.python.org/3/library/cgitb.html)
    or
    [python 2 cgitb module](http://docs.python.org/2/library/cgitb.html)
    is a configurable traceback handler for CGI scripts. Doug Hellmann
    [cgitb tutorial](https://pymotw.com/3/cgitb/).
-   [cgi](http://docs.python.org/3/library/cgi.html)
    Helpers for running Python scripts via the Common Gateway Interface.
    [python 2 cgi module](http://docs.python.org/2/library/cgi.html).
-   [CGIHTTPServer](http://docs.python.org/3/library/cgihttpserver.html)
    HTTP servers which can run CGI scripts.
    [python 2 CGIHTTPServer
    ](http://docs.python.org/2/library/cgihttpserver.html)
-   [Using Python for CGI programming*
    ](http://www.python.org/doc/essays/ppt/sd99east/index.htm)
    a 1999 tutorial to python and cgi programming by Guido van Rossum.
-   [CGI Web Applications with Python, Part Two
    ](http://www.voidspace.org.uk/python/articles/cgi_web_applications_two.shtml)



# WSGI {#wsgi}

[WSGI or Web Server Gateway Interfaces](http://en.wikipedia.org/wiki/WSGI)
define an interface between web servers and web applications or
{{< iref "#web_frameworks" "Web frameworks" >}} for the Python
programming language.

Numerous Web application frameworks are
[supporting WSGI](http://wsgi.readthedocs.org/en/latest/frameworks.html):
see the {{< iref "#web_frameworks" "framework section" >}}

-   The   [new wsgi specification PEP 3333](https://www.python.org/dev/peps/pep-3333/)
    for python 3 updates
    [PEP333](https://www.python.org/dev/peps/pep-0333/ "python.org pep-0333")
    the reference implementation for python 2 that is standard since python 2.5,
-   The python module is [wsgiref](https://docs.python.org/3/library/wsgiref.html).

    Quoting the module introduction:
    _wsgiref can be used to add WSGI support to a web server or
    framework. It provides utilities for manipulating WSGI environment
    variables and response headers, base classes for implementing WSGI
    servers, a demo HTTP server that serves WSGI applications, and a
    validation tool that checks WSGI servers and applications for
    conformance to the WSGI specification_.

## WSGI Documentation and Tutorials
-   Wsgi specification for python 3 is the
    [PEP 3333](http://www.python.org/dev/peps/pep-3333/) that replaces the
    [PEP 333](http://www.python.org/dev/peps/pep-0333/) which is the python 2 implementation.
-   [HOWTO Use Python in the web](https://docs.python.org/3/howto/webservers.html)
    by Marek Kubica introduces cgi fastcgi and wscgi.
-   [wsgi.org](http://wsgi.readthedocs.org/en/latest/) includes
    lists of
    [wsgi specifications](http://wsgi.readthedocs.org/en/latest/specifications.html),
    [tutorials](http://wsgi.readthedocs.org/en/latest/learn.html), and
    [presentations](http://wsgi.readthedocs.org/en/latest/presentations.html).
-   [Web Python Tutorial](http://webpython.codepoint.net/)
    is an elementary tutorial covering WSGI, CGI and mod_python.
-   Paul Bonser's
    [Building a Python Web Application, Part 1
    ](http://blog.paulbonser.com/2008/06/26/building-a-python-web-application-part-1/)
    is a tutorial on wsgiref.
-   [Introducing WSGI: Python's Secret Web Weapon part I
    ](http://www.xml.com/lpt/a/1674)
    and [part II](http://www.xml.com/lpt/a/1675) By
    James Gardner gives a very clear introduction to  wsgi _2008_.
-   [WSGI tutorial from Chris Rossi](http://archimedeanco.com/wsgi-tutorial/)
    introduces wsgi and webob and pastedeploy _2009_.


## Wsgi Servers {#wsgi_servers}
[wsgi.org](http://www.wsgi.org/) has a list of
[Servers which support WSGI](http://www.wsgi.org/en/latest/servers.html).

-   To test wsgi applications one needs a simple wsgi server. You can play with
    servers:
    [wsgiref.simple_server
    ](http://docs.python.org/3/library/wsgiref.html#module-wsgiref.simple_server)
    from  [wsgiref](http://docs.python.org/3/library/wsgiref.html)
    or the older  [WsgiUtils](http://www.owlfish.com/software/wsgiutils/)
    from Colin Stewart that provides multi-threads, basic user
    authentication, signed cookies, and persistent sessions.
    There is also a  multi-threaded
    [James WSGI Server](http://wsgiarea.pocoo.org/james/).
-   [Gunicorn](http://gunicorn.org/) <a name="gunicorn"></a>(MIT License)
     is a Python WSGI HTTP Server for UNIX built on pre-fork worker
     model. It is usually deployed behind {{< iref "nginx" "nginx" >}}.
     -   [Gunicorn documentation](http://docs.gunicorn.org/)
-   [uWSGI](http://projects.unbit.it/uwsgi/wiki)
    is a fast application container server coded in pure C.
    It can work stand-alone or behind apache/nginx/lighttpd/cherokee.
    -   [The uWSGI project documentation](http://uwsgi-docs.readthedocs.org/en/latest/)
    -   [ArchWiki: uWsgi](https://wiki.archlinux.org/index.php/Uwsgi)
    -   [django can be used with uWSGI](https://docs.djangoproject.com/en/dev/howto/deployment/wsgi/uwsgi/).
    -   See below in the {{< iref "#wsgi_servers" "wsgi Servers section" >}} how
        uWSGI can be used with apache, nginx, lighttpd, and cherokee.
-   Applications can also be tested with
    [WebTest](http://pythonpaste.org/webtest/) that provides an interface to run WSGI applications
    and verify the output without starting
    an HTTP server.<br />
    Ian Bicking has a
    [WebTest Howto](http://blog.ianbicking.org/2010/04/02/webtest-http-testing/)
    in his blog.
-   [flup](http://www.saddi.com/software/flup/)
    (BSD license) is a collection of WSGI modules.
    It provides three set of
    [WSGI servers/gateways](http://trac.saddi.com/flup/wiki/FlupServers)
    which speak AJP, FastCGI, and SCGI.
    [flup on pypi](https://pypi.python.org/pypi/flup/)
-   {{< iref "apache" "Apache" >}}
    provides a wsgi [mod_wsgi](http://code.google.com/p/modwsgi/) module.
    It allows also to run uwsgi with [Apache2 mod_uwsgi or mod_proxy_uwsgi
    ](http://projects.unbit.it/uwsgi/wiki/RunOnApache2).
-   {{< iref "nginx" "nginx" >}}.
    has also its [wsgi module](http://wiki.nginx.org/NginxNgxWSGIModule)
    and alternatively can also
    [delegate to uwsgi](http://projects.unbit.it/uwsgi/wiki/RunOnNginx)
    or act as a reverse proxy in front of {{< iref "#gunicorn" "Gunicorn" >}}
-   {{< iref "lighttpd" "Lighttpd" >}}
    recommends to run wsgi via FastCGI in its
    [HOW-TO WSGI](http://redmine.lighttpd.net/projects/4/wiki/Howto_WSGI).
    There is an [experimental uwsgi module](http://projects.unbit.it/uwsgi/wiki/RunOnLighttpd)
-   [Cherokee](http://www.cherokee-project.com) has an
    [uWSGI handler](http://www.cherokee-project.com/doc/cookbook_uwsgi.html).
-   [ bjoern](https://github.com/jonashaag/bjoern) (BSD License)
    by Jonas Haag, a Python WSGI server written in C.

##  WSGI Libraries
As a WSGI Library is the heart of a Web framework you may want to look also at the
{{< iref "#web_frameworks" "Web Frameworks section" >}}

The {{< iref "#http_libraries" "http libraries" >}}
can also be used for wsgi programming, but are mainly used on the client side.

[wsgi.org](http://www.wsgi.org/) has lists of
[Middleware and libraries for WSGI
](http://www.wsgi.org/en/latest/libraries.html),
[Frameworks that run on WSGI](http://www.wsgi.org/en/latest/frameworks.html)
[Testing tools for WSGI](http://www.wsgi.org/en/latest/testing.html)
that may be more up-to-date than the
-[Python Wiki: Implementations of WSGI
](http://wiki.python.org/moin/WSGIImplementations).

-   [Pesto](http://pesto.redgecko.org/)
    is a small library for Python wsgi applications.
-   [WebOb](http://pythonpaste.org/webob/) <a name="webob"></a>
    (MIT-style license), a refinement of Paste, is a WSGI library.
    Since version 1.2 it is compatible with python 3.

    Ian Bicking has written numerous examples of use of WebOb:

    -   [What Does A WebOb App Look Like?](http://blog.ianbicking.org/2010/03/12/a-webob-app-example/)
        an example explaining the use of _dispatcher_ and _controller_.
    -   [WebOb File-Serving Example](http://pythonpaste.org/webob/file-example.html)
        shows how you can make a static-file-serving application using WebOb.
    -   [Comment Example](http://pythonpaste.org/webob/comment-example.html)
        shows how to write with WebOb a WSGI middleware which adds a
        simple comment form to HTML web pages.
    -   [Wiki Example](http://pythonpaste.org/webob/wiki-example.html)
        is an example of how to write a WSGI application using WebOb.
        This example application implements a very simple wiki.
    -   [JSON-RPC Example](http://pythonpaste.org/webob/jsonrpc-example.html)
        is an example of how to write a web service using WebOb.
    -   [Another Do-It-Yourself Framework](http://pythonpaste.org/webob/do-it-yourself.html "pythonpaste.org webob/do-it-yourself.html")
        shows you how to create a web framework of your own using
        WSGI and WebOb.
    -   [Ian Bicking blog: Decorators and Descriptors](http://blog.ianbicking.org/2008/10/24/decorators-and-descriptors/)
    -   [webob descriptors](https://github.com/Pylons/webob/blob/master/webob/descriptors.py)
        and [webob decorators](https://github.com/Pylons/webob/blob/master/webob/dec.py)
        in the
        [Pylon webob  repository](https://github.com/Pylons/webob)
    -   [WebOb static]()
        is a tiny module to serve from WSGI your files/directories.
    -   [GitHub: Sergey Schetinin (Maluke) ]()
-   [werkzeug](http://werkzeug.pocoo.org/) (BSD License) <a name="werkzeug"></a>
    is a wsgi framework for python 2.x/3.x. It is the base of
    {{< iref "#flask" "Flask" >}}
    the development is hosted in the
    [werkzeug gitHub Repository](http://github.com/mitsuhiko/werkzeug/).


##  WSGI Middlewares.

-   [Middleware and libraries for WSGI
    ](http://wsgi.readthedocs.org/en/latest/libraries.html),
    at [wsgi.org](http://wsgi.readthedocs.org/en/latest/).
-   Luke Arno's
    [yaro](https://pypi.python.org/pypi/yaro) (LGPL) _Yet Another
    Request Object_ _2008_.
-   [repoze.who](https://github.com/repoze/repoze.who) (BSD License)
    is a WSGI Authentication Middleware
    -   [Repoze.who Documentation](http://repozewho.readthedocs.org/en/latest/)
    -   [Understanding Repoze.who with BottlePy](http://blog.nturn.net/?tag=bottle)
        in Hailstone3 blog.


# Web application framework {#web_frameworks}
A [web application framework
](http://en.wikipedia.org/wiki/Web_application_framework)
is aimed to supporting the development of dynamic websites, Web
applications and Web services. They are closely related to
{{< iref "#wsgi" "WSGI" >}} that provide interface with web
servers and they all use a {{< iref "#template_engines" "template engine" >}}.

The {{< iref "static_sites" "static site generators" >}} have their own section.

-   Two large lists of frameworks:
    [python wiki: Web frameworks](http://wiki.python.org/moin/WebFrameworks) and
    [WSGI Wiki](http://wsgi.readthedocs.org/en/latest/frameworks.html).
-   [Choosing a WSGI Framework for API Services
    ](https://doughellmann.com/blog/2012/10/15/ods-grizzly-choosing-a-wsgi-framework-for-api-services/)
    by Doug Hellmann  look how frameworks may, or may not, be suitable
    for use when building new API servers for OpenStack projects. _2012_

## Bottle {#bottle}
[Bottle](http://bottlepy.org/docs/dev/index.html)
is a single-file, lightweight WSGI Python web-framework. It has no dependencies other
than the Python Standard Library. It is built around a powerfull routing scheme,
supports a custom template system and mako, cheetah, jinja2. It provides the usual
development server, and can be served by any compatible WSGI server.

-   [GitHub: Bottle dev](https://github.com/defnull/bottle)
-   [ArchWiki: Bottle](https://wiki.archlinux.org/index.php/Bottle)
-   A minimal 60 slocs [Bottle Example](https://gist.github.com/Arthraim/994641)
-   [Kiss Bottle Wiki](https://github.com/Matael/kiss-bottle-wiki/)
    is a trivial 170 slocs _Bottle_ wiki _2012_.
-   [Yaki-tng](https://github.com/rcarmo/yaki-tng) is a rewrite of the
    [Yaki](https://github.com/rcarmo/Yaki) Python wiki, using _Bottle_.
    The [Yaki web Page](https://the.taoofmac.com/space/projects/Yaki).
-   [Understanding Repoze.who with BottlePy
    ](http://blog.nturn.net/?tag=bottle)
    in Hailstone3 blog.

## CherryPy
[CherryPy](http://www.cherrypy.org/) (Bsd license)
 <a name="cherrypy"></a>
 is a python, object-oriented Web framework. The
 templating system is  released as a separate standalone module.
-   [CherryPY Bitbucket repo.](https://bitbucket.org/cherrypy/cherrypy)
-   [CherryPy Documentation](http://cherrypy.readthedocs.org/en/latest/)


## Django {#django}
[Django](http://www.djangoproject.com/)
    (BSD License) is a Python Web framework that includes a template
    language. Django sites can be served by wsgi,
    apache+modpython,  or fastcgi.

-   List of [Django ressources
    ](http://code.djangoproject.com/wiki/DjangoResources).
-   [List of Django tutorials
    ](http://code.djangoproject.com/wiki/Tutorials).
-   [Documentation en français de Django](http://docs.django-fr.org/).
-   [The Django Book version 2](http://djangobook.com/en/2.0/)
-   [Pinax](http://pinaxproject.com/)
    is a collection of reusable apps for Django.
-   Some CMS built on the top of Django:
    [Django-cms](https://www.django-cms.org/en/) (BSD Licence),
    [Mezzanine](http://mezzanine.jupo.org/) (BSD Licence)

## Flask {#flask}
[Flask](http://flask.pocoo.org) (BSD License)
is a microframework for Python based on
[Werkzeug](http://werzeug.pocoo.org) and Jinja 2.

-   [OpenTechSchool - Websites with Python Flask
    ](http://opentechschool.github.io/python-flask/)
-   [Python Web Applications With Flask
    ](http://www.realpython.com/blog/python/python-web-applications-with-flask-part-i/),
    [Part II
    ](http://www.realpython.com/blog/python/python-web-applications-with-flask-part-ii-app-creation/)
-   [The Flask Mega-Tutorial
    ](http://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world)
    by  Miguel Grinberg, Miguel has
    [many flask tutorials](http://blog.miguelgrinberg.com/category/Flask)
    I have used also [Designing a RESTful API with Python and Flask
    ](http://blog.miguelgrinberg.com/post/designing-a-restful-api-with-python-and-flask)
    and [Designing a RESTful API using Flask-RESTful
    ](http://blog.miguelgrinberg.com/post/designing-a-restful-api-using-flask-restful)
    which are part of his [Rest Tutorial (GitHub)
    ](https://github.com/miguelgrinberg/REST-tutorial).


There are many extensions for Flask some in the
[list of approved Flask extensions
](http://flask.pocoo.org/extensions/),
you can find many others by
[searching pypi for Flask
](https://pypi.python.org/pypi?%3Aaction=search&term=flask&submit=search).

-   [Frozen-Flask](https://github.com/SimonSapin/Frozen-Flask)
    (BSD License) by Simon Sapin; allow to froze a flask
    application into a set of static files.
    -   [Hosting static Flask sites for free on Github Pages
        ](http://www.stevenloria.com/hosting-static-flask-sites-for-free-on-github-pages/)
        is a tutorial by Steven Loria accompanied by an
        [example of  static Flask app on Github pages
        ](https://github.com/sloria/flask-ghpages-example),
        [_killtheyak_ - a larger example
        ](https://github.com/killtheyak/)
        the source of [killtheyak.com](http://killtheyak.com/)
        is also available.
    -   [Creating Plume: A static site generator with Flask - Part 1
        ](http://obsoleter.com/2012/12/12/creating-plume-a-static-site-generator-with-flask-part-1/)
        by Jeremy Axmacher.
-   [Flask-mustache](https://github.com/ahri/flask-mustache)
     allow use of mustache with Flask, using *pystache*.
-   [flask-mustachejs](https://github.com/bradleywright/flask-mustachejs)
     is  a *Mustache* templating tools for integration with Flask, written in
     javascript with *jQuery*.
-   [Flask-rst](https://github.com/jarus/flask-rst)
    is a python tool to create a website from a source of
    reStructuredText that uses Flask.
-   <a name="markwiki"></a>[MarkWiki
    ](http://pythonhosted.org/MarkWiki/) (BSD License)
    is a _Python_ + Flask wiki _not static_ that uses Markdown to create pages.
    Markwiki has an option to _freeze_ the wiki with
    {{< iref "#frozen" "Frozen-Flask" >}} and export it to a
    static site.
    -   [GitHub: MarkWiki](https://github.com/mblayman/markwiki)
-   <a name="simple-docs"></a>[simple-docs
    ](https://github.com/chrislaskey/simple-docs)
    (MIT license) is a Python Flask website for
    viewing _Markdown_ documentation files online. It is not a static
    site generator, but can be used for this task with
    {{< iref "#frozen" "Frozen-Flask" >}}.

## Nevow
[Nevow](https://launchpad.net/nevow)
(MIT License) a [divmod.org project](http://divmod.org)
is a Python web application framework. It includes a
pure Python XML expression syntax to express the view logic in
Python, it uses a small XML attribute language to provide
templates. Nevow also includes a two-way bridge between Javascript
in a browser and Python on the server.

_Nevow development seem quite slow since 2011 and the last release is
in 2009_.



## Pyramid and Pylons {#pylon}

[Pylons](http://www.pylonsproject.org/projects/pylons-framework/)
(BSD License) is a lightweight
web framework that uses a common api to templating engines like
Cheetah, Cherry Templates, Kid, Myghty, Breve, Genshi, Mako
and {{< iref "#webob" "WebOb" >}} as wsgi framework.
[Wikipedia:Pylons](http://en.wikipedia.org/wiki/Pylons_%28web_framework%29)

[Pyramid](http://www.pylonsproject.org/projects/pylons-framework/)
is a minimalistic web framework inspired by Zope, Pylons and Django.

## Tornado {#tornado}
[Tornado](http://www.tornadoweb.org/) (Apache License)
is a Python web framework and asynchronous networking library.

-   {{< wp "Tornado_(web_server"  "Wikipedia: Tornado" >}}
-   [cyclone](http://cyclone.io/) (Apache License) <a name="cyclone"></a>
    is a web server framework
    for Python that implements the Tornado API as a Twisted protocol.

## Turbogears
[Turbogears](http://www.turbogears.org/)
(MIT License, LGPL) is a web framework designed around the
model-view-controller architecture, it uses a python written
infrastructure composed of SQLObject as backend to interface with
the database, one of Kid, Genshi, Cheetah, Django templates, Jinja
as templating engine, Cherrypy to wrap the http protocol and
optionaly MochiKit to wrap javascript in a pythonic way.
[Wikipedia: Turbogears](http://en.wikipedia.org/wiki/Turbogears)

Turbogears uses {{< iref "#webob" "Pylons and WebOb" >}}.

## web2py
[web2py](http://mdp.cti.depaul.edu/examples/default/index)
(GPL for the software, but no free manual) is a lightweight web
framework, web2py is **NOT** web.py.

## webpy
[webpy](http://webpy.org/) (Public Domain) is a
lightweight web framework. web.py offers a custom templating
language *Templetor*, but allows also Mako or Cheetah. It relies on
*flup* for wsgi, and postgresql+psycopg2 or mysql+MySQLdb for the
databases.*

-   [webpy list at google groups](http://groups.google.com/group/webpy).
-   A recipe to
    [Use SQLObject and SQLite with web.py](http://schwarzwald.infogami.com/blog/webpysqlobject).
-   The [Infogami](http://infogami.org/) wiki is powered
    up by web.py.

## Zope
[Zope](http://www.zope.org) an open source (Zope Public License
GPL compatible) application server for building content management
systems.

# Client side web browser programming {#browser_programming}

-   [Python Wiki: Web browser programming
    ](http://wiki.python.org/moin/WebBrowserProgramming)
-   [Deliverance](https://github.com/deliverance/Deliverance/)
    (BSD like license) is a tool to theme HTML, applying a consistent
    style to applications and static files, separating site-wide
    styling from application-level templating. It is
    similar in function to XSLT but using a simpler
    XML-based language to express the transformation.
    -   [Deliverance package documentation
    ](http://packages.python.org/Deliverance/)
    -   [PyPi: Deliverance release
        ](https://pypi.python.org/pypi/Deliverance)
-   [PyJamas or pyjs](http://pyjs.org/)
    is a toolkit for the Web. PyJamas comprises a widget set, AJAX
    library and a python-to-javascript compiler.
    -   <a name="pyjamasdesktop"></a>__PyjamasDesktop__ or __pyjs__
        is a cross-platform framework and
        applications widget set for the desktop using PyJamas. There are
        three back-ends: WebKit taht uses PyWebkitGtk, XULrunner port that
        uses python-xpcom and hulahop, and MSHTML taht uses python win32
        comtypes.. The XULrunner port uses python-xpcom and hulahop; the
        Webkit port uses PyWebkitGtk and the MSHTML port uses python win32
        comtypes. You can use the API without knowing anything about the
        actual backend.
    -   [Introduction to Pyjamas, Part 1: Exploit the synergy of GWT and Python
        ](http://www.ibm.com/developerworks/web/library/wa-aj-pyjamas/)
        an _IBM Developer work talk_ by Rick Hightower.
    -   [Pyjamas Example](http://pyjs.org/examples/)
    -   [Pyjamas FAQ](http://pyjs.org/#FAQ)
    -   [Pyjamas Book](http://pyjs.org/book/output/Bookreader.html)
-   [pyquery](http://packages.python.org/pyquery/)(BSD License)
    allows you to make jquery queries on xml documents.
    The API is as much as possible the similar to jquery.
    pyquery uses lxml for fast xml and html manipulation.
-   [Skulpt](http://www.skulpt.org/) is a Python-to-JavaScript
    compiler that is focussing on providing full Python syntax.
    it is used online by [CodeSkulptor](http://www.codeskulptor.org/).
    [Skulpt GitHub repository](https://github.com/bnmnetp/skulpt/).
-   [Brython](http://brython.info/)
    is a  Python 3 implementation for client-side web programming.
    Brython is designed to replace Javascript as the
    scripting language for the Web.


# Web client side programming {#web-client-programming}
See also the section {{< iref "python_libraries#xml_parsers" "XML parsers" >}}

In the following list the most up-to-date frameworks to do web client
programming seems to be {{< iref "#mechanize" "mechanize" >}} and
{{< iref "#splinter" "splinter" >}}.

-   [Python Wiki: Web client programming
    ](http://wiki.python.org/moin/WebClientProgramming)
-   [Beautiful Soup](http://www.crummy.com/software/BeautifulSoup/)
    is a Python permissive HTML/XML parser that can be used for site scraping.
-   [lxml.html can be used as a web scraping library
    ](http://blog.ianbicking.org/2008/12/10/lxml-an-underappreciated-web-scraping-library/)
    a blog from Ian Bicking.
-   <a name="mechanize"></a>[Mechanize
    ](http://wwwsearch.sourceforge.net/mechanize/) (BSD License)
    is a python module by John J. Lee that implements stateful
    programmatic web browsing in Python.
    -   [Mechanize repository at GitHub](https://github.com/jjlee/mechanize)
    -   [Browsing in Python with Mechanize
        ](http://www.pythonforbeginners.com/python-on-the-web/browsing-in-python-with-mechanize)
        and [Python Mechanize Cheat Sheet
        ](http://www.pythonforbeginners.com/cheatsheet/python-mechanize-cheat-sheet/)
-   [Mechanoid
    ](http://pypi.python.org/pypi?:action=display&name=mechanoid)
    (GPL) is a programmatic browser
    written in Python. It is a fork of  mechanize _released in 2006_
-   [mxTidy
    ](http://www.egenix.com/products/python/mxExperimental/mxTidy/)
    (CNRI Python license like) provides a Python interface to a
    thread-safe, library version of the HTML Tidy command line tool.
-   [Red Bot](http://mnot.github.io/redbot/) (MIT License) is a python
    web tool that check and report HTTP resources.  A public instance
    of RED is available at [redbot.org](http://redbot.org).  It allows
    to follow all redirects on an URL, you just follow the succession
    of *Location* headers. It can be very useful to see how big server
    redirect a download depending on your ip geographic zone.
-   [Scrapy](http://scrapy.org/)
    is a high-level screen scraping and web crawling framework
-   <a name="splinter"></a>[Splinter
    ](http://splinter.readthedocs.org/en/latest/index.html)
    (BSD License) is a python web-automation tool. It lets you
    automate browser actions, such as visiting URLs and interacting
    with their items.
    -   [GitHub: Splinter](https://github.com/cobrateam/splinter)
    -   Splinter is built on the top of the
        [Selenium](http://docs.seleniumhq.org/) (Apache License)
        web automation tool.
-   [twill](http://twill.idyll.org/)(MIT license)
    a fork of mechanize, is a simple scripting language intended for
    programmatic or automated browsing of Web sites. _Last release
    2007_
-   The modules of the {{< iref "python_libraries#structured_markup_libs" "Structured markup section" >}}
    are also relevant, mainly {{< iref "python_libraries#xml_parsers" "XML Parsers" >}}
    [HTML5lib](http://code.google.com/p/html5lib/),
    [ElementTree](http://www.effbot.org/zone/element-index.htm),
    [lxml.html](http://codespeak.net/lxml/lxmlhtml.html),
    [4suite](http://4suite.org/),
    [Universal Feed Parser](http://www.feedparser.org/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
