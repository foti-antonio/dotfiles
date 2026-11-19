# dotfiles

Minimal mangowm setup (scroller layout, light animations), waybar, mako, foot, rofi.
Font: JetBrainsMono Nerd Font (`ttf-jetbrains-mono-nerd`).

Packages: `mangowm waybar mako foot rofi swaybg grim slurp wl-clipboard ttf-jetbrains-mono-nerd`

Install: copy `.config/*` to `~/.config/`.

## What is where

Every setting is explained by a comment right above it in the file itself.

| File | Program | What it controls |
| --- | --- | --- |
| `.config/mango/config.conf` | mangowm (compositor) | Monitor, autostart, look, animations, layout, input, all key and mouse bindings |
| `.config/waybar/config.jsonc` | waybar (status bar) | Which modules the bar shows and what they print |
| `.config/waybar/style.css` | waybar | Fonts, colours and spacing of the bar |
| `.config/mako/config` | mako (notifications) | Position, colours and timeout of notification popups |
| `.config/foot/foot.ini` | foot (terminal) | Terminal font |
| `.config/rofi/config.rasi` | rofi (launcher) | Launcher behaviour and look |

Colours are gruvbox dark in all of them.

## Keys

`SUPER` is the Windows key. Direction keys are `h` `j` `k` `l` or the arrows.

| Keys | Action |
| --- | --- |
| `SUPER` + `Return` | Terminal (foot) |
| `SUPER` + `d` or `space` | App launcher (rofi) |
| `SUPER` + `SHIFT` + `Return` | Firefox |
| `SUPER` + `SHIFT` + `n` | File manager (nautilus) |
| `SUPER` + `w` | Close window |
| `SUPER` + direction | Focus the window in that direction |
| `SUPER` + `SHIFT` + direction | Swap the window with its neighbour |
| `SUPER` + `f` | Fullscreen on/off |
| `SUPER` + `SHIFT` + `space` | Floating on/off |
| `SUPER` + `r` | Cycle window width: 50% → 80% → 100% |
| `SUPER` + `SHIFT` + `f` | Window width 100% |
| `SUPER` + `Tab` | Overview of all windows |
| `SUPER` + `1`…`9` | Go to tag 1…9 |
| `SUPER` + `SHIFT` + `1`…`9` | Send window to tag 1…9 |
| `SUPER` + scroll wheel | Previous/next tag that has windows |
| `SUPER` + left-drag / right-drag | Move / resize window |
| Volume keys | Volume ±5%, mute, mic mute |
| `Print` | Screenshot of a region to the clipboard |
| `SHIFT` + `Print` | Screenshot of the screen to `~/Pictures/Screenshots/` (create the folder first) |
| `SUPER` + `SHIFT` + `r` | Reload mango config |
| `SUPER` + `SHIFT` + `e` | Exit mango |

## Applying changes

| Program | How |
| --- | --- |
| mango | `SUPER` + `SHIFT` + `r`; check for errors with `mango -c ~/.config/mango/config.conf -p` |
| waybar | `pkill waybar; waybar &` |
| mako | `makoctl reload` |
| foot, rofi | Open a new one |
