# `/boot/efi`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical bootloading programs, applications,
and configuration files to initialize the operating system (OS) using
Extensible Firmware Interface (EFI) like
Unified Extensible Firmware Interface (UEFI). This partition has specific
rules where it **MUST** be `FAT32` format with `MSDOS_SUPER_MAGIC` and
boot flag enabled.

The goal is simple: boot up the supported OS with hardware-software
matching boot configurations, initialize kernel until the OS' initializers
takes over to achieve `Minimal & Critical` functionalities stage.

Generally, you **SHOULD ONLY** place EFI bootloading programs and their
configuration files inside this directory. Due to early boot sequences are
hardware specific which can be very complex yet critical, this directory is
often housing the bootloading artifacts reliably and systematically generated
from the higher OS' functionalities.

This directory is the legacy mount point for the EFI boot partition. In
some UNIX-Like OS notably SystemD implementations, this directory is no longer
used and is replaced by `/efi` or `/boot` entirely instead. According to their
specifications, tools will look for this directory as a fallback after searching
for `/efi`.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

EFI has strict filename requirements located at the root directory of this
partition such that:

```
amd64   /EFI/BOOT/BOOTX64.EFI
arm     /EFI/BOOT/BOOTARM.EFI
arm64   /EFI/BOOT/BOOTAA64.EFI
i386    /EFI/BOOT/BOOTIA32.EFI
riscv   /EFI/BOOT/BOOTRISCV64.EFI
```

Then, the OS distributor provided UEFI bootloader chainloads from the
standardized loader into their specific loaders such as but not limited to:

```
# GNU+Linux
/EFI/BOOT/GRUBX64.efi
/EFI/BOOT/SHIMX64.efi
/EFI/BOOT/FBX64.efi
...
```
