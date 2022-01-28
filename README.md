MongoDB (mongodb)
=========

This role/playbook will help in installing MongoDB instance 5.0 or any specific version on RHEL machine

Requirements
------------

We need RHEL VM to install MongoDB instance, where OS image should be hardened with latest patches, yum configuration should be enabled and should have a proper naming convention to connect with applications

Role Variables
--------------

At this moment, we are using only one variable to specific the version of MongoDB instance.
```
mongodb_version: "5.0"
```

Dependencies
------------

Operating system dependencies like Yum update, latest packages like net-tools, wget and epel-release would be an added advantage.
Also, check the status of SELinux as well, better to be in permissive mode.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```
---
- hosts: mongodb_instance
  gather_facts: true
  become: true

  tasks:
    - include_role:
        name: mongodb
```

License
-------

BSD/MIT

Author Information
------------------

https://www.linkedin.com/in/raghavendra-guttur-24525420/

