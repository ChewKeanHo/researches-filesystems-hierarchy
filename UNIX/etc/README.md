# `/etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating systems' critical and distribtor
supplied configuration files.

The goal is to have minimum possible configuration files for the
operating system to boot and initialize as intended.

Generally, you **SHOULD ONLY** place or modify system-level
configuration files that are very critical to the operating systems
excluding bootloader artifacts (as they are housed inside `/boot` instead).
Bootloader artifacts generator is allowed as it is part of the operating
system maintenance tool.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

The use of `.d` configuration directory strategy reduces the
configuration complexities and making maintainability easier by just
keeping 1 configuration for 1 file. The program would loop through the
directory and parse everything.

Here are the examples with and without using `trademark` directory:

```
/etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

/etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```
