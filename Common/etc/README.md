# `etc`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all configuration scripts including non-executing
shell scripts (those that uses dot import (e.g. `$ . lib.sh`).




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

By experiences, programs and apps always grow big and flexible that
always bloat the configurations and manifest files. Such big files
are usually hard to maintain and usually break things easily.

Fortunately, UNIX systems uses the `.d` configuration directory strategy
to solve this problem. The idea is to read the directory with a `.d`
suffix in its name and then have **ONLY 1** configuration resides in 1
file. The design is as follows:

```
myconfig             - `[OPTIONAL]` main config file that sources the
                       `.d` of itself.
myconfig.d/          - the directory config file.
  setting1.conf
  setting2.conf
  ...
```

Program can either source a main configuration file which later instructs
to source the `.d/` config directory files or just go straight for config
directory files. It is up to the project designer.
