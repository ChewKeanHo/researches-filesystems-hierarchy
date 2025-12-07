# `/usr/libARCH`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) distributor
supplied, non-critical CPU-architecture specific library files for extending the
OS functionalities from *Critical & Minimal* stage to *Full Catalogue* stage and
supporting cross-architectures operations (e.g. multi-arch boot) and
compilations (e.g. cross-compilation). This means it can operate in `Multi-User`
mode in BSD realm or `Full Mode` in Linux realm. Example: `/usr/lib32` for
32-bits CPU architecture library files in a 64-bit CPU architecture OS.

The goal is to extend the OS' functionalities for distributor level full
functionalities while supporting cross-compilation across CPU-architectures in
the same OS. At this stage, the OS can operate as per its distributor's
engineering specifications.

Depending on the OS engineering specifictions, this directory is
**ENTIRELY OPTIONAL AND GETTING REMOVED OVERTIME** (e.g. some OSes use
`[OS]-[ARCH]` filename notation which makes no sense to split the `/usr/lib`
itself). As of year 2025, a lot of OSes are dropping 32-bits supports making
`lib32` directories obselete.

All files here are available to all users.

Generally, you **SHOULD ONLY** place distributor's registered files here. For
your own locally build or custom sourced packages, you should place them inside
`/usr/local/libARCH` directory instead.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory for 32-bits
libraries (`lib32`):

```
/usr/
  lib32/
    trademark/
      product/
        lib1.so
        lib1_freebsd-i386.so
        kernel8.ko
        kernel8_freebsd-i386.ko
        ...

# OR

/usr/
  lib32/
    product/
      lib1.so
      lib1_freebsd-i386.so
      kernel8.ko
      kernel8_freebsd-i386.ko
      ...
```
