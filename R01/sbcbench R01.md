http://ix.io/40wo

```
sbc-bench v0.9.8 Allwinner D1 (Mon, 20 Jun 2022 11:38:41 +0000)

Distributor ID:	Ubuntu
Description:	Ubuntu 22.04 LTS
Release:	22.04
Codename:	jammy

/usr/bin/gcc (Ubuntu 11.2.0-19ubuntu1) 11.2.0

Uptime: 11:38:44 up 27 min,  2 users,  load average: 3.27, 1.92, 1.16

Linux 5.4.61 (devterm-R01) 	06/20/22 	_riscv64_	(1 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
          27.90    0.20   16.53    2.56    0.00   52.80

Device             tps    kB_read/s    kB_wrtn/s    kB_dscd/s    kB_read    kB_wrtn    kB_dscd
mmcblk0          10.92       269.59       334.11         0.00     439731     544964          0

               total        used        free      shared  buff/cache   available
Mem:           960Mi        70Mi       811Mi       1.0Mi        78Mi       873Mi
Swap:          2.0Gi          0B       2.0Gi

Filename				Type		Size		Used		Priority
/swapfile                               file		2097148		0		-2

##########################################################################

##########################################################################

Hardware sensors:

axp20x_battery-isa-0000
in0:           4.04 V  
curr1:       579.00 mA 

##########################################################################

##########################################################################

##########################################################################

Executing benchmark on each cluster individually

OpenSSL 3.0.2, built on 15 Mar 2022 (Library: OpenSSL 3.0.2 15 Mar 2022)

##########################################################################

Compression: 
Decompression: 
Total: 

##########################################################################

Testing maximum cpufreq again, still under full load. System health now:

System health while running 7-zip single core benchmark:

##########################################################################

Hardware sensors:

axp20x_battery-isa-0000
in0:           4.04 V  
curr1:       583.00 mA 

##########################################################################

Thermal source: /sys/devices/virtual/thermal/thermal_zone0/ (cpu_thermal_zone)

System health while running tinymembench:

System health while running ramlat:

System health while running OpenSSL benchmark:

System health while running 7-zip single core benchmark:

##########################################################################

Linux 5.4.61 (devterm-R01) 	06/20/22 	_riscv64_	(1 CPU)

avg-cpu:  %user   %nice %system %iowait  %steal   %idle
          27.89    0.20   16.60    2.64    0.00   52.68

Device             tps    kB_read/s    kB_wrtn/s    kB_dscd/s    kB_read    kB_wrtn    kB_dscd
mmcblk0          11.13       286.69       333.34         0.00     468747     545020          0

               total        used        free      shared  buff/cache   available
Mem:           960Mi        70Mi       782Mi       1.0Mi       107Mi       873Mi
Swap:          2.0Gi          0B       2.0Gi

Filename				Type		Size		Used		Priority
/swapfile                               file		2097148		0		-2

CPU sysfs topology (clusters, cpufreq members, clockspeeds)
                 cpufreq   min    max
 CPU    cluster  policy   speed  speed   core type
  0       -1        0       -      -         -

Architecture:        riscv64
Byte Order:          Little Endian
CPU(s):              1
On-line CPU(s) list: 0

Signature: 10
DT compat: allwinner,d1
           arm,sun20iw1p1
           allwinner,sun20iw1p1
 Compiler: /usr/bin/gcc (Ubuntu 11.2.0-19ubuntu1) 11.2.0 / riscv64-linux-gnu
 Userland: riscv64
   Kernel: 5.4.61/riscv64
           CONFIG_HZ=100
           CONFIG_HZ_100=y
           CONFIG_PREEMPTION=y
           CONFIG_PREEMPT=y
           CONFIG_PREEMPT_COUNT=y
           CONFIG_PREEMPT_RCU=y

| Allwinner D1 | no cpufreq support | 5.4 | Ubuntu 22.04 LTS riscv64 | 0 | 0 | 0 | 0 | 0 | - |
```