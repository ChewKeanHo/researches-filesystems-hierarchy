# `/usr/local/share`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing user supplied system-wide CPU
architecture independent files (e.g. manpage, `README.pdf`, `logo.svg`,
`docs.txt`) for extending the operating system's functionalities from
full catalogue stage to complete stage. This means it can operate in
`Multi-User` mode in BSD realm.

Generally, you **SHOULD** place your custom installed files here and
it will be made available for all users.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
/usr/
  local/
    share/
      trademark/
        product/
          file1.pdf
          file2.txt
          ...

OR

/usr/
  local/
    share/
      product/
        file1.pdf
        file2.txt
        ...
```
