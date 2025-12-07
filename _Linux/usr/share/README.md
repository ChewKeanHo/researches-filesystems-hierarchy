# `/usr/share`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory for housing operating system's (OS) distributor
supplied, non-critical CPU independent files (e.g. manuals, PDF files, images,
static databases, etc) for extending the OS functionalities from
*Critical & Minimal* stage to *Full Catalogue* stage. This means it can operate
in `Full Mode`.

The goal is to extend the OS' functionalities for distributor level full
functionalities. At this stage, the OS can operate as per its distributor's
engineering specifications.

All files here are available to all users.

Generally, you **SHOULD ONLY** place distributor's registered files here. For
your own locally build or custom sourced packages, you should place them inside
`/usr/local/share` directory instead.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  share/
    trademark/
      product/
        file1.pdf
        file2.txt
        ...

OR

/usr/
  share/
    product/
      file1.pdf
      file2.txt
      ...
```
