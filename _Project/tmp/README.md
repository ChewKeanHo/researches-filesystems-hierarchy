# `tmp`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all temporary files. While the directory is temporary,
interrupting any on-going processing files can cause unwanted and unpredicable
concequences.

Programs and applications should not be dependent on files located in this
directory as they can be randomly removed by clean up services or human
interventions. Perform safe querying before use.

It is **ALWAYS ENCOURAGED** to clean up the temporary directory of your specific
location before use to avoid any transient data corruptions. Whenever possible,
do clean up after use as the last step or provide a realiable way for user to
perform clean up.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces
the naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
tmp/
  trademark/
    product1/
      lib1.o
      lib1_freebsd-amd64.o
      kernel8.o
      kernel8_freebsd-amd64.o
      ...

OR

tmp/
  product/
    lib1.o
    lib1_freebsd-amd64.o
    kernel8.o
    kernel8_freebsd-amd64.o
    ...
```




## Temporary Natures

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

File extension is **ALWAYS REQUIRED** for type identifications among all the
files. Name the file with the correct language (preferbly latin-1 for character
compatibility) and seamlessly imply the content of the file.

It is **ALWAYS ENCOURAGED** to use *Copy-On-Write* method to reliably manage
a file. It is done by writing the file with a `.tmp` file extension suffix
first and leave the original file in-tact. Once the write is fully written,
perform a file overwrite to refresh into new file. Example:

```
$ printf -- "Hello World" > tmp/myfile.txt.tmp    # write to .tmp file first
$ mv tmp/myfile.txt.tmp tmp/myfile.txt            # overwrite the existing file
```
