copy-ssh-key
=========

We copy id_ed25519.pub to the server, because later any access to the server other than via ssh and already known hosts will be blocked.

Requirements
------------

It is required to generate id_ed25519.pub for the user who will later remotely connect to the hosts. There is a tutorial for this, for example, on the github page.

Role Variables
--------------

You should change the path to the generated public key, the variable, w katalogu ./vars/main.yml:
~~~bash
ssh_public_key_path
~~~

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass --tags=copy-ssh-key
~~~

License
-------

BSD

