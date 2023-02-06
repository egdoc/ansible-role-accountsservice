Ansible role: accountsservice
=========

Ansible role to configure AccountsService user entries.

Requirements
------------

None

Role Variables
--------------

```yaml
accountsservice_users: []
```

A list of dictionaries describing user entries. Available keys are:

- name (string): The name of the user
- icon (string): The URL or local path of the image to use as Avatar.
- language (string): The user language
- xsession (string): The default User Xsession (optional)
- system_user (bool): Whether the user is a system user or not (default is false).

```yaml
accountsservice_icons_dir: /var/lib/AccountsService/icons
accountsservice_users_dir: /var/lib/AccountsService/users
```

The directories where user icons and profiles are stored, respectively.


Dependencies
------------

None

Example Playbook
----------------

    - hosts: servers
      roles:
        - role: egdoc.accountsservice
          accountsservice_users:
            - name: vagrant
              language: en_US.UTF-8
              icon: https://example.com/user/picture.png
              system_user: false

License
-------

GPLv2

Author Information
------------------

Role created by Egidio Docile
