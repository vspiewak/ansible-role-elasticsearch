Ansible role for Elasticsearch
==============================

This role use https://github.com/vrischmann/ansible-role-java

Sample of variables:

    elasticsearch:
      version: 1.4
      clustername: my-elasticsearch-cluster
      nodename: node-master-{{ hostvars[inventory_hostname]['ec2_id'] }}
      quorom: 3
      number_of_replicas: 4
      plugins:
        - head
        - hq
        - bigdesk
        - kopf
        - paramedic

    java_versions: 
      - oracle-java8-installer
