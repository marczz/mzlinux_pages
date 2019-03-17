<!--
.. description:
.. date: 2016-09-12
.. slug: ssl
.. tags:
.. link:
.. book: mzlinux
.. title: SSL/TLS
-->

[TOC]

---

This Page is on Transport Layer Security (TLS) and its predecessor,
Secure Sockets Layer (SSL) they provides endpoint authentication
and communications privacy using cryptography. See also
<!-- [Gnu privacy Guard (GPG) and PGP page](/node/ "internal
reference"),
-->
[SSH](/node/ssh "internal reference"),
<!--[Javascript encryption libraries](/node/107#js_encrypt "internal
--reference")
-->

-   [w:Transport Layer Security],
    [w:Symmetric-key cryptography],
    [w:Public-key cryptography],
    [w:Cipher],
    [w:Block cipher modes of operation],
    and the hundred of page in [w:Portal:Cryptography]
-   [w:GNU Privacy Guard|Wikipedia: GNU Privacy Guard],
-   Open source implementations of TLS are provided by
    [w:OpenSSL]
    and [w:GnuTLS],
    OpenSSL has an apache like license that entail some
    [license incompabilities](http://en.wikipedia.org/wiki/OpenSSL#GPL_exception)
    with GPL software. GnuTLS has a LGPL license.
-   Wikipedia: [w:Comparison of TLS implementations]
-   [OpenSSL Project](http://www.openssl.org/), The command line tool
    is [Openssl(1)](http://www.openssl.org/docs/apps/openssl.html).
-   [Ubuntu OpenSSL HowTo](https://help.ubuntu.com/community/OpenSSL).
-   Paul Heinlein's
    [OpenSSL Command-Line HOWTO](http://www.madboa.com/geek/openssl/)
    is a  clear, concise, up to date,  introduction to the use of openssl
    command line to create digest, encrypt/decrypt and manage certificates.
-   [Encryption and Decryption with OpenSSL
    ](http://farid.hajji.name/blog/2009/07/15/encryption-and-decryption-with-openssl/)
    is an openssl tutorial by Farid Hajji with a section on acquiring passwords, and one on
    the relation between passwords, keys and IVs. Is is followed by a tutorial on
    [Public-key Cryptography](http://farid.hajji.name/blog/2009/07/27/public-key-cryptography-with-openssl/)
    and
    [Public Key Infrastructure](http://farid.hajji.name/blog/2009/07/27/public-key-cryptography-with-openssl/).
-   [OpenSSL Hacks](http://www.linuxjournal.com/node/8958/)
    and [GnuPG Hacks](http://www.linuxjournal.com/article/8732) by Tony Stieber
    focus mainly on password strength, an on digests.
-   [WolfSSL and [Yassl](https://www.wolfssl.com/) (GPL and
    commercial licence) are is a lightweight C-language-based SSL/TLS
    library targeted for embedded, RTOS,
    and ssl library implemented in C++ with (some
    level of ?) compatibility with openssl api. **CyaSSL** is a
    lightweight version. The complete SSLv3/TLSv1.1 client/server
    footprint is under 60K.
-   [Qca](http://delta.affinix.com/qca/) (LGPL) is the Qt
    Cryptographic Architecture, Qt depends on QT but not on a full kde
    environment.
-   [sslwrap](http://www.rickk.com/sslwrap/)
    and [stunnel](http://www.stunnel.org/) are two
    wrappers to pack a tcp connection insto a secure socket layer.

## Certificates
-   Paul Heinlein's
    [OpenSSL Command-Line HOWTO](http://www.madboa.com/geek/openssl/)
    is a very clear and concise introduction to the use of openssl
    command line. It includes a certificate management HowTo.
    It is updated very often _checked in 2016_.
-   Openssl [FAQ](http://www.openssl.org/support/faq.html) and
    [manpages](https://www.openssl.org/docs/manmaster/apps/)
    [certificates.txt](http://www.openssl.org/docs/HOWTO/certificates.txt),
    [key.txt](http://www.openssl.org/docs/HOWTO/keys.txt),
    [proxy\_certificates.txt](http://www.openssl.org/docs/HOWTO/proxy_certificates.txt).They
    are also part of the OpenSSL distribution, in doc/HOWTO/
-
    [OpenSSL Cookbook
    ](https://www.feistyduck.com/books/openssl-cookbook/)
    covers the most frequently used OpenSSL features and commands. It
    is updated often. _checked version 2016_.
-   [SSL Certificates HOWTO](http://tldp.org/HOWTO/SSL-Certificates-HOWTO/)
    by Franck Martin _obsolete 2002_
-   [Zitrax survival guide - SSL/TLS and X.509 (SSL) Certificates
    ](http://www.zytrax.com/tech/survival/ssl.html)
    explains also how to create self signed certificates, for root, server, CA, Subordinate CAs,
    Intermediate and Cross certificates.
-   [Notes pour la création de CA avec OpenSSL
    ](http://zertrin.org/how-to/openssl-ca/) par zertrin.
-   [CAcert wiki](http://wiki.cacert.org/wiki/)
-   [Apache SSL Indtroduction](http://httpd.apache.org/docs/ssl/ssl_intro.html#certificates) :
    [Certificates](http://httpd.apache.org/docs/ssl/ssl_intro.html#certificates)
-   [Apache SSL FAQ](http://httpd.apache.org/docs/ssl/ssl_faq.html) :
    [about certificates](http://httpd.apache.org/docs/ssl/ssl_faq.html#aboutcerts).
-   See also the [Apache page](node/252).

## Simple Authentication and Security Layer (SASL)

-   [Wikipedia:SASL](http://en.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer)
-   [RFC 4422](http://tools.ietf.org/html/rfc4422 "ietf.org rfc4422")
    - Simple Authentication and Security Layer (SASL) - obsoletes
    [RFC 2222](http://tools.ietf.org/html/rfc2222 "ietf.org rfc2222");
    [RFC 4505](http://tools.ietf.org/html/rfc4505 "ietf.org rfc4505") -
    Anonymous Simple Authentication and Security Layer (SASL) Mechanism
    - obsoletes
    [RFC 2245](http://tools.ietf.org/html/rfc2245 "ietf.org rfc2245").
