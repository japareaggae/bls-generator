bls-generator
=====

A Boot Loader Specification entry generator for Arch Linux.

The idea for this script is that you can run it while installing Arch,
and it will automatically detect where your root partition is and
generate a BLS entry for it.

This script is mostly useless, however, because:

* Arch already ships a sample entry in `/usr/share/systemd/bootctl/arch.conf`,
  and `lsblk -no UUID /dev/sda2 >> arch.conf` isn't really that hard, is it?
* The [Discoverable Partitions Specification](https://systemd.io/DISCOVERABLE_PARTITIONS/)
  means you can boot Linux with an empty options line and it will
  still be able to find and mount your root partition

This was a good learning experience nonetheless.

