---
{"dg-publish":true,"permalink":"/kynzo-s-wonderful-gnome-settings/","created":"2026-03-02T02:20:16.217+01:00","updated":"2026-03-02T20:34:35.366+01:00"}
---

This mainly serves as a reference for when I switch to NixOS (I am currently on Fedora) because I will probably forget all the little settings and plugins that I make to my Fedora setup. And it will be nice to have them here so I don't have to find them all again when i make the switch.
Regardless I'll probably publish it cus why not :D
# Plugins
- appindicator - to add the tray with apps running in the bg
# Settings
## Keybinds
- Launch Terminal: Super + Enter
- Resize windows with right click: resize-with-right-button = true
## Terminal config
Alacritty:
```toml
[window]
padding = { x = 10, y = 10 }

[font.normal]
family = "FiraCode Nerd Font"

[terminal.shell]
program = "/usr/bin/fish"
```
Fish:
```
starship init fish | source
```
copyous:
- Vertical Position: Bottom
- Auto Hide Search: false
- Show Item Title: false
- Header Controls Visibility: Visible on Hover
- Items:
	- Text Item: Show Text Info: Words
	- Code Item: Show Code Info: Lines
	- File Item: File Preview Visibility: File Preview and File Info
	- Character Item: Show Unicode: true
- Shortcuts:
	- Open Clipboard Dialog: Super + V

# Apps
- Terminal: Alacritty
- tui text editor: Fresh?
- Gnome styled clipboard manager: copyous