Role Name
=========

Configure one or more openvpn  server instances...
working on FreeBSD and OpenBSD, will see later for linux

ldap authentication currently not implemented
brige mode  not currently implemented

Requirements
------------

The host must be able to install packages

Role Variables
--------------

TODO

Dependencies
------------

No dependencies

Example Playbook
----------------
    - hosts: servers
      roles:
         - { role: boxeman.openvpn }
         - { role: boxeman.openvpn, openvpn_instance_name: openvpn_name1, openvpn_instance: "{{ openvpn_name1 }}"
         - { role: boxeman.openvpn, openvpn_instance_name: openvpn_name2, openvpn_instance: "{{ openvpn_name2 }}"
      vars:
      openvpn_name1:
        openvpn_server: 10.1.1.0 255.255.255.0
        openvpn_port: 1191
        openvpn_use_pam: yes
        openvpn_use_pam_users:
        - [ name: user1, password: toto ]
        - [ name: user2, password: toto ]
      openvpn_name2:
        openvpn_server: 10.1.2.0 255.255.255.0
        openvpn_port: 1192
        openvpn_use_simple_auth : yes
        openvpn_use_simple_autj_passord: '5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8'

License
-------

BSD

Author Information
------------------

:)

