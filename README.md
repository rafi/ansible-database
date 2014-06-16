### Ansible Database ware

Ansible roles for installing and setting up different database ware
on Debian/Ubuntu and Archlinux.

### Install
Add this repo as a submodule in your `roles/` folder and include it in
a playbook of yours.

### Config example
```yaml
---
postgresql:
  version: 9.3
  user: postgres
  group: postgres
  config:
    timezone: UTC
    shared_buffers: 24MB
    work_mem: 1MB

    checkpoint_segments: 3
    checkpoint_completion_target: 0.5

    effective_cache_size: 128MB
  users:
    - name: john
      role: SUPERUSER
    - name: bob
```

### License
MIT
