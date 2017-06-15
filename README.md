# opichon.docker-mysql

An Ansible role to run a MySQL server as a docker container.

See also [opichon.mysql-backup](https://galaxy.ansible.com/opichon/mysql-backup/)

## Requirements

This role requires Ansible 1.2 or higher.

It also requires the Docker engine to run on the target host.

## Role variables

Ansible variables are listed below with their default values.

```
mysql_backups_dir: /var/mysql/backups
mysql_character_set: utf8mb4
mysql_collation: utf8mb4_unicode_520_ci
mysql_conf_dir: /var/mysql/conf.d
mysql_container_name: mysql
mysql_database
mysql_lib_dir: /var/mysql/lib
mysql_network: mysql
mysql_password
mysql_port: 3306
mysql_root_password
mysql_state: started
mysql_user
```

## Example playbook

```
---
- hosts: servers
  roles:
  	- opichon.docker-mysql
  	  mysql_database: mydb
  	  mysql_network: default
  	  mysql_password: secret
  	  mysql_root_password: very_secret
  	  mysql_user: me
```

## License

MIT

