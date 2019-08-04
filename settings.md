# Quick Configs
## Disable Auto Screen Lock (use ctrl alt L to lock)
```bash
gsettings set org.gnome.desktop.screensaver lock-enabled false
```

## Disable Weird Alt Tab / Alt ~ differentiation:
```bash
gnome-shell-extension-tool -e alternate-tab@gnome-shell-extensions.gcampax.github.com
```

## Enable Window List
```bash
gnome-shell-extension-tool -e window-list@gnome-shell-extensions.gcampax.github.com
```

## Set Clock to 12 Hour
```bash
gsettings set org.gnome.desktop.interface clock-format '12h'
```

## Set Themes
```bash
gsettings set org.gnome.desktop.interface gtk-theme 'Kali-X-Dark'
gsettings set org.gnome.desktop.wm.preferences theme 'Kali-X-Dark'

```

## Enumerate through various gsettings
```bash
gsettings list-schemas
gsettings list-keys org.gnome.desktop.screensaver
gsettings list-keys org.gnome.desktop.wm.keybindings
gsettings describe org.gnome.shell enabled-extensions

#Clock Settings
gsettings list-keys org.gnome.desktop.interface | grep clock
clock-show-seconds
clock-format
clock-show-weekday
clock-show-date

#Extensions
ls /usr/share/gnome-shell/extensions/

```
