# cpu-performance
A simple Bash script that sets the CPU governor to performance on all cores.

This is one of my first proper Bash scripts, mainly intended for personal use — but feel free to use or modify it if you find it helpful.

## Features

* Checks current CPU governor and sets it to performance if it isn't already

* Optional systemd service to automatically execute the script at boot


## Installation (Arch based systems)

```
git clone https://github.com/ashisgreat22/cpu-performance.git
cd cpu-performance
makepkg -si
```
## Requirements

* Linux system with CPU frequency scaling (/sys/devices/system/cpu/cpu*/cpufreq/)

* Root privileges

* `bash` and `coreutils`

## Disclaimer
 This script assumes:

* All CPU cores are online and support the same governor

* You're intentionally overriding any default or distro-specific power management behavior

It’s a personal project and far from perfect
