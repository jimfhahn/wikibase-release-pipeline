Install WikibaseImpoer Extension: through Wikibase Bundle CLI 
(all steps)
====================================
``
cd extensions
``

``
git clone https://github.com/Wikidata/WikibaseImport.git
``

``
cd WikibaseImport
``

Composer install
================
``
apt update
``

``
apt install wget
``

``
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
``

``
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
``

``
php composer-setup.php
``

``
php -r "unlink('composer-setup.php');"
``

``
mv composer.phar /usr/local/bin/composer
``

``
composer install
``

Load Extension Wikibase Importer
=====================
``
cd ..
``

``
cd ..
``

``
apt install nano
``

``
nano LocalSettings.php
``

Add this to the end of the file:

``
wfLoadExtension( 'WikibaseImport' );
``

Create tables in MySql
======================
``
cd maintenance
``

``
php update.php
``

Import Data
============
``
cd ..
``

``
cd extensions 
``

``
cd WikibaseImport
``

``
php maintenance/importEntities.php --entity Q147
``
