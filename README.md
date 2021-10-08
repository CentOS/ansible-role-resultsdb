Role Name
=========

A brief description of the role goes here.

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      vars:
        resultsdb_namespace: gating-services
        resultsdb_amqp_url: amqps://resultsdb:@rabbitmq.fedoraproject.org/%2Fpubsub
        resultsdb_topic_prefix: org.stream.centos.prod
        resultsdb_secret_key: '12345'
        resultsdb_database_uri: ''
        resultsdb_additional_result_outcomes:
          - CRASHED
          - QUEUED
          - RUNNING
        resultsdb_httpd_username: resultsdb
        resultsdb_httpd_password: resultsdb
        resultsdb_replicas: 1
        resultsdb_image_name: quay.io/fedora/resultsdb:latest
        resultsdb_image_pull_policy: Always
        resultsdb_fedora_messaging: true # skips fedora messaging config if set to false
        resultsdb_fedora_messaging_ca_path: ''
        resultsdb_fedora_messaging_crt_path: ''
        resultsdb_fedora_messaging_key_path: ''

      roles:
         - { role: ansible-role-resultsdb }

License
-------

MIT

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
