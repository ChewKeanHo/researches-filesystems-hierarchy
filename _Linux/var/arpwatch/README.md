# `/var/arpwatch`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `arpwatch` databases and
control files. Due to its processing nature, one **MUST** carefully work here to
prevent any data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications and `arpwatch` being used. In Red Hat Linux, it is by default
for arp spoofing monitoring.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Consult `arpwatch` manual when used.
