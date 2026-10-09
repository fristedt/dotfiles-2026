# Neovim setup

Small Neovim configuration for Kubernetes/YAML, Ansible, Go, and React/TypeScript. The editor uses GitHub Dark Default to match Ghostty, with a transparent background so Ghostty's terminal background carries through.

## Requirements

- Neovim 0.11 or newer
- Git
- `ripgrep` (`rg`) for Telescope live grep
- A C compiler for Treesitter parser installation

## First-time setup

The lazy.nvim bootstrap requires Git/network access once. Then, in Neovim, run:

```vim
:Lazy sync
:MasonInstall yaml-language-server ansible-language-server gopls typescript-language-server
:TSUpdate
```

These are explicit setup actions. The config disables plugin update checks, missing-plugin installs, Mason auto-install, Treesitter auto-install, and remote YAML schema-store access during normal startup. This keeps regular launches offline-friendly. Telescope live grep uses the local `rg` executable.

## Keys

| Key | Action |
| --- | --- |
| `<Space>e` | Toggle file tree |
| `<Space>ff` | Find files |
| `<Space>fg` | Live grep |
| `<Space>fb` | Find open buffers |
| `<Space>fh` | Search Neovim help |
| `gd` / `gr` / `K` | Definition / references / hover (when an LSP is attached) |
| `<Space>rn` / `<Space>ca` | Rename / code action |

YAML language-server support is configured without remote schemas. To add Kubernetes schema validation later, install/configure a schema source that is available locally on the remote host.
