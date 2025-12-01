# UNIX Filesystem Hierarchy Standard

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is UNIX specific Filesystem Hierarchy Standard (FHS) covering both
`Berkeley Software Distribution` (BSD) and UNIX-like operating system
like `GNU's Not Unix!` (GNU) + Linux operating system.




# Understanding The 4 Stages of Functionalities Extensions

UNIX operating systems generally go through 4 stages of functionalities
extensions:

1. **Critical & Minimal** - focuses on booting up the operating system
   upto the minimal point for further extension and rescue. This only
   uses tools from the Root (`/`) directory excluding any system
   directories mounting (e.g. `/usr`).
2. **Full Catalogue** - focuses on extending the operating system
   upto its full potentials. This access and extends tools from the
   mounted system directories (`/usr`).
3. **Complete** - focuses on extending the operating system further
   with user introduced system functionalities. This access and extends
   tools from user-introduced localized system directories (`/usr/local`).
   At this point, the operating system functionalities are now completed.
4. **Personalized** - focuses on extending the operating system's
   functionalities with user-only system directories
   (`/home/USERNAME/.local`). This stage can change from time-to-time
   based on the user-only configurations in his/her user-only system
   directory.




## The Root

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The root directory is the very foundational directory represented by `/`.
When root combines with [Common](/Common) FHS, you get a list of basic
functional directories as such:

```
/bin     - OS critical user utilities programs.
/etc     - OS critical configuration files and scripts.
/lib     - OS critical libraries used by `/bin` and `/sbin` programs.
/libexec - OS Critical system files not importable as libraries but not
           suitable for any users to call upon.
/sbin    - OS critical system administration programs.
/tmp     - OS temporary work files.
```

The root directory also has other critical system directories that provides
various system roles:

```
/boot      - OS critical bootloading component.
/dev       - OS mapped IO devices filesystems.
/media     - OS removable media like CDs, floppy disks, and portable disks.
/mnt       - temporary mountpoint for sysadmin and root user to deal with
             storage devices.
/usr       - OS User utilities, programs, and applications.
/var       - OS variable data directory like log, data, and spool files.
```

Then, the operating systems can specify its specific directories such as:

```
FreeBSD
-------
/net       - Automounted Network Area Storage (NAS) share mounting.
/rescue    - Statically linked programs for emergency recovery.


GNU+Linux
---------
/proc      - OS process files (optional).
/sys       - OS sysfs (optional). On Linux it's kernel info. On BSD, it's
             a symlinked to '/usr/src/sys'.
```




## Primary Objectives

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The primary objective of this layer is to bring the operating system's
critical component up and running with minimum resources before any
functionalities expansion including mounting and loading `/usr`
directory. This is known as `Single User` operating mode in FreeBSD
realm.

There are 2 possibilities:

* user use the operating system as it is (commonly seen in bare-metal
  embedded deployment like OpenWRT project); OR
* operating system expands to its full potentials by mount and load
  the `/usr` directory (common computing deployment).

You can explore each root layer's base directories in details. Once
done, head over to [`/usr`](/UNIX/usr) directory which is the second
layer for functionalities' expansions.
