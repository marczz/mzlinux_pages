---
title: Network Security
---

See also
{{< iref "./security" "Security" >}},
{{< iref "firewall" "Firewall" >}},
{{< iref "encrypt" "Encryption" >}},
{{< iref "authentication" "Authentication" >}},
{{< iref "ssl" "SSL / TLS" >}},
{{< iref "vpn" "Vpn" >}},
{{< iref "nettools" "Network Tools" >}},
{{< iref "monitoring" "Monitoring" >}},
{{< iref "mail" "mail section" >}} for securing the MTA
such as {{< iref "mail#postfix" "Postfix" >}}.

-----

# References

Don't miss references in
{{< iref "security#references" "Security references" >}}.

-   [Securing networks - Red Hat Enterprise Linux 8
    ](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/8/html/securing_networks/index)
-   Wikipedia: {{< wp "Intrusion detection system" >}},
    {{< wp "Intrusion prevention system" >}}.
-   [OWASP testing Guide v4
    ](https://www.owasp.org/index.php/OWASP_Testing_Guide_v4_Table_of_Contents).
    provide a complete testing framework delivered a complete testing framework
    for web applications.
-   [OWASP Testing Guide list of testing tools
    ](https://www.owasp.org/index.php/Appendix_A:_Testing_Tools)
-   [Darknet Networking Hacking resources
    ](https://www.darknet.org.uk/category/hacking-tools/networking-hacking/).

# Network intrusion detection
## Intrusion Detection Systems (IDS)
See also {{< iref "security#forensic_tools" "Forensic Tools" >}}
and {{< iref "lightweight_distributions#forensic_distributions" "Forensic Distributions" >}}.

-   {{< wp " Intrusion detection system" >}}, {{< wp "Port scanner" >}}

-   Some sites offers to test the ports of
    __the system from which you connect__ :
    [Shields UP! Internet Vulnerability Profiling
    ](https://grc.com/x/ne.dll?bh0bkyd2),
    [Scan my ports with check.sdv.fr](http://check.sdv.fr:3658/cgi/scan)
-   {{< wp "Nikto_Scanner" >}} (GPL) is a Web server scanner that
    tests Web servers for dangerous files/CGIs.
    [CIRT Nikto2 Home Page](http://www.cirt.net/nikto2)

-   [Checksecurity
    ](https://manpages.debian.org/stretch/checksecurity/checksecurity.8.en.html)
    do some very basic system security checks on insecurely mounted
    remote file systems, open ports to detect rogue programs, empty or
    duplicate system accounts, mounted filesystems nearing capacity,
    scan iptables logs to look for intrusion attempts. _Checksecurity_
    is a Debian package.
-   <a name="nmap"></a>{{< wp "Nmap" >}} (GPL)
    is a network exploration tool and security scanner.  There are GTK
    front ends `nmapfe` or `xnmap`.
    -   [nmap Home](http://nmap.org/)
    -   {{< wp "Nmap"  "Wikipedia Nmap page" >}}.
    -   [nmap Reference Guide](https://nmap.org/book/man.html).
    -   [nmap(1)
        ](https://manpages.debian.org/stretch/nmap/nmap.1.en.html).
-   [Snort](http://en.wikipedia.org/wiki/Snort_%28software%29)(GPL)
    is a network intrusion detection system. It is in Debain.
    -   [Snort Home](http://www.snort.org/)
-   [Suricata](http://suricata-ids.org/) (GPL)
    is a high performance Network IDS, IPS and Network Security
    Monitoring engine. It is in Debian.

## Brute forcers {#brute_forcers}
See also {{< iref "authentication#hash_cracking" "Hash Cracking" >}} in the
{{< iref "authentication" "Authentication Section" >}}.

-   [THC-Hydra](https://github.com/vanhauser-thc/thc-hydra)
    is a parallelized login cracker which supports numerous protocols
    Cisco, CVS, FTP, HTTP(S), ICQ, IMAP, IRC, LDAP, MS-SQL, MySQL,
    NNTP, Oracle, NFS, POP3, PostgreSQL, RDP, Rexec, Rlogin, Rsh, SIP,
    SMB, SMTP, SNMP, SOCKS5, SSH, Subversion, Teamspeak, Telnet,
    VMware-Auth, VNC and XMPP.
    Hydra is in Debian.
    -   _hydra-gtk_ is a GTK gui for hydra, it is in Debian.
    -   [Hydra, un outil de Bruteforce en ligne
        ](https://www.supinfo.com/articles/single/6336-hydra-outil-bruteforce-ligne)
        a tutorial by Adrien Flahaut.
-   [Medusa](http://foofus.net/goons/jmk/medusa/medusa.html)
    is a parallel, and modular, login brute-forcer.  It support many
    protocols (see [this page
    ](http://foofus.net/goons/jmk/medusa/medusa-compare.html)).
    It is in Debian.
    -   [GitHub - Medusa](https://github.com/jmk-foofus/medusa)
    -   [Comparison of Medusa, Hydra, Ncrack
        ](http://foofus.net/goons/jmk/medusa/medusa-compare.html))
-   [ncrack](https://nmap.org/ncrack/man.html) from the
    {{< iref "#nmap" "Nmap tools suite" >}}
    is a high-speed network authentication cracking tool. _ncrack_ is
    a Debian package.
-   [Patator](https://github.com/lanjelot/patator) (GPL)
    Patator is a multi-purpose brute-forcer, with a modular design It
    support many protocols: dns, imap, ftp, java keystore, ldap,
    mssql, mysql, oracle, pgsql, pop, smb, smtp, snmp, ssh, telnet,
    unzip, vnc It is in Debian.

-  [Get SSH username & Password For Any Server easily with Brute Force Attack
   ](https://securitytraning.com/brute-force-ssh/)
   a tutorial using either ncrack, hydra, or medusa.

## Penetration testing
-   Wikipedia {{< wp "Penetration test" >}}, {{< wp "Category:Computer security" >}}.
-   [ArchWiki - List of applications/Security
    ](https://wiki.archlinux.org/index.php/List_of_applications/Security

-   [Bro](https://www.bro.org/) (BSD License)
    is a network analysis framework. It inspects all traffic on a link
    for signs of suspicious activity. It performs analysis and
    detection tasks, including detecting malware by interfacing to
    external registries, reporting vulnerable versions of software
    seen on the network, identifying popular web applications,
    detecting SSH brute-forcing, validating SSL certificate chains.
    _Bro_ is available in multiple Debian packages: _bro_, _broctl_,
    _bro-aux_, _bro-pkg_.
-   {{< wp "Lynis" >}}
    is a security auditing tool for Linux, it can perform
    Security auditing, Compliance testing (e.g. PCI, HIPAA, SOx),
    Penetration testing,  Vulnerability detection, System hardening.
    -   [Lynis Home](https://cisofy.com/lynis/)
    -   [GitHub - Lynis](https://github.com/CISOfy/lynis)
    -   [Debian Admin - Lynis
        ](http://www.debianadmin.com/lynis-security-and-system-auditing-tool.html)
-   {{< wp "Metasploit" >}} (BSD License, private source commercail version)
    is a penetration testing framework.
    -   [Metasploit Home Page)(https://www.metasploit.com/)
    -   [GitHub - Metasploit Framework
        ](https://github.com/rapid7/metasploit-framework).
    -   [Metasploit Framework Wiki
        ](https://github.com/rapid7/metasploit-framework/wiki).
    -   [ArchWiki - Metasploit Framework
        ](https://wiki.archlinux.org/index.php/Metasploit_Framework).
    -   [WikiBook: Metasploit
        ](https://en.wikibooks.org/wiki/Metasploit).
-   {{< wp "Nessus" >}} (proprietary, free for personal use)
    Nessus is a vulnerability scanner, previously opensource, but
    which switched to private source in 2005.
-   {{< wp "OpenVAS" >}} (GPL)
    is a remote security scanner It is a fork of Nessus when this
    later became private source in 2005.  It is in Debian.
    -   [OpenVas Home](http://www.openvas.org/)
    -   [ArchWiki - OpenVas
        ](https://wiki.archlinux.org/index.php/OpenVAS).

# Web security exploits
-   Wikipedia:
    -   {{< wp "Category:Web_security_exploits"  "Wikipedia category: Web security exploits" >}},
        {{< wp "Internet security" >}}
    -   {{< wp "Session_hijacking"  "Session hijacking" >}}
        is the hijacking of a session key to gain unauthorized access
        to  web information or services.
    -   {{< wp "Fuzzing" >}}
-   [Fuzz Testing Tutorial: Fuzzing Strategy & Tools
    ](https://www.guru99.com/fuzz-testing.html).


-   [Dirb](http://dirb.sourceforge.net/)
    is a Web Content Scanner. It looks for existing (and/or hidden)
    Web Objects. It basically works by launching a dictionary based
    attack against a web server and analizing the response.
    It is a content scanner not a vulnerability scanner.
    _Dirb_ is in Debian.
-   [Qualys SSL Server Test
    ](https://www.ssllabs.com/ssltest/index.html)
    is a free online service performs a deep analysis of the
    configuration of any SSL web server on the public Internet.
-   [Wapiti](http://wapiti.sourceforge.net/)
    is an application to audit the security of web applications. It
    performs "black-box" scans, i.e. it does not study the source code
    but will scan the web pages, looking for scripts and forms where it can inject
    data. Once it gets this list, Wapiti do {{< wp "Fuzzing" >}} by injecting
    payloads to see if a script is vulnerable. _Waipiti is in Debian_.

    Wapiti can detect the following vulnerabilities:

    -   file handling errors (local and remote include/require, fopen,
        readfile...)
    -   database injection (PHP/JSP/ASP SQL Injections and XPath
        Injections)
    -   XSS (Cross Site Scripting) injection
    -   LDAP injection
    -   command execution detection (eval(), system(), passtru()...)
    -   CRLF injection (HTTP response splitting, session fixation...)
-   _SPIKE proXy_
    is an an HTTP and HTTPS proxy, which includes automated tools to provide
    SQL Injection detection, web crawling, login form brute forcing ,
    overflow detection, d directory traversal detection.
    It also rovide access to the entire  web application interface,
    and allow viewing and changing all variables, cookies, headers, or
    other parts of a request and resubmit it. It is in the Debian
    package _spikeproxy_.
-   [Wfuzz](http://www.edge-security.com/wfuzz.php) (GPL)
    is a python tool designed for bruteforcing Web Applications, it
    can be used for finding resources not linked directories,
    servlets, scripts, etc, bruteforce GET and POST parameters for
    checking different kind of injections (SQL, XSS, LDAP,etc),
    bruteforce Forms parameters (User/Password), Fuzzing, etc.
    _Wfuzz_ is in Debian.
    -   [GitHub - Wfuzz](https://github.com/xmendez/wfuzz).
-   [Zed Attack Proxy (ZAP)](https://github.com/zaproxy/zaproxy)
    (Apache Licence)
    is a java security tool to find vulnerabilities in web
    applications.  It can be also used for manual penetration testing.

# Forensic Distributions {#forensic_distributions}
-   <a name="kali_linux"></a>[Kali Linux](https://www.kali.org/)
    is a Debian-based Linux
    distribution aimed at Penetration Testing and Security
    Auditing. It can run on X86, amd64, armel and armhf computers.
    Kali Linux is  available for BeagleBone Black, HP
    Chromebook, CubieBoard 2, CuBox, CuBox-i, Raspberry Pi, EfikaMX,
    Odroid U2, Odroid XU, Odroid XU3, Samsung Chromebook, Utilite Pro,
    Galaxy Note 10.1 and SS808.<br/>
    It can be installed on live-iso, usb, pxe booted
    image, disk image or encrypted disk image.
    -   Wikipedia {{< wp "Kali Linux" >}}
    -   [Kali Linux Documentation](http://docs.kali.org/)
    -   [Kali list of tools
        ](http://tools.kali.org/tools-listing)
        each tool name reference a page describing it.
-   <a name="remnux"></a>[REMnux](https://remnux.org/)
    is an unbuntu based forensic distribution, that is based on REMnux
    is a free Linux toolkit for assisting malware analysts with
    reverse-engineering malicious software.
    -   [REMnux list of tools](https://remnux.org/docs/distro/tools/)
        the use of the tool are summarized in the
        [Usage Tips for Malware Analysis on Linux
        ](https://zeltser.com/remnux-malware-analysis-tips/).

<!-- Local Variables: -->
<!-- mode: markdown -->
<!-- ispell-local-dictionary: "english" -->
<!-- End: -->
