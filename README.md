Role Name
=========

Installs and configures Gerrit Code Review...https://www.gerritcodereview.com/

Requirements
------------

None

Role Variables
--------------

````
---
# defaults file for ansible-gerrit
gerrit_account_info:
  - user: gerrit
    comment: Gerrit User
    home: '{{ gerrit_site_dir }}'
    group: gerrit
gerrit_db_info:
  - host: localhost
    type: h2
    db: db/ReviewDB
    user: gerrit
    pass: gerrit
gerrit_dl_info:
  - url: https://www.gerritcodereview.com/download
    filename: 'gerrit-{{ gerrit_version }}.war'
gerrit_install_plugins: []
gerrit_install_dir: /opt/gerrit
gerrit_service_name: gerrit
gerrit_site_dir: /var/gerrit
gerrit_smtp_server: 'smtp.{{ pri_domain_name }}'
gerrit_version: 2.11.4
pri_domain_name: example.org
````

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

Notes
-----
Portions of this role have been borrowed from https://github.com/kbrebanov/ansible-gerrit

License
-------

BSD

Author Information
------------------

Larry Smith Jr.
- @mrlesmithjr
- http://everythingshouldbevirtual.com
- mrlesmithjr [at] gmail.com
