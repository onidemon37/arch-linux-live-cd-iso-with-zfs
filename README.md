# Arch Linux Archiso builder with zfs support

This repository contains a simple, free as in freedom, wrapper to automate the steps mentioned in the [arch linux wiki](https://wiki.archlinux.org) for the [zfs installation](https://wiki.archlinux.org/index.php/ZFS#Installation) and the [archios package installation](https://wiki.archlinux.org/index.php/Archiso#Installing_packages).

The current change log can be found [here](CHANGELOG.md).

All you need to do is to execute the [build.sh](https://github.com/stevleibelt/arch-linux-live-cd-iso-with-zfs/blob/master/build.sh).

You can download a build iso to use [here](https://archzfs.leibelt.de/).

All needed packages where installed automatically. The build script will output the path to the created iso file.

At the end, you only need to dd the iso to your favorit usb drive, use [venotoy](https://www.ventoy.net) or burn it on an optical disk.

## Howto

```
####
#build an iso
####
#flags
#   -f|--force
#   -d|--dry-run
#   -h|--help
#   -r|--repo-index [<string: last|week|month|yyyy\/mm\/dd>]
#       if you just use -r, default of >>last<< is used
#       @see: https://archive.archlinux.org/repos/
#   -v|--verbose
####
# tired of repeating the same flags again and again?
#
# optional configuration file is supported and saves your keystrokes
# cp configuration/build.sh.dist configuration/build.sh
# adapt file configuration/build.sh
####
./build.sh

#test run an existing iso
./run_iso.sh [<string: path to the iso>]

#upload the iso
./upload_iso.sh [<string: path to the iso>]
```

## Possible issues

Following issues are not reproducable on all my machines.

### error: target not found: ipw2100-fw

* This error happens when calling `build.sh`
* [This](https://gitlab.archlinux.org/archlinux/archiso/-/commit/4d64a58a905403b3abfca5077dcd924ef7901ba7) commit seams to be the reason
* [This](https://bbs.archlinux.org/viewtopic.php?id=279908) thread contins information
* [This](https://forum.endeavouros.com/t/missing-aur-packages-ipw2100-fw-ipw2200-fw/32019) is a solution for endevour os

## Links

* [Another archiso build script by Maurice Zhou](https://gitlab.com/m_zhou/archiso)
* [archiso documentation](https://git.archlinux.org/archiso.git/tree/docs)
* [archiso project page](https://git.archlinux.org/archiso.git)
* [Install UEFI and BIOS compatible Arch Linx with encrypted ZFS and ZFSBootMenu by Kayvlim](https://wiki.archlinux.org/title/User:Kayvlim/Install_UEFI_and_BIOS_compatible_Arch_Linux_with_Encrypted_ZFS_and_ZFSBootMenu#Swap) - 20221108
* [pacman wiki page](https://wiki.archlinux.org/index.php/Pacman)
* [Ubuntu server zfsbootmenu](https://github.com/Sithuk/ubuntu-server-zfsbootmenu) - 20221108

## Contributers

In alphabetically order.

* [derzahla](https://github.com/derzahla)
* [gardar](https://github.com/gardar)
  * Added [git workflows](https://github.com/stevleibelt/arch-linux-live-cd-iso-with-zfs/pull/11)
* [Kodiman](https://github.com/Kodiman)
  * Added information of the [Ubuntu server zfsbootmenu](https://github.com/stevleibelt/arch-linux-live-cd-iso-with-zfs/issues/14)
* [stevleibelt](https://github.com/stevleibelt)
  * Main Developer

