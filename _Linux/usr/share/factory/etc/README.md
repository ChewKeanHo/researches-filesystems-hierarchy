# `/usr/share/factory/etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) distributor
supplied, non-critical, factory default configurations files for extending the
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

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

The use of `.d` configuration directory strategy reduces the configuration
complexities and making maintainability easier by just keeping 1 configuration
per file. The program would loop through the directory and parse everything.

Here are the examples with and without using `trademark` directory:

```
/usr/
  share/
    factory/
      etc/
        trademark/
          product/
            settings.d/
              setting1.conf
              setting2.conf
              ...

OR

/usr/
  share/
    factory/
      etc/
        product/
          settings.d/
            setting1.conf
            setting2.conf
            ...
```
