# Synthwave Neon Dark — macOS Terminal

A synthwave-inspired neon dark theme for macOS Terminal.app and [Starship](https://starship.rs) prompt.

Companion to [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) for Zed — same colors, same vibe.

![Synthwave Neon Dark Terminal](images/terminal.png)

## Features

- Minimal neon prompt: purple (directory), cyan (git), gray (context), red (errors)
- Default Starship git status indicators with cyan accent
- Git state detection (REBASING, MERGING, CHERRY-PICKING)
- 30+ language/runtime/framework modules with auto-detection
- Python virtualenv display, cloud provider context (AWS, GCP), sudo/SSH warnings
- 16 ANSI colors tuned for synthwave aesthetic
- 95% background opacity with full blur (frosted glass)
- JetBrains Mono Nerd Font for monospace rendering
- 1.1x line height for comfortable reading
- Git identity greeting on terminal open
- zsh-autosuggestions and syntax highlighting support

## Prompt colors

| Element | Color | Hex |
|---------|-------|-----|
| Directory | Purple | `#e08fff` |
| Git branch & status | Cyan | `#00fff5` |
| Right-side context | Gray | `#9595a8` |
| Errors & sudo | Red | `#ff4466` |
| Default text | Lavender white | `#eee9f5` |

## ANSI colors

| Color   | Normal    | Bright    |
|---------|-----------|-----------|
| Black   | `#262040` | `#6a6490` |
| Red     | `#ff4466` | `#ff7888` |
| Green   | `#5cffaa` | `#90ffc0` |
| Yellow  | `#ffd580` | `#ffe8a0` |
| Blue    | `#c89fff` | `#ddb4ff` |
| Magenta | `#ff6eb4` | `#ff9ed0` |
| Cyan    | `#00fff5` | `#70fffa` |
| White   | `#eee9f5` | `#ffffff` |

**Background:** `#14101f` (95% opacity) · **Foreground:** `#eee9f5` · **Cursor:** `#b49fd0`

## Install

### 1. Install JetBrains Mono Nerd Font

The terminal profile and Starship prompt require [JetBrains Mono Nerd Font](https://www.nerdfonts.com/font-downloads) for prompt icons and dev symbols.

```sh
brew install --cask font-jetbrains-mono-nerd-font
```

Or download manually from [nerdfonts.com](https://www.nerdfonts.com/font-downloads) and install the `.ttf` files.

### 2. Terminal.app

1. Download [`Synthwave-Neon-Dark.terminal`](Synthwave-Neon-Dark.terminal)
2. Double-click the file to import it
3. Open **Terminal > Settings > Profiles**
4. Select **Synthwave Neon Dark** and click **Default**

The profile includes JetBrains Mono Nerd Font 13pt, 95% opacity with full blur (frosted glass), and 1.1x line height. You can adjust these in Terminal > Settings > Profiles > Window/Text.

### 3. Starship prompt

The Starship config creates a neon-colored prompt with git info on the left and language/framework versions on the right.

Copy [`starship.toml`](starship.toml) to your Starship config:

```sh
cp starship.toml ~/.config/starship.toml
```

The config uses a named palette, so you can tweak all colors from one place:

```toml
[palettes.synthwave]
purple = "#e08fff"
cyan = "#00fff5"
red = "#ff4466"
gray = "#9595a8"
fg = "#eee9f5"
```

### Shell extras (optional)

Add these to your `~/.zshrc` for a git identity greeting and zsh plugins:

```sh
# Git identity greeting (once per terminal)
_name=$(git config --global user.name 2>/dev/null)
_email=$(git config --global user.email 2>/dev/null)
[[ -n "$_name" ]] && printf '\e[38;2;238;233;245m\uf09b %s <%s>\e[0m\n' "$_name" "$_email"
unset _name _email

# zsh plugins (install: brew install zsh-autosuggestions zsh-syntax-highlighting)
source /opt/homebrew/share/zsh-autosuggestions/zsh-autosuggestions.zsh
source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

## Related

- [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) — Synthwave Neon for Zed
