# `/var`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) multi-purpose transient
variable data files like log files, data files, databases, etc.

Some data files are sharable while some are not. Do check the ownership and
access permissions before action.

Generally, you **SHOULD ONLY** place variable data files used by the programs
and applications here.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The first sub-directory layer is a list of function oriented (e.g. `log`,
`mail`, `lock`, `cache`, `tmp`, `crash`, `www`, `spool`, ...) directories. This
is defined by the OS' engineering specification itself.

Within the function oriented sub directory, it is a practice to house the
configuration files using `trademark` and `product` sub-directories
organization. This can significantly reduces the naming collision for common
names.

Here are the examples with and without using `trademark` directory:

```
/var/
  cache/
    trademark/
      product/
        icons/
          banner_1200x1200.svg
          ...
  log/
    trademark/
      product/
        access.log
        info.log
        ...
  ...

# OR

/var/
  cache/
    product/
      icons/
        banner_1200x1200.svg
        ...
  log/
    product/
      access.log
      info.log
      ...
  ...
```
