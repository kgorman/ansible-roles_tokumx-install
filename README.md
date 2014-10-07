ansible-roles_tokumx_install
=========

Installs TokuMX and starts up a nice base configuration that should be pre-set for high performance. TokuMX is a high performance fork of the popular MongoDB.

Role Variables
--------------

You will want to hack on the variables in vars/mail.yml to fit your liking.


Install
-------
[See here](https://galaxy.ansible.com/intro)

Example Playbook
----------------

To use this simply setup a YAML file for running:

```yaml
$>cat test.yml
---
- hosts: mongoservers
  roles:
  - { role: ansible-roles_tokumx-install }
```

```yaml
$>cat hosts.txt
[mongoservers]
0.0.0.0
```

and execute like:
```bash
$>ansible-playbook -i hosts.txt test.yml
```

License
-------

Apache

Author Information
------------------
[Twitter](http://www.twitter.com/kennygorman)
[Github](www.github.com/kgorman)
