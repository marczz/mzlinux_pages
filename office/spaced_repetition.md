---
title: Spaced Repetition
---

{{% toc /%}}

# References
-   Wikipedia: {{< wp "Memory" >}}, {{< wp "Memory improvement" >}}, {{< wp "Memorization" >}},  {{< wp "Rote learning" >}},
    {{< wp "Mnemonic" >}},{{< wp "Mnemonic major system" >}}
-   The {{< wp "Art of memory" >}} is the use of mnemotechnics, this
    Wikipedia article summarize the differents techniques like the
    {{< wp "Method of loci" >}} which is a general designation for mnemonic
    techniques that rely upon memorized spatial relationships to
    establish, order and recollect memorial content.
-   {{< wp "Spaced repetition" >}} is a learning technique that incorporates
    increasing intervals of time between subsequent review of previously
    learned material. It is used in {{< wp "Flashcard" >}} Software.
    Wikipedia has a {{< wp "List of flashcard software" >}}, the two
    outstanding Open Source Software being Anki and Mnemosyne.
-   An other application is {{< wp "Incremental reading" >}} only available in
    SuperMemo and Org-drill _and in alpha state in an Anki plugin_.

# Flashcard principles.
-   [SuperMemo Twenty rules of formulating knowledge](http://www.supermemo.com/articles/20rules.htm)

# Main stream software.

The two more popular and achieved software are written in python
{{< wp "Anki" >}} (GNU AGPL) and  {{< wp "Mnemosyne_(software)"  "Mnemosyne" >}} (GPL).
Anki has a lot more feature. Anki 2 is based on the
[Sm2 algorithm from Piotr Wozniak](http://www.supermemo.com/english/ol/sm2.htm)
the reason to prefer it to other algorithm is
[stated in the Anki FAQ](http://ankisrs.net/docs/dev/manual.html#_what_spaced_repetition_algorithm_does_anki_use). Mnemosyne 2
use also a variant of sm2 algorithm as explained in the
[principles of MnemoSyne](http://mnemosyne-proj.org/principles.php). They
both are written with QT interface and use a sqlite3 database.

The synchronization is handled by both, but while Mnemosyne use a pair
to pair sync, Anki synchronize thru a central web interface. _Hosted Proprietary
web interface_.

They also both allow plugins but the
[Anki library of plugins](https://ankiweb.net/shared/addons/)
is a lot richer than the
[Mnemosyne plugins list](http://mnemosyne-proj.org/scripts-and-plugins).

-   Three comparisons of Anki an Mnemosyne _but not using the new
    release of each software, which are quite recent_ in
    -   [Anki vs. Mnemosyne](http://www.xamuel.com/anki-vs-mnemosyne/)
     by Sam Alexander (2009)
    -   [Review of Mnemosyne vs. Anki vs. SuperMemo
    ](http://nihongoperapera.com/mnemosyne-anki-review.html)
        by Nihongo Pera Pera (fluent Japanese) (2008 updated 2009) as part
        of his
        [Memory Software Pages](http://www.nihongoperapera.com/mnemosyne.html)
        _mainly dedicated to Mnemosyne_,
    -   [Memory Reminder
    ](http://www.ubuntu-user.com/Magazine/Archive/2009/2/Mnemosyne-and-Anki)
        by David Harding in Ubuntu Magazine (2009).

You can find shared Decks either in the two mainstream sites or in some
_Deck sharing Sites_ that try to get some money from subscriptions of
users or from adds_.

-   [Mnemosyne 2 list of Decks](http://mnemosyne-proj.org/card-sets)
-   [Anki 2 shared Decks](https://ankiweb.net/shared/decks/)
-   [cueflash](http://cueflash.com/)
-   [Flashcard Exchange](http://www.flashcardexchange.com/) _Paid
    service, 20$ to use main features_ see
    [WikiPedia: Flashcard Exchange](http://en.wikipedia.org/wiki/Flashcard_Exchange)
-   {{< wp "Quizlet" >}}, [Quilet Home](http://quizlet.com/) _Adds powered_.
-   [FlashCard Machine](http://www.flashcardmachine.com/)
-   [FlashCardDb](http://flashcarddb.com/)

## {{< wp "Anki" >}}
-   [Anki 2 Home](http://ankisrs.net/anki2.html)
-   [Anki 2 Manual](http://ankisrs.net/docs/dev/manual.html)
-   [AnkiWeb: the online web interface to Anki 2](https://ankiweb.net/)
-   [Anki 2 plugin API](http://ankisrs.net/docs/dev/addons.html)
-   [Anki 2 plugins library](https://ankiweb.net/shared/addons/)
-   The sources of Anki are on GitHub:
    [Anki Plugins](https://github.com/dae/ankiplugins),
    [Libanki](https://github.com/dae/libanki),
    [Anki Docs](https://github.com/dae/ankidocs).

Out of the plugin library you can find many scripts, helpers and
plugins for Anki. Many of them are in [GitHub](https://github.com).

-   [AnkiMini](https://github.com/typerlc/ankimini)
    A small webserver for mobile devices, _not updated to Anki 2_.
-   [Anking](https://github.com/muflax/anking)
    A custom interface for anki and the related
    [anki tcp server](https://github.com/muflax/anki-server).
    The goals of Anking are
    [explained in the _muflax_ Blog](http://daily.muflax.com/log/105/).
-   [subs2srs](http://subs2srs.sourceforge.net/)
    allows you to create import files for Anki or other Spaced
    Repetition Systems (SRS) based on your favorite foreign
    language movies and TV shows.
-   [poem2anki](https://github.com/quentinsf/poem2anki)
    Convert a text file contain lines of poetry into Anki flash cards.
-   [ankilyrics](https://github.com/sobjornstad/ankilyrics)
    A script for generating Anki cards out of lyrics and poetry.

## Other software
-   [Org-drill](http://orgmode.org/worg/org-contrib/org-drill.html)
    is an extension for Org mode. Org-Drill uses a spaced repetition
    is uses the [sm5 algorithm from SuperMemo](http://supermemo.com/english/ol/sm5.htm)
    implemented in
    [org-learn](http://orgmode.org/w/?p=org-mode.git;a=blob_plain;f=contrib/lisp/org-learn.el;hb=HEAD)
-   [Learning with Texts (LWT)](http://lwt.sourceforge.net/) (Public Domain)
    is a spaced repetition software aimed at language learning.
