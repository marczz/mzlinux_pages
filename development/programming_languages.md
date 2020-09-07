---
title: Programming Languages
---

See also {{< iref "source_code" "Source code beautifiers" >}}.

---

# General References

More references on  Wikipedia:

-   {{< wp "List of programming languages" >}}
-   {{< wp "List of programming languages by type" >}}
-   {{< wp "Comparison of programming languages" >}}
-   {{< wp "List of object-oriented programming languages" >}}
-   {{< wp "Category:Object-oriented programming languages" >}}
-   {{< wp "List of JVM languages" >}}.
-   {{< wp "List of concurrent and parallel programming languages" >}}
-   {{< wp "List of programming languages for artificial intelligence" >}}
-   {{< wp "Category:Functional languages" >}}
-   {{< wp "Category:Compiling tools" >}}
-   {{< wp "Category:Unix programming tools" >}}

-   [Rosetta Code](http://rosettacode.org)
    present solutions to the same task in as many different languages
    as possible, Rosetta Code currently has 771 tasks, 163 draft
    tasks, and is aware of 576 languages, though we do not (and
    cannot) have solutions to every task in every language.
-   Arch Wiki Categories:
    [Programing languages
    ](https://wiki.archlinux.org/index.php/Category:Programming_languages)
    and [Package development
    ](https://wiki.archlinux.org/index.php/Category:Package_development)
-   [List of languages that compile to JS · coffeescript Wiki
    ](https://github.com/jashkenas/coffeescript/wiki/List-of-languages-that-compile-to-JS)
-   There are many *awesome* lists relative to languages, some are
    referenced below but there are two lists of *awesome lists*
    [awesome-awesomeness
    ](https://github.com/bayandin/awesome-awesomeness) and
    [awesome](https://github.com/sindresorhus/awesome).

# Programming Paradigms
I mention only some paradigms look at
{{< wp "programming paradigms"  "Wikipedia: programming paradigms" >}} for a full
list.

-   {{< wp "Comparison of programming paradigms" >}}
-   {{< wp "Category:Programming paradigms" >}}

{{< wp "Constraint Programming" >}}
:   is a form of declarative programming,
    where relations between variables are stated in the form of
    constraints. Constraints do not specify a step or sequence of
    steps to execute, but rather the properties of a solution to be
    found. Constraint programming can be expressed in the form of
    {{< wp "constraint logic programming" >}} like in prolog, or realized in
    imperative programming via a separate library. There are
    constraints library for all major programming languages
    ( [List in Wikipedia
    ](https://en.wikipedia.org/wiki/Constraint_programming#Constraint_programming_libraries_for_imperative_programming_languages))

{{< wp "Declarative programming" >}}
:   is a style of building computer
    programs, that expresses the logic of a computation without
    describing its control flow. It is an umbrella for
    many other paradigms, Constraint programming,
    Domain-specific languages, Functional programming,
    Hybrid languages, Logic programming, Modeling

{{< wp "Functional programming" >}}
:   is a declarative programming which
    treats computation as the evaluation of mathematical functions and
    avoids changing-state and mutable data.
    Among functional programming languages whe find Common Lisp,
    Scheme, Clojure, Racket,Erlang, OCaml, Haskell.
    A language is {{< wp "purely functional" >}} if it guarantees the (weak)
    equivalence of {{< wp "call-by-name" >}}, {{< wp "call-by-value" >}} and
    {{< wp "call-by-need" >}}, often by excluding updates of entities
    in the program's {{< wp "runtime system" >}}.
    Variables are used in a mathematical sense, with identifiers
    referring to immutable, persistent values.

{{< wp "Metaprogramming" >}}
:   is the writing of computer programs with the
    ability to treat programs as their data. It means that a program
    could be designed to read, generate, analyse or transform other
    programs, and even modify itself while running.

    It includes:

    -   {{< wp "Template metaprogramming" >}} like in C++ or D;
    -   {{< wp "Reflection_(computer_programming)"  "reflective programming" >}}
        i.e. the ability of a computer program to examine _type
        introspection_ and modify its' structure and behavior at runtime.
        this feature is present in many languages like ECMAScript, clojure,
        Java, lisp, Objective-C, Perl, PHP, Python, R, Ruby, scheme ...

{{< wp "Object-oriented programming" >}} (OOP)
:   is a paradigm based on the
    concept of {{< wp "objects" >}}, which are {{< wp "data structures" >}} that contain
    data, in the form of fields, known as attributes; and code, in the
    form of procedures, known as methods.  An object's procedures can
    access and often modify the attributes of the object with which
    they are associated (objects have a notion of "this"). Most
    popular OOP languages are {{< wp "class-based" >}}, meaning that objects are
    instances of classes, which also determines their type.  Most OOP
    language combines OOP with {{< wp "imperative" >}},
    {{< wp "procedural programming" >}}.  Significant object-oriented languages
    include Python, C++, Objective-C, Smalltalk, Delphi, Java, C#,
    Perl, Ruby and PHP.

{{< wp "Polymorphism (computer science)"  "Polymorphism" >}}
:   is the provision
    of a single interface to entities of different types.
    -   If a function denotes different and potentially heterogeneous
        implementations depending on a limited range of individually
        specified types and combinations, it is called
        {{< wp "ad hoc polymorphism" >}}. Ad hoc polymorphism is supported in
        many languages using {{< wp "function overloading" >}}.
    -   If the code can be used transparently with any number of new
        types, it is called {{< wp "parametric polymorphism" >}}. In the
        object-oriented programming community, this is often known as
        {{< wp "generic programming" >}}. In the functional programming
        community, this is often simply called polymorphism.
    -   {{< wp "Subtyping" >}} (or inclusion polymorphism) is a concept wherein a
        name may denote instances of many different classes as long as
        they are related by some common superclass.[3] In
        object-oriented programming, this is often referred to simply
        as polymorphism.

{{< wp "Reflection (computer programming)"  "Reflection" >}}
:   reflection is the ability of a computer program to examine (see
    {{< wp "type introspection" >}}) and modify the structure and behavior
    (specifically the values, meta-data, properties and functions) of
    the program at runtime.

    The [:Reflection (computer programming)#Examples|Wikipedia page]
    gives examples of reflection in ECMAScript, Java, Objective-C,
    Perl, PHP, Python, R, Ruby.

{{< wp "Type inference" >}}
:   refers to the automatic deduction of the data type of an
    expression. If some, but not all, {{< wp "type annotations" >}} are already
    present it is referred to as type reconstruction.

    It is a feature present in some strongly statically typed
    languages. It is often characteristic of, but not limited to,
    functional programming languages in general. Some languages that
    include type inference are ML, OCaml, F#, Haskell, Scala, D,
    Clean, Opa, Rust, Swift, Visual Basic (starting with version 9.0),
    C# and C++11.

# Language benchmarks
-   [kostya/benchmarks · GitHub](https://github.com/kostya/benchmarks)
    is a benchmark for Nim Clang, Nim Gcc, C++, D Ldc, Crystal, Go, D,
    D Gdc, Julia, Javascript V8, Rust, Scala, Go Gcc, Javascript Node,
    C# Mono, Python Pypy, Ruby JRuby, Ruby Topaz, Ruby, Ruby JRuby9k,
    Python, Ruby Rbx.

    Concerning speed for most test Nim Clang is among the best in the
    same group than C++/D nearly with twice the Rust speed, _except
    matmult where the are ex aequo_, Go is  sometime better than Rust,
    most often worse, always slower than Nim Clang.

    For resident memory size, the results are varying from test to
    test.
-   [attractivechaos/plb · GitHub
    ](https://github.com/attractivechaos/plb/pulse)
    is a benchmark made in 2011 with only classical langages: C, C#,
    D, Go, Java, javascript, Lua, Perl, Python (2, 3, Jython), R,
    Ruby.
    There is a [page of results
    ](http://attractivechaos.github.io/plb/)

# Language comparisons {#language_comparison}
They compare {{< iref "#rust" "Rust" >}}, {{< iref "#golang" "Go" >}} and
{{< iref "#nim" Nim >}}.

-   [Of  Rust, D, Go and Nim, which is the strongest language and why? - Quora
    ](http://www.quora.com/Of-the-emerging-systems-languages-Rust-D-Go-and-Nim-which-is-the-strongest-language-and-why)
-   an Interview with Steve Klabnik:
    [How Rust Compares to Other Languages
    ](https://www.codementor.io/rust/tutorial/steve-klabnik-rust-vs-c-go-ocaml-erlang)
    He thinks that Rust should replace C++ for system programming,
    compared to ocaml or haskell rust is s not full-blown functional
    language; he compares also Rust with Go and Erlang.
-   [Rust vs Go
    ](https://jaredforsyth.com/posts/rust-vs-go/) _2014_
    concludes that Go win on stability, active community and strong
    standard library. Rust win for the type system and the memory
    management and  functional programming.
-   [A Quick Comparison of Nim vs. Rust
    ](http://arthurtw.github.io/2015/01/12/quick-comparison-nim-vs-rust.html)
    _2015_
    compare two simple examples written in Nim and Rust _with the full
    source code_, the rough
    execution time comparison, and the impressions of coding in both.
    These two examples show a slightly faster Rust than Nim. The blog
    summarizes the main difference like this:

    Nim’s strengths:
    -   Productivity,  Ease of learning, Scripting in a compiled
        language, good for prototyping, interactive exploration,
        batch processing etc.
    -   Language features: method overloading, new operator
        definition,  named arguments, default values,
        powerful compile-time coding

    Rust’s strengths:
    -   A true systems programming language: embeddable, GC-free and bare metal
    -   Safety, correctness, runtime reliability
    -   Language features: pattern matching (excellent!), enum variants,
        let mut instead of var,  powerful destructuring syntax
-   Will Yager [Why Go Is Not Good](http://yager.io/programming/go.html)
    point out many defects of Go by comparing it to Rust Haskell,
    Python: mediocre type system, bad support
    for generic programming, no support operator overloading or
    keyword extensibility, bad failure handling instead of a clean
    algebraic types and type-safe failure modes, bad type inference,
    no support immutability declarations, Go is not suitable for
    programming embedded systems.
-   [How do Rust and Go compare?
    ](https://www.quora.com/How-do-Rust-and-Go-compare-1).
-   Göran Krampe [I missed Nim - Roads Less Taken
    ](http://goran.krampe.se/2014/10/20/i-missed-nim/) gives a
    comparison of Nim with Julia, Go, Rust _2014_
-   [We switched from Rust to Nim for a very large proprietary project
    ](https://news.ycombinator.com/item?id=9050114)
    while not being a comparison, gives some elements on language
    choice for a system project.
-   [5 Programming Languages You Should Really Try
    ](http://www.bradcypert.com/2017/06/28/5-programming-languages-you-could-learn-from/)
    by Brad Cypert _2017_ Nim, Go, F#, Rust Clojure.

# ATS
{{< wp "ATS_(programming_language)" "ATS" >}} is a derivative of Ocaml that focus on
theorem proving support.  ATS is very quick, a lot better than Ocaml and Haskell, and
comparable to C cf. [The  benchmarks game](http://shootout.alioth.debian.org/)

#  C programming Language
-   Wikipedia: {{< wp "C (programming language)"  "C programming language" >}}
    [C syntax](http://en.wikipedia.org/wiki/C_syntax),
    {{< wp "C preprocessor" >}}.
-   A wikibook :
    [C Programming](http://en.wikibooks.org/wiki/C_Programming)
    (GNU FDL)
-   The book
    [The New C Standard](http://www.knosof.co.uk/cbook/cbook.html)
    available in pdf is a detailed analysis of the International
    Standard C99 for the C language.
-   [Notes to Accompany *The (K&R) C Programming Language
    ](http://www.eskimo.com/~scs/cclass/krnotes/top.html),
    [Introductory C Programming Class Notes
    ](http://www.eskimo.com/~scs/cclass/notes/top.html)
    and
    [Intermediate C Programming Class Notes
    ](http://www.eskimo.com/~scs/cclass/int/top.html)
    by Steve Summit who also gives
    [Introductory](http://www.eskimo.com/~scs/cclass/asgn.beg/index.html)
    and
    [Intermediate C Programming -- Assignments
    ](http://www.eskimo.com/~scs/cclass/asgn.int/index.html).
-   [comp.lang.c Frequently Asked Questions](http://c-faq.com/)
    and Peter Seebach's
    [infrequently asked questions](http://www.seebs.net/faqs/c-iaq.html).
-   [C cheatsheet — csheeet](http://www.csheeet.com/en/latest/)
    built in Sphinx from the
    [Source on GitHub](https://github.com/crazyguitar/csheeet).
-   [Splint](http://splint.org/) (GPL) is a tool for
    statically checking C programs for security vulnerabilities and
    coding mistakes.
-   The _around 20 000_ [questions about C and the related answers
    ](http://stackoverflow.com/questions/tagged/c) on
    [StackOverflow](http://stackoverflow.com/).
-   See also the section on
    {{< iref "security" "Security and Encryption" >}}
    which has references on secure programming techniques.

## C compilers
-   [GCC home page](http://gcc.gnu.org/)(FAQ , doc)
-   {{< wp " Distcc" >}} is a tool for speeding up compilation of source code
    by using distributed computing.
-   [ArcWiki: Distcc](https://wiki.archlinux.org/index.php/Distcc).
-   [Gentoo: Distcc](https://wiki.gentoo.org/wiki/Distcc),
    [Distcc Cross-Compiling](https://wiki.gentoo.org/wiki/Distcc/Cross-Compiling).
-   [distcc repository](https://code.google.com/p/distcc/)

## C coding standards
-   Chris Lott's [List of C and C++ Style Guides
    ](http://www.maultech.com/chrislott/resources/cstyle/)
-   [GNU Coding Standards](http://www.gnu.org/prep/standards/standards.html)
-   Original *Indian Hill C Style and Coding Standards* with
    annotations by H. Spencer:
    [Recommended C Style and Coding Standards
    ](http://www.maultech.com/chrislott/resources/cstyle/indhill-annot.html)
-   [Indian Hill C style guide, as amended at UofT, UW, and elsewhere
    ](http://www.maultech.com/chrislott/resources/cstyle/indhill-cstyle.html)
-   [Jim Larson's C coding standards](http://www.jetcafe.org/jim/c-style.html)
    is advertised as
    *A style guide for programming in C, handed down from God himself*.
-   [Kernel Programming Style Guidelines
    ](http://kernelnewbies.org/New_Kernel_Hacking_HOWTO/Kernel_Programming_Style_Guidelines)
-   BSD man page [style(9)](http://www.freebsd.org/cgi/man.cgi?query=style&sektion=9)
    gives the preferred style for kernel source files in the FreeBSD source tree.
-   [Apache Developers' C Language Style Guide
    ](http://httpd.apache.org/dev/styleguide.html)
-   [What is the best comment in source code you have ever encountered?
    ](http://stackoverflow.com/questions/184618/what-is-the-best-comment-in-source-code-you-have-ever-encountered/)
    a review of the most funny comments.
-   About the  [Single Function Exit Point
    ](http://c2.com/cgi/wiki?SingleFunctionExitPoint) rule.
-   {{< wp "lint_(software)"  "Lint" >}} is the original static code analyzer for C.
-   {{< wp "Splint" >}} (GPL) is an enhancement of Lint.
    [Splint Manual](http://splint.org/manual/)
-   {{< wp "Frama-C" >}} (LGPL) is a set of interoperable program analyzers for C programs.
-   [C-C++ Beautifier HOW-TO](http://www.yolinux.com/HOWTO/C-C++Beautifier-HOWTO.html)
    by Alavoor Vasudevan.
-   Other links to pretty-print code are in the section
    {{< iref "source_code" "Source code beautifiers" >}}

## C libraries
-   [Gnu Libc](http://www.gnu.org/software/libc/ "www.gnu.org libc")
    (GPL)
    *[Glibc manual](http://www.gnu.org/software/libc/manual/ "www.gnu.org libc/manual")*.
-   The Gnome library {{< wp "GLib" >}} is a cross-platform library that began as part
    of the {{< wp "GTK+" >}} project but contain now non-GUI-specific code.  _Glib_
    provides the core object system used in Gnome {{< wp "GObject" >}}), the main loop
    implementation, and a large set of utility functions for strings and common data
    structures. It provides typedefs to ensure portability and a large set of
    containers. Glib, GObject and other GTK+ components are in the
    {{< iref "gtk#gtk+" "GTK+ section" >}}.
-   [AT&T Open Source software tools (pdf)
    ](http://www2.research.att.com/~astopen/publications/open-2000-1.pdf)
    (Common Public License) ast, Graphviz, sfio, dytona ....
    [AST downloads](http://www.research.att.com/sw/download/ "research.att.com sw/download").
-   [PCRE - Perl Compatible Regular Expressions](http://www.pcre.org/)
    is library for C that implement
    [Perl RE](http://perldoc.perl.org/perlre.html).
    -   [PCRE2 HTML documentation
        ](http://www.pcre.org/current/doc/html/):
        [pcre2syntax - pcre2 expression syntax quick-reference
        ](http://www.pcre.org/current/doc/html/pcre2syntax.html).
    -   The [Wikipedia:  PCRE](http://en.wikipedia.org/wiki/PCRE)
        page details the features of pcre expressions and the differences
        with perl re.
    -   There are many online pcre tester:
        [regexpal](http://www.regexpal.com/),
        [regex101](https://regex101.com/),
        [debuggex](https://www.debuggex.com/),
        [myregextester](https://www.myregextester.com/),
        [reg-exp](http://reg-exp.com/),
        [pythex](http://pythex.org/) _python regexp_.
    -   See also the {{< iref "python_libraries#python_re" "Python _re_ references" >}}

### antlr

{{< wp "Antlr" >}} (ANother Tool for Language Recognition) provides a framework for
constructing recognizers, compilers, and translators from grammatical
descriptions containing C++ or Java actions

-   [Antlr Home Page](http://www.antlr.org/)

### lexical parsers

-   [flex](http://flex.sourceforge.net/) (GPL)
    is a tool for
    generating scanners
-   The [boost Tokenizer package](http://www.boost.org/libs/tokenizer/)
    provides a flexible and easy to use way to break of a string or
    other character sequence into a series of tokens.

## C debugging

-   [GDB](https://www.sourceware.org/gdb/),
    [GDB Documentation](https://www.sourceware.org/gdb/documentation/),
    [GDB Manual _Debugging with gdb_](http://sourceware.org/gdb/current/onlinedocs/gdb/).
-   [GDB reference card (pdf)](https://sourceware.org/gdb/current/onlinedocs/refcard.pdf.gz)

### System Functions

njamd
:   A malloc debugger {{< man "libnjamd(3)" >}}, {{< man "malloc(3)" >}}

efence
:   An other malloc debugger {{< man "efence(3)" >}}

# C++
-   Wikipedia:  {{< wp "Caml" >}}
-   [Objective Caml Home](http://ocaml.org/),
-   [manual](http://caml.inria.fr/pub/docs/manual-ocaml/)
-   [Functional programming using Caml Light
    ](http://caml.inria.fr/pub/docs/fpcl/index.html)

## Clojure {#clojure}
 {{< wp "Clojure" >}} (eclipse public license) is a lisp dialect that compiles
directly to JVM bytecode (and the CLR, and JavaScript). It supports
multithreaded programming.
-   [Clojure - home](http://clojure.org/)
-   [Clojure Programming (the book)](http://www.clojurebook.com/)
-   [The Clojure Style Guide
    ](https://github.com/bbatsov/clojure-style-guide/blob/master/README.md)
-   [Awesome-clojure (by Vlad Bokov *razum2um*)
    ](https://github.com/razum2um/awesome-clojure) and
    [Awesome-clojure (by Michał Buczko)
    ](https://github.com/mbuczko/awesome-clojure) lists of clojure
    resources.
-   [Clojure with Emacs
    Tutorial](http://clojure-doc.org/articles/tutorials/emacs.html)
-   [leiningen (GitHub)](https://github.com/technomancy/leiningen)
    is a package manager for clojure, to create new
    projects fetch dependencies for your project, run tests, run a
    fully-configured REPL, compile Java sources, run the project, and more
-   [cider](https://github.com/clojure-emacs/cider)
    formerly _nrepl.el_ is the Clojure Interactive Development
    Environment that Rocks for Emacs, built on top of
    [nREPL](https://github.com/clojure/tools.nrepl),
    the Clojure networked REPL server.
-   [nREPL](https://github.com/clojure/tools.nrepl),
    the Clojure networked REPL server.
-   [Ritz
    ](https://github.com/pallet/ritz)
    is a collection of libraries and servers for clojure
    development environments and for debuggers.
    [ritz-nrepl](https://github.com/pallet/ritz/tree/develop/nrepl)
    is an nREPL server with a debugger.
    [Debugging with Ritz slides
    ](http://hugoduncan.github.com/ritz-conj) and
    [video](http://www.youtube.com/watch?v=sA5zOLCa3Xw)
-   [criterium](https://github.com/hugoduncan/criterium)
    is a benchmarking library for clojure.
-   [Clojure Android support
    ](http://dev.clojure.org/display/design/Android+Support)
-   [Clojure-Py](http://halgari.github.io/clojure-py/)
    an implementation of Clojure that runs on the Python VM to prove
    it. With a proper dynamic JIT (like PyPy), a version of Clojure
    running on a dynamic VM can outperform its JVM and CLR
    counterparts.
-   [clojurescript](https://github.com/clojure/clojurescript) a
    Clojure to JS compiler
-   [Scala Vs Clojure - Let's get down to business - Best In Class
    ](http://www.bestinclass.dk/blog/scala-vs-clojure-lets-get-down-to-business),
    [Scala Vs Clojure - Round 2: Concurrency - Best In Class
    ](http://www.bestinclass.dk/blog/scala-vs-clojure-round-2-concurrency)
-   [Python v. Clojure v. Julia
    ](http://matthewrocklin.com/blog/work/2014/01/13/Text-Benchmarks/)
-   [Why I Switched from Python to Clojure
    ](http://www.bradcypert.com/2016/07/18/why-i-switched-from-python-to-clojure/)
    by Brad Cypert among the
    [articles tagged clojure](http://www.bradcypert.com/tag/clojure/)
    from his Blog.
-   [How I Start clojure](http://howistart.org/posts/clojure/1)
-   [Category Clojure - Rosetta Code
    ](http://rosettacode.org/wiki/Category:Clojure)

# D Programming Language
-   Wikipedia: {{< wp "D(programming_language)"  "D Programming Language" >}}
-   The [D Programming Language](http://digitalmars.com/d/) originated
    as a re-engineering of C++, and as C++ is an object-oriented,
    imperative, multi-paradigm system programming language

# Go
-   {{< wp "Go_(programming_language)"  "Go" >}} is a compiled, garbage-collected,
    concurrent programming language developed by Google.
-   [Go Home Page](http://golang.org/)
-   [Awesome Go](https://awesome-go.com/)
    list of awesome Go frameworks, libraries and software.
    [GitHub repository](https://github.com/avelino/awesome-go/)
-   [Awesome - Go Patterns](http://tmrts.com/go-patterns/)
    [GitHub repository](https://github.com/tmrts/go-patterns).
-   [Go for Python Programmers — Go for Python Programmers documentation
    ](https://golang-for-python-programmers.readthedocs.org/en/latest/).
-   [Go Arm support](https://github.com/golang/go/wiki/GoArm) includes
    arm v5, v6, v7, v8 (not v4)
-   [Category:Go - Rosetta Code
    ](http://rosettacode.org/wiki/Category:Go)
-   There are many critisisms to Go Concepts and structure:
    Will Yager [Why Go Is Not Good
    ](http://yager.io/programming/go.html),
    [C&C - Leaving Go
    ](http://jozefg.bitbucket.org/posts/2013-08-23-leaving-go.html),
    [What reasons are there to not use Go (programming language)? - Quora
    ](http://www.quora.com/What-reasons-are-there-to-not-use-Go-programming-language)
    ...
-   [Installing Go from source](http://golang.org/doc/install/source)
    from the official [Go Sitee](http://golang.org/).
-   [An introduction to cross compilation with Go
    ](http://dave.cheney.net/2013/07/09/an-introduction-to-cross-compilation-with-go-1-1),
    [part II
    ](http://dave.cheney.net/2015/03/03/cross-compilation-just-got-a-whole-lot-better-in-go-1-5)
-   [GoArm](https://github.com/golang/go/wiki/GoArm)
    explain compilation of go on arm systems, it gives also a list of linux nas, where
    go is usable.

## Go documentation
-   [Go Home Page](http://golang.org/) has
    [Go Documentation](https://golang.org/doc/)
    -   [A Tour of Go](https://tour.golang.org/list) the official tutorial from
        [The Golang Home](https://golang.org/).
    -   [How to Write Go Code](https://golang.org/doc/code.html)
        demonstrates the development of a simple Go package and introduces the go tool.
    -   [The Go Programming Language Specification](https://golang.org/ref/spec).
    -   [Effective Go](https://golang.org/doc/effective_go.html)
        gives tips for writing clear, idiomatic Go code.
-   [awesome-go: list of tutorials](https://github.com/avelino/awesome-go#tutorials)
    and [Ebooks](https://github.com/avelino/awesome-go#e-books).
-   [A list of Golang books](https://github.com/dariubs/GoBooks), some are free.
-   [Go by Example](https://gobyexample.com/)  introduction to Go using annotated
    example programs.
-   [Golang cheat sheet](https://github.com/a8m/golang-cheat-sheet)
    by  Ariel Mashraki is an overview of Go syntax and features with examples taken from
    [A Tour of Go](https://tour.golang.org/list). The [GitHub repository
        ](https://github.com/a8m/golang-cheat-sheet) also contains a reference card in
    _odt_ and _pdf_.
-   [Golang CheatSheet](https://cheatsheet.dennyzhang.com/cheatsheet-golang-a4)
    from [GitHub - DennyZhang Cheat Sheets
    ](https://github.com/dennyzhang/cheatsheet.dennyzhang.com).
-   [Go cheatsheet](https://devhints.io/go) from
    [devints.io](https://devhints.io/).
-   [Golang Templates Cheatsheet
    ](https://curtisvermeeren.github.io/2017/09/14/Golang-Templates-Cheatsheet).

# Haskell {#haskell}
-   Wikipedia {{< wp "Haskell_(programming_language)"  "Haskell" >}}
-   [Haskell Home](http://www.haskell.org/)
    in the [Haskell Wiki](http://www.haskell.org/haskellwiki/)
-   [Hugs](http://www.haskell.org/hugs/) is a bytecode interpreter for Haskell.
-   [Hackage](http://hackage.haskell.org/packages/archive/pkg-list.html)
    is the Haskell package library list.
-   [Haskell mode for emacs](http://www.haskell.org/haskellwiki/Emacs)
-   [Go for Python Programmers](https://golang-for-python-programmers.readthedocs.org/en/latest/)
-   [List of Go Projects](https://github.com/golang/go/wiki/Projects)
-   [Why Go Is Not Good :: Will Yager](http://yager.io/programming/go.html)

## Haskell  Tutorials and Manuals:
-    [Learning Haskell](http://www.haskell.org/haskellwiki/Learning_Haskell)
     from the Haskell wiki, reference the haskell learning
     resources.
     <!------------------------------------------------>
-    [Haskell in 5 steps
    ](http://www.haskell.org/haskellwiki/Haskell_in_5_steps)
    help you get started as quickly as possible.
-   [Learn Haskell in 10 minutes
    ](http://www.haskell.org/haskellwiki/Learn_Haskell_in_10_minutes),
-   [A Gentle Introduction To Haskell
    ](http://www.haskell.org/tutorial/)
    by Reuben Thomas is written for someone who has experience
    with at least one other language, preferably a functional
    language.
-   [Learn You a Haskell for Great Good!
    ](http://learnyouahaskell.com/)
    is a tutorial aimed at people who have experience in
    imperative programming languages but haven't programmed in a
    functional language before.
-   [Real World Haskell
    ](http://book.realworldhaskell.org/read/)
    is a book available online by Bryan O'Sullivan, Don Stewart,
    and John Goerzen.
-   [Software Tools in Haskell
    ](http://www.crsr.net/Programming_Languages/SoftwareTools/index.html)
    by Tommy M. McGuire are working programs that solve real-world
    problems.

# Haxe
{{< wp "Haxe" >}} (GPL, MIT) is a multiplatform programming language and compiler
that can translate the Haxe language into Adobe Flash applications,
JavaScript programs, Java, C#, C++ standalone applications, Python,
PHP, Apache CGI, and Node.js server-side applications.

The Haxe compiler is developed in the OCaml. Haxe is a general-purpose
language with object-oriented programming, exceptions, and
{{< wp "type inference" >}} with class parameters.
{{< wp "Generic classes" >}},
{{< wp "Reflection (computer programming)"  "Reflection" >}}, {{< wp "iterators" >}},
and {{< wp "functional programming" >}} are built-in functionality of the language and
libraries.

-   [Haxe Home](http://haxe.org/).


# Lua
-   Wikipedia {{< wp "Lua (programming language)"  "Lua" >}}
-   [lua](http://www.lua.org/) (MIT License) [
    [lua projects](http://www.lua.org/uses.html)]
-   {{< wp "Lua_(programming_language)"  "Wikipedia: Lua (programming language)" >}}
    has a feature list, programming examples of the Lua programming language and
    numerous references to software that can embed lua code.
-   [awesome-lua (by forhappy)
    ](https://github.com/forhappy/awesome-lua)
    and [awesome-lua (by Lewis J Ellis)
    ](https://github.com/LewisJEllis/awesome-lua)
-   [A Look at Lua](http://www.linuxjournal.com/article/9605) a tutorial by Joseph
    Quigley in linux-journal 2007.
-   [Embeddable scripting with Lua](http://www.ibm.com/developerworks/linux/library/l-lua.html)
    by Martin Streicher  in _IBM developer works_ 2006.
-   [lua-users wiki](http://lua-users.org/wiki/) [
    [Lua Faq](http://lua-users.org/wiki/LuaFaq),
    [Learning Lua](http://lua-users.org/wiki/LearningLua),
    [Lua tutorials](http://lua-users.org/wiki/TutorialDirectory),
    [Lua addons](http://lua-users.org/wiki/LuaAddons),
    [Sample Code](http://lua-users.org/wiki/SampleCode),
    [Binding Code To Lua](http://lua-users.org/wiki/BindingCodeToLua),
    [Libraries And Bindings
    ](http://lua-users.org/wiki/LibrariesAndBindings) ]
-   [LuaForge](http://luaforge.net/)
    [software map](http://luaforge.net/softwaremap/trove_list.php)
-   [toLua home page](http://www.tecgraf.puc-rio.br/~celes/tolua/)
-   For c/c++ binding generation we can use
    [tolua](http://www.tecgraf.puc-rio.br/~celes/tolua/),
    [toLua++](http://sourceforge.net/projects/toluapp.berlios/),
    [swig](http://www.swig.org/) _a multi language binding generator_.
-   [Kepler Project](http://www.keplerproject.org/) (MIT License) includes WSAPI,
    CGILua; the frameworks built upon _wsapi_: _xavante_, _orbit_,
     _sputnik_ , the _cosmo_ template system, development tools
    _LuaDoc_, _LuaRocks_ a deployment and management system,
    _Shake_ test engine  and
    other components that allow the use of SQL, LDAP, XML, SOAP etc.
    -   [LuaJava - A Script Tool for Java
        ](http://www.keplerproject.org/luajava/)
-   [Lua Manual 5.4](http://www.lua.org/manual/5.4/)
-   [Programming in Lua (first edition lua 5.0)
    ](http://www.lua.org/pil/)
-   [Litt's Lua Laboratory
    ](http://www.troubleshooters.com/codecorn/lua/index.htm)
    by Steve Litt are Lua snippets and tips.
-   [lunatic python](http://labix.org/lunatic-python) (LGPL)
    is a two way bridge between lua and python.
-   Julien Danjou who implemented the Lua programming language in the window manager
    {{< iref "desktop" "Awesome" >}},
    does not appreciate the lua design so he made some
    [rants about Lua](https://julien.danjou.info/blog/2008/rants-about-lua) in 2008
    that he extended in 2011 in
    [why not Lua](https://julien.danjou.info/blog/2011/why-not-lua)
-   [lua ncurses](https://github.com/msva/lua-ncurses)
    is a wrapper around the ncurses library for terminal programming.

# Mirah
-   Wikipedia: {{< wp "Mirah_%28programming_language%29"  "Mirah" >}}
-   [Mirah](http://en.wikipedia.org/wiki/Mirah_%28programming_language%29) (Apache License)
    is a programming language based on Ruby syntax,
    local type inference, hybrid static/dynamic type system, that compile to JVM bytecode.
-   [Mirah Home](http://www.mirah.org/)

# Nim   {#nim}

Nim is an imperative compiled language supporting metaprogramming,
functional, message passing, procedural, and object-oriented
programming styles.

It provides compile time code generation, algebraic data types, an
elegant FFI with C and compilation to Javascript.

The compiler generates optimized C code and defers compilation to an
external compiler, it can also generate C++ and Objective C

Nim is a statically typed programming language, it supports
{{< wp "Macro_(computer_science)#Syntactic_macros"  "syntactic macros" >}}
and term rewriting macros.

There are existing bindings for many libraries, for example GTK+2,
SDL2, Cairo, OpenGL, WinAPI, zlib, libzip, OpenSSL and cURL.[19] Nim
works with PostgreSQL, MySQL and SQLite databases. Nim can interface
with the Lua and Python interpreter. The tool c2nim helps to generate
new bindings from C code.

-   Wikipedia: {{< wp "Nim" >}}.
-   [Nim Home](http://nim-lang.org/)
-   [Nim Wiki](https://github.com/Araq/Nim/wiki)
-   [GitHub: Nim](https://github.com/Araq/Nim)
-   [Nim Documentation](https://nim-lang.org/documentation.html):
    -   [Nim Manual](http://nim-lang.org/docs/manual.html)
-   [official Nim Blog](https://nim-lang.org/blog.html)
-   [Awesome-nim](https://github.com/VPashkov/awesome-nim)
    is a list of Nim resources frameworks, libraries and software.
-   [Nim by Example
    ](http://nim-by-example.github.io/).
-   [Nim Editor Support
    ](https://github.com/Araq/Nim/wiki/Editor-Support),
    for emacs you should use [nim-mode
    ](https://github.com/reactormonk/nim-mode) _in elpa_,
    [Aporia
    ](https://github.com/nim-lang/Aporia/)
    is an IDE/Advanced text editor writtten in Nim and mainly focusing
    on support for the Nim programming language.
-   [Nim IDE Integration Guide
    ](http://nim-lang.org/docs/nimsuggest.html)
    describe the use of
    [nimsuggest](https://github.com/nim-lang/nimsuggest).
-   [Nim standard libraries and list of Nimble packages
    ](http://nim-lang.org/docs/lib.html).
-   [Nim community projects
    ](https://github.com/Araq/Nim/wiki/Community-Projects).
-   [Official List of Nim Tutorials Examples and Articles
    ](http://nim-lang.org/learn.html)
-   [Nim Wiki: Nim for Python Programmers
    ](https://github.com/Araq/Nim/wiki/Nim-for-Python-Programmers).
-   [Nim's Community](http://nim-lang.org/community.html)
-   Göran Krampe [ Roads Less Taken: Category: Nim
    ](http://goran.krampe.se/category/nim/):
    -   [Nim features
        ](http://goran.krampe.se/2015/03/26/nim-voodoo/)
        describe the main features and facilities of Nim. It peculiarly
        stressed up {{< wp "Meta programming" >}}.
    -   [Nim Crash Course in LXC
        ](http://goran.krampe.se/2017/10/24/nim-crash-course-inside-lxc)
        _lxc part is optional_.
-   [Dennis Felsing](http://felsin9.de/nnis/):
    -   [How I start Nim](http://howistart.org/posts/nim/1) _updated 2018_.
    -   [Dennis Felsing (def-) GitHub repo](https://github.com/def-)
        has many Nim projects.
    -   [HookRace - Dennis Felsing Blog](http://hookrace.net/)
        has [nim posts](https://hookrace.net/blog/nim/) _only until 2016_.
    -   [Nim binary size from 160 KB to 150 Bytes
        ](http://hookrace.net/blog/nim-binary-size/)
    -   [What is special about Nim?
        ](http://hookrace.net/blog/what-is-special-about-nim) see the paragraph
        [Bind to your favorite C functions and libraries
        ](http://hookrace.net/blog/what-is-special-about-nim/#bind-to-your-favorite-c-functions-and-libraries)
    -   [What makes Nim practical?
        ](http://hookrace.net/blog/what-makes-nim-practical/)
        look at the section [Wrapping libraries with c2nim
        ](http://hookrace.net/blog/what-makes-nim-practical/#wrapping-libraries-with-c2nim)
-   [Category:Nim - Rosetta Code](http://rosettacode.org/wiki/Nim).
-   [Nim Forum](http://forum.nim-lang.org/)
    -   [Topic Program size](http://forum.nim-lang.org/t/963)

## Nim projects

-   [gh_nimrod_doc_pages](https://github.com/gradha/gh_nimrod_doc_pages)
    Generates a GitHub documentation website for Nim projects
    [gh_nimrod_doc_pagesusage guide ](http://gradha.github.io/gh_nimrod_doc_pages/)


# Perl

-   Wikipedia: {{< wp "Perl" >}}
-   [PERL Home](http://www.perl.com/) (GPL or Artistic License)
-   {{< wp "Perl_6" >}}
-   [free perl books
    ](http://www.freeprogrammingresources.com/perlbook.html).
-   [wikiversity topic:Perl](http://en.wikiversity.org/wiki/Topic:Perl)
-   [perl quickref  5.004 (pdf)
    ](http://www.squirrel.nl/pub/perlref-5.004.1.pdf)
-   [perl quickref  5.001 (text only)
    ](http://www.squirrel.nl/pub/perl_quickref_5_001-refguide.txt),
    [perl quickref (html-ified)
    ](http://www.rexswain.com/perl5.html)
-   [Learning Perl the hard way (pdf)
    ](http://www.greenteapress.com/perl/perl.pdf)
-   [wikibook: Perl Programming](http://en.wikibooks.org/wiki/Perl_Programming)

# Prolog
-   Wikipedia: {{< wp "Prolog" >}}, {{< wp "Logic_programming" >}},
    {{< wp "Category:Logic programming" >}}
-   [SWI-Prolog: Edinburgh compatible Prolog compiler](http://www.swi-prolog.org/)


# Ruby
_Ruby is covered by GPL or the GPL compatible {{< wp "Ruby License" >}}_

-   Wikipedia:  {{< wp "Ruby_(programming_language)"  "Ruby" >}}
-   [Ruby home page](http://www.ruby-lang.org/)
-   [Ruby in twenty minutes](http://www.ruby-lang.org/en/documentation/quickstart/)
    the official tutorial.
-   [Ruby From Other Languages
    ](http://www.ruby-lang.org/en/documentation/ruby-from-other-languages/)
    : [ruby from python
    ](http://www.ruby-lang.org/en/documentation/ruby-from-other-languages/to-ruby-from-python/).
-   [List of Ruby tutorials and manuals](http://www.ruby-lang.org/en/documentation/)
-   [Ruby-Doc](http://www.ruby-doc.org/)
-   [Programming Ruby](http://www.ruby-doc.org/docs/ProgrammingRuby/)
     _first edition, year 2000_
-   [Wikibook: Ruby Programming](http://en.wikibooks.org/wiki/Ruby_programming_language)
-   {{< wp "JRuby" >}} (GPL) is a Java implementation of the Ruby programming language.
-   [w:Ruby on Rails](MIT License) is a web application framework for the Ruby programming language.
-   [Rubygems](http://rubygems.org/) the Ruby community's gem hosting service.
-   [gem command reference](http://docs.rubygems.org/read/book/2)

# Rust {#rust}

Rust is a systems programming language for highly concurrent and
highly safe code.
It is designed to be memory safe.

The type system supports a mechanism similar to type classes, called
'traits', inspired directly by  Haskell that allows  an {{< wp "ad-hoc polymorphism" >}}.

Rust features {{< wp "type inference" >}}, its object system uses
_implementation_ that fulfill a role similar to that of classes.

-   Wikipedia: {{< wp "Rust_(programming_language)" "Rust" >}}
-   [Rust book - The Rust Programming Language
    ](https://doc.rust-lang.org/stable/book/)
-   [The Rust Reference
    ](https://doc.rust-lang.org/stable/reference.html)
-   [Cookin' with Rust](https://brson.github.io/rust-cookbook/)
    is a collection of simple examples that demonstrate good
    practices to accomplish common programming tasks, using the
    crates of the Rust ecosystem.
-   [awesome-rust
    ](https://github.com/rust-unofficial/awesome-rust)
    a list of Rust code and resources.
-   [Rust Projects](http://www.rust-ci.org/projects/)
-   [a very brief intro to rust
    ](https://ashleygwilliams.github.io/a-very-brief-intro-to-rust/)
-   [Rust by Example](http://rustbyexample.com/)
-   [Category:Rust - Rosetta Code
    ](http://rosettacode.org/wiki/Category:Rust)
-   [Rosetta Code problems in Rust
    ](https://github.com/Hoverbear/rust-rosetta)
-   [Rust vs Go
    ](http://jaredly.github.io/2014/03/22/rust-vs-go/)
-   Matt Butcher series [The Go Developer's Quickstart Guide to Rust
    ](http://technosophos.com/2018/05/27/the-go-developers-quickstart-guide-to-rust.html)    ,
    [From Go to Rust with an HTTP Server
    ](http://technosophos.com/2018/06/04/from-go-to-rust-with-an-http-server.html),
    [From Go to Rust - JSON and YAML
    ](http://technosophos.com/2018/06/12/from-go-to-rust-json-and-yaml.html),
    [From Go to Rust - Unit Testing
    ](http://technosophos.com/2018/07/07/from-go-to-rust-testing.html),
    [From Go To Rust - Advanced Testing
    ](http://technosophos.com/2018/07/25/from-go-to-rust-advanced-testing.html).
-   an Interview with Steve Klabnik:
    [How Rust Compares to Other Languages
    ](https://www.codementor.io/rust/tutorial/steve-klabnik-rust-vs-c-go-ocaml-erlang)
-   [My first program in Rust - Siosm's blog
    ](https://tim.siosm.fr/blog/2014/02/16/first-rust-prog-and-rss-reader-update/)
-   [Rust severely disappoints me](http://esr.ibiblio.org/?p=7294)
    by  Eric Raymond who found the learning curve  worse than
    expected, and that *things that should be dirt-simple, are
    unreasonably difficult*. He compares it with the learning curve of
    Go that is smoother, and conclude that Rust still lack of maturity.
-   [hyper](http://hyper.rs/hyper/hyper/index.html)
    is a fast, modern HTTP implementation written in and for Rust.
    Hyper offers both a Client and a Server which can be used to drive
    complex web applications written entirely in Rust.
-   [remacs](https://github.com/Wilfred/remacs) is a port to Rust of
    emacs. In February 2018 it is a very active project.

# Rusthon {#rusthon}

Rusthon is a pythonic language with some extra syntax inspired by Go,
JavaScript, Rust and C++. Rusthon is written in Python, and uses the
native AST parser, and so is able to parse all valid Python code.

It can compile to JavaScript and C++ backends, there are also Go and
Rust backends in development.

The JavaScript backend is able to preserve most of the dynamic
semantics, while other backends require you write fully typed Python
code

There is a package in Debian, but the developpement seemed to have
stopped in 2015.

-   [Rusthon Wiki Home](https://github.com/rusthon/Rusthon/wiki)
-   [Rusthon GitHub Repository](https://github.com/rusthon/Rusthon)
-   [Rusthon Blog](http://rusthon-lang.blogspot.fr/)
-   [Nim and Rusthon
    ](http://rusthon-lang.blogspot.fr/2015/02/nim-and-rusthon.html)
-   [Literate Programming
    ](http://rusthon-lang.blogspot.fr/2015/03/literate-programming.html)
-   [Rusthon C++11 Backend
    ](http://rusthon-lang.blogspot.fr/2015/02/rusthon-c11-backend.html)

# Scala
{{< wp "Scala_(programming_language)" "Scala" >}} combines object-oriented language and
functional programming and compile to java byte code.  Scala speed compare with java
speed in
[The computer language benchmarks game](http://shootout.alioth.debian.org/)

# Scheme

-   Wikipedia: {{< wp "Scheme (programming language)"  "Scheme" >}}
-   [Revised6 Report on the Algorithmic Language Scheme (R6RS)
    ](http://www.r6rs.org/)
-   [Revised(5) Report on the Algorithmic Language Scheme (R5RS)
    ](http://www.schemers.org/Documents/Standards/R5RS/HTML/r5rs.html)
    and
    [r4rs](http://www.cs.indiana.edu/scheme-repository/R4RS/r4rs_toc.html)
-   [R7RS Home Page](http://trac.sacrideo.us/wg/wiki/R7RSHomePage)
-   [schemers.org](http://www.schemers.org/),
    [SRFI - Scheme Requests for Implementation](http://srfi.schemers.org/)
-   [Scheme home page at MIT
    ](http://groups.csail.mit.edu/mac/projects/scheme/index.html)
-   [The Scheme Underground Network Package
    ](http://scsh.net/resources/sunet.html)
-   [w:Bigloo](GPL), [Bigloo Home
    ](http://www-sop.inria.fr/members/Manuel.Serrano/bigloo/) de
    [Manuel Serrano](http://www-sop.inria.fr/members/Manuel.Serrano/)
    compile scheme to C or JVM; and has now a support for Android.
-   {{< wp "Kawa" >}}, [Kawa Home](http://www.gnu.org/software/kawa/),
    the Java-based Scheme system,
    [Hello world in Scheme (Kawa) for Android
    ](http://per.bothner.com/blog/2010/AndroidHelloScheme/)
    from [Per Bothner](http://per.bothner.com/index.html)
    the creator of Kawa.
-   {{< wp "Racket" >}} is the new name of PLT Scheme.
    [Racket Home Page](http://racket-lang.org/)
    [[The TeachScheme! Project](http://www.teach-scheme.org/)
    including the book
    [How to Design Programs
    ](http://docs.racket-lang.org/htdp-langs/index.html),
    [DrRacket](http://docs.racket-lang.org/drracket/index.html)
    Programming Environment (formerly DrScheme),
    MzScheme,   Racklog: Prolog-Style Logic Programming in Racket],
    [Nu PLT](http://www.ccs.neu.edu/scheme/),
    [Matthias Felleisen](http://www.ccs.neu.edu/home/matthias/) (the
    little schemer ...),
-   [Dorai Sitaram Home Page](http://www.ccs.neu.edu/home/dorai/):
    [Teach Yourself Scheme in Fixnum Days
    ](http://www.ccs.neu.edu/~dorai/t-y-scheme/t-y-scheme.html)
    TeX2page, pregexp, Schelog)
-   [Jaffer](http://people.csail.mit.edu/jaffer/)'s
    [SCM Home Page](http://people.csail.mit.edu/jaffer/SCM.html)
-   {{< wp "GNU Guile" >}}:
    [GNU Guile Home Page](http://www.gnu.org/software/guile/guile.html),
    [Gnu Guile projects and libraries](http://www.gnu.org/software/guile/gnu-guile-projects.html)
    [Guile FAQ](http://www.gnu.org/software/guile/docs/faq/guile-faq.html)
-   [Chicken - A practical and portable Scheme system](http://www.call-cc.org/)
-   [Gauche](http://practical-scheme.net/gauche/index.html)
    an R7RS Scheme implementation developed to be a handy script
    interpreter. It includes many features (most SRFIs) a CLOS-like
    object system, multibyte support; and network, threads, dbm, sxml,
    opengl, gtk bindings.
-   [sawfish](http://sawfish.wikia.com/wiki/Main_Page) lisp window manager

## Lisp
-   Wikipedia: {{< wp "Lisp_(programming_language)"  "Lisp" >}},
    {{< wp "Common Lisp" >}}.
-   [CLISP](http://clisp.cons.org/)


## Scheme as preprocessor
-   [BRL, the Beautiful Report Language](http://brl.sourceforge.net/)
-   [Skribe](http://www-sop.inria.fr/mimosa/fp/Skribe/) is a text
    processor aimed at writing of technical documents such as web pages
    or technical reports _unmaintained since 2008_.
-   [escm](http://practical-scheme.net/vault/escm.html)
    embedded scheme preprocessor written in C
-   [Dorai Sitaram \\eval for TeX
    ](http://www.ccs.neu.edu/home/dorai/eval4tex/eval4tex-doc.html)

# Unicon and Icon

-    {{< wp "Icon_(programming_language)"  "Icon" >}} is a programming language with syntax similar
     to C or Pascal released in  1977. It features goal directed execution and many facilities
     for managing strings and textual patterns. There is a
     [WikiBook: Icon Programming](http://en.wikibooks.org/wiki/Icon_Programming).
     [The Icon Programming Language  (home page)](http://www.cs.arizona.edu/icon/index.htm).
-    {{< wp "Unicon_programming_language"  "Unicon" >}} (GPL) was developed in 1996.
     It descends from Icon but offers better access to the operating system
     as well as support for object-oriented programming.

# Vala, Genie {#vala}
-   Wikipedia: {{< wp "Vala_(programming_language)"  "Vala" >}},
    {{< wp "Genie_%28programming_language%29"  "Genie" >}}
-   {{< wp "Vala_(programming_language)"  "Vala" >}} (LGPL)
    is a programming language whose syntax borrows heavily from C#.
    Vala is compiled to C and uses the {{< wp "GObject" >}} object system.
-   [Gnome Project: Vala](https://wiki.gnome.org/Projects/Vala)
-   [Valadoc](https://wiki.gnome.org/Projects/Valadoc)
    is a documentation generator for generating API documentation from Vala source code
-   [Libgee](https://wiki.gnome.org/action/show/Projects/Libgee)
    (LGPL) is a collection library written in vala, which provides
-   {{< wp "Genie_%28programming_language%29"  "Genie" >}} is an alternative,
    more pythonic, syntax for Vala, that generates the same code.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
