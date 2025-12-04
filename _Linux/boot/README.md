# `/boot`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical bootloading programs, applications,
and configuration files to initialize the operating system (OS).

The goal is simple: boot up the operating system with hardware-software
matching boot configurations, initialize kernel until the OS' initializers
takes over to achieve `Minimal & Critical` functionalities stage.

Generally, you **SHOULD ONLY** place bootloading programs and their
configuration files inside this directory. Due to early boot sequences are
hardware specific which can be very complex yet critical, this directory is
often housing the bootloading artifacts reliably and systematically generated
from the higher OS' functionalities.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

No restrictions. It is all depending on the chosen bootloader (e.g. `U-Boot`,
`Grub`, etc), hardware, firmware, etc). Some bootloaders have strict partitions
setup, strict file names and pathing, stricts locations, and etc.
