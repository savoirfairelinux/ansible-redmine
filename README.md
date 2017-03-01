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
* Ansible roles:
    * [postgres-install][ansible-postgres-install]
    * [uwsgi-nginx][ansible-uwsgi-nginx]


Usage example
-------------

See [default variables](defaults/main.yml) for more variables.

```yaml
- role: redmine
  redmine_username: redmine
  redmine_database_password: SOMEPASSWORD
```


[ansible-postgres-install]: https://github.com/savoirfairelinux/ansible-postgres-install
[ansible-uwsgi-nginx]: https://github.com/savoirfairelinux/ansible-uwsgi-nginx
