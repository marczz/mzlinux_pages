---
title: Spaced Repetition
---


# References
-   Wikipedia: {{< wp "Memory" >}}, {{< wp "Memory improvement" >}},
    {{< wp "Memorization" >}},  {{< wp "Rote learning" >}},
    {{< wp "Mnemonic" >}},{{< wp "Mnemonic major system" >}}.
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

## Incremental reading
 {{< wp "Incremental reading" >}} is  available in
    SuperMemo, Org-drill, and
    [incremental-reading](https://github.com/luoliyan/incremental-reading)
    Anki add-on.

# Flashcard principles.
-   [SuperMemo Twenty rules of formulating knowledge
    ](http://www.supermemo.com/articles/20rules.htm)

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
-   {{< wp "Quizlet" >}}, [Quilet Home](http://quizlet.com/) _Freemium Adds powered_.
-   [FlashCard Machine](http://www.flashcardmachine.com/)
-   [Cram.com](https://www.cram.com/)

## Anki
-   [Anki Home](https://apps.ankiweb.net/)
-   [AnkiWeb](https://ankiweb.net/) the online web interface to Anki 2.
-   [Anki Manual](https://docs.ankiweb.net/)
-   [Anki FAQ](https://faqs.ankiweb.net/)
-   [Anki 2 Addons](https://ankiweb.net/shared/addons/) _or Plugins_
-   [Anki 2 plugins library](https://ankiweb.net/shared/addons/)
-   [Anki 2 shared Decks](https://ankiweb.net/shared/decks/)
-   The sources of Anki are on GitHub:
    -   [anki](https://github.com/ankitects/anki) (AGPL3 and other opensource licenses)
    -   [anki-addons](https://github.com/ankitects/anki-addons),
        [addons-doc](https://github.com/ankitects/addon-docs).
    -   [Anki Manual](https://github.com/ankitects/anki-manual).
    -   [ankimobile-docs](https://github.com/ankitects/ankimobile-docs)

-   [Anki - ArchWiki](https://wiki.archlinux.org/title/Anki)
-    Wikipedia: {{< wp "Anki" >}}
-   [awesome-anki](https://github.com/tianshanghong/awesome-anki)
    A curated list of awesome Anki add-ons, decks and resources

-   [subs2srs](http://subs2srs.sourceforge.net/)
    allows you to create import files for Anki or other Spaced
    Repetition Systems (SRS) based on your favorite foreign
    language movies and TV shows.

-   [anki-sync-server](https://github.com/tsudoko/anki-sync-server)
    Self-hosted Anki sync server.
    -   [ankisyncd – A Custom Sync Server for Anki 2.1 | Gene Dan's Blog
        ](https://genedan.com/no-127-ankisyncd-a-custom-sync-server-for-anki-2-1/).

Out of the plugin library you can find many scripts, helpers for Anki in
[GitHub](https://github.com/search?q=%23anki&type=Repositories).

_   [poem2anki](https://github.com/quentinsf/poem2anki)
    Convert a text file contain lines of poetry into Anki flash cards.
    _Last release 2017_
-   [ankilyrics](https://github.com/sobjornstad/ankilyrics)
    A script for generating Anki cards out of lyrics and poetry.
-   [anki-templates-superlist](https://github.com/Troyciv/anki-templates-superlist)
    A collection of Anki card styles
-   [AnkiVim](https://github.com/MFreidank/AnkiVim) (MIT License)
    Use vim (or your favorite editor) to write anki cards quickly in plain text or latex.
-   [anki-connect](https://github.com/FooSoft/anki-connect) (GPL)
    Anki plugin to expose a remote API for creating flash cards.
-   [mdanki](https://github.com/ashlinchak/mdanki)
    Markdown to Anki converter.
-   [Obsidian_to_Anki](https://github.com/Pseudonium/Obsidian_to_Anki)
    Script to add flashcards from text/markdown files to Anki.
    Built with [Obsidian](https://obsidian.md/) markdown syntax in mind.

### Incremental Reading add-ons {#incremental_reading_addons}
-   [incremental-reading](https://github.com/luoliyan/incremental-reading) (ISC License)
    Anki add-on providing incremental reading features
### Dictionary add-ons
-   [ODH](https://github.com/ninja33/ODH)
    A chrome extension to show online dictionary content.
-   [FastWordQuery](https://github.com/sth2018/FastWordQuery) (GPL-3.0 License)
    Query words definitions or examples etc. from local or web dictionaries to fill
    into Anki cards.
-   [dictionariez](https://github.com/pnlpal/dictionariez) (GPL-2.0 License)
    a browser extension to look up words in all kinds of dictionaries and export
    your look-up words to Anki. Work with Firefox or Chromium, on android with
    [Kiwi](https://kiwibrowser.com/) or
    [Flow](https://play.google.com/store/apps/details?id=org.flow.browser).
-   [WordQuery](https://github.com/finalion/WordQuery)
    word fast-querying addon for anki

## Other software
Org Mode provide several
{{< iref "org-mode#spaced_repetition" "spaced repetition packages" >}}.


-   [Learning with Texts (LWT)](https://sourceforge.net/projects/learning-with-texts/)
    is a spaced repetition software aimed at language learning.
