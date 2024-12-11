Role Name
=========

This role creates a basic config for vim. If you need to change vim configuration settings, make the changes in ./templates/vimrc.j2. Before use this role. If I decide that I should configure something for more convenient use of the server, I will do it here. 

Requirements
------------

No requirements are required.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass --tags=configure-environment
~~~

License
-------

BSD

