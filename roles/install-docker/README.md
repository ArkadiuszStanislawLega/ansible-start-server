install-docker
=========

In this role, docker is downloaded, installed and the user is added to the docker group.

Requirements
------------

Internet connection.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --aks-become-pass --tags=install-docker
~~~

License
-------

BSD

