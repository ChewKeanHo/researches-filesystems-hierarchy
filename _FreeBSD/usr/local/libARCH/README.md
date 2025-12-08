# `/usr/libARCH`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied, non-critical,
CPU-architecture specific libraries files to extend its functionalities from
*Full Catalogue* stage to *Complete* stage and supporting cross-architectures
operations (e.g. multi-arch boot) and compilations (e.g. cross-compilation).
This means it can operate in `Multi-User` mode. Example: `/usr/local/lib32` for
32-bits CPU architecture library files in a 64-bit CPU architecture operating
system (OS).

The goal is to extend the OS' functionalities to its complete form while
supporting cross-architectures operations in the same OS. In this stage, the OS
can operate as per its distributor's engineering specifications and customized
as per user.

Also, depending on the OS engineering specifictions, this directory is
**ENTIRELY OPTIONAL AND GETTING REMOVED OVERTIME** (e.g. some OSes use
`[OS]-[ARCH]` filename notation which makes no sense to split the
`/usr/local/lib` itself). As of year 2025, a lot of OSes are dropping 32-bits
supports making `lib32` directories obselete.

All libraries files here are available to all users.

Generally, when this directory is used, you **SHOULD AND STRONGLY ENCOURAGED**
to place your distributor's unregistered library files here (e.g. from a custom
package elsewhere). It will be available to all users system-wide.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory for 32-bits
libraries (`lib32`):

```
/usr/
  local/
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
  local/
    lib32/
      product/
        lib1.so
        lib1_freebsd-i386.so
        kernel8.ko
        kernel8_freebsd-i386.ko
        ...
```
