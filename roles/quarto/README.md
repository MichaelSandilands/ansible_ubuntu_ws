# Quarto Role

Installs the [Quarto](https://quarto.org) scientific and technical publishing system using the `Appsilon.quarto` role from Ansible Galaxy.

## Features

- Installs latest Quarto CLI
- Cross-platform and user-local
- Integrates well with both R and Python setups

## Dependencies

This role depends on:

```yaml
- name: Appsilon.quarto
```

## Example Playbook

```yaml
- hosts: localhost
  roles:
    - quarto
```