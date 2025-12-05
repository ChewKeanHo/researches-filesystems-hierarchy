# `src`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all readily importable and usable source files.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
src/
  trademark/
    product1/
      lib1.c
      lib1_freebsd-amd64.c
      kernel8.c
      kernel8_freebsd-amd64.c
      ...

OR

src/
  product/
    lib1.c
    lib1_freebsd-amd64.c
    kernel8.c
    kernel8_freebsd-amd64.c
    ...
```




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support cross-compliations, it is advisable to use the `[OS]-[ARCH]` filename
suffix convention to denote a platform-specific source file while without it
implicitly implies it is applicable to all. For example:

```
myprogram.c                              # this applies to all
myprogram_freebsd-amd64.c
myprogram_freebsd-arm64.c
myprogram_linux-amd64.c
myprogram_linux-arm64.c
myprogram_windows-amd64.c
myprogram_windows-arm64.c
module_linux-amd64.c
module_linux-arm64.c
module_freebsd-amd64.c
module_freebsd-arm64.c
...
```

File extension is **ALWAYS REQUIRED** for type identifications among all the
libraries files.
