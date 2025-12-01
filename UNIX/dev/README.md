# `/dev`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system maps all the devices
(by `devfs` or `Linux kernel`) into the filesystem for
hardware-software interactions.

You **DEFINITELY SHOULD NOT** place anything here. Let the operating
system controls it entirely.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Based on operating systems engineering specification. Refer to their
documents for more info. For examples:

* Hard disk can be repesented as:
  * `/dev/sdX` in `GNU+Linux`; OR
  * `/dev/adaN` in `FreeBSD`.
* USB storage device can be represented as:
  * `/dev/sdX` in `GNU+Linux`; OR
  * `/dev/daN` in `FreeBSD`.
