# `datastore`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This directory houses all production data files used by a service server. In
short, **this is the critical production data directory**.

It is used when the project repository is used as a version controlled server
control repository like file storage server in a network area storage (NAS)
data service server.

Due to its persistent storage role and data warehousing, one
**MUST BE VERY CAREFUL** working here to prevent any data poisoning,
data losses, or break the server's internal operating mechanisms.




## Naming Convention

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

The naming convention is **singular `datastore`** since it represents the
entire datastore of a service. The service can do internal structuring on its
own accords inside this directory.

This directory **IS STRONGLY ENCOURAGED** to be excluded from version control
tracking like adding it into the `.gitignore` file with exception to its
existences file like `datastore/.gitkeep`. Datastore uses other methods to
perform backups like `rsync` and other large-scale data transfer applications
and source-code version control technology is unsuitable for the job.
