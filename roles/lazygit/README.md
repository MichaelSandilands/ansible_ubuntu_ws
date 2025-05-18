# Create README.md content for the lazygit role
lazygit_readme_content = """\
# Lazygit Role

This role installs the latest version of [Lazygit](https://github.com/jesseduffield/lazygit), a simple terminal UI for Git commands.

## Features

- Dynamically fetches the latest Lazygit version from GitHub.
- Skips installation if the correct version is already present.
- Downloads and installs the binary to a system-wide location.
- Cleans up temporary files after install.

## Variables

Defined in `defaults/main.yml`:

```yaml
lazygit_version: latest             # Uses GitHub API to resolve to latest version
lazygit_install_path: /usr/local/bin  # Path where the binary will be copied

