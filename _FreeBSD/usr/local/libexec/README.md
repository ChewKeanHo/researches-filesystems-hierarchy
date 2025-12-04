# `/usr/local/libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied non-user,
system-only, critical, programs and applications to extend its functionalities
from *Full Catalogue* stage to *Complete* stage. This means it can operate in
`Multi-Users` mode.

The goal is to extend the OS functionalities upto its complete user's
system-wide customization level. At this point, the OS should be fully operable
as configured by the user.

All programs and applications here are **NOT AVAILABLE** as callable commands
to any users. Sysadmins (users in `wheel` group) and root account must execute
them via full pathing manually.

Generally, you **SHOULD AND STRONGLY ENCOURAGED** to place your custom supplied
programs and applications here. The sole reason with the split between
`/usr/libexec` and `/usr/local/libexec` is to ensure you **DO NOT** interfere
with your OS' distributor installed packages (they are in `/usr/libexec`) and
allows them to smoothly update the OS from time-to-time.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support cross-compliations, it is advisable to use the `[OS]-[ARCH]` filename
suffix convention. For example:

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

Then for common name, it is best to either:

1. symbolic link into your program name (e.g.
   `$ ln -s libexec/myprogram_linux-amd64.elf libexec/myprogram`); OR
2. create a shell script (preferbly polygot script) as `libexec/myprogram`
   that smartly execute the correct program
   (`libexec/myprogram_linux-amd64.elf`).

This strategy depends on how the project is being managed and one knows how to
create a polygot shell script.
