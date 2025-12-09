# `/var/ftp`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) file transfer protocol (FTP)
data files. Due to its processing nature, one **MUST** carefully work here to
prevent any data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications. In Red Hat Linux, it is being used similar to FreeBSD.

Programs **SHOULD NOT** assume any file and directory here and **SHOULD** always
practice safe-querying before use.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and `product`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
/var/
  ftp/
    trademark/
      product/
        node1
        node2
        file1.data
        file2.data
        ...

# OR

/var/
  ftp/
    product/
      node1
      node2
      file1.data
      file2.data
      ...
```
