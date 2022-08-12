# linux-kernel-quectel-RM502Q
- Out-of-the-box Linux kernel compatible with Quectel RM502Q 
- Tested on Dell XPS laptop 15-inch:
Architecture:        x86_64,
CPU op-mode(s):      32-bit, 64-bit,
Byte Order:          Little Endian,
CPU(s):              8,
On-line CPU(s) list: 0-7,
Thread(s) per core:  2,
Core(s) per socket:  4,
CPU family:          6,
Model:               158,
Model name:          Intel(R) Core(TM) i7-7700HQ CPU @ 2.80GHz,
Stepping:            9,
CPU MHz:             900.064,
CPU max MHz:         3800.0000,
CPU min MHz:         800.0000,
BogoMIPS:            5599.85,

- Based on linux kernel version 4.19.254. The base kernel is modifed according to Quectel RM502Q documentations to accomodate Quectel's provided drivers: USB for GSM and CDMA modems and QMI_WWAN.
- Quectel provides QMI_WWAN and Gobinet drivers. Only either of them should be used. This repo use QMI_WWAN only.
- Usage: pull the repo, cd into the source directory, then:
```console 
$ cp ./config-4.19.254-Quectel-Compatible .config
```
- ***Note: this is the configuration for DELL XPS laptop 15-inch; it does not necessarily work with any other machines. Contrast this one with the config file on your own machine (i.e, /boot/linux-$(uname -r)/ for Debian/Ubuntu) for proper configuration. If you cannot boot into the system, most likely the configurations are wrong.***
- then:
```console 
$ sudo sh ./make_all.sh
```
