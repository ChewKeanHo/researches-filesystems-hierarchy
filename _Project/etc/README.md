# `etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses all configuration files.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
etc/
  trademark/
    product/
      settings.d/
        setting1.conf
        setting2.conf
        ...

OR

etc/
  product/
    settings.d/
      setting1.conf
      setting2.conf
      ...
```




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Programs and applications always grow big and be flexible such that they
always bloat their configurations and manifest files. Such big files are
usually very hard (requires file jumping across thousands of lines) to
maintain and usually break things easily overtime.

Fortunately, on many UNIX operating systems, they introduced the `.d`
configuration directory strategy to solve this problem. The idea is to
read the entire configuration directory with a `.d` suffix in its name
and then have **ONLY 1** configuration resides in 1 file. The design
pattern is as follows:

```
myconfig.d/              - the configuration files directory.
  setting1.conf
  setting2.conf
  ...
```

Program and applications can then loop through the directory and parse
each file to source all its configurations.

Sub-directory **is usable but discouraged** as it complicates the looping
algorithm with recursive scanning. This may be a problem especially in
real-time embedded implementations where time-deterministic is a requirement.
