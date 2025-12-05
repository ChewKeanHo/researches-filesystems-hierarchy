# `lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses all readily importable library files.

When a project is built, all the libraries' outputs including Microsoft Windows'
`.dll` binary files are placed here.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
lib/
  trademark/
    product/
      lib1.so
      lib1_freebsd-amd64.so
      kernel8.ko
      kernel8_freebsd-amd64.ko
      ...

OR

lib/
  product/
    lib1.so
    lib1_freebsd-amd64.so
    kernel8.ko
    kernel8_freebsd-amd64.ko
    ...
```




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support cross-compliations, it is advisable to use the `[OS]-[ARCH]`
filename suffix convention. For example:

```
myprogram_linux-amd64.a
myprogram_linux-arm64.a
module_linux-amd64.ko
module_linux-arm64.ko
myprogram_freebsd-amd64.so
myprogram_freebsd-arm64.so
module_freebsd-amd64.ko
module_freebsd-arm64.ko
myprogram_windows-amd64.dll
myprogram_windows-arm64.dll
...
```

File extension is **ALWAYS REQUIRED** for type identifications among all the
libraries files. Per standards, known functional file extensions are as
follows:

```
.dll  - Microsoft Windows userspace library file
.a    - UNIX userspace static archived file
.so   - UNIX userspace shared library file
.ko   - UNIX kernel library/module file
```
