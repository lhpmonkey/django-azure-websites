django-azure-websites
=====================

Example of a django project using mysql that can be deployed to an Azure websites instance.


### Background
Deploying a basic django app on an azure website instance is fairly straightforward, however using any database other than sqllite3 is at first a great challenge.

The solution is to use a pure-python database driver instead of the stock python-mysql ( which azure websites currently cannot run )

The database driver in question is here:
https://github.com/jloic/django-mysql-pymysql


This project simply aims to create a django 1.5.1 template project with a site-packages folder setup ready to deploy to azure websites, and have a mysql db from the word go.

### Instructions

Follow the basic Azure websites tutorial for creating a django site here: 
http://www.windowsazure.com/en-us/develop/python/tutorials/web-sites-with-django/

Use this repository as a base for your project instead. Setup everything else according to the tutorial.

use the included updated wfastcgi.py which fixes a bug with querystring passing in the stock azure version.

