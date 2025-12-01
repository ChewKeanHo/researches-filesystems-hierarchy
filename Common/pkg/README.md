# `pkg`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is an output directory housing readily releasable packages.

Release processes are also done here. The directory structure
**MUST BE FLAT** (no sub-directory) since a lot of release portals
(notably GitHub, Gitea, and GitLab) do not support sub-directories
structures.

The best practice is to let end-users use their package manager to
install the software rather than providiing a long list of manual
steps.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

To support seamless import for end-users, it is advisable to use the
`[OS]-[ARCH]` filename suffix convention whenever available. For example:

```
myprogram_v1.0.0_linux-amd64.deb
myprogram_v1.0.0_linux-amd64.rpm
myprogram_v1.0.0_linux-amd64.pkg
myprogram_v1.0.0_linux-amd64.tar.xz
...
myprogram_v1.0.0_linux-arm64.deb
myprogram_v1.0.0_linux-arm64.rpm
myprogram_v1.0.0_linux-arm64.pkg
myprogram_v1.0.0_linux-arm64.tar.xz
...
myprogram_v1.0.0_freebsd-amd64.deb
myprogram_v1.0.0_freebsd-amd64.rpm
myprogram_v1.0.0_freebsd-amd64.pkg
myprogram_v1.0.0_freebsd-amd64.tar.xz
...
myprogram_v1.0.0_freebsd-arm64.deb
myprogram_v1.0.0_freebsd-arm64.rpm
myprogram_v1.0.0_freebsd-arm64.pkg
myprogram_v1.0.0_freebsd-arm64.tar.xz
..
myprogram_v1.0.0_windows-amd64.zip
myprogram_v1.0.0_windows-arm64.exe
myprogram_v1.0.0_windows-arm64.msi
...
RELEASE
CITATION.cff
LICENSE.txt
README.md
```

File extension is required for consistency sake. Some packages can have
repository files setup (e.g. `.deb` has its `RELEASE`) manifest.
