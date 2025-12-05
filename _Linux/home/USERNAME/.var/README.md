# `/home/USERNAME/.var`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is a functional directory used for user-only programs and applications
transient data storage. Most graphical user interface (GUI) desktop manager (DM)
will create this directory as it is.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

For complying with the `.local` FHS, It is symlinked to `.local/var`. This can
easily be done by the following commands:

```
# cd ~
$ mkdir -p ./.local/var
$ if [ -d .var ]; then do mv .var/* ./.local/var/.; done
$ rm -rf .var
$ sync .
$ ln -s .var .local/var
```
