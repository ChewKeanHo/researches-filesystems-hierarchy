# `/proc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the **deprecated** base directory housing all process nodes
(special files). This directory appears only when absolutely needed (e.g.
FreeBSD enabling Linux inter-compatibility layer which requires `/proc` to
exist). On Linux, it is always exist for backward compatibilities purposes.

The goal is simple: allow OS process filesystems (e.g. `procfs`) to map
every process files into filesystems for use.

You **SHOULD NOT** place anything here.
