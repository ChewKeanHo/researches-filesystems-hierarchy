# `/var/spool/mailman`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `mailman` mailer spooling data
files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on `mailman` installed in the
OS.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Refer to `mailman` manual.
