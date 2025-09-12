### WORK IN PROGRESS
# lext-artwork-lubuntu
AUR package for the **Lubuntu Arc** LXQt desktop theme (as used by Lubuntu).

## Target: Arch Linux
### AUR
This software **will eventually be made** available on AUR: 
```bash
$ yay -S lext-artwork-lubuntu
```
### Arch Linux without AUR helper
Until then, or if you don't have an AUR helper like *yay* installed:
```bash
$ git clone https://github.com/lext-next/lext-artwork-lubuntu
$ cd lext-artwork-lubuntu
$ makepkg -si
```
Optionally followed by: 
```bash
$ cd ..
$ rm -Rf lext-artwork-lubuntu 
```

## What is this?
This repository is intended for use with AUR (for Arch Linux and derived systems). There is already a package 'lubuntu-artwork' in AUR. That one is supposed to install the Lubuntu-Arc theme as well. Mentioned package has a problem (due to that it is not being maintained) and can't be used anymore to install the theme (witdout tweaking the PKGBUILD file).

The upstream Lubuntu-Arc theme is available at: http://archive.ubuntu.com/ubuntu/pool/universe/l/lubuntu-artwork. This website contains many incarnations of the LXQt theme, each for a specific release of LXQt. 

The various versions of the theme have a specific identifier (e.g. '24.04.3'). The first part obviously denotes for which release of LXQt it is intended ('24.04'). This is followed by a version number (in this case '3'). When a new version of LXQt is released (or in status nascendi) the LXQt project release a new tar file with version number 1 for that release number. When upstream upgrade a theme (for the same LXQt release) the version number is increased. The upstream archive keeps only the latest version, and unfortunately for LXQt 24.04 that is the third version, with identifier '24.04.3' in its tar filename. 

Since the aforementioned 'lubuntu-artwork' package (on AUR) is no longer maintained, it expects to find a specific release and version identifier, which is '24.04'2', valid when the package was last updated to reflect the then actual situation. 

This implies that aforementioned AUR package must be updated regularily (at least for the semiannual releases, and in practice even more than twice a year due minor updates by upstream with a higher version number).

A long story, but it explains why the AUR 'lubuntu-artwork' package no longer works. 

This is where this repository ('lext-artwork-lubuntu') may help. It allows you to easily load a version of the Lubuntu-Arc theming onto your system, with AUR. If someone 'here' changes the release and version numbering according to the situation on the upstream archive it may also be the latest version. 

For most use cases this will suffice. If you explictly need an earlier version (as available on te source URL), and want to use this you need to tweak the PKGBUILD file, as described on the original 'lubuntu-artwork' page on AUR. 

Or ask for a specific version of this AUR package. 

## Changes with the upstream package
The upstream package is used by the Lubuntu distribution, which has more artwork artefacts than required by LXQt. This package requires only the *Lubuntu Arc* theme, and the following parts are excluded:
* wallpapers
* grub
* Kvantum
* plymouth
* sddm
* newt 
