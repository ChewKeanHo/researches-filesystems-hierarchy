# `/home/USERNAME`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all user level data directory.

Depending on the operating system's engineering specification, this
directory can be entirely **optional**.

Programs **SHOULD NOT** assume any file or directory and always
perform safe query before use.




## Common File Structures

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

[Common](/Common) directories structure is used for housing user-only
filesystems inside a `.local` sub-directory. The commonly seen structures
would be:

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
      share/
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
    Pictures/
    Videos/
    Public/
    Musics/
    .cache -> .local/var/cache
    .var -> .local/var
    .config -> .local/etc
    .fonts -> .local/share/fonts
    ...
    .local/
      bin/
      etc/
      include/
      lib/
      libexec/
      sbin/
      share/
      var/
```
