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

Issue with display ribbon cable


## Keyboard

https://forum.clockworkpi.com/t/using-gamepad-arrows-and-buttons-in-command-line-apps/7059

Fn+<> brightness

Fn+Vol = Vol up

### update keyboard firmware 

`dfu-util -d 1EAF:0003 -a 2 -D devterm_keyboard.ino.bin` 
There are DIP switches on the base, switch DIP 2 to be seen by computer
UART on one side of keyboard.




### 3D prints

https://www.tinkercad.com/things/iB2n0KXmySi


