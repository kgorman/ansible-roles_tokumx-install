ansible-roles_tokumx_install
=========

Installs [TokuMX](http://www.tokutek.com/tokumx-for-mongodb/) and starts up a nice base configuration that should be pre-set for high performance. TokuMX is a high performance fork of the popular MongoDB.

Role Variables
--------------

You will want to hack on the variables in defaults/main.yml to fit your liking. One thing you will absolutely want to change is:

```yaml
TokuMX cache size
mongodb_cache_size: 99000M
```

It's generally recommended to set this to about 80%-90% of main memory on a dedicated DB box.

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

Testing and Requirements
------------------------
This role is tested on Rackspace [onMetal High I/O](http://www.rackspace.com/cloud/servers/onmetal/) servers with Centos 7.

```
uname -a | awk '{print $3}'
3.10.0-123.el7.x86_64
```

License
-------

BSD

Author Information
------------------
[Twitter](http://www.twitter.com/kennygorman)
[Github](www.github.com/kgorman)
