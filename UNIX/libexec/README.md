# `/libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical non-user programs and
applications (e.g. daemon server) for the operating system to function
properly without any mounting (e.g. when `/usr` is not mounted). This
means it can operate in `Single-User` mode in BSD realm.

The goal is to have minimum possible programs and applications enough
to function including extending its functionalities by mounting `/usr`
directory.

Generally, you **SHOULD ONLY** place programs that are very critical at
early booting stage without conflicting with existing POSIX compliant
programs.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
