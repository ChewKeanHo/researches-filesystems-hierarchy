# `/usr/local/etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied, non-critical
configuration files to extend its functionalities from *Full Catalogue* stage to
*Complete* stage. This means it can operate in `Multi-User` mode.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as per its distributor's engineering specifications
and customized as per user.

All configuration files here are available to all users.

Generally, you **SHOULD AND STRONGLY ENCOURAGED** to place your distributor's
unregistered configuration files here (e.g. from a custom package elsewhere). It
will be available to all users system-wide.




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
