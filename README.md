# Ansible Netdata Installation role

This role can do a basic installation of Netdata without any configuration.

Optional variables:

* `netdata_server_certificate`: If this variable is defined, it'll copy a certificate to `/etc/netdata/ssl/cert.pem` which can be picked up to encrypt traffic between two Netdata instances.
* `netdata_server_certificate_key`: If this variable is defined, it'll copy a certificate key to `/etc/netdata/ssl/key.pem`.
