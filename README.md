
Role infomation
---------------
Role install Haproxy and config load blance backend postgresql

Role Variables
--------------

	listen_rw:
	  name: pg_5432_rw_rw
	  port: 5442

	listen_ro:
	  name: pg_5433_ro_ro
	  port: 5433

	backend_list_add:
	  - name: node-1
	    ip: 10.0.0.11
	    port: 5432
	  - name: node-2
	    ip: 10.0.0.12
	    port: 5432  
	  - name: node-3
	    ip: 10.0.0.13
	    port: 5432  

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
	 - {role: haproxy-postgresql, tags: haproxy-postgresql}

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
