1. Install Ubuntu Server Arm

2. Remove unnecessary Ubuntu Server-specific packages
   ``` sudo apt purge --autoremove ubuntu-server -y ```
4. Download Desktop:<br>
``` sudo apt-get install --no-install-recommends ubuntu-desktop -y ```
5. Fix Dark Mode:<br>
``` sudo apt purge ubuntu-session yaru-theme-gnome-shell yaru-theme-gtk yaru-theme-icon yaru-theme-sound && sudo apt install ubuntu-session yaru-theme-gnome-shell yaru-theme-gtk yaru-theme-icon yaru-theme-sound ```
