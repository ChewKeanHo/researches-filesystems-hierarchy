# `public`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses readily publishable static website contents. It was
first introduced by Hugo.io (https://gohugo.io/) and later picked up by many
static site generator (SSG) programs.

Note that due to its being a production data role, one must carefully
work here to prevent any data poisoning or losses.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is a singular `public` name. This name is critical
on certain service providers like GitLab where their continuous integrations
only recogizes this directory for static website.
