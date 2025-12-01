# `/root`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses root account data directory like
`/home/[USERNAME]` (`/home`). It is entirely **optional** and is
specifically designed for system administration works only.




## Common Files

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

[Common](/Common) directories structure is used for housing user-only
filesystems inside a `.local` sub-directory. The commonly seen structures
would be:

```
root/
  .local/
    bin/
    etc/
    var/
    ...
```

It is **NOT RECOMMENDED** to enable graphical user interface (GUI)
desktop management (DM) for the root account. However, if it is,
additional common directories are added as follows:

```
/root/
  Desktop/
  Documents/
  Downloads/
  Pictures/
  Videos/
  Public/
  Musics/
  ...
  .local/
    bin/
    etc/
    var/
    ...
```
