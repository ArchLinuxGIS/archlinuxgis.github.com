---
title: Repositories
layout: default
---

You can find here some information on how to check out code and binaries for
the project.

### Code ###

You can find the PKGBUILDs and any other related files on [this repo on
github](https://github.com/ArchLinuxGIS/archlinuxgis).

### Binary Packages ###

Binary packaging is expected to arrive in the near future.

For the moment you can add the repository for your architecture adding this
snippet to your `/etc/pacman.conf`:

    [archlinuxgis]
    SigLevel = PackageOptional
    Server = http://archlinuxgis.no-ip.org/$arch

Please be patient. The repository is hosted on a private system with low
upstream bandwith.

