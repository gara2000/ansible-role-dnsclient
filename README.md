DNSSERVER
=========

This role Enables DNS on a server

Requirements
------------

- Should run on Ubuntu distribution
- A DNS Server should already be configured

Role Variables
--------------

This role requires 2 variables to be set:
- domain [default: test.net]: the domain name 
- dnsserver_ip [required]: the ip of the local DNS server 

Dependencies
------------

No dependencies

Example Playbook
----------------
```bash
- hosts: servers
  become: yes
  vars:
    domain: "my_domain.net"
    dnsserver_ip: "192.168.60.4"
  roles:
      - gara2000.dnsclient 
```

License
-------

BSD