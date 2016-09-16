# mariadb

This Ansible Role is meant to install mariadb and put basic configuration in
place. It is only meant to be used at an Ubuntu 16-04 box. Also, extra configuration and databases should be put in separately.


## Requirements

None

## Role Variables

### Character Set and Collation

Three variables are used for __character set__ and __collation__. Those set with these variables will provide with the default values used by mariadb when it is starting up. You may create databases with other values if You like, but the values You set for these would be the defaults.

- __mariadb_default_character_set__ sets the default character set for the client
- __mariadb_character_set_server__ sets the default character set for the server
- __mariadb_collation_server__ sets the default collation at the server

If You need more knowledge about character sets and collation in mariadb, I recommend You check out the following resources at the mariadb site:

- [Character Set and Collation Overview](https://mariadb.com/kb/en/mariadb/character-set-and-collation-overview/
)
- [Supported Character Sets and Collations](https://mariadb.com/kb/en/mariadb/supported-character-sets-and-collations/)
- [Collation](https://mariadb.com/kb/en/sql-99/22-sql-collations-collation/)



Dependencies
------------

None

Example Playbook
----------------

The easiest way to tweak the variables is to copy and paste the ones You would
like to change from the __defaults/main.yml__ file. Put them in a __config.yml__
file and use it from within Your playbook.

    ---
    - hosts: your-host
      become: True

      vars_files:
        - config.yml

      roles:
        - gubjoa.mariadb


License
-------

GPLv2
