# Synthwave Neon Dark — macOS Terminal

A synthwave-inspired neon dark theme for macOS Terminal.app and [Starship](https://starship.rs) prompt.

Companion to [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) for Zed — same colors, same vibe.

![Synthwave Neon Dark Terminal](images/preview.png)

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

### Starship prompt

Merge the contents of [`starship.toml`](starship.toml) into your `~/.config/starship.toml`:

```sh
cat starship.toml >> ~/.config/starship.toml
```

Or copy individual sections you want. The Starship config uses ANSI color names that map to the terminal palette, plus hex values for colors without ANSI equivalents (purple, orange).

## Related

- [synthwave-theme](https://github.com/eneko-codes/synthwave-theme) — Synthwave Neon for Zed
