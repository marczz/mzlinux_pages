---
title: SSL/TLS
---

See also {{< iref "authentication" "Authentication" >}}

This Page is on Transport Layer Security (TLS) and its predecessor,
Secure Sockets Layer (SSL) they provides endpoint authentication
and communications privacy using cryptography. See also
[Gnu privacy Guard (GPG) and PGP page of my Unix Memo
](https://unix-memo.readthedocs.io/en/latest/gnupg.html) and the
[SSH page](https://unix-memo.readthedocs.io/en/latest/ssh.html).

-   {{< wp "Transport Layer Security" >}},
    {{< wp "Symmetric-key cryptography" >}},
    {{< wp "Public-key cryptography" >}},
    {{< wp "Cipher" >}},
    {{< wp "Block cipher modes of operation" >}},
    and the hundred of page in {{< wp "Portal:Cryptography" >}}
-   {{< wp "GNU Privacy Guard"  "Wikipedia: GNU Privacy Guard" >}},
-   Open source implementations of TLS are provided by
    {{< wp "OpenSSL" >}}
    and {{< wp "GnuTLS" >}},
    OpenSSL has an apache like license that entail some
    [license incompabilities](http://en.wikipedia.org/wiki/OpenSSL#GPL_exception)
    with GPL software. GnuTLS has a LGPL license.
-   Wikipedia: {{< wp "Comparison of TLS implementations" >}}
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
    [proxy\_certificates.txt](http://www.openssl.org/docs/HOWTO/proxy_certificates.txt).
    They are also part of the OpenSSL distribution, in doc/HOWTO/
-   [OpenSSL Cookbook
    ](https://www.feistyduck.com/books/openssl-cookbook/)
    covers the most frequently used OpenSSL features and commands. It is a free book
    in pdf, epub and online and is updated often. _checked version 2016_.

    The cookbook is taken from a book of [Ivan Ristić](https://blog.ivanristic.com/)
    _Bulletproof SSL and TLS_ second edition 2021.

    Two other articles are available in [SSL Labs](https://www.ssllabs.com/) Github
    [research wiki](https://github.com/ssllabs/research/wiki) :
    [SSL and TLS Deployment Best Practices
    ](https://github.com/ssllabs/research/wiki/SSL-and-TLS-Deployment-Best-Practices)
    and [SSL Server Rating Guide
    ](https://github.com/ssllabs/research/wiki/SSL-Server-Rating-Guide).

    This [wiki](https://github.com/ssllabs/research/wiki) gives also lists of
    assessment tools, attack tools, configuration tools.
-   [SSL Certificates HOWTO](http://tldp.org/HOWTO/SSL-Certificates-HOWTO/)
    by Franck Martin _obsolete 2002_
-   [Zitrax survival guide - SSL/TLS and X.509 (SSL) Certificates
    ](http://www.zytrax.com/tech/survival/ssl.html)
    explains also how to create self signed certificates, for root, server, CA,
    Subordinate CAs, Intermediate and Cross certificates. _update in december 2019_.
-   [Notes pour la création de CA avec OpenSSL
    ](http://zertrin.org/how-to/openssl-ca/) par zertrin.
-   [CAcert wiki](http://wiki.cacert.org/wiki/)
-   [Apache SSL Introduction](http://httpd.apache.org/docs/ssl/ssl_intro.html) :
    -   [Certificates](http://httpd.apache.org/docs/ssl/ssl_intro.html#certificates)
    -   [about certificates](http://httpd.apache.org/docs/ssl/ssl_faq.html#aboutcerts).
    -   [Apache SSL FAQ](http://httpd.apache.org/docs/ssl/ssl_faq.html) :
    -   [Name based SSL Vhosts With SNI
        ](https://cwiki.apache.org/confluence/display/httpd/NameBasedSSLVHostsWithSNI)
-   {{< man "openssl(1)" >}}
-   See also {{< iref "apache#mod_ssl" "Apache mod_ssl deocumentation" >}} .

### Certificate providers
-   [CAcert](http://wiki.cacert.org/) deliver free server certificates.
    -   [FAQ/ServerCerts
        ](http://wiki.cacert.org/FAQ/ServerCerts?action=show&redirect=ServerCerts)
        explain how to produce the certificate request (CSR)
    -   Wikipedia {{< wp "Cacert" >}}.
-   [Let's Encrypt - Wikipedia](https://en.wikipedia.org/wiki/Let%27s%5FEncrypt)
    -   [Let's Encrypt](https://letsencrypt.org/) provides X.509 certificates for
        Transport Layer Security (TLS) encryption at no charge.
    -   [Let's Encrypt Community Support](https://community.letsencrypt.org/)
    -   [Certbot](https://certbot.eff.org/) is an open source software tool, made by the
        Electronic Frontier Foundation (EFF), for automatically using Let’s Encrypt
        certificates on manually-administrated websites to enable HTTPS.
-   [SSLkeys - Debian Wiki](https://wiki.debian.org/SSLkeys)
-   {{< man "update-ca-certificates(8)" >}} is a program that updates the directory
    `/etc/ssl/certs` to hold SSL certificates and generates `ca-certificates.crt`.


## Simple Authentication and Security Layer (SASL)

-   [Wikipedia:SASL](http://en.wikipedia.org/wiki/Simple_Authentication_and_Security_Layer)
-   [RFC 4422](http://tools.ietf.org/html/rfc4422 "ietf.org rfc4422")
    - Simple Authentication and Security Layer (SASL) - obsoletes
    [RFC 2222](http://tools.ietf.org/html/rfc2222 "ietf.org rfc2222");
    [RFC 4505](http://tools.ietf.org/html/rfc4505 "ietf.org rfc4505") -
    Anonymous Simple Authentication and Security Layer (SASL) Mechanism
    - obsoletes
    [RFC 2245](http://tools.ietf.org/html/rfc2245 "ietf.org rfc2245").
