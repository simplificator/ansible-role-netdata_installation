# Ansible Role: Netdata Installation

[![CI](https://github.com/simplificator/ansible-role-netdata_installation/workflows/CI/badge.svg?event=push)](https://github.com/simplificator/ansible-role-netdata_installation/actions?query=workflow%3ACI)

An Ansible Role that installs a plain version of [Netdata](https://www.netdata.cloud/).

Both our [Netdata client](https://github.com/simplificator/ansible-role-netdata_client) and [Netdata server](https://github.com/simplificator/ansible-role-netdata_server) role use this role as a common base for installing Netdata.

## Requirements

N/A

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

* `netdata_version`: "1.32.1"

If you plan to send metrics from a client to a server, the role allows to distribute a certificate and a key by setting the variables `netdata_server_certificate` and `netdata_server_certificate_key`.

## Dependencies

None.

## Example Playbook

```yaml
- hosts: myserver
  roles:
    - { role: simplificator.netdata_installation }
```

## License

MIT / BSD
