Ansible Start Server
=========

This project allows you to set up a Django project web server on nginx and with a postgressql database. Additionally, it sets up basic ssh protocol and iptables security. Django, nginx and postgressql are set up in a different repository. Thanks to this repository, you can just throw an archived and prepared django project into the ./docker -project/files/app.tar role and wait until it finishes. This project allows you to set up a Django project web server on nginx and with a postgressql database. Additionally, it sets up basic ssh and iptables protocol security.

Requirements
------------

To run the project, you need to create a docker-compose in which the django project supported by nginx and postgressql will be set up. You can find one on my profile. Then you need to change the project variables according to the REDME guidelines of the individual roles. No additional ansible libraries are used.

Variables
--------------

First of all, you need to change the host address in the hosts.yaml file, username in the main_playbook.yaml file. The next variables should be changed according to the README descriptions.

Dependencies
------------

All dependencies are installed in the install-dependencies role, then depending on the django project, separate dependencies should be installed in containers thanks to docker-compose.

Example Playbook
----------------

The --ask-vault-pass argument is of course optional. Each project role can be started individually after the tag, as in the example below.

~~~bash
ansible-playbook -i hosts.yaml main-playbook.yaml --ask-become-pass --ask-vault-pass
ansible-playbook -i hosts.yaml main-playbook.yaml --tags=docker-project
~~~

License
-------

BSD

