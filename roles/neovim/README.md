# Neovim Role

This role installs a modern Neovim setup suitable for use with Kickstart and LazyVim.

## What It Does

- Uses the community `gikeymarcia.neovim` role to install Neovim from source.
  - Ensures LuaJIT is enabled and version is ≥ 0.9 (required for LazyVim).
- Clones my Neovim configuration from GitHub.

## Requirements

- The `gikeymarcia.neovim` role must be available (via Ansible Galaxy or requirements).
- Your system must have the necessary build tools. These are expected to be pre-installed via the `apt` role.

## Configuration

You can override these defaults in `defaults/main.yml`:

```yaml
neovim_config_repo: "https://github.com/MichaelSandilands/lazyvim.git"
neovim_config_path: "{{ ansible_user_dir }}/.config/nvim"
