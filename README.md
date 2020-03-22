Go (Ansible Role)
=================

Install multiple versions of Go onto a system using the upstream binaries.

Requirements
------------

None.

Role Variables
--------------

- go_architecture (string) = ``amd64`` (default), ``armv6l``, ``arm64``, ``ppc64le``, ``s390x``, or ``386``.
- go_operating_system (string) = ``darwin``, ``freebsd``, or ``linux`` (default). ``windows`` is not supported by this role.
- go_versions (list) = All Go versions that should be installed.

For more information about supported cominbations of architectures and operating systems, visit the [Go downloads page](https://golang.org/dl/).

Dependencies
------------

None.

Example Playbook
----------------

```
---
- hosts: app_servers
  roles:
    - name: ansible_role_go
      vars:
        go_architecture: 386
        go_operating_system: freebsd
        go_versions:
          - 1.12.17
          - 1.11.13
```

License
-------

Apache Software License 2.0 (ASLv2.0)
