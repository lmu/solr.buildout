=============
solr.buildout
=============

This buildout is a provisioning setup for the Open Source Search Engine Web-Wrapper Apache Solr/Lucene.




------------
Installation
------------


Prerequirements
===============

To use Solr you need a Java Runtime Environment. In order to run this buildout Python 2.4+ is required, as additional Python Services as Supervisor a Python 2.6+ is recommended.






SLES 11 SP 3
------------


.. code:: bash
    
    # Install Java Runtime Environment to run jetty/solr
    zypper install java-1_7_0-ibm

    # install GIT to use this buildout in version control
    zypper install git git-core 


Ubuntu 14.04 / Debian 7.6 („Wheezy“)
------------------------------------

.. code:: bash

    sudo apt-get install 
    sudo apt-get install git 



Checkout the buildout
=====================

.. code:: bash

    git clone https://github.com/loechel/solr.buildout.git

    cd solr.buildout
    python bootstrap.py

If the Checkout from GitHub fails due to proxy / ssl issues, set git flag to ignore ssl checks:

.. code:: bash

    git config --global http.sslVerify false

Configure Secrets
=================

This buildout need a set of login and password for Supervisor. As you should never have usernames and passwords in version control, you have to create a secrets.cfg file that contains those required secrets. 

.. code:: bash

    cp secrets.cfg.tmpl secrets.cfg

Run Buildout to setup Solr
==========================

This buildout contains 3 major cfg-files:

* buildout.cfg
* master.cfg
* slave.cfg

you could run 

.. code:: bash

    # run for buildout.cfg
    ./bin/buildout

    # run for master/slave.cfg
    ./bin/buildout -c master.cfg
    # or
    ./bin/buildout -c slave.cfg


