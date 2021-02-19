Unterstützte Tags und entsprechende `Dockerfile` Links
======================================================

 - [`latest` (*latest/Dockerfile*)](https://github.com/kurthuwig/docker-shopware/blob/master/Dockerfile)

Was ist Shopware?
=================

Shopware is a flexible, powerful and scalable software solution with which you can quickly and easily create an online shop for all requirements.

These instructions describe how to start Shopware with Docker. We recommend installing the docker-compose program . With this program installed, you create the file docker-compose.ymland can then start the containers much more easily than with the Docker CLI. If you are using an older Docker version, e.g. under Ubuntu 14.04 LTS, then use fig , the predecessor of docker-compose. The operation is identical, you just have to replace the text docker-composewith in all examples fig. This also applies to the file name, i.e. from docker-compose.ymlis fig.yml. All commands are also described for the Docker CLI in case you docker-composedon't want to use them.

These instructions also describe how to create a suitable database server for the shop. If you already have one, skip everything related shopwaredbto.

The configuration described stores all persistent data on the Docker host in the directory local volume or /var/lib/docker/persistent-volumes/shopware/. This should be secured.

Installation
============

Shopware initialisieren
-----------------------

Clone the URL:-
git clone https://github.com/deck-app/shopware.git

cd shopware

    docker-compose up -d

Then open the URL [http://localhost/recovery/install/](http://localhost/recovery/install/) in a browser.
If you do not run Docker on your computer but on another server, replace it `localhost` with the name or IP of the server. 
[Hier](http://wiki.shopware.com/Shopware-4-Installer_detail_874.html) is a very good guide on how to use the installer:

1. In the first step, select your language and click on "Next".
2. In the second step, scroll all the way down and click "Next".
3. Enter the name as the database serverdb . Enter the database user , database password and database name each shopwareone and click "Next"
4. In the next step click on "Start" and as soon as the two runs are finished, click on "Next".
5. Select the license type you want and click "Next".
6. Adjust the Shopware basic configuration according to your needs and click on "Next" to complete the setup.