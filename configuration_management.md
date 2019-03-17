<!--
.. description:
.. date: 2011-10-02
.. slug: configuration_management
.. tags:
.. link:
.. book: mzlinux
.. title: System configuration management
-->


[TOC]



See also
[Monitoring](/node/monitoring "internal reference"),
[Continuous Integration
](/node/software_design#continuous_integration "internal reference").


# Introduction
Configuration Management software allow to do
[w:software configuration management] it includes two main aspects,
first controling the coherence of system software and administering
changes; then recording t(he changes with the ability to review them
and to roll back them. The last part is dealed with in the
[Source Configuration Management section
](/node/scm "internal reference").
but some tools combine the two aspects in an unified front-end.


-   Wikipedia has pages on [w:configuration management] _a general
    panorama_, [w:software configuration management] _deal more with
    source code management_, [w:Network management],
    [w:Network management system].
-   Wikipedia
    [w:comparison of open source configuration management software]
    and
    [w:comparison of web hosting control panels].
-   A [search in alternativeto
    ](http://alternativeto.net/software/webmin/?platform=linux)
    give also a fresh look on present web-based system configuration
    tools.


# Software
-   <a name="ansible"></a>[w:Ansible_(software)|Ansible] is a python
    software that automates software provisioning, configuration
    management, and application deployment. It is  part of Fedora and
    availabe in Debian.

    -   [Ansible Home](http://www.ansible.com/)
    -   [Ansible GitHub repository
        ](https://github.com/ansible/ansible).
    -   [awesome ansible
        ](https://github.com/jdauphant/awesome-ansible)
        list of ansible resources.

    Ansible is close to [Salt](#salt "internal references")
    the following articles compare them:

    -   [Salt vs. Ansible
        ](http://jensrantil.github.io/salt-vs-ansible.html)
    -   [Ansible vs Salt
        ](https://www.upguard.com/articles/ansible-vs-salt)
    -   [SaltStack vs Ansible Revisited
        ](https://www.upguard.com/articles/saltstack-vs-ansible-revisited)
    -   [Puppet vs. Chef vs. Ansible vs. SaltStack
        ](https://www.intigua.com/blog/puppet-vs.-chef-vs.-ansible-vs.-saltstack)
    -   [Ansible vs Salt meta review
        ](http://www.alexandrejoseph.com/blog/2016-03-23-ansible-vs-salt-meta-review.html)

-   [cdist](http://www.nico.schottelius.org/software/cdist/)
    is a configuration management systems, following KISS principle. It has shell
    scripting configuration language and no dependency except /bin/sh and ssh.
    It is in Debian.
-   [w:Froxlor] (GPL)  is a  server-management-panel
    for managing e-mail-addresses, domains, FTP, cron jobs.
    It is a fork of _SysCP_. _Froxlor_ offers packages for Debian and Ubuntu.
    [Froxlor Home](http://www.froxlor.org/).
-   [Puppet](https://puppet.com/) (proprietary and GPL)
    is a client-server tool written in ruby which
    consists of a custom declarative language to describe system
    configuration. It enables administrators to describe the
    configuration in high-level terms, such as users, services and
    packages.

    There is a proprietary _Puppet Entreprise_ and GPL
    _Open source Puppet_ for individuals. See the table of
    [differences between the entreprise and open source Puppet
    ](https://puppet.com/product/puppet-enterprise-and-open-source-puppet).

-   [pyinfra](https://github.com/Fizzadar/pyinfra) (MIT License)
    is an agentless remote server deployment tool and service
    provisioner comparable to
    [Ansible](#ansible "internel reference"),
    -   [pyinfra documentation
        ](https://pyinfra.readthedocs.io/en/latest/)
-   <a name="salt">[w:Salt_(software)|SALT] (Apache license)
    is a configuration management and remote execution application written in Python.<br />
    Salt packages are available in Debian. It is close to
    [Ansible](#ansible "internal reference") see this entry for
    comparisons.
    -   [Salt Open Source Software Project Home](http://www.saltstack.com/community/)
    -   [Salt documentation Home](http://docs.saltstack.com/)
-   [Webmin](http://www.webmin.com/) (BSD License) is a web-based
    interface for system administration.
    It features a plugin system with numerous
    [standard](http://www.webmin.com/standard.html) and
    [third party modules](http://www.webmin.com/third.html)
    -   [Webmin on the Buffalo LinkStation
        ](http://buffalo.nas-central.org/wiki/Webmin_to_remotely_administer_your_LinkStation)
    -   Due to problems in package maintenance, it is no longer part of
        Debian, but a [Debian package](http://www.webmin.com/deb.html)
        is still available.
-   [w:Zentyal] (GPL and proprietary) _previously Ebox_
    is a web interface intended to manage services in a computer network,
    it is based on apache and mod perl.
    Zentyal provide an
    [Ubuntu package](https://wiki.zentyal.org/wiki/Installation_Guide)
    and can be
    [installed in Debian
    ](http://www.debianadmin.com/manage-network-and-servers-using-ebox-in-debian.html).

<!--  Local Variables: -->
<!--  mode: markdown -->
<!--  ispell-local-dictionary: "english" -->
<!--  End: -->
