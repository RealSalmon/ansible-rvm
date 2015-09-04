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
- rvm_rubies: ruby-head
- rvm_update: false
- rvm_install_path: ~{{ rvm_user }}/.rvm
- rvm_installer_dir: ~{{ rvm_user }}/bin
- rvm_installer_file: rvm-installer.sh

Dependencies
------------
None

Example Playbook
----------------
    ---
    - hosts: all
      roles:
        - RealSalmon.rvm-prerequisites
        - {role: RealSalmon.rvm, become: true, become_method: sudo, rvm_user: joeuser}
        - {role: RealSalmon.rvm, become: true, become_method: sudo, rvm_user: jrubyguy, rubies: "ruby-head,jruby"}

License
-------
BSD

Author Information
------------------
Ben Jones <ben@fogbutter.com>
