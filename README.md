# dotfiles
Ensemble de fichiers de configuration pour desktop Gruvbox Themes/icons/cursors/ULauncher/Grub.
Tous ces fichiers sont réunis dans un seul endroit, et prêts à l'emploi.
Other programs: Vs code , htop, cava.

[inspiration](https://github.com/lime-desu/dootsfile)
[neofetch](https://itsfoss.com/using-neofetch/)

## Desktop Gnome :
**Extensions : Blur My Shell, Just Perfection, Freon, Clipboard indicator, User Theme, Aylur's Widgets, AppIndicator and KStatusNotifierItem Support; ArcMenu; Bluetooth Quick Connect, Blur My Shell, Caffeine, Dash to Dock, Date Menu Formatter, Dynamic Panel Transparency, GSConnect, Media Controls, Privacy Quick Settings Menu, Rounded Corners, Workspace Indicator, Plank


---
## (GTK-Theme)[https://github.com/Fausto-Korpsvart/Gruvbox-GTK-Theme]
1. Intall `sudo dnf install gtk-murrine-engine`
2. Move the extracted files to the following paths:
	3. For GTK3: `~/.themes` In this path you must move the entire theme folder.
	4. For GTK4: `~/.config/gtk-4.0` The files to move to this path can be found inside the theme directory in the gtk-4.0 folder, copy only the `assets`, `gtk.css` and `gtk-dark.css` files or create a symlinks.
5. Applying GTK Themes to Flatpak Apps
	6. Override flatpak themes to `~/.themes`: `sudo flatpak override --filesystem=$HOME/.themes`
	7. Override flatpak icons to `~/.icons`: `sudo flatpak override --filesystem=$HOME/.icons`
	8. Override flatpak themes to `~/.config/gtk-4.0` locally: `flatpak override --user --filesystem=xdg-config/gtk-4.0`
	9. Override flatpak themes to `~/.config/gtk-4.0` globally: `sudo flatpak override --filesystem=xdg-config/gtk-4.0`
10. For icons and cursors move `icons` to `~/.icons`
10. For fonts move `fonts` to `~/.fonts`

---
## [Tartarus Grub](https://github.com/AllJavi/tartarus-grub)
[TODO](https://github.com/shvchk/fallout-grub-theme)
1. Intall
```bash
git clone https://github.com/AllJavi/tartarus-grub.git
cd tartarus-grub
sudo cp tartarus -r /usr/share/grub/themes/
sudo vim /etc/default/grub
```
Change `#GRUB_THEME=` to
`GRUB_THEME="/usr/share/grub/themes/tartarus/theme.txt"`
```bash
sudo grub2-mkconfig -o /boot/grub2/grub.cfg
```
If all works correctly you should get this line in the out put:
```bash
Found theme: /usr/share/grub/themes/tartarus/theme.txt
```
When editing the file `/etc/default/grub`, you also have to comment the line `'GRUB_TERMINAL_OUTPUT="console"`

---
## [ulauncher](https://ulauncher.io/#Download)  
1. Intall 
```bash
sudo dnf install ulauncher
``` 
2. To apply the Ulauncher themes, go to `~/.config/ulauncher`, and create the folder `/user-themes`.
	- Move the files to the `~/.config/ulauncher/user-themes`.
	- Now press `Ctrl+Spacebar` and click on the cog in the Ulauncher bar or click in Ulauncher systray icon and go to app config and choose the new themes.

## [Conky](https://github.com/brndnmtthws/conky)
1. install
```bash
sudo dnf install conky
``` 
2. Pour lancer conky au démarrage sous Gnome, il faut créer un fichier conky.desktop dans `~/.config/autostart` avec le contenu :
```bash
[Desktop Entry]
Name=Conky
Comment=Moniteur système
Exec=conky &
Terminal=false
Type=Application
Icon=gnome-monitor
Categories=System;
StartupNotify=false
``` 
3. start conky $`conky`
4. Par défaut, Conky ira chercher le fichier de configuration ~/.config/conky/conky.conf. S'il n'existe pas, Conky se repliera sur /etc/conky/conky.conf. Pour lancer un fichier de configuration de conky particulier, la commande à exécuter est :
```bash
conky -c /home/user/.config/conky/conky_alt.conf
```
5. pour lancer plusieurs Conky avec différentes configuration en même temps, vous devez réaliser un script bash. Pour cela, il faut créer un fichier en ".sh". Dans cet exemple, il sera nommé conky.sh.
```bash
#!/bin/sh
conky -c ~/.scripts/.conkyrc
conky -c ~/.scripts/.conkyrc2
conky -c ~/.scripts/.conkyrc3
conky -c ~/.scripts/.conkyrc4
```
6. Ensuite, ce fichier conky.sh doit être rendu exécutable. Pour cela, il suffit de faire
```bash
chmod +x conky.sh
```

##[cava](https://github.com/karlstav/cava)
1. install dependencies
```bash
sudo dnf install alsa-lib-devel ncurses-devel fftw3-devel pulseaudio-libs-devel libtool autoconf-archive
```
2. install
```bash
sudo dnf install cava
```

---
##  shell  
2. Intall [starship](https://starship.rs/) colors for prompt shell
3. Intall [synth-shell](https://github.com/andresgongora/synth-shell) replace starship


---
## Polybar 
1. Intall [polybar](https://github.com/polybar/polybar/wiki)
```bash
sudo dnf install polybar
``` 
2. Intall [starship](https://starship.rs/) colors for prompt shell.
3. Intall [synth-shell](https://github.com/andresgongora/synth-shell) replace starship

