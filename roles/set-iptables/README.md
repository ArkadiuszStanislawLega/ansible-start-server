set-iptables
=========

In this role, the rules for allowing network traffic in iptables are entered. A service is created to enter these rules every time the server is restarted.

Requirements
------------

Installed iptabels.

Role Variables
--------------

We need to change:
~~~bash
sudo iptables -A INPUT -p tcp --dport 2222 -j ACCEPT
~~~
to the port that we determined ssh uses.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass tags=set-iptables
~~~

License
-------

BSD

