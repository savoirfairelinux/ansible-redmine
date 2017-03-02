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
    * [gitpush-deploy Ansible Role][ansible-gitpush-deploy]
    * [postgres-install][ansible-postgres-install]

Usage example
-------------

See [default variables](defaults/main.yml) for more variables.

```yaml
- role: redmine
  redmine_rails_environment: production
  redmine_database_password: SOMEPASSWORD
```

You will need to set a handler into your playbook in order to restart the application server when changes are made.

The handler name must be named `appserver reload` and you can replace `uwsgi` with your application server.

```
handlers:
  - name: appserver reload
    service:
      name: uwsgi
      state: reloaded
```

[ansible-gitpush-deploy]: https://github.com/savoirfairelinux/ansible-gitpush-deploy
[ansible-postgres-install]: https://github.com/savoirfairelinux/ansible-postgres-install
