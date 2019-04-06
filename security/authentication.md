---
title: Authentication
---

{{% toc /%}}

---

Apache authentication is in the
{{< iref "apache" "Apache Page" >}},
{{< iref "nginx" "Nginx Authentication" >}}.
See also {{< iref "security" "Security" >}},
{{< iref "passwords_managers" "Passwords Managers" >}},
{{< iref "Network" "Network Security" >}}

# Authentication references
-   Wikipedia:
    [Authentication](http://en.wikipedia.org/wiki/Authentication) and the ,
    [numerous related pages
    ](http://en.wikipedia.org/wiki/Authentication#See_also)
-   [Open Web Application Security Project (OWASP)
    ](https://www.owasp.org/)
    an organization focused on improving the security of software.
    -   [OWASP principles
        ](https://www.owasp.org/index.php/Category:Principle)
    -   [list of How To](https://www.owasp.org/index.php/Category:How_To)
    -   [Guide to Building Secure Web Applications and Web Services
        ](https://www.owasp.org/index.php/Category:OWASP_Guide_Project)
    -   [Guide to Authentication
        ](https://www.owasp.org/index.php/Guide_to_Authentication).
        _page deleted?_
    -   [Authentication Cheat Sheet
        ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)
    -   [OWASP Testing Guide
        ](https://www.owasp.org/index.php/OWASP_Testing_Guide_v4_Table_of_Contents)
        ([pdf
        ](https://www.owasp.org/images/5/52/OWASP_Testing_Guide_v4.pdf))
-   [User Authentication HOWTO
    ](http://www.tldp.org/HOWTO/User-Authentication-HOWTO/index.html)
    that explains how user and group information is stored and how users are
    authenticated on a Linux system (PAM) and
    [Authentication Gateway HOWTO
    ](http://tldp.org/HOWTO/Authentication-Gateway-HOWTO/)
    An authentication gateway forces the user to authenticate in order
    to use the network. It can be used for wireless networks and public
    access areas.
    These two howtos are outdated _2002/2003_.
-   [Wikipedia: Cram-Md5](http://en.wikipedia.org/wiki/CRAM-MD5)
    is a challenge-response authentication mechanism defined in the
    [RFC 2195](http://tools.ietf.org/html/rfc2195) and  often used
    as part of the authentication of SMTP, POP and IMAP, as well as in
    LDAP, XMPP, BEEP, and other protocols.
    It is of the authentication methods supported by
    {{< wp "Simple Authentication and Security Layer" >}} (SASL)
-   [SANS](http://www.sans.org/) is an institute for information
    security training and security certification. It has a
    [collection of Authentication related papers
    ](http://www.sans.org/reading-room/whitepapers/authentication).
-   [Dos and Don’ts of Client Authentication on the Web (pdf)
    ](https://pdos.csail.mit.edu/papers/webauth:sec10.pdf)
-   [The definitive guide to form-based website authentication
    ](http://stackoverflow.com/questions/549/the-definitive-guide-to-form-based-website-authentication)

# Multifactor Authentication {#multifactor_authentication}
The authentication factors of a multi-factor authentication scheme may include:
-   __Possession factors__: some physical object in the possession of
    the user, such as a USB stick with a secret token, a bank card, a
    key, etc.
-   __Knowledge factors__: some secret known to the user, such as a
password, PIN, TAN, etc.
-   __Inherence factors__: some physical characteristic of the user
    (biometrics), such as a fingerprint, eye iris, voice, typing
    speed, pattern in key press intervals, etc

-   Wikipedia:
    {{< wp "Authentication#Types_of_Authentication"  "Types of Authentication" >}},
    {{< wp "Multi-factor authentication" >}},
    {{< wp "Strong Authentication" >}},
    {{< wp "Comparison of authentication solutions" >}},
    {{< wp "One-time password" >}},
    {{< wp "S/KEY" >}},
    {{< wp "Security token" >}},
    {{< wp "Smart Card" >}},
    {{< wp "Google Authenticator" >}}

## One Time Password - OTP
A one-time password (OTP) is a password that is valid for only one
login session or transaction.
So OTP is not vulnerable to replay attacks.

The OTP may be calculated on a time basis (TOTP) or derived by a
mathematical algorithm or {{< wp "Hash chain" >}} among wich  HOTP.

The OTP may be delivered by SMS, mobile phose, prprietary tokens,
web-based methods, or hardcopy on paper or plastic card.

One-time passwords are vulnerable to phtising and  man-in-the-middle
attacks, and are only secure when used as part of multi-factor
authentication.

TOTP is an algorithm that computes a one-time password from a shared
secret key and the current time.TOTP is an example of a hash-based
message authentication code (HMAC). TOTP is based on HOTP with a timestamp
replacing the incrementing counter.  It combines a secret key with the
current timestamp using a cryptographic hash function to generate a
one-time password. The timestamp typically increases in 30-second
intervals, so passwords generated close together in time from the same
secret key will be equal.


-   {{< wp "One-time password" >}},
    {{< wp "Time-based One-time Password Algorithm" >}},
    {{< wp "HMAC-based One-time Password Algorithm" >}},
    {{< wp "S/KEY" >}},{{< wp "OTPW" >}},


-   [One Time PassWord - ArchWiki
    ](https://wiki.archlinux.org/index.php/One_Time_PassWord)
-   [PPP Perfect Paper Password]( https://www.grc.com/ppp.htm)
    GRC's One Time Password System, has a
    [ppp-pam](http://code.google.com/p/ppp-pam/)
    module _last update 2009_, the use is explained in
    [Perfect Paper Passwords - One Time Password System (OpenSuse)
    ](http://linuxpoison.blogspot.fr/2009/04/perfect-paper-passwords-one-time.html)
    _2009_.
    There is also an  android client
    [android-ppp](http://code.google.com/p/android-ppp/) _updated 2013_.

### Google Authenticator
{{< wp "Google Authenticator" >}} (proprietary)
is a client for Android, iOS, and BlackBerry, and also PAM module
for the server side, that uses TOTP and HOTP. Authenticator
provides a six- to eight-digit one-time password which in addition
to the username and password allow log in to Google services or
third-party applications, such as password managers or file
hosting services. It has
{{< wp "Google_Authenticator#Implementations"  "numerous implementations" >}}.

-   [Archwiki: Google Authenticator
    ](https://wiki.archlinux.org/index.php/Google_Authenticator)
-   [google-authenticator Home](http://code.google.com/p/google-authenticator/)
-   [Android App: Google Authenticator
    ](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)
-   [FreeOTP](https://fedorahosted.org/freeotp/) (Apache Licence)
    is a two-factor authentication applicationwith support for ​Android
    and ​iOS.

## Security Token

-   Wikipedia: {{< wp "Security Token" >}}
-   {{< wp "YubiKey" >}} implement HOTP and TOTP
-   [U2F — FIDO Universal 2nd Factor
    ](https://www.yubico.com/about/background/fido/)
    is supported by Github, Dropbox, Gitlab, Bitbucket, it can be used
    in Linux with the
    [Pam-U2F module](https://developers.yubico.com/pam-u2f/).
    -   [What is U2F
        ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
    -   [U2F Technical Overview
        ](https://developers.yubico.com/U2F/Protocol_details/Overview.html)
    -   [Using a U2F library
        ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
-   [Extension adding support for U2F standard to Firefox
    ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
    U2f is also supported by Chrome.
-   [Nitrokey](https://www.nitrokey.com/)
-   [The OpenPGP card](http://www.g10code.com/p-card.html)

## Smart cards
-   [Smartcards - Debian Wiki
    ](https://wiki.debian.org/Smartcards),
    [fr/Smartcards - Debian Wiki
    ](https://wiki.debian.org/fr/Smartcards)
-   [Ludovi Rousseau blog](http://ludovicrousseau.blogspot.fr/)
    and [GitHub repository](https://github.com/LudovicRousseau).
    -   [GitHub - LudovicRousseau/CCID: CCID driver
        ](https://github.com/LudovicRousseau/CCID)
-   [Smartcard resources](https://thesmartcard.org/resource/)
-   [PCSClite project](http://pcsclite.alioth.debian.org/ccid.html)

## SSH and OTP

# Kerberos
-   [Kerberos Infrastructure HOWTO
    ](http://cryptnet.net/fdp/admin/kerby-infra/en/kerby-infra.html)
    covers design and configuration of a Kerberos infrastructure for
    handling authentication with GNU/Linux. _2009_
-   [Tutorial Kerberos
    ](http://varrette.gforge.uni.lu/download/polys/Tutorial_Kerberos.pdf)
    (PDF french) by Sebastien Varrette.

# Password Strength
-   Wikipedia: {{< wp "Password strength" >}},
    [Key Size](http://en.wikipedia.org/wiki/Key_size),
    [Key strengthening](http://en.wikipedia.org/wiki/Key_strengthening),
    [Password](http://en.wikipedia.org/wiki/Password),
    [Password cracking](http://en.wikipedia.org/wiki/Password_cracking),
    {{< wp "cryptographic hash functions" >}},
    {{< wp "comparison of cryptographic hash functions" >}}.
-   [OWASP](https://www.owasp.org/):
    [Authentication Cheat Sheet
    ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)
    has a section on
    [Implement Proper Password Strength Controls
    ](https://www.owasp.org/index.php/Authentication_Cheat_Sheet#Implement_Proper_Password_Strength_Controls)
    and also a
    [Password Storage Cheat Sheet
    ](https://www.owasp.org/index.php/Password_Storage_Cheat_Sheet)
-   [Ubuntu Help: Strong
    Passwords](https://help.ubuntu.com/community/StrongPasswords)
-   [SANS: Simple Formula for Strong Password
    ](http://www.sans.org/reading-room/whitepapers/authentication/simple-formula-strong-passwords-sfsp-tutorial-1636)
    (pdf).
  - [The Diceware Passphrase Home Page
    ](http://world.std.com/~reinhold/diceware.html)
    teach a method to generate strong passwords.
-   [The Stanford SRP Authentication Project
    ](http://srp.stanford.edu/) (BSD Licence)
    Secure Remote Password protocol integrates secure password
    authentication into new and existing networked applications.
-   [xkcd web commic](http://xkcd.com/) gave a popular
    [password illustrated recipe](http://xkcd.com/936/) to choose a password
    that both has a good [entropy
    ](http://en.wikipedia.org/wiki/Password_strength#Entropy_as_a_measure_of_password_strength)
    and easy to memorize.
-   [xzbcn (GitHub repo)](https://github.com/lowe/zxcvbn)
    introduced in dropbox blog:
    [zxcvbn: realistic password strength estimation
    ](https://tech.dropbox.com/2012/04/zxcvbn-realistic-password-strength-estimation/)
    is a javascript application for testing the password strength.
    It is on-line at
    [zxcvbn test page](https://dl.dropbox.com/u/209/zxcvbn/test/index.html).
-   [Generating an XKCD Password _with Python_
    ](http://interactivepython.org/courselib/static/everyday/2013/01/4_password.html)
    a tutorial in [Everyday Python Blog
    ](http://interactivepython.org/courselib/static/everyday/).

## password strength test
-   [hydra](https://github.com/vanhauser-thc/thc-hydra)
    is a parallelized login cracker which supports numerous protocols
    to attack. _hydra_ is packaged in Debian along with the GUI
    _hydra-gtk_.
-   [John The Ripper](http://www.openwall.com/john/doc/) help to test
    your passwords strength.
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
-   zxcvbn password strength test
    -   [introduction to zxcvbn](http://tech.dropbox.com/?p=165),
    -   [GitHub - zxcvbn](https://github.com/dropbox/zxcvbn).
    -   [An other test page for zxcvbn
        ](https://www.cygnius.net/snippets/passtest.html)

## Hash cracking {#hash_cracking}
See also {{< iref "network" "Brute forcers" >}}
in the {{< iref "network" "network security section" >}}.

{{< wp "Password Cracking" >}} is now mainly done by {{< wp "Rainbow tables" >}} and
{{< wp "Brute-force attack" >}} There are many programs to apply these methods.

-   [RainbowCrack](http://project-rainbowcrack.com/) (private licence)
    is a rainbow table hash craker, binary are  available for linux and window.
    -   [Découverte de RainbowCrack
        ](https://www.supinfo.com/articles/single/6236-decouverte-rainbowcrack) par
        Adrien Flahaut.
-   [John the Ripper](https://www.openwall.com/john/) (GPL)
    perform dictionary attacks and brute force cracking. The basic version is GPL and
    available in Debian under the name _john_, there is also a private _Pro_ version.
    An alternative opensource communauty verstion is available at
    [magnumripper/JohnTheRipper](https://github.com/magnumripper/JohnTheRipper).
-   <a name="hashcat">[Hashcat](https://hashcat.net/hashcat/) (MIT Licence)
    is a very fast brute-force attack program. It support many hash format including
    LM hashes, MD4, MD5, SHA-family, Unix Crypt format. It can use brute-force,
    dictionary or an hybrid mode. It is available in Debian.
    -   [Découverte de Hashcat
        ](https://www.supinfo.com/articles/single/6242-decouverte-hashcat)
        par Adrien Flahaut.
    -   [How to Hack KeePass Passwords using Hashcat
        ](https://www.rubydevices.com.au/blog/how-to-hack-keepass).

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

## Password Hashing
Password hashing is a strategy that uses a single master password that is hashed with a
salt made from the domain of the accessed site to generate a unique password that won't
be cracked if you don't know the master password.

Before using them you may read
[The case against password hashers](https://anarc.at/blog/2017-03-02-password-hashers/)
and
[A short history of password hashers](https://anarc.at/blog/2017-03-02-hashers-history/)
by _Anarcat_. It points out the cryptography havoc of old hashing mechanism _wich is
similar for every hashing use_, the necessity to copy  the username and password from
the hasher to the site, the necessity to reenter all your passwords when you change of
hasher, or from hashing function.

It is also to note that while these passsword hashers are used to avoid you use the same
password for many sites, when it is discovered either on a badly managed site that don't
hash or hash not properly your password and has its data stolen; or if it is stolen when
you type it because you javascript library has been replaced by a malicious one, or
because you type it in an unsecure environment where a key logger steal it; you are
actually giving access not only to one site but to all your private data.

An other problem with password hashers pointed out by _Anarcat_ is that one of their
benefit is to be stateless, serverless. But the sites have different requirements for
the passwords, so the options must be stored and available in every place you use
them. The recent password hashers offer a way to store them in the cloud or other
internet accessible place, even if this information is not sensitive, your hasher is no
longer stateless and don't work offline.

This defect is also object of the paper by Tony Arcieri:
[4 fatal flaws in deterministic password managers
](https://tonyarcieri.com/4-fatal-flaws-in-deterministic-password-managers).


But personally, I still find them usefull in some cases, in the past I was using the
same password for all harmless site, I mean all the shopping sites that you use once or
twice and where you are supposed not entering many critical data. I am a gardener who
buy seeds at many shops, what matter if my credentials are stolen, people will only
learn what I have sown the last years!

But this strategy is still dangerous, may be you use this password also on a site that
can use your credit card or have some sensitive data, if this password is captured on
one site, may be a fake site used for phishing, it is compromised everywhere.

But for these _low value_ sites the password hashers are still an help, you can put the
hash in your password manager and use it as usual, but in an environment where the
password manager is unavailable, and you fill it si not secure to log into its web site,
because you use an unknown computer you can still use the password hasher with the web
interface.


-   [Stanford PwdHash](https://pwdhash.github.io/webs)
    is the oldest password hasher with wide use.
    will come with browser extensions for Firefox, Chrome, Opera and a
    [local javascript stand alone page
    ](https://crypto.stanford.edu/PwdHash/RemotePwdHash/). It still use md5 which is no
    longer considered as secure.
-   There are many other extensions for hashing passwords in Firefox or Chrome that you
    get by looking for _password hasher_ in the extensions search. But many of them are
    limited to one browser, if you use many browsers, many systems or desktop and mobile
    like everyone today, it is of no use. Moreover the extensions are versions
    sensitive, and when you update say Firefox, you will soon or later see that the
    extension is no longer compatible, may be a new version of the extension will pop
    out some time later, but you can you login to your sites in the meantime.

    Some of these extension propose also a standalone javascript solution like
    [passhash-ng](https://github.com/phreaknerd/passhash-ng).
-   [SuperGenpass](https://chriszarate.github.io/supergenpass/) uses as basic method
    javascript bookmarklets that you can use in any javascript enabled browser.
    As it is a trivial script it has also be ported to many
    [alternative implementations
    ](https://github.com/chriszarate/supergenpass/wiki/Implementations)
    including browsers extensions and standalone programs, that will be very usefull to
    open sites in a non javascript enabled browser like elinks, w3m, ewww, ....
    Be aware that SuperGenPass defaults to MD5 with not enough rounds, you should select
    the SHA512 hashing function.
-   [LesPass](https://github.com/lesspass/lesspass) (GPL)
    by  Guillaume Vincent uses [PBKDF2](https://en.wikipedia.org/wiki/PBKDF2)
    key derivation with 100,000 iterations and a hash function sha-256. out of the web
    interface it provides a [cli](https://github.com/lesspass/lesspass/tree/master/cli)
    a firefox and chrome extension and an Androip app.

    A _connected_ version  works by saving your password’s profile, in in database
    hosted by the site or your own server. Of course you have the problem mentioned
    above of being no longer stateless!

    There are also an alternative
    [python cli](https://github.com/mevdschee/lesspass.py),
    a [go implementation](https://github.com/mevdschee/lesspass.go) with a cli and gui,
    and a [php implementation](https://github.com/mevdschee/lesspass.php).

# Pam
-   [rfc 86. unified login with pluggable authentication modules
    ](http://www.opengroup.org/rfc/mirror-rfc/rfc86.0.txt)
-   An introduction to Pam is the
    [pam Howto](http://susefaq.sourceforge.net/howto/pam.html) from the
    [Unofficial SUSEFAQ](http://susefaq.sourceforge.net/)
-   [The Linux-PAM System Administrators' Guide
    ](http://www.kernel.org/pub/linux/libs/pam/Linux-PAM-html/Linux-PAM_SAG.html)
-   [pam-list archive (@ MARC)
    ](http://marc.theaimsgroup.com/?l=pam-list)

## Pam Memo

### type

-   __account__ performs non-authentication based account management. It
    is typically used to restrict/permit access to a service.
-   __auth__ Firstly, it establishes that the user is who they claim
    to be, Secondly, the module can grant group membership.
-   __password__ used for updating the authentication token associated
    with the user.
-   __session__ things to do before or after authentification

### control

-   __requisite__ --  Failure to authenticate via this module results
    in immediate denial of authentication.
-   __ required__ --      Failure also results in denial of
    authentication, although PAM will still call all the other modules
    listed for this service before denying authentication.
    For the function to be able to return success to the
    application all `required' modules have to report success.
-   __sufficient__ -- If authentication by this module is
    successful, PAM will grant authentication immediatly.
    In the case this module succeed no other stacked module is called.
-   __optional__  -- Whether this module succeeds or fails is only
    significant if it is the only module of its type for this service.

### options
-   __use_first_pass__  Use the same password used by the first
    mechanism that asked for a password.
-   __try_first_pass__  This is the same as `use_first_pass', except
    that if the primary password is not valid, it should prompt the
    user for the password.

For the new syntax:

-   __required__ is equivalent to
    `[new_authtok_reqd=ok ignore=ignore default=bad](success=ok)`
-   __requisite__ is equivalent to
    `[new_authtok_reqd=ok ignore=ignore default=die](success=ok)`
-   __sufficient__ is equivalent to
    `[new_authtok_reqd=done default=ignore](success=done)`
-   __optional__ is equivalent to
    `[new_authtok_reqd=ok default=ignore](success=ok)`

Myc onfig is in `/etc/pam.d/system-auth`
and `/etc/nsswitch.conf`

# Polkit
{{< wp "Polkit" >}}, previously known as Policy Kit is an application-level toolkit
for defining and handling the policy that allows unprivileged
processes to speak to privileged processes.

It is used to grant a temporay privilege to perform some task as
Hibernate and shutdown the computer, manage network connections,
mount/eject a removable media, access devices, like audio, scanner,
removable storage, etc.

-   [polkit Reference Manual
    ](http://www.freedesktop.org/software/polkit/docs/latest/)
-   [polkit(8)
    ](http://www.freedesktop.org/software/polkit/docs/latest/polkit.8.html)
    -   [ArchWiki: PolicyKit](https://wiki.archlinux.org/index.php/PolKit)


# Radius
-   [Wikipedia: Radius](http://en.wikipedia.org/wiki/RADIUS),
    [gnu Radius](http://www.gnu.org/software/radius/)
    is a server for remote user authentication and accounting.
-   A
    [Captive Portal (Wikipedia page)](http://en.wikipedia.org/wiki/Captive_portal)
    forces an HTTP client on a network to see a special web page
    (usually for authentication purposes) before surfing the Internet
    normally.
    [Chillispot](http://www.chillispot.info/) (GPL)
    is a captive portal or wireless LAN access point controller this
    project is continued in
    [CoovaChilli](http://coova.org/CoovaChilli)
    which uses RADIUS and is part of the [CoovaAP for OpenWRT
    ](http://www.coova.org/CoovaAP/) which is a
    firmware specialized for hotspots; and with
    [Sweetspot](http://sweetspot.sourceforge.net/)
    (GPL) user-land daemon.
-   [802.1X Port-Based Authentication HOWTO
    ](http://www.tldp.org/HOWTO/8021X-HOWTO/index.html) _2004_.

# Httpd authentication
-   Wikipedia: {{< wp "Digest access authentication" >}}, {{< wp "HTTP cookie" >}},
    {{< wp "HTTP+HTML form-based authentication" >}},
-   [rfc2617](http://www.faqs.org/rfcs/rfc2617.html) basic and digest
    authentication
-   [The definitive guide to forms based website authentication
    ](http://stackoverflow.com/a/477578/965798) is a very comprehensive guide in a
    [StackOverflow](http://stackoverflow.com/) answer.
-   [Basic Authentication
    ](http://www.voidspace.org.uk/python/articles/authentication.shtml)
    shows how to deal with authentication in python,
    (french translation:
    [Authentification basique
    ](http://www.voidspace.org.uk/python/articles/authentication_francais.shtml))
-   {{< wp "OAuth" >}} provides a method for clients to access server resources on behalf
    of a resource  owner (such as a different client or an end-user).
    It also provides a process for end-users to authorize third-party access to their server
    resources without sharing their credentials, using user-agent redirections.

## OpenId
-   {{< wp "OpenId" >}}   is a URL based distributed identity system, see also
    [OpenId Home](http://openid.net/).
-   __MyOpenId__  provider have shut down their service in  February
    2014.
    Look at [Replacing MyOpenID
    ](http://evertpot.com/replacing-myopenid/) to use instead
    [IndieAuth](https://indieauth.com/) part of
    [IndieWeb](http://indiewebcamp.com/Getting_Started)
-   For OpenId development see
    [OpenId Wiki](http://wiki.openid.net/Main_Page),
    libraries are available at
    [openidenabled Home Page](http://www.openidenabled.com/)

## SSO
-   {{< wp "Single sign-on" >}} allows users to log in once and gain
    access to all systems without being prompted to log in again.
    This is typically accomplished using LDAP, when the sites are on
    the same domain it can also be achieved using cookies.
-   [Ubuntu SingleSignOn HowTo
    ](https://help.ubuntu.com/community/SingleSignOn)
    describes how to set up network-connected Ubuntu machines to
    support Single Sign On (SSO).


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
