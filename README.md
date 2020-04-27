Ansible Role: Rethinkdb
=========

install and configure [Rethinkdb](https://rethinkdb.com) proxy On GNU/Debian 10.

Requirements
------------

Compatible with Debian 10. `sudo`, `ca-certificates` and `apt-transport-https`must be available on the server.

Role Variables
--------------

Available variables are listed below :

  rethinkdb_version: 2.3.7~0buster

Rethinkdb Version to use (default: 2.3.7~0buster).


	rethinkdb_joins:  
 	  - ip: 10.0.0.1
	    port: 29015
	  - ip: 10.0.0.2
	    port: 29015

Array of host and transport to join to. (Cluster'nodes)

Dependencies
------------

None

Example Playbook
----------------

    - hosts: Proxy_host
      roles:
         - gpkfr.rethinkdb-proxy
      
       vars:
        rethinkdb_joins:
          - ip: 10.0.0.1
            port: 29015
          - ip: 10.0.0.2
            port: 29015
  
License
-------

MIT / BSD

Author Information
------------------

This role was created in 2019 by gpkfr.

