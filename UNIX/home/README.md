# `/home`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all user level data directory. The first-level
directory name is mapped against the user's username.

Depending on the operating system's engineering specification, this
directory can be entirely **optional**.

Programs **SHOULD NOT** assume any file or directory and always
perform safe query before use.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The first layer is mapped against the username from the operating
system's user management system (e.g. `/etc/passwd`). Anything within
the user directory is at the owner's own discretions.


```
/home/
  USERNAME/
    ...
```

Note that while technically one can create a user directory using
sysadmins or root accounts, the operating system's user account is
still requiring updates for matching the user and the directory
associations (e.g. update the `/etc/passwd`).

Hence, when in doubt, always use `$ adduser` command instead.
