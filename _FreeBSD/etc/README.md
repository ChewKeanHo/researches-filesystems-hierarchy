# `/etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This base directory houses all operating systems' (OS) critical and distribtor
supplied configuration files to function properly and minimally without any
mounting (e.g. `/usr` is not mounted or absent). This means it can operate
in `Single-User` mode in BSD realm or `Emergency Mode` in Linux realm.

The goal is to have minimum possible configuration files for the OS to
initialize as intended achieving basic functionalities. This allows the OS
to perform critical tasks like mounting `/usr` UNIX System Resources directory
for functionalities extension, performing self-rescue, or straight up
operational in resources constraint environment such as but not limited to
OpenWRT embedded router.

Generally, you **SHOULD ONLY** place or modify system-level configuration files
that are very critical to the operating systems excluding bootloader artifacts
(as they are housed inside `/boot` or `/efi` respectively instead). However,
bootloader artifacts' generator is allowed here as it is part of the operating
system maintenance tool.




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
