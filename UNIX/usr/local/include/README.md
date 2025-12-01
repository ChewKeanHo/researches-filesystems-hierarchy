# `/usr/local/include`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing user supplied non-critical system-wide
inclusion files (e.g. C header files) for extending the operating system's
functionalities from full catalogue stage to complete functionalities stage.
This means it can operate in `Multi-User` mode in BSD realm.

Generally, you **SHOULD** place your custom programs and applications
configuration files here.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the libraries files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    include/
      trademark/
        product/
          lib1.h
          lib1_freebsd-amd64.h
          kernel8.h
          kernel8_freebsd-amd64.h
          ...

# OR

/usr/
  local/
    include/
      product/
        lib1.h
        lib1_freebsd-amd64.h
        kernel8.h
        kernel8_freebsd-amd64.h
        ...
```
