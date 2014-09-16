Role Name
========

The purpose of this role is to install diaspora to a web server and enable
access with nginx. This install uses the MySQL backend rather than Postgres. The
diaspora server name can be specified by changing the diaspora_hostname variable
in defaults/main.yml.

This has only been trusted on Ubuntu trusty. It will not work as-is on precise
as diaspora requires ruby 1.9 and precise uses ruby 1.8 as the system binary.

Role Variables
--------------

- diaspora_hostname: hostname that diaspora will service, will be set to 
                     "diaspora" by default
- diaspora_port: hostname that diaspora will service, will be set to 8888 by 
                 default.
- diaspora_root_mysql_password: root mysql password, will be set to a random 
                                value by default.
- diaspora_diaspora_mysql_password: diaspora mysql password, will be set to a 
                                    random value by default

Example Playbook
-------------------------

Including an example of how to use your role (for instance, with variables 
passed in as parameters) is always nice for users too:

    - hosts: default
      sudo: True
      roles:
        - diaspora

Try it Out
---------------------------

Check out the diaspora repository, vagrant up, and load http://localhost:8888 in
your web browser.

License
-------

GPLv2

Author Information
------------------

http://stillwell.me

