# `/usr/local`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing all user custom supplied non-user,
system-only, critical, programs; applications; and files to extend its
functionalities from *Full Catalogue* stage to *Complete* stage. This means it
can operate in `Multi-Users` mode.

The goal is to extend the OS functionalities upto its complete user's
system-wide customization level. At this point, the OS should be fully operable
as configured by the user.

Generally, you **SHOULD AND STRONGLY ENCOURAGED** to place your custom supplied
programs, applications, and files here. The sole reason with the split between
`/usr` and `/usr/local` is to ensure you **DO NOT INTERFERE** with your OS'
distributor installed packages (they are in `/usr`) and allows them to smoothly
update the OS from time-to-time.




## The Localized UNIX System Resources (`usr/local`) Directory

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The `/usr/local` directory is one of the foundational directory for completing
the entire UNIX operating system's functionalities. When `/usr/local` combines
with the [Common](/Common) FHS, you get a list of basic functional directories
as such:

```
/usr/local/bin     - user supplied utilities programs and applications.
/usr/local/etc     - user supplied configuration files.
/usr/local/lib     - user supplied libraries used by non-critical programs
                     and applications.
/usr/local/sbin    - user supplied non-critical system administration
                     programs and applications.
/usr/local/share   - user supplied architecture independent files.
/usr/local/src     - user supplied source files.
/usr/local/tmp     - user supplied content temporary workspaces.
```

The `/usr/local` directory also has other critical system directories that
provide various system roles:

```
/usr/local/include - user supplied include files (e.g. c header files).
/usr/local/libexec - user supplied system daemons and system utilities executed
                     by other programs and applications.
```




## Primary Objectives

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The primary objective of this layer is to facilitates system-wide user
customizations for the OS without tempering the critical or the full layers
of system software. This isolation enables easier packages distribution
management free from tempering while providing a safe space for users to deal
with their unpredictable software installations and configurations.

Anything placed here will be available to all users system-wide and specific
to this operating system. Hence, it has the name `local`.

Feel free to explore all the sub-directories. When it's done. Head over
to [/home/USERNAME/.local](/UNIX/home/USERNAME/.local) for user-specific
filesystem layers.
