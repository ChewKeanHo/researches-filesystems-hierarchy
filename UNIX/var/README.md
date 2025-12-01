# `/var`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating systems' multi-purpose variable
data files like log files, data files, databases, etc.

Some data files are sharable while some are not.

Generally, you **SHOULD ONLY** place variable data files used by the
programs and applications here.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The first sub-directory layer is function oriented (e.g. `log`,
`mail`, `lock`, `cache`, `tmp`, `crash`, `www`, ...). This is defined by
the operating system's engineering specification.

Within the function oriented sub directory, it is a practice to house
the configuration files using `trademark` and `product` sub-directories
organization. This can significantly reduces the naming collision for
common names.

The use of `.d` configuration directory strategy reduces the
configuration complexities by keeping 1 configuration for 1 file.

Here are the examples with and without using `trademark` directory:

```
/var/
  log/
    trademark/
      product/
        access.log
        info.log
        ...
  cache/
    trademark/
      product/
        settings.d/
          setting1.conf
          setting2.conf
          ...
        icons/
          banner_1200x1200.svg
          ...
  ...
```
