# `/var/named`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `bind` or `bind9` DNS
configuration files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the use of `bind`/`bind9`
in the OS.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Refer to `bind` or `bind9` manual.
