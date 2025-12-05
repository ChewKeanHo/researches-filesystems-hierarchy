# `/home/USERNAME/.fonts`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is a functional directory used for user-only font files. Most graphical
user interface (GUI) desktop manager (DM) will create this directory as it is.

Depending on the operating system's engineering specification, this directory
can be **ENTIRELY OPTIONAL**.

Programs **SHOULD NOT** assume any file or directory and always perform safe
query before use.

For complying with the `.local` FHS, It is symlinked to `.local/share/fonts`.
This can easily be done by the following commands:

```
# cd ~
$ mkdir -p ./.local/share
$ if [ -d .fonts ]; then do mv ".fonts" "./.local/share/fonts"; done
$ rm -rf .fonts
$ sync .
$ ln -s .fonts .local/share/fonts
```
