# Workstation Configuration Files

This repository stores personal workstation configuration files, starting with shell setup for `zsh`.

## Repository Layout

```text
.
├── README.md
└── shell/
    └── .zshrc
```

## Included Configuration

### `shell/.zshrc`

The current Zsh configuration includes:

- `oh-my-zsh` with the `gianu` theme
- Plugins: `git`, `colorize`, `zsh-autosuggestions`, `zsh-syntax-highlighting`
- Custom `PATH` updates for `~/.local/bin`
- Vite+ environment loading from `~/.vite-plus/env`
- Shortcuts for source directories, Terraform, Kubernetes, and Docker

Custom aliases currently defined:

- `src` -> `<YOUR_SOURCE_CODE_DIRECTORY>`
- `tfi`, `tfp`, `tfa` -> Terraform workflow helpers
- `k`, `start-k8s`, `stop-k8s` -> Kubernetes and local cluster helpers
- `d`, `dps`, `dpa`, `di`, `drm`, `drmi`, `dlogs`, `dexec` -> Docker helpers

## Installation

Back up any existing shell config before replacing it:

```sh
cp ~/.zshrc ~/.zshrc.backup
cp shell/.zshrc ~/.zshrc
source ~/.zshrc
```

If you prefer to test it first without replacing your current file:

```sh
source shell/.zshrc
```

## Requirements

Some parts of this configuration assume the following tools or paths already exist:

- `oh-my-zsh` installed at `~/.oh-my-zsh`
- `zsh-autosuggestions` and `zsh-syntax-highlighting` available to `oh-my-zsh`
- `terraform`, `kubectl`, `docker`, and `minikube` installed if you use the related aliases
- `~/.vite-plus/env` present if you want the Vite+ environment to load cleanly

## Notes

- The alias paths are personal to this workstation and may need adjustment on another machine.
- This repo can be expanded over time with additional shell, editor, terminal, or tool configuration files.
