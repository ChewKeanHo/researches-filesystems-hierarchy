# `/sys`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing all kernel, devices, drivers, and
process nodes (special files) for Linux kernel.

The goal is simple: allowing Linux kernel to map its control surfaces
into the filesystems for use.

You **DEFINITELY SHOULD NOT** place anything here. Let the Linux kernel
takes full control over the directory.
