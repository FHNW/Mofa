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

Create notifications database ::

 $ bin/moxiepy src/moxie-notifications/create_db.py

Include environment variables in current shell ::

 $ source bin/mofaenv.sh

Start the supervisor ::

 $ bin/supervisord


Deploying App
=============

Fetch git repositories not handled by mr.developer: ::

 $ cd src/moxie-phonegap/mobilefhnw/moxie-js-client
 $ git submodule init
 $ git submodule update


Install dependencies (in directory
*src/moxie-phonegap/mobilefhnw/moxie-js-client*): ::

 $ bundle install --path=.

Developing App
==============

 Generate APP ::

 $ cd src/moxie-phonegap/mobilefhnw/
 $ make assets

