# Ansible Role: PHP-XDebug

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-php-xdebug.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-php-xdebug)

Installs PHP [XDebug](http://xdebug.org/) on Linux servers.

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    workspace: /root

Where Xdebug setup files will be downloaded and built.

    php_xdebug_version: 2.2.4

The version of Xdebug to be installed (see [Xdebug docs](http://xdebug.org/docs/install) for a current listing).

    php_xdebug_module_path: /usr/lib64/php/modules

The path where `xdebug.so` will be installed.

    php_xdebug_remote_enable: "false"

Whether remote debugging is enabled.

    php_xdebug_remote_connect_back: "false"

If this is set to true, Xdebug will respond to any request from any IP address; use only for local development on non-public installations!

    php_xdebug_remote_host: localhost
    php_xdebug_remote_port: "9000"

The host and port on which Xdebug will listen.

    php_xdebug_remote_log: /tmp/xdebug.log

The location of the xdebug log (useful if you're having trouble connecting).

    php_xdebug_idekey: sublime.xdebug

The IDE key to use in the URL when making Xdebug requests (e.g. `http://example.local/?XDEBUG_SESSION_START=sublime.xdebug`).

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
