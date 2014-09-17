solr.buildout
=============
zypper in git git-core java-1_7_0-ibm

cd /data
git config --global http.sslVerify false

git clone https://github.com/loechel/solr.buildout.git

cd /data/solr.buildout/
python bootstrap.py
