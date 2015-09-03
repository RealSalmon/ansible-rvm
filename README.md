[![Build Status](https://travis-ci.org/RealSalmon/ansible-rvm.svg?branch=master)](https://travis-ci.org/RealSalmon/ansible-rvm)

RealSalmon.rvm
==============
Ansible role to perform a user-level rvm installation

Requirements
------------
- Ubuntu 14.04
- Ansible 1.9

Role Variables
--------------
- rvm_user: "{{ ansible_ssh_user }}"
- rvm_become: true
- rvm_rubies: "ruby-head"
- rvm_update: false
- rvm_cmd_path: "~{{ rvm_user }}/.rvm/bin/rvm"
- rvm_installer_dir: "~{{ rvm_user}}/bin"
- rvm_installer_file: "rvm-installer.sh"

Dependencies
------------
None

Example Playbook
----------------
    ---
    - hosts: all
      vars:
        rvm_user: joeuser
      roles:
        - RealSalmon.rvm-prerequisites
        - RealSalmon.rvm

License
-------
BSD

Author Information
------------------
Ben Jones <ben@fogbutter.com>
