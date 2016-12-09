Ansible Role: Directory v1.0
===

[![Build Status](https://travis-ci.org/mm0/ansible-role-directory.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-directory)


An Ansible role that simply runs the file module to create a directory.

Occassionally, you will need to create a directory between role executions, there is no built-in way to do this, instead use this role in between.

See Also: ansible-role-touch


Requirements
---

None 

Role Variables
---

Available variables are listed below, along with default values:

```yml
owner: ubuntu # owner of final directory uploaded remotely
group: ubuntu 
mode: 644 # mode for remote directory
directories: # a list of directories to create
```
Dependencies

None 

Example Playbook
---
```yml
- hosts: webservers
  roles:
  - { role: ansible-role-directory,
      directories: ["/var/log/mylog","/var/log/mylog.2""],
      owner: ubuntu,
      group: ubuntu,
      mode: "0755"
    }
```

License
---------------

BSD-2

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
