```text
devterm-r01
    description: Computer
    product: sun20iw1p1
    width: 64 bits
  *-core
       description: Motherboard
       physical id: 0
     *-cpu:0
          description: CPU
          product: cpu
          physical id: 0
          bus info: cpu@0
          size: 24MHz
          width: 32 bits
     *-cpu:1 DISABLED
          description: CPU
          product: idle-states
          physical id: 1
          bus info: cpu@1
     *-memory
          description: System memory
          physical id: 2
          size: 960MiB
  *-usbhost:0
       product: EHCI Host Controller
       vendor: Linux 5.4.61 ehci_hcd
       physical id: 1
       bus info: usb@1
       logical name: usb1
       version: 5.04
       capabilities: usb-2.00
       configuration: driver=hub slots=1 speed=480Mbit/s
     *-usb
          description: USB hub
          product: USB2.0 Hub
          vendor: Genesys Logic, Inc.
          physical id: 1
          bus info: usb@1:1
          version: 85.38
          capabilities: usb-2.00
          configuration: driver=hub maxpower=100mA slots=4 speed=480Mbit/s
        *-usb
             description: Human interface device
             product: ClockworkPI DevTerm Mouse
             vendor: ClockworkPI
             physical id: 1
             bus info: usb@1:1.1
             logical name: input1
             logical name: /dev/input/event1
             logical name: input2
             logical name: /dev/input/event2
             logical name: input2::capslock
             logical name: input2::compose
             logical name: input2::kana
             logical name: input2::numlock
             logical name: input2::scrolllock
             logical name: input3
             logical name: /dev/input/event3
             logical name: input4
             logical name: /dev/input/event4
             version: 2.00
             serial: 20210531
             capabilities: usb-2.00 usb
             configuration: driver=usbhid maxpower=100mA speed=12Mbit/s
  *-usbhost:1
       product: OHCI Host Controller
       vendor: Linux 5.4.61 ohci_hcd
       physical id: 2
       bus info: usb@2
       logical name: usb2
       version: 5.04
       capabilities: usb-1.10
       configuration: driver=hub slots=1 speed=12Mbit/s
  *-mmc0
       description: MMC Host
       physical id: 3
       logical name: mmc0
     *-device
          description: SD Card
          product: SL64G
          vendor: SanDisk
          physical id: aaaa
          logical name: /dev/mmcblk0
          version: 8.0
          date: 11/2015
          serial: 763962840
          size: 59GiB (63GB)
          capabilities: sd partitioned partitioned:dos
          configuration: logicalsectorsize=512 sectorsize=512 signature=da568ce2
        *-volume:0
             description: Windows FAT volume
             vendor: mkfs.fat
             physical id: 2
             logical name: /dev/mmcblk0p2
             version: FAT16
             serial: 8d26-7ee3
             size: 121MiB
             capacity: 122MiB
             capabilities: primary fat initialized
             configuration: FATs=2 filesystem=fat
        *-volume:1
             description: EXT4 volume
             vendor: Linux
             physical id: 3
             logical name: /dev/mmcblk0p3
             logical name: /boot
             version: 1.0
             serial: 9cdb105d-4919-4f91-8a99-0d709255e00f
             size: 489MiB
             capacity: 489MiB
             capabilities: primary bootable journaled extended_attributes large_files huge_files dir_nlink recover 64bit extents ext4 ext2 initialized
             configuration: created=2021-11-16 17:22:25 filesystem=ext4 label=_/boot lastmountpoint=/boot modified=2022-03-18 16:12:23 mount.fstype=ext4 mount.options=rw,no
atime mounted=2022-03-18 16:12:23 state=mounted
        *-volume:2
             description: EXT4 volume
             vendor: Linux
             physical id: 4
             logical name: /dev/mmcblk0p4
             version: 1.0
             serial: 13270b62-ee26-426e-ab89-fd6af83aaaad
             size: 58GiB
             capacity: 58GiB
             capabilities: primary journaled extended_attributes large_files huge_files dir_nlink recover 64bit extents ext4 ext2 initialized
             configuration: created=2022-02-14 00:10:27 filesystem=ext4 lastmountpoint=/ modified=2022-03-31 07:40:04 mounted=2022-03-18 16:12:11 state=clean
  *-mmc1
       description: MMC Host
       physical id: 4
       logical name: mmc1
     *-device
          description: SDIO Device
          physical id: 0
          bus info: mmc@1:0001
          serial: 0
          capabilities: sdio
        *-interface:0
             description: Wireless interface
             product: 43455
             vendor: Broadcom
             physical id: 1
             bus info: mmc@1:0001:1
             logical name: mmc1:0001:1
             logical name: wlan0
             serial: d4:9c:dd:a3:7e:82
             capabilities: ethernet physical wireless
             configuration: broadcast=yes driver=brcmfmac driverversion=7.45.96 firmware=es7.c5.n4.a3 ip=172.16.0.95 multicast=yes wireless=IEEE 802.11
        *-interface:1
             product: 43455
             vendor: Broadcom
             physical id: 2
             bus info: mmc@1:0001:2
             logical name: mmc1:0001:2
        *-bt
             description: BlueTooth interface
             product: 43455
             vendor: Broadcom
             physical id: 3
             bus info: mmc@1:0001:3
             logical name: mmc1:0001:3
             capabilities: wireless bluetooth
             configuration: wireless=BlueTooth
  *-sound
       description: audiocodec
       physical id: 5
       logical name: card0
       logical name: /dev/snd/controlC0
       logical name: /dev/snd/pcmC0D0c
       logical name: /dev/snd/pcmC0D0p
  *-graphics
       physical id: 6
       logical name: /dev/fb0
       capabilities: fb
       configuration: depth=32 resolution=480,1280
  *-input:0
       product: sunxi-keyboard
       physical id: 7
       logical name: input0
       logical name: /dev/input/event0
       capabilities: platform
  *-input:1
       product: audiocodec sunxi Audio Jack
       physical id: 8
       logical name: input5
       logical name: /dev/input/event5
```



