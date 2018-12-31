## Connection details:

* IP: `http://35.182.53.192`
* SSH Port: `2200`
* link: `http://35.182.53.192.xip.io`

**`ssh grader@35.182.53.192 -i key`**

## Configuration
### Installed several packages for the OS:
  * apache2
  * libapache2-mod-wsgi
  * libapache2-mod-wsgi-py3
  * python-pip
  * python3-pip
  * python-dev
  * python3-venv
  * postgresql (Not used)
  * finger

### Install several packages for python:
  * flask
  * sqlalchemy
  * requests
  * virtualenv
  * oauth2client
  * requests

### Environment and Apache Configuration:
* Created the project folder in `/var/www/`. Created a virtual environment.
* Created a conf file for the virtual env in `/etc/apache2/site-available/catalog.conf`
* Cloned Item Catalog project from GitHub.
* Changed the ownership and access permissions of my database file.

## Security Configuration
### SSH
* Changed the port to `2200` instead of `22`
* `PermitRootLogin no`
* `PasswordAuthentication no`

### Firewall `ufw`
* 2200/tcp, ALLOW, Anywhere                  
* 80/tcp, ALLOW, Anywhere                  
* 123, ALLOW, Anywhere                  
* 2200/tcp (v6), ALLOW, Anywhere (v6)             
* 80/tcp (v6), ALLOW, Anywhere (v6)             
* 123 (v6), ALLOW, Anywhere (v6)

## Grader User
* Created a new user `grader`
* Added grader to the sudoers list.
* Create a new pair of ssh key on my local machine and copied the public key on the server

## Third Party Resources

Many articles and links, including, but not limited to:
* https://atom.io
* https://getbootstrap.com/
* https://github.com/hhatto/autopep8
* http://maxdesign.com.au/articles/select-required/
* https://github.com/googleapis/oauth2client
* http://manpages.ubuntu.com/manpages/xenial/en/man5/sshd_config.5.html
* https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps#step-four-%E2%80%93-configure-and-enable-a-new-virtual-host
* https://www.digitalocean.com/community/tutorials/how-to-install-python-3-and-set-up-a-local-programming-environment-on-ubuntu-16-04
* https://stackoverflow.com/questions/48218065/programmingerror-sqlite-objects-created-in-a-thread-can-only-be-used-in-that-sa
* https://serverfault.com/questions/57596/why-do-i-get-sqlite-error-unable-to-open-database-file
