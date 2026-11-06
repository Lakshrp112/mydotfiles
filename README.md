# mydotfiles

Personal dotfiles managed with [rigrc](https://github.com/roypriyanshu02/rigrc).

## Profiles

- `dev.conf` — Workstation and WSL setup
- `dev-server.conf` — Headless server setup

## Quick Start

### 1. WSL Prerequisites (Windows only)

If running in WSL2, copy `.wslconfig` to your Windows user directory to enable mirrored networking:

```powershell
# Run in PowerShell on Windows:
Copy-Item .wslconfig "$env:USERPROFILE\.wslconfig" -Force
wsl --shutdown
```

Or from inside your WSL terminal:
```bash
cp .wslconfig "$(wslpath "$USERPROFILE")/.wslconfig"
```

### 2. Run Setup

```bash
git clone https://github.com/Lakshrp112/mydotfiles.git ~/.dotfiles-repo
cd ~/.dotfiles-repo

# Workstation (interactive)
./rigrc.sh --config=dev.conf

# Server (headless)
./rigrc.sh --config=dev-server.conf --non-interactive
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
