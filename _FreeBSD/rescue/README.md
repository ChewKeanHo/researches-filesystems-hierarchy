# `/rescue`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This is the base directory housing all the critical programs, applications,
configuration files, and data files for the operating system (OS) to perform
self-rescue.

The goal is to have minimally sufficient programs enough for basic
functionalities to perform operating system's self-rescue.

All programs and applications here are available to all the system adminstrators
and root account users only.

Generally, you **SHOULD ONLY** place programs that are very critical at
early booting stage without conflicting with existing POSIX compliant
programs.

This directory **MUST NOT** have any sub-directory.
