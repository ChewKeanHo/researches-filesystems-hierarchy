# `/usr/libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing OS distributor's supplied non-critical,
non-user, system-wide programs and applications for extending the operating
system's functionalities from full catalogue stage to complete stage. This
means it can operate in `Multi-User` mode in BSD realm.

Generally, you **SHOULD** place your programs and applications here which
will be available system-wide.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
