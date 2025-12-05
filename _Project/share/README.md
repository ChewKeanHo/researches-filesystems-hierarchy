# `share`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses readily usable CPU-architecture independent files
such as but not limited to `.pdf` documents, `.txt` documents, `.svg` images,
and etc.

It is a practice to house the configuration files using `trademark` and
`product` sub-directories organization. This can significantly reduces the
naming collision for common names.

Here are the examples with and without using `trademark` directory:

```
lib/
  trademark/
    product/
      image/
        logo_1200x1200.svg
        logo_1200x630.svg
        ...
      manual/
        man.1
        user.pdf
        man.2
        os.pdf
        ...
      license/
        product.pdf
        product.txt
      ...

OR

lib/
  product/
    image/
      logo_1200x1200.svg
      logo_1200x630.svg
      ...
    manual/
      man.1
      user.pdf
      man.2
      os.pdf
      ...
    license/
      product.pdf
      product.txt
      ...
    ...
```




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

File extension is **ALWAYS REQUIRED** for type identifications among all the
files. Name the file with the correct language (preferbly latin-1 for character
compatibility) and seamlessly imply the content of the file.
