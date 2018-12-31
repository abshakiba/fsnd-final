## Connection details:

* IP: `http://35.182.53.192`
* SSH Port: `22`, `2200`
* link: `http://35.182.53.192.xip.io`

### `ssh grader@35.182.53.192 -i key`

## Configuration

* Installed several packages for python3, apache, flask, sqlalchemy, requests, etc.

* Created the project folder in `/var/www/`. Created a virtual environment.

* Created a conf file for the virtual env in `/etc/apache2/site-available/catalog.conf`

* Cloned Item Catalog project from GitHub.

* Changed the ownership and access permissions of my database file.


## Grader User

* Created a new user `grader`

* Added grader to the sudoers list.

* Create a new pair of ssh key on my local machine and copied the public key on the server
