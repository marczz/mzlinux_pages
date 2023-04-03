---
title: Password strength
---
a
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
-   [xkcd web commic](http://xkcd.com/) gave a popular
    [password illustrated recipe](http://xkcd.com/936/) to choose a password
    that both has a good [entropy
    ](http://en.wikipedia.org/wiki/Password_strength#Entropy_as_a_measure_of_password_strength)
    and easy to memorize.
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

Taking a 10 billion guess per second
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
of these three ten billions of centuries to be cracked with a massive cracked array.

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
    english names and adjectives, an improved version of  the list originally published
    by A G Reinhold containing 8192 words
    [heartsucker/diceware](https://github.com/heartsucker/diceware). It can use also any
    wordlist that you provide. There are also many options to use a custom separator,

    Two Debian packages _diceware_ and _diceware-doc_ are provided.

    -   [diceware documentation](https://diceware.readthedocs.io/en/stable/readme.html).


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

-   [owasp-password-strength-test
    ](https://github.com/viaforensics/owasp-password-strength-test)
    is a password-strength tester, written in javascript,  based off of the
    OWASP Guidelines for enforcing secure passwords.
    It can be used on the server (nodejs) or in-browser.
    <!--script src='/js/owasp-password-strength-test.js'></script-->
-   [OWASP Passfault](http://www.passfault.com/)
    is another strength evaluator.
-   [Yet Another Password Meter](http://www.yetanotherpasswordmeter.com/).
-   [owasp-password-strength-test
    ](https://github.com/viaforensics/owasp-password-strength-test)
    is a password-strength tester, written in javascript,  based off of the
    [OWASP Guidelines for enforcing secure passwords
    ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet#Implement_Proper_Password_Strength_Controls).
    It can be used on the server (nodejs) or in-browser.
    <!--script src='/js/owasp-password-strength-test.js'></script-->
-   [OWASP Passfault](https://passfault.appspot.com/)
    is another strength evaluator.
-   [Yet Another Password Meter](http://www.yetanotherpasswordmeter.com/).

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
