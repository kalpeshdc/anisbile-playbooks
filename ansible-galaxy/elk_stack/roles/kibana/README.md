Kibana
=========

Use this role to install kibana on the ubuntu VM using ansible-playbook. Please check /template/kibana.yml.j2 file for kibana configuration.

Requirements
------------

- Ubuntu 16+
- ansible 2.x

Role Variables
--------------

Global Variable (group_vars):
- **es_version**: 6.x

Role Vars (/vars/main.yml):
- **kibana_config_dest_path**: /etc/kibana/kibana.yml
- **kibana_config_source_path**: kibana.yml.j2
- **kibana_server_name**: sre-demo
- **kibana_server_port**: 5601
- **kibana_server_host**: 0.0.0.0

Dependencies
------------

Make sure common role is executed before executing this role.

Example Playbook
----------------

Usags example:

    - hosts: servers
      roles:
      - common
      - kibana

License
-------

BSD
