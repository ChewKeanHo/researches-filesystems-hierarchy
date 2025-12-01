# `datastore`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all production data files used in data server or
network area storage (NAS) data systems. In short,
**this is that critical production data directory**.

Due to its persistent storage role and data warehousing, one
**MUST** carefully work here to prevent any data poisoning or losses.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `datastore`** as it represent the
entire datastore of a service. The service can do internal structuring
on its own accords inside this directory.
