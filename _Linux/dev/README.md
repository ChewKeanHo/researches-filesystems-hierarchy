# `/dev`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing all device nodes (special files).

The goal is simple: the operating system (OS) maps all the device nodes by
kernel into the filesystem for hardware-software interactions.

You **DEFINITELY SHOULD NOT** place anything here. Let the OS controls it
entirely.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

You need to refer to your OS's documentations for device nodes definitions.
For examples:

* Hard disk and USB storages can be repesented as:
  * `/dev/sdX`
