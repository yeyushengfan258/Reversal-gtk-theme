## Reversal gtk theme

![Reversal](Reversal.png?raw=true)

## Requirements

- GTK `>=3.20`
- `gnome-themes-extra` (or `gnome-themes-standard`)
- Murrine engine — The package name depends on the distro.
  - `gtk-engine-murrine` on Arch Linux
  - `gtk-murrine-engine` on Fedora
  - `gtk2-engine-murrine` on openSUSE
  - `gtk2-engines-murrine` on Debian, Ubuntu, etc.
- `sassc` — build dependency

## Installation

### Manual Installation

Run the following commands in the terminal:

```sh
./install.sh
```

> Tip: `./install.sh` allows the following options:

```
-d, --dest DIR          Specify destination directory (Default: ~/.themes)
-n, --name NAME         Specify theme name (Default: Reversal)
-t, --theme VARIANT...  Specify theme color variant(s) [default|purple|pink|red|orange|yellow|green|teal|grey|all] (Default: blue)
-c, --color VARIANT...  Specify color variant(s) [standard|light|dark] (Default: All variants)
-s, --size VARIANT...   Specify size variant [standard|compact] (Default: standard variant)

-l, --libadwaita        Install specify gtk-4.0 theme into config folder ($HOME/.config/gtk-4.0) for all gtk4 apps use this theme
                        Default ColorSchemes theme will follow the system style (light/dark mode switch), all ColorSchemes versions not support this !
                        Options for default ColorSchemes:
                        1. system                      Default option (using system colors for light/dark mode switching)
                        2. fixed                       Using fixed theme colors (that will break light/dark mode switch)

--tweaks                Specify versions for tweaks
                        1. [nord|dracula|gruvbox|everforest|catppuccin|all]  (Nord/Dracula/Gruvbox/Everforet/Catppuccin/all) ColorSchemes version
                        2. black                       Blackness color version
                        3. rimless                     Remove the 1px border about windows and menus
                        4. normal                      Normal windows button style like gnome default theme (titlebuttons: max/min/close)
                        5. float                       Floating gnome-shell panel style

-r, --remove,
-u, --uninstall         Uninstall/Remove installed themes or links

-h, --help              Show help
```

> For more information, run: `./install.sh --help`

### Fix for Libadwaita

```sh
./install.sh -l
```

### Fix for Flatpak

```sh
sudo flatpak override --filesystem=xdg-config/gtk-3.0 && sudo flatpak override --filesystem=xdg-config/gtk-4.0
```

If you use flatpak apps, you can run this to fix theme issue

### Flatpak Installation (gtk-3.0)

Automatically install your host GTK+ theme as a Flatpak. Use this:

- [pakitheme](https://github.com/refi64/pakitheme)
