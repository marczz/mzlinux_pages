---
title: Org Mode
---

{{% toc /%}}

# Org Mode

-   [OrgMode Home](http://orgmode.org/),
    [Emacs org manual](http://orgmode.org/org.html),
    [The compact Org-mode Guide](http://orgmode.org/guide/)
-   [Emacswiki: OrgMode](http://www.emacswiki.org/emacs/OrgMode)


## Tutorials:
-   [Worg List of Org tutorials
    ](http://orgmode.org/worg/org-tutorials/index.html)
-   [Org Mode - Organize Your Life In Plain Text
    ](http://doc.norang.ca/org-mode.html)
    by Bernt Hansen is a very useful compact guide that includes a section on
    [Git synchronization](http://doc.norang.ca/org-mode.html#GitSync)
-   [David O'Toole Org tutorial
    ](http://orgmode.org/worg/org-tutorials/orgtutorial_dto.html)
    appropriate for org-mode's beginners.
-   [LaTeX Export](http://orgmode.org/worg/org-tutorials/org-latex-export.html)
    ([Exporting in Org manual](http://orgmode.org/org.html#Exporting) )
-   [Publishing Org-mode files to HTML
    ](http://orgmode.org/worg/org-tutorials/org-publish-html-tutorial.html)
-   [Putting Your org Files Under Version Control
    ](http://orgmode.org/worg/org-tutorials/org-vcs.html)
-   Eric Neilsen's [Emacs org-mode examples and cookbook
    ](http://home.fnal.gov/~neilsen/notebook/orgExamples/org-examples.html)
-   Eric Schulte [collection of Org-mode snippets using code blocks
    ](https://eschulte.github.io/org-scraps/).
-   [org2latex - a yasnippet
    ](http://www.sharons.org.uk/org2latex.html)
-   [Org-mode Basics](http://www.star.bris.ac.uk/bjm/org-basics.html)
-   [Emacs In a Box](http://caiorss.github.io/Emacs-Elisp-Programming/)
    A tutorial about programming Elisp and Emacs text editor customization.
    The source repository is [GitHub - Emacs-Elisp-Programming
    ](https://github.com/caiorss/Emacs-Elisp-Programming)



## Articles and Blogs
-   [Sacha Chua
    ](http://sachachua.com):
    [last posts category org](http://sachachua.com/blog/category/org/)
-   [emacs-fu: nice-looking pdfs with org-mode and xetex
    ](http://emacs-fu.blogspot.com/2011/04/nice-looking-pdfs-with-org-mode-and.html)
-   [Kitchin Group at CMU - category orgmode
    ](http://kitchingroup.cheme.cmu.edu/blog/category/orgmode/)
    -   [New link features in org 9
        ](http://kitchingroup.cheme.cmu.edu/blog/2016/11/04/New-link-features-in-org-9/),
        [New color link in org 9.0 using font-lock to color the text
        ](http://kitchingroup.cheme.cmu.edu/blog/2016/11/08/New-color-link-in-org-9-0-using-font-lock-to-color-the-text/),
        [Persistent highlighting in Emacs
        ](http://kitchingroup.cheme.cmu.edu/blog/2016/11/10/Persistent-highlighting-in-Emacs/).


## Org Babel {#babel}

-   [The Org Manual: Working with source code
    ](https://orgmode.org/manual/Working-with-source-code.html#Working-with-source-code)
-   [Babel: Introduction](http://orgmode.org/worg/org-contrib/babel/intro.html)
-   [Index of babel/languages/
    ](https://orgmode.org/worg/org-contrib/babel/languages/)
-   [GitHub - dfeich/org-babel-examples
    ](https://github.com/dfeich/org-babel-examples)
    with different backend languages.

### Org-Babel literate programming

See also {{< iref "source_code#literate_programming" "Literate Programming" >}}
-   [Introduction to Literate Programming
    ](http://www.howardism.org/Technical/Emacs/literate-programming-tutorial.html)
    _with Org Babel_.
-   [Babel Introduction - Code Blocks
    ](https://orgmode.org/worg/org-contrib/babel/intro.html#source-code-blocks)
    and
    [Babel Introduction - Literate Programming
    ](https://orgmode.org/worg/org-contrib/babel/intro.html#literate-programming).
    the same document show a
    [simple literate emacs init file
    ](https://orgmode.org/worg/org-contrib/babel/intro.html#literate-emacs-init)
    and recommend for a complete example the literate programming version of starter kit
    by Eric Schulte, they give an old version but you may prefer
    [eschulte/emacs24-starter-kit](https://github.com/eschulte/emacs24-starter-kit).
-   [Org-mode - Literate Programming Recipes
    ](https://caiorss.github.io/Emacs-Elisp-Programming/Org-mode-recipes.html)
-   [org-mode examples and cookbook -Writing literate python code
    ](http://ehneilsen.net/notebook/orgExamples/org-examples.html#sec-25)
-   [Org-mode - Literate Programming Recipes
    ](https://caiorss.github.io/Emacs-Elisp-Programming/Org-mode-recipes.html)
-   [Formatting tangled output in org-mode
    ](https://jamesaimonetti.com/fr/posts/formatting-tangled-output-in-org-mode/)
    explains _org-babel-post-tangle-hook_.

## Org mode parsing

[Org Mode tools: Org-mode parsers](http://orgmode.org/worg/org-tools/#sec-1)

-   [CL-org-mode](http://common-lisp.net/project/cl-org-mode/)
    is a parser for org-mode files that uses an extensible CLOS-based
    recursive descent parser to create a tree of org-mode nodes. _2009_
-   [PyOrgMode](https://github.com/bjonnh/PyOrgMode)
    by Jonathan Bisson is a python library for creating and parsing
    Org files. _up to date in may 2015_
-   [Neo - No Emacs Org](http://chadok.info/darcs/neo/)
    by Olivier Schwander is another Python tool for parsing org mode
    files. _2012_
-   [org-mode-parser](https://github.com/daitangio/org-mode-parser)
    by Giovanni Giorgi is a Node.js parser for org mode.
-   [Orgile](http://toshine.org/etc/orgile-emacs-org-mode-file-html-parser-php-publishing-tool/)
    is a PHP  Org-mode  parser.
    [Orgile GiHub repository](https://github.com/mashdot/orgile). _2012_
-   [orgnode](http://members.optusnet.com.au/~charles57/GTD/orgnode.html) (MIT)
    by [Charles Cave](http://members.optusnet.com.au/~charles57/GTD/)
    is a python program to read org-mode files. _2010_
-  [org.js](http://mooz.github.io/org-js/)
    JavaScript Parser and converter for org-mode. _updated in 2014_

## Utilities
-   [Deft](http://jblevins.org/projects/deft/) by Jason Blevin
    is an emacs mode for quickly browsing, filtering, and editing
    directories of plain text notes, inspired by Notational Velocity.
    -   [EmacsWiki: Using a major mode for Deft files
        ](https://www.emacswiki.org/emacs/DeftMode)
    -   [Setting Up Deft Mode in Emacs with Org-Mode
        ](http://jonathanchu.is/posts/setting-up-deft-mode-in-emacs-with-org-mode/)
-   [ical2org](https://bitbucket.org/dhellmann/ical2org)
    is a python tool by Doug Helmann, for exporting data from the  iCal format emacs
    org-mode. _2012_.
    [PyPi ical2org](https://pypi.python.org/pypi/ical2org/)
-   [ical2org.py](https://github.com/asoroa/ical2org.py)
    is a python script to converts an ical calendar into an org-mode
    document.  It is conceived as a replacement of the awk script
    [ical2org.awk ](http://orgmode.org/worg/org-tutorials/org-google-sync.html).
    The main difference is that ical2org.py correctly manages
    recurring events of "yearly", "daily" and "weekly"
    types. ical2org.py duplicates all recurring events falling into a
    specified time-frame into the exported org-document.
-   [memacs](https://github.com/novoid/Memacs) (GPL) by Karl Voit
    extracts metadata from many different existing data sources
    (file names, emails, tweets, bookmarks, …)
    on your computer and generates org-mode files.
-   [org-annotate-file](http://emacswiki.org/wiki/OrgAnnotateFile)
    allows the annotation of a file in org-mode without modification
    of the file itself.  There is at least three versions of
    _org-annotate-file_ that was successively forked by
    [Philip Jackson](http://emacswiki.org/emacs/org-annotate-file.el),
    [Nick Daly
    ](https://bitbucket.org/nickdaly/org-annotate-file/src/tip/org-annotate-file.el)
    _2011_,
    and [Diego Sevilla
    ](https://bitbucket.org/dsevilla/org-annotate-file/src/tip/org-annotate-file.el) _2011_
    after he wrote [this comment
    ](http://stackoverflow.com/questions/7295708/how-to-use-org-annotate-file).
-   [org-contacts](http://julien.danjou.info/software/org-contacts.el)
    by Julien Danjou allows to manage your contacts using Org-mode
    without BBDB. He has also written
    [google-contacts](http://julien.danjou.info/software/google-contacts.el)
    to allow managing  google contacts from Emacs (>= 24).
-   [org-info-js](http://orgmode.org/worg/code/org-info-js/)
    is a javascript tool to navigate through a HTML page exported by
    Org using
    [shortcuts](http://orgmode.org/worg/code/org-info-js/#shortcuts)
    in the same way you navigate through an info manual.
-   [org-mutt (git repo)](http://git.upsilon.cc/?p=utils/org-mutt.git)
    _updated in 2014_
    [integrating Mutt with Org-mode
    ](http://upsilon.cc/~zack/blog/posts/2010/02/integrating_Mutt_with_Org-mode/)
    by [stefano zacchiroli](http://upsilon.cc/~zack/)
-   Converting html tables to org-mode is difficult, it is often
    easier to first convert to cvs using Seb Sauvage [html2csv.py
    ](http://sebsauvage.net/python/html2csv.py).
-   [Tufte Org Mode](https://github.com/tsdye/tufte-org-mode)
    is a front end for
    {{< iref "latex#tufte" "Tufte Latex" >}}

## Slides with Org Mode {#org-mode_slides}
There are many ways to produce slides with an org mode formatted text;

-   [Beamer presentations in org-mode
    ](http://orgmode.org/worg/exporters/beamer/tutorial.html)
    may be the more achieved. It uses the
    {{< iref "latex#beamer" "LaTeX class Beamer" >}}.
    It allow to deal with the Beamer complexity at an higher level.
    Some complicated layout can be achieved from Org Mode,
    but it definitely needs that you conceive a source text, very customized for the backend.
    <br />
    To my own taste this mode is convenient if your initial intent is to produce
    a Beamer presentation. If you just want to produce a document with distinct
    outputs as a running pdf, an html, __and__ some presentation, using org-beamer
    can be to much demanding.
-   There is also a Worg tutorial titled
    [Writing Non-Beamer presentations in org-mode](http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html) by Eric Schulte,
    that introduces shortly Epresent and
    {{< iref "html#s5" "S5 presentations" >}} .
-   [Epresent](https://github.com/eschulte/epresent) is an Emacs minor mode
    for giving presentations inside the Emacs Window.
-   [org-s5](https://github.com/sigma/org-s5) by Yann Hodique
    provides a glue to produce {{< iref "html#s5" "S5 based presentations" >}}
    from Org-Mode files.
-   An [altered version of Org-mode's existing html export to produce static S5](http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html#sec-3-1)
    is described in
    [Writing Non-Beamer presentations in org-mode](http://orgmode.org/worg/org-tutorials/non-beamer-presentations.html)
    and available in Eric Schulte's [org-s5 git repository](https://github.com/eschulte/org-S5).
-   [org-html5presentation.el](https://gist.github.com/509761) by Dominik Carsten
    is an Exporter of Org-mode documents to
    [HTML5 slide show presentations](http://www.html5rocks.com/en/features/presentation).
    There is also a
    [fork of org-html5presentation.el](https://github.com/twada/org-html5presentation.el).
-   [org-slidy](https://github.com/dov/org-slidy) by Dov Grobgeld produces Slidy Slideshow.
    There is  an example of
    [Interactive slide shows with R, Org mode , and Slidy](http://tucker-kellogg.com/blog/slideshow/org-gvis.html)
    by Greg Tucker-Kellogg.
-   The javascript and css of
    [org-info-js](http://orgmode.org/worg/code/org-info-js/)
    allow to play the produced HTML as
    [Presentation](http://orgmode.org/worg/code/org-info-js/#sec-12).
    It is a very light way of producing a presentation without
    adding anything to your source code.

## Org Mobile

-   [Mobile.org](http://mobileorg.ncogni.to/),
    [Mobile.org documentation](http://mobileorg.ncogni.to/),
    [Org Manual: Mobile.org](http://orgmode.org/manual/MobileOrg.html)
-   [Mobile.org for android](https://github.com/matburt/mobileorg-android/wiki/)
-   [Scripting · matburt/mobileorg-android Wiki · GitHub
    ](https://github.com/matburt/mobileorg-android/wiki/Scripting)

# Org Export
-   [Trello](https://trello.com/) GTD with  lists filled with cards
    has a bidirectional synch wit
    [org-trello](http://org-trello.github.io/),
    [GitHub: org-trello](https://github.com/org-trello/org-trello)
-   [toodledo](http://www.toodledo.com/) online to-do list with
    [org-toodledoo](https://github.com/christopherjwhite/org-toodledo)
    syncing to emacs.

# Notes Html Export

-   [Publishing](http://orgmode.org/org.html#Publishing) has its own
    settings that are configured thru
    [org-publish-project-alist](http://orgmode.org/org.html#Project-alist)
    [Bert Hansen's settings](http://doc.norang.ca/org-mode.html#sec-14_5)
    are interesting examples of publishing configuration.  See also
    the tutorial
    [Publishing Org-mode files to HTML
    ](http://orgmode.org/worg/org-tutorials/org-publish-html-tutorial.html)
-   For __publishing__ we use  [org-publish-project-alist
    ](http://orgmode.org/org.html#Project-alist)  to get a custom format.
    But for standard publishing we can use `OPTIONS` and `BIND`.
    - I avoid toc and numbered headers in html and set my custom title
        author email and date with:

             #+OPTIONS: toc:nil num:nil author:nil
             #+TITLE: My Title
             #+DATE: 2099-04-01
             #+EMAIL: me@mymbox.org

     -   But I don't like the postamble provided that default to:

             (("en" "<p class=\"author\">Author: %a (%e)</p>
             <p class=\"date\">Date: %d</p>
             <p class=\"creator\">Generated by %c</p>
             <p class=\"xhtml-validation\">%v</p>
             "))

    -   So I set it with:

             #+BIND  org-export-html-postamble-format (("en" "<p class=\"date\">Last changed: %d</p>"))

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
