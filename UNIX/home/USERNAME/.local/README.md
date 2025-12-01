# `/home/USERNAME/.local`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all user-specific data directory. It houses
a [Common](/Common) filesystems specifically for this user only.

Depending on the operating system's engineering specification, this
directory can be entirely **optional**.

Programs **SHOULD NOT** assume any file or directory and always
perform safe query before use.




## Common File Structures

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

[Common](/Common) directories structure is used for housing user-specific
filesystems inside this directory. The commonly seen structures would be:

```
/home/
  [USERNAME]/
    .local/
      bin/
      etc/
      include/
      lib/
      libexec/
      sbin/
      var/
```

Then on graphical user interface (GUI) desktop management (DM), additional
common directories are added as follows:

```
/home/
  [USERNAME]/
    Desktop/
    Documents/
    Downloads/
    Musics/
    Pictures/
    Public/
    Videos/
    ...
    .local/
      bin/
      etc/
      include/
      lib/
      libexec/
      sbin/
      var/
```
