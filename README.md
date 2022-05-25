# Ansible Role for the mysqld_exporter

![molecule](https://github.com/elan-ev/monitoring_mysqld_exporter/actions/workflows/molecule.yml/badge.svg)

Install the latest [mysqld_exporter](https://github.com/prometheus/mysqld_exporter) version with [ansible](https://docs.ansible.com/).

## Role Variables

There are only two variables, both are required: `mysqld_exporter_password` for the
exporter user on the database and `mysqld_exporter_db_root_password` to be able to create said user.

## Example Playbook

If you do not want to change the defaults, just add the role to your playbook:

```yaml
- hosts: all
  become: true
  roles:
    - role: elan.monitoring_mysqld_exporter
      vars:
        mysqld_exporter_password: 1234
        mysqld_exporter_db_root_password: 5678
```

## License

[BSD-3-Clause](LICENSE)

## Author Information

[ELAN e.V](https://elan-ev.de/)
