# Nerd Font Role

This role installs JetBrainsMono Nerd Font using the [hurricanehrndz.nerdfonts](https://github.com/hurricanehrndz/ansible-nerdfonts) Ansible role.

## What It Does

- Downloads and installs the **JetBrainsMono** font patched with Nerd Font glyphs.
- Uses `nerdfonts_mono: yes` to install the monospaced variant—ideal for development and terminal usage.

## Dependencies

- Relies on the `hurricanehrndz.nerdfonts` role, which must be available via Ansible Galaxy.

## Role Variables

Defined inline in `tasks/main.yml`:

```yaml
nerdfonts_font:
  - fontname: 'JetBrainsMono'

nerdfonts_mono: yes
