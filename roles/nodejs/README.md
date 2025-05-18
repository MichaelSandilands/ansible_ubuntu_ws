# Node.js Role

This role installs Node.js using the well-known [geerlingguy.nodejs](https://github.com/geerlingguy/ansible-role-nodejs) Ansible role.

## What It Does

- Installs Node.js version 18.x via the NodeSource repository.
- Automatically includes `npm`, the Node.js package manager.
- Ensures compatibility for frontend tools, LSP servers, and Neovim plugins that rely on Node.js.

## Role Variables

Defined inline in `tasks/main.yml`:

```yaml
nodejs_version: "18.x"
