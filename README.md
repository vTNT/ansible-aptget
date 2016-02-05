# Ansible role for Aptget

apt-get update;apt-get upgrade

## Tested On

  * Ubuntu 14.04

## Defaults

The `defaults/main.yml` should be pretty clear on the usage and values. The 
version used by defaults are:

  * `aptget_update`: True
  * `aptget_update_cache_valid_time`: 3600
  * `aptget_upgrade`: False

## Usage

The tests in the respository should be pretty straight forward, but here are
some examples:

### Apt-get

playbook.yml:

```
- name: Install and run apt-get
  hosts: all
  sudo: True

  vars:
    aptget_upgrade: True
  
  roles:
    - { role: ansible-aptget }

```

## TODO

  * Extract supervisor to it's own role
  * Extend to other distros

