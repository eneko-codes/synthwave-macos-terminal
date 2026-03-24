# Synthwave Neon Dark — macOS Terminal

A synthwave-inspired neon dark theme for macOS Terminal.app and [Starship](https://starship.rs) prompt.

Companion to [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) for Zed — same colors, same vibe.

![Synthwave Neon Dark Terminal](images/terminal.png)

## Features

- 16 ANSI colors matched to the Zed synthwave theme
- 90% background opacity with 50% blur (frosted glass)
- 1.1x line height for comfortable reading
- Starship prompt with named synthwave color palette

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

### Terminal.app

1. Download [`Synthwave-Neon-Dark.terminal`](Synthwave-Neon-Dark.terminal)
2. Double-click the file to import it
3. Open **Terminal > Settings > Profiles**
4. Select **Synthwave Neon Dark** and click **Default**

The profile includes 90% opacity with 50% blur and 1.1x line height spacing. You can adjust these in Terminal > Settings > Profiles > Window/Text.

### Starship prompt

The Starship config defines a `synthwave` palette with named colors and applies them to prompt modules. Requires a [Nerd Font](https://www.nerdfonts.com/) for the icons.

Merge the contents of [`starship.toml`](starship.toml) into your `~/.config/starship.toml`:

```sh
cat starship.toml >> ~/.config/starship.toml
```

Or copy individual sections. The config uses a named palette, so you can tweak all colors from one place:

```toml
[palettes.synthwave]
pink = "#ff2d95"
cyan = "#00fff5"
purple = "#c96eff"
yellow = "#fffe6e"
orange = "#ff9e64"
green = "#5cffaa"
blue = "#88aaff"
red = "#ff4055"
fg = "#e2d9f3"
muted = "#6e6890"
```

### Shell colors (optional)

Add these to your `~/.zshrc` for colorized `ls`, `grep`, and `man` pages:

```sh
export CLICOLOR=1
export LSCOLORS="GxFxCxDxBxegedabagaced"
alias grep='grep --color=auto'

export LESS_TERMCAP_mb=$'\e[1;35m'
export LESS_TERMCAP_md=$'\e[1;36m'
export LESS_TERMCAP_me=$'\e[0m'
export LESS_TERMCAP_so=$'\e[1;33m'
export LESS_TERMCAP_se=$'\e[0m'
export LESS_TERMCAP_us=$'\e[1;32m'
export LESS_TERMCAP_ue=$'\e[0m'
```

## Related

- [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) — Synthwave Neon for Zed
