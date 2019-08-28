keycloak
========

[![Build Status](https://travis-ci.org/andrelohmann/ansible-role-keycloak.svg?branch=master)](https://travis-ci.org/andrelohmann/ansible-role-keycloak)

Use this role to install keycloak.

Requirements
------------

This role requires ubuntu.

Dependencies
------------

This role depends on andrelohmann.percona_mysql and andrelohmann.zulu_openjdk

Role Variables
--------------

The default set of variables defines the settings, keycloak will be installed with

    keycloak_version: 7.0.0
    keycloak_dir: /var/lib/keycloak
    keycloak_archive: keycloak-{{ keycloak_version }}.tar.gz
    keycloak_url: http://downloads.jboss.org/keycloak/{{ keycloak_version }}/{{keycloak_archive }}
    keycloak_jboss_home: "{{ keycloak_dir }}/keycloak-{{ keycloak_version }}"
    keycloak_log_dir: "{{ keycloak_jboss_home }}/standalone/log"
    keycloak_bind_port: "8080"
    keycloak_bind_address: "0.0.0.0"
    keycloak_admin_username: "admin"
    keycloak_admin_password: "admin"
    keycloak_create_admin: True
    keycloak_mysql: False
    keycloak_mysql_connector_version: 8.0.17
    keycloak_mysql_connector_url: "https://dev.mysql.com/get/Downloads/Connector-J/mysql-connector-java-{{ keycloak_mysql_connector_version }}.zip"
    keycloak_mysql_host: localhost
    keycloak_mysql_user: keycloak
    keycloak_mysql_password: keycloak
    keycloak_mysql_database: keycloak
    keycloak_mysql_port: 3306

Example Playbook
----------------

    - hosts: keycloak
      roles:
         - andrelohmann.keycloak

License
-------

MIT

Author Information
------------------

https://github.com/andrelohmann
