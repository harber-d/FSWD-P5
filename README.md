Item Catalog
============

### Before you get started
* Make sure you have a google account to log into the catalog

### About the instance
* The instance can be accessed via ssh at 52.38.253.248 with port 2200
* Access the catalog at http://ec2-52-38-253-248.us-west-2.compute.amazonaws.com/
This is important because Google's OAuth framework doesn't allow 
external IPs to be used as authorized redirect URIs.

### Changes made:
* Added user "grader" and added them to the sudoers
* Disabled remote ssh root access
* Configured SSH port to 2200, to allow http on port 80, and to allow NTP on port 123
* Gave apache read/write permissions to database and image directory (for item images)
* Added 10.20.15.40 to /etc/hosts to resolve "unable to resolve host ip-10-20-15-40" errors

### Installed items
* Apache web server with mod-wsgi library
* Postgres
* Item catalog source
* Python Flask and related libraries

### Third-party resources
* https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps - used this guide to configure item-catalog.wsgi correctly.
