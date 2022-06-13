remove update-notifier-common



ripgrep
mosh
neofetch
feh



sudo apt install devterm-fan-temp-daemon-rpi



for trs terminal

sudo apt install libfltk1.3-dev libjpeg-dev libpng-dev libxft-dev libxinerama-dev libxext-dev

git clone https://github.com/sboger/VirtualT-DevTerm.git

make







take screenshot

xwd -root -display :0 | convert xwd:- jpg:- > file.jpg



modify gkrellm and nedit and xterm fonts


setup swap

   33  sudo fallocate -l 2G /swapfile
   34  sudo chmod 600 /swapfile
   35  sudo mkswap /swapfile
   36  sudo swapon /swapfile
   38  sudo swapon --show
   
set swap in /etc/fstab
/swapfile swap swap defaults 0 0

add cpi user to lp and lpadmin groups
useradd cpi lp





sudo apt install thonny mu-editor python3 python3-rshell pyboard-rshell micropython



   47  sudo apt install rxvt-unicode
   49  sudo apt install zathura
   52  sudo apt install fonts-ibm-plex fonts-cabin fonts-noto-color-emoji fonts-noto
   56  sudo apt install bsdgames fonts-hack-ttf rxvt-unicode
   68  sudo apt install i3blocks
   71  sudo apt install gh
   zip unzip
   sudo apt install rofi
  150  sudo apt install zsh-syntax-highlighting zsh-autosuggestions zsh
  
  
  I want Avahi / network discovery
  
  sudo systemctl enable avahi-daemon.service
  
  sudo apt install cruft-ng plocate
  sudo apt install debhelper devscripts cme
  
  
  Configure i3 and i3blocks
  
  
  Install VNC server
  https://forum.clockworkpi.com/t/setup-easy-temporary-vnc-for-devterm/8319