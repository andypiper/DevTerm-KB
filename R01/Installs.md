
## Fix apt sources to Jammy
sudo sed -i 's/devel/jammy/g' /etc/apt/sources.list

## Remove update notifier
sudo apt purge update-notifier common


## Remove pointless things
sudo apt purge gimp inkscape freedoom chocolate-doom colord motd-news-config gnome-terminal devterm-fan-temp-daemon-rpi snapd 


## Disable u-boot update for kernel upgrades
FWIW, /boot/exlinux/extlinux.conf is updated by u-boot-update. It looks like you can turn off automatic updating by adding `U_BOOT_UPDATE=false` to `/etc/default/u-boot`.


## My packages
  
sudo apt install -y 
ripgrep mosh neofetch libfltk1.3-dev libjpeg-dev libpng-dev libxft-dev libxext-dev thonny mu-editor python3 python3-rshell pyboard-rshell micropython zathura fonts-ibm-plex fonts-cabin fonts-noto-color-emoji fonts-noto bsdgames fonts-hack-ttf rxvt-unicode i3blocks gh zip unzip rofi zsh-syntax-highlighting zsh-autosuggestions zsh cruft-ng plocate debhelper devscripts cme x11vnc gpm i3-wm i3blocks fbterm fbcat nm-applet terminology bat focuswriter ne wordgrinder cargo fonts-mononoki fonts-hermit fonts-firacode fonts-league-mono nethack-console jq httpie fbset


terminews rsstail irssi* tinyirc inxi glirc f-irc tty-clock


## devterm stuff

sudo apt install devterm-fan-temp-daemon-rpi

### for trs terminal

- sudo apt install libfltk1.3-dev libjpeg-dev libpng-dev libxft-dev libxinerama-dev libxext-dev
- git clone https://github.com/sboger/VirtualT-DevTerm.git
- make

TODO: package, .desktop file etc

~~modify gkrellm and nedit and xterm fonts~~


## setup swap

sudo fallocate -l 2G /swapfile
sudo chmod 600 /swapfile
sudo mkswap /swapfile
sudo swapon /swapfile
sudo swapon --show
   
set swap in `/etc/fstab`
`/swapfile swap swap defaults 0 0`


## Fix printing permissions
add cpi user to lp and lpadmin groups
sudo adduser cpi lpadmin
sudo adduser cpi lp

and do the apparmo fix


## change console font size
sudo dpkg-reconfigure console-setup
  
  
## I want Avahi / network discovery
 sudo systemctl enable avahi-daemon.service
  

echo "set sandbox none" > .config/zathura/zathurarc


  Configure i3 and i3blocks
  
  
  Install VNC server
  https://forum.clockworkpi.com/t/setup-easy-temporary-vnc-for-devterm/8319
  
  
  
  
## terminology

- https://linoxide.com/terminology-terminal/
- https://ostechnix.com/terminology-a-best-terminal-emulator-with-lots-of-features/
- 