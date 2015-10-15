eZ Publish
==========
[![Travis branch](https://img.shields.io/travis/GMaissa/ansible-role-ezpublish5/master.svg)](https://travis-ci.org/GMaissa/ansible-role-ezpublish5)

This Ansible role configures your environment for [eZ Publish](http://www.ez.no).


Requirements
------------

No external requirements exists for this role.


Role Variables
--------------

    # Define php session save handler
    # Value to false will leave the default value
    ezpublish_php_session_save_handler: false

    # Define php session save path
    # Value to false will leave the default value
    ezpublish_php_session_save_path: false

    # Define php timezone
    ezpublish_php_date_timezone: "Europe/Paris"

    # Define Apache listen port
    ezpublish_apache_port: 80

    # eZ Publish vhost configuration
    ezpublish_apache_vhost:
      filename: ezpublish.conf
      enabled: yes
      listen: '*:80'
      root: /var/www/ezpublish
      name: ezpublish.local
      aliases:
        - bo.ezpublish.local

    # Define trusted proxies for eZ Publish
    ezpublish_trusted_proxies: false

    # Enable|disable eZ Publish cluster mode
    ezpublish_cluster_mode: false

    # Define eZ Publish environment
    ezpublish_environment: prod

    # Enable|disable eZ Publihs debug mode
    ezpublish_debug_mode: 0

    # Download eZ Publish sources
    ezpublish_download: false

    # eZ Publish version to download
    ezpublish_version: v2014.11.1

    # Additional packages
    ezpublish_additional_packages: []


License
-------

BSD


Author Information
------------------

Guillaume Maïssa <pro.g@maissa.fr>
