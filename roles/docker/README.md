# Docker Role

This role provisions Docker on the system using the community-supported `geerlingguy.docker` Ansible role.

## What It Does

- Installs Docker CE (Community Edition).
- Ensures Docker Compose (v2) is available as a plugin (`docker compose`).
- Adds the current Ansible user to the `docker` group for non-root Docker access.

## Tasks

1. **Include geerlingguy.docker**
   - Handles all Docker installation, setup, and service management.
   - See: [geerlingguy/ansible-role-docker](https://github.com/geerlingguy/ansible-role-docker)

2. **Add user to docker group**
   - Grants Docker access without requiring `sudo`.

   ```yaml
   - name: Add user to docker group
     user:
       name: "{{ ansible_user }}"
       groups: docker
       append: yes
