virtualbox
=========

An Ansible role that installs VirtualBox.

Requirements
------------

This target host must run Linux. For VirtualBox to be of any use after it's installed, the target host should have virtualization extensions enabled and preferably not be a virtual machine.

Role Variables
--------------

- `virtualbox_version`: Set this to the version you want to install.
- `virtualbox_user`: Set this to a user account that you want added to the `vboxusers` group (allows that user to use VirtualBox without elevating privileges).

Dependencies
------------

See meta/main.yml.

Example Playbook
----------------

```yaml
- hosts: localhost
  roles:
     - role: devoperate.virtualbox
       vars:
         virtualbox_version: '6.0'
         virtualbox_user: '{{ ansible_user }}' # The user that called the playbook.
```

License
-------

See LICENSE.

Author Information
------------------

- [Claude Léveillé](https://claude-leveille.com)
