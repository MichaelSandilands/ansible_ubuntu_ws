FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt update && apt install -y \
    curl git unzip build-essential \
    neovim python3 python3-pip \
    nodejs npm \
    lua5.1 liblua5.1-0-dev luajit \
    ripgrep fzf lazygit tree-sitter-cli \
    xclip && \
    apt clean

# Optional: Create a non-root user (e.g., dev)
RUN useradd -ms /bin/bash dev
USER dev
WORKDIR /home/dev

# Install Neovim config (Kickstart)
RUN git clone https://github.com/MichaelSandilands/kickstart.nvim.git ~/.config/nvim

CMD [ "nvim" ]
