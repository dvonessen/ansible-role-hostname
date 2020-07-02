# ansible-role-hostname

Ansible role which sets the system hostname.

## Description

This role configures the fqdn and hostname. It also maintains `/etc/hosts` file, means that it is possible to add
multiple IP addresses and FQDNs to the system, e.g. if no DNS is available or it is a small local network.

## Role Variables


| Name           | Default | Description                                                                                                                                |
| :------------- | :-----: | ------------------------------------------------------------------------------------------------------------------------------------------ |
| hostname_fqdn  |   ""    | Fully qulified domain name for system. It will be set for each IP address configured on system. Except, if overwritten in `hostname_hosts` |
| hostname_hosts |   {}    | Map IP address to hostname. See [defaults/main.yml](defaults/main.yml)                                                                     |

## Role Tags

| Name         | Description                     |
| ------------ | ------------------------------- |
| hostname_all | Run all tasks within this role. |

## Dependencies

**None**

## Example Playbook


```yaml
- name: All
  hosts: all
  debugger: on_failed
  roles:
    - role: ansible-role-hostname
```

## License

MIT License

## Contributors

Daniel von Eßen
