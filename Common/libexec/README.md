# `libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is an output directory housing readily usable executable programs
and applications but not suitable for any user to run at will
(e.g. daemon server).

Unlike `bin` or `sbin`, only sysadmin and root users can calling the
full path to the program or application. They will not be avilable as
a straightforward command.

When a project is built, all the executable outputs including
Microsoft Windows' `.exe` binary files are placed here.




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
   `$ ln -s libexec/myprogram_linux-amd64.elf libexec/myprogram`); OR
2. create a shell script (preferbly polygot script) as `libexec/myprogram`
   that smartly execute the correct program
   (`libexec/myprogram_linux-amd64.elf`).

The strategy depends on how the project is being managed and one knows how
to create a polygot shell script.
