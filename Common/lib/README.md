# `lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is an output directory housing readily importable library files.

When a project is built, all the libraries' outputs including
Microsoft Windows' `.dll` binary files are placed here.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support cross-compliations, it is advisable to use the `[OS]-[ARCH]`
filename suffix convention. For example:

```
myprogram_linux-amd64.a
myprogram_linux-arm64.lib
myprogram_freebsd-amd64.so
myprogram_freebsd-arm64.so
myprogram_windows-amd64.dll
myprogram_windows-arm64.dll
...
```

File extension is **always** required to uniquely identify them. Per
standards, it is as follows:

```
.lib, .a             - UNIX userspace static archived file
.lib, .so            - UNIX userspace shared library file
.dll                 - Microsoft Windows userspace library file

.ko                  - UNIX kernel library/module file
```
