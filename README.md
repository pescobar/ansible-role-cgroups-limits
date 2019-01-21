[![Build Status](https://travis-ci.org/pescobar/ansible-role-cgroups-limits.svg?branch=master)](https://travis-ci.org/pescobar/ansible-role-cgroups-limits)
[![Ansible Galaxy](https://img.shields.io/badge/galaxy-pescobar.katello_agent-blue.svg)](https://galaxy.ansible.com/pescobar/cgroups_mem_limit)

ansible-role-cgroups-limits
=========

Configure a memory cgroup limit for users in a group

This role was written to limit the amount of ram memory that a single user can
allocate in a login node in an HPC cluster to avoid a single user consuming 
all the ram in the login node an hanging the machine.

Role Variables
--------------

```
cgroup_memory_limit: '10G'

cgroup_to_whom_the_limit_applies: '@users'
```

Dependencies
------------

none

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: ansible-role-cgroups-limits, cgroup_memory_limit: "15G" }

Requirements
------------

None

License
-------

GPLv3

Author Information
------------------

Pablo Escobar Lopez

