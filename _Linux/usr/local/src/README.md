# `/usr/local/src`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing user custom supplied, non-critical
source files to extend its functionalities from *Full Catalogue* stage to
*Complete* stage. This means it can operate in `Multi-User` mode.

The goal is to extend the OS' functionalities to its complete form. At this
stage, the OS can operate as per its distributor's engineering specifications
and customized as per user.

In many UNIX-like OSes like SystemD and UAPI, this directory is
**DEPRECATED AND REMOVED** in favor of using `/home/USERNAME/.local/src`
instead.

All source files here are available to all users.

Generally, when this directory is used, you **SHOULD AND STRONGLY ENCOURAGED**
to place your distributor's unregistered source files here (e.g. from a custom
package elsewhere). It will be available to all users system-wide.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    src/
      trademark/
        product/
          file1.c
          file2.c
          ...

OR

/usr/
  local/
    src/
      product/
        file1.c
        file2.c
        ...
```
