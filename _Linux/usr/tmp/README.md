# `/usr/tmp`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses the operating system's (OS) `/usr`'s temporary files and
directory. On some UNIX-like OSes like Red Hat Linux and Fedora, this directory
is replacing `/tmp` directory. Also, this directory is linked to `/var/tmp`
temporary directory. In short, if this directory is used, then `/tmp` should
not be available.

On many OSes design, this directory gets cleared and cleaned on boot up.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.

The details are the same as [/tmp](/_Linux/tmp).
