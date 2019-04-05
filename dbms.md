---
title: DBMS
---

{{% toc /%}}

For the python interfaces look at the section
{{< iref "python_dbms" "Python Database Programming" >}}.

# SQL

-   {{< wp "SQL"  "Wikipedia: SQL" >}}, {{< wp "Comparison of relational database management systems" >}},
    {{< wp "Comparison of object-relational database management systems" >}}
-   [SQL 92](http://www.contrib.andrew.cmu.edu/~shadow/sql/sql1992.txt) Second Informal Review Draft

## SQL Tutorials

-   [WikiBook: SQL](http://en.wikipedia.org/wiki/Book:SQL)
-   [SQL Tutorial at 1keydata.com](http://www.1keydata.com/sql/sql.html)
-   [SQL92 tutorial](http://www.firstsql.com/tutor.htm)
    from FirstSQL
-   [SQL Tutorial from BayCon Group](http://www.baycongroup.com/tocsql.htm)
-   [SQL Tutorial at tizag.com](http://www.tizag.com/sqlTutorial/)
-   [Sql Zoo](http://sqlzoo.net/) Tutorial, examples,
    assignements ... from the School of Computing of Napier University.
-   [MySQL Tutorial at webdevelopersnotes.com
    ](http://www.webdevelopersnotes.com/tutorials/sql/index.php3)
-   [SQL Fundamentals
    ](http://databases.about.com/od/sql/a/sqlfundamentals.htm)
    by Mike Chapple
-   [w3school SQL index](http://www.w3schools.com/sql/default.asp)
-   [sqlfiddle](http://sqlfiddle.com/)
    allow to execute and test a sql schema with MS sql server, MySql,
     Oracle, SQlite, PostgreSQL.


## SQL Formatters {#sql_formatters}

### open source with online frontend
-   [SQLFormat](http://sqlformat.org/)
    is a free online formatter for SQL. It is powered by the
    [sqlparse](https://github.com/andialbrecht/sqlparse) python
    module (BSD License).
-   [pgFormatter](http://sqlformat.darold.net/)
    is a free online PostgreSQL SQL syntax beautifier. The perl
    source code is available in the
    [pgformatter GitHub Repository](https://github.com/darold/pgFormatter)
    (PostgreSQL Licence)

### Private software with free online frontend
-   [Web Toolkit Online SQL Formatter
    ](http://www.webtoolkitonline.com/sql-formatter.html)
    [Web Toolkit Online](http://www.webtoolkitonline.com/) offers many
    online toolkits, like this SQL Formatter, a Json Formatter, other
    formatters, minifiers, ...
-   [T-SQL Tidy](http://www.tsqltidy.com/) free online SQL formatter.
-   [Instant SQL Formatter](http://www.dpriver.com/pp/sqlformat.htm)
    free online service from a proprietary software. (configurable,
    many dialects)
-   [format SQL](http://format-sql.com/) free online formatter from
    the Red Gate proprietary software.
-   [Poor SQL](http://poorsql.com/) online SQL formatter
    (configurable).
-   [Pat's Online SQL Formatter
    ](http://patsformatters.appspot.com/SqlFormatter.html)

### opensource, no online frontend
-   [Free SQL Formatter](http://sourceforge.net/projects/fsqlf/) (LGPL)
    is a C++ tool that adds linebreaks and indentation to sql source
    code.
    [GitHub: Free SQL Formatter](https://github.com/dnsmkl/fsqlf) (LGPL)
-   [SqlFormatter](http://jdorn.github.io/sql-formatter/)
    is a PHP class for formatting and highlighting SQL statements.
    [GitHub: SqlFormatter](https://github.com/jdorn/sql-formatter).

# MySQL{#mysql}

{{< wp "MySQL" >}} (GPL) was a product of the firm _MySQL AB_, it as been
bought by _Sun_; then by _Oracle_.
So we cannot be too optimistic about the GPL future of MySql.

Since the purchase of MySQL by Oracle, the founder of the original
MySQL lead a true community-driven replacement for MySQL. __MariaDB__
is touted as a drop-in replacement for MySQL on a verion-by-version
basis.

-   [MariaDB fondation](https://mariadb.org/en/) you can find a repository for all main distributions in
    [mariadb repositories](https://downloads.mariadb.org/mariadb/repositories/)
-   [MariaDB Documentation](https://mariadb.com/kb/en/mariadb-documentation/):
    [MariaDB versus MySQL - Compatibility](https://mariadb.com/kb/en/mariadb-vs-mysql-compatibility/)
-   [MySql](http://www.mysql.com/ "Mysql.com") (GPL)
-   [Mysql 5.7  Manual](http://dev.mysql.com/doc/refman/5.7/en/).
    (Free but not GPL)
-   [tutorial (5.7)](http://dev.mysql.com/doc/refman/5.7/en/tutorial.html),
    [FAQ 5.7](http://dev.mysql.com/doc/refman/5.7/en/faqs.html),
    [server administration  (5.7)](http://dev.mysql.com/doc/refman/5.7/en/server-administration.html),
    [Language Structure (5.7)](http://dev.mysql.com/doc/refman/5.7/en/language-structure.html)
    and [Sql Syntax (5.7)](http://dev.mysql.com/doc/refman/5.7/en/sql-syntax.html).
-   There are a lot of connectors to allow use of MySql thru legacy api
    like ODBC,JDBC, and also APIs for most programming languages
    (python, perl, C, C++, PHP ...) they are described in the
    [Connectors and APIs page of MySql manual (5.6)](http://dev.mysql.com/doc/refman/5.6/en/connectors-apis.html "mysql.com refman/5.6 connectors-apis.html").

# MySQL Tutorial


# PostgreSQL
[PostgreSQL](http://www.postgresql.org/) ([PostgreSQL Licence
    ](http://www.postgresql.org/about/licence/) BSD like)
-   Wikipedia: {{< wp "PostgreSQL" >}}
-   [PostgeSQL Manual](http://www.postgresql.org/docs/devel/static/).
-   [MySQL vs PostgreSQL](http://www.wikivs.com/wiki/MySQL_vs_PostgreSQL)
-   [ArchWiki: PostgreSQL](https://wiki.archlinux.org/index.php/PostgreSQL)

## PostgreSQL Database Design
-   [Druid Database Manager](http://druid.sourceforge.net/) (GPL)
    is a java GUI tool for database build and management.
    You can add/change/delete DB objects (tables, fields, etc).
    Druid generates: SQL scripts, docs in XHTML, PDF, DocBook, etc;
    code in C, C++ & Java Beans.
-   [Glom](http://www.glom.org/) (GPL) is a database
    design framework that uses the PostgreSQL database backend.
-   [pgModeler](http://www.pgmodeler.com.br/) (GPL)
    is a C tool for modeling databases that combines entity-relationship
    diagrams with specific PostgreSQL features.<br />
    [pgModeler Wiki](http://www.pgmodeler.com.br/wiki/),
    [GitHub: pgModeler](https://github.com/pgmodeler/pgmodeler).
-   [PostgreSQL Autodoc](http://autodoc.projects.pgfoundry.org/)
    is an utility which will generates HTML, Dot, Dia and DocBook
    database description from PostgreSQL system tables.
    It is in the debian package *postgresql-autodoc*.

## PostgreSQL Administration
-   [PostgreSQL Wiki: Category Administration
    ](http://wiki.postgresql.org/wiki/Database_Administration_and_Maintenance).
-   [PostgreSQL Wiki:  Converting from other Databases to PostgreSQL
    ](http://wiki.postgresql.org/wiki/Converting_from_other_Databases_to_PostgreSQL)
-   [pgloader](https://github.com/dimitri/pgloader) ([PostgreSQL Licence
    ](http://www.postgresql.org/about/licence/) BSD like)
    by Dimitri Fontaine is a Common Lisp program that uses the COPY
    command to import data from flat files and insert it into a
    database table.  A configuration file contain sections, which each
    defines how to load a table.  CSV and text format are
    supported. CVS import with -T option can import MySQL dumps.<br />
    You can find
    [pgloader examples in the Dimitri's blog
    ](http://tapoueh.org/tags/pgloader).<br />
    _pgloader_ is in debian.
-   [phpPgAdmin](http://phppgadmin.sourceforge.net/) (GPL)
    is a web-based administration tool for PostgreSQL.
    [ArchWiki: PhpPgAdmin](https://wiki.archlinux.org/index.php/PhpPgAdmin)
-   [pgAdmin](http://www.pgadmin.org/) ([PostgreSQL Licence
    ](http://www.postgresql.org/about/licence/) BSD like)
    is an administration and development platform for PostgreSQL. It
    is packaged in all major distributions.
    [pgAdmin III latest documentation
    ](http://www.pgadmin.org/docs/dev/index.html).
-   [PostgreSQL Studio](http://www.postgresqlstudio.org/)
     ([ Open Source Consulting Group  License
     ](https://bitbucket.org/openscg/pgstudio/src/7c349d49281a7d67c41f98b20bd77edc77ddec4b/LICENSE?at=master))
     allows to perform PostgreSQL database development tasks from a web-based console.
     [PostgreSQL Studio git repository](https://bitbucket.org/openscg/pgstudio/)
-   [Slony-I](http://slony.info/) ([PostgreSQL Licence
    ](http://www.postgresql.org/about/licence/) BSD like)
    is a "master to multiple slaves" replication system for
    PostgreSQL. [PostgreSQL Wiki: Slony](http://wiki.postgresql.org/wiki/Slony).
    Slony-I is packaged in Debian.

## PostgreSQL configuration
-   [PostgeSQL Manual](http://www.postgresql.org/docs/devel/static/):
    [Server Configuration](http://www.postgresql.org/docs/devel/static/config-setting.html)
-   [PostgreSQL Wiki](http://wiki.postgresql.org/wiki/):
    [Tuning Your PostgreSQL Server](http://wiki.postgresql.org/wiki/Tuning_Your_PostgreSQL_Server)
-   [Debian Wiki: https://wiki.debian.org/PostgreSql](https://wiki.debian.org/PostgreSql)
-   [PostgreSQL Database Server Configuration in Debian
    ](http://www.debianhelp.co.uk/postgresql.htm)
-   [PGCon (PostgreSQL Conference)](http://www.pgcon.org/):
    [PGCon 2008 - GUCs: A Three Hour Tour
    ](http://www.pgcon.org/2008/schedule/events/104.en.html)
    [commented table of configuration options
     (pdf) ](http://www.pgcon.org/2008/schedule/attachments/45_guc_tutorial.pdf)
    and [OpenOffice (odp)
     ](http://www.pgcon.org/2008/schedule/attachments/47_guc_tutorial.odp).


## PostgreSQL Tutorials
-   [PostgreSQL Wiki](http://wiki.postgresql.org/wiki/):
    [list of PostgreSQL Tutorials
    ](http://wiki.postgresql.org/wiki/PostgreSQL_Tutorials).
-   [postgresqltutorial.com: PostgreSQL Tutorial
    ](http://www.postgresqltutorial.com/)
-  [Postgres Guide](http://www.postgresguide.com/)



# No SQL databases
-   Wikipedia: {{< wp "NOSQL" >}}


-   [Cassandra Home at apache.org](http://cassandra.apache.org/),
    [Cassandra Wiki](http://wiki.apache.org/cassandra/),
    [Cassandra articles and presentations
    ](http://wiki.apache.org/cassandra/ArticlesAndPresentations).
-   [Hamsterdb](http://hamsterdb.com/) (GPL)
    is a lightweight embedded "NoSQL" key-value store.
    [Hamsterdb git repository](https://github.com/cruppstahl/hamsterdb).
-   [memcached](http://www.danga.com/memcached/) a
    high-performance, distributed memory object caching system,
    intended for use in speeding up dynamic web applications by
    alleviating database load.
-   {{< wp "Redis" >}} (BSD License) is a networked, in-memory, key-value data
    store with optional durability. It is written in ANSI C.
     - [Redis Home](http://redis.io)
     - [The Little Redis Book](http://openmymind.net/redis.pdf)
       an open pdf book by Karl Seguin.
-   {{< wp "Riak" >}} (Apache License 2.0)
     is a key/value store following the principles of
     {{< wp "Dynamo_(storage_system)"  "Amazon's Dynamo" >}}.
     - [Riak Home](http://basho.com/products/)

## CouchDB {#couchdb}

-   {{< wp "Document-oriented database" >}}s are members of the {{< wp "NoSQL" >}} family.
-   Wikipedia: {{< wp "CouchDB" >}}  ({{< wp "Apache License" >}} 2.0) is a
    document-oriented, Non-Relational DataBase Management Server.
    CouchDB is written in Erlang language.
    -    The Wikipedia page contains
         {{< wp "CouchDB#Examples"  "an example of use of HTTP API through curl" >}}.
-   [CouchDB Home (Apache fondation)](http://couchdb.apache.org/),
    [CouchDb Wiki](http://wiki.apache.org/couchdb/).
-   [CouchDB: The Definitive Guide](http://books.couchdb.org/relax/)
    a free O’Reilly Media book.
-   [DesktopCouch documentation
    ](http://www.freedesktop.org/wiki/Specifications/desktopcouch/Documentation),
    [DesktopCouch specification
        ](http://www.freedesktop.org/wiki/Specifications/desktopcouch)
-   [Stuart Langridge blog](http://www.kryogenix.org/):
    [using CouchDB to store contacts
    ](http://www.kryogenix.org/days/2009/06/19/using-couchdb-to-store-contacts)
-   [Desktop CouchDB in Launchpad](https://launchpad.net/desktopcouch)
-   [ubuntu fr: DesktopCouch](http://doc.ubuntu-fr.org/desktopcouch)

## MongoDB
-   {{< wp "MongoDB" >}} Cloud-scale document oriented database,
    [MongoDB Home](http://www.mongodb.org/) ({{< wp "Affero General Public License"  "GNU AGPL" >}}).
-   [sleepy.mongoose](https://github.com/kchodorow/sleepy.mongoose/wiki/)
     provide a RESTful interface too MongoDB.
-   [mongodb-rest](https://github.com/tdegrunt/mongodb-rest)
    is a REST server for MongoDB using
    [Node](http://nodejs.org/), using the native node.js MongoDB driver.
     See also [MongoDB HTTP interface](http://www.mongodb.org/display/DOCS/Http+Interface)

## Berkeley DB
-   [Gnu gdbm](http://directory.fsf.org/wiki/Gdbm)
    (GPL) : [gdbm(3)](http://man.cx/gdbm(3)) is an
    implementation of a unix
    [dbm(3)](http://man.cx/dbm(3)) and
    [ndbm(3)](http://man.cx/ndbm(3)). It provides
    an associative array with strings as keys.
-   [Berkeley DB](http://www.oracle.com/database/berkeley-db/)
    from Berkeley university previously maintained by
    *Sleepycat software* is now found in *oracle.com* pages. It has now
    a double license free open source(berkeley modified, for details
    visit oracle site) and commercial.
    The Berkeley Database is an embedded database system. Its access
    methods include B+tree, Extended Linear Hashing, fixed and
    variable-length records, and Persistent Queues. Berkeley DB
    provides full transactional support, database recovery, online
    backups, and separate access to locking, logging and shared memory

# SQLite
-   [SQLite](http://www.sqlite.org/) (public domain)
    - [SQLite FAQ](http://www.sqlite.org/faq.html)
    - [SQL As Understood By SQLite](http://www.sqlite.org/lang.html)

## SQLite tutorials
-   [SQLite Tutorial I
    ](http://linuxgazette.net/109/chirico1.html) and
    [SQLite Tutorial I|
    ](http://souptonuts.sourceforge.net/) by Mike Chirico.

## SQLite administration
-   [phpLiteAdmin](https://bitbucket.org/phpliteadmin/public/) (GPL)
     is a web-based SQLite database admin tool written in PHP._active in 2015_.
-   [SQLite Database Browser]( http://sqlitebrowser.sourceforge.net/) (public domain)
    is a visual tool in QT, used to create, design and edit SQLite databases.
-   [SQLiteManager](http://www.sqlitemanager.org/) (GPL)
    PHP web tool to manage SQLite databases. SQLiteManager is now
    managed by a french company, it is still GPL but take care to have
    a working adds blocker before visiting their site.
-   [sqlite-manager firefox plugin](https://code.google.com/p/sqlite-manager/)
    ([downloads](https://addons.mozilla.org/fr/firefox/addon/sqlite-manager/))
     (Mozilla Public License) manage any SQLite database on your computer.
-   [TkSQLite](http://reddog.s35.xrea.com/wiki/TkSQLite.html)
    (BSD license) is a GUI database manager for SQLite implemented by
    Tcl/Tk. It can manage SQLite version2.8 and SQLite version3.x. database.

## SQLite bindings
-   [pysqlite](https://pypi.python.org/pypi/pysqlite) (MIT License)
    is a sqlite binding for Python that complies to the Database
    API 2.0. It is integrated into python under the module name of
    [sqlite3](http://docs.python.org/py3k/library/sqlite3.html)

## SQLite conversion
-   [ sqlite - Converter Tools
    ](http://www.sqlite.org/cvstrac/wiki?p=ConverterTools)
-   [SQL-Translator](http://search.cpan.org/dist/SQL-Translator/) is a
    perl package.
-   To translate SQLite to MySQL ou find on stackoverflow a
    [perl conversion script](http://stackoverflow.com/a/1070463/965798)
    and a
    [pythonconversion script](http://stackoverflow.com/a/3675869/965798)
-   [Stackoverflow: script to convert mysql dump sql file into format
    that can be imported into sqlite3 db
    ](http://stackoverflow.com/questions/489277)
-   The main differences between MySQL an SQLite syntax are:
    -    MySQL don't use BEGIN TRANSACTION, COMMIT, CREATE UNIQUE
         INDEX, sqlite_sequence
    -    SQLlite uses CREATE TABLE/INSERT INTO "table_name" and MySQL
         uses CREATE TABLE/INSERT INTO table_name
    -    MySQL doesn't use quotes inside the schema definition
    -    MySQL uses single quotes for strings inside the INSERT INTO
         clauses SQLlite and MySQL have different ways of escaping
         strings inside INSERT INTO clauses.
    -    SQLite uses 't' and 'f' for booleans, MySQL uses 1 and 0
    -    SQlite uses AUTOINCREMENT, MySQL uses AUTO_INCREMENT

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
