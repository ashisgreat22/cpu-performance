# cpu-performance
A simple Bash script that sets the CPU governor to performance on all cores.

This is one of my first proper Bash scripts, mainly intended for personal use — but feel free to use or modify it if you find it helpful.

## Features

* Checks current CPU governor and sets it to the defined governor if it isn't already
* Config file to change which governor is used when run without any arguement
* Optional systemd service to automatically execute the script at boot
* Ability to list all available governors

## Installation (Arch based systems)

```
git clone https://github.com/ashisgreat22/cpu-performance.git
cd cpu-performance
makepkg -si
```

## Manual installation (All distros)

1. Download the ```cpu-performance``` file from the latest release
2. Place the file at /usr/local/bin 
3. Make it executable: ```chmod +x /usr/local/bin/cpu-performance```

(Optional)
To configure the default target_governor
Download the config file and place it at /etc/cpu-performance.conf (Can also be placed at ~/.config/cpu-performance.conf)

To install the systemd service
1. Download the .service file and place at /etc/systemd/system/cpu-performance.service

## Usage 
To run the script manually:

```sudo cpu-performance <target_governor>```
If no governor is specified it will check config files in this order
1. /etc/cpu-performance.conf 
2. ~/.config/cpu-performance.conf (Overrides 1., This file is not checked when using the systemd service)
3. Falls back to performance if no config file is found
```cpu-performance --list # Lists all available governors for your system```

To enable the systemd service at boot:

```sudo systemctl enable cpu-performance.service # target governor can only be changed by editing /etc/cpu-performance.conf```

## Configuration
The default config can be found in this repo, and can be found at /etc/cpu-performance.conf if installed via ```makepkg -si```. Editing this file is the only way to control which governor is applied by the systemd service.

An additional file can be created at ~/.config/cpu-performance.conf 
This file will override the file at /etc/cpu-performance.conf if the command is run manually.

## Requirements

* Linux system with CPU frequency scaling (/sys/devices/system/cpu/cpu*/cpufreq/)

* Root privileges

* `bash` and `coreutils`

## Disclaimer
 This script assumes:

* All CPU cores are online and support the same governor

* You're intentionally overriding any default or distro-specific power management behavior

This is a personal project and far from perfect, free feel to use however you want.
