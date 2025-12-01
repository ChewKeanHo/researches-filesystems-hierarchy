# `log`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all production log files from a service.

Due to its processing nature, one **MUST** carefully work here to
prevent any data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and
**SHOULD** always practice safe-querying before use.

Also, it is recommended to rotate the log files before use (e.g.
by datetime or id number increment) to avoid post-use blaming or
data loss.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `log`** as it represent the
entire logging service.

The file extension can either be `.txt` or `.log`.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/var/
  log/
    trademark/
      product/
        20251201_info.log
        20251202_info.log
        ...

OR

/var/
  log/
    product/
      20251201_info.log
      20251202_info.log
      ...
```
