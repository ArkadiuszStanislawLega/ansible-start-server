add-rules-fail2ban
=========

This role creates failn2ban rules for nginx to block:

- nginx-badbots: Blocks access to bots and crawlers that try to access the site or perform attacks.
- nginx-noscript: Prevents attempts to access hidden configuration or system files.

Then it runs fail2ban.

Requirements
------------

All requirements are installed in the install-dependencies role. If it was started before you started this role, you should install fail2ban on the host.

Role Variables
--------------

In the templates file, change port = 2222 to the one we will use for ssh.

Dependencies
------------

You should run install-dependencies role beforehand.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass --tags=add-rules-fail2ban
~~~

License
-------

BSD

