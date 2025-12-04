# `/lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for only critical libraries used by
critical programs and applications of an operating system (OS) to
function properly and minimally without any mounting (e.g. `/usr` is not
mounted or absent). This means it can operate in `Single-User` mode in
BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimally sufficient libraries to perform critical
tasks like mounting `/usr` UNIX System Resources directory for
functionalities extension, performing self-rescue, or straight up
operational in resources constraint environment such as but not limited
to OpenWRT embedded router.

All libraries here are available to all users.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr`
is always being mounted and hardware are no longer seeing performance
differences between `/` and `/usr`, this directory is being symbolic linked
to `/usr/lib` instead; unifying both directories. This reduces the separation
complexities while simplifying the package managements to target `/usr/lib`
only.

Generally, you **SHOULD ONLY** place programs that are very critical at
early booting stage without conflicting with existing POSIX compliant
programs. In the case of `/lib` being symbolic linked to `/usr/lib`, you
**SHOULD NOT** place anything here and instead use `/usr/lib` exclusively.

This directory **MUST NOT** have any sub-directory.




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

Optional layouts introduced by some specific operating systems are:

```
# GNU+Linux
modules  - houses Linux kernel modules' library and configuration files.
```
