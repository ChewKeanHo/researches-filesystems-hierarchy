# `/var/lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) programs and applications'
persistent data.

Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `lib`** as it represent the entire data
directory.

The file extension can be anything.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/var/
  lib/
    trademark/
      product/
        data.save
        profile1.jpg
        transient.json
        ...

OR

/var/
  lib/
    product/
      data.save
      profile1.jpg
      transient.json
      ...
```
