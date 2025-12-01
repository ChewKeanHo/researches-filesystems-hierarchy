# `/home/USERNAME/.fonts`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is a **deprecated** functional directory used for font data purposes.
It is replaced by `.local/share/fonts` which is FHS compliant.

Modern practices makes symbolic link of this directory pointing to the
new directory.

```
# cd ~
$ rm -rf .fonts
$ ln -s .fonts .local/share/fonts
```

Depending on the operating system's engineering specification, this
directory can be entirely **optional**.

Programs **SHOULD NOT** assume any file or directory and always
perform safe query before use.
