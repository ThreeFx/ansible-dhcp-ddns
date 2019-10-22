dhcp-ddns
=========

Sets up isc-dhcp-server with automatic DDNS updates to BIND9. Currently IPv4
only.

Requirements
------------

None.

Role Variables
--------------

| Variable Name | Default Value | Description |
--------------- |---------------|--------------
 **`dhcp_ddns_domain_name`** | - | Domain to use for DDNS updates, must be set
 `dhcp_ddns_v4_dhcp_interfaces` | [] | Interfaces on which dhcpd should listen
 `dhcp_ddns_v6_dhcp_interfaces` | [] | _currently unused_
 `dhcp_ddns_v4_dns_servers` | [] | DNS servers which should be advertised
 `dhcp_ddns_v4_subnets` | [] | Subnets which should be configured, see `defaults/main.yml` for more information
 `dhcp_ddns_v4_reverse_zones` | Reverse zones for PTR updates. Only /24 supported, see `defaults/main.yml` for more information
 `dhcp_ddns_v4_static_mappings` | [] | Static mappings between MACs and IP addresses, swee `defaults/main.yml` for more information
 `dhcp_ddns_key` | `"ddns_key"` | Name of the key used for signing DDNS updates
 `dhcp_ddns_key_hmac_algorithm` | `hmac-sha384` | Hash used for signing DDNS updates

Dependencies
------------

None.

Example Playbook
----------------

See `molecule/default/playbook.yml`.

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx)
