# Miniconda Role

This Ansible role installs [Miniconda](https://docs.conda.io/en/latest/miniconda.html) using the community role `andrewrothstein.miniconda`.

## Features

- Installs Miniconda 3 (Python 3.10) to `~/miniconda3`
- Adds Conda initialization to `.bashrc` using shell hook
- Fully user-local install (no sudo required)

## Dependencies

This role includes the `andrewrothstein.miniconda` role from Ansible Galaxy.

Ensure it's in your `requirements.yml`:

```yaml
- name: andrewrothstein.miniconda
```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - miniconda
```
