# `log`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all production log files from a service.

Due to its processing nature, one **MUST** carefully work here to
prevent any data poisoning or losses.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `log`** as it represent the
entire logging service.

The file extension can either be `.txt` or `.log`.
