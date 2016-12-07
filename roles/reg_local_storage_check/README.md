Regression Test - Local Storage Used Size
============

This role check if local storage has enough space
 - 100% : FAIL
 - 99% - 80% : WARN 
 - 79% - 70% : INFO

Requirements
------------

Role Variables
--------------

From this role:

| Name                    | Default value                                 | Description                                                                 |
|-------------------------|-----------------------------------------------|-----------------------------------------------------------------------------|
| regression_result_path  | /tmp                                          | Regression Test result folder                                               |

Dependencies
------------


Example Playbook
----------------

```
---
 - name: Check if local storage has enough spaces. Full of /var, /var/log, /var/lib/docker and docker-pool can impact OCP.
   hosts: all
   gather_facts: false

   roles:
    - { role: reg_local_storage_check }

```

License
-------

Apache License Version 2.0

Author Information
------------------

Jooho Lee (jlee@redhat.com)