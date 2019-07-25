---
title: Python Programming
---

{{% toc /%}}

-----

# Python coding style
The page {{< iref "structured_text" "Structured text formatters" >}}
references many python formatters like the docutil restructured text,
asciidoc, markdown, txt2tags ....

-   [Pep 8: Style Guide for Python Code](http://www.python.org/dev/peps/pep-0008/).
-   [Pep 257 Docstring Conventions](http://www.python.org/dev/peps/pep-0257/).
-   [PEP 20: The Zen of Python](http://www.python.org/dev/peps/pep-0020/)
    the philosophy of python in 20 aphorisms that you get with any python
    shell by: `import this`.
-   [Code Style](http://docs.python-guide.org/en/latest/writing/style/)
    in [The Hitchhiker’s Guide to Python!](http://docs.python-guide.org/en/latest/).
-   [Google Python style guide](http://google-styleguide.googlecode.com/svn/trunk/pyguide.html)
-   Barry Warsaw's [Python coding style guide](http://barry.warsaw.us/software/STYLEGUIDE.txt).
    Barry wrote also [Warsaw's Laws of Hackering](http://barry.warsaw.us/software/laws.html),
    that can stand in the {{< wp "Murphy%27s_law"  "category of murphy laws" >}}
     _see [Murphy's laws and corollaries](http://roso.epfl.ch/dm/murphy.html)
     for a large sample of murphy's laws_
-   [A Guide to NumPy/SciPy Documentation
    ](https://github.com/numpy/numpy/blob/master/doc/HOWTO_DOCUMENT.rst.txt).<br >
    Numpy provide the Sphinx extension [numpydoc](http://pypi.python.org/pypi/numpydoc)
    to support docstrings in Numpy format.

# Documentation tools
-   [Python Wiki: Documentation tools](https://wiki.python.org/moin/DocumentationTools)
-   [Documenting Python](http://www.python.org/doc/current/doc/doc.htm)
    by Fred L. Drake describes the document classes
    and special markup used in the Python documentation.
-   [Epydoc](http://epydoc.sourceforge.net/)
    <a name="epydoc"></a> ( MIT open-source license) a documentation generator that
    renders its own lightweight markup language Epytext as well as
    {{< iref "structured_text#reStructuredText" "reStructuredText" >}}
    for Python documentation strings.
    Epytext supports linking between different pieces of documentation.</br>
    It has been the most popular api documentation generator, but is by now often replaced by
    {{< iref "#apidoc" "sphinx-apidoc" >}}, and is now stalled.</br>
-   [pdoc](http://pdoc.burntsushi.net/pdoc) is a new fork of epydoc,
     and intend to continue the development of the now inactive epydoc.
-   [pydoc](http://docs.python.org/3/lib/module-pydoc.html)
     the native documentation generator of python uses the
    [Documentation Strings
    ](http://docs.python.org/3.3/tutorial/controlflow.html#tut-docstrings)
    included in the code.
-   [pydoctor](https://launchpad.net/pydoctor)
    is a documentation generator that replaced epydoc for the
    twisted project. Pydoctor depends on twisted and Nevow.
-   [Pylookup](http://taesoo.org/Opensource/Pylookup) by Taesoo Kim
    is a mode to search python documents especially within emacs.
-   [Sphinx](http://sphinx.pocoo.org/) is a tool originally to build HTML and PDF documentation
    using reStructuredText. It has support for highlighting source
    with Pygment and autogenerating documentation from source code
    with the [autodoc extension](http://sphinx-doc.org/ext/autodoc.html).
    The [extension autosummary] generates function/method/attribute summary lists,
    similar to those output e.g. by Epydoc and other API doc generation tools.
-   <a name=apidoc></a>[sphinx-apidoc
    ](http://sphinx-doc.org/man/sphinx-apidoc.html)
    is a tool for automatic generation of Sphinx sources that,
    using the autodoc extension. It document a whole package in the
    style of
    {{< iref "#epydoc" "epydoc" >}}
    or related documentation tools.

The documentation of python can be done using
{{< iref "source_code#literate_programming" "Literate Programming" >}}
, we can use a langage agnostic tool, or
one of the manifold python literate tools.
See the references to Cog, pyreport , pyWeb, PyLit in the
{{< iref "source_code#literate_programming" "Literate Programming Section" >}}


# Static Code Analyzers
-   [PyCQA](http://meta.pycqa.org/en/latest/)
    or _Python Code Quality Authority_ is an organization which group
    projects in the domain of automatic style and quality reporting.
    -   [GitHub - PyCQA](https://github.com/PyCQA)
-   [PyChecker](http://pychecker.sourceforge.net/)
    (BSD License) is a python syntax checker, it allows to report
    errors found by the compiler in a compiled language. We must
    syntaxly check our python programs, otherwise piece of codes that
    stay unused will keep gross mistakes, until we meet the causes of
    a program crash. PyChecker has a faster
    alternative
    {{< iref "#pyflakes" "Pyflakes" >}}.
    Pychecker is limited to Python 2.
-   [PyLint](http://www.pylint.org/) (GPL)
    includes PyChecker checks, plus checking line-code's
    length, checking if variable names are well-formed, checking if declared
    interfaces are truly implemented ...<br />
    [Pylint User Manual](http://docs.pylint.org/).
    You can configure the rules used by pylint by a `.pylintrc` file,
    the defaults are given by: `pylint --generate-rcfile`.
    Pylint is now compatible with Python 3k.
-    <a name=pyflakes"></a>[Pyflakes](http://pypi.python.org/pypi/pyflakes)
    is program to analyze Python programs and detect various errors.
    Pylint import the analyzed module but Pyflakes only parse the source file,
    so it is safe to use on modules with side effects.
    It's also much faster. Pyflakes has a Python 3 port:
    [Pyflakes3k](http://pypi.python.org/pypi/pyflakes3k)
    ([Pyflakes3k Bitbucket repository
    ](http://bitbucket.org/hsoft/pyflakes3k)).
-   [pycodestyle](https://github.com/PyCQA/pycodestyle)
    (MIT _Expat_ Licence)
    formerly pep8.py is a Python PEP 8 code style checker
    that can be used both for Python 2.x and Python 3.x.
    -   [pycodestyle documentation
        ](http://pycodestyle.pycqa.org/en/latest/)
-   [PEP257.py]( https://github.com/halst/pep257)
    is a docstring style checker by Vladimir Keleshev.
-   [Black](https://github.com/ambv/black) (MIT Licence)
    is a Python code formatter. It intentionally does not allow to
    choose your own rules, its ensure that all black formatted code
    have a common look.



# Encoding
# Python 2 vs. python 3 encoding
-   [chardet](http://chardet.feedparser.org/)
    is an universal encoding detector library for python 2 and 3, that attempt
    to guess the text encoding from its content.
-   [encutils](http://www.python.org/pypi/encutils)
    is a library of helper functions to deal with encodings of text
    files via HTTP and directly.
-   [Python Unicode HOWTO](http://www.amk.ca/python/howto/unicode)
    is for python 2.x
-   [Python 3 Unicode HOWTO](http://docs.python.org/3/howto/unicode.html) is
    updated for the new _3.x_ use of text (_str_) and data (_bytes_).
-   [Practical Python porting for systems programmers
    ](http://www.catb.org/esr/faqs/practical-python-porting/)
    by Peter A. Donis and [Eric S. Raymond](http://www.catb.org/esr/)
    examine the porting from Python 2 to 3.

## Unicode memo

-   Representation of text has
    [changed a lot since v 3.0](http://docs.python.org/3.1/whatsnew/3.0.html#text-vs-data-instead-of-unicode-vs-8-bit).

-   Now python name _text_ what was previously called _unicode_ but
    the type is the new _str_,  and the old _str_ is now _bytes_.

    You no longer use _u"..."_ for text but you have to use _b"..."_ for _bytes_.

-   Python has a clear distinction between _text_ and _data_ the text "au cœur de l'été" has
    16 characters, if you want to repesent these characters as data, you need to convert them
    using an _encoding_, these encoding can use a fixed number of bytes to render a single character
    as do `ascii`, `iso-8859-1` or `utf-32` _but ascii or iso-8859-1 cannot render the previous text_
    or a variable number of bytes like `utf-8` or `utf-16`.

- In python 2.6 _in an utf-8 terminal_ you write:

~~~~
>>> s=u"au cœur de l'été"
>>> type(s)
<type 'unicode'>
>>> len(s)
16
>>> print s
au cœur de l'été
>>> print repr(s)
u"au c\u0153ur de l'\xe9t\xe9"
>>> print s.encode('utf-8')
au cœur de l'été
>>> type(s.encode('utf-8'))
<type 'str'>
>>> len(s.encode('utf-8'))
19
>>> print repr( s.encode('utf-8'))
"au c\xc5\x93ur de l'\xc3\xa9t\xc3\xa9"
>>> len(s.encode('utf-16'))
34
>>> print repr(s.encode('utf-16'))
"\xff\xfea\x00u\x00 \x00c\x00S\x01u\x00r\x00 \x00d\x00e\x00 \x00l\x00'\x00\xe9\x00t\x00\xe9\x00"
~~~~

If you yse python 3.1 it turns out to:

~~~~
>>> s="au cœur de l'été"
>>> type(s)
<class 'str'>
>>> print(s)
au cœur de l'été
>>> print(repr(s))
"au cœur de l'été"
>>> print(s.encode('utf-8'))
b"au c\xc5\x93ur de l'\xc3\xa9t\xc3\xa9"
>>> type(s.encode('utf-8'))
<class 'bytes'>
>>> len(s.encode('utf-8'))
19
>>> print(repr( s.encode('utf-8')))
b"au c\xc5\x93ur de l'\xc3\xa9t\xc3\xa9"
~~~~

# Data model {#data_model}

-   Wikipedia {{< wp "Python_philosophy#Programming_philosophy"  "Python Programming philosophy" >}}
-   Python support {{< wp "Duck typing" >}}, that allow a behavioral rather than family approach to classes.
    _You recognize a duck because it quarks rather to check if it's parents are duck too_.
-   In Python Duck typing can be complemented by
    [Abstract Base Classes (abc)](http://docs.python.org/3/library/abc.html),
    it allows you to see your class as an instance of the (abstract) base class.
    They are defined in
    [PEP 3119 -- Introducing Abstract Base Classes](http://www.python.org/dev/peps/pep-3119/)
-   Abstract Base Classes is peculiar case of {{< iref "#metaclasses" "Metaclass" >}}
    that act as templates for producing classes.
-   The Python data model unify types and classes, it used to be
    called {{< iref "#newstyle_classes" "New Style Classes" >}}
-   Python allows higher type programming, the functions
    transformation are clarified by {{< iref "#decorators" "Decorators" >}}.
-   Python attributes of a class are not limited to data members
    but can be  an instance of a class that implements special methods
    to get and set the value of the attribute. Such class is called a
    {{< iref "#descriptors" "Descriptor" >}}

## Python 2 New Style classes and Python 3 classes {#newstyle_classes}
-   The data model for python 2.x first used _classic classes_ with two distincts concepts of
    _type_ and _class_  the
    [new-style  classes](http://docs.python.org/reference/datamodel.html#newstyle)
    have been introduced to unify classes and types.
    A new-style class is neither more nor less than a user-defined type.
    Note that _new style classes_ are the only class model since 3.0
    since old-style classes are removed .
-   [Unifying types and classes in Python 2.2
    ](https://www.python.org/download/releases/2.2.3/descrintro/1)
    by Guido van Rossum, first part of
    [New-style Classes](http://www.python.org/doc/newstyle/2). Read also
    [Making Types Look More Like Classes (pep 252)
    ](http://www.python.org/dev/peps/pep-0252/)
    and [Subtyping Built-in Types (pep 253)](http://www.python.org/dev/peps/pep-0253).
-   Michael Fötch
    [Introduction To New-Style Classes In Python
    ](http://realmike.org/python/new_style_classes.htm) _2005-2010_
    describes
    Properties, Static Methods, Class Methods, Descriptors, Attribute Slots .
-   In [Python Types and Objects
    ](http://www.cafepy.com/article/python_types_and_objects/contents.html)
    and [Python Attributes and Methods
    ](http://www.cafepy.com/article/python_attributes_and_methods/contents.html) _2005-2009_
    Shalabh Chaturvedi explains the new Python type system.
-   The easy side of [super
    ](http://docs.python.org/library/functions.html#super)
    is expounded in the chandler wiki
    [The Long and Short of Using super
    ](http://chandlerproject.org/Projects/UsingSuper).
-   James Knight warns you against difficulties of using super in
    [Python's Super is nifty, but you can't use it
    ](http://fuhm.net/super-harmful/).
    It is further expanded in Michele Simionato
    [Things to Know About Python, Super Part 1
    ](http://www.artima.com/weblogs/viewpost.jsp?thread=236275),
    [Part2](http://www.artima.com/weblogs/viewpost.jsp?thread=236278),
    [Part 3](
    http://www.artima.com/weblogs/viewpost.jsp?thread=237121) _2008_.
-   Super is a lot easier in python3 where all classes are new-style.
    Raimond Hettinger in
    [Python’s super() considered super!
    ](http://rhettinger.wordpress.com/2011/05/26/super-considered-super/)
    _2011_ explains its use, with examples.

## Decorators {#decorators}

-   Bruce Eckel gives a very comprehensive tutorial to _decorators_ in his three articles:
    [Decorators I: Introduction to Python Decorators
    ](http://www.artima.com/weblogs/viewpost.jsp?thread=240808),
    [Python Decorators II: Decorator Arguments
    ](http://www.artima.com/weblogs/viewpost.jsp?thread=240845),
    [Python Decorators III: A Decorator-Based Build System
    ](http://www.artima.com/weblogs/viewpost.jsp?thread=241209) _2008_.<br />
    The [second tutorial](http://www.artima.com/weblogs/viewpost.jsp?thread=240845)
    teach the way to use decorators __without__ and __with__ arguments, the
    [third one](http://www.artima.com/weblogs/viewpost.jsp?thread=241209)
    is a case study.
-   [Decorators make magic easy
    ](http://www.ibm.com/developerworks/linux/library/l-cpdecor.html)
    by David Mertz.
-   [The decorator module]( http://micheles.googlecode.com/hg/decorator/documentation3.html)
    by Michele Simionato is a detailled explanation
    of the use and utility of decorators in recent python.
    It introduces the decorator module which help to define  new decorators.
-   [PEP 3129: Class Decorators](http://www.python.org/dev/peps/pep-3129/)
    extend the use of decorators to
    classes. Class decorators are available in python >= 2.6.
-   [Function Decorators
    ](http://programmingbits.pythonblogs.com/27_programmingbits/archive/50_function_decorators.html)
    and
    [More On Function Decorators
    ](http://programmingbits.pythonblogs.com/27_programmingbits/archive/51_more_on_function_decorators.html)
    _2009_ by Ariel Ortiz.

## Decorators Market
-   [PythonDecoratorLibrary](http://wiki.python.org/moin/PythonDecoratorLibrary)
    is a  central repository of decorator code pieces.
-   There are some articles about making a deprecation decorator:
    [Python decorator mini-study](http://muharem.wordpress.com/2006/10/18/3/),
    [How to decorate Python GIS code](http://sgillies.net/blog/858/how-to-decorate-python-gis-code/)
    _also about a logging decorator_,
    [Deprecation decorator](http://seewhatever.de/blog/?p=161).


## Descriptors {#descriptors}

-   [How-To Guide for Descriptors
    ](http://users.rcn.com/python/download/Descriptor.htm) _2003_
    by Raymond Hettinger, on this
    _difficult_ subject read also the end of
    [Python Elegance, Python Warts, Part2
    ](http://gnosis.cx/publish/programming/charming_python_b26.html) _2005_
    by David Mertz, this last paper shows how to define _instance_
    descriptors, most other examples are _class_ descriptors.
-   [Python Descriptors](http://www.informit.com/articles/printerfriendly.aspx?p=1309289) _2008_
    by Mark Summerfield is an introduction to descriptors
-   [Python Attributes and Methods
    ](http://www.cafepy.com/article/python_attributes_and_methods/python_attributes_and_methods.html)
    _2006_ by Shalabh Chaturvedi is a tutorial explaining the
    mechanics of object attribute access for new-style Python objects.
-   [Python 3k: datamodels: Customizing attribute access
    ](http://docs.python.org/3/reference/datamodel.html#customizing-attribute-access)
    details the attributes access and document both the `__getattr__`
    and the new `__getattribute__` method.
-   [Python 3k: datamodels: descriptors
    ](http://docs.python.org/3/reference/datamodel.html#descriptors)
    explains the difference between data descripors and non data descriptors,
    and how they override or not instance attributes.
-   [Python 3k: functions: property
    ](http://docs.python.org/3/library/functions.html#property)
    defines properties and the use of the `@property` decorator.

## Metaclasses {#metaclasses}

Metaclasses have changed in Python 3, so be careful of tweaking the syntax of the Python 2 recipes.
I include only references on the python 3 metaclasses

-   Wikipedia: {{< wp "Metaclass" >}}
-   [Metaclasses in Python 3000 (pep 3115)](
    http://www.python.org/dev/peps/pep-3115/) _2007_.
-   [Metaclasses in Python 3.0 part I](http://www.artima.com/weblogs/viewpost.jsp?thread=236234)
    and
    [Part II](http://www.artima.com/weblogs/viewpost.jsp?thread=236260) _2008_
    by Michele Simionato
-   [Python 3 primer, Part 2: Advanced topics Metaclasses, decorators,
     and other strange creatures
    ](http://www.ibm.com/developerworks/library/l-python3-2/)
    by Cesar Otero, in _ibm developerworks_.
-   [Python 3 Patterns, Recipes and Idioms: Metaprogramming
    ](http://python-3-patterns-idioms-test.readthedocs.org/en/latest/Metaprogramming.html)

## {{< wp "Aspect-oriented programming" >}}
{{< wp "Aspect-oriented programming" >}} includes also {{< iref "#metaclasses" "Metaprogramming" >}}

-   {{< wp "Aspect-oriented programming" >}} is available in Python3 with the library
    [pylities](http://pypi.python.org/pypi/pytilities/), read the [pylities Manual](http://pytilities.sourceforge.net/doc/1.2.0/)


## {{< wp "Design by contract" >}}

{{< wp "Design by contract" >}} define formal, precise and verifiable interface specifications for software components, which extend the ordinary definition of abstract data types with preconditions, postconditions and invariants. These specifications are referred to as "contracts".
The concept of design by contract as been first deployed with the language _Eiffel_ and you will find introductions and material to use this paradigm in the [Eiffel: design by contract](lhttp://www.eiffel.com/developers/design_by_contract.html) page.

The [PEP 316- Programming by Contract for Python
](https://www.python.org/dev/peps/pep-0316/) is implemented by the library
[contract](http://pypi.python.org/pypi/contract/) which is not updated
since 2007.

The library [PyContracts](https://pypi.python.org/pypi/PyContracts)
is a more recent attempt using decorators to implement contracts in Python.

## {{< wp "Design Patterns" >}} in Python
-   [Thinking in Python](http://www.mindview.net/Books/TIPython/)
    by Bruce Eckel is a book focused on design patterns in Python,
    available on-line at
    [jamesthornton.com eckel books page
    ](http://jamesthornton.com/eckel/TIPython/html/Index.htm) _2002_
-   [Python 3 Patterns, Recipes and Idioms
    ](http://python-3-patterns-idioms-test.readthedocs.org/en/latest/)
    _2008_ by Bruce Eckels and als. Open source downloadable book in
    [Bruce Eckels Bitbucket repository
    ](https://bitbucket.org/BruceEckel/python-3-patterns-idioms/)
-   [Data Structures and Algorithms with Object-Oriented Design Patterns in Python
    ](http://www.brpreiss.com/books/opus7/html/book.html) _2004_
    by Bruno R. Preiss.
-   [Building Skills in OO design
    ](http://www.itmaybeahack.com/homepage/books/oodesign.html)
    by Steven F. Lott (Creative Commons License) is a sequence of
    exercises in OO design _it is not a manual_, the book has two editions
    which differ by the programming examples. One is for _Java_ the
    other one is
    [Building Skills in Object-Oriented Design with Python
    ](http://buildingskills.itmaybeahack.com/book/oodesign-python-2.2/html/index.html).
-   [Introduction to Programming using Python chap 19
    ](http://www.pasteur.fr/formation/infobio/python/ch19s06.html)
    a book from Catherine Letondal & al.
-   [Design patterns in Python](http://www.testingperspective.com/?page_id=1941)
    an online book by Rahul Verma and Chetan Giridhar. _In 2013 all
    links are broken, either at the given page or one of the many
    pages refering  to it._
-   [pypatterns](https://pypi.python.org/pypi/pypatterns/)
    by michael j pan, give generic examples of the patterns: _command_ and
    _filter_.



## Polymorphism

Python is a dynamically typed language, polymorphism in dynamically
and statically typed languages is described in
[Wikipedia Polymorphism in object-oriented
programming](http://en.wikipedia.org/wiki/Polymorphism_in_object-oriented_programming#Python).

It his book [Building Skills in Python](http://homepage.mac.com/s_lott/books/python/htmlchunks/ "homepage.mac.com/s_lott books/python") Steven F. Lott
[introduces python polymorphism](http://homepage.mac.com/s_lott/books/python/htmlchunks/ch22s02.html "homepage.mac.com/s_lott ch22s02.html").

The polymorphism in python is on the class of the object on which the method is called. We cannot use operator
overloading
to solve polymorphism on other arguments as we can do in a statycally strong typing language as C++.
This asymmetry is pointed out by David Merz in his  article
[Multiple Dispatch Generalizing Polymorphism with Multimethods
](http://gnosis.cx/publish/programming/charming_python_b12.html).

[Multiple dispatch (wikipedia)](http://en.wikipedia.org/wiki/Multiple_dispatch)
differ from overloading in that the called function is choosed based on the run time dynamic type and not on a compiled
type computed static type.
[Multiple dispatch in python](http://en.wikipedia.org/wiki/Multiple_dispatch#Python)
uses library extension as described in the previous article of David
Merz or the _multimethod decorator_ described buy
Guido van van Rossum in his article
[Five-minute Multimethods in Python](http://www.artima.com/weblogs/viewpost.jsp?thread=101605").

There are many packages to implement multiple dispatch:
[pymultimethods](http://sourceforge.net/projects/pymultimethods/),
[multimethods](http://pypi.python.org/pypi/multimethod/),
[PEAK-Rules](http://pypi.python.org/pypi/PEAK-Rules).

Note that use of multiple dispatch can imply the use of _isinstance_ that adepts of Duck Typing
[consider harmful](http://www.canonical.org/~kragen/isinstance/)


# Python idioms
## __with__ construct

The usage of the with statement is often quite confusing, and most people use it only to open files `with open('somefile') as file:`. But is is a lot more powerfull than only aimed at cleanly close files.

We have first to read the [Python language documentation
](http://docs.python.org/reference/compound_stmts.html#the-with-statement)
without forgetting [context managers
](http://docs.python.org/reference/datamodel.html#context-managers).

A first very useful tutorial is composed of articles of Frederik
Lundh:
[The with statement](http://effbot.org/pyref/with.htm),
[With Statement Contexts and Context Managers
](http://effbot.org/pyref/context-managers.htm),
the main one being
[Understanding Python's "with" statement
](http://effbot.org/zone/python-with-statement.htm)
wich offers comprehensive examples.

The main reference is [PEP 343: The "with" Statement
](http://www.python.org/dev/peps/pep-0343/) it is itself very detailed
and offers many useful examples.

As the main task is to define context managers you may want to use the
[contextlib module](http://docs.python.org/library/contextlib.html)
see also Doug Hellmann tutorial
[contextlib – Context manager utilities
](https://pymotw.com/3/contextlib/index.html)

# Network Programming

See also [Network Libraries](python_libraries#network_libs "Internal reference")
{{< iref "python_web#wsgi" "WSGI" >}}
and {{< iref "python_web" "Web frameworks" >}}

## Net
-   [Socket Programming HOWTO](http://docs.python.org/dev/howto/sockets.html)
    by Gordon McMillan.
-   The Daniel Zappala tutorial
    [Python Network Programming](http://ilab.cs.byu.edu/python/)
-   [Network Protocols
    ](http://www.effbot.org/librarybook/network-protocols-index.htm)
    in
    [the effbot.org guide to The Standard Python Library](http://www.effbot.org/librarybook/)
    gives some examples of use of the network modules from the standard
    library.

# Unit Tests {#python_unit_tests}
This is the __Python__ Unit Test section; an other page deals with
the non language specific, software design idiom of
{{< iref "software_design#unit_tests" "Unit Tests" >}}.

-   [Python testing tools taxonomy](http://wiki.python.org/moin/PythonTestingToolsTaxonomy)
    is the python wiki index of  testing tools.
-   [Agile Testing Articles and Tutorials](http://pycheesecake.org/wiki/AgileTestingArticlesAndTutorials)
    contains links to articles and tutorials (mainly using python)
    from Grig Gheorghiu's
    [Agile Testing Blog](http://agiletesting.blogspot.com/).
-   [Cheesecake project](http://www.pycheesecake.org/wiki/)
    is aimed as python package quality assurance and quality
    measurement. Cheesecake use nose for automatic testing, and require
    pylint and setuptools.
-   [Dive Into Python3](http://getpython3.com/diveintopython3/) by
    Mark Pilgrim has a
    [chapter on unit testing](http://getpython3.com/diveintopython3/unit-testing.html)
    which is a very good tutorial.


We  consider three ways of testing: _doctest_, _unit tests_ and _Mock objects_.
There are packages for these three validations methods in the
{{< iref "python_libraries#modules" "standard library modules" >}}
and in Pypi packages.

A [doctest](http://en.wikipedia.org/wiki/Doctest "Wikipedia page")
allows the generation of tests based on output from the
standard Python interpreter shell, cut and pasted into docstrings.
It searches for pieces of text that look like interactive Python
sessions, and then executes those sessions to verify that they work
exactly as shown. The library reference includes the
{{< iref  "python_libraries#doctest" "doctest module" >}}

{{< wp "Unit Test" >}} are helped by the module
{{< iref "python_libraries#unittest" "UnitTest" >}}

Since python 3.3 there is a new module for {{< wp "Mock Objects" >}}:
{{< iref "python_libraries#unittest" "unittest.mock" >}}.

The other libraries are under the section
{{< iref "python_libraries#test_libs" "Test Libraries" >}}.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
