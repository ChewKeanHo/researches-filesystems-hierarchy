# `/usr/sbin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) distributor
supplied, non-critical, system administrators (sysadmins) only programs and
applications the OS to extend the OS functionalities from *Minimal & Critical*
stage to *Full Catalogue* stage. This means it can operate in `Full Mode`.

The goal is to extend the OS' functionalities for distributor level full
functionalities. At this stage, the OS can operate as per its distributor's
engineering specifications.

All programs and applications here are **ONLY** available to sysadmins and root
account.

Generally, you **SHOULD ONLY** place distributor's registered programs here. For
your own locally build or custom sourced packages, you should place them inside
`/usr/local/sbin` directory instead.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
