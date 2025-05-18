# R Role

This role installs the R programming language from the official CRAN repository on Debian/Ubuntu systems.

## What It Does

- Updates the APT package index.
- Installs required helper packages: `software-properties-common` and `dirmngr`.
- Adds the CRAN signing key and repository using the appropriate Ubuntu codename.
- Installs `r-base` using `--no-install-recommends` for a minimal footprint.

## Requirements

- The system must be Debian-based (uses `apt` and `apt_repository`).
- You must run this role with `become: true`.

## Role Variables

None needed. The Ubuntu codename is detected automatically via `ansible_lsb.codename`.

## Example Usage

```yaml
- hosts: localhost
  become: true
  roles:
    - r
