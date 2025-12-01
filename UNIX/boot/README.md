# `/boot`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical boot configuration files and
bootloading programs.

The goal is simple: boot up the operating system by hardware-software
matching configurations and initialize kernel until the operating system
is usable with minimal critical functionalities. This is known as
`Single-User` mode in BSD realm.

Generally, you **SHOULD ONLY** place bootloading programs and their
configuration files inside this directory. Due to early boot sequences are
hardware specific and can be very complex yet critical, this directory
often housing the boot artifacts generated from the higher operating
operating system's higher functionalities.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

No restrictions and it all depends on the chosen bootloader (e.g.
hardware boot specifications, strict file names and pathing locations, etc).
