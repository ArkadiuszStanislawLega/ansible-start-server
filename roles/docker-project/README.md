docker-project
=========

In this role, the archive from the django project is copied, the environment files are prepared for it. The service for the project is set up. The first start-up takes place, static files are collected and the database is prepared. After starting this role, if we have a well-prepared archive with the project, we can check in web browser whether the project has started and is working correctly.

Requirements
------------

It is required to copy the project archive to the ./files/app.tar directory.

Dependencies
------------

Apart from executing previous roles, especially the one where docker is installed, there is no need to install additional dependencies.

Example Playbook
----------------

~~~bash
ansible-playbook -i hosts.yaml main_playbook.yaml --ask-become-pass tags=docker-project
~~~

License
-------

BSD

