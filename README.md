[![Build Status](https://travis-ci.org/Blue-Bag/ansible-role-first5init.svg?branch=main)](https://travis-ci.org/Blue-Bag/ansible-role-first5init)

# Ansible Role: First5Init
=========

Part of the Blue-Bag First5 set.
This role is designed to be run first to run any initialising tasks


At present it contains the following tasks:

SELInux  Prerequisites:

If SELinux is installed you may get the following message:

  msg: Aborting, target uses selinux but python bindings (libselinux-python) aren't installed!

If SELinux is installed then we need the python library - libselinux-python

Handy check to to a fact if SELInux is in operation

TO_DO: enumerate states - it maybe necessary for other tasks to determine the actual state
At present it only sets present | absent


## Requirements
------------

None

## Role Variables
--------------



## Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      gather_facts: true
      tags: ['provision_core']

      roles:
        - { role: ansible-role-first5init, tags: ['provision'], become: true}

## License
-------

MIT / BSD

## Author Information
------------------

George Boobyer Blue-Bag

refs:
https://github.com/ansible/ansible-examples/commit/c769d5e045cb8e5b992c9ad71f9ee2109cb2c897
