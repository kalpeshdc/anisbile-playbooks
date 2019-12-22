Elasticsearch
=========

Use this role to install elasticsearch on the ubuntu VM using ansible-playbook. Please check /template/elasticsearch.yml.j2 file for elasticsearch configuration.

Requirements
------------

- Ubuntu 16+
- ansible 2.x

Role Variables
--------------

Global Variable (group_vars):
- **es_version**: 6.x

Role Vars (/vars/main.yml):
- **es_data_path:** /data/elasticsearch/data
- **es_logs_path**: /data/elasticsearch/log
- **es_config_source_path**: elasticsearch.yml.j2
- **es_config_dest_path**: /etc/elasticsearch/elasticsearch.yml
- **es_cluster_name**: cluster-name

Dependencies
------------

Make sure common role is executed before executing this role.

Example Playbook
----------------

Usage example:

    - hosts: servers
      roles:
      - common
      - elasticsearch

License
-------

BSD

