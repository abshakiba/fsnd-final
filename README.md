## Connection details:

* IP: `http://35.182.53.192`
* SSH Port: `2200`
* link: `http://35.182.53.192.xip.io`

** `ssh grader@35.182.53.192 -i key`

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
