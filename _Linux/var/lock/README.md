# `/var/lock`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) serial devices' lock files.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

In some UNIX-like OSes like Red Hat Linux, SystemD, and UAPI, this directory
is **NO LONGER USED AND REMOVED** with `/var/run/lock` and `/run/lock` as their
replacements. Some UNIX-like OSes like FreeBSD uses `/var/spool/lock` directory
instead.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `lock`** as it represent the entire data
directory.

The file extension can be anything.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/var/
  lock/
    ...
    trademark/
      product/
        service1.lock
        service2.lock
        data1.lock
        profile1.lock
        ...

OR

/var/
  lock/
    ...
    product/
      service1.lock
      service2.lock
      data1.lock
      profile1.lock
      ...
```
