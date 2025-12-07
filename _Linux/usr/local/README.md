# `/usr/local`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) user supplied,
system-wide available custom programs, applications and files for extending its
functionalities from *Full Catalogue* stage to *Complete* stage. This means it
can operate in `Full Mode`.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as designed by its distributor and customized by the
user. The sole reason with the split between `/usr` and `/usr/local` is to
ensure any user **DOES NOT** interfere with your OS' distributor installed
packages (they are in `/` and `/usr` levels) allowing them to update the OS
seamlessly and smoothly across time. This is why every setup here is specfically
only for this host.

On some Linux UNIX-like OSs notably SystemD and UAPI, this directory is
**UNAVAILABLE** as they shifted all user customizations entirely into user home
directory with dedicated software like rootless package manager implementations
like Flatpak (`$ flatpak --user install`) instead.

All programs and applications here are available to all users.

Generally, you **SHOULD AND STRONGLY ENCOURAGED** to place your distributor's
unregistered (as in you bring your own custom packages) programs, applications,
and files here. If you wish to place user-only (only for 1 specific user), you
should use `/home/[YOUR_USERNAME]/.local` filesystem directory instead.




## The Localized UNIX System Resources (`usr/local`) Directory

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The `/usr/local` directory is one of the foundational directory for completing
the entire OS' functionalities. When `/usr/local` combines with the
[Common](/Common) FHS, you get a list of basic functional directories as such:

```
/usr/local/bin     - user supplied utilities programs and applications.
/usr/local/etc     - user supplied configuration files.
/usr/local/lib     - user supplied libraries used by user customized
                     non-critical programs and applications.
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

Then, the OS can specify its specific directories such as:

```
Redhat Linux
------------
/usr/local/libexec  - user supplied system daemons and system utilities executed
                      by other programs and applications.
```

Feel free to explore all the sub-directories. When it's done. Head over
to [/home/USERNAME/.local](/_Linux/home/USERNAME/.local) for the user-only
filesystem layer.
