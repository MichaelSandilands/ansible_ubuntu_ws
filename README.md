# Tuxedo OS Ansible Provisioning

This project provisions a fresh Tuxedo OS install with a personalized development environment using [Ansible](https://www.ansible.com/). It includes:

- Neovim (with Kickstart or LazyVim)
- Kitty terminal
- Docker + Compose
- Node.js + npm
- Nerd Fonts (JetBrainsMono)
- Lazygit
- Starship shell prompt
- R and tidyverse
- Obsidian (AppImage)
- And more...

## 🔧 One-Time Setup Instructions

From a **fresh Tuxedo OS installation**, run the following in a terminal:

```bash
# Update and upgrade system packages
sudo apt update && sudo apt upgrade -y

# Install Ansible
sudo apt install -y ansible

# Install Ansible Galaxy role dependencies
curl -L -o requirements.yml https://raw.githubusercontent.com/MichaelSandilands/ansible_ubuntu_ws/refs/heads/main/requirements.yml
ansible-galaxy install -r requirements.yml
rm requirements.yml

# Pull and run the provisioning playbook
ansible-pull -U https://github.com/MichaelSandilands/ansible_ubuntu_ws.git -K
