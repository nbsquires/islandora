BUILD STATUS
------------
Current build status:
[![Build Status](https://travis-ci.org/Islandora/islandora.png?branch=7.x)](https://travis-ci.org/Islandora/islandora)

CI Server:
http://jenkins.discoverygarden.ca

SUMMARY
-------

Islandora Fedora Repository Module

For installation and customization instructions please see the documentation
and the DuraSpace Wiki:

https://wiki.duraspace.org/display/ISLANDORA/Islandora

All bugs, feature requests and improvement suggestions are tracked at the
DuraSpace JIRA:

https://jira.duraspace.org/browse/ISLANDORA

REQUIREMENTS
------------
The Tuque library must be installed to use Islandora. It can be found here:
http://github.com/Islandora/tuque
It is expected to be in one of two paths:
 - sites/all/libraries/tuque (libraries directory may need to be created)
 - islandora_folder/libraries/tuque

OPTIONAL REQUIREMENTS
---------------------

If you want to support languages other than English download and enable
[String Translation](https://drupal.org/project/i18n), And follow our
[guide](wiki/Multilingual-Support) for setting up additional languges.


INSTALLATION
------------

Before installing Islandora the XACML policies located in the policies folder
should be copied into the Fedora global XACML policies folder. This will allow
"authenticated users" in Drupal to access Fedora API-M functions. It is to be
noted that the permit-upload-to-anonymous-user.xml and
permit-apim-to-anonymous-user.xml files do not need to be present unless
requirements for anonymous ingesting are present.

You will also have to remove some default policies if you want full
functionality as well.

Remove deny-purge-datastream-if-active-or-inactive.xml to allow for purging of
datastream versions.

CONFIGURATION
-------------

The islandora_drupal_filter passes the username of 'anonymous' through to
Fedora for unauthenticated Drupal Users.  A user with the name of 'anonymous'
may have XACML policies applied to them that are meant to be applied to Drupal
users that are not logged in or vice-versa.  This is a potential security issue
that can be plugged by creating a user named 'anonymous' and restricting access
to the account.

Drupal's cron will can be ran to remove expired authentication tokens.

CUSTOMIZATION
-------------

[Customize ingest forms](http://github.com/Islandora/islandora/wiki/Multi-paged-Ingest-Forms)

TROUBLESHOOTING
---------------


F.A.Q.
------


CONTACT
-------


SPONSORS
--------
