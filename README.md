# Ansible Role: Install MySQL and phpmyadmin as docker containers

An Ansible role to install MySQl and phpmyadmin as docker containers.

See also [opichon.mysql-backup](https://github.com/opichon/ansible-mysql-backup) and [opichon.mysql-restore](https://github.com/opichon/ansible-mysql-restore)

## Requirements

This role requires Ansible 1.2 or higher.

It also requires the Docker engine to run on the target host.

This task assumes that the containers will be running in a bride network.

## Role variables

Ansible variables are listed below with their default values.

```
mysql_lib_dir: /var/lib/mysql
mysql_backups_dir: /var/backups/mysql
mysql_root_password
network
phpmyadmin_absolute_uri
phpmyadmin_host
```

## Example playbook

```
---
- hosts: servers
  roles:
  	- opichon.docker-mysql
```

## License

MIT

