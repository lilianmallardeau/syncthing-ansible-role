Syncthing Ansible role
======================

An Ansible role to install Syncthing and enable the systemd service. Works on Debian-based distributions.

Requirements
------------

None

Role Variables
--------------

- `syncthing_enable_service`: boolean, default `yes`  
Enable or disable the syncthing systemd service for user `syncthing_user`

- `syncthing_user`: default empty  
User to run the systemd service as. The service will not be enabled if no user is specified, even if `syncthing_enable_service` is set to `true`.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: syncthing
      vars:
        syncthing_user: syncguy
        syncthing_enable_service: yes
```

License
-------

MIT
