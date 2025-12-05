# `/home/USERNAME`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all user level data directory.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.




## File Structures

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

When this directory combines with [Common](/Common) directories structure,
it houses user-only specific filesystems on top of the operating system (OS),
personalized it just for this user. The combination happens inside a `.local`
sub-directory of this directory. The commonly seen structures would be:

```
/home/
  [USERNAME]/
    .local/
      bin/
      etc/
      include/
      lib/
      sbin/
      share/
      var/
```

Then, if the OS has graphical user interface (GUI) desktop management (DM)
supports, this directory is usually further combined with [User](/User)
filesystems, yielding additional common directories as follows:

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
      sbin/
      share/
      var/
```

For this research, this project only works with the functional directories from
both combinations.
