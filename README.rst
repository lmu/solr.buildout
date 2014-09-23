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

    git config --global http.sslVerify false
    git clone https://github.com/loechel/solr.buildout.git

    cd solr.buildout
    python bootstrap.py

