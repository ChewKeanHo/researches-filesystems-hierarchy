# `/usr/share/factory/var`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) distributor
supplied, non-critical, factory default transient data files for extending the
OS functionalities from *Critical & Minimal* stage to *Full Catalogue* stage.
This means it can operate in `Full Mode`.

The goal is to extend the OS' functionalities for distributor level full
functionalities. At this stage, the OS can operate as per its distributor's
engineering specifications.

All files here are available to all users.

Generally, you **SHOULD ONLY** place distributor's registered files here. These
files are used to systematically and reliably restore the OS settings back to
the distributor original supplied version.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The first sub-directory layer is function oriented (e.g. `log`, `mail`, `lock`,
`cache`, `tmp`, `crash`, `www`, `spool`, ...). This is defined by the OS'
engineering specification itself.

Within the function oriented sub directory, it is a practice to house the
configuration files using `trademark` and `product` sub-directories
organization. This can significantly reduces the naming collision for common
names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  share/
    factory/
      var/
        icons/
          trademark/
            product/
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

/usr/
  share/
    factory/
      var/
        icons/
          product/
            banner_1200x1200.svg
            ...
        log/
          product/
            access.log
            info.log
            ...
        ...
```
