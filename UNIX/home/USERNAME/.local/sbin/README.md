# `/home/USERNAME/.local/sbin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the user-specific directory housing user supplied non-critical
user-specific system administrators' programs and applications for
extending the operating system's functionalities from complete stage to
personalized stage. This means that executables in this directory only
appears specifically for this user.

Generally, you **SHOULD** place your own custom programs and applications
here. It will be made available only for you.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files with yours.
The second purpose is to facilitate a way to procure programs and
applications without using sysadmins or root account that affects the
entire operating system.

This directory **MUST NOT** have any sub-directory.

This directory is **entirely optional** as it serves as a clean design
structure.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
