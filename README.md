Base (Ansidev)
=========
[![Build Status](https://travis-ci.org/Ilyes512/ansible-role-base.svg)](https://travis-ci.org/Ilyes512/ansible-role-base)

This role installs (base) apt packages for Ubuntu Trusty (14.04).

Requirements
------------

No requirements.

Role Variables
--------------

```
ansidev_package_state: present
ansidev_production: false

base_package_state: "{{ ansidev_package_state }}"
base_upgrade_packages: "no" # Options: "no"|"yes"|safe|full|dist
base_force_upgrade_packages: true
base_sys_packages:
  - curl
  - wget
  - software-properties-common
  - python-software-properties
  - git
  - vim
  - unzip
base_local_sys_packages: []
base_production_sys_packages:
  - tmux
  - nano
  - fail2ban
  - logrotate
  - acl
  - htop
```

Dependencies
------------

No dependencies.

Example Playbook
----------------
```
- hosts: servers
  roles:
    - { role: ilyes512.base, tag: ['ansidev.base'] }
```

License
-------

MIT

Author Information
------------------

Ilyes Ahidar [@Ilyes512](https://twitter.com/ilyes512)
