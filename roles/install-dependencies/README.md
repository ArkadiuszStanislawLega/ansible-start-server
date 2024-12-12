install-dependencies
=========

In this role, the necessary services and programs needed to run the django project are installed. Docker is not installed here, for docker installation, a separate role is prepared.

Requirements
------------

Internet connection.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass --tags=install-dependencies
~~~

License
-------

BSD

