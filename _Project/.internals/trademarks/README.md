# `.internals/trademarks`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses the project (e.g. `git`) trademark graphic files like
icons and banners. This is for end-users or customers to quickly recognizes
the project as a product visually.

The outer-most layer here is production ready uses files.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

It is always recommended to use generic naming instead of product names
(e.g. `animated-banner_1200x100.svg`) to ensure maximum operating
compatibilities across the project repository.

A good guidance would be:

```
[purpose]_[width]x[height].[file extension]
```

* **[purpose]** - states the purpose of the trademark (e.g.
  `animated-banner` for web page display). Some examples:
  *  **`animated-banner`** - web browsers animated banner.
  *  **`banner`** - static banner.
  *  **`banner-monochrome`** - static black and white monochromatic icon.
  *  **`icon`** - static icon.
  *  **`icon-monochrome`** - static black and white monochromatic icon.
* **[width]** - states the width of the file. Sonic/Audio trademark
    files can ignore this.
* **[height]** - states the height of the file. Sonic/Audio trademark
    files can ignore this.
* **[file extension]** - states the file type.


Some artists are very sloppy when it comes to data management (e.g.
not exporting publicly usable `svg` files and locked the project with
expensive proprietary software). Some even have extremely bad tempers
and bad mouths (as in the
`I am an artist and I do whaever the @#$@#$ I like` attitude`).

Hence, it's best to keep the names as generic as possible and only have
them work on the design files.




## `.internals/trademarks/principals`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Depending on the project, you might want to create the `principals`
directory to house the main graphic files (that generates the production
ready versions).

The former names were `masterpieces` or `masters` but were renamed to
`principals` for inclusion and purging the `master-slave` relations
from the project.

The name of the file should be the same as the production ready files.
However, it is recommended to prefix the software you use to the name.
Example:

```
principals/inkscape-animated-banner_1200x100.svg

# for

animated-banner_1200x100.svg
```

That way, future maintainer knows where to hunt for such software.
