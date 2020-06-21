ansible-role-apache
=========
Basic role to setup Apache 2. The role is prepared for usage with froxlor.

Requirements
------------
This role was created for Debian 10.x (Buster). It is configured to work with [froxlor](https://froxlor.org).

You might use this role in conjunction with the roles:

* ansible-role-mysql
* ansible-role-froxlor
* ansible-role-postfix
* ansible-role-dovecot

Role Variables
--------------

In `defaults/main.yaml` the following variables and default-values are specified.

```yaml
# Apache modules to load
apache_modules_load:
  - headers
  - ssl

# Apache modules to unload
apache_modules_unload:
  - userdir
```
Example Playbook
----------------
This role can be easily used in a playbook like this: 

```yaml
- hosts: froxlor-servers
  roles:
      - ansible-role-postfix
```

License
-------
GNU GENERAL PUBLIC LICENSE VERSION 3

Author Information
------------------
[blog.retter.jetzt](https://blog.retter.jetzt)