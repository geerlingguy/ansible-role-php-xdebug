# Ansible Role: PHP-XDebug

Installs PHP [XDebug](http://xdebug.org/) on Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `vars/main.yml`):

    workspace: /root

Where Xdebug setup files will be downloaded and built.

    php_xdebug_version: 2.2.4

The version of Xdebug to be installed (see [Xdebug docs](http://xdebug.org/docs/install) for a current listing).

    php_xdebug_module_path: /usr/lib64/php/modules

The path where `xdebug.so` will be installed.

    php_xdebug_remote_host: localhost
    php_xdebug_remote_port: "9000"

The host and port on which Xdebug will listen.

## Dependencies

  - geerlingguy.php

## Example Playbook

    - hosts: webservers
      roles:
        - { role: geerlingguy.php-xdebug }

## License

MIT / BSD

## Author Information

This role was created in 2014 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://ansiblefordevops.com/).
