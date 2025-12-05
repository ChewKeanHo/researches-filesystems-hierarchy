# `log`

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

This output directory houses all production logs related to the project. It is
meant for developers to perform forensic analysis against a particular project's
process with interest.

It is temporary in nature. However, interrupting any on-going processing files
can cause unwanted and unpredicable concequences.

Programs and applications should not be dependent on files located in this
directory as they can be randomly removed by clean up services or human
interventions. Perform safe querying before use.

It is **ALWAYS ENCOURAGED** to timestamp new log file or clean up the existing
one before use to avoid any transient data corruptions. Whenever possible, do
clean up the log files after use as the last step or provide a realiable way for
user to perform the clean up.

It is a practice to house the log files using `trademark` and `service`
sub-directories organization. This can significantly reduces the naming
collision for common names.

Here are the examples with and without using `trademark` directory:

```
log/
  trademark/
    service1/
      202511301200_build.log
      202511301230_build.log
      202511301240_build.log
      ...

OR

log/
  service1/
    202511301200_build.log
    202511301230_build.log
    202511301240_build.log
    ...
```




## Naming Conventions

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

File extension is **ALWAYS REQUIRED** for type identifications among all the
files.

Name the file with the correct language (preferbly latin-1 for character
compatibility) and seamlessly imply the content of the file.
It is **ALWAYS ENCOURAGED** but not required to prefix a full timestamp
(against `UTC` timezone) in reverse pattern (`YYYYMMDDhhmmssuuuu_`) to separate
each logs.

Otherwise, it is **ALWAYS ENCOURAGED** to use *Copy-On-Write* method to reliably
manage a file. It is done by writing the file with a `.tmp` file extension
suffix first and leave the original file in-tact. Once the write is fully
written, perform a file overwrite to refresh into new file. Example:

```
$ printf -- "Hello World" > tmp/myfile.txt.tmp    # write to .tmp file first
$ mv tmp/myfile.txt.tmp tmp/myfile.txt            # overwrite the existing file
```
