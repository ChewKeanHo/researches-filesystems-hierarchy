# Filesystems Hierarchy Layouts Research Project

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Having trouble working with filesystems hierarchy layouts especially those that
has standardized regulations like UNIX and Windows? Are you looking for some
design references that are comforming and portable to as many operating as
possible? This is the right research dataset.

At (Holloway) Chew, Kean Ho's Filesystems Hierarchy Layouts Research Project,
tech volunteers and me are continuously updating this repository for abstracting
common filesystems and directory layouts for various purposes. The research
goals are simple:

1. **Maximizing Compatibilities, Minimizing Conflicts** - analyzes and abstracts
   various standards for common patterns. Through these patterns, new projects
   can maximize inter-compatibilities and minimizing conflicts across multiple
   operating systems; AND
2. **Unifying Filesystems** - With common patterns in filesystems and directory
   organizations, packaging software for end-user can be simplified and unified
   for easier and maintainable maintenances works, automations, documentations,
   and communitions sakes; AND
3. **Solid and Hygienic Design References For Project Structuring** - something
   clean and reliable to refer (not a rule to enforce) when designing a project
   directory layout.

This dataset is a 100% deterministic with futuristic directive concequencies.
It is **100% human-made. Direct artificial intelligences (A.I) contributions
(e.g. vibe coding) IS STRICTLY PROHIBITED**. Only use A.I. for
non-concequential tasks like scouting for data source materials across the
broken search engines.

> [!WARNING]
>
> **REMEMBER: THESE ARE DESIGN REFERENCES; NOT RELIGIOUS RULES**. In other
> words, they are **opinions**.
>
> **DO NOT ATTEMPT TO RELIGIOUSLY ENFORCE** your project layouts by pointing
> back to this project. **IN NO WAY** this project is encourages anyone to
> adhere opinions.
>
> **Fanaticism destroys**. Please act responsbily and sensibly.

