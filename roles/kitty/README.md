# Kitty Role

This role installs and configures the [Kitty terminal emulator](https://sw.kovidgoyal.net/kitty/) locally for the current user. It ensures the terminal is up-to-date, properly linked, and integrated into the desktop environment.

## What It Does

- Downloads and installs the latest Kitty build using the official install script.
- Symlinks `kitty` and `kitten` binaries to `~/.local/bin`.
- Installs desktop `.desktop` launchers locally.
- Updates `.desktop` entries to use local icons and executables.
- Sets Kitty as the preferred terminal using `xdg-terminal-exec`.

## Why Local Install?

Kitty is not always available in the system package manager with the latest version. Installing locally ensures:
- The most recent features and fixes.
- No need for root or `apt`.

## Files and Configuration

- **Kitty install path**: `~/.local/kitty.app`
- **Binaries linked to**: `~/.local/bin/kitty` and `kitten`
- **Desktop entries**: `~/.local/share/applications/kitty.desktop`
- **Terminal preference**: `~/.config/xdg-terminals.list`

## Notes

- The installation is performed on every run unless the Kitty app directory exists.
- You can modify this behavior using the `creates:` directive or by checking versions manually.
