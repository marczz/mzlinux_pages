---
title: Authentication
---

<!-- [[file:../../../../content-org/notes/security_notes/authentication_notes.org][Authentication notes]] -->

Apache authentication is in the
{{< iref "apache" "Apache Page" >}},
{{< iref "nginx" "Nginx Authentication" >}}.
See also {{< iref "security" "Security" >}},
{{< iref "password_managers" "Passwords Managers" >}},
{{< iref "network_security" "Network Security" >}}

# Authentication references
-   Wikipedia:
    [Authentication](http://en.wikipedia.org/wiki/Authentication) and the
    [numerous related pages
    ](http://en.wikipedia.org/wiki/Authentication#See_also)
-   [Open Web Application Security Project (OWASP)
    ](https://www.owasp.org/)
    an organization focused on improving the security of software.
    -   [OWASP principles
        ](https://www.owasp.org/index.php/Category:Principle)
    -   [list of How To](https://www.owasp.org/index.php/Category:How_To)
        _obsolete_.
    -   [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)
    -   [Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)
    -   [Password Storage Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Password_Storage_Cheat_Sheet.html)
    -   [OWASP Testing Guide
        ](https://www.owasp.org/index.php/OWASP_Testing_Guide_v4_Table_of_Contents)
        ([pdf
        ](https://www.owasp.org/images/5/52/OWASP_Testing_Guide_v4.pdf))
-   [User Authentication HOWTO
    ](http://www.tldp.org/HOWTO/User-Authentication-HOWTO/index.html)
    that explains how user and group information is stored and how users are
    authenticated on a Linux system (PAM) and
    [Authentication Gateway HOWTO](http://tldp.org/HOWTO/Authentication-Gateway-HOWTO/)
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
-   __Knowledge factors__: some secret known to the user, such as a password, PIN, TAN,
    etc.
-   __Inherence factors__: some physical characteristic of the user (biometrics), such
    as a fingerprint, eye iris, voice, typing speed, pattern in key press intervals, etc

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

The OTP may be delivered by SMS, mobile phose, proprietary tokens,
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
-   [OTPW](https://www.cl.cam.ac.uk/~mgk25/otpw.html)
    is a one-time password login package.It consists of the one-time-password generator
    otpw-gen plus two verification routine that can
    be added to programs such as login or ftpd,  a PAM wrapper is also included.
    The user uses a previously printed list of one time password. The scheme is designed
    to be robust against theft of the paper list and race-for-the-last-letter attacks.
    A detailed description is found
    [in OTPW Home Page](https://www.cl.cam.ac.uk/~mgk25/otpw.html).
    The password generator _otpw-bin_ and _libpam-otpw_ are provided in Debian.

### TOTP authentificator

-   [OATH Toolkit](https://www.nongnu.org/oath-toolkit/)
    contains shared C libraries, command line tools and a PAM module. It supports many
    protocols, event-based HOTP algorithm (RFC 4226), the time-based TOTP algorithm (RFC
    6238), and Portable Symmetric Key Container (PSKC, RFC 6030) to manage secret key
    data.

    The components included in the package is
    -   liboath and libpskc: two shared and static C library for OATH and PSKC handling.
    -   [oathtool](https://www.nongnu.org/oath-toolkit/man-oathtool.html):
        A command line tool for generating and validating OTPs.
    -   [pskctool](https://www.nongnu.org/oath-toolkit/man-pskctool.html):
        Portable Symmetric Key Container (PSKC) tool
    -   [pam_oath](https://www.nongnu.org/oath-toolkit/pam_oath.html):
        A PAM module for pluggable login authentication for OATH.
    These components are packaged in Debian.
    -   [OATH Documentation](https://www.nongnu.org/oath-toolkit/docs.html) with
        _previously listed_ manuals for liboath, pskctool.
    -   [pyoath-toolkit](https://github.com/malept/pyoath-toolkit)
        Python bindings for the OATH Toolkit.
    -   [pam_oath - ArchWiki](https://wiki.archlinux.org/title/Pam_oath)
    -   [Two-factor time based (TOTP) SSH authentication with pam_oath and Google
        Authenticator](https://spod.cx/blog/two-factor-ssh-auth-with-pam_oath-google-authenticator.shtml)
-   <a name="google_authenticator"></a>{{< wp "Google Authenticator" >}}
    is a free proprietary, or Apache2 licensed client for Android, iOS, and BlackBerry, and
    also PAM module for the server side, that uses TOTP and HOTP.

    Authenticator provides a six- to eight-digit one-time password which in addition to the
    username and password allow log in to Google services or third-party applications, such
    as password managers or file hosting services.

    It has few open source implementations.

-   [Archwiki: Google Authenticator
    ](https://wiki.archlinux.org/index.php/Google_Authenticator)
-   [google-authenticator-libpam](https://github.com/google/google-authenticator-libpam)
    (Apache-2.0 License)
    is a PAM module demonstrating two-factor authentication for logging into servers via
    SSH, OpenVPN, etc…
    -   {{< man "google-authenticator" >}} command creates a new secret key in the
        current user's home directory.
-   [google-authenticator Home](http://code.google.com/p/google-authenticator/)
-   [Android App: Google Authenticator
    ](https://play.google.com/store/apps/details?id=com.google.android.apps.authenticator2)
-   [OTP Authenticator | F-Droid
    ](https://f-droid.org/en/packages/net.bierbaumer.otp_authenticator/) (MIT License)
    an open source TOTP authenticator compatible with Google Authenticator, with
    encrypted storage
    -   [OTP Authenticator - GitHub](https://github.com/0xbb/otp-authenticator)
-   [FreeOTP](https://freeotp.github.io/) (Apache Licence)
    implements open standards: HOTP and TOTP. Tokens can be added by scanning a QR code.
    There are application for ​Android on Google Play or F-Droid and ​iOS.
    -   [FreeOTP - GitHub](https://github.com/freeotp/freeotp-android).
    -   [FreeOTP](https://f-droid.org/en/packages/org.fedorahosted.freeotp/)
    -   [FreeOTP+ | F-Droid
        ](https://f-droid.org/en/packages/org.liberty.android.freeotpplus/)
         a fork of FreeOTP with enhancements including exporting and importing settings.

## Security Token

-   Wikipedia: {{< wp "Security Token" >}}
-   {{< wp "YubiKey" >}} are USB tokens that act like
    keyboards and generate one-time passwords, they  implement HOTP and TOTP.

-   <a name="nitrokey"></a>[Nitrokey](https://www.nitrokey.com/)
    both hardware and software are open-source.  price start at 29€.

    Nitrokey series:
    -    Nitrokey _storage_, _start_ (29€), and the _nirokey3_ serie support
         OpenPGP/GnuPG _with Gnuk_, S/MIME and can store 3 ECC and 3 RSA key pairs.
    -    Nitrokey _storage_ and _pro_ (49€), _fido2_ (29€) support OTP and FIDO2.
    -    Nitrokey _storage_ (109€ 16GB, 199€ 64GB) has a storage encryption with AES-256
    _   _Nitrokey3_ (49€) supports FIDO2 and FIDO2 UF;
    -   _Nitrokey HSM_ (69€) support S/MIME, and can store 38 RSA pairs and 300 ECC pairs.

    Nitrokey references:
    -   [Nitrokey Documentation](https://docs.nitrokey.com/index.html)
    -   [Nitrokey App](https://github.com/Nitrokey/nitrokey-app)
        is a QT application created to manage Nitrokey Pro and storagedevices, it
        supports TOTP and HOTP.
        Debian contains the package _nitokey-app_.
        -   [Nitrokey Pro, Linux — Nitrokey Documentation
            ](https://docs.nitrokey.com/pro/linux/index.html)
    -   [Nitrokey Encryption Tool](https://github.com/Nitrokey/nitrokey-encryption-tool)
        is a command line interface application which uses on-device RSA keys.
        we use it with Nitrokey HSM.
        -   [Nitrokey HSM with GNU/Linux — Nitrokey Documentation
            ](https://docs.nitrokey.com/hsm/linux/index.html)
    -   For nitrokey start we use {{< iref "#psclite" "psclite" >}} in the Debian
        package _pcscd_. We can also use the {{< iref "#psc-tools" "psc-tools" >}}.
        -   [Nitrokey Start, Linux — Nitrokey Documentation
            ](https://docs.nitrokey.com/start/linux/index.html).
    -   Nitro Key documentation [Desktop Login And Linux User Authentication
        ](https://docs.nitrokey.com/fido2/linux/desktop-login.html) and
        [FIDO2 with Linux](https://docs.nitrokey.com/fido2/linux/index.html) are
        for the nitrokey fido2, u2F is explained in
        [Nitrokey FIDO U2F with Linux](https://docs.nitrokey.com/u2f/linux/index.html).

-   <a name="yubikey"></a>[YubiKeys](https://www.yubico.com/products/)
    are small USB Security tokens, with a panel of features and a price Which vary from
    25€ to 90€.

    Yubikey 5 and YubiKey FIPS serie support; FIDO2/WebAuthn, U2F, Smart card, OpenPGP,
    OTP, with varying connectors USB-A, USB-C, Lightning, NFC. Price from 45€ to 70€.

    YubiKey Bio Series supports FIDO2/WebAuthn, FIDO U2F, with biometric authentication
    with a price of 85€.

    Security Key Series supports FIDO2/WebAuthn, U2F. they connect through NFC and
    either USB-A or USB-C.

    YubiHSM 2 and YubiHSM 2 FIPS are {{< wp "Hardware security module" >}}
    with {{< wp "PKCS 11" >}} protocol with prices of 650€ and 950€.

    -   [YubiKey - ArchWiki](https://wiki.archlinux.org/title/YubiKey).
    -   [yubioath-desktop](https://developers.yubico.com/yubioath-desktop/)
        the Yubico Authenticator is a cross-platform application for generating Open
        Authentication (OATH) time-based TOTP and event-based HOTP one-time password
        codes using a Yubikey.
    -   [yubikey-manager-qt](https://developers.yubico.com/yubikey-manager-qt/)
        is a cross-platform application for configuring any YubiKey over all USB
        interfaces. A command line client is available in the
        [YubiKey Manager CLI](https://developers.yubico.com/yubikey-manager/).
-   [Solo](https://solokeys.com/collections/all)
    is a small USB Security token supporting Universal 2nd Factor (U2F) requests and
    the newer FIDO2 standard. In contrast to Yubikeys the software is open-source.
    The solo price go from 25€ to 45€. They do not support OPENPGP.
    -   [Solo - ArchWiki](https://wiki.archlinux.org/title/Solo)
-   The [Tomu](https://tomu.im/) is a family of FIDO2 security key, with an open-source
    hardware and firmware.
    -   [Tomu - ArchWiki](https://wiki.archlinux.org/title/Tomu)
-   [How to set up 2FA TOTP with KeepassXC, Aegis and Authy. | Linux.org
    ](https://www.linux.org/threads/in-depth-tutorial-how-to-set-up-2fa-totp-with-keepassxc-aegis-and-authy.36577/).

### PAM authentication {#fido_pam}
-   [YubiKey and SSH via PAM
    ](https://developers.yubico.com/yubico-pam/YubiKey_and_SSH_via_PAM.html)
    -   [Pam-U2F module](https://developers.yubico.com/pam-u2f/) which is in the Debian
        package _libpam-yubico_.
    -   [yubico-pam](https://developers.yubico.com/yubico-pam/)
    -   [pam_yubico(8)](https://man.archlinux.org/man/pam_yubico.8)

### FIDO / U2F

-   {{< wp "Universal 2nd Factor" >}} (U2F)
    is an open standard for two-factor authentication (2FA) using USB or NFC, it is
    based on the {{< wp "Client to Authenticator Protocol" >}} (CTAP) and
    {{< wp "WebAuthn" >}} _Wev authentication".

    U2F has a successor FIDO2 which is a standard of the {{< wp "FIDO Alliance" >}}.

    The  CTAP1/U2F protocol is the reference for U2F while CTAP2 protocol is used in
    FIDO2. An authenticator that implements CTAP2 often r implements CTAP1/U2F as well
    to provide backward compatibility with U2F.

    An authenticator may be used in either single-factor mode or multi-factor mode. In
    single-factor mode, the authenticator is activated by a button push.  In
    multi-factor mode, the authenticator is activated by checking  a secret such as a
    PIN, passcode or swipe pattern, or a biometric data.

    The authenticator performs user verification locally on the device, data is not sent
    to the network.

    WebAuthn is supported by Google Chrome, Mozilla Firefox, Microsoft Edge, Apple
    Safari and the Opera web browser.

    Many services support U2F, among which Google, Azure, Dropbox, GitHub, GitLab,
    Bitbucket, Nextcloud, Facebook (supported by Github), Dropbox, Gitlab, Bitbucket,
    it

-   [FIDO Alliance](https://fidoalliance.org/)
    -   [How FIDO Works](https://fidoalliance.org/how-fido-works/)
    -   [Inside the FIDO2 Specifications](https://fidoalliance.org/fido2/)
    -   [FIDO Authentication Specifications
        ](https://fidoalliance.org/specifications/download/)
    -   [FIDO® Certified
        ](https://fidoalliance.org/certification/fido-certified-products/)
        gives products (authenticator, client, server) compliant with the FIDO UAF,
        FIDO U2F and FIDO2 specifications.
    -   [FIDO Certified Showcase](https://fidoalliance.org/fido-certified-showcase/)
        is an other search form which show results by company, with selectable criteria.
-   [Universal 2nd Factor - ArchWiki
    ](https://wiki.archlinux.org/title/Universal_2nd_Factor)
-   [FIDO Universal 2nd Factor (U2F) - yubico
    ](https://www.yubico.com/about/background/fido/)
    can be used in Linux with {{< iref "#fido_pam" "PAM U2F module" >}}
    -   [What is U2F
        ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
    -   [U2F Technical Overview
        ](https://developers.yubico.com/U2F/Protocol_details/Overview.html)
    -   [Using a U2F library
        ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
-   [Extension adding support for U2F standard to Firefox
    ](https://developers.yubico.com/U2F/Libraries/Using_a_library.html)
    U2f is also supported by Chrome.
-   [StrongKey/fido2](https://github.com/StrongKey/fido2) (LGPL-2.1)
    Open-source FIDO server, featuring the FIDO2 standard.
    -   [FIDO2 Server API and Demo
        ](https://demo4.strongkey.com/getstarted/#/openapi/fido)

There are many other FIDO/U2F and FIDO2 authenticators listed in the [FIDO® Certified
](https://fidoalliance.org/certification/fido-certified-products/) page. They should
work on linux but they rarely mention it.

I list some keys only selected by their availability and price in addition to
{{< iref "#nitrokey" "Nitrokey" >}} and {{< iref "#yubikey" "Yubikey" >}} _price
begining 2022_.

-   [HyperFIDO by Hypersecu](https://www.hypersecu.com/hyperfido)
    cheap FIDO2/HOTP keys available on amazon.
-   [FIDO range - NEOWAVE](https://neowave.fr/en/products/fido-range/) includes Keydo
    FIDO U2F _not fido2_ 10€,Winkeo FIDO U2F _not fido2_ 20€, Winkeo FIDO2 25€, Winkeo-C
    FIDO2 _USB C_, Badgeo FIDO2 _a dual interface contact and contactless fido2
    smartcard_ 20€. Neowave is a french industry.

    The fido2 keys are sold on amazon and in their online shop
    [Authentification web](https://authentification-web.fr/).

    Neowave has also a serie of Contact and / or contactless
    [Smart card readers](https://neowave.fr/en/products/smart-card-readers/)
    and USB Micro-SIM card reader; and [USB and smartcard ID 2.0 solutions
    ](https://neowave.fr/en/products/id-2-0-solutions/).

-   [FEITIAN Technologies Co., Ltd.](https://www.ftsafe.com/),the shop is at
    [FEITIAN Store](https://www.ftsafe.com/store/), som product are in the shop
    [Feitian — StakeBox](https://www.stakebox.org/collections/vendors?q=Feitian),
    you can also find some on amazon.
    -   [MultiPass FIDO® Series Multi-interface Security Keys
        ](https://www.ftsafe.com/products/fido/multi) a FIDO-U2F/FIDO2 key with USB, NFC
        and bluetooth. 35€.
    -   [ePass FIDO-NFC Security Key
        ](https://www.ftsafe.com/store/product/epass-fido-nfc-security-key/)
         FIDO U2F & FIDO2 & HOTP, FC & USB-A/USB-C 25€.
-   [TOKEN2 Switzerland](https://www.token2.com/home) have cheap FIDO2 tokens,
    the token with  HOTP, U2F, and FIDO2 cost USB-A  10€ (19€ pack of two) USB-C 12€,
    minikey 18€

    A key adding TOTP with a companion app for iphone, ios or in linux or OSX by using
    the tools integrated into Chromium costs 14€ USB-A, with apped fingerprint
    protection 35€. An USB-A to USB-C adapter cost 2€.

    A key with only U2F (no fido2) is sold 5€.

    _Token2_ produces also non programable TOTP tokens (many models hardware token or display
    card 18€) or programmable TOTP tokens from 22€ to 32€ for pin protected multiple
    profile token.

    There is a comprehensive documentation on companion apps and use including in Linux.
    The shop for EU customers is [TOKEN2 France](https://www.token2.eu/home).

-   [Crayonic KeyVault](https://www.crayonic.com/keyvault) is a FIDO2/HOTP/TOTP/PGPkey
    produced in netherland with micro-usb, nfc, bluetooth and figerprint sensor.




## OpenPGP/GnuPG Key {#gnupg_key}
Debian has the package _scdaemon_ which is used by gpg-agent to access& OpenPGP smart
cards.

-   [GNUK - Debian Wiki](https://wiki.debian.org/GNUK)  is an implementation of USB
    cryptographic token for GNU Privacy Guard. Gnuk supports OpenPGP card protocol
    version 3.

    Hardware requirement for Gnuk is the micro controller STM32F103
-   [YubiKeys](https://www.yubico.com/products/) serie 5 or 5 FIPS series support OPENPGP.
-   {{< iref "#nitrokey" "Nitrokey" >}} start, pro 2, storage 2 support openpgp, with
    Gnuk opensource software.
-   [Olimex - STM32-H103](https://www.olimex.com/Products/ARM/ST/STM32-H103/).
-   [Gnuk on STM32 Blue Pill
    ](https://blog.dan.drown.org/gnuk-open-source-gpg-ssh-hardware-key-storage/).
-   [Development boards | STM32-base project](https://stm32-base.org/boards/):
    [STM32F051C8T6 - F0 Blue Pill](https://stm32-base.org/boards/STM32F051C8T6-Blue-Pill)
-   The {{< wp "OpenPGP card" >}} is a  smart card[2] that is integrated with many
    OpenPGP function, It allows secure storage of private/public OpenPGP key pair;
    Several mutually compatible JavaCard implementations of the OpenPGP Card's interface
    protocol are available as open source software and can be installed on generic
    JavaCard smart cards.  Some Nitrokey and Yubico keys emulate this protocol.

## Smart cards
{{< wp "Smart card" >}} is a plastic credit often card-sized card with an embedded
integrated circuit chip.

{{< wp "Smart_card#Identification" "Cryptographic smart cards" >}} are used for single
sign-on. The most common way to access cryptographic smart card functions on a computer
is to use a vendor-provided {{< wp "PKCS 11" >}} library.

{{v wp "CCID" >}} (chip card interface device) protocol is a USB protocol that allows a
smartcard to be connected to a computer via a card reader using a standard USB
interface, without the need for each manufacturer of smartcards to provide its own
reader or protocol. This allows the smartcard to be used as a security token for
authentication and data encryption.

-   [Smartcards - Debian Wiki](https://wiki.debian.org/Smartcards),
    [fr/Smartcards - Debian Wiki](https://wiki.debian.org/fr/Smartcards)
-   [MUSCLE](https://muscle.apdu.fr/) Movement for the Use of Smart Cards in a Linux
    Environment. Contains:
    -   <a name="psclite"></a>[PCSClite project](https://pcsclite.apdu.fr/)
        Middleware to access a smart card using SCard API ({{< wp "PC/SC" >}}) which
        Handles smart card reader communications and forwarding requests over message
        queues.. It is in the Debian package _pcscd_.
    -   [CCID driver](https://ccid.apdu.fr/) a generic
        {{< wp "CCID_(protocol)" "USB CCID" >}}  (Chip/Smart Card
        Interface Devices) driver and ICCD (Integrated Circuit(s) Card Devices).
    -   [Reader Selection](https://ccid.apdu.fr/select_readers/)
    -   [Ludovic Rousseau's blog](https://ludovicrousseau.blogspot.com/)and
        [GitHub repository](https://github.com/LudovicRousseau).
    -   [GitHub - LudovicRousseau/CCID: CCID driver.](https://github.com/LudovicRousseau/CCID)
    -   <a name="psc-tool"></a>[pcsc-tools
        ](http://ludovic.rousseau.free.fr/softwares/pcsc-tools/) (GPL-2)
        are used to test a PC/SC driver, card or reader or send commands with a CLI or
        GUI. It has a Debian package. It includes:
        -   pcsc_scan: scans every PC/SC reader connected to the host if a card is
            inserted or removed a "line" is printed.
        -   ATR_analysis: is a Perl script used to parse the smart card ATR. This
            script is called (by default) by pcsc_scan.
        -   scriptor: is a Perl script to send commands to a smart card using a batch
            file or stdin.
        -   gscriptor: the same idea as scriptor.pl but with a Perl-Gtk3 GUI.
-   [Online Smart card ATR parsing](https://smartcard-atr.apdu.fr/)
    uses [pyscard - Python for smart cards](https://pyscard.sourceforge.io/).
-   [Feitan card readers](http://www.pcscreader.com/product.html)
    uses the {{< wp "CCID_(protocol)" "CCID protocol" >}} so can be used with
    {{< iref "#psclite" "psclite" >}} {{< iref "#psc-tools" "psc-tools" >}}.
    You can by them on [Smart Card Reader – FEITIAN Store
    ](https://www.ftsafe.com/store/product-category/smart-card-reader/#productCategory))


# Kerberos
-   [Kerberos Infrastructure HOWTO
    ](http://cryptnet.net/fdp/admin/kerby-infra/en/kerby-infra.html)
    covers design and configuration of a Kerberos infrastructure for
    handling authentication with GNU/Linux. _2009_
-   [Tutorial Kerberos
    ](http://varrette.gforge.uni.lu/download/polys/Tutorial_Kerberos.pdf)
    (PDF french) by Sebastien Varrette.

# Password Strength {#password_strength}
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


## Hash cracking {#hash_cracking}
See also {{< iref "network_security#brute_forcer" "Brute forcers" >}}
in the {{< iref "network_security" "network security section" >}}.

{{< wp "Password Cracking" >}} is now mainly done by {{< wp "Rainbow tables" >}} and
{{< wp "Brute-force attack" >}} There are many programs to apply these methods.

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
-   [John the Ripper](https://www.openwall.com/john/) (GPL)
    perform dictionary attacks and brute force cracking. The basic version is GPL and
    available in Debian under the name _john_, there is also a private _Pro_ version.
    An alternative opensource communauty verstion is available at
    [magnumripper/JohnTheRipper](https://github.com/magnumripper/JohnTheRipper).
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

-   __requisite__ -- Failure to authenticate via this module results in immediate denial
    of authentication.
-   __required__ -- Failure also results in denial of authentication, although PAM will
    still call all the other modules listed for this service before denying
    authentication.  For the function to be able to return success to the application
    all `required' modules have to report success.
-   __sufficient__ -- If authentication by this module is successful, PAM will grant
    authentication immediatly.  In the case this module succeed no other stacked module
    is called.
-   __optional__ -- Whether this module succeeds or fails is only significant if it is
    the only module of its type for this service.

### options
-   __use_first_pass__ Use the same password used by the first mechanism that asked for
    a password.
-   __try_first_pass__ This is the same as `use_first_pass', except that if the primary
    password is not valid, it should prompt the user for the password.

For the new syntax:

-   __required__ is equivalent to
    `[new_authtok_reqd=ok ignore=ignore default=bad](success=ok)`
-   __requisite__ is equivalent to
    `[new_authtok_reqd=ok ignore=ignore default=die](success=ok)`
-   __sufficient__ is equivalent to
    `[new_authtok_reqd=done default=ignore](success=done)`
-   __optional__ is equivalent to
    `[new_authtok_reqd=ok default=ignore](success=ok)`

The configuration is in `/etc/pam.d/system-auth`
and `/etc/nsswitch.conf`

# Sudo
[Sudo](https://www.sudo.ws/) llows a system administrator to delegate authority to give
certain users (or groups of users) the ability to run some (or all) commands as root or
another user.

-   [Sudo Home](https://www.sudo.ws/)
-   [sudo - GitHub](https://github.com/sudo-project/sudo)
-   [Sudo - ArchWiki](https://wiki.archlinux.org/title/Sudo)
-   [sudo - Debian Wiki](https://wiki.debian.org/sudo)

__doas__ is a minimal replacement for sudo. It was written for OpenBSD to provide 95% of the
features of sudo with a fraction of the codebase.

-   [OpenDoas](https://github.com/Duncaen/OpenDoas) (BSD License)
    is a portable fork of the OpenBSD `doas` command, it is packaged in Debian.

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
-   [polkit · FreeDesktop GitLab](https://gitlab.freedesktop.org/polkit/polkit/)
-   [polkit(8)
    ](http://www.freedesktop.org/software/polkit/docs/latest/polkit.8.html)
-   [ArchWiki: PolKit](https://wiki.archlinux.org/index.php/PolKit)


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


## SSO
-   {{< wp "Single sign-on" >}} allows users to log in once and gain
    access to all systems without being prompted to log in again.
    This is typically accomplished using LDAP, when the sites are on
    the same domain it can also be achieved using cookies.
-   [Ubuntu SingleSignOn HowTo
    ](https://help.ubuntu.com/community/SingleSignOn)
    describes how to set up network-connected Ubuntu machines to
    support Single Sign On (SSO).
-   {{< wp "OAuth" >}} provides a method for clients to access server resources on behalf
    of a resource  owner (such as a different client or an end-user).
    It also provides a process for end-users to authorize third-party access to their server
    resources without sharing their credentials, using user-agent redirections.
-   {{< wp "Security Assertion Markup Language" >}} or _SAML_
    is an open standard for exchanging authentication and authorization data between
    an identity provider and a service provider. It is used in  web-browser single
    sign-on (SSO).
    -   [SAML at Stanford University IT](https://uit.stanford.edu/service/saml).

### OpenId
-   {{< wp "OpenId" >}}   is a URL based distributed identity system, see also
    [OpenId Home](http://openid.net/).
-   __MyOpenId__  provider have shut down their service in  February
    2014. Other providers are [Replacing MyOpenID
    ](http://evertpot.com/replacing-myopenid/).
-   [IndieAuth](https://indieauth.com/) is an OpenId provider part of
    [IndieWeb](http://indiewebcamp.com/Getting_Started)
-   For OpenId development see [OpenId Wiki](http://wiki.openid.net/Main_Page),
    libraries are available at [openidenabled Home Page](http://www.openidenabled.com/)


<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
