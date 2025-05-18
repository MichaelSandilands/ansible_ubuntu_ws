# APT Role

This role installs system dependencies using `apt` that are required for setting up a Tuxedo OS with Neovim (Kickstart and LazyVim), development tools, and terminal utilities.

## Installed Packages

- build-essential
- curl
- fd-find
- fonts-noto-color-emoji
- fzf
- git
- imagemagick
- libmagickwand-dev
- lua5.1
- liblua5.1-0-dev
- luajit
- make
- ripgrep
- tree-sitter-cli
- tmux
- unzip
- xclip

## Why These Packages?

### Kickstart Neovim Requirements:
[kickstart.nvim](https://github.com/nvim-lua/kickstart.nvim)
- **git, make, unzip, gcc**: Basic build and version control tools.
- **ripgrep, fd-find**: Required for fast file and text search within Neovim.
- **xclip**: Clipboard integration for Linux.
- **fonts-noto-color-emoji**: Emoji support (Ubuntu only).

### LazyVim Requirements:
[lazvim](https://www.lazyvim.org/)
- **curl**: Required by plugins like `blink.cmp`.
- **fzf, ripgrep, fd**: Used by `fzf-lua` plugin.
- **luajit, gcc, make**: For compiling Neovim with LuaJIT and supporting `nvim-treesitter`.

### Optional/Additional:
- **imagemagick, libmagickwand-dev**: Useful for image processing tools.
- **tmux**: Terminal multiplexer often used alongside Neovim.
- **tree-sitter-cli**: Treesitter parsing support.

## Note
- Additional tools like Neovim, Kitty, Node.js, Nerd Fonts, and Lazygit are provisioned using their own roles, as they are not fully managed via apt.

