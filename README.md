Role Name
=========

dotfiles

[![Build Status](https://travis-ci.org/cmihai-ansible/dotfiles.svg?branch=master)](https://travis-ci.org/cmihai-ansible/dotfiles)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/dotfiles](https://galaxy.ansible.com/crivetimihai/dotfiles)

```bash
ansible-galaxy install crivetimihai.dotfiles
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
dotfiles_remove_packages: true
dotfiles_enable_service: true
dotfiles_enable_selinux: true
dotfiles_firewall_configure: true
dotfiles_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install dotfiles on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: dotfiles is configured
      import_role:
        name: crivetimihai.dotfiles
      vars:
        dotfiles_remove_packages: true
        dotfiles_enable_service: true
        dotfiles_firewall_configure: true
        dotfiles_firewall_rules:
          - service:
      tags: dotfiles
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
