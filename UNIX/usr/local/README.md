# `/usr/local`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all users' custom installed non-critical
system-wide programs, applications, and files. The directory is
sharable but read-only for preventing unwanted temperment.

The goal is to expand the operating system's functionalities from
full catalogue stage into its complete setup stage.




## The Localized UNIX System Resources (`usr/local`) Directory

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The `/usr/local` directory is one of the foundational directory for
completing the entire UNIX operating system's functionalities. When
`/usr/local` combines with [Common](/Common) FHS, you get a list of
basic functional directories as such:

```
/usr/local/bin     - user supplied utilities programs and applications.
/usr/local/etc     - user supplied configuration files.
/usr/local/lib     - user supplied libraries used by non-critical programs
                     and applications.
/usr/local/libexec - user supplied daemons and utilities executed by other
                     programs and applications.
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
```




## Primary Objectives

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The primary objective of this layer is to facilitates system-wide user
customizations of the UNIX operating system without tempering the critical
and full layers of system software. This isolation enables easier packages
distribution management and provides a safe space for users to deal with
their unstable software.

Anything placed here will be available to all users system-wide and specific
to this operating system. Hence, it has the name `local`.

Feel free to explore all the sub-directories. When it's done. Head over
to [/home/USERNAME/.local](/UNIX/home/USERNAME/.local) for user-specific
filesystem layers.
