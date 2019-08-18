## Toying around with Gnome
My loose objective here is simply to get better touch guestures in kali.
It appears that we have touch screen support in gnome 3.14
https://help.gnome.org/misc/release-notes/3.14/touchscreen-gestures.html.en
And the version of gnome in kali is 3.30.2 at the time of writing

Please note this is just a journal, not a tech article. 

```bash
apt install gnome-shell-extension-onboard
apt install gnome-shell-extension-redshift
apt install gnome-shell-extension-taskbar
```

Post installation:
- after installing redshift, my nightlight feature is now gone. 
- the redshift extension does not seem to be enabled.
https://extensions.gnome.org/extension/685/redshift/

How can I find my installed extensions and enable them? Why does tweak tool not show these? 

gnome-shell-extension-tool doesn't seem to have a list feature. Only seems to have enable/disable/reload/ and create. 

## Commands for gnome shell extensions
```bash
# Local User Shell Extensions
ls ~/.local/share/gnome-shell/extensions/
# Global Shell Extensions
ls /usr/share/gnome-shell/extensions/
# Show Enabled Shell Extensions
gsettings get org.gnome.shell enabled-extensions
# Enable Shell extension
gnome-shell-extension-tool -e alternate-tab@gnome-shell-extensions.gcampax.github.com
# Disable Shell Extension
gnome-shell-extension-tool -d alternate-tab@gnome-shell-extensions.gcampax.github.com
```

## My Manual install of Extended Guestures
This is for touchpad, but it's a step in the right direction.
*Side note - This didn't seem to work really well. 
https://help.gnome.org/misc/release-notes/3.14/touchscreen-gestures.html.en

- Download the zip file appropriate for your version of gnome.
- extract zip file to ``/root/.local/share/gnome-shell/extensions/extendedgestures``
- copy the ``/root/.local/share/gnome-shell/extensions/extendedgestures/schemas/org.gnome.shell.extensions.extendedgestures.gschema.xml`` file to ``glib-compile-schemas /usr/share/glib-2.0/schemas/``
- run ``glib-compile-schemas /usr/share/glib-2.0/schemas/``
- run ``gnome-shell-extension-tool -e extendedgestures``

