egeneralov.openvpn
=========

Provide twice openvpn installation (with full iptables configuration). Also will be created users .ovpn config files.

Will be used ports with external ip binding: 53(udp) and 8443(tcp). Yes, every user will have 2 config files.

Requirements
------------

Any debian-based system with systemd.

Role Variables
--------------


- my_clients: list with strings (names for client)
- verb: int, openvpn verbosity
- days: int, certificate valid for
- country_name: str, ISO country.
- organization_name: str, any, will be included into crt

Dependencies
------------

- egeneralov.base
- egeneralov.iptables

Example Playbook
----------------

    - hosts: openvpn
      vars:
        my_clients:
          - client
          - tneilc
      roles:
        - egeneralov.openvpn

License
-------

MIT

Author Information
------------------

Eduard Generalov <eduard@generalov.net>
