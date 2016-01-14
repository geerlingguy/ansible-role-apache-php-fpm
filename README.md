# Ansible Role: Apache FastCGI PHP

[![Build Status](https://travis-ci.org/geerlingguy/ansible-role-apache-fastcgi-php.svg?branch=master)](https://travis-ci.org/geerlingguy/ansible-role-apache-fastcgi-php)

An Ansible Role that configures FastCGI for PHP-FPM usage with Apache on RHEL/CentOS and Debian/Ubuntu.

## Requirements

This role is dependent upon `geerlingguy.apache`, and also requires you have PHP running with PHP-FPM somewhere on the server or elsewhere (I usually configure PHP with the `geerlingguy.php` role).

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    apache_enablerepo: ""

The repository to use when installing Apache dependencies (only used on RHEL/CentOS systems). If you'd like later versions of Apache than are available in the OS's core repositories, use a repository like EPEL (which can be installed with the `geerlingguy.repo-epel` role).

TODO.

## Dependencies

None.

## Example Playbook

    - hosts: webservers
      roles:
        - { role: geerlingguy.apache }
        - { role: geerlingguy.php }
        - { role: geerlingguy.apache-fastcgi-php }

## License

MIT / BSD

## Author Information

This role was created in 2016 by [Jeff Geerling](http://jeffgeerling.com/), author of [Ansible for DevOps](http://www.ansiblefordevops.com/).
