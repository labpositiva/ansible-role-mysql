# Ansible Role MySQL

[![Build Status](https://travis-ci.org/labpositiva/ansible-role-mysql.svg)](https://travis-ci.org/labpositiva/ansible-role-mysql)
[![GitHub issues](https://img.shields.io/github/issues/labpositiva/ansible-role-mysql.svg)](https://github.com/labpositiva/ansible-role-mysql/issues)
[![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat-square)](LICENSE)


Installs and configures [mysql][link-mysql] on a host.

## Requirements

 - Linux
   - none
 - OSX
   - [Homebrew][link-brew] must be installed.


## Role Variables

The default role variables in `defaults/main.yml` are:

    ---
    # defaults file for mysql
    mysql_user_home: /root
    mysql_root_username: root
    mysql_root_password: root
    mysql_port: "3306"
    mysql_bind_address: '0.0.0.0'
    mysql_slow_query_log_enabled: no
    mysql_databases:
      - name: example
        collation: utf8_general_ci
        encoding: utf8
    mysql_users:
      - name: example
        host: 127.0.0.1
        password: secret
        priv: *.*:USAGE


## Dependencies

none

## Example Playbook

See the [examples](./examples/) directory.

To run this playbook with default settings, create a basic playbook like this:

    - hosts: servers
      roles:
         - mysql

To install a specific version:

    - hosts: servers
      roles:
         - { role: labpositiva.mysql }


## Changelog

Please see [CHANGELOG](CHANGELOG.md) for more information what has changed recently.

## Contributing

Please see [CONTRIBUTING](CONTRIBUTING.md) for details.

## Credits

- [Luis Mayta][link-author]
- [All Contributors][link-contributors]

[link-mysql]: https://mysql.com/
[link-brew]: http://brew.sh/

<!-- Other -->

[link-author]: https://github.com/luismayta
[link-contributors]: AUTHORS
