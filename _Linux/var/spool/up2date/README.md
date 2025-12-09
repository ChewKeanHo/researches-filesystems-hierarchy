# `/var/spool/up2date`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) `.rpm` rollback data files
for `rpm`.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on OS type and `rpm` package
managers being installed in the OS. Example, for Red Hat Linux, Fedora, and
similar types of OSes, this directory is heavily used.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Refer `rpm` or `rpmbuild` manual.
