# Obsidian Role

This role installs the [Obsidian](https://obsidian.md) note-taking application using its AppImage release from GitHub.

## What It Does

- Downloads the latest (or specific version) of the Obsidian AppImage.
- Installs it to a local user directory (by default: `~/.local/bin`).
- Makes the AppImage executable.
- Optionally runs the AppImage once to initialize configs (idempotently).

## Role Variables

Defined in `defaults/main.yml`:

```yaml
obsidian_version: latest              # or a version string like "1.5.8"
obsidian_appimage_dir: "{{ ansible_user_dir }}/.local/bin"
