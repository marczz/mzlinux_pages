---
title: Password strength
---
<!--
[[file:../../../../content-org/notes/security_notes/password_strength_notes.org::+hugo_front_matter_format: yaml][password strength notes]]
[[file:authentication.md::---][Authentication]]
-->
See also
{{< iref "authentication" "Authentication" >}},
{{< iref "password_managers" "Passwords Managers" >}},

# Password Strength References {#password_strength}
-   Wikipedia: {{< wp "Password strength" >}},
    [Key Size](http://en.wikipedia.org/wiki/Key_size),
    [Key strengthening](http://en.wikipedia.org/wiki/Key_strengthening),
    [Password](http://en.wikipedia.org/wiki/Password),
    [Password cracking](http://en.wikipedia.org/wiki/Password_cracking),
    {{< wp "cryptographic hash functions" >}},
    {{< wp "comparison of cryptographic hash functions" >}},
    {{< wp "Entropy_(information_theory)" "Information Entropy" >}}.
-   [OWASP](https://www.owasp.org/):
    [Authentication Cheat Sheet
    ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)
    has a section on
    [Implement Proper Password Strength Controls
    ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet#Implement_Proper_Password_Strength_Controls)
    and also a
    [Password Storage Cheat Sheet
    ](https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet)
-   [Ubuntu Help: Strong Passwords
    ](https://help.ubuntu.com/community/StrongPasswords)
-   [SANS: Simple Formula for Strong Password
    ](http://www.sans.org/reading-room/whitepapers/authentication/simple-formula-strong-passwords-sfsp-tutorial-1636)
    (pdf).
-   [The Stanford SRP Authentication Project](http://srp.stanford.edu/) (BSD Licence)
    Secure Remote Password protocol integrates secure password authentication into new
    and existing networked applications.
-   [Pwned Passwords](https://haveibeenpwned.com/Passwords) are hundreds of millions of
    real world passwords previously exposed in data breaches. They're searchable online
    as well as being downloadable.
    -   We can also use the [Pwned Passwiords API](https://haveibeenpwned.com/API/) to
    query the pawned password database, you can use it by sending a sh1 hash of your
    password, and so not exposing it on internet.

## Choosing a password
When choosing a password always check that you follow a
[guideline for good passwords
](https://en.wikipedia.org/wiki/Password_strength#Common_guidelines).
This includes a proper length (ban passwords less than 10 characters), if possible
use randomly generated characters, or words when using diceware passwords.

Avoid using any knowable information about you or close people, including names,
address, birthdates, id numbers....

Avoid dictionary names, even with prepending or postpending symbols or numbers;
unless when purposely using them with a diceware formula.

Don't use any password that [has been pwned](https://haveibeenpwned.com/Passwords).

Avoid repeating characters, common symbol substitutions.

A human generated password use to follow some rules, you capitalize the first
letter, you use dates, or words. You use common language composition rules, like
following a consonant by a vowel, or using only only some known pairs of consonnants
or vowels. All these made trigraphs in any language distinct from randomly generated
triple of letters.

So you introduce in your passwords a structure that can be used by a password
breaking program to reduce drastically the time to crack the password compared to a
single brute force attack.

Also beware that many old password tests, or entropy calculators, make the
assumption that any long string with uppercase, lowercase, symbols, and digits is to
is a randomly generated character string; and gives it a very hight entropy, making
them claim that passwords like `D0g-----------------------` or
`1234567890!Abcdefghij` or `We shall/overC0me` are strong passwords; while they are
easily cracked.

Some sites give an estimate on how long it is to crack a password depending of the
character set and number of character, but it is only meaningful if you give also the
hashing algorithm used and the hardware running the hash cracker. See more on this
subject in the following  hash cracking section.

Note that is is only an example, the number of cracked hases per second vary both
depending of the computer and of the hash used.

An hash cracking aray like those used by criminal or governemental institution is
incomparably quicker than an home multiprocessor aray.

The hash make also an huge difference, but if you can choose on your computer hashes
that need more work, you don't master how your passwords are stored on the remote
sites. This is why it is so important to never reuse a password, a breach on one site
would compromise all your security.

An idicative result on an home array is given in
[8x Nvidia GTX 1080 Hashcat Benchmarks · GitHub
](https://gist.github.com/epixoip/a83d38f412b4737e99bbef804a270c40)

These 8 GTX 1080 may compute in one second 334 Giga NTLM, 200 Giga MD5, 179 Giga
NetNTLMv1, 68 Giga SHA1, 13 Giga NetNTLMv2, 3 mega sha256crypt, 1 Mega sha512crypt, 1
Mega Keepass AES, 4 mega scrypt, PBKDF2-HMAC-SHA512 or WPA2, 105 Kilo bcrypt Blowfish.

It means that if a password is NTLM or md5 encoded, even random and long it can be
cracked offline.

It also means that giving a table of time to crack passwords offline, depending only of
their entropy (i.e. length and complexity) is meaningless if you don' say how it is
hashed, and if the hash is salted.

Taking a 10 giga (10^10) guesses per second
The compared estimate of _haystack_ and _zxcvbn_ are for these three passwords
to which we add a 17 characters randomly generated passsword
`]M:aEH+*v\kuz*9c}`


| password | haystack    | zxcvbn   |
|:---------|:----------- |:---------|
| D0g---   | 10^34 years | < 1s     |
| 123456   | 10^24 years | < 1s     |
| We shal  | 10^14 years | 15mn     |
| ]M:aEH   | 10^16 years | 4 months |

The [Haystack GRC calculator](https://www.grc.com/haystack.htm) gives for the weaker
of these three ten giga centuries to be cracked with a massive cracked array.

While zxcvbn test estimate the first two to be cracked in less than a second.

The third which has the lower score in _haystack_ is the better for _zxcvbn_ with 11mn.

_haystack_ warn that their test is not a password strength test, but they claim that
their _Dog0_ password is safe because

>> after exhausting all of the standard password cracking lists, databases and
>> dictionaries, the attacker has no option other than to .. start guessing every
>> possible password.

May be this was true in 2012 when it was written, but a modern password attack will
try to guess the structure of the password, looking for dictionary words, and
repeated characters before, engaging with a massive brute force cracking.

## Diceware
Diceware passphrases was popularized by was by the [xkcd](http://xkcd.com/) comic
[password illustrated recipe](http://xkcd.com/936/), it allows to choose a password
that both has a good [entropy
](http://en.wikipedia.org/wiki/Password_strength#Entropy_as_a_measure_of_password_strength)
and easy to memorize.

-   [The Diceware Passphrase Home Page](http://world.std.com/~reinhold/diceware.html)
    teach a method to generate strong passwords.
-   Wikipedia: {{< wp "Diceware" >}}
-   [EFF's New Wordlists for Random Passphrases
    ](https://www.eff.org/deeplinks/2016/07/new-wordlists-random-passphrases) fixes many
    problems in the original diceware wordlist, which make diceware passwords hard to
    remember.

    The long list has the same word number than the original Diceware list 7,776 words
    6^5, giving an entropy of 12.925 per word.

    As the average length of each word is 7 letters, the average letter entropy is 1.85.
    Which means tht with 6 words of the list you have to type around 42 characters
    to get an entropy of 77.5; while if you use random lowercase characters you achieve
    it with 17 characters.

    But if you can memorize 6 words, it is difficult to remember 17 random characters!

    The short list contains only 6^4 words i.e 1296, with an entropy of 10.340 per word.
    So you need to use more words to attain the same entropy. Using eight words from the
    short will provide a slightly stronger strength than 6 words in the long list.

    The average length in this list is of 4.5 characters per word giving an entropy of
    2.3 per character.

-   [Diceware web application](https://diceware.dmuth.org/)
    is an application in javascript to generate diceware passwords in your web browser.
    -   [dmuth/diceware -GitHub](https://github.com/dmuth/diceware) (GPL-2.0).
-   [ulif/diceware](https://github.com/ulif/diceware) (GPL-3.0)
    is a python program to, generate Diceware passwords. It can use the EFF wordlist,
    [Natural Language Passwords database for password generation
    ](https://github.com/NaturalLanguagePasswords/system) which has a separate list of
    english names and adjectives, and an improved version of the legacy list originally
    published by A G Reinhold containing 8192 words
    [heartsucker/diceware list](https://github.com/heartsucker/diceware). It can use also any
    wordlist that you provide. There are also many options to use a custom separator,

    Two Debian packages _diceware_ and _diceware-doc_ are provided.

    -   [diceware documentation](https://diceware.readthedocs.io/en/stable/readme.html).
-   [goxkcdpwgen](https://github.com/martinhoefling/goxkcdpwgen) (MIT License)
    xkcd style password generator library and cli tool written in Go language.
    It uses the eff long or short word list, or a German short or long wordlist.
    Packaged in Debian.
-   [XKCD-password-generator](https://github.com/redacted/XKCD-password-generator)
    (BSD Licence) is a diceware passphrase generator written in Python. Is has options to
    choose an acrostic of the first letters of the words, the length of the passphrase
    and the range of word length, and the range of valid characteres.

    It can use the eff long list, the legacy word list, and additional word lists in
    many languages. _xkcdpass_ is in Debian.

### liste française
there are many french lists, the list [la liste diceware française - diceware.fr
](https://diceware.fr/) seems the more known, the material on the construction of this
list is scarse. It is not directly available on the wen but only through some text files
in a zip archive.

This list is built with a lexique from [lexique.org](http://www.lexique.org/). It keeps
only common names of less than 6 letters.

This list has 2724 words, aproximatively twice the eff short
list, with an entropy of 11.412.

As this list does not contain a power of 6 numbers, the dices are not approriate to
generate a random word. but even with the official diceware list, one barely rely on
material dices.

An other [liste diceware-fr de Christophe-Marie Duquesne
](https://github.com/chmduquesne/diceware-fr) is improved by _mbelivo_
[diceware-wordlists-fr](https://github.com/mbelivo/diceware-wordlists-fr) which has
lists of 7776 or 1296 words as the EFF lists (power of 6) or 4096 words.

The construction of the list from [lexique.org](http://www.lexique.org/) is explained
in the [README](https://github.com/mbelivo/diceware-wordlists-fr/blob/master/README.md).

The entropy given by the diferrent lists is given by the following table:
<!--
#+ORGTBL: SEND diceware_entropy orgtbl-to-html
| words | french | eff short | eff long |
|-------+--------+-----------+----------|
|     4 | 45.648 |     41.36 |     51.7 |
|     5 |  57.06 |      51.7 |   64.625 |
|     6 | 68.472 |     62.04 |    77.55 |
|     7 | 79.884 |     72.38 |   90.475 |
|     8 | 91.296 |     82.72 |    103.4 |
|     9 | 102.708 |     93.06 |  116.325 |

#+TBLFM: $2=$1*11.412::$3=$1*10.340::$4=$1*12.925
-->

| words | french | eff short | eff long |
|------:|-------:|----------:|---------:|
|     4 |  45.64 |     41.36 |    51.70 |
|     5 |  57.06 |     51.70 |    64.62 |
|     6 |  68.47 |     62.04 |    77.55 |
|     7 |  79.88 |     72.38 |    90.47 |
|     8 |  91.29 |     82.72 |   103.40 |
|     9 | 102.70 |     93.06 |   116.32 |



## password strength test
There are two kinds of password test, to test a candidate password you try to evaluate
how much work it is for an attacker to crack the password.

Or to check the security of the passwords on your computer, you use an hash cracker to
eliminate those who are the weaker. The
{{< iref "hash_cracking" "Hash Cracking programs" >}} are below.

The [Password Policy Testing Framework](http://password-policy-testing.wikidot.com/)
compare some strength tests, it has been presented in a conference but the lack of
documentatiopn, make it difficult to evaluate.

-   [passwdqc](https://github.com/openwall/passwdqc)
    Password/passphrase strength checking and policy enforcement
    from [Openwall](https://www.openwall.com/) which also produces
    {{< iref "authentication#john_the_ripper" "John the Ripper" >}}.

    _passwdqc_ can be used as a pam module,  for
     PAM-aware password changing programs, such as passwd(1).

     The accepted password are configurable with many options.

     _passwdqc_ is in Debian as the _passwqqc_ package which provides standalone password/passphrase
    strength checking and random passphrase generator programs pwqcheck and pwqgen; and
    the  libpam-passwdqc pam module.

    -   [passwdqc OpenWall page](https://www.openwall.com/passwdqc/)
-   [owasp-password-strength-test
    ](https://github.com/viaforensics/owasp-password-strength-test)
    is a password-strength tester, written in javascript,  based off of the
    OWASP Guidelines for enforcing secure passwords.

    It is no longer updated since 2015, and is replaced by zxcvbn.
    It can be used on the server (nodejs) or in-browser..
   [OWASP Passfault](https://passfault.appspot.com/)
    is another strength evaluator.

### zxcbvn
[xzbcn (GitHub repo)](https://github.com/lowe/zxcvbn)
introduced in dropbox blog:
[zxcvbn: realistic password strength estimation
](https://tech.dropbox.com/2012/04/zxcvbn-realistic-password-strength-estimation/)
is a javascript application for testing the password strength.
-   [GitHub - zxcvbn](https://github.com/dropbox/zxcvbn) is the original zxcvbn
    javascript application. The last commit is in 2017.
-   [zxcvbn-ts/zxcvbn](https://github.com/zxcvbn-ts/zxcvbn)
    is a complete rewrite of zxcvbn into typescript

    It is on-line at [zxcvbn-ts demo](https://zxcvbn-ts.github.io/zxcvbn/demo/).
    -  [zxcvbn-ts Guide](https://zxcvbn-ts.github.io/zxcvbn/guide/)

# Password hashes {#password_hashes}
-   [OWASP Password Storage Cheat Sheet
    ](https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet)

## Hashing Passwords {#hashing_passwords}

A random password entropy is computed with the formula e=l*log<sub>2</sub>(r) where l is the
number of characters and r the range of character. This means than you choose a random
password among a set of 2<sup>e</sup> choices, or that a cracking program will need to crack an
average of 2<sup>e</sup>/2 hashes to find your password.

If we have a calculator with only log<sub>10</sub> or ln functions we can use
e=l*log<sub>10</sub>(r)/log<sub>10</sub>(2) or e=l*ln(r)/ln(2)

## hashing passwords on linux {#hashing_passwords_on_linux}

The passwords on linux are primarily managed with the  {{< man "crypt(3)" >}},
the format and algorithms supported are described in {{< man "crypt(5)" >}}.

Hashed passphrase consists of four components: _prefix_, _options_, _salt_, and _hash_.

The prefix control which hashing method is used, the _options_ are method specific, the
_hash_ also is provided by the selected method but is encoded in a base 64 encoding
which uses only printable asccii character and avoid a set of reserved characters
symbols. The components are separated by the character `$`.

The methods are:

| prefix | method        | hash size | salt size | cpu cost             | obsolete |
|:-------|---------------|:----------|:----------|:---------------------|:--------:|
| $y$    | [yescript]    | 256       | ≤512     | 1-11 (log)           |          |
| $gy$   | gost-yescript | 256       | ≤512     | 1-11 (log)           |          |
| $7$    | [scrypt]      | 256       | ≤512     | 6-11 (log)           |          |
| $2b$   | [bcrypt]      | 184       | 128       | 4-31 (log)           |          |
| $6$    | [sha512crypt] | 512       | 6-96      | 10³-10<sup>10</sup>  |          |
| $5$    | [sha256crypt] | 256       | 6-96      | 10³- 10<sup>10</sup> |          |
| $sha1$ | [sha1crypt]   | 160       | 6-384     | 4-10⁹                | O        |
| $md5$  | [md5crypt]    | 128       | 6-48      | 10³                  | O        |
| ""     | [DEScrypt]    | 64        | 12        | 25                   | O        |
| $3$    | [NTLM]          | 256       | 9         | 1                    | O        |
|        |               |           |           |                      |          |


[NTLM]: https://en.wikipedia.org/wiki/NTLM
[sha512crypt]: https://en.wikipedia.org/wiki/SHA-2
[sha256crypt]: https://en.wikipedia.org/wiki/SHA-2
[sha1crypt]: https://en.wikipedia.org/wiki/SHA-1
[bcrypt]: https://en.wikipedia.org/wiki/Bcrypt
[scrypt]: https://en.wikipedia.org/wiki/Scrypt
[md5crypt]: https://en.wikipedia.org/wiki/MD5
[DEScrypt]: https://en.wikipedia.org/wiki/MD5
[yescrypt]: https://github.com/openwall/yescrypt

[NTLM] has many weakness and vulnerabilities, as it is one of the more easily exploited
hash it is the primary target of hash crackers,
{{< wp "Crypt_(Unix)" "crypt" >}} is weak,
{{< wp "MD5#Security" "md5 is vulnerable to collision attacks" >}},
for [sha1crypt] there is a possibility of {{< wp "Sha1#Attacks" "sha1 attacks" >}}.

[sha512crypt] was the default under Debian until Debian 11, but the CPU cost of
[sha512crypt] and [sha256crypt] is too low for modern hardware.

The old methods was made supposing than an attacker will hash passwords using an array
of classic processors where the limiting factor is CPU speed. But we can now also use
GPU that can be a lot more efficient at cracking the previous known hashes including
some which was considered as secyre like sha256crypt and sha512crypt. The price of
{{< iref "Application-specific_integrated_circuit" "AICs" >}}, and
{{< iref "Field-programmable_gate_array" "FGPAs" >}} allow cracking at a speed which was
previously reserved to supercomputers.



The newer hashing method are enginered to be slow and costly not only in CPU but also in
memory to avoid fast cracking with GPU hardware. The CPU cost can be adjusted with the
_CPU time cost_ parameter of {{< man  "crypt_gensalt(3)" >}}.

In {{< man "pam_unix(8)" >}} you can adjust the number of rounds used by SHA256, SHA512,
blowfish, gost-yescrypt, and yescrypt by setting the paramater `round=n`.

The login password settings in Debian are explained in
[Debian reference Chapter 4. Authentication and access controls
](https://www.debian.org/doc/manuals/debian-reference/ch04.en.html#_configuration_files_accessed_by_pam_and_nss)
more details are given i
[Securing Debian Manual - 4.11. Providing secure user access
](https://www.debian.org/doc/manuals/securing-debian-manual/ch04s11.en.html).

The password hashing algorithm is set in `/etc/login.defs` with the variable
`ENCRYPT_METHOD`  for the group passwords see {{< man "login.defs(5)" >}}.

For the user it is configured in `/etc/pam.d//common-password`.

The options are explained in {{< man "pam_unix(8)" >}}.

If you want to change password hashes you must reenter the old passwords to
rehash them.

## Hash cracking {#hash_cracking}
See also {{< iref "network_security#brute_forcer" "Brute forcers" >}}
in the {{< iref "network_security" "network security section" >}}.

{{< wp "Password Cracking" >}} is now mainly done by {{< wp "Rainbow tables" >}} and
{{< wp "Brute-force attack" >}}.

The easiest attacks are done using {{< wp "rainbow tables" >}}, because it doesn't need
a lot of cpu power, but rather an important storage, which is cheap by today.

The better protection against rainbow tables is
[salt](https://en.wikipedia.org/wiki/Salt_(cryptography)).

There are many programs to apply these two methods.

-   <a name="john_the_ripper"></a>[John the Ripper](https://www.openwall.com/john/) (GPL)
    from [Openwall](https://www.openwall.com/)
    performs dictionary attacks and brute force cracking. The basic version is GPL and
    available in Debian under the name _john_, there is also a private _Pro_ version.a
    -   [GitHub - openwall/john](https://github.com/openwall/john)
    -   An alternative opensource communauty verstion is available at
        [magnumripper/JohnTheRipper](https://github.com/magnumripper/JohnTheRipper)
    -   [Johnny - GUI for John the Ripper](https://openwall.info/wiki/john/johnny)
        is a qt gui for John the Ripper.
    -   [GitHub - openwall/johnny](https://github.com/openwall/johnny)
-   <a name="hashcat">[Hashcat](https://hashcat.net/hashcat/) (MIT Licence)
    is a very fast brute-force attack program. It support many hash format including
    LM hashes, MD4, MD5, SHA-family, Unix Crypt format. It can use brute-force,
    dictionary or an hybrid mode. It is available in Debian.
    -   [Découverte de Hashcat
        ](https://www.supinfo.com/articles/single/6242-decouverte-hashcat)
        par Adrien Flahaut.
    -   [How to Hack KeePass Passwords using Hashcat
        ](https://www.rubydevices.com.au/blog/how-to-hack-keepass).
-   [hydra](https://github.com/vanhauser-thc/thc-hydra)
    is a parallelized login cracker which supports numerous protocols
    to attack. _hydra_ is packaged in Debian along with the GUI
    _hydra-gtk_.
-   {{< wp "Ophcrack" >}} is an rainbow table cracker.
-   [RainbowCrack](http://project-rainbowcrack.com/) (private licence)
    is a rainbow table hash craker, binary are  available for linux and window.
    -   [Découverte de RainbowCrack
        ](https://www.supinfo.com/articles/single/6236-decouverte-rainbowcrack) par
        Adrien Flahaut.

### Online password crackers
-   [hashkiller](https://hashkiller.co.uk/md5-decrypter.aspx)
    try to crack md5, sha1, ntlm.
-   [Online Hash Crack](https://www.onlinehashcrack.com/)
    crack hashes in md4/md5/sha1/sha256, and WPA(2) crack.
-   [CrackStation Free Password Hash Cracker](https://crackstation.net/)
    crack hashes in LM, NTLM, md2, md4, md5, md5(md5_hex), md5-half, sha1, sha224,
    sha256, sha384, sha512, ripeMD160, whirlpool, MySQL 4.1+ (sha1(sha1_bin)),
    QubesV3.1BackupDefaults.
    it also explain how to implement a secure
    [salted password hashing](https://crackstation.net/hashing-security.htm).
-   [md5crack](http://www.md5crack.com/) crack md5 _unsalted_ hashes with rainbow tables.

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
