<!--
.. description:
.. date: 2015-05-03
.. slug: python_dbms
.. tags:
.. link:
.. book: mzlinux
.. title: Python database programming in python
-->



[TOC]

-----

This page deals with database programming in python, at the low and higher
level i.e. Object Relational Mappers.

The database management systems are in the
[Databases section](/node/dbms "internal reference") and sub-sections.

## Low level DBMS interfaces
-   [Python Wiki: Database programming
    ](http://wiki.python.org/moin/DatabaseProgramming)
    is the starting point for learning about using databases from
    Python, it gives references to the DB API and databases management
    systems supported by Python libraries.

-   [Python Wiki: Database Interfaces
    ](http://wiki.python.org/moin/DatabaseInterfaces)
    lists database systems that have Python interfaces available.
-   [PEP 249 -- Python Database API Specification v2.0
    ](http://www.python.org/dev/peps/pep-0249/);
    the [FAQ](http://wiki.python.org/moin/DbApiFaq)
    explains how to pass parameters to the _cursor.execute_ method.

### DBM and Berkeley DB
-   The module [dbm](http://docs.python.org/py3k/library/dbm.html)
     interfaces variants of the DBM database — dbm.gnu, dbm.ndbm or
     dbm.dumb, both in py2k and py3k.
-   [pybsdbd](http://www.jcea.es/programacion/pybsddb_doc/)
    provides python wrappers for Berkeley DB. For py3k you have
    to use this third party module as the legacy module
    [bsddb](http://www.python.org/doc/lib/module-bsddb.html)
    is deprecated and no longer present in python 3.x.
-   The module [dbhash](http://docs.python.org/library/dbhash.html)
    bridges berkeley db to an dbm like interface is also deprecated
    and no longer present in py3k.

### Mysql
-   There are
    [many MySQL interfaces](http://wiki.python.org/moin/MySQL), all of them
    are not compatible with the
    [PEP 249](http://www.python.org/dev/peps/pep-0249/) nor ported to py3k.
-   [mysql-python: MySQLdb](http://mysql-python.sourceforge.net/MySQLdb.html)(GPL)
    is an thread-compatible, PEP249 compatible,   low level interface to
    [MySQL](/node/dbms "internal reference"). _for version 1.2 only
    python 2_. It is packaged in debian.
    See [PyMySQL](#pymysql "local reference) for a compatible
    python 3 library.
-   [MySQL Connector/Python](https://launchpad.net/myconnpy) (GPL) compatible
    with PEP249. It is a pure python implementation. You find the
    [source code in Bazaar
    ](http://bazaar.launchpad.net/~geertjmvdk/myconnpy/main/view/head)
    _python 2 and 3_. It is packaged in _debian_ as _python3-mysql.connector_.
    -   [MySQL Connector/Python Developer Guide
        ](http://dev.mysql.com/doc/connector-python/en/index.html).
-   )<a name="pymysql"></a>[PyMySQL
    ](https://github.com/PyMySQL/PyMySQL) (MIT License)
    is  a drop-in replacement for MySQLdb and work on CPython, PyPy,
-   IronPython and Jython. It works with CPython >= 2.6 or >= 3.3.
-   [OurSQL](http://packages.python.org/oursql/)
    provides MySQL bindings for python 2.4+ and python 3.x.

### Sqlite3
-   [sqlite3 module](http://docs.python.org/py3k/library/sqlite3.html)
    is a standard python module, and is compatible with the
    [PEP 249](http://www.python.org/dev/peps/pep-0249/)
-   [PyMOTW: sqlite3](https://pymotw.com/3/sqlite3/index.html)

## Postgresql
-   [psycopg](http://initd.org/psycopg/) (GPL) a PostgreSQL adapter
    that fully implements the Python DB API 2.0 specifications. It
    is designed for heavily multi-threaded applications, and
    works with with both python 2 and python 3.

## Other relational DBMS
-   [pymssql](http://pymssql.org/)
    provides access to Microsoft SQL Servers (proprietary),
    It is compliant with Python DB-API 2.0 Specification
    support python > 2.6 or Python > 3.3
-   [KInterbasDB ](http://www.ibphoenix.com/download/connectivity/python) (BSD license)
     implements Python Database API 2.0-compliant support for
     Firebird (Mozilla Public License like).
-   [pyfirebirdsql](https://github.com/nakagami/pyfirebirdsql/)
    is a python binding to Firebird. It works on Python 2.5+
    (including Python 3.x).

## [CouchDB](/node/dbms#couchdb)
-   [Getting started with  couchDB and Python
    ](http://wiki.apache.org/couchdb/Getting_started_with_Python)
    in the CouchDB Wiki, list all python interfaces.
-   [couchdb-python](https://github.com/djc/couchdb-python) (New BSD License)
    is Python package for working with CouchDB from Python code 2.x or
    3.x.
    -   [CouchDB-Python Manual](http://packages.python.org/CouchDB/)
-   [py-couchdb (GitHub)](https://github.com/niwibe/py-couchdb) (BSD
    License) is a pure python _CouchDB_ Client, compatible with Python 3.
    It's main specific feature is to use the
    [request library](http://docs.python-requests.org/en/latest/).
    -   [py-couchdb documentation](https://py-couchdb.readthedocs.org/en/latest/)
-   [couchquery](http://mikeal.github.com/couchquery/) (LGPL)
     is a  Python library for CouchDB.
    -   Couchquery contains the
        [module couchshelve
        ](https://github.com/mikeal/couchquery/blob/master/couchquery/shelve.py)
        that provides an API identical to the standard python
        shelve module, but using couchdb for backend.
        One of the major differences between shelve and couchshelve
        is that couchshelve is safe to use with multiple simultaneous
        readers and writers.
    -   Couchquery does not yet support Python 3 (in 2013).
-   [couchdbkit](http://couchdbkit.org/) (Apache License 2)
    a python client for Couchdb which allow to reflect python objects
    in the database. provides you a full featured and easy client to
    access and manage CouchDB.  It allows you to manage a CouchDB
    server, databases, doc managements and view access.  Not yet ready
    for Python 3 in 2013.
-   You can also use the
    [CouchDB HTTP Document API
    ](http://wiki.apache.org/couchdb/HTTP_Document_API)
    to use CouchDB in a RESTful way.
    -   [Getting started with  couchDB and Python
        ](  http://wiki.apache.org/couchdb/Getting_started_with_Python)
        gives an introductory example.
    -   Frédéric Laurent in
        [Couchdb : Accès en HTTP avec Python
        ](http://opikanoba.org/python/couchdb)
        gives a french tutorial. The source code is
        [available on GitHub
        ](https://github.com/flrt/couchette/blob/master/couchette.py).
-   [Erica (GitHub)](https://github.com/benoitc/erica)
    previously _couchapp_ is an application written in erlang and gcc
    that gives you JavaScript and HTML5 applications served directly
    from CouchDB. You can interract with Erica with curl, node.js or
    Python.
   -   [Erica/Couchapp site](http://couchapp.org/).

## Other Non-Relational Databases
-   [Brain](http://pypi.python.org/pypi/brain/)
    is a Document Database wrapper for relational databases.
    It support python 2 or 3.
-   [GitPython ](https://pypi.python.org/pypi/GitPython/) (BSD License)
    is a python library used to interact with git repositories. It
    provides abstractions of git objects for easy access of repository data.
    It uses [Gitdb](https://pypi.python.org/pypi/gitdb/)
    for the access to git object database.
-   [MongoDb](http://www.mongodb.org/) (GNU AGPL v3.0.) it has a
    [PyMongo Python Driver
    ](https://github.com/mongodb/mongo-python-driver) for python 2.x.
    [PyMongo API Documentation](http://api.mongodb.org/python/current/)
    -   [sleepy.mongoose
        ](https://github.com/kchodorow/sleepy.mongoose/wiki/)
        uses PyMongo to provide a RESTful interface too MongoDB
-   [w:Redis] (BSD License) is an in-memory, key-value data store
    with optional persistence.
    [redis-py](https://github.com/andymccurdy/redis-py)
    is the Python interface to the Redis key-value store.
-   [Riak](http://basho.com) (Apache License 2.0) is a key/value store with
    [Python Bindings](http://basho.github.com/riak-python-client/)
    the
    [python client is hosted on GitHub](https://github.com/basho/riak-python-client)
-   [shelve](http://docs.python.org/3/library/shelve.html)
    ([py2k](http://docs.python.org/2/library/shelve.html))
    Python object persistence,
    -   [PyMOTW: shelve](https://pymotw.com/3/shelve/index.html)
-   [Shove](http://pypi.python.org/pypi/shove/) (BSD License) is an
    object storage frontend that supports dictionary-style access,
    object serialization and compression.
    -    Shove supports multiple storage (S3, Cassandra, DBM, Durus,
         Filesystem, Firebird, Memory, MySQL,Oracle, PostgreSQL,
         Redis, SQLite, ZODB, ...)
    -    and also caching backends (Filesystem, Firebird, MySQL,
         Oracle, PostgreSQL, SQLite, memcache ...)
    -    [Introduction to shove in EvilChuck blog
        ](http://www.evilchuck.com/2008/02/tell-python-to-shove-it.html)
-   [w:Zope Object Database] is an object-oriented database for
    storing Python objects.  It is part of [w:Zope] but an also be
    used independently.
    -   [ZODB Documentation](http://www.zodb.org/)
    -   [SQLite dictionnary-like object for LARGE datasets Recipe
        ](http://sebsauvage.net/python/snyppets/index.html#dbdict) pa Seb Sauvage.

## Object Relational Mappers {#orm}
-   [Python Wiki: Higher level database programming
    ](http://wiki.python.org/moin/HigherLevelDatabaseProgramming)
    gives a list of Objects Relational Models and SQl Wrappers.
-   [SqlAlchemy](http://www.sqlalchemy.org/ "sqlalchemy.org") (MIT
    License) is a Python SQL toolkit and Object Relational Mapper.
    -   The [SQLAlchemy Documentation](http://www.sqlalchemy.org/docs/)
        includes a [Tutorial
        ](http://www.sqlalchemy.org/docs/05/ormtutorial.html)
    -   [SQLAlchemy tutorial
        ](http://mapfish.org/doc/tutorials/sqlalchemy.html)
        based on the Pylons Book
    -   [SqlAlchemy-Migrate
        ](https://github.com/stackforge/sqlalchemy-migrate)
        (MIT License) is a tool to assist the user in importing an existing
        database into *SqlAlchemy*.
-   [SqlObject](http://sqlobject.org/) (LGPL) Object
    Relational Manager for providing an object interface to your
    database, with tables as classes, rows as instances, and columns as
    attributes.It is the object of the article
-   [Storm](https://storm.canonical.com/ "storm.canonical.com") (LGPL)
    is an (ORM) for Python developed at Canonical, with a lightweight
    api, and designed to work both with thin relational databases, such
    as SQLite, and big iron systems like PostgreSQL and MySQL.


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
