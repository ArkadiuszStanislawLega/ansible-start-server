set-ssh-settings
=========

In this role I change ssh settings, I secure the server from logging in with a password. To be sure, before starting this role, check if you are listed in the .ssh/authorized_keys file in your home directory.

Role Variables
--------------

new_ssh_port in ./vars/main.yml shuld be set. 


Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass --tags=set-ssh-settings
~~~

License
-------

BSD

