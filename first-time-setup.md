# Arch Linux Hyprland setup guide

list of packages: 
```
sudo pacman -S polkit firefox keyd 
```
## Add macos keybindings using keyd
1. Install Keyd: `sudo pacman -S keyd`
2. create new file /etc/keyd/default.conf with the following contents
```
# NOTE: to use this, rename this file to default.conf and put in /etc/keyd/

# Mac-Like Configuration Example
#
# Uses "Alt" button to the left of spacebar as "Cmd" key
#
# Note:
#   This 'trick' generally requires that the press+release of the Meta
#   key will do nothing.

[ids]
*

[main]

# Create a new "Cmd" button, with various Mac OS-like features below
leftalt = layer(meta_mac)

# Swap meta/alt
leftmeta = alt


# meta_mac modifier layer; inherits from 'Ctrl' modifier layer
#
# The main part! Using this layer, we can remap our new "Cmd" key to
# do almost everything our muscle memory might need...
[meta_mac:C]

# Switch directly to an open tab (e.g. Firefox, VS code)
1 = A-1
2 = A-2
3 = A-3
4 = A-4
5 = A-5
6 = A-6
7 = A-7
8 = A-8
9 = A-9

# Copy
c = C-insert
# Paste
v = S-insert
# Cut
x = S-delete

# Move cursor to beginning of line
left = home
# Move cursor to end of Line
right = end
```
3. Enable keyd `sudo systemctl enable keyd --now`

## Dual booting
todo

## Hyprland config
1. copy hyprland.conf to ~/.config/hypr/hyprland.conf

## Electron / Discord
update configuration to make it work with
