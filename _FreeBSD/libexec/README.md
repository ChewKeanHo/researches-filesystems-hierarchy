# `/libexec`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing non-user, system-only, critical, programs
and applications of an operating system (OS) to function properly and minimally
without any mounting (e.g. `/usr` is not mounted or absent). This means it can
operate in `Single-User` mode.

The goal is to have minimally sufficient programs enough for basic
functionalities to perfrom critical tasks like mounting `/usr` UNIX System
Resources directory for functionalities extension, performing self-rescue, or
straight up operational in resources constraint environment such as but not
limited to OpenWRT embedded router.

All programs and applications here are **NOT AVAILABLE** as callable commands to
any users. Sysadmins (users in `wheel` group) and root account must execute them
via full filepath manually.

In some UNIX-like OSes like Oracle's Solaris (first to transform back in 2012)
and Red Hat's Fedora (second to transform back in 2023), due to `/usr` is always
being mounted and hardware are no longer seeing performance differences between
`/` and `/usr`, this directory is being symbolic linked to `/usr/libexec`
instead; unifying both directories. This reduces the separation complexities
while simplifying the package managements to target `/usr/libexec` only.
**FreeBSD however, have not seen to perform such implementation yet.**

Generally, you **SHOULD ONLY** place programs that are very critical at
early booting stage without conflicting with existing POSIX compliant
programs.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Otherwise, to support cross-compliations, it is advisable to use the
`[OS]-[ARCH]` filename suffix convention. For example:

```
myprogram_linux-amd64.elf
myprogram_linux-arm64.elf
myprogram_freebsd-amd64.elf
myprogram_freebsd-arm64.elf
myprogram_windows-amd64.exe
myprogram_windows-arm64.exe
...
```

File extension is optional but for consistency sake, it's best to include them
regardless of OSes.

Then for common name, it is best to either:

1. symbolic link into your program name (e.g.
   `$ ln -s libexec/myprogram_linux-amd64.elf libexec/myprogram`); OR
2. create a shell script (preferbly polygot script) as `libexec/myprogram`
   that smartly execute the correct program
   (`libexec/myprogram_linux-amd64.elf`).

This strategy depends on how the project is being managed and one knows how to
create a polygot shell script.
