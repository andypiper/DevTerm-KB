

Fn+<> - screen brightness


- how to upgrade
- how to manage fan
  - modify Rpi fan control for different temperature tooling 
- how to manage printer
- cores on CPU
- why is default config in a zip?
- 



Switch to zsh

... default setup uses .bash_profile to invoke startx, if you install zsh, this is skipped, so it goes to cmd prompt on login. 



- boot dmesg error
proc: Bad value for 'hidepid'

--> https://bugs.launchpad.net/ubuntu/+source/systemd/+bug/1918328
(old kernel new systemd + harmless)



PICO-8 no version for RISC-V
- also, unable to install libsdl2 at the moment.








to take screenshot

xwd -root -display :0 | convert xwd:- jpg:- > file.jpg