```text
cpi@devterm-R01:~$ ls /dev
block		 fd	      initctl	 mmcblk0p4  ptyp5  ptype      spidev1.0       tty0   tty17  tty25  tty33  tty41  tty5	tty58  tty9   ttyp6  ttypf     vcs6   vcsu1
bus		 full	      input	 null	    ptyp6  ptypf      stderr	      tty1   tty18  tty26  tty34  tty42  tty50	tty59  ttyS0  ttyp7  ubi_ctrl  vcsa   vcsu2
cedar_dev	 fuse	      ion	 ptmx	    ptyp7  random     stdin	      tty10  tty19  tty27  tty35  tty43  tty51	tty6   ttyS1  ttyp8  urandom   vcsa1  vcsu3
char		 g2d	      kmsg	 pts	    ptyp8  rfkill     stdout	      tty11  tty2   tty28  tty36  tty44  tty52	tty60  ttyp0  ttyp9  vcs       vcsa2  vcsu4
console		 gpiochip0    log	 ptyp0	    ptyp9  rpaf-dsp0  sunxi-reg       tty12  tty20  tty29  tty37  tty45  tty53	tty61  ttyp1  ttypa  vcs1      vcsa3  vcsu5
cpu_dma_latency  hdmi	      mem	 ptyp1	    ptypa  rtc	      sunxi-wlan      tty13  tty21  tty3   tty38  tty46  tty54	tty62  ttyp2  ttypb  vcs2      vcsa4  vcsu6
disk		 i2c-0	      mmcblk0	 ptyp2	    ptypb  rtc0       sunxi_pwm0      tty14  tty22  tty30  tty39  tty47  tty55	tty63  ttyp3  ttypc  vcs3      vcsa5  watchdog
disp		 iio:device0  mmcblk0p2  ptyp3	    ptypc  shm	      sunxi_soc_info  tty15  tty23  tty31  tty4   tty48  tty56	tty7   ttyp4  ttypd  vcs4      vcsa6  watchdog0
fb0		 iio:device1  mmcblk0p3  ptyp4	    ptypd  snd	      tty	      tty16  tty24  tty32  tty40  tty49  tty57	tty8   ttyp5  ttype  vcs5      vcsu   zero
```


Issue with display ribbon cable


## Keyboard

https://forum.clockworkpi.com/t/using-gamepad-arrows-and-buttons-in-command-line-apps/7059

Fn+<> brightness

Fn+Vol = Vol up

### update keyboard firmware 

`dfu-util -d 1EAF:0003 -a 2 -D devterm_keyboard.ino.bin` 
There are DIP switches on the base, switch DIP 2 to be seen by computer
UART on one side of keyboard.



## GPIO access

may need udev rule + setuid tools / group?


## sound


## video out

Failing.

dmesg:

