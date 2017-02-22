Ansible Redmine Role
====================

For Debian-based operating systems
----------------------------------

**Installs and globally configures Redmine in a secure way.**


Requirements
------------

* Ansible 2.0+
* PostgreSQL 9.5+
* One of these target systems:
    * Debian Jessie
    * Ubuntu 16.04
* [postgres-install Ansible Role][ansible-postgres-install]


Usage example
-------------

See [default variables](defaults/main.yml) for more variables.

```yaml
- role: redmine
  redmine_database_password: SOMEPASSWORD
```


[ansible-postgres-install]: https://github.com/savoirfairelinux/ansible-postgres-install
