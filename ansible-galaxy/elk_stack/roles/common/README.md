Common Role
=========

Role to configure the dependencies on the VM. This role also installs Java on the VM.

Role Variables
--------------

This role requires elasticsearch version. If not set it will pickup the ``es_version`` from the group_vars/all.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: elk_vm
      roles:
      - common

License
-------

BSD
