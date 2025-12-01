# `/usr/local/etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing users' supplied non-critical
system-wide configuration files for extending the operating system's
functionalities from full catalogue stage to complete stage. This means
it can operate in `Multi-User` mode in BSD realm.

Generally, you **SHOULD** place your custom installed configuration
files here rather than the base `/etc` configuration directory. They
will be available to all users.

Depending on operating system's engineering specifications, some do not
provide or use this directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

The use of `.d` configuration directory strategy reduces the configuration
complexities and making maintainability easier by just keeping 1
configuration per file. Then, the program would loop through the
directory and parse every files to reconstruct the setup.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    etc/
      trademark/
        product/
          settings.d/
            setting1.conf
            setting2.conf
            ...

# OR

/usr/
  local/
    etc/
      product/
        settings.d/
          setting1.conf
          setting2.conf
          ...
```
