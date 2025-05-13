# cpu-performance
A simple Bash script that sets the CPU governor to performance on all cores.

This is one of my first proper Bash scripts, mainly intended for personal use — but feel free to use or modify it if you find it helpful.
Just don’t expect anything too fancy (yet).

## What it does

It checks if the current CPU scaling governor is already set to performance. If not, it updates the governor for all CPU cores.
Requirements

* Linux system with cpufreq support (e.g., /sys/devices/system/cpu/cpu*/cpufreq/scaling_governor)

* Root privileges (via sudo, doas, or running as root)

* bash and basic coreutils

## Planned features

- [x] Basic functionality

- [x] PKGBUILD for Arch

- [ ] Optional systemd service for automatic application on boot

- [x] Cleaner handling of privilege escalation 

## Disclaimer

This script assumes:

* All CPU cores are online and have the same governor capabilities.

* You're okay with hard-setting the performance governor manually.

It’s a personal project, so expect some rough edges — but I’m using it daily.
