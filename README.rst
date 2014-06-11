======================
Mofa - Mobile FHNW App
======================

Requirements
============

See moxie

Python 2.7
buildout

Installation
============

Bootstrap and run buildout ::

 $ python2.7 bootstrap.py
 $ bin/buildout

Start and terminate solr server manually the first time. This will create a directory structure for solr which
is needed to copy the jts libraries to. ::

 $ cd parts/solr/example
 $ java -jar start.jar

Copy the jts libraries ::

 $ cd <buildout-dir>
 $ bin/buildout install extra-config

Include environment variables in current shell ::

 $ source bin/mofaenv.sh

Start the supervisor ::

 $ bin/supervisord
