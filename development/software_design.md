---
title: Software Design
---

# General References

-   [The Architecture of Open Source Applications (aosabook)
    ](http://aosabook.org/en/index.html), the volume I and II are available on-line.
    The [Aosabook GitHub repository
    ](https://github.com/aosabook) contains their source and the new
    [source of 500 Lines or Less](https://github.com/aosabook/500lines)

# Programming Paradigms

# Design patterns
-   [Wikipedia: Design Pattern](http://en.wikipedia.org/wiki/Design_pattern_(computer_science))
    contains definition, and links to this field as long as an
    {{< wp "Design_pattern_(computer_science)#Classification_and_list"  "index of patterns" >}}.
-   The Wikipedia Page
    [Design Pattern (gang of four)](http://en.wikipedia.org/wiki/Design_Patterns)
    detail with references to sub-pages each pattern of the book by
    Gamma et al.
-   The use of design patterns in Python is described
    {{< iref "python/python_programming" "in the Python page" >}}

## Agile methods
-   Wikipedia: {{< wp "Agile software development" >}},
    {{< wp "Scrum_(software_development)"  "Scrum" >}}
-   {{< wp "Extreme_programming"  "Wikipedia: Extreme Programming" >}}
    {{< wp "Extreme programming practices" >}} and
    {{< wp "Extreme project management" >}}
-   [Extreme Programming Roadmap](http://c2.com/cgi/wiki?ExtremeProgrammingRoadmap) at c2.com
-   Ron Jeffries' blog [Category XProgramming](http://www.xprogramming.com/)


# Project management
-   Wikipedia: {{< wp "Project management software" >}},
    {{< wp "Project management" >}},
    {{< wp "Project planning" >}},
    {{< wp "Comparison of project management software" >}}
-   [TaskJuggler]( http://www.taskjuggler.org/)  (GPL) is a  project management software.
    Version 2 is programmed in C++ using the Qt toolkit and KDE libraries.
    TaskJuggler III is completely re-implemented  in ruby.<br />
    -   [Creating Gantt charts by Exporting to TaskJuggler
        ](http://orgmode.org/worg/org-tutorials/org-taskjuggler.html)
        export from {{< iref "org-mode" "Org Mode" >}} to _TaskJuggler_.
    -   [emacs taskjuggler-mode for editing taskjuggler tasks
    ](http://www.skamphausen.de/cgi-bin/ska/taskjuggler-mode)
-   [Project Planning with org-mode
    ](http://www.contextualdevelopment.com/articles/2008/project-planning)
    by Peter Jones.

# Continuous Integration {#continuous_integration}
A concept closely related to {{< wp "Continuous integration" >}} is {{< wp "DevOps" >}}
_(DEVelopement & OPerationS)_ they both prone automation and monitoring
at all steps of software construction, from building, integration,
testing, releasing, deployment and infrastructure management.


{{< wp "Build automation" >}} refer to the process of compiling, testing and packaging.
This term was coined to refer to the process traditionally handled by _Make_ and
_Autotools_ for programs in language C. _Continuous Integration_ _(CI)_ is a more recent
concept which came with the development of source control. We can see _Build automation_
as a lower level part of _CI_, we hold this view in these pages, but some people
classify _CI_ as a _build automation_ category!

See also {{< iref "python/python_libraries#build_automation" "Build Automation" >}}
in  {{< iref "python/python_libraries" "Python Libraries section" >}}.

## CI Software

-   Wikipedia  {{< wp "Continuous integration" >}},
    {{< wp "Category:Continuous integration" >}}.
-   Wikipedia {{< wp "List of build automation software" >}},
    {{< wp "Category:Build automation" >}}
-   [Awesome DevOps](https://github.com/joubertredrat/awesome-devops)
    listov DevOps Resources.
-   [Awesome Continuous Integration and Continuous Delivery
    ](https://github.com/ciandcd/awesome-ciandcd)
-   [Stackify: list of Continuous integration tools
    ](https://stackify.com/top-continuous-integration-tools/)
    _mars 2017_.
-   [CI/CD Tools Comparison - DigitalOcean
    ](https://www.digitalocean.com/community/tutorials/ci-cd-tools-comparison-jenkins-gitlab-ci-buildbot-drone-and-concourse),
    compare  GitLab CI, Buildbot, Drone, and Concourse.
-   {{< wp "Buddy_(software)"  "Buddy" >}} (private license)
    is a web-based and self-hosted
    continuous integration and delivery software for Git.
    There is a cloud version and an on premise version _Buddy Go_
    that  employs Docker containers. There is a free cloud plan with 5
    projects and 120 runs/month.
    -   [Buddy Home](https://buddy.works/)
-   {{< wp "Jenkins_(software)"  "Jenkins" >}} (MIT License)
    is a java continuous integration server.  It supports SCM tools
    including CVS, Subversion, Git, Mercurial, Perforce and
    Clearcase. Jenkins is langage agnostic.  Jenkins is available in
    Debian.
    -   [Jenkins Home](http://jenkins-ci.org/)
        -   [Butler](https://github.com/AshtonKem/Butler) (GPL)
        is an Emacs Integration for Jenkins.
    -   [Jenkins and Python
        ](http://www.alexconrad.org/2011/10/jenkins-and-python.html)
        by Alex Conrad.
    -   Numerous Python [packages for Jenkins integration
        ](https://pypi.python.org/pypi?%3Aaction=search&term=jenkins&submit=search)
        are available in [PyPi](https://pypi.python.org/pypi).
-   {{< wp "Travis CI" >}}) (MIT license)
    is a hosted continuous integration service written in ruby
    integrated with GitHub, it support many languages
    [including python
    ](http://docs.travis-ci.com/user/languages/python/).
    -   [Tavis CI (open source)](https://travis-ci.org/)
    -   [Travis CI](http://docs.travis-ci.com/)
    -   [Travis CI on GitHub](https://github.com/travis-ci/travis-ci)

## Build Automation
Many python build automation software (_scons_, _buildout_, _paver_, _pybuilder_,
_doit_, _redo_, _waf_) are described in the
{{< iref "python/python_libraries#build_automation" "Build Automation sction" >}}
of the  {{< iref "python/python_libraries" "Python Libraries Page" >}}.

-   {{< wp "Make_(software)" Make >}} is the the most widespread build automation tool,
    it is included in every Unix System.
    -   [GNU Make Home](https://www.gnu.org/software/make/)
    -   [GNU Make Documentation
        ](https://www.gnu.org/software/make/manual/html_node/index.html)
-   [Remake](http://bashdb.sourceforge.net/remake/) (GPL 3.0)
    is an enhanced version of GNU Make with  improved error reporting, better tracing,
    profiling and a debugger. _Remake is in Debian._
    -   [Remake - GitHub](https://github.com/rocky/remake)
    -   [Remake Documentation](https://remake.readthedocs.io/en/latest/)
    -   [Remake Wiki](https://github.com/rocky/remake/wiki)
-   [CMake](https://cmake.org/) (BSD 3-clause License)
    is a family of tools designed to build, test and package software. CMake use
    platform and compiler independent configuration files, and generate native makefiles
    and workspaces that can be used in the compiler environment of your choice.
    _CMake is in Debian._
    -   [CMake Documentation](https://cmake.org/cmake/help/latest/)
-   [Ninja](https://ninja-build.org/) (Apache-2.0 License)
    is a small build system, designed to have its input files generated by a
    higher-level build system _such as Cmake_, and run builds as fast as possible.
    _Ninja is in Debian._

# UML

## UML References

-   Wikipedia: {{< wp "Unified Modeling Language" >}}, {{< wp "List of UML tools" >}},
    {{< wp "Class diagram" >}}, {{< wp "Activity diagram" >}},
    {{< wp "Use Case Diagram" >}}, {{< wp "Sequence diagram" >}}
-   [OMG: UML Resource Page](http://www.uml.org/)
-   [uml-diagrams.org](http://www.uml-diagrams.org/)
     Everything about the last specification of UML, diagram by diagram.
-   [UML basics: The sequence diagram
    ](http://www.ibm.com/developerworks/rational/library/3101.html) and
    [UML basics: The class diagram: An introduction to structure diagrams in UML 2
    ](http://www.ibm.com/developerworks/rational/library/content/RationalEdge/sep04/bell/)
    by Donald Bell in IBM developerWorks _2004_.
-   [SparxSystems: UML Tutorial I](http://www.sparxsystems.com/uml-tutorial.html),
    [UML 2 Tutorial](http://www.sparxsystems.com/resources/uml2_tutorial/)

## UML Tools
-   [ArgoUml](http://argouml.tigris.org)
    *(Eclipse Public License)* is a Java based UML tool for UML 1.4. It it has the
    ability to reverse engineer compiling Java code and generate UML
    diagrams for it. ArgoUml export XMI files containing models.
    -   [ArgoUml-Python](http://argouml-python.tigris.org/) adds support for python to argouml.
    -   [ArgoUml-Graphviz](http://argouml-graphviz.tigris.org/) uses graphviz to position and
        postprocess UML diagrams produced by ArgoUml.
-   [Blockdiag](http://blockdiag.com/en/index.html) is a set of graph generators
    from text source similar to {{< iref "#graphviz" "graphviz" >}}’s `dot` format.
    It includes  block diagrams, sequence diagrams,  activity diagrams, and network diagrams.<br />
    In the [sphinx contribs](https://bitbucket.org/birkenfeld/sphinx-contrib)
    there is a {{< iref "rest#sphinx" "Sphinx" >}} extension for _Blockdiag_.
-   [Bouml](http://www.bouml.fr/) previously GPL has now a private licence.
-   [Dia](http://projects.gnome.org/dia/docs.html) supports UML Class and activity diagrams.
-   [Dia Links](http://projects.gnome.org/dia/links.html) gives Dia extensions,
    including some UML related ones
-   [dia2code](http://dia2code.sourceforge.net/)(GPL) reads a
    [Dia](http://www.gnome.org/projects/dia/) diagram file that
    contains an UML class diagram and creates files in the language of
    choice that contain the bare bones of the classes represented in
    the diagram. It supports Ada, C, C++, Java, PHP, PHP5, Python,
    Ruby, shapefile, SQL and C\#. It is packaged in Debian.
-   {{< wp "Graphviz" >}} {{< wp "DOT language" >}} can be used to draw UML diagrams,
    either by hand as described in
    [UML Diagrams Using Graphviz Dot](http://www.ffnn.nl/pages/articles/media/uml-diagrams-using-graphviz-dot.php)
    or as output of many tools of this page.
-   [Gaphor](http://gaphor.sourceforge.net/) (GPL) is a UML 2.0
    tool for gnome written in python. It supports diagrams for classes, use cases,
    Actions, and Components. It can export to xmi, svg and pdf. Reverse
    engineering is available for python,.
-   [PlantUml](http://plantuml.sourceforge.net/) (GPL) is a java tool that allow to draw all java diagrams
     _sequence, use case, class, activity, component, state, object_.
    PlantUml uses Graphviz and it can be used in Sphinx with  the
    [plan Uml Extension](https://bitbucket.org/birkenfeld/sphinx-contrib/src).
-   [Pyreverse](http://www.logilab.org/blogentry/6883)
    extracts UML class diagrams and package dependencies from python code.
    it is now included in [Pylint](http://www.pylint.org/).
-   [Pyut](http://sourceforge.net/projects/pyut/) (GPL) UML1.3
    class diagram editor with support for input and output plug-ins.
    Export to XML, JPEG, BMP and PS...; import from Java, Python, XSD,
    DTD....The features looks great, alas as far as v1.4 it crashed
    before I could truly use it! _Pyut seems to be stalled at v 1.4
    2006_
-   [PyWebUml](http://pypi.python.org/pypi/pywebuml/)(BSD License)
    is a python program that will parse c#, java or python files,
    and generate the UML class diagram using a web interface.
-   [Quick Sequence Diagram Editor](http://sdedit.sourceforge.net/)
    (BSD license) is a tool for creating UML sequence
    diagrams from textual descriptions of objects and messages.
    It can be used in Sphinx with  the
    [sdedit  Extension](https://bitbucket.org/birkenfeld/sphinx-contrib/src).
-   [Umbrello](http://uml.sourceforge.net/) (GPL) is a UML diagram
    programme for KDE. It has only with basic kde dependencies, so with
    proper configuration options I use it without a full kde
    environment. Umbrello can generate code in C++, Java, JavaScript,
    ActionScript, SQL, Ruby, Python, PHP, Ada, IDL XML Schema, Perl and
    import code from C++, Java, Ada and Python There is a
    [French Umbrello wiki](http://umbrello.tuxfamily.org/doku.php).
-   [yUML](http://yuml.me/) is an online tool to create UML diagrams.

# Unit Tests

Python has its own page
{{< iref "python/python_programming#python_unit_tests" "Unit tests in python" >}}

-   [Kent Beck seminal paper on unit testing](http://www.xprogramming.com/testfram.htm)
-   {{< wp "Unit_testing"  "Unit testing" >}} is is an essential step of
    {{< wp "Software testing" >}} before {{< wp "Integration testing" >}}
-   {{< wp "Extreme Programming" >}} is a technic of {{< wp "test driven development" >}}
    and  use unit tests as an early step, and {{< wp "Acceptance Tests" >}} are used for
    {{< wp "Integration testing" >}}.
-   [Awesome Testing](https://github.com/TheJambo/awesome-testing)
    a list of resources for software testing.
-   [Awesome Test Automation
    ](https://github.com/atinfo/awesome-test-automation)
-   [Awesome Visual Regression Testing
    ](https://github.com/mojoaxel/awesome-regression-testing)
    Resources on Regression Testing *ensures changes did not break
    the functionality or style.*
-   [Ron Jeffries'Blog](http://ronjeffries.com/)
    has many
    links on testing framework in the categories
    [Software](http://ronjeffries.com/xprog/software/),
    [Agile Methods](http://ronjeffries.com/categories/agile-related/),
    [XProgramming](http://ronjeffries.com/categories/xprogramming/).
-   [Testing Framework wiki](http://c2.com/cgi/wiki?TestingFramework)
-   {{< wp "Test double" >}} is a term coined to reference differents technics to use
    objects or procedures that look and behave like their release-intended
    counterparts. It is used in the popular paper of Martin Fowler:
    [Mocks Aren't Stubs](http://martinfowler.com/articles/mocksArentStubs.html).
-   {{< wp "Mock object" >}} are simulated objects that mimic the behavior of real
    objects in controlled ways.  They allow to incorporate into a unit test complex, a
    fake object when real objects would beimpossible to use directly.
    -   [Testing Framework wiki: Mock Object Page](http://c2.com/cgi/wiki?MockObject)
    -   For python look at the section
        {{< iref "python/python_libraries#mock_objects" "Mock objects Libraries" >}}.
-   [junit](http://www.junit.org/index.htm) java testing framework.
-   [cppunit](http://cppunit.sourceforge.net/)

# Miscellaneous graphing tools

-   [Railroad Diagram Generator](http://railroad.my28msec.com/rr/ui)
    is an online tool for creating SVG {{< wp "syntax diagrams" >}}, also known as
    railroad diagrams, from context-free grammars specified in EBNF.

# Websocket
-   {{< wp "WebSocket" >}} is a protocol providing full-duplex communication
    channels over a single TCP connection.
-   __PubSub__ or {{< wp "publish subscribe" >}} is a messaging pattern where
    publishers (senders) characterize published messages into classes
    without knowledge of which subscribers (receivers) there may
    be. Similarly, subscribers subscribe to one or more classes
    without knowledge of publishers.
-   {{< wp "Web Application Messaging Protocol" >}} WAMP is a WebSocket
    subprotocol registered at IANA, to offer routed RPC and PubSub.
-   [Wamp Proto Home](http://wamp-proto.org/),
    [Wamp Proto comparison](http://wamp-proto.org/compared/).
-   {{< wp "Web_Application_Messaging_Protocol#Comparison"  "Wikipedia Wamp Comparison" >}}
    with other protocols.
-   [REST vs WebSocket Comparison
    ](http://blog.arungupta.me/rest-vs-websocket-comparison-benchmarks/)
-   [pubnub.com: WebSockets vs REST: Understanding the Difference
    ](https://www.pubnub.com/blog/2015-01-05-websockets-vs-rest-api-understanding-the-difference/)
-   [Crossbar.io](http://crossbar.io/)
    is an open-source message router for the WAMP
    protocol that runs on-premise, in the cloud or embedded in
    devices. It enables unified real-time communication between
    application components and devices in IoT, mobile and Web
    applications.
-   [Sam & Max: Crossbar, le futur des applications Web Python ?
    ](http://sametmax.com/crossbar-le-futur-des-applications-web-python/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
