# `/home/USERNAME/.cache`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is a **deprecated** functional directory used for programs and
applications data caching purposes. It is replaced by `.local/var/cache`
which is FHS compliant.

Modern practices makes symbolic link of this directory pointing to the
new directory.

```
# cd ~
$ rm -rf .cache
$ ln -s .cache .local/var/cache
```

Depending on the operating system's engineering specification, this
directory can be entirely **optional**.

Programs **SHOULD NOT** assume any file or directory and always
perform safe query before use.
