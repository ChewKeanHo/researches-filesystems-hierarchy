# `/var/run`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) files containing information
about the operating system (OS) since it was booted.

In certain UNIX-like OSes such as Debian Linux, this directory is symbolic
linked to `/run` instead.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.
