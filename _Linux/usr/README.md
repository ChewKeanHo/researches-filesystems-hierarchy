# `/usr`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating systems' (OS) distributor supplied
non-critical programs, applications, and files. It is sharable but read-only for
preventing unwanted temperment.

The goal is to expand the OS' functionalities from *Minimum & Critical* stage to
*Full Catalogue* stage.




## The UNIX System Resources (`usr`) Directory

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The `/usr` directory is one of the very foundational directory for extending the
base UNIX OS' functionalities. When `/usr` combines with the [Common](/Common)
filesystems, you get a list of basic functional directories as such:

```
/usr/bin           - OS distributor's supplied utilities programs and
                     applications.
/usr/lib           - OS distributor's supplied libraries used by non-critical
                     programs and applications.
/usr/sbin          - OS distributor's supplied non-critical system
                     administration programs and applications.
/usr/share         - OS distributor's supplied architecture independent files.
/usr/src           - OS distributor's supplied source files.
```

* `/usr/etc` is generally unavailable as `/etc` is being used instead. However,
  in some UNIX-like OS like Red Hat Linux, it is available for scoping down
  distributor supplied configuration files.
* `/usr/tmp` is generally unavailable as `/tmp` is being used instead. However,
  in some UNIX-like OS like Red Hat Linux, it is available for replacing the
  `/tmp` directory.

The `/usr` directory also has other critical system directories that provides
various system roles:

```
/usr/include       - OS distributor's supplied include files (e.g. c header
                     files).
/usr/local         - local user-installed system-wide utilities programs and
                     applications.
```

Then, the OSes can specify its specific directories such as:

```
Red Hat Linux
-------------
/usr/etc           - OS distributor's supplied configuration files.
/usr/kerberos      - OS distributor's Kerberos-related binaries and files.
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
/usr/tmp           - OS distributor's "/usr" temporary files directory.


SystemD
-------
/usr/share/factory - OS distributor's default configurations and data files for
                     factory reset.

UAPI Linux
----------
/usr/libexec       - OS distributor's supplied system daemons and system
                     utilities executed by other programs and applications.
```




## Primary Objectives

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The primary objective of this layer is to extend the OS's functionalities.

You can explore each `/usr` layer's base directories in details. Once done, head
over to [`/usr/local`](/_Linux/usr/local) directory which is the last
system-level layer for functionalities' expansions.
