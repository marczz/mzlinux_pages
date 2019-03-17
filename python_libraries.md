<!--
.. description:
.. date: 2015-05-03
.. slug: python_libraries
.. tags:
.. link:
.. book: mzlinux
.. title: Python Libraries
-->

[TOC]

-----

# Modules {#modules}
Subset of the
[Python full module index](http://docs.python.org/3/py-modindex.html)
([py2k](http://docs.python.org/2/modindex.html)),
The modules not included in the standard library are in the section:
[Libraries](#libraries "internal reference").

Some modules are commented in the
[Python Module of the Week - PyMOTW](https://pymotw.com/3/) from
Doug Hellmann.

Frederik Lunch in his
[eff-bot guide to The Standard Python Library
](http://www.effbot.org/librarybook/) also
provides brief descriptions and sample scripts for all standard modules
in the Python 2.0 library, while being outdated, it can still be useful.

The source code of python modules is found in the
[cpython mercurial repository](http://hg.python.org/cpython).


## Data Model {#base_types_modules}
-   [Built-in Types](http://docs.python.org/3/library/stdtypes.html)
    _not strictly a module_
    contains the
    [Mapping Types - dict
    ](http://docs.python.org/3/library/stdtypes.html#mapping-types-dict),
    the
    [Sequence Types
    ](http://docs.python.org/3/library/stdtypes.html#sequence-types-str-bytes-bytearray-list-tuple-range)
    and
    [String Methods
    ](http://docs.python.org/3/library/stdtypes.html#string-methods)
    but the format used for
    [str.format()
    ](http://docs.python.org/3/library/stdtypes.html#str.format)
    is in
    [string formatting
    ](http://docs.python.org/3/library/string.html#string-formatting)
    is in the
    [String Module](http://docs.python.org/3/library/string.html)
-   [Built-in Functions
    ](http://docs.python.org/3/library/functions.html) -
    [py2k](http://docs.python.org/2/library/functions.html) -
    _not strictly a module_.
-    [abstract base classes](http://docs.python.org/3/library/abc.html),
    [PyMotw: abstract base classes](http://pymotw.com/2/abc/)
-   [Collections](http://docs.python.org/3/library/collections.html) -
    [py2k](http://docs.python.org/2/library/collections.html) -
    are
    _abstract base classes_
    that extend the
    [Builtin Sequence Types
    ](http://docs.python.org/3/library/stdtypes.html#sequence-types-str-bytes-bytearray-list-tuple-range)
    and
    [Builtin Mapping Types
    ](http://docs.python.org/3/library/stdtypes.html#mapping-types-dict).
    It helps the creation and use of user defined collections. <br />
    [PyMOTW: Collections](https://pymotw.com/3/collections/index.html)
     -   [namedtuple
         ](http://docs.python.org/3/library/collections.html#collections.namedtuple)
         is used to parse CVS files by Michele Simionato in
         [Managing Records in Python
         ](http://www.artima.com/weblogs/viewpost.jsp?thread=236637).
-   [imp](http://docs.python.org/3/library/imp.html)
    the import internals provides the functions:
    `reload`, find_module`, `load_module`, `acquire_lock`, `release_lock`.
    [PyMOTW imp](https://pymotw.com/3/imp/index.html).
-   [functools](http://docs.python.org/3/library/functools.html) -
    [py2k](http://docs.python.org/3/library/functools.html) -
    <a name="functools"></a>decorators for second-order programming,
    mainly the [partials decorator
    ](http://docs.python.org/3/library/functools.html#functools.partial)
    that allow to do a partial binding on arguments of a function ie a
    [w:partial application]
    *see also [w:currying] and
    [w:Closure_(computer_science)|closure]*.
    Examples of use are in
    [PyMOTW: functools](https://pymotw.com/3/functools/index.html).
    <br />
    The [Functional Programming HOWTO
    ](http://docs.python.org/3/howto/functional.html)
    has a [functool section
    ](http://docs.python.org/3/howto/functional.html#the-functools-module).
-   [inspect](http://docs.python.org/3/library/inspect.html)
    functions for introspecting on live objects and their source code.
    [PyMOTW: inspect](https://pymotw.com/3/inspect/index.html)
-   [itertool](http://docs.python.org/3/library/itertools.html) -
    [py2k](http://docs.python.org/3/library/itertools.html) -
    iterator building blocks inspired by constructs from APL, Haskell, and SML.
    [PyMOTW: itertools](https://pymotw.com/3/itertools/index.html).<br />
    The [Functional Programming HOWTO
    ](http://docs.python.org/3/howto/functional.html)
    has an [itertool section
    ](http://docs.python.org/3/howto/functional.html#the-itertools-module).
-   <a name="python_re"></a>
    [re](http://docs.python.org/3/library/re.html)
    [py2k](http://docs.python.org/2/library/re.html)
    Regular expression operations _string or bytearrays_.
    -   [Regular Expression HOWTO (py3k)
        ](http://docs.python.org/3/howto/regex.html)
         by A.M. Kuchling *(gives also pcre syntax)*
    -   [PyMOTW: re – Regular Expressions](https://pymotw.com/3/re/index.html)
    -   You can test online your regular expressions with one of:
        [pythonregex](http://python-regex.com/),
        [pythex](http://pythex.org/),
        [regex101](https://regex101.com/),
        [debuggex](https://www.debuggex.com/),
    -   For an off-line test instal the
        [Kodos](http://kodos.sourceforge.net/)
        GUI , or the downloadable Ajax tool
        [retest](http://cthedot.de/retest/) ( Creative Commons
        License) that you can use on any machine with python and an
        ajax enabled browser like firefox, chrome, opera (vivaldi),
        safari,....
    -   See also the [pcre references
        ](/node/programming_languages#pcre "internal reference")

## Development tools
-   The <a name="distutils"></a>
    [module distutils](http://docs.python.org/3/library/distutils.html) -
    [py2k](http://docs.python.org/2/library/distutils.html) -
    is described in
    [Distributing Python Modules](http://docs.python.org/3/distutils/)
    and [Installing Python Modules](http://docs.python.org/3/install/)
     see also [Libraries: packaging](#packaging "internal reference")
     for alternatives and enhancements of _distutils_.
-   [doctest](http://docs.python.org/3/library/doctest.html) -
    [py2k](http://docs.python.org/2/library/doctest.html) -
    [PyMOTW page](https://pymotw.com/3/doctest/index.html)
    allows the generation of tests based on output from the
    standard Python interpreter shell, cut and pasted into docstrings.
    It searches for pieces of text that look like interactive Python
    sessions, and then executes those sessions to verify that they work
    exactly as shown.<br />
    [Doctest2](http://packages.python.org/doctest2/) extend _doctest_.
-   [unittest](http://docs.python.org/3/library/unittest.html) -
    [py2k](http://docs.python.org/library/unittest.html) -
    [PyMOTW page](https://pymotw.com/3/unittest/index.html)
    is a unit testing framework.The new
    [python 3k unittest
    ](http://docs.python.org/3/library/unittest.html)
    has important improvements that are backported in the
    [unitest2 library](http://pypi.python.org/pypi/unittest2).
    The enhancements are described in the article
    [New features in unittest
    ](http://www.voidspace.org.uk/python/articles/unittest2.shtml)
-   <a name="unittest.mock"></a>
    [unittest.mock
    ](http://docs.python.org/3/library/unittest.mock.html)
    _new in version3.3_ is a mock object library. It allows you to
    replace parts of your system under test with mock objects and make
    assertions about how they have been used. _See also the
    [mock libraries section](#mock_objects "internal reference")
    for alternatives.
-   <a name="venv_module"></a>
    [venv](http://docs.python.org/3/library/venv.html) is
    a port to standard library of
    [virtualenv](#virtualenv "internal reference"), it is available
    since python 3.3 and is used with the `python -m venv` or with
    `pyvenv` script.<br />
-   <a name="venv_module"></a>
    [venv](http://docs.python.org/3/library/venv.html) -
    [PyMOTW Page](https://pymotw.com/3/venv/)
    is
    a port to standard library of
    [virtualenv](#virtualenv "internal reference"), it is available
    since python 3.3 and is used with  `python -m venv`.<br />
    This is further developped in
    [Python Packaging User Guide: Creating and using virtual
    environments
    ](https://packaging.python.org/tutorials/installing-packages/#creating-virtual-environments).

## Interfaces {#interface_modules}
-   [curses](http://docs.python.org/3/library/curses.html) -
    [py2k](http://docs.python.org/2/library/curses.html) -
    interface to the curses library.
    -   A tutorial: [Curses programming
        ](http://www.ibm.com/developerworks/linux/library/l-python6.html)
        by David Merz.
    -   An How-To: [Curses Programming with Python
        ](http://docs.python.org/howto/curses.html)
        by A.M. Kuchling and Eric S. Raymond.
    -   Not specific to python the introduction to Ncurses:
        [Writing Programs with NCURSES
        ](http://invisible-island.net/ncurses/ncurses-intro.html)
        by Eric S. Raymond, Zeyd M. Ben-Halim, Thomas Dickey.
-   [tkinter](http://docs.python.org/3/library/tkinter.html) -
    [py2k](http://docs.python.org/2/library/tkinter.html) -
    Python interface to the Tk GUI toolkit. *See at the beginning of
    the previous page for introductory materials.*
    -   [introduction to TkInter](http://effbot.org/tkinterbook/)
        by Fredrik Lundh in
        [zone.effbot.org](http://effbot.org/zone/index.htm).
-   [PyGtk](/node/pygtk "internal link") Python wrapper for the GTK library

## Operating System services {#os_modules}
-   [argparse](http://docs.python.org/3/library/argparse.html)
    command-line parsing library,
    [PyMOTW: argparse](https://pymotw.com/3/argparse/).
    Since python 2.7 replaces the deprecated
    [optparse](http://docs.python.org/library/optparse.html) .
-   [logging](http://docs.python.org/3/library/logging.html)
     standard API for reporting errors and status information
     from applications and libraries.
     -   [PyMOTW: logging](https://pymotw.com/3/logging/)
     -   [Logging: Basic Tutorial
         ](http://docs.python.org/3/howto/logging.html#logging-basic-tutorial)
     -   [Logging: Advanced Tutorial
         ](http://docs.python.org/3/howto/logging.html#logging-advanced-tutorial)
     -   [Logging Cookbook
         ](http://docs.python.org/3/howto/logging-cookbook.html#logging-cookbook)
-   [os](http://docs.python.org/3/library/os.html) -
    [py2k](http://docs.python.org/library/os.html) -
    Operating system interfaces. Note that legacy functions to manage processes like
    `system()`, `popen()`, `popen2()`, `popen3()`
    [must be replaced by the subprocess module
    ](http://docs.python.org/3/library/subprocess.html#subprocess-replacements).
-   [os.path](http://docs.python.org/3/library/os.path.html) -
     [py2k](http://docs.python.org/library/os.path.html) -
    Operations on pathnames.
-   [print](http://docs.python.org/3/library/pprint.html) -
    [py2k](http://docs.python.org/library/pprint.html) -
     Data pretty printer.
-   [io](http://docs.python.org/3/library/stringio.html)
    tools for working with streams in py3k includes  the high-level
    IO class
    [io.BufferedIOBase
    ](http://docs.python.org/3/library/io.html#io.BufferedIOBase)
    for binary streams and
    [io.TextIOBase
    ](http://docs.python.org/3/library/io.html#io.TextIOBase)
    for text streams. <br />
    There are two in memory buffer classes that provide a file-like api:
    [io..BytesIO](http://docs.python.org/3/library/io.html#io.BytesIO)
    for in-memory binary streams and
    [io.StringIO](http://docs.python.org/3/library/io.html#io.StringIO) -
    [py2k: StringIO](http://docs.python.org/2/library/stringio.html) -
    for in-memory binary text streams.
    [PyMOTW: StringIO](https://pymotw.com/3/StringIO),
    [effbot: StringIO](http://effbot.org/librarybook/stringio.htm)
-   [traceback](http://docs.python.org/3/library/traceback.html)
     provides a standard interface to extract, format and print stack
     traces of Python programs.

## Databases and Object Relational Mappers

They are covered in the [databases programming section
](/node/python_dbms "internal reference").

## Processes {#process_modules}
-   [subprocess](http://docs.python.org/3/library/subprocess.html) -
    [py2k](http://docs.python.org/2/library/subprocess.html) -
    spawn new processes, connect to their input/output/error pipes,
    and obtain their return codes.
    The main class is
    [subprocess.Popen
    ](http://docs.python.org/3/library/subprocess.html#subprocess.Popen)
    [PyMOTW: subprocess](https://pymotw.com/3/subprocess/).
-   [multiprocessing
    ](http://docs.python.org/3/library/multiprocessing.html)
    offers both local and remote concurrency.
    It's API is similar to the _threading module_ one.<br />
    [PyMOTW multiprocesing](https://pymotw.com/3/multiprocessing/)
-   [threading](http://docs.python.org/3/library/threading.html)
    higher-level threading interfaces.
    [PyMOTW threading](https://pymotw.com/3/threading/)
-   [queue](http://docs.python.org/3/library/queue.html),
    [PyMOTW queue](https://pymotw.com/3/Queue/)
    module implements multi-producer, multi-consumer queues.
    It is especially useful in threaded programming.
-   [pipe](http://docs.python.org/3/library/pipes.html) -
    [py2k](http://docs.python.org/2/library/pipes.html) -
    A class to create  Unix command pipelines.
    [PyMOTW:pipe](https://pymotw.com/3/pipes/)

## Network {#network_modules}

### Low level
-   [ipaddress](http://docs.python.org/3/library/ipaddress.html )
    <a name="ipaddress_module"></a>
    is an IPv4/IPv6 manipulation library, it  provides a mechanisms
    to access to properties of an ip address, for defining
    and inspecting IP network definitions with a mask and a network address,
    and dealing with interfaces. This module is new in python 3.3.
-   [socket](http://docs.python.org/3/library/socket.html)
    Low-level networking interface.
-   [SocketServer](http://docs.python.org/3/library/socketserver.html)
    A framework for network servers.

### High Level
See also the [xCGI stuff](/node/python_web#wsgi "internal reference") and
[Web programming](/node/python_web "internal reference").

-   [email](http://docs.python.org/3/library/email.html) Parsing,
    manipulating, and generating email messages, including MIME
    documents.
-   [imaplib](http://docs.python.org/3/library/imaplib.html) -
    [py2k](http://docs.python.org/2/library/imaplib.html) -
    IMAP4 protocol client.
    You find examples in [PyMOTW: imaplib](https://pymotw.com/3/imaplib/)
-   [smtplib](http://docs.python.org/3/library/smtplib.html)
    SMTP client session objects.

#### ssl and python
-   [TLS Lite](https://github.com/trevp/tlslite)
    is an open source python library that implements SSL and TLS. TLS
    Lite supports RSA and SRP ciphersuites. TLS Lite is pure python, however it
    can use other libraries for faster crypto operations like OpenSSL,
    cryptlib, pycrypto, and GMPY.<br/>
    TLS Lite supports non-traditional authentication methods such
    as SRP, shared keys, and cryptoIDs in addition to X.509
    certificates.
-   [PythonNSS](http://fedoraproject.org/wiki/Features/PythonNSS)
    is a  Python bindings module for NSS/NSPR allowing Python
    programs to utilize the NSS cryptographic libraries
    for SSL/TLS and PKI certificate management.
-   [PyCrypto](https://www.dlitz.net/software/pycrypto/)
    is a collection of cryptographic algorithms and protocols,
    implemented for use from Python.

## Serializing {#serializing_modules}
See also [Python Libraries - serializing](#serializing_libs "internal reference")

-   Doug Hellmann PyMOTW[Data Persistence and Exchange
    ](https://pymotw.com/3/persistence.html)
    is a panorama of the various ways to achieve persistence in python.
-   [json](http://docs.python.org/3/library/json.html)  -
    [py2k](http://docs.python.org/library/json.html) -
    Encode and decode the
    [JSON](/node/107/#json "internal link") format..
    [PyMOTW: json](https://pymotw.com/3/json/)</br >
    You can use the included script `json.mtool` to validate and pretty-print a
    json string. _jsonpickle_ (see
    [Python Libraries - serializing](#serializing_libs "internal
    reference"))
    extend the standard Python module _json_.
-   [pickle](http://docs.python.org/3/library/pickle.html) -
    [py2k](http://docs.python.org/3/library/pickle.html) -
    Convert Python objects to streams of bytes and back,.
-   [shelve](http://docs.python.org/3/library/shelve.html) (
    [py2k](http://docs.python.org/2/library/shelve.html))
    Python object persistence.

## Structured Markup {#markup_modules}
See also [XML Parsers Libraries](#xml_parsers}

-   [Structured Markup Processing Tools
    ](https://docs.python.org/3/library/markup.html)
    ([py2k](https://docs.python.org/2/library/markup.html))
-   [xml.etree.ElementTree](https://docs.python.org/3/library/xml.etree.elementtree.html)
    The ElementTree XML API.<br/>
    The Element type is a container object, designed to store
    hierarchical data structures, such as simplified XML infosets, in
    memory. The ElementTree wrapper type adds code to load XML files
    as trees of Element objects, and save them back again.
    -   [Process XML in Python with ElementTree
        ](http://www.opensourcetutorials.com/tutorials/Server-Side-Coding/Python/xml-matters/page1.html)
        is a tutorial by  David Mertz.
-
<!---------------------------------------------------------->

# Libraries
The standard Python modules are in the
[Modules section](#modules "internal reference") and
the [Python 3 full module index](http://docs.python.org/3/modindex.html) or
[Python 2.7 full module index](http://docs.python.org/2/py-modindex.html).

There is a wider list of
[Useful Modules, Packages and Libraries](http://wiki.python.org/moin/UsefulModules).
In the python wiki, and a more recent in [awesome-python
](https://awesome-python.com/).

_This section also includes python script collections_,

see also the [xCGI stuff](/node/python_web#wsgi "internal reference").

## Packages repositories

-   [PyPI - the Python Package Index]( http://pypi.python.org/pypi)
    is a repository of software for Python and 3rd party Python modules.
    You can find there package in *sdist* source distribution and some
    in the new *wheel* built distribution.
-   The [Wheels site](http://pythonwheels.com/) list *PyPI* packages
    available in *wheel* format.
-   You can find the
    [libraries for py3k in PyPI](http://pypi.python.org/pypi?:action=browse&c=533)
-   [on python3 yet](http://onpython3yet.com/)
    help to test the packages compatibility with Python3
-   [Useful Modules, Packages and Libraries
    ](http://wiki.python.org/moin/UsefulModules) from the
    [Python wiki](http://wiki.python.org/)
-   [Python Cookbook](http://aspn.activestate.com/ASPN/Python/Cookbook)
    is a huge collection of recipes and tips.
-   The  [PLEAC project](http://pleac.sourceforge.net/)
    is an (*old*) project to translate the *Perl Cookbook* in various language
    It has a [python section](http://pleac.sourceforge.net/pleac_python/)
    with 85% of  *Perl Cookbook* recipes translated in a *quite old
    2.2 to 2.4* python.

## Programming Utilities
-   [configobj](https://github.com/DiffSK/configobj)
    is a config file reader and writer.
    -   [configobj manual](http://configobj.readthedocs.org/en/latest/).
-   [Online python tutor](http://pythontutor.com/) (BSD-license)
    is an educational tool that allow to write Python program
    directly in the web browser, and step through its execution,
    it can run Python 3 code.
    [GitHub repository](https://github.com/pgbovine/OnlinePythonTutor/).
    -   Use it [online at pythontutor.com
        ](http://pythontutor.com/visualize.html).
-   [PyMacs](http://pymacs.progiciels-bpi.ca/pymacs.html)
    by François Pinard allows two-way communication between Emacs Lisp and Python.
    The [Manual](http://pymacs.progiciels-bpi.ca/pymacs.html)
    contains many reference to examples.
    [PyMacs repository](https://github.com/pinard/Pymacs)
-   [Rope](http://rope.sourceforge.net/)
    is a python refactoring library, that integrates with emacs using the
    [ropemacs plugin](http://rope.sourceforge.net/ropemacs.htm)
    and pymacs. Rope has now a Py3k branch.
-   [Python Six](http://packages.python.org/six/)
    is a Python 2 and 3 Compatibility Library.
-   [Skulpt](http://www.skulpt.org/) (MIT License)
    is an entirely in-browser javascript implementation of Python.
    it is used online by [CodeSkulptor](http://www.codeskulptor.org/).
    [Skulpt GitHub repository](https://github.com/bnmnetp/skulpt/).
-   [stevedore](https://github.com/dreamhost/stevedore) (Apache License)
    allows you to configure and extend your application by discovering
    and loading extensions (“plugins”) at runtime, by using an
    extension of setuptools entry points.  You can find it
    [in Pypi](https://pypi.python.org/pypi/stevedore), read also the
    [stevedore documentation](http://stevedore.readthedocs.org/en/latest/).

## Data Model
-   [toolz](http://toolz.readthedocs.org)
    provides a set of utility functions for iterators, functions, and dictionaries.
    They extend the [standard libraries itertools and functools
    ](#functools "internal reference") .

## Build Automation {#build_automation}
The continuous integration software is in the main
[Continuous Integration](/node/software_design#continuous_integration "internal reference")


-   see also the Wikipedia [w:Category:Compiling tools],
    [w:Category:Build automation],  [w:Continuous integration]
-   [Buildout](http://www.buildout.org/) (Zope Public License)
    is a Python-based build system for creating,
    assembling and deploying applications from multiple
    parts. Wikipedia: [w:Buildout].
-   [Paver](http://paver.github.com/paver/)(BSD license) is a
    Python-based software project scripting tool
-   [Doit](http://pydoit.org/) <a name="pydoit"></a>
    alias *pydoit* alias *python-doit* is a tool that brings
    the power of build-tools to execute any kind of task. It integrates
    [inotify](/node/schedulers#inotify "internal reference").
-   [Redo](https://github.com/apenwarr/redo) (GPL) from Avery Pennarun
    is a Gnu Make replacement in python allowing recursive build.
-   [Scons](http://www.scons.org/wiki/AboutSCons) (MIT license) is a Gnu
    Make replacement in python. Wikipedia: [w:Scons] _Scons is in
    Debian._
    [Scons Versus Other Build Tools
    ](http://www.scons.org/wiki/SconsVsOtherBuildTools)
    from scons Wiki,
    [Alternatives to Make, Part II
    ](http://quirkygba.blogspot.fr/2008/10/alternatives-to-make-part-ii.html)
    by Richard Quirk,
    [Empirical Comparison of SCons and GNU Make
    ](http://www.genode-labs.com/publications/scons-vs-make-2008.pdf)
    by Ludwig Hähne and
    [Make alternatives](http://freecode.com/articles/make-alternatives)
    by Adrian Neagu compare Scons with Gnu Make and many other tools
    _(but not Redo)_
-   [w:Waf](BSD License) is a Python-based framework for configuring,
    compiling and installing applications.
    [Waf Home](http://code.google.com/p/waf/).
    It aims at being an improvement of Scons, providing higher-level functionality similar
    to that of Autotools. .

## Command Line

-   [Python packaging](http://www.scotttorborg.com/python-packaging/)
    includes a [Command Line Scripts page
    ](http://www.scotttorborg.com/python-packaging/command-line-scripts.html)
    which introduce to the use of setup tools _entry points_.
-   [CommandLineApp](https://doughellmann.com/blog/2007/08/12/commandlineapp/)
    by Doug Hellmann is a base class for command line applications. It
    is described in his article
    [Command line programs are classes, too!
    ](http://www.doughellmann.com/articles/pythonmagazine/features/commandlineapp/)
-   [Cliff](https://github.com/dhellmann/cliff)  (Apache License)
    by Doug Hellmann is a framework for building command line
    programs. It uses setuptools entry points to provide subcommands,
    output formatters, and other extensions.
-   [Clint](https://github.com/kennethreitz/clint) (BSD? / MIT?)
    by Kenneth Reiz is a module grouping tools for developing
    commandline applications.
-   _Cli_ or [Pypi: pyCLI](https://pypi.python.org/pypi/pyCLI/)
    is a framework for  command line applications it helps to
    add standard command line parsing; logging; unit and functional
    testing; and profiling to your apps.
    -   [Cli documentation](http://pythonhosted.org/pyCLI/).
    -   [Cli GitHub repository](https://github.com/whilp/cli)
-   [Click](https://github.com/pallets/click)
    is a Python package for creating command line interfaces. It
    provides arbitrary nesting of commands, automatic help page
    generation, lazy loading of subcommands at runtime.
    It is in Debian as python(3)-click, and for multithreaded
    development as  python(3)-click-threading.
-   [Clime](http://clime.mosky.tw/)
    converts any module into a multi-command CLI program without any
    configuration by a single `import`.
    [GitHub: Clime](https://github.com/moskytw/clime).
-   [Docopt](http://docopt.org/) (MIT License)
    is a python command line arguments parser, that can be used with python scripts
    and  also bash, ruby, coffeescript, javascript; go, ...
    [GitHub: docopt](https://github.com/docopt/docopt)
-   [Plac](http://micheles.googlecode.com/hg/plac/doc/plac.html) (BSD
    License) By Michele Simionato.

## Cryptography

-   [M2crypto](http://chandlerproject.org/Projects/MeTooCrypto)
    is a complete python interface to openssl.
    It features RSA, DSA, DH, HMACs, message digests, symmetric ciphers (including AES);
    SSL functionality to implement clients and servers;
    HTTPS extensions to Python's httplib, urllib, and xmlrpclib;
    unforgeable HMAC'ing AuthCookies for web session management;
    FTP/TLS client and server; S/MIME;  ...
    -   [GitHub: M2Crypto](https://github.com/martinpaljak/M2Crypto)
    -   The previous maintainer of M2Crypto has a
        [Python Blog](http://www.heikkitoivonen.net/blog/category/python/)
-   [Passlib](http://pythonhosted.org/passlib/) (BSD License)
     is a password hashing library for Python 2 & 3, which provides
     implementations of over 30 password hashing algorithms.
-   [Pycrypto](https://www.dlitz.net/software/pycrypto/)
    is a collection of cryptographic algorithms (AES, DES, RSA,
    ElGamal, etc.) and secure hash functions
    (such as SHA256 and RIPEMD160), implemented for
    use from Python 2 & 3.
    -   [pycrypto manual](https://www.dlitz.net/software/pycrypto/doc/)
    -   [GitHub: pycrypto](https://github.com/dlitz/pycrypto)
-   [PyMe](http://pyme.sourceforge.net/) (GPL)
     is a python interface to GPGME library. It is in the Debian package
     _python-pyme_
-   [Python-gnupg](http://code.google.com/p/python-gnupg/) (New BSD LIcense)
    is a python wrapper for GnuPG. It is in PyPI.
    [Python-gnupg documentation](http://pythonhosted.org/python-gnupg/).
-   [GnuPGInterface](http://py-gnupg.sourceforge.net/)  (LGPL)
    is a Python module to interface with GnuPG. It  interacts with GnuPG via filehandles,
    It is in PyPI and in the Debian package _python-gnupginterface_

## Development environment

-   [PyPI: Integrated Development Environments](http://wiki.python.org/moin/IntegratedDevelopmentEnvironments) gives a full list of python IDEs.
-   [Pydbgr](http://code.google.com/p/pydbgr/)
    is an extended python debugger replacing the previous
    [Pydb](http://bashdb.sourceforge.net/pydb/), but it is not _yet_
    ported to Py3k.
-   [WinPdb](http://winpdb.org/) (GPL) is a platform independent GPL Python debugger said to be up to 20 times faster than pdb.
    It is
    [packaged in Debian](http://packages.debian.org/unstable/python/winpdb);
    _Winpdb_ development seems to have slow down, and the last release
    at the time of this writting is 1.4.8 with support of python 3.0. Nothing
    for 3.2 and 3.3, and the Debian package is only for python 2.x.
-   <a name="ipython"> [IPython](http://ipython.org/)
    is an interactive development environment for python
    which provides an enhanced interactive Python shell..
    IPython is introduced in the article
    [IPython: A System for Interactive Scientific Computing (pdf)
    ](http://fperez.org/papers/ipython07_pe-gr_cise.pdf)
    from Fernando Pérez &amp; Brian E. Granger.<br />
    The [documentation of IPython
    ](http://ipython.readthedocs.io/en/stable/)
    contains the Manual.</br>
    It has now [support for py3k](http://wiki.ipython.org/Python_3).
-   [CodeMirror](http://codemirror.net/)
    is a JavaScript component that provides a code editor in the
    browser.
    [CodeMirror GitHub repository](https://github.com/marijnh/CodeMirror).
-   __Emacs__:
    -    EmacsWiki gives many configuration recipes for editing python in
        emacs in the page [Python Programming In Emacs
        ](http://www.emacswiki.org/emacs/PythonProgrammingInEmacs).
    -   [emacs-for-python](http://gabrielelanaro.github.io/emacs-for-python/)
        by Gabriele Lanaro is a collection of emacs extensions.
    -   [Jedi.el - Python auto-completion for Emacs
        ](http://tkf.github.io/emacs-jedi/)
    -   [Elpy](https://github.com/jorgenschaefer/elpy) (GPL)
        is an Emacs package to bring Python editing to Emacs.
-   [Eric](http://eric-ide.python-projects.org/) (GPL) is a Python and
    Ruby editor and IDE, written in python/QT on the top of Scintilla.
-   [Leo](http://webpages.charter.net/edreamleo/front.html) (MIT License)
    is a Python programmer's editor, scriptable in Python  which requires either the Tkinter or PyQt.
    Leo provides an outline-oriented browser and project manager.
-   [Medit](https://bitbucket.org/medit/medit/) is a PyGTK programming editor,
    with python source support and pluginss in C, LUA, Python, shell.
-   [Pida](https://bitbucket.org/aafshar/pida-main) (GPL)
    is an integrated development environment written in PyGTK, that can be used
    from an external editor like vim or the embedded Medit widget. Ali Afshar
    the author of Pida has stopped contributing in 2010, some other contributors
    have continued the development until begining 2012, and since the project seems stalled.
-   [SPE](http://pythonide.blogspot.com/) (said GPL!)
    is an Integrated Development Environment for python.Even if _spe_
    is GPL, there is no help, and the manual is not open-source nor
    free. Of course it is not said you have to _pay_ for it, no you
    just _donate_ money, and it is sent back to thank you.


## Embedding Extending
Read first the
[Extending and Embedding the Python Interpreter Tutorial
](http://docs.python.org/3/extending/index.html) (
[py2k](http://docs.python.org/extending/index.html)).

- [Extending Vs. Embedding](http://www.twistedmatrix.com/users/glyph/rant/extendit.html)
  explains why you should favor extending upon embedding.
- [swig](http://www.swig.org/) is a multi language binding generator.
  It takes a definition file consisting of a mixture of C code and
  specialised declarations, and produces an extension module.
- [Elmer](http://elmer.sourceforge.net/) is a tool which embeds a Python
  module into a C, C++, or Tcl application. The embedded Python module is
  used just as if it was written in the same language as the application
  itself, without requiring any knowledge of the Python/C API.
- [w:Pyrex_(programming_language)|Pyrex (Wikipedia Page)]
  generates the glue  necesary to use C extension for  Python. It goes
  further than swig an pyinline because  it helps to create new python
  extension type. Pyrex  deals with the basic types just  as SWIG, but
  it also lets you write code to convert between arbitrary Python data
  structures and arbitrary C data structures, without knowing anything
  about the Python/C API.
  [Pyrex Home Page](http://www.cosc.canterbury.ac.nz/greg.ewing/python/Pyrex/)
- [w:Cython] (Apache License)
  is a derivative of the Pyrex language, and supports more features
  and optimizations than Pyrex.

## Graphic User Interfaces
The standard modules are in the [Modules Section](#modules "Internal Reference")
there is also the page on [Web Programming](/node/python_web "Internal Reference")

-   [EasyGui](http://easygui.sourceforge.net/)
    is a module for very simple *non event driven* GUI programming
-   [Python Dialog](http://pythondialog.sourceforge.net/)
    is a Python module for making simple Text/Console-mode
    user interfaces on Unix/Linux systems.
-   [PyZenity](http://brianramos.com/?page_id=38)
    is an interface to Zenity.
-   [PyjamasDesktop](/node/python_web#pyjamasdesktop "Internal Reference")
    in the section
    [Web Programming](/node/python_web "Internal Reference").


## Icalendar
You may also want to look at the [Icalendar Section](/node/calendar "Internal reference")

-   [iCalendar package for Python](http://codespeak.net/icalendar/)
    (LGPL) is an older project than vobject, no more developed
    since 2006
-   [vobject](http://vobject.skyhouseconsulting.com/) (Apache
    License) is a python icalendar library, intended to be a full
    featured Python package for parsing and generating vCard and
    vCalendar files. It is reviewed in
    [VObject - An iCalendar and vCard Library (presentation at PyCon 2006)](http://www.python.org/pycon/2006/papers/53/)
    - [Vobject usage examples](http://vobject.skyhouseconsulting.com/usage.html)
    - [Vobject API](http://vobject.skyhouseconsulting.com/epydoc/)

## Image processing
-   The [Python Imaging Library
    ](http://www.pythonware.com/products/pil/) (custom open source license)
    and [Python Imaging Library Handbook
    ](http://www.pythonware.com/library/pil/handbook/).
-   [PythonMagick](http://wiki.python.org/moin/ImageMagick)
    is the Python binding of the ImageMagick library. (py2k and py3k)
    but [does not seems to install on linux](http://wiki.wxpython.org/PythonMagick).
-   [pgmacick](http://pypi.python.org/pypi/pgmagick/) (BSD style license)
     is a boost.python based wrapper for GraphicsMagick.
    It is packaged in Debian/Ubuntu.
-   [PyCairo](http://www.cairographics.org/pycairo/)
    is a python binding (py2k and py3k) for the
    [Cairo Librairy](http://cairographics.org/).
-   [PyLibTiff](http://code.google.com/p/pylibtiff/) (BSD License)
     is a package that provides a wrapper to the libtiff library.
-   [SciPy](http://www.scipy.org/) has a package dedicated to image processing:
    [scipy.ndimage](http://docs.scipy.org/doc/scipy/reference/tutorial/ndimage.html)

## Network services {#network_libs}
### Low Level
#### Ip manipulation
See also the [ipaddress module](#ip_address_module "Internal Reference")

-   [ipaddr](http://code.google.com/p/ipaddr-py/) (Apache License)
    is a library for working with IP addresses, both IPv4 and IPv6 developed by Google.
    [Pypi: ipaddr](https://pypi.python.org/pypi/ipaddr/)
-   [ipcalc](https://github.com/tehmaze/ipcalc)
    allows you to perform IP subnet calculations, there is support
    for both IPv4 and IPv6 CIDR notation.
    [Pypi: ipcalc](http://pypi.python.org/pypi/ipcalc).<br />
    [ipcalc documentation](http://ipcalc.readthedocs.org/en/latest/).
-   [iptools](https://github.com/bd808)(BSD License)
    are utilities for manipulating IPv4 and IPv6 addresses, and CIDR networks.
    It is aimed at the definition of `INTERNAL_IPS` in a Django project’s settings.
    [iptools documentation](http://python-iptools.readthedocs.org/en/latest/).<br />
    [Pypi: iptools](https://pypi.python.org/pypi/iptools).
-   [netaddr](https://github.com/drkjam/netaddr/) (BSD License)
    is a network address manipulation library for Python2/Python3.
    [netaddr on pypi](https://pypi.python.org/pypi/netaddr/).<br />
    [netaddr documentation](http://pythonhosted.org/netaddr/).


### High level
-   The [Google data Python client library
    ](http://code.google.com/p/gdata-python-client)
    is a python interface to [Google data protocol
    ](http://code.google.com/apis/gdata/).
    [Getting Started with the Google Data Python Library
    ](http://code.google.com/apis/gdata/articles/python_client_lib.html)
    is a short tutorial that give no true help, you may better look at the API, the
    [code api documentation](http://code.google.com/apis/gdata/)
    itself is quite comprehensive. There are also
    [Wiki Entries](http://code.google.com/p/gdata-python-client/w/list)
    each of which is an HowTo.
-   [GoogleCL](http://code.google.com/p/googlecl/)
    is a command line python interface to google services, it covers
    _Blogger_, _Calendar_, _Contacts_, _Docs_, _Picasa_,
    _YouTube_. You can read the
    [Manual](http://code.google.com/p/googlecl/wiki/Manual) and set
    [Configuration options
    ](http://code.google.com/p/googlecl/wiki/ConfigurationOptions).
-   [imaplib](http://docs.python.org/3/library/imaplib.html),
    ([py2k](http://docs.python.org/2/library/imaplib.html))
    IMAP4 protocol client from the standard library.
    You find examples in [PyMOTW: imaplib](https://pymotw.com/3/imaplib/)
-   [IMAPClient](http://imapclient.freshfoo.com/) (BSD License)
    Pythonic and complete IMAP client library with no dependencies
    outside the Python standard library.
-   [gocept.imapapi](http://pypi.python.org/pypi/gocept.imapapi/)
    an object-oriented API for accessing IMAP servers.
-   [Python ldap](http://python-ldap.sourceforge.net/)
    is the python interface to ldap, there is an
    [on line python-ldap documentation
    ](http://python-ldap.sourceforge.net/doc/python-ldap/index.html).
-   [Ldaptor](https://github.com/twisted/ldaptor)
    is a LDAP server, client and utilities, using Twisted Python.
    [Ldaptor’s documentation](https://ldaptor.readthedocs.org/en/latest/)
    Slides of a talk by Tommi Virtanen
    [Creating a simple LDAP application](http://tv.debian.net/talks/ldaptor/).
-   [libcloud](http://libcloud.apache.org/) (apache licence)
    is a Python library for interacting with many of the popular cloud
    service providers using a unified API.
-    <a name="paramiko"></a>[Paramiko](http://www.lag.net/paramiko/)
    (LGPL) is a module that implements the SSH2 protocol.
    - [SSH Programming with Paramiko | Completely Different
      ](http://jessenoller.com/2009/02/05/ssh-programming-with-paramiko-completely-different/) by Jesse Noller.
    - [Using SSH in Python with Paramiko
      ](http://sujitpal.blogspot.com/2010/11/using-ssh-in-python-with-paramiko.html) by Sujit Pal

-   [A list of open-source HTTP proxies written in python
    ](http://xhaus.com/alan/python/proxies.html).
-   [Twisted](https://twistedmatrix.com/trac/) is an
    asynchronous networking framework written in Python, supporting
    TCP, UDP, multicast, SSL/TLS, serial communication.
    -   [Twisted Documentation
        ](https://twistedmatrix.com/trac/wiki/Documentation)
    -   [projects using twisted
        ](http://twistedmatrix.com/trac/wiki/ProjectsUsingTwisted)



## Packaging - Installing {#packaging}
-   The <a name="pypa"></a>[Python packaging user guide
    ](https://python-packaging-user-guide.readthedocs.org/)
    is the official reference for python packages.
-   <a name="setuptools"></a> The new
    [Setuptools](http://pythonhosted.org/setuptools/index.html)
    from version 1.x (2013) reconcile Setuptools with the
    [Distribute](#distribute "internal reference") fork in a single
    merge. By now we can use it on both Python 2.x and Python 3.x
    where it replaces the two previous forks.
-   [PyPi: setuptools](http://pypi.python.org/pypi/setuptools)
-   [setuptools documentation](https://pythonhosted.org/setuptools/index.html):
    -   [Building and Distributing Packages with Setuptools
        ](https://pythonhosted.org/setuptools/setuptools.html),
    -   [Easy Install](https://pythonhosted.org/setuptools/easy_install.html)
    -   [Package Discovery and Resource Access using pkg_resources
        ](https://pythonhosted.org/setuptools/pkg_resources.html)
-   <a name="distribute">[Distribute](http://pythonhosted.org/distribute/)
    was a fork from the older version of
    [Setuptools](#setuptools "internal reference")
    project version 0.x, it is now deprecated after a merge with
    [Setuptools](#setuptools "internal reference").
    It was  providing  a drop-in replacement for
    [setuptools](#setuptools "internal reference") and offered Python
    3 support with the same commands than
    [Setuptools](#setuptools "internal reference").<br >
    [The Hitchhiker’s Guide to Packaging
    ](http://guide.python-distribute.org/index.html)
    (don't confuse with the [Hitchhiker’s Guide to Python
    ](http://docs.python-guide.org/en/latest/) which is an up to date guide to all
    python development)
    was a guide to [Distribute](#distribute "internal reference")
    and [Pip](#pip "internal reference"), which is the base of the present
    [Python Packaging Guide](#pypa "internal reference")
-   The [module distutils](#distutils "internal reference")
    is part of the standard library.
-   [PIP](http://www.pip-installer.org/en/latest/)<a name="pip"></a>
    is an enhancement of setuptool and a replacement for easy_install,
    it is complementary with
    [virtualenv](#virtualenv "internal reference") and can be used
    inside virtualenv.
-    <a name="fabric"></a>[Fabric](http://docs.fabfile.org/)
    (BSD License) is a library and command-line tool for streamlining
    the use of SSH for application deployment or systems
    administration tasks.  It is similar to Makefiles but with the
    ability to execute commands on a remote server. <br />
    Fabric uses [paramiko](#paramiko "Internal Reference").<br/>
    The [Fabric documentation](http://docs.fabfile.org/) provides a
    [Tutorial](http://docs.fabfile.org/en/latest/tutorial.html),
    [Recipes](http://wiki.fabfile.org/Recipes)
    [UseCases](http://wiki.fabfile.org/UseCases) and a
    [FAQ](http://docs.fabfile.org/en/latest/faq.html).
    -   [GitHub: Fabric](https://github.com/fabric/fabric)
    -   [Debian Administration: A simple introduction to fabric
        ](http://www.debian-administration.org/articles/671).
    -   [Python For Beginners: How to use Fabric in Python
        ](http://www.pythonforbeginners.com/systems-programming/how-to-use-fabric-in-python/).
    -   [Using Fabric to manage your deployments
        ](http://johan.beyers.co.za/2012/09/23/using_fabric_to_manage_your_deployments.html)
        a tutorial by Joyan Beyers.
    -   [Using Fabric for SSH](http://advanced-python.readthedocs.org/en/latest/fabric.html)
        in [Curriculum for Advanced Python](http://advanced-python.readthedocs.org/en/latest/).
    -   An example of use is  the [Flask site deployment with Fabric
        ](http://flask.pocoo.org/docs/patterns/fabric/) or also the
        [Byte of python fabfile
        ](https://github.com/swaroopch/byte_of_python/blob/develop/fabfile.py)

## Parsers
-   [Python Wiki: Language Parsing
    ](https://wiki.python.org/moin/LanguageParsing)

### PEG Parsers
They use [w:Parsing expression grammar] you can look at the
[slides of the presentation
](http://www.brynosaurus.com/pub/lang/peg-slides.pdf) by Bryan Ford
the author of PEG grammars (2004).

-   [PyPeg](http://fdik.org/pyPEG/)  for Python version 2.7 and 3.x.
    [BitBucket: PyPeg](https://bitbucket.org/fdik/pypeg/).
-   [Parcimonious](https://github.com/erikrose/parsimonious) for
    Python version 2.7 and 3.x. [Pypi: parsimonious
    ](https://pypi.python.org/pypi/parsimonious).
-   [Grako](http://pythonhosted.org//grako/) work with  Python 2.7,
    3.4, or PyPy 2.3
    . [BitBucket: Grako](https://bitbucket.org/apalala/grako).

### MISC Parsers

-   [mxTextTools
    ](http://www.egenix.com/products/python/mxBase/mxTextTools/)
    from eGenix (Open source license derived from python cnri
    license) is a high performance text processing library, it is described in the
    chapter 4 of the David Mertz's book _Text Processing in Python_,
    ([on-line text version
    ](http://gnosis.cx/TPiP/chap4.txt)).
    SimpleParse is an EBNF parser library written on the top of
    mxTextTools, it is descibed in the same chapter 4 of the book of David Mertz
    and in his article in the _Charming Python_ serie
    [Parsing with the SimpleParse module
    ](http://www.ibm.com/developerworks/library/l-simple.html).
-   [pyexcelerator](http://sourceforge.net/projects/pyexcelerator/)
    and [pyxlwriter](http://sourceforge.net/projects/pyxlwriter/)
    are packages for excel generation in Python.
-   [Pyparsing](http://pyparsing.wikispaces.com/)
    is an alternative approach to creating and executing simple
    grammars, vs. the traditional lex/yacc approach, or the use of regular
    expressions.<br/>
    [PyPi: PyParsing](https://pypi.python.org/pypi/pyparsing).
-   [xlrd](https://pypi.python.org/pypi/xlrd)
    is a library for developers to use to extract information from
    Microsoft Excel (tm) spreadsheet


### XML Parsers {#xml_parsers}
Along an
[answer from Ian Bicking](http://stackoverflow.com/a/2680724/965798)
the standard library module HTMLParser fails on lots of very common
HTML, and there are really only 3 reasonable ways to parse HTML (as it
is found on the web): lxml.html, BeautifulSoup, and html5lib.

-   The python wiki gives a list of
    [XML processing solutions](http://wiki.python.org/moin/PythonXml)
-   [Beautiful Soup](http://www.crummy.com/software/BeautifulSoup/)
    is a Python permissive HTML/XML parser
-   [html5lib-python
    ](https://github.com/html5lib/html5lib-python) HTML parser based on the
    [WHATWG HTML5 specification](https://html.spec.whatwg.org/).<br/>
    [html5lib-python documentation](http://html5lib.readthedocs.org/en/latest/).
-   [lxml](http://lxml.de/) is a Pythonic binding
    for the  [libxml2](http://xmlsoft.org/) and libxslt libraries. It is compatible with ElementTree.
    It allows to parse HTML and provides a number of utilities for common tasks.
-   [appy.pod (python open document)](http://appyframework.org/pod.html)
    (GPL ) is a library that generate Open Document Format,
    documents whose content is dynamic.
    [appy is in PyPi](https://pypi.python.org/pypi/appy).
-   [reportlab](http://www.reportlab.com/)
    provides open source software like the [ReportLab Toolkit
    ](http://www.reportlab.com/opensource/)
    for generating printable PDF documents from any data source, _Preppy_ a small
    preprocessor utility written in python, _pyRXP_ a fast XML parser,
    _PythonPoint_ which is part of _ReportLab Toolkit_
    is a Python library for creating PDF documents from an XML
    source format.<br/>
    [ReportLab Toolkit Manual (pdf)
    ](http://www.reportlab.com/docs/reportlab-userguide.pdf).
-   [4Suite](https://pypi.python.org/pypi/4Suite-XML/)
    is a collection of Python tools for XML processing and object database management.
    It is no longer maintained since 2006.

### RSS Parsing

-   [feedvalidator](https://github.com/rubys/feedvalidator)
    (MIT license)
    is a validator for syndicated feeds. It works with Atom,
    RSS feeds as well as OPML and KML formats.
    It powers [feedvalidator](http://feedvalidator.org/).<br/>
    [FeedValidator Howto install and run
    ](http://feedvalidator.org/docs/howto/install_and_run.html).
-   [feedparser](https://github.com/kurtmckee/feedparser)
    Parse Atom and RSS feeds in Python.  It can handle RSS 0.90,
    Netscape RSS 0.91, Userland RSS 0.91, RSS 0.92, RSS 0.93, RSS
    0.94, RSS 1.0, RSS 2.0, Atom 0.3, Atom 1.0, and CDF feeds.
    -   [feedparser in PyPi](https://pypi.python.org/pypi/feedparser).
    -   [feedparser documentation
        ](http://pythonhosted.org/feedparser/).
-   [PyRSS2Gen](http://www.dalkescientific.com/Python/PyRSS2Gen.html)
    A Python library for generating RSS 2.0 feeds.<br/>
    [PyRSS2Gen on PyPi](https://pypi.python.org/pypi/PyRSS2Gen)

### static html content generation {#static_html}
See also the [Static Site section
](/node/static_sites "internal reference").

-   [Houdini.py](http://python-houdini.61924.nl/)
    ([GitHub Repository](https://github.com/FSX/houdini.py)
    by [Frank Smit (FSX)](https://github.com/FSX) is a Python binding for
    [Houdini](https://github.com/vmg/houdini)  a simple C library by
    [Vicent Martí (vmg)](https://github.com/vmg/) for escaping text for the web.


##  Preprocessor

-   [Karnickel](http://pypi.python.org/pypi/karnickel) BSD License)
    allows you to use macros in Python code.
     It is different from calling functions in that the code is inserted before it is compiled.
-   [Preprocess](http://code.google.com/p/preprocess/) (MIT License)
    is a variation on the C preprocessor that works on multiple languages and
    encodes preprocessor statements as comments. _2009 Python 2_
-   [pppp — Poor's Python Pre-Processor](http://pymacs.progiciels-bpi.ca/pppp.html)
     by François Pinard is a python preprocessor that was written
     to help porting Pymacs to Python 3.

We can also use [literate programming tools](/node/literate_programming "internal reference") like
[cog](/node/literate_programming#cog "internal reference") or [template engines](/node/python_web#template_engines  "internal reference") like [Jinja2](/node/python_web#jinja2  "internal reference")

## Processes {#process}
See also the
[python modules in the process section](#process_modules "internal reference")

-   [Dbus-Python](http://dbus.freedesktop.org/doc/dbus-python/) is the python Dbus bindings.
    Freedesktop has a [Dbus Python Tutorial](http://dbus.freedesktop.org/doc/dbus-python/doc/tutorial.html).  There are also some
    [Dbus Examples on the Python Wiki](http://wiki.python.org/moin/DbusExamples) and you can refer to the
    [Dbus Python API](http://dbus.freedesktop.org/doc/dbus-python/api/).
-   [Pyinotify](https://github.com/seb-m/pyinotify)
    is a Python package used for monitoring filesystems events
    with [inotify](http://inotify.aiken.cz/) _Wikipedia: [w:inotify]_.
    The [pynotify documentation](https://github.com/seb-m/pyinotify/wiki)
    includes a tutorial and some examples.
    -   Pynotify is used in
        [pirsyncd - Python Inotify Rsync Daemon
        ](http://ebalaskas.gr./blog/?page=pirsyncd)
        see the [pirsyncd repository](https://bitbucket.org/ebal/pirsyncd)
    -   You may be interrested also in
        [incron](http://inotify.aiken.cz/?section=incron&page=doc)
        _a C compiled daemon_.

The following tools implement a subprocess management; similar to the
shells process combinators like the pipe.

-   [envoy](https://github.com/kennethreitz/envoy)
    is a wrapper around the subprocess module. It is in pypi and
    similar to _sh_; but the project seems less active _2014_.
-   [ipython](#ipython "internal reference") referenced
    [above](#ipython "internal reference") can be
    [used as a system interactive shell
    ](http://ipython.readthedocs.io/en/stable/interactive/shell.html).
-   [plumbum](http://plumbum.readthedocs.io/en/latest/)
    is a library for writing shell script-like programs in Python.
    It mimic the shell syntax _(shell combinators)_  while keeping it
    all Pythonic.

    It provides  local and remote command execution (over SSH),
    local and remote file-system paths, working-directory and
    environment manipulation, and a programmatic Command-Line
    Interface (CLI) application toolkit.

    Plumbum is available in debian as python-plumbum or
    python3-plumbum.

-   [sh](http://amoffat.github.io/sh/index.html)
    is a subprocess replacement for Python 2.6 - 3.5, PyPy and PyPy3
    that allows you to call any program as if it were a function.
-   [sarge](https://bitbucket.org/vinay.sajip/sarge/)
    provides a wrapper for subprocess which provides command pipeline
    functionality.
-   [xonsh](http://xon.sh/)
    Xonsh is a Python-powered, cross-platform, Unix-gazing shell
    language and command prompt. The language is a superset of Python
    3.4+.


There are many tools to implement in python command line text
manipulation tool similar to awk or sed which uses standard python
string and list methods as well as custom functions.
They are compared in two threads from 2014 and 2015 of _HackerNews_:
[here](https://news.ycombinator.com/item?id=8847141),
[and here](https://news.ycombinator.com/item?id=8158976)

-   [_pyp_ - The Pyed Piper](http://code.google.com/p/pyp/) (BSD License)
    In pypi _2012_.
-   [Pyped](http://github.com/ksamuel/Pyped)
    works in python2 and python3. In _pypi_, _2014_.
-   [pythonpy](https://github.com/Russell91/pythonpy) (MIT License)
    works in python2 and python3. In _pypi_, _active in 2016_.
    This [thread in _python-ideas_
    ](https://mail.python.org/pipermail/python-ideas/2015-January/030837.html)
    give some evaluation / criticisms to the concepts of
    *pythonpy*, the end of the thread compare it with _spy_.
-   [pyin](https://github.com/geowurster/pyin) (BSD License)
    aimed at replacing sed.  In _pypi_, _active in 2016_.
-   [spy](https://github.com/edk0/spy)
    derived from pythonpy and pyp. Only python3, In _pypi_ with
    name _spy-cli_, _2015_.
-   [pit](https://github.com/samzhang111/pit)
    Or Python as a stream filter, python3 _2015_.
-   [pype](https://github.com/ircflagship2/pype)
    Python 2 or 3, in _pypi_ under the name _pypecli_, _2015_.

## Serializing {#serializing_libs}
See also [Modules:Serializing](#serializing_module "internal reference")

-   [jsonpickle](http://jsonpickle.github.com/)
    is a Python library for serialization and deserialization of
    complex Python objects to and from JSON. It extend the standard
    Python module
    [json](http://docs.python.org/3/library/json.html).
-   [simplejson](https://pypi.python.org/pypi/simplejson/)
    is a JSON  encoder and decoder for Python 2.5+ and Python 3.3+.
-   [PyYAML](http://pyyaml.org/) (MIT license)
    is a YAML parser and emitter for Python. _in Debian package python3-yaml_.
    It includes a  complete  YAML 1.1 parser with unicode support.
    PyYAML  supports Python 3.
    -   [PyYAML Documentation](http://pyyaml.org/wiki/PyYAMLDocumentation)
    -   [pretty-yaml _or pyaml_](https://github.com/mk-fg/pretty-yaml)
        is a module to produce pretty and readable YAML-serialized
        data  that extend PyYAML.
-   [PySyck](http://pyyaml.org/wiki/PySyck) (BSD License)
    is a python binding for the
    [Syck](https://github.com/indeyets/syck) YAML library.
    But Syck is minimally maintened since 2005, and stopped at YAML 1.0.
-   [Ijson](https://github.com/isagalaev/ijson) (BSD License)
    is an iterative JSON parser with a standard Python iterator interface.
    Ijson provides several implementations of the actual parsing by using
    [YAJL](http://lloyd.github.io/yajl/) or a pure Python parser (to use under PyPy).
    -   [PyPi: ijson](https://pypi.python.org/pypi/ijson/).

## Test Libraries {#test_libs}
-   [awesome test automation - python
    ](https://github.com/atinfo/awesome-test-automation/blob/master/python-test-automation.md)
-   [awesome-python - testing
    ](https://github.com/vinta/awesome-python#testing)
-   [pythonidae - QA
    ](https://github.com/svaksha/pythonidae/blob/master/QA.md)
-   [pycrumbs - Testing](https://github.com/kirang89/pycrumbs#testing)

### Program Testing packages

-   [coverage](http://nedbatchelder.com/code/coverage/) by Ned Batchelder
    is a tool for measuring code coverage of Python programs.
    It monitors your program, noting which parts of the code have been
    executed, then  analyzes the  source to  identify code  that could
    have been executed but was not.<br />
    Coverage works with python 3.x.
-   [nose](http://readthedocs.org/docs/nose/)
    is a unit test discovery and execution package. described in
    [An Extended Introduction to the nose Unit Testing Framework
    ](http://ivory.idyll.org/articles/nose-intro.html).
    Nose works with python 2.x and 3.x.
    - [Nose GitHub Repository](https://github.com/nose-devs/nose)
    - nose allow use of [test generators
    ](http://readthedocs.org/docs/nose/en/latest/writing_tests.html#test-generators)
-   [py.test](http://pytest.org/) is
    a rest runner, that can integrate unittest, doctest, and nose.
    It works  with python 2.x and 3.x.
-   [ScriptTest](http://pythonpaste.org/scripttest/) (MIT license)
     test command-line scripts. It runs a script and watches the output,
     looks for non-zero exit codes, output on stderr, and any files created,
     deleted, or modified.
-   [TestOOB](http://testoob.sourceforge.net/) (Apache license) is an
    extension of unittest. It add the possibility to run the tests in
    different processes or multiple threads

### Mock objects {#mock_objects}
Gary Bernhardt gives a
[Python Mock Library Comparison](http://garybernhardt.github.com/python-mock-comparison/)
which compare _mock_, _flexmock_, _mox_, _Mocker_, _Dingus_, and _fudge_.

All the following libraries can be used in Python 3.

-   [MiniMock](http://pypi.python.org/pypi/MiniMock)
    is a simple library for doing [w:Mock_object|Mock objects] with doctest.
-   [Mock](http://www.voidspace.org.uk/python/mock/)  is a  library for
    [w:Mock objects] in python including py3k. It is designed for use with unittest.
    It has a very
    [good quality and detailed documentation](http://www.voidspace.org.uk/python/mock/).<br />
    It is integrated in the standard library as
    [unittest.mock](http://docs.python.org/3/library/unittest.mock.html)
    since Python 3.3.
-   [Mox](https://code.google.com/p/pymox/)(Apache License)
    is a mock object framework for Python based on the
    [java library EasyMock](http://www.easymock.org).
     Mox allow to mock the
    public/protected interfaces of Python objects.
-   [Fudge](http://farmdev.com/projects/fudge/) (MIT license)
    is a  module for using fake objects (mocks and stubs).
-   [dingus](https://github.com/garybernhardt/dingus)
    define mock-like objects.  You run your code, using a _dingus_ in
    place of another object or class, and it will record what happens
    to it. Then you can make assertions about what it did to the
    dingus.
-   [flexmock](http://has207.github.com/flexmock/index.html) (BSD License)
    is a mock objects library inspired by the
    [ruby library also named flexmock](https://github.com/jimweirich/flexmock).
-   [chai](https://pypi.python.org/pypi/chai) is a mock library
    patterned after the [Mocha](http://mocha.rubyforge.org/) library for Ruby.

### Web application testing {#webunittest}
-   [Funcload](http://funkload.nuxeo.org/) (GPL) is an extension of unittest
     that allows the functional and load testing of a web application.
-   [twill](http://twill.idyll.org/) is a simple
    scripting language intended for programmatic or automated browsing
    of Web sites.
    [Mechanoid](http://pypi.python.org/pypi/mechanoid) (GPL)
    is also a python console browser based on the same project
    [Mechanize](http://wwwsearch.sourceforge.net/mechanize/)
    (BSD License).
    Both projects are now abandoned since 2007 and stuck to python
    2.3. There was a fork in 2012 [
    retwill](http://bitbucket.org/brandizzi/retwill/);
    it is not yet clear if the project will be maintained.
    -   [Testing Python Web applications using twill and wsgi\_intercept
        ](http://www.advogato.org/article/874.html)
      by Titus Brown.
-   [webunit](http://pypi.python.org/pypi/webunit)
    is a framework for unit testing websites still useful, and used in
    other frameworks like _Funcload_ or _wsgi-intercept_; but badly
    documented and not updated since 2004.
-   [wsgi-intercept](http://code.google.com/p/wsgi-intercept/)
    lets you intercept calls to any specific host/port combination
    and redirect them into a WSGI application importable by your test program.
    wsgi-intercept allows to do functional _or integration_ tests.
-   [webtest](http://pythonpaste.org/webtest/)

    wrap a WSGI application to allow to test it without starting a
    web server. Since version 1.3.1 WebTest is compatible with py3k.
    [WebTest Repository](https://bitbucket.org/ianb/webtest/)

## Virtualenv {#virtualenv}

-   [Virtualenv](http://pypi.python.org/pypi/virtualenv/) (MIT license)
    is a python program that creates an environment that has its own
    installation directories, that doesn't share libraries with other
    virtualenv environments (and optionally doesn't use the globally
    installed libraries either).

    It makes a copy of python *(optionally a specific version)* and
    pip local to the local environment. It may use the globally
    installed libraries, or if it does not, install the dependent
    libraries into that environment.

    It is used for testing and deployment as you know
    exactly which libraries, at which versions, are used and a
    global change will not impact your module.

    -   The [Virtualenv PyPI page](http://pypi.python.org/pypi/virtualenv/)
        is an install manual.
    -   [Neuroimaging project nypi](http://nipy.org/nipy/)
        has a tutorial : [Setting up virtualenv
        ](http://nipy.org/nipy/devel/tools/virtualenv-tutor.html).
    -   Doug Hellmann has written a case study :
        [IPython and virtualenv
        ](https://doughellmann.com/blog/2008/02/01/ipython-and-virtualenv/).

-   virtualenv is no longer necessary with [python 3 venv module
    ](https://docs.python.org/3/library/venv.html), that we should use
    now to create Python 3 virtual environment.

-   [virtualenvwrapper
    ](https://virtualenvwrapper.readthedocs.io/en/latest/)
    (BSD like license)
    by Doug Hellmann is a set of wrappers for creating
    and deleting virtual environments and otherwise managing your development
    workflow, making it easier to work on more than one project at a time
    without introducing conflicts in their dependencies. It is
    compatible with python 3 but does not support [python 3 venv
    ](https://docs.python.org/3/library/venv.html).
    <br />
    Doug Hellmann [does no longer maintain nor use it
    ](https://doughellmann.com/blog/2016/01/03/virtualenvwrapper-needs-a-new-maintainer/).
-   [virtualenv.el](https://github.com/aculich/virtualenv.el)(GPL)
    is an emacs minor mode for setting the virtualenv for the
    Python shell in python-mode.el and python.el
-   [pyenv](https://github.com/yyuu/pyenv)
    *not the python 3 script that was used to call venv until 3.6*
    is a bash extension that lets you easily switch between multiple
    versions of Python.

    It intercepts your calls to python, pip, etc., to direct them to
    one of several of the system python tool-chains.  So you always
    have all the libraries that you have installed in the selected
    python version available

-   [pyenv-virtualenv](https://github.com/yyuu/pyenv-virtualenv),
    *installed by [pyenv-installer](
    https://github.com/yyuu/pyenv-installer)*,
    is a pyenv plugin that provides features to manage virtualenvs
    and conda environments for Python on UNIX-like systems.
    with this you can have a base installation that
    includes more than one version of python and create isolated
    environments within each of them
-   [pyenv-virtualenvwrapper
    ](https://github.com/yyuu/pyenv-virtualenvwrapper)
    is a pyenv plugin which provides a pyenv virtualenvwrapper command
    to manage your virtualenvs with virtualenvwrapper.
-   [PyInstaller](http://www.pyinstaller.org/)
    can take your python code, possibly developed & tested under
    VirtualEnv, and bundle it up so that it can run one platforms that
    do not have *your version of* python installed
-   Since python 3.3 the standard python library includes the
    module [venv](#venv_module "internal reference") which replace
    virtualenv.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
