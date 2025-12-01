# `/usr`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's distributor supplied
non-critical programs, applications, and files. It is sharable but
read-only for preventing unwanted temperment.

The goal is to expand the operating system's functionalities from
minimum critical stage to full catalogue stage.




## The UNIX System Resources (`usr`) Directory

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The `/usr` directory is one of the very foundational directory for
extending the base UNIX operating system's functionalities. When
`/usr` combines with [Common](/Common) FHS, you get a list of basic
functional directories as such:

```
/usr/bin     - OS distributor's supplied utilities programs and applications.
/usr/lib     - OS distributor's supplied libraries used by non-critical
               programs and applications.
/usr/libexec - OS distributor's supplied system daemons and system
               utilities executed by other programs and applications.
/usr/sbin    - OS distributor's supplied non-critical system administration
               programs and applications.
/usr/share   - OS distributor's supplied architecture independent files.
/usr/src     - OS distributor's supplied source files.
```

* `/usr/etc` is not available as `/etc` is being used instead.
* `/usr/tmp` is not available as `/tmp` is being used instead.

The `/usr` directory also has other critical system directories that provides
various system roles:

```
/usr/include - OS distributor's supplied include files (e.g. c header files).
/usr/local   - local user-installed system-wide utilities programs and
               applications.
```

Then, the operating systems can specify its specific directories such as:

```
FreeBSD
-------
/usr/libdata  - OS distributor's supplied miscellaneous utility data files.
/usr/ports    - The FreeBSD Ports Collection (optional).
```




## Primary Objectives

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The primary objective of this layer is to extend the operating system's
functionalities to full catalogue stage. This is known as `Multi-User`
operating mode in FreeBSD realm.

You can explore each `/usr` layer's base directories in details. Once
done, head over to [`/usr/local`](/UNIX/usr/local) directory which is
the last system-level layer for functionalities' expansions.