To use this dataset, first setup the markdown rendering `git` repository
(e.g. its GitHub mirror:
https://github.com/ChewKeanHo/researches-filesystems-hierarchy). There you can
read the descriptions of each directory. For dataset, you need an UNIX program
called `tree`. Then execute the command:

```
$ tree -a -d path/to/TARGET/
```

The final outputs are consolidated into:

* **Common Directory Structure** - the [/Common](/Common). This is used for all
  common functioning directories that can combine with other directories for
  inter-compatible interpretations.
* **User Home Directory Structure** - the [/User](/User). This is used to setup
  an user's home directory especially for graphical user interface. It can
  combine with other directories for inter-compatible interpretations.
* **UNIX Filesystems Hierarchy** - the [/UNIX](/UNIX). The abstracted compatible
  filesystems across ALL UNIX OSes including BSD and Linux-based.

Any specific filesystem hierarchies are prefixed with an underscore (`_`). These
are dedicated directories for consolidating their respective specific designs
prior to `/UNIX` abstractions. Among them are:

* **FreeBSD Filesystems Hierarchy** - the [/_FreeBSD](/_FreeBSD) UNIX-like OS.
* **Linux Filesystems Hierarchy** - the [/_Linux](/_Linux)-based UNIX-like OS.
  Note that this consolidates all kinds of Linux-based OSes including but not
  limited to SystemD, FreeDesktop.org, Red Hat, Debian, Devuan, Void Linux,
  Fedora, etc.
* **Project Directory Structures** - the [/_Project](/_Project) commonly used
  for small modular project repository (e.g. `git` project repository).




## Design Sources & References

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

Currently, this project had already processed the following engineering
specifications to match the outputs:

1. FreeBSD, 2025, "3.5. Directory Structure", *FreeBSD Handbook*, 4th Edition,
   The FreeBSD Project by The FreeBSD Community & The FreeBSD Foundations,
   viewed 09 December 2025, available at:
   https://docs.freebsd.org/en/books/handbook/basics/#dirstructure
2. Software Freedom Conservancy, 2025, "file-hierarchy — File system hierarchy overview",
   FreeDesktop via Software Freedom Conservancy, viewed 09 December 2025,
   available at:
   https://www.freedesktop.org/software/systemd/man/latest/file-hierarchy.html
3. FreeDesktop Filesystem Hierarchy Standard Project Contributors,
   The Linux Foundation, Daniel Quinlan, Paul 'Rusty' Russell, Christopher Yeoh;
   2025; "Filesystem Hierarchy Standard"; FreeDesktop via Software Freedom
   Conservancy; viewed 09 December 2025; available at:
   https://specifications.freedesktop.org/fhs/latest/rootFilesystem.html
4. GoHugo Authors; 2025; "Directory Structure"; The GoHugo Team; viewed
   09 December 2025; available at: https://gohugo.io/getting-started/directory-structure/
5. Palebloodsky; 2025; "Filesystems"; OpenWRT.org; viewed 09 December 2025;
   available at:
   https://openwrt.org/docs/guide-user/storage/filesystems-and-partitions
6. bxbzq, Cath O'Deray, kpedersen; 2021;
   "What's the proper way to install truetype fonts"; the FreeBSD Forum;
   The FreeBSD Foundation via XenForo Ltd; viewed 09 December 2025; available at:
   https://forums.freebsd.org/threads/whats-the-proper-way-to-install-truetype-fonts.79999/
7. Graham Perrin, David Edmundson; 2024; "Bug 442976"; bugs.kde.org; KDE.org;
   viewed 09 December 2025; available at: https://bugs.kde.org/show_bug.cgi?id=442976
8. Joe Brockmeier; 2025; "Debian Technical Committee overrides systemd change";
   *Articles*; lwn.net via Eklektix, Inc.; viewed 09 December 2025; available at:
   https://lwn.net/Articles/1041316/
9. rfc1036 et al.; 2025; "/var/lock/ is the standard interface for locks of serial devices";
   GitHub via GitHub.Inc; viewed 09 December 2025; available at:
   https://github.com/systemd/systemd/issues/38563
10. Devuan; 2025; "Welcome to Devuan"; Devuan.org; viewed 09 December 2025;
    available at: https://www.devuan.org/
11. Void Linux Contributors and Juan RP; 2025; "The Void (Linux) distribution";
    VoidLinux.org; viewed 09 December 2025; available at:
    https://docs.voidlinux.org/about/index.html
12. SystemD; 2025; "The Case for the /usr Merge"; SystemD.org; viewed
    09 December 2025; available at: https://systemd.io/THE_CASE_FOR_THE_USR_MERGE/
13. Oracle; 2012; "User Environment Feature Changes";
    *Oracle Solaris 11 Information Library*; Oracle and/or its affiliates;
    viewed 09 December 2025; available at:
    https://docs.oracle.com/cd/E23824_01/html/E24456/userenv-1.html
14. Debian; 2025; "UsrMerge - The Debian /usr Merge"; *Wiki*; Debian.org;
    viewed 09 December 2025; available at: https://wiki.debian.org/UsrMerge
15. Red Hat; 2025; "Changes/Unify bin and sbin"; *Wiki*; FedoraProject.org via
    Red Hat Inc. and others; viewed 09 December 2025; available at:
    https://fedoraproject.org/wiki/Changes/Unify_bin_and_sbin
16. Flatpak Team; 2025; "Introduction to Flatpak"; *Documentations*; Flatpak
    Team via @pradyunsg's Furo; viewed 09 December 2025; available at:
    https://docs.flatpak.org/en/latest/introduction.html
17. Red Hat; 2025; "Chapter 2. File System Structure and Maintenance";
    *Red Hat Enterprise Linux > 7 > Storage Administration Guide*; viewed
    09 December 2025; available at:
    https://docs.redhat.com/en/documentation/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-filesystem
18. The Linux Userspace API Group; 2025; "UAPI.9 Linux File System Hierarchy#";
    *UAPI Group Specifications*; Version 0.1; The Linux Userspace API Group;
    viewed 09 December 2025; available at:
    https://uapi-group.org/specifications/specs/linux_file_system_hierarchy/
19. FreeBSD; 2025; "`hier` - Miscellaneous Information Manual";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?hier(7)
20. FreeBSD; 2025; "Ports - Miscellaneous Information Manual";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=ports&sektion=7&apropos=0&manpath=FreeBSD+15.0-RELEASE+and+Ports
21. FreeBSD; 2025; "Chapter 4. Installing Applications: Packages and Ports";
    *FreeBSD Handbook*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://docs.freebsd.org/en/books/handbook/ports/
22. FreeBSD; 2025; "FreeBSD Porter's Handbook"; *FreeBSD Handbook*;
    The FreeBSD Project via The FreeBSD Community and The FreeBSD Foundation;
    viewed 09 December 2025; available at:
    https://docs.freebsd.org/en/books/porters-handbook/book/
23. FreeBSD; 2025; "`yp` - System Manager's Manual"; *FreeBSD Manual Pages*;
    The FreeBSD Project via The FreeBSD Community and The FreeBSD Foundation;
    viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=yp&manpath=FreeBSD+13.2-STABLE
24. FreeBSD; 2025; "`named` - Internet domain name server";
    *FreeBSD Manual Pages*; The FreeBSD Project via The FreeBSD Community and
    The FreeBSD Foundation; viewed 09 December 2025; available at:
    https://man.freebsd.org/cgi/man.cgi?query=named&sektion=8&manpath=OpenBSD+5.1




## License

[![banner](/.internals/trademarks/animated-banner_1200x100.svg)](#)

* [Agreed GIMP License](.internals/terms-of-services/GimpORG_License.pdf)
* [Agreed GIMP Privacy Policy](.internals/privacy-policy/GimpORG-Privacy-Policy.pdf)
* [Agreed Inkscape License](.internals/terms-of-services/Inkscape_License.pdf)
* [Agreed Inkscape Privacy Policy](.internals/privacy-policy/Inkscape-Privacy-Policy.pdf)
* [Agreed (Holloway) Chew, Kean Ho's Upscaler License](.internals/terms-of-services/Upscaler_LICENSE.txt)

This entire project is licensed under
[Creative Commons Attribution-NoDerivatives 4.0 International License](LICENSE.txt).

Under this license, you are allowed to use the image for any means AS LONG AS
YOU **MUST** attribute back to the arist(s) as follows:

```
--------------------------------------------------------------------------------
Title: (Holloway) Chew, Kean Ho's Filesystems Hierarchy Layouts Research Project
Creators: (Holloway) Chew, Kean Ho
Contact: hello@chewkeanho.com
UUID: 3113F0A2-61BD-449C-BC0F-DE4C09997AC6
SKU: chewkeanho-researches-filesystems-hierarchy
License: Creative Commons Attribution-NoDerivatives 4.0 International License
Made On: 2025-11-30
Procure: https://github.com/ChewKeanHo/researches-filesystems-hierarchy
--------------------------------------------------------------------------------
```

For registered non-profit organizations (NGO), you're considered as a
`Commercial Entity` similar to for-profit organizations by default but with
the NGO disbursement grant and exception from the artist. Please process them
as such.



### Internal Use - Personal

> [!NOTE]
>
> This targets customers wanting to use the dataset just for internal use
> without broadcasting to any other 3rd-party and without monetary intention
> such as but not limited to:
>
> * Reading via handphone; OR
> * Reading via computer.

You're **ALLOWED as long as you comply to the attribution above**.



### Internal Use - Commerical

> [!NOTE]
>
> This targets customers wanting to use the dataset just for internal use
> without broadcasting to any other 3rd-party and with monetary intention such
> as but not limited to:
>
> * Every examples from `Internal Use - Personal`; AND
> * Sampling dataset for enhancing company's procurement list.

You're **ALLOWED as long as you comply to the attribution above**.



### Broadcast Redistribution - Personal

> [!NOTE]
>
> This targets customers wanting to share the dataset via broadcasting without
> monetary intention to multiple receiving 3rd-parties in both public or private
> spaces disregarding their respective license compliances such as but not
> limited to:
>
> * Every examples from `Internal Use - Personal`; AND
> * Private GitHub group sharing among team members; OR
> * Private self-hosted Gitea sharing among family members.

You're **ALLOWED as long as you comply to the attribution above**.



### Broadcast Redistribution - Commercial

> [!NOTE]
>
> This targets customers wanting to share the dataset via broadcasting with
> monetary intention to multiple 3rd-parties in both public or private spaces
> disregarding their respective license compliances such as but not limited to:
>
> * Every examples from `Internal Use - Personal`; AND
> * Every examples from `Internal Use - Commercial`; AND
> * Every examples from `Broadcast Redistribution - Personal`; AND
> * Company's public events; OR
> * Company's private events; OR
> * Company's public exhibition; OR
> * Company's entry payable private exhibition; OR
> * YouTube public livestreaming; OR
> * Company's marketing roadshow; OR
> * Public GitHub group mirrored repository; OR
> * Public self-hosted Gitea mirrored repository.

You're **ALLOWED as long as you comply to the attribution above**.



### Integration - Personal

> [!NOTE]
>
> This targets customers wanting to use the dataset for direct integration into
> their creation as it is without any remixes or modifications and without any
> monetary intention from the project such as but not limited to:
>
> * YouTube video creation **WITHOUT** any profits including advertisement
>   commission; OR
> * Personal video production and collection; OR
> * Personal web portfolio project; OR
> * Machine learning training for conceiving artificial intelligence model.

You're **ALLOWED as long as you comply to the attribution above**.



### Integration - Commercial

> [!NOTE]
>
> This targets customers wanting to use the dataset for direct integration into
> their creation as it is without any remixes or modifications and with any
> monetary intention from the project such as but not limited to:
>
> * Every examples from `Integration - Personal`; AND
> * YouTube video creation **WITH** any profits mechansim including but not
>   limited to advertisement commission; OR
> * Company internal event's dataset material; OR
> * Company internal meeting's dataset material; OR
> * Company public advertisement dataset materials; OR
> * Company public digital display signage dataset materials.

You're **ALLOWED as long as you comply to the attribution above**.



### Reference Remix - Personal

> [!NOTE]
>
> This targets customers wanting to reference the dataset's elements for new
> creation without any monetary intention from the project such as but not
> limited to:
>
> * YouTube video creation **WITHOUT** any profits including advertisement
>   commission; OR
> * YouTube thumbnail images with edited images; OR
> * Creating a new research paper referencing to this dataset; OR
> * Creating a new research dataset referencing to this dataset; OR
> * Personal web art expression portfolio project.

You're **ONLY ALLOWED to reference WITHOUT ANY REMIXING** to the original
dataset for your pursue including academic referencing as long as you comply
to the attribution above without any count limitations or any other
restrictions.

You are **NOT ALLOWED** to create any derivatives (e.g. translating this paper
into another language) as the license itself **STORNGLY PROHIBITS** anyone to
do as such.



### Reference Remix - Commercial

> [!NOTE]
>
> This targets customers wanting to reference the dataset's elements for new
> creation without any monetary intention from the project such as but not
> limited to:
>
> * Every examples from `Reference Remix - Personal`; AND
> * YouTube image video creation **WITH** any profits including
>   advertisement commission; OR
> * YouTube thumbnail images with edited images; OR
> * Journal publications; OR
> * News reporting this dataset; OR
> * Company internal units' dataset material with internal researchers.

You're **ONLY ALLOWED to reference WITHOUT ANY REMIXING** to the original
dataset for your pursue including academic referencing as long as you comply
to the attribution above without any count limitations or any other
restrictions.

You are **NOT ALLOWED** to create any derivatives (e.g. translating this paper
into another language) as the license itself **STORNGLY PROHIBITS** anyone to
do as such.



### Composition Remix - Personal

> [!NOTE]
>
> This targets customers wanting to modify the original dataset's elements
> compositions directly for producing a new dataset without any monetary
> intention such as but not limited to:
>
> * Every examples from `Reference Remix - Personal`; AND
> * Personal dataset remixing practice using editing techniques such as but not
>   limited to digital processing, etc; OR
> * YouTube video remix creation **WITHOUT** any profit including advertisement
>   commission; OR
> * Create a modified dataset for personal use; OR
> * Create a modified dataset for social media's attentions.

You are **NOT ALLOWED** to create any derivatives as the license itself
**STORNGLY PROHIBITS** anyone to do as such.



### Composition Remix - Commercial

> [!NOTE]
>
> This targets customers wanting to modify the original dataset's elements
> compositions directly for producing a new dataset with any monetary intention
> such as but not limited to:
>
> * Every examples from `Reference Remix - Personal`; AND
> * Every examples from `Reference Remix - Commercial`; AND
> * Every examples from `Composition Remix - Personal`; AND
> * Post-processing dataset remixing or re-editing production; OR
> * YouTube video creation remixing **WITH** any profit including advertisement
>   commission; OR
> * Create a modified dataset for company's internal use; OR
> * Create a modified dataset for company's social media's uses.

You are **NOT ALLOWED** to create any derivatives as the license itself
**STORNGLY PROHIBITS** anyone to do as such.



### Resell Redistribution - Personal

> [!NOTE]
>
> This targets customers wanting to share and to redistribute the dataset and
> its derrivatives without any monetary intention such as but not limited to:
>
> * Sharing the dataset across social media **WITHOUT** any income including
>   but not limited to advertisement commissions; OR
> * Share the dataset among friends via email/messaging attachment **WITHOUT**
>   any monetary transaction in any form involved.

You are **ALLOWED as long as you comply to the attribution above**.



### Resell Redistribution - Commercial

> [!NOTE]
>
> This targets customers wanting to resell the dataset and its derrivatives
> for any monetary intention such as but not limited to:
>
> * Every examples from `Resell Redistribution - Personal`; AND
> * Sharing the dataset across company's social media; OR
> * Selling the dataset to the public; OR
> * Distribute the dataset into multiple profit-earning streaming platform.

You are **ALLOWED as long as you comply to the attribution above**.
