# `sbin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses readily usable executables programs and
applications **ONLY FOR system administrators and root account**. They are
designed to be as readily usable terminal command. Conventional users should not
be able to access them except calling it from full path.

When a project is built, all the executable outputs including
Microsoft Windows' `.exe` binary files are placed here.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.

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
