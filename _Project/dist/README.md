# `dist`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses readily publishable web contents and packages. It
is first introduced by Node.js technology
(https://nodejs.org/en/learn/modules/publishing-a-package#two-full-distributions)
and was later followed suited by its kind like Deno and Bun.

Fortunately, it is configurable in the technology configuration files. Hence,
it may or may not appear depending on the project maintainer.

Note that due to its being a production data role, one must be careful working
here for preventing any data poisoning or losses.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is a singular `dist` name.
