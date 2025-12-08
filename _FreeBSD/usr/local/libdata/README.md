# `/usr/libdata`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied, non-critical
miscellaneous utility data files to extend its functionalities from
*Full Catalogue* stage to *Complete* stage. This means it can operate in
`Multi-User` mode.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as per its distributor's engineering specifications
and customized as per user.

This directory is **ENTIRELY OPTIONAL**. Programs and applications should
practice safe-query before use. Alternatively, use `/var` directory for
transient data instead.

All miscellaneous utility data files here are available to all users.

Generally, when this directory is used, you **SHOULD AND STRONGLY ENCOURAGED**
to place your distributor's unregistered miscellaneous utility data files here
(e.g. from a custom package elsewhere). It will be available to all users
system-wide.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    libdata/
      trademark/
        product/
          map.data
          gui_freebsd-amd64.data
          kernel-interface.data
          kernel-interface8_freebsd-amd64.data
          ...

# OR

/usr/
  local/
    libdata/
      product/
        map.data
        gui_freebsd-amd64.data
        kernel-interface.data
        kernel-interface8_freebsd-amd64.data
        ...
```
