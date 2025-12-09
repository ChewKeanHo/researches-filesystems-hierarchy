# `/var/gdm`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) GNOME data files. Due to its
processing nature, one **MUST** carefully work here to prevent any data
poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications. In Red Hat Linux, it is being used similar to FreeBSD.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Refer GNOME Desktop Manager's manual. In some UNIX-like OSes, this directory is
no longer being used but using `/var/lib/gdm` as the direct replacement.
