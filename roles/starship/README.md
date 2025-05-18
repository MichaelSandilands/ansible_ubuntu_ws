# Starship Role

This role installs the [Starship](https://starship.rs/) prompt using the `andrewrothstein.starship` Ansible Galaxy role and ensures it's initialized in the Bash shell.

## What It Does

- Installs the latest Starship binary into the user's path.
- Adds the Starship initialization command to `~/.bashrc` (if not already present).
- Uses a simple line-based modification to keep things idempotent and rerunnable.

## Dependencies

- The role `andrewrothstein.starship` must be installed (via `ansible-galaxy install andrewrothstein.starship`).

## Tasks Overview

```yaml
- name: Install Starship using andrewrothstein.starship
  include_role:
    name: andrewrothstein.starship

- name: Ensure Starship init line is in .bashrc
  ansible.builtin.lineinfile:
    path: "{{ ansible_user_dir }}/.bashrc"
    line: 'eval "$(starship init bash)"'
    insertafter: EOF
    state: present
