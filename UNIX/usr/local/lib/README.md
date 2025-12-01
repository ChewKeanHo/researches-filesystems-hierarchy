# `/usr/local/lib`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing user supplied non-critical system-wide
libraries files for extending the operating system's functionalities from
full catalogue stage to complete stage. This means it can operate in
`Multi-User` mode in BSD realm.

Generally, you **SHOULD ONLY** place your custom installed libraries files
here. They will be made available to every users.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    lib/
      trademark/
        product/
          lib1.so
          lib1_freebsd-amd64.so
          kernel8.ko
          kernel8_freebsd-amd64.ko
          ...

# OR

/usr/
  local/
    lib/
      product/
        lib1.so
        lib1_freebsd-amd64.so
        kernel8.ko
        kernel8_freebsd-amd64.ko
        ...
```
