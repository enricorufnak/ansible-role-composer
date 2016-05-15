[![Build Status](https://travis-ci.org/enricorufnak/ansible-role-composer.svg?branch=master)](https://travis-ci.org/enricorufnak/ansible-role-composer)

Ansible Role: Composer
=========

Installs Composer, the PHP Dependency Manager, on any Linux system.

Requirements
------------

- `php` (version 5.4+) should be installed and working (you can use the `geerlingguy.php` role to install).
- `git` should be installed and working (you can use the `geerlingguy.git` role to install).

Role Variables
--------------

The path where composer will be installed and available to your system:

    composer_path: /usr/local/bin/composer

Set this to false to disable Composer update to the latest release every time the playbook is run:

    composer_update: true

Days ago when Composer has to be updated:

    composer_update_day: 30

Dependencies
------------

Make sure you've installed PHP.

Example Playbook
----------------

After the playbook runs, `composer` will be placed in `/usr/local/bin/composer`, and will be accessible via normal system accounts.

    - hosts: servers
      roles:
         - { role: enricorufnak.composer }

License
-------

MIT / BSD

Author Information
------------------

This role was created in 2016 by [Enrico Rufnak](http://www.rufnak.de)
