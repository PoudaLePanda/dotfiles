# dotfiles
Ensemble de fichiers de configuration pour desktop Gnome sur fedora 38.
Tous ces fichiers sont réunis dans un seul endroit, et prêts à l'emploi.

Avant de commencer on s'[ambiance](https://www.youtube.com/watch?v=9Broidxg7w0) !
- **OS**: [Fedora Linux](https://getfedora.org/)
- **Shell**: bash
  - **Prompt**: [Starship](https://starship.rs/)
- **Terminal**: [gnome terminal](https://help.gnome.org/users/gnome-terminal/stable/)
- **Editor**: [code](https://code.visualstudio.com/)
- **Browser**: [brave](https://brave.com/)
- **Fonts**: Jetbrains Mono [Nerd Font](https://www.nerdfonts.com/), SF Pro Mono
- **Icons**:
  - **Application**: [Skeouwaita](https://github.com/Frostbitten-jello/Skeuowaita)
  - **Cursor**: [Catppuccin Cursor](https://github.com/catppuccin/cursors), [Phinger Cursors](https://github.com/phisch/phinger-cursors)
- **Colorscheme**: [Catppuccin](https://github.com/catppuccin/catppuccin) Mocha (Lavender)

## Post-install fedora 38
1. Update & Upgrade (En Preums):
	- sudo dnf update -y && sudo dnf upgrade -y
	- sudo fwupdmgr refresh --force
	- sudo fwupdmgr update
	- sudo dnf upgrade --refresh
6. Speed up DNF:
	- echo 'fastestmirror=1' | sudo tee -a /etc/dnf/dnf.conf
	- echo 'max_parallel_downloads=10' | sudo tee -a /etc/dnf/dnf.conf
7 Activer rpm fusion
	- [rpm fusion](https://rpmfusion.org/Configuration)
	- sudo dnf upgrade --refresh
7. Install DNFDragora:
	- sudo dnf install dnfdragora
4. Install Preload
	- sudo dnf copr enable elxreno/preload -y && sudo dnf install preload -y
2 Installing essential packages
	- sudo dnf install timeshift mpv gnome-tweaks git vlc unrar unzip python3-pip cargo p7zip p7zip-plugins ntfs-3g steam htop kdeconnectd chrome-gnome-shell gnome-extensions-app bleachbit
11. Better Fonts:
	- sudo dnf copr enable dawid/better_fonts -y
	- sudo dnf install fontconfig-font-replacements -y
	- sudo dnf install fontconfig-enhanced-defaults -y
13. gnome extension manager & dynamic wallpaper using the flatpak. 
	- flatpak install flathub com.mattjakeman.ExtensionManager
	- flatpak install flathub me.dusansimic.DynamicWallpaper
14. [Setup MacOS theme](https://github.com/vinceliuice/WhiteSur-gtk-theme)
	- git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git
	- ./install.sh -m -t all -l -N stable --normal --round
	- sudo ./tweaks.sh -g

[inspiration](https://github.com/lime-desu/dootsfile)
[neofetch](https://itsfoss.com/using-neofetch/)

- **DE**: [Gnome](https://www.gnome.org/)
  - **Extensions**:
    -  [user-themes](https://extensions.gnome.org/extension/19/user-themes/)
    -  [just-perfection](https://extensions.gnome.org/extension/3843/just-perfection/)
    -  [caffeine](https://extensions.gnome.org/extension/517/caffeine/)
    -  [blur-my-shell](https://extensions.gnome.org/extension/3193/blur-my-shell/)
    -  [rounded-window-corners](https://extensions.gnome.org/extension/5237/rounded-window-corners/)
    -  [dash-to-dock](https://extensions.gnome.org/extension/307/dash-to-dock/)
    -  [pop-os-shell](https://github.com/pop-os/shell)
    -  [tray-icons-reloaded](https://extensions.gnome.org/extension/2890/tray-icons-reloaded/)
    -  [netspeed](https://extensions.gnome.org/extension/104/netspeed/)
    -  [todotxt](https://extensions.gnome.org/extension/570/todotxt/)
    -  [dash-to-panel](https://extensions.gnome.org/extension/1160/dash-to-panel/)
    -  [openweather](https://extensions.gnome.org/extension/750/openweather/)
    -  [weather](https://extensions.gnome.org/extension/613/weather/)
    -  [coverflow-alt-tab](https://extensions.gnome.org/extension/97/coverflow-alt-tab/)
    -  [burn-my-windows](https://extensions.gnome.org/extension/4679/burn-my-windows/)
    -  [compiz-alike-magic-lamp-effect](https://extensions.gnome.org/extension/3740/compiz-alike-magic-lamp-effect/)
    -  [workspaces-to-dock](https://extensions.gnome.org/extension/427/workspaces-to-dock/)
    -  [aylurs-widgets](https://extensions.gnome.org/extension/5338/aylurs-widgets/)
    -  [hidetopbar](https://extensions.gnome.org/extension/545/hide-top-bar/)
    -  [pano](https://extensions.gnome.org/extension/5278/pano/)

---


