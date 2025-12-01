# `/usr/local/tmp`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all users' custom installed system-wide programs'
and applications' temporary files and directory. On many operating
systems engineering design, this directory gets cleared and cleaned on
boot up. Any `/usr/local` temporary files should use placed into this
directory instead of the `/tmp` base operating system directory.

In some operating systems engineering design, this directory can be
unavailable for use.

Programs **SHOULD NOT** assume any file and directory here and should
always practice safe-querying before use.

Also, it is recommended to clean up the temporary files before and
after use to avoid post-use blaming or corrupted data usage.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    tmp/
      trademark/
        product/
        ...

OR

/usr/
  local/
    tmp/
      product/
      ...
```
