# `/lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing critical libraries used by the
critical executables and programs for an operating system to function
properly without any mounting (e.g. when `/usr` is not mounted). This
means it can operate in `Single-User` mode for BSD realm.

The goal is to have minimum possible libraries for the operating
system to operate properly including mounting `/usr` directory for
expanding its functionalities.

Generally, you **SHOULD ONLY** place libraries that are very critical
early on without conflicting with existing POSIX compliant libraries
files.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

All libraries here are POSIX compliant registered libraries that are
usable across all UNIX and UNIX-like OSes.

It is a practice to house the libraries files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/lib/
  trademark/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

# OR

/lib/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```

Optional layouts introduced by specific operating systems are:

```
# GNU+Linux
modules  - houses Linux kernel modules' library and configuration files.
```
