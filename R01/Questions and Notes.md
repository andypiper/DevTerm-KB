

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


- using byobu


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
    (( chrg = $((`/usr/bin/cat /sys/class/power_supply/axp20x-battery/capacity`)) ))
    echo $chrg%, `/usr/bin/cat /sys/class/power_supply/axp20x-battery/status`
}

function cputemp() {
    (( temp = $((`/usr/bin/cat /sys/class/thermal/thermal_zone0/temp` / 1000)) ))
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








## Trying out sbcbench

See [this issue](https://github.com/ThomasKaiser/sbc-bench/issues/43) for related conversation

Need to shut down a lot of background stuff to get CPU load below ~10% for bench:

```
   sudo systemctl stop devterm-audio-patch.service
   sudo systemctl stop devterm-socat
   sudo systemctl stop devterm-printer
   sudo systemctl stop cups
   sudo systemctl stop unattended-upgrades
   sudo systemctl stop rtkit-daemon
   sudo systemctl stop devterm-keyboard
```

```
cpi@devterm-R01:~$ sudo /bin/bash ./sbc-bench.sh -c
[sudo] password for cpi:

Average load and/or CPU utilization too high (too much background activity). Waiting...

dirname: invalid option -- '1'
Try 'dirname --help' for more information.
dirname: missing operand
Try 'dirname --help' for more information.
Too busy for benchmarking: 11:13:21 up 1 min,  3 users,  load average: 1.17, 0.65, 0.25,  cpu: 57%
Too busy for benchmarking: 11:13:26 up 1 min,  3 users,  load average: 1.08, 0.64, 0.25,  cpu: 12%
Too busy for benchmarking: 11:13:31 up 1 min,  3 users,  load average: 0.99, 0.63, 0.25,  cpu: 10%
Too busy for benchmarking: 11:13:36 up 2 min,  3 users,  load average: 0.91, 0.62, 0.25,  cpu: 9%
Too busy for benchmarking: 11:13:41 up 2 min,  3 users,  load average: 0.84, 0.61, 0.25,  cpu: 9%
Too busy for benchmarking: 11:13:46 up 2 min,  3 users,  load average: 0.77, 0.60, 0.25,  cpu: 9%
Too busy for benchmarking: 11:13:51 up 2 min,  3 users,  load average: 0.71, 0.59, 0.25,  cpu: 10%
Too busy for benchmarking: 11:13:57 up 2 min,  3 users,  load average: 0.65, 0.58, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:02 up 2 min,  3 users,  load average: 0.60, 0.57, 0.24,  cpu: 11%
Too busy for benchmarking: 11:14:07 up 2 min,  3 users,  load average: 0.55, 0.56, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:12 up 2 min,  3 users,  load average: 0.51, 0.55, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:17 up 2 min,  3 users,  load average: 0.47, 0.54, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:23 up 2 min,  3 users,  load average: 0.51, 0.55, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:28 up 2 min,  3 users,  load average: 0.47, 0.54, 0.24,  cpu: 9%
Too busy for benchmarking: 11:14:33 up 3 min,  3 users,  load average: 0.43, 0.53, 0.24,  cpu: 9%
Too busy for benchmarking: 11:14:38 up 3 min,  3 users,  load average: 0.44, 0.53, 0.24,  cpu: 10%
Too busy for benchmarking: 11:14:43 up 3 min,  3 users,  load average: 0.40, 0.52, 0.24,  cpu: 9%
Too busy for benchmarking: 11:14:48 up 3 min,  3 users,  load average: 0.37, 0.51, 0.24,  cpu: 9%
Too busy for benchmarking: 11:14:54 up 3 min,  3 users,  load average: 0.34, 0.50, 0.24,  cpu: 9%
Too busy for benchmarking: 11:14:59 up 3 min,  3 users,  load average: 0.31, 0.49, 0.24,  cpu: 9%
Too busy for benchmarking: 11:15:04 up 3 min,  3 users,  load average: 0.29, 0.49, 0.23,  cpu: 9%
Too busy for benchmarking: 11:15:09 up 3 min,  3 users,  load average: 0.26, 0.48, 0.23,  cpu: 14%
Too busy for benchmarking: 11:15:14 up 3 min,  3 users,  load average: 0.24, 0.47, 0.23,  cpu: 10%
Too busy for benchmarking: 11:15:20 up 3 min,  3 users,  load average: 0.22, 0.46, 0.23,  cpu: 11%
```

