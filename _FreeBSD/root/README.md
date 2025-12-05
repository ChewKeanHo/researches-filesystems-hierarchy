# `/root`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses root account's data directory. The structure is the same
as [/home/USERNAME](/_FreeBSD/home/USERNAME) directory.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.
