# dotfiles
Ensemble de fichiers de configuration pour desktop Gnome sur fedora 38.
Tous ces fichiers sont réunis dans un seul endroit, et prêts à l'emploi.

## Post-install fedora 38
1. Update & Upgrade (En Preums):
	- sudo dnf update -y && sudo dnf upgrade -y
	- sudo fwupdmgr refresh --force
	- sudo fwupdmgr update
	- sudo dnf upgrade --refresh
1.5. Activer rpm fusion
	- [rpm fusion](https://rpmfusion.org/Configuration)
	- sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm
	- sudo dnf upgrade --refresh
2.5 Installing essential packages
	- sudo dnf install mpv gnome-tweaks git vlc unrar unzip python3-pip cargo p7zip p7zip-plugins ntfs-3g steam htop kdeconnectd
3. Install Timeshift backup:
	- sudo dnf install timeshift
4. Install Preload
	- sudo dnf copr enable elxreno/preload -y && sudo dnf install preload -y
5. Firefox Tweaks:
	- about:config
	- layers.acceleration.force-enabled
	- gfx.webrender.all
6. Speed up DNF:
	- echo 'fastestmirror=1' | sudo tee -a /etc/dnf/dnf.conf
	- echo 'max_parallel_downloads=10' | sudo tee -a /etc/dnf/dnf.conf
7. Install DNFDragora:
	- sudo dnf isntall dnfdragora
8. Install GNOME Extensions:
	- dnf install chrome-gnome-shell gnome-extensions-app
11. Better Fonts:
	- sudo dnf copr enable dawid/better_fonts -y
	- sudo dnf install fontconfig-font-replacements -y
	- sudo dnf install fontconfig-enhanced-defaults -y
12. Install Bleachbit:
	- sudo dnf install bleachbit
13. gnome extension manager & dynamic wallpaper using the flatpak. 
	- flatpak install flathub com.mattjakeman.ExtensionManager
	- flatpak install flathub me.dusansimic.DynamicWallpaper
14. [Setup MacOS theme](https://github.com/vinceliuice/WhiteSur-gtk-theme)
	- git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git
	- ./install.sh -m -t all -l -N stable --normal --round
	- sudo ./tweaks.sh -g
	- sudo ./tweaks.sh -f (pour firefox)
15. Open the Dynamic Wallpaper application and import both the Light and Dark wallpapers.

[inspiration](https://github.com/lime-desu/dootsfile)
[neofetch](https://itsfoss.com/using-neofetch/)

## Desktop Gnome :
**Extensions : Blur My Shell, Just Perfection, Freon, User Theme, Aylur's Widgets, AppIndicator and KStatusNotifierItem Support; ArcMenu; Bluetooth Quick Connect, Blur My Shell, Caffeine, Dash to Dock, Date Menu Formatter, Dynamic Panel Transparency, GSConnect, Media Controls, Privacy Quick Settings Menu, Rounded Corners,Quick Settings Tweaker , Workspace Indicator, Plank, dash to dock animator, Compiz Magic Lamp Effect, Gnome 4X UI Improvements

---
##  shell  
1. Intall [starship](https://starship.rs/) colors for prompt shell
2. Intall [synth-shell](https://github.com/andresgongora/synth-shell) replace starship


