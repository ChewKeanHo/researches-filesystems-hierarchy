# `/usr/src`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing operating system's distributor
supplied non-critical source files for extending the operating system's
functionalities from minimal critical stage to full catalogue stage. This
means it can operate in `Multi-User` mode in BSD realm.

Generally, you **SHOULD ONLY** place distributor's registered files here.
Otherwise, for any user-specific installed programs and applications, you
should use `/usr/local/src` instead.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  src/
    trademark/
      product/
        file1.c
        file2.c
        ...

OR

/usr/
  src/
    product/
      file1.c
      file2.c
      ...
```
