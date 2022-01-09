ansible-role-podman
====

Manage podman.

Requirements
------------

* RHEL8+

Role Variables
--------------

* `podman_git_repos` - list of git repos to fetch.
* `podman_images` - list images to pull.
* `podman_pods` - list of pods to manage.
* `podman_containers` - list of containers to manage.

Dependencies
------------

Collections:

* `containers.podman`

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
