# `/var/crash`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all operating system's (OS) kernel crash dump data files.
Due to its processing nature, one **MUST** carefully work here to prevent any
data poisoning or losses.

This directory is **ENTIRELY OPTIONAL** depending on the OS' engineering
specifications.

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
  crash/
    202511011500_kernel.log
    202511011530_kernel.log
    ...
    trademark/
      product/
        file1.log
        file2.log
        ...

# OR

/var/
  crash/
    202511011500_kernel.log
    202511011530_kernel.log
    ...
    product/
      file1.log
      file2.log
      ...
```
