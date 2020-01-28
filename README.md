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
 `dhcp_ddns_domain_name` | - | required, domain to use for DDNS updates, must be set
 `dhcp_ddns_v4_dhcp_interfaces` | [] | required, interfaces on which dhcpd should listen
 `dhcp_ddns_v6_dhcp_interfaces` | [] | _currently unused_
 `dhcp_ddns_v4_dns_servers` | [] | optional, default DNS servers which should be advertised
 `dhcp_ddns_v4_subnets` | [] | optional, subnets which should be configured, see `defaults/main.yml` for more information
 `dhcp_ddns_bind_allowed_hosts` | [] | optional, hosts / ip ranges allowed to query BIND9, put at least localhost addresses here.
 `dhcp_ddns_key` | `"ddns_key"` | optional, name of the key used for signing DDNS updates
 `dhcp_ddns_key_hmac_algorithm` | `hmac-sha384` | optional, hash used for signing DDNS updates

Dependencies
------------

None.

## Optional

Works well with my [unbound](https://github.com/ThreeFx/unbound) role.

Example Playbook
----------------

See `molecule/default/playbook.yml`.

License
-------

BSD

Author Information
------------------

Find me on [GitHub](https://github.com/ThreeFx).