```
[    0.199831] [DISP]disp_module_init
[    0.200403] disp 5000000.disp: Adding to iommu group 0
[    0.239946] [DISP] disp_init_hdmi,line:1047:
[    0.239950] dont support hdmi
[    0.240357] raoyiming +++LCD_cfg_panel_info
[    0.240435] display_fb_request,fb_id:0
[    0.256841] [DISP] Fb_copy_boot_fb,line:1444:
[    0.256845] no boot_fb0
[    0.257361] disp_al_manager_apply ouput_type:0
[    0.257763] [DISP] lcd_clk_config,line:731:
[    0.257776] disp 0, clk: pll(330000000),clk(330000000),dclk(55000000) dsi_rate(55000000)
                    clk real:pll(324000000),clk(324000000),dclk(81000000) dsi_rate(150000000)
[    0.258107] raoyiming +++ LCD_open_flow
[    0.272681] <0>raoyiming +++ sunxi_lcd_gpio_set_value
[    0.382658] <0>raoyiming +++ LCD_panel_init
[    1.252847] [DISP] disp_lcd_gpio_set_value,line:2565:
[    1.252853] of_get_named_gpio_flags for lcd_gpio_1 failed
```


## Printer module

Needs user to be added to lp and lpadmin groups

Ideally needs some wrapper scripts or an app to actually send text and images to the printer.

Default text is large and not very helpful for keeping text files on paper.



## gpm / console pointer

```
devterm-R01% sudo apt install gpm
[sudo] password for cpi:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  gpm
0 upgraded, 1 newly installed, 0 to remove and 370 not upgraded.
Need to get 0 B/177 kB of archives.
After this operation, 496 kB of additional disk space will be used.
Preconfiguring packages ...
Selecting previously unselected package gpm.
(Reading database ... 158816 files and directories currently installed.)
Preparing to unpack .../gpm_1.20.7-10build1_riscv64.deb ...
Unpacking gpm (1.20.7-10build1) ...
Setting up gpm (1.20.7-10build1) ...
Could not execute systemctl:  at /usr/bin/deb-systemd-invoke line 142.
Job for gpm.service failed because the service did not take the steps required by its unit configuration.
See "systemctl status gpm.service" and "journalctl -xeu gpm.service" for details.
invoke-rc.d: initscript gpm, action "restart" failed.
× gpm.service - Console Mouse manager
     Loaded: loaded (/lib/systemd/system/gpm.service; enabled; vendor preset: enabled)
     Active: failed (Result: protocol) since Mon 2022-06-20 12:59:02 UTC; 100ms ago
       Docs: man:gpm(8)
             man:gpm.conf(5)
             man:gpm-types(7)
    Process: 9814 ExecStart=/usr/share/gpm/gpm-systemd-wrapper.sh (code=exited, status=0/SUCCESS)
        CPU: 30ms

Jun 20 12:59:01 devterm-R01 systemd[1]: Starting Console Mouse manager...
Jun 20 12:59:01 devterm-R01 /usr/sbin/gpm[9816]: *** info [daemon/startup.c(131)]:
Jun 20 12:59:01 devterm-R01 /usr/sbin/gpm[9816]: Started gpm successfully. Entered daemon mode.
Jun 20 12:59:01 devterm-R01 /usr/sbin/gpm[9816]: O0o.oops(): [daemon/old_main.c(58)]:
Jun 20 12:59:01 devterm-R01 /usr/sbin/gpm[9816]: Could not open /dev/input/mice.
Jun 20 12:59:02 devterm-R01 systemd[1]: gpm.service: New main PID 9816 does not exist or is a zombie.
Jun 20 12:59:02 devterm-R01 systemd[1]: gpm.service: Failed with result 'protocol'.
Jun 20 12:59:02 devterm-R01 systemd[1]: Failed to start Console Mouse manager.
dpkg: error processing package gpm (--configure):
 installed gpm package post-installation script subprocess returned error exit status 1
Processing triggers for man-db (2.10.2-1) ...
Processing triggers for install-info (6.8-4build1) ...
Errors were encountered while processing:
 gpm
E: Sub-process /usr/bin/dpkg returned an error code (1)
devterm-R01%
```

then... 
sudo ln -s /dev/input/event4 /dev/input/mice
vi /etc/gpm.conf

```
device=/dev/input/mice
responsiveness=
repeat_type=none
type=evdev
append=''
sample_rate=
```

Daemon starts now, but still failing 
```
Jun 20 13:12:45 devterm-R01 /usr/sbin/gpm[10992]: Error in read()ing first: Invalid argument
Jun 20 13:12:45 devterm-R01 /usr/sbin/gpm[10992]: *** err [daemon/getmousedata.c(47)]:
```

(also, there's no console cursor visible anyway)

## Addons

### 3D prints

https://www.tinkercad.com/things/iB2n0KXmySi


