# dotfiles

Personal configuration for Ghostty, tmux, Neovim, and OpenCode.

## Install

Clone this repository, then link the configs into their standard locations:

```sh
git clone git@github.com:fristedt/dotfiles-2026.git ~/code/dotfiles-2026
cd ~/code/dotfiles-2026

mkdir -p ~/.config/ghostty ~/.config/nvim ~/.config/opencode
ln -sfn "$PWD/ghostty/config" ~/.config/ghostty/config
ln -sfn "$PWD/tmux/tmux.conf" ~/.tmux.conf
ln -sfn "$PWD/nvim" ~/.config/nvim
ln -sfn "$PWD/opencode/opencode.jsonc" ~/.config/opencode/opencode.jsonc
```

OpenCode's personal `opencode.json` may contain machine- or organization-specific provider settings; this repository includes only the general JSONC config.

The tmux config optionally invokes `~/.tmux/kube-tmux/kube.tmux` for its status bar. Install that script separately or remove that status-right setting if it is not available.

## Neovim

See [`nvim/README.md`](nvim/README.md) for requirements, first-run setup, and key bindings.
