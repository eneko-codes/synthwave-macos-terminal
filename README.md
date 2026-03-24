# Synthwave Neon Dark — macOS Terminal

A synthwave-inspired neon dark theme for macOS Terminal.app and [Starship](https://starship.rs) prompt.

Companion to [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) for Zed — same colors, same vibe.

![Synthwave Neon Dark Terminal](images/terminal.png)

## Features

- 16 ANSI colors matched to the Zed synthwave theme
- Purple powerline pill-shaped prompt with rounded edges
- 95% background opacity with full blur (frosted glass)
- JetBrains Mono Nerd Font for powerline glyphs and dev icons
- 1.1x line height for comfortable reading
- Starship prompt with named synthwave color palette
- Auto-detected language/framework icons (Node.js, Python, Rust, Go, Java, Ruby, Swift, and more)
- Git identity greeting on terminal open
- zsh-autosuggestions and syntax highlighting support

## Colors

| Color   | Normal    | Bright    |
|---------|-----------|-----------|
| Black   | `#3a3558` | `#6a6490` |
| Red     | `#ff4055` | `#ff7888` |
| Green   | `#5cffaa` | `#90ffc0` |
| Yellow  | `#fffe6e` | `#ffffaa` |
| Blue    | `#88aaff` | `#aaccff` |
| Magenta | `#ff2d95` | `#ff70be` |
| Cyan    | `#00fff5` | `#70fffa` |
| White   | `#e2d9f3` | `#ffffff` |

**Background:** `#1c182c` · **Foreground:** `#e2d9f3` · **Cursor:** `#c96eff` · **Selection:** `#3a3558`

## Install

### 1. Install JetBrains Mono Nerd Font

The terminal profile and Starship prompt require [JetBrains Mono Nerd Font](https://www.nerdfonts.com/font-downloads) for powerline arrows and dev icons.

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

The Starship config creates a purple powerline prompt with pill-shaped edges, git branch info, and right-aligned language/framework versions.

Copy [`starship.toml`](starship.toml) to your Starship config:

```sh
cp starship.toml ~/.config/starship.toml
```

The config uses a named palette, so you can tweak all colors from one place:

```toml
[palettes.synthwave]
pink = "#ff2d95"
cyan = "#00fff5"
purple = "#e48fff"
purple_dark = "#382a58"
purple_mid = "#4d3b70"
yellow = "#fffe6e"
orange = "#ff9e64"
green = "#5cffaa"
blue = "#88aaff"
red = "#ff4055"
fg = "#e2d9f3"
bg = "#14101f"
muted = "#5e5575"
```

### Shell extras (optional)

Add these to your `~/.zshrc` for a git identity greeting, colorized tools, and zsh plugins:

```sh
# Git identity greeting (once per terminal)
_name=$(git config --global user.name 2>/dev/null)
_email=$(git config --global user.email 2>/dev/null)
[[ -n "$_name" ]] && printf '\e[38;2;242;232;248m\uf09b %s <%s>\e[0m\n' "$_name" "$_email"
unset _name _email

# Colors for BSD tools (ls, grep)
export CLICOLOR=1
export LSCOLORS="GxFxCxDxBxegedabagaced"
alias grep='grep --color=auto'

# Colorized man pages
export LESS_TERMCAP_mb=$'\e[1;35m'
export LESS_TERMCAP_md=$'\e[1;36m'
export LESS_TERMCAP_me=$'\e[0m'
export LESS_TERMCAP_so=$'\e[1;33m'
export LESS_TERMCAP_se=$'\e[0m'
export LESS_TERMCAP_us=$'\e[1;32m'
export LESS_TERMCAP_ue=$'\e[0m'

# zsh plugins (install: brew install zsh-autosuggestions zsh-syntax-highlighting)
source /opt/homebrew/share/zsh-autosuggestions/zsh-autosuggestions.zsh
source /opt/homebrew/share/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

## Related

- [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) — Synthwave Neon for Zed
