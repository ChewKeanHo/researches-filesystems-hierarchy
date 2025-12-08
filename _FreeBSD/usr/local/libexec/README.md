# `/usr/local/libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied, non-critical,
non-user system-only programs and applications to extend its functionalities
from *Full Catalogue* stage to *Complete* stage. This means it can operate in
`Multi-User` mode.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as per its distributor's engineering specifications
and customized as per user.

All programs and applications here are **NOT AVAILABLE** as callable commands to
any user. Sysadmins (users in `wheel` group) and root account must execute them
via full filepath manually.

Generally, you **SHOULD AND STRONGLY ENCOURAGED** to place your distributor's
unregistered programs here (e.g. from a custom package elsewhere). It will be
available to all users system-wide.

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
