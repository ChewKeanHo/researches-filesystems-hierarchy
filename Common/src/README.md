# `src`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses source files.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is recommended to keep the files structurally clean and seamlessly
explorable. Example:

```
src/
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
```

OR

```
src/
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
```

Scoping your `product` under your registered `trademark` (e.g. your name)
can greatly reduces common words naming collision. It is optional but
highly recommended.
