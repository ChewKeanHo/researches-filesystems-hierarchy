# `/sbin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical system administrators'
programs and applications for an operating system to function properly
without any mounting (e.g. when `/usr` is not mounted). This means it
can operate in `Single-User` mode.

Unlike `/bin`, only sysadmin and root users can access these programs.

The goal is to have minimum possible programs for the sysadmins to operate
including functionalities extension by mounting the `/usr` directory.

In certain UNIX-like operating system design, this directory can be a
symbolic link to `/usr/sbin` (System V.4, Debian, etc).

Generally, you **SHOULD ONLY** place administrative programs that are
very critical early on without conflicting with existing POSIX compliant
programs.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

All programs here are registered programs that are usable across all UNIX
and UNIX-like OSes (POSIX Compliant). Among them are:

```
shutdown - program to shutdown the operating system.
```

Optional programs (for robust functionalities) are:

```
fastboot - program to reboot the OS without checking the disk.
fasthalt - program to stop the OS without checking the disk.
fdisk    - program to configure partition table.
fsck     - program to check and repair a disk and partition.
fsck.*   - program(s) to check and repair specific disk and partition.
getty    - program to perform terminal robust configurations.
halt     - program to stop the OS.
ifconfig - program to configure a network interface.
init     - program to initialize the OS.
mkfs     - program to make filesystem format to a partition.
mkfs.*   - program to make specific filesystem format to a partition.
mkswap   - program to setup a swap area.
reboot   - program to reboot the OS.
route    - program to configure IP routing table.
swapon   - program to enable paging and swapping.
swapoff  - program to disable paging and swapping.
update   - program to flush filesystem periodically (daemon).
```
