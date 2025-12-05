# `/media`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing all mounted removable media such as but not
limited to CD, floppy disks, USB storage devices, external disks, decrypted
partitions, or volume managed partitions.

Each first-level sub-directory holds a mounted device.

The rationale is rather than queue-and-hold the `/mnt` directory per device,
`/media` caters for one or more devices. This made `/mnt` a temporary mounting
directory only for sysadmins and root user to debug mountable transactions.

In some operating systems (OS) like Red Hat or Fedora, this directory was
replaced as `/var/run/media` directory instead.

You can place files or directory in the media directory here in accordance to
the designated filesystem ownership and permissions.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Each sub-directory holds a mounted device be it physical or virtual
(e.g. decrypted partitions). The first sub-directory layer is recommended
to use the device's hardware label for identifications. Otherwise, the
hardware UUID is a good fallback.
