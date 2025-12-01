# `sbin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is an output directory housing system administrators' readily
usable executable and programs. Unlike `bin`, only sysadmin or root
can have them as command. Conventional users will not be able to
access them except calling it from full path.

When a project is built, all the executable outputs including
Microsoft Windows' `.exe` binary files are placed here.

Unlike `bin`, only sysadmin and root users can access these programs.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support cross-compliations, it is advisable to use the `[OS]-[ARCH]`
filename suffix convention. For example:

```
myprogram_linux-amd64.elf
myprogram_linux-arm64.elf
myprogram_freebsd-amd64.elf
myprogram_freebsd-arm64.elf
myprogram_windows-amd64.exe
myprogram_windows-arm64.exe
...
```

File extension is optional but for consistency sake, it's best to include
them regardless of OSes.




## OS-Ready Executables

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

For OS-Ready executables, complying the above, it's best to either:

1. symbolic link into your program name (e.g.
   `$ ln -s sbin/myprogram_linux-amd64.elf sbin/myprogram`); OR
2. create a shell script (preferbly polygot script) as `sbin/myprogram` that
   smartly execute the correct program (`sbin/myprogram_linux-amd64.elf`).

The strategy depends on how the project is being managed and one knows how
to create a polygot shell script.
