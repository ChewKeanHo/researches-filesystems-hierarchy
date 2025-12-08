# `/var/tmp`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's temporary files and directory.
Unlike `/tmp` base directory, this temporary directory **get persisted** across
reboot (without deletion) enabling post booting forensic analytics use.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and after use to
avoid post-use blaming or corrupted data usage.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/var/
  tmp/
    trademark/
      product/
        ...

OR

/var/
  tmp/
    product/
      ...
```
