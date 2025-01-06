ansible-role-podman
====

Manage podman.

Requirements
------------

* RHEL8+

Role Variables
--------------

* `podman_packages` - list of podman packages to install.
* `podman_git_repos` - list of git repos to fetch.
* `podman_images` - list images to pull.
* `podman_pods` - list of pods to manage.
* `podman_containers` - list of containers to manage.
* `podman_auto_update_systemd_units` - list of `podman-auto-update` systemd units.
* `podman_auto_update_enabled` - boolean to enable/disable systemd units from `podman_auto_update_systemd_units` variable.
* `podman_auto_update_state` - desired state of systemd units from `podman_auto_update_systemd_units` variable.

Dependencies
------------

Collections:

* `containers.podman` >= '1.16.1'

Example Playbook
----------------

```
- hosts: my_servers
  vars:
    podman_images:
      - name: docker.io/library/nginx
        tag: alpine
  roles:
    - ansible-role-podman
```

License
-------

GPLv3

Author Information
------------------

Vladimir Vasilev (@vladi-k)
