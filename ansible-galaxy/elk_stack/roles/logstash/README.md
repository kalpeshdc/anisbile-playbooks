Logstash
=========

Use this role to install logstash on the ubuntu VM using ansible-playbook. Please check templates/logstash-5400.conf.j2 file for logstash pipeline configuration.

Requirements
------------

- Ubuntu 16+
- ansible 2.x

Role Variables
--------------

Global Variable (group_vars/all):
- **es_version**: 6.x

Role Vars (/vars/main.yml):
- **logstash_pipeline_config_dest_path**: /etc/logstash/conf.d/logstash-5400.conf
- **logstash_pipeline_config_source_path**: logstash-5400.conf.j2
- **logstash_index_pattern**: demo-%{indexName}
- **elasticsearch_server**: localhost:9200

Dependencies
------------

Make sure common role is executed before executing this role.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
        - common
        - logstash

License
-------

BSD
