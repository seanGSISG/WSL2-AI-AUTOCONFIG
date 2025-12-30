# WSL2-AI-AUTOCONFIG

Streamlined WSL2 development environment with AI coding agents.

A stripped-down fork of [agentic_coding_flywheel_setup](https://github.com/Dicklesworthstone/agentic_coding_flywheel_setup) optimized for WSL2.

## Quick Install

```bash
curl -fsSL "https://raw.githubusercontent.com/seanGSISG/WSL2-AI-AUTOCONFIG/main/install.sh" | sudo bash -s -- --yes --mode vibe
```

## What's Installed

### Shell Environment
- zsh + Oh My Zsh + Powerlevel10k theme
- zsh-autosuggestions + zsh-syntax-highlighting
- Modern CLI tools: lsd/eza, bat, fd, ripgrep, fzf, tmux

### Language Runtimes
- **Bun** - Fast JS runtime for tooling
- **uv** - Python package manager
- **Rust** - Nightly + cargo
- **Go** - Go toolchain
- **Node.js** - via nvm

### AI Coding Agents
- **Claude Code** (`ccd` alias) - Anthropic
- **Codex CLI** (`cod` alias) - OpenAI
- **Gemini CLI** (`gmi` alias) - Google

## Aliases

| Alias | Command | Description |
|-------|---------|-------------|
| `ccd` | Claude Code | Dangerous mode with extra memory |
| `cod` | Codex CLI | Bypass approvals and sandbox |
| `gmi` | Gemini CLI | YOLO mode |
| `ls` | lsd --color=always | Colorized file listing |

## After Installation

```bash
# Source the new shell config
source ~/.zshrc

# Check system health
wsl2aiac doctor

# Login to agents
claude auth login
codex login
gemini

# Start coding!
ccd "Hello! Let's build something."
```

## What's Different from ACFS

| Removed | Reason |
|---------|--------|
| Cloud Tools (Vault, PostgreSQL, Wrangler, Supabase, Vercel) | Focus on local dev |
| ACFS Stack Tools (NTM, MCP Agent Mail, UBS, etc.) | Reduced complexity |
| VPS/SSH features (Tailscale, SSH key handling) | WSL2 doesn't need them |
| Web UI | CLI-focused workflow |

| Changed | From | To |
|---------|------|-----|
| Claude alias | `cc` | `ccd` |
| `ls` output | Verbose (permissions, dates) | Minimal (names, icons, colors) |

## Directory Structure

```
~/.wsl2aiac/           # Config home
  └── zsh/
      ├── wsl2aiac.zshrc
      └── p10k.zsh
/data/projects/        # Workspace root
```

## License

MIT - See upstream repository for details.
