# mydotfiles

Personal dotfiles managed with [rigrc](https://github.com/roypriyanshu02/rigrc).

## Profiles

- `dev.conf` — Workstation and WSL setup
- `vps.conf` — Headless server setup

## Quick Start

```bash
git clone https://github.com/Lakshrp112/mydotfiles.git ~/.dotfiles-repo
cd ~/.dotfiles-repo

# Workstation (interactive)
./rigrc.sh --config=dev.conf

# Server (headless)
./rigrc.sh --config=vps.conf --non-interactive
```

## Maintenance

```bash
# Environment diagnostics and repair
./rigrc.sh --doctor --fix

# Clean broken symlinks
./rigrc.sh --clean-symlinks

# Validate configuration syntax
./rigrc.sh --lint

# Roll back changes
./rigrc.sh --rollback
```
