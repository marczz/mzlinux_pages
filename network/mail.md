---
title: Mail
---

# SMTP {#smtp}

-   Wikipedia: {{< wp "Simple Mail Transfer Protocol" >}},
    {{< wp "Extended_SMTP"  "ESMTP" >}},{{< wp "SMTP Authentication" >}},
    {{< wp "Simple Authentication and Security Layer" >}} (SASL),
    {{< wp "STARTTLS" >}}
-   The *smtp* protocol is fiven by two base RFCs:
    [RFC 821 - Simple Mail Transfer Protocol (SMTP)
    ](http://www.ietf.org/rfc/rfc0821)
    updated by
    [RFC 2821 - Simple Mail Transfer Protocol (SMTP)
    ](http://tools.ietf.org/html/rfc2821).
    The message format itself is given by the
    [RFC 2822](http://tools.ietf.org/html/rfc2822) which
    obsolete the older rfc 822.
-   There are numerous extensions (look at next entry to have RFC
    references), among them:
    [RFC 1652 - SMTP Service Extension for 8bit-MIMEtransport
    ](http://tools.ietf.org/html/rfc1652),
    [RFC 3207 - SMTP Service Extension for Secure SMTP over Transport
    Layer Security](http://tools.ietf.org/html/rfc3207)
    (STARTTLS)
-   __DANE__ is short for "DNS-based Authentication of Named Entities". DANE establishes
    a downgrade-resistant method to verify an SMTP servers identity before it starts to
    transport an email message.
    -   [DANE for SMTP How To
        ](https://github.com/internetstandards/toolbox-wiki/blob/master/DANE-for-SMTP-how-to.md)
    -   [DANE SMTP Validator](https://dane.sys4.de) sheck mail servers against
        [common mistakes](https://dane.sys4.de/common_mistakes).
-   [MTA-STS (RFC8461)](https://tools.ietf.org/html/rfc8461) is a new standard that
    makes it possible to send downgrade-resistant email over SMTP. In that sense, it is
    like an alternative to DANE.
    -   [MTA-STS validator](https://aykevl.nl/apps/mta-sts/).

# Mail User Agents

My {{< iref "mutt" "Mutt page" >}}

-   Wikipedia: {{< wp "Comparison of e-mail clients" >}} and {{< wp "Webmail" >}},
    {{< wp "Mixmaster anonymous remailer" >}}
-   E-mail storage systems from Wikipedia: {{< wp "maildir" >}}, {{< wp "mbox" >}},
    {{< wp "MH_Message_Handling_System"  "mh" >}}, {{< wp "MIX_(Email)"  "mix" >}}
    _an hybrid between mbox and maildir used as imap backend_.
-   [ArchWiki: List of email clients
    ](https://wiki.archlinux.org/index.php/List_of_applications#Email_clients)
-   [Comparing Mail Back Ends
    ](http://www.gnu.org/software/emacs/manual/html_node/gnus/Comparing-Mail-Back-Ends.html)
    from [Gnus Manual](http://www.gnu.org/software/emacs/manual/html_node/gnus/)
-   [aerc](https://aerc-mail.org/)
    is a terminal mail client with support for IMAP, Maildir, SMTP, and sendmail
    transfer protocols. It has Vim-style keybindings and render HTML emails with an
    interactive terminal web browser, highlight patches with diffs, and browse with an
    embedded less session. _aerc is in Debian._
    -   [aerc - sourcehut git](https://git.sr.ht/~sircmpwn/aerc).
    -   _aerc_ documentation is in the man pages; their source is in
        [aerc/doc](https://git.sr.ht/~sircmpwn/aerc/tree/master/item/doc).
    -   [aerc miling list](https://lists.sr.ht/~sircmpwn/aerc), the irc is `#aerc2` on
        freenode.
-   [Alpine](http://www.washington.edu/alpine/)
    (apache license) from Washington University is the successor of
    [Pine](http://www.washington.edu/pine/)
    (free software with half-closed license!)
    -   Now the development of Alpine continue in a fork:
        [re-alpine](http://sourceforge.net/projects/re-alpine/),
        [re-alpine git repo
        ](http://sourceforge.net/p/re-alpine/code/ci/master/tree/).
    -   [ArchWiki: Alpine](https://wiki.archlinux.org/index.php/Alpine).
-   [cone - COnsole Newsreader And Emailer](http://www.courier-mta.org/cone/)
    (GPL) handles local mail folders, maildirs, IMAP and POP3
    accounts, and Usenet newsgroups.  Cone shares a lot of its code
    base with the Courier mail server.  and supports SSL/TLS and SASL,
    PGP/GPG based encryption, and digital signatures.
-   <a name=gnus"></a>[Gnus](http://www.gnus.org/) by Lars Magne Ingebrigtsen.
    -   [Gnus Manual](http://www.gnu.org/software/emacs/manual/html_node/gnus/)
    -   [Practical guide to use Gnus with Gmail
        ](https://github.com/redguardtoo/mastering-emacs-in-one-year-guide/blob/master/gnus-guide-en.org)
        in [Master Emacs in one year
        ](https://github.com/redguardtoo/mastering-emacs-in-one-year-guide/blob/master/guide-en.org)
        by 陈斌 Chen bin.
    -   [EmacsWiki: GnusGmail](https://www.emacswiki.org/emacs/GnusGmail)
-   [S-nail](http://sourceforge.net/projects/s-nail/) ([open source Licence
    ](http://sourceforge.net/p/s-nail/code/ci/master/tree/COPYING))
    is the continuation of [Heirloom mailx](http://heirloom.sourceforge.net/mailx.html)
    from the [Heirloom project](http://heirloom.sourceforge.net/) ([CDDL
    ](http://en.wikipedia.org/wiki/Common_Development_and_Distribution_License))
    _a set of unix sys V compliant tools no longer developped since 2009_

    _S-nail_ also packaged with the previous name _Heirloom mailx_ is a mail user agent
    with an interface like the original Berkeley mailx, but that supports mime, imap,
    pop3, ssl, s/mime. It was previously known as *nail*.
    -   [S-nail git repo](http://sourceforge.net/p/s-nail/code/ci/master/tree/)
    -   [Using Mailx with Gmail](http://forums.debian.net/viewtopic.php?f=16&t=103322)
    -   [ArchWiki: S-nail](https://wiki.archlinux.org/index.php/S-nail)
-   <a name="mu4e"></a>
    [mu4e (documentation)](http://www.djcbsoftware.nl/code/mu/mu4e/index.html)
    is an emacs-based e-mail clien based on the
    [mu](http://www.djcbsoftware.nl/code/mu) e-mail indexer/searcher
    by  Dirk-Jan Binnema (djcb)
    -   [introducing mu4e
        ](http://emacs-fu.blogspot.fr/2012/08/introducing-mu4e-for-email.html)
        by djcb.
    -   [mu4 for Gmail guide in StackExchange
        ](http://emacs.stackexchange.com/a/12932)
    -   [EmacsWiki: mu4e](http://www.emacswiki.org/emacs/mu4e)
    -   [Mu CheatSheet](http://www.djcbsoftware.nl/code/mu/cheatsheet.html)
-   [mailfilter](http://mailfilter.sourceforge.net/) (GPL) a spam filter.
-   [Roundcube](https://roundcube.net/) (GPL)
    is a browser-based multilingual IMAP client.
    -   [Archwiki: Roundcube](https://wiki.archlinux.org/index.php/Roundcube).
-   [Sup](http://supmua.org/) (GPL)
    is a console-based email client written in ruby.
    It uses a list of threads, which are each hierarchical collections email messages.
    Threads can have multiple tags applied to them (_Reminiscent from Gmail_).
    -   [Sup Wiki](https://github.com/sup-heliotrope/sup/wiki).
    -   [GitHub: Sup](https://github.com/sup-heliotrope/sup/)
    -   [ArchWiki: Sup](https://wiki.archlinux.org/index.php/Sup)
-   [Mozilla Thunderbird](http://en.wikipedia.org/wiki/Mozilla_Thunderbird)
    (MPL/GPL/LGPL),
    [Thunderbird Home](http://www.mozilla.com/thunderbird/)
    cross-platform e-mail and news client.
    -   [ArchWiki: Thunderbird
        ](https://wiki.archlinux.org/index.php/Thunderbird).

# Temporary email adresses
-   [jetable.org](http://www.jetable.org/en/index),
    ([fr](http://www.jetable.org/fr/index)),
    [guerilla.com](https://www.guerrillamail.com/),
    [10minutemail.com](http://10minutemail.com/),
    [mailnull.com](https://mailnull.com/)
    -   [1sec MAIL](https://www.1secmail.com/) provide you with a temporary disposable
        email address receive emails at this temporary address, after certain period of
        time email will be delated and address will be canceled.
        [sdushantha/tmpmail](https://github.com/sdushantha/tmpmail)
        is a sh script which creates an address on _1sec MAIL_, and send and receive
        message at this address. It uses _curl_, _w3m_, and yhr json procesor
        [jq](https://github.com/stedolan/jq).
    -   [more sites on google
        ](https://www.google.com/search?q=mail+temporary+disposable)

# Mail search tools {#mail_search}
-   [mairix](http://www.rpcurnow.force9.co.uk/mairix/index.html) (GPL)
    is a program for indexing and searching email messages
    stored in {{< wp "maildir" >}}, [MH Message Handling System] or {{< wp "mbox" >}} folders.
-   [Notmuch](http://notmuchmail.org/) is an efficient mail indexer. It comes with an
    [emacs message reading client](http://notmuchmail.org/emacstips/)
    _notmuch.el_, but can be used with many imap email clients as
    _gnus_, or _mutt_.
    Notmuch is packaged in Debian.
    -   [ArchWiki: Notmuch
        ](https://wiki.archlinux.org/index.php/Notmuch)
-   [mu](https://github.com/djcb/mu) (GPL)
    is a {{< wp "maildir" >}} indexer/searcher, it also includes the emacs client
    {{< iref "#mu4e" "mu4e" >}}, and can also be used with
    {{< iref "mutt" "Mutt" >}} or _WanderLust_.
    _mu_ is available in Debian/Ubuntu under the name _maildir-utils_.

# Mail filtering
-   [Gentoo Wiki: Mailfiltering Gateway
    ](https://wiki.gentoo.org/wiki/Mailfiltering_Gateway)
-   [Procmail home page](http://www.procmail.org/)
    -   [Procmail at alcor
        ](http://alcor.concordia.ca/topics/email/auto/procmail/)
    -   [Panix](http://www.panix.com)  procmail spam filter:
        [responding to UCE rules](http://www.panix.com/uce.html);
    -   [Timo Salmi's procmail tips
        ](http://www.netikka.net/tsneti/info/proctips.php)
    -   [Procmail Resource File Builder
        ](http://www.troubleshooters.com/emailtech/procmail_maker.htm)
        is intended to organize your procmail rules.
-   [Bogofilter](http://bogofilter.sourceforge.net/) is a mail filter
    written in C _in debian_.
-   [Spam Assassin](http://www.spamassassin.org/) written in perl, and
    so very slow, but well maintained _in debian_.
-   [Mail Scanner](http://www.mailscanner.info/) perl script that
    integrates spam assassin and virus scanners.
    [MailWatch](http://mailwatch.sourceforge.net/) is a web-based
    front-end to MailScanner.
-   [Tagged Message Delivery Agent (TMDA)](http://www.tmda.net/) use
    white/black lists, challenge response for unknown senders and tagged
    addresses for temporary or limited scope email communication.
-   [Postfix Add-on Software](http://www.postfix.org/addon.html)
-   [Postfix Anti-UCE
    Cheat-Sheet](http://jimsun.linxnet.com/misc/postfix-anti-UCE.txt) by
    Jim Seymour

# Mail Notification
We can use a system notification monitor to get mail notification,
references are given in the
{{< iref "monitoring" "Monitoring section" >}} for
{{< iref "monitoring#conky" "conky" >}},
{{< iref "monitoring#gkrellm" "gkrellm" >}};
and in {{< iref "desktop" "Desktop section" >}} for
{{< iref "desktop#i3_wm" "i3bar or i3blocks" >}},
{{< iref "desktop#dzen" "dzen" >}}.

These tools can be a good choice if you want to have a light mail
notification daemon as the are weighting only
1.5M for dzen2, 4M for conky, 20M for gkrellm.


-   Mail notification is done by programs inherited from
    [biff](http://en.wikipedia.org/wiki/Biff_(computing))
    and all its improvements xbiff, xlbiff, kbiff, gnubiff, wmbiff and xbuffy.
-   [checkgmail](http://checkgmail.sourceforge.net/)
    is a perl/gtk  Gmail Notifier in systray using gmail atom feeds.
    Marking as read, archiving, deleting or reporting as spam can be
    carried out directly within CheckGmail. It is in Debian.
-   [gnubiff](http://gnubiff.sourceforge.net/ "gnubiff.sourceforge.net Home")
    (GPL v3) from Nicolas Rougier includes notification for pop3, apop,
    imap4, mh, qmail and mailfile, with multiple mailboxes. It can be
    used from the terminal (tty) or with X, using GTK or gnome when
    available. It has full SSL and certificates support. I use it to
    check both my local, pop3 and imap mboxes. It works well with
    gmail. An interresting feature of newbiff is that it shows an
    excerpt of your new mail when you click upon the notification, so
    you can dispense to launch your email client for many mails. But
    when you use it with gtk it uses 20M of resident memory, to compare
    with the 5M of mutt (with imap), or with gkrellm which is of the
    same size but for which mail-notification is a feature among many.
    By using the `--nogui` option, you get a 4.3M resident program, but
    with only the bell notification, it is a very spartan interface,
    which can make you prefer to keep a mutt terminal open.
-   [Kbiff](http://www.granroth.org/kbiff/ "granroth.org kbiff") is
    a mail notification utility for the KDE, it support pop3, imap4,
    ssl. Kbiff can be build without kde (but with qt!), resident size
    is 17M. I have been unable to connect to gmail by imap-ssl with it.
-   [Gbuffy from](http://www.fiction.net/blong/programs/gbuffy/ "fiction.net gbuffy")
    [Brandon Long](http://www.fiction.net/ "fiction.net Home") is also
    a xbiff improvement with imap support but it is no more developed
    since 2003 so it is still using GTK 1.2 and has no ssl support.
-   [Gmail Notifier](http://gmail-notify.sourceforge.net/) (GPL)
    alias _gmail-notify_, but different from the next piece of software,
    is a python/pyGtk notifier for Gmail. It is in Debian.
-   [gmailnotify](https://github.com/knopwob/gmailnotify)
    by Sascha Kruse is a python notifier for Gmail that uses the notify dbus framework.
    _now an abandoned project_.
-   [mailnag](https://github.com/pulb/mailnag) (GPL)
    checks  POP3  and IMAP servers for new mail.
    It is a Gnome3 application that uses the dbus notification framework.
    while being labeled _Gnome3_, it has quite few gnome dependencies except the
    _gir1_ libraries. mailnag is in Debian.
-   [mailnotify](http://www.nongnu.org/mailnotify) (GPL)
    is a mail notification in freedesktop systray for local mail,
    pop3, imap, gmail...  It is a featurefull product,
    but with heavy dependencies. It is provided in the
    _mail-notification_ package.
-   [newmail](http://www.infodrom.org/projects/newmail) (GPL)
    by Joey Schulze is a biff like program for local mailboxes. It is in Debian.
-   [Trysterobiff](https://bitbucket.org/gsauthof/trysterobiff/src) (GPL)
    is a cross-plattform non-polling (IMAP Idle) new-mail systray notifier, built with QT toolkit.
-   [Wmbiff](http://wmbiff.sourceforge.net/ "wmbiff.sourceforge.net")
    (GPL) is a mail notifier running as an applet for wmaker. It
    supports pop3/imap with ssL. Wmbiff uses only 4M of resident size,
    which makes it among the lightest email notifier. It can check up
    to 5 mailboxes, and is easily configurable. I use it to check local
    and imaps mboxes (including gmail).



# MTA and Mail administration {#MTA}
-    Wikipedia: {{< wp "Message transfer agent" >}},
    {{< wp "MIME"  "Multipurpose Internet Mail Extensions (MIME)" >}}
-   [Debian Wiki: Default MTA discussion
    ](https://wiki.debian.org/Debate/DefaultMTA) compares postfix,
    exim4, sendmail, nullmailer, Dma, ssmtp.
-   [Gentoo Wiki: Complete Virtual Mail Server
    ](https://wiki.gentoo.org/wiki/Complete_Virtual_Mail_Server)
    a full manual distributed in subpages.
-   {{< wp "Qmail" >}} ({{< wp "public domain" >}}) [Qmail Home](http://www.qmail.org/top.html) smtp server and replacement for sendmail by {{< wp "Daniel J. Bernstein" >}}.
-   [Maildir format](http://cr.yp.to/proto/maildir.html) ,
    [maildir(5) man page from qmail](http://www.qmail.org/man/man5/maildir.html)
-   [Bongo](http://bongo-project.org/)
    (GPL) the continuation of previous Novell {{< wp "Hula" >}} is a
    server-side e-mail and calendaring server, and a web GUI for
    accessing your e-mail and calendar.
-   [OpenSMTPD](https://www.opensmtpd.org/)
    is a complete smtp implementation, part of openBSD he is also
    available in other BSD flavors and linux including a Debian
    package.
    -   [OpenSMTPD manual pages
        ](https://www.opensmtpd.org/manual.html).
    -   [OpenSMTPD FAQ
        ](https://www.opensmtpd.org/faq/index.html).

## Exim
{{< wp "Exim" >}} (GPL) the default MTA on Debian.

-   [Exim Home page](http://www.exim.org/index.html)
-   [Exim Specification i.e exim Manual
    ](http://www.exim.org/exim-html-current/doc/html/spec_html/)
-   [Exim FAQ](https://github.com/Exim/exim/wiki/FAQ)
-   [Exim Wiki](https://github.com/Exim/exim/wiki)
-   [Exim 4 for Debian README
    ](http://pkg-exim4.alioth.debian.org/README/README.Debian.html)
-   [Debian Wiki: Exim](https://wiki.debian.org/Exim)
-   [Ubuntu/Debian Exim 4 Configuration
    ](http://koivi.com/exim-4-on-ubuntu-debian) by Justin Koivisto.
-   [ArchWiki: Exim with Remote SMTP server
    ](https://wiki.archlinux.org/index.php/Exim_with_Remote_SMTP_server).

##  Postfix {#postfix}
-   [The Postfix Home Page](http://www.postfix.org/),
    [Postfix Documentation](http://www.postfix.org/documentation.html)
    README FILES and
    [Manual Pages](http://www.postfix.org/postfix-manuals.html),
    [Postfix Howtos and FAQs](http://www.postfix.org/docs.html).
-   Some [postfix.org](http://www.postfix.org/) selected pages:
    [Postfix XCLIENT Howto](http://www.postfix.org/XCLIENT_README.html),
    [Postfix XFORWARD Howto](http://www.postfix.org/XFORWARD_README.html),
    [Postfix TLS Support](http://www.postfix.org/TLS_README.html)
-   [Jim Seymour](http://jimsun.linxnet.com/):
    [postfix contribs](http://jimsun.linxnet.com/postfix_contrib.html),
    [Postfix Anti-UCE Cheat Sheet
    ](http://jimsun.linxnet.com/misc/postfix-anti-UCE.txt)
-   gentoo:   [Gentoo mailfiltering gateway guide: configuring postfix
    ](https://wiki.gentoo.org/wiki/Mailfiltering_Gateway#Configuring_Postfix),
    [Complete Virtual Mail Server/Postfix to Database
œ    ](https://wiki.gentoo.org/wiki/Complete_Virtual_Mail_Server/Postfix_to_Database)

Common postfix admininistration commands
:   The most used commands taken from
    [Manual Pages](http://www.postfix.org/postfix-manuals.html) are:

    -   [postcat(1)](http://www.postfix.org/postcat.1.html), examine
        Postfix queue file.
    -   [postqueue(1)](http://www.postfix.org/postqueue.1.html), Postfix
        mail queue control, used to start manually a delivery with
        `postqueue -f`.
    -   [postsuper(1)](http://www.postfix.org/postsuper.1.html), Postfix
        housekeeping, used to delete mail with ` postsuper -d queue_id`,
        you can get the *queue\_id* with `mailq`.
    -   [mailq(1)](http://www.postfix.org/mailq.1.html), List the mail
        queue.
    -   [sendmail(1)](http://www.postfix.org/sendmail.1.html), Sendmail
        compatibility interface. Use it as:
        `cat message_file | sendmail -i -f enveloppe_sender recipient`.

# Pop3 and Imap

-   [Wikipedia: Pop3](http://en.wikipedia.org/wiki/Pop3),
-   [Imap](http://en.wikipedia.org/wiki/Imap),
-   [RFC 1939 Post Office Protocol - Version 3
    ](http://tools.ietf.org/html/rfc1939),
    look at wikipedia page for other rfcs.
-   {{< wp "Dovecot_(software)"  "Dovecot" >}} (MIT and LGPL)
    is an open source IMAP and POP3 server for Linux
    -   [Dovecot Home](http://dovecot.org/).
    -   [ArchWiki: Dovecot
        ](https://wiki.archlinux.org/index.php/Dovecot).
    -   [Email Troubleshooting, Including IMAP, Dovecot, and Linux
        ](http://www.troubleshooters.com/emailtech/imap_troubleshooting.htm)
        by Steve Litt.
-   [Fetchmail](http://www.fetchmail.info/)
    is a remote-mail retrieval and forwarding utility intended to be
    used over on-demand TCP/IP links
-   [TeaPop](http://teapop.1my.net/)is an RFC1939 and
    RFC2449 compliant POP3-server with MySql, PostgreSQL, and Apache
    htpasswd authentication support.
-   [tpop3d](http://savannah.nongnu.org/projects/tpop3d/)is a pop3
    server that uses apam, passwd, amysql, or pgsql to authentificate
    and can use mailspools or maildirs.
-   [Imap at university of Washington](http://www.washington.edu/imap/)
-   [isync](http://isync.sourceforge.net/) (GPL)
    Synchronize a local maildir with a remote IMAP4 mailbox.
    -   [Migrating from offlineimap to mbsync for mu4e
        ](http://pragmaticemacs.com/emacs/migrating-from-offlineimap-to-mbsync-for-mu4e/)
-   [OfflineImap](http://offlineimap.org/)
    synchronize imap maiboxes from multiple computers.
    -   [OfflineImpap repository at GitHub
        ](https://github.com/OfflineIMAP/offlineimap)
    -   [OfflineImap latest documentation
        ](https://offlineimap.readthedocs.org/en/latest/)
    -   [ArchWiki OfflineIMAP
        ](https://wiki.archlinux.org/index.php/OfflineIMAP).


# SMTP relays and Null Mailers {#smtp_relays}
<a name="null_mailers"></a>
A _null mailer_ is a replacement MTA for hosts, which relay to a fixed
set of smart relays the following smtp agents _nullmailer_, _msmtp_,
_ssmtp_, _emsmtp_, _DragonFly Mail Agent (dma)_ can act as null
mailers.

These smtp relay are not full fledged SMTP servers, so they do not
listen on port 25 for incoming connections.

You can also use standard MTA with a remote smtp server like described
in [ArchWiki: Exim with Remote SMTP server
](https://wiki.archlinux.org/index.php/Exim_with_Remote_SMTP_server).

[ArchWiki: cron](https://wiki.archlinux.org/index.php/Cron) describe
how to deal with root mails sent by cron with the smtp relay agents.

-   [DragonFly Mail Agent (dma)](https://github.com/corecode/dma)
    packaged in Debian as _dma_ is a small Mail Transport Agent
    (MTA). It accepts mails from local Mail User Agents (MUA) and
    delivers the mails either locally or to a remote smtp server it
    features TLS/SSL support and SMTP authentication.
    _active in 2017_.

    -   [Using the DragonFly Mail Agent as default MTA in Debian
        ](https://wiki.debian.org/Debate/DefaultMTA/DMA)
        discusses the pros and cons of dma.

    A feature of dma, that is missing in other smtp only MTA or _null
    mailers_, is that it is able to do local delivery. So it can be
    used on a small server when you want to keep the cron mail local.
    This feature is also available with esmtp.
    It can also in the same way than others _null mailers_ deliver to
    a _smart host_.

-   [esmtp](http://esmtp.sourceforge.net/manual.html) is a
    relay-only Mail Transfer Agent (MTA),
    [supporting startTLS
    ](http://esmtp.sourceforge.net/manual.html#using-the-starttls-extension),
    with a sendmail compatible syntax. _esmtp_ is based on
    [libesmtp](http://www.stafford.uklinux.net/libesmtp/) _(GPL)_.
    Esmtp can do direct local delivery, by using a local delivery
    agent. _procmail_ is usually used for this task with a
    configuration option `mda "/usr/bin/procmail -d %T"`.
    _support of esmtp stopped beginning 2010._
-   [mailsend](https://github.com/muquit/mailsend)
    is a simple command line program to send mail via SMTP protocol.
    It support ESMTP authentication and IPV6. _Active in 2019_.
-   <a href="#msmtp"></a>[msmtp](http://msmtp.sourceforge.net/)
    _(GPL v3)_ is a SMTP client (or *mail sending agent* or
    *relay-only MTA* ) that transmits a mail to an SMTP server which
    does the delivery. _msmtp_ supports tls encrypted connections with
    Openssl or GnuTLS.  _msmtp_ allow to use multiple smtp
    accounts. Debian has a _msmtp_ package, a _mstp-gnome_ package
    which is compiled with gnome-keyring support, and the MTA is in a
    separate package _msmtp-mta_. _A new release in 2019._
    -   [msmtp manual](http://msmtp.sourceforge.net/doc/msmtp.html).
    -   [ArchWiki: msmtp](https://wiki.archlinux.org/index.php/Msmtp).
    -   [Configuring msmtp on Ubuntu
        ](https://xand.es/2016/05/09/configuring-msmtp/).
    -   [The Quick-N-Dirty Guide to Using mutt with gmail
        ](http://www.scottro.net/qnd/qnd-gmail.html)
        explains how to configure msmtp to deliver to gmail mail
        server.
    -   The Emacs wiki use _msmtp_ in emacs for configuring
        [multiple SMTP accounts
        ](https://www.emacswiki.org/emacs/MultipleSMTPAccounts).
    -   [Command Line Gmail Using msmtp/mailx
        ](http://www.klenwell.com/is/UbuntuCommandLineGmail)
-       [OAuth2 authentication for offline email clients
        ](https://jrvcomputing.wordpress.com/2016/11/21/oauth2-authentication-for-offline-email-clients/)
        uses [cscorley/send.py](https://github.com/cscorley/send.py) _2014_
         to access gmail with Oauth2 authentication.
    -   [mir.msmtpq](https://github.com/darkfeline/mir.msmtpq)
        is a python drop-in  replacement for sendmail or msmtp. Unlike
        sendmail or msmtp, msmtpq will only queue messages. It is in
        PyPi.
-   [nbsmtp](https://wiki.archlinux.org/index.php/NBSMTP)
    (archwiki page) is a relay-only Mail Transfer Agent with ssl and
    tls support. _stopped in 2015, home page unreachable._
-   [nullmailer
    ](http://untroubled.org/nullmailer/)
     is a sendmail/qmail/etc replacement MTA for hosts which relay to
     a fixed set of smart relays. _packaged in Debian an is active in
     2018_.
    -   [GitHub:  bruceg/nullmailer
        ](https://github.com/bruceg/nullmailer)
    -   [Nullmailer, Mutt, and Automated Email: The Tiny Mail Transfer
        Agent](http://www.troubleshooters.com/linux/nullmailer/)
    -   [Nullmailer Landmine Map
        ](http://www.troubleshooters.com/linux/nullmailer/landmines.htm)
        is a repair manual for Nullmailer.
-   [qpsmtpd](http://smtpd.github.io/qpsmtpd/)
    is a flexible smtpd daemon written in Perl.  which installs
    alongside a MTA such as Exim, Postfix or Qmail, or used as an SMTP
    proxy for a remote/DMZ MTA.  The qpsmtpd damon emphasizes spam
    detection during the SMTP transaction. _active in 2017_.
    -   [GitHub: qpsmtpd](https://github.com/smtpd/qpsmtpd).
-   [ssmtp](http://packages.qa.debian.org/s/ssmtp.html)
    is a send-only sendmail emulator. It accepts a mail stream on
    standard input with recipients specified on the command line and
    synchronously forwards the message to the mail transfer agent of
    a mailhub. It is abandoned since 2011, [ArchLinux Wiki][AW ssmtp]
    propose to replace it by {{< iref "#msmtp" "mstmtp" >}}.
    -   [ArchLinux Wiki: Ssmtp][AW ssmtp]
        _gives the configuration to forward to gmail_,
    -   [The Quick-N-Dirty Guide to ssmtp
        ](http://www.scottro.net/qnd/qnd-ssmtp.html),
    -   [ssmtp(8)](http://linux.die.net/man/8/ssmtp).

# Mail providers
-   {{< wp "Comparison of webmail providers" >}}
-   [Serverlist | dismail.de](https://dismail.de/serverlist.html)
    gives the security features of email providers.
-   [Posteo](https://posteo.de/en) uses only open-source software and
    offers support for
    [DNSSEC](https://en.wikipedia.org/wiki/Domain_Name_System_Security_Extensions)/
    [DANE](https://en.wikipedia.org/wiki/DNS-based_Authentication_of_Named_Entities) and
    S-Mime and {{< wp "PGP" >}} (through {{< wp "Mailvelope" >}} ) in the web interface,
    which is running {{< wp "Roundcube" >}}.
    Additionally they offer two-factor-authentication via
    {{< wp "Time-based One-time Password Algorithm" >}} _TOTP_ and use
    {{< wp "Extended Validation Cerificates" >}} and
    {{< wp "HTTP Public Key Pinning" >}} for the https connection.

    An account is billed 12€/yearly with 2GB (3€/year*GB for extra storage) 2 email
    adresses (1€20/year for additional adresses) 3 calendars (1€20/year for additional
    calendar), attachments of up to 50 MB, MAP/POP3 support, spam and virus filter,
    unlimited addresse filters, support via email.

    An AES encrypted adress book which can be can be synchronised using CardDAV.
    In the same way the calendar can be AES encrypted and synchronized with CalDav.

    -   [Email accounts features](https://posteo.de/en/site/features).

-   {{< wp "protonMail" >}} is an end-to-end encrypted email service which uses
    ProtonMail uses a combination of public-key cryptography and symmetric encryption.
    Emails sent from ProtonMail to non-ProtonMail email addresses may optionally be sent
    in plain text or with end-to-end AES encryption wit a  a previously exchanged
    password.

    There is a Free plan with limits of 150 mails/day, 3 folders, 20 labels, 500MB
    storage. For 45€/yearly you get 5GB storage, and VPN connection.

    -   [ProtonMail Home](https://protonmail.com/)

-   {{< wp "Tutanota" >}}  offers end-to-end encryption for emails sent from one Tutanota
    user to another. It uses  symmetrical and an asymmetrical algorithm - AES with a
    length of 128 bit and RSA with 2048 bit. To external recipients who do not use
    Tutanota a notification is sent with a link to a temporary Tutanota account. After
    entering a previously exchanged password, the recipient can read the message and
    reply end-to-end encrypted.

    There is a Free plan with 1GB storage and limited search, the free plans are deleted
    after 6 monts of inactivity. For 12€/yearly you get unlimited serch, multiple
    calendars, 5 aliases, and email support. _price 2021_.
    -   [Tutanota Home](https://tutanota.com/).



[AW ssmtp]: http://wiki.archlinux.org/index.php/SSMTP

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
