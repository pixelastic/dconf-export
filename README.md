dconf-export
============
Export your dconf settings in an editable `.sh` file.

Usage
-----
    dconf-export org.gnome.desktop.wm.keybindings

Use it to make a backup of your dconf settings or if you'd rather edit them
manually than in a GUI.

Example
-------

Previous example will create and executable file
`org.gnome.desktop.wm.keybindings.sh` with following content :

```Shell
#!/usr/bin/env sh
gsettings set org.gnome.desktop.wm.keybindings close "['<Alt>F4']"
gsettings set org.gnome.desktop.wm.keybindings maximize "['<Super>Up']"
gsettings set org.gnome.desktop.wm.keybindings minimize "['<Primary><Super>Down']"
# [...]
gsettings set org.gnome.desktop.wm.keybindings show-desktop "['<Super>D']"
gsettings set org.gnome.desktop.wm.keybindings switch-applications "['<Alt>Tab']"
gsettings set org.gnome.desktop.wm.keybindings switch-applications-backward "['<Alt><Shift>Tab']"
# [...]
```


Limitations
-----------

`dconf-export` needs ruby to run. It will also not work on relocatable schemas.

Alternatives
------------

* dconf has its own mechanism to dump the configuration with the command `dconf dump /`.
