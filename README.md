# Ansible Role: Netdata Installation

[![CI](https://github.com/simplificator/ansible-role-netdata_installation/workflows/CI/badge.svg?event=push)](https://github.com/simplificator/ansible-role-netdata_installation/actions?query=workflow%3ACI)

An Ansible Role that installs a plain version of [Netdata](https://www.netdata.cloud/).

Both our [Netdata node](https://github.com/simplificator/ansible-role-netdata_node) and [Netdata collector](https://github.com/simplificator/ansible-role-netdata_collector) role use this role as a common base for installing Netdata.

## Requirements

N/A

## Role Variables

The role doesn't require any variable to be set. The following are available for customization:

* `netdata_installation_version`: The version of Netdata that will be installed.
* `netdata_installation_certificate`: If you plan to use our collector role, we require to provision a certificate to encrypt traffic between client and collector. Set the certificate with this variable.
* `netdata_installation_certificate_key`: Key for the mentioned traffic certificate.
* `netdata_installation_disable_cloud`: Set it to `yes` if your Netdata installation should make a connection to Netdata cloud. Disabled per default.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: myserver
  roles:
    - { role: simplificator.netdata_installation }
```

## Development

### Variable naming

To ensure that our Netdata roles remain compatible with each other, follow this variable naming convention:

* Role-specific variables are prefixed with the role name (`netdata_installation_` in this case).
* General variables that are used in multiple roles will be prefixed with just `netdata_`.

## License

MIT / BSD
