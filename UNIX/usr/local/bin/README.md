# `/usr/local/bin`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing user supplied non-critical system-wide
programs and applications for extending the operating system functionalities
from full catalogue stage to complete stage. This means it can operate in
`Multi-User` mode in BSD realm.

Generally, you **SHOULD** place your custom installed programs and
applications here. It will be made available for all users system-wide.

The main purpose of such separation is to make sure the operating system's
update transaction goes smoothly without any conflicting files.

This directory **MUST NOT** have any sub-directory.




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Like any executable programs and applications, on UNIX, the filename
**MUST BE THE SAME** as desired command.
