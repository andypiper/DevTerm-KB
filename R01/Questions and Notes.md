

- how to upgrade (software)
  - switch back to Jammy repos to avoid confusing apt with Kinetic
  - remove broken packages
  - clean, update, slowly update packages

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

`xwd -root -display :0 | convert xwd:- jpg:- > file.jpg`


hardware access macros (zsh)
```
function battery() {
	(( chrg = $((`cat /sys/class/power_supply/axp20x-battery/capacity`)) ))
	echo $chrg%
}

function cputemp() {
	(( temp = $((`cat /sys/class/thermal/thermal_zone0/temp` / 1000)) ))
	echo $temp C
}

function fanon() {
	gpio mode 41 out
	gpio write 41 1
}

function fanoff() {
	gpio mode 41 out
	gpio write 41 0
}
```




look into Julia
look into Oberon
