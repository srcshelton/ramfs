ramfs
=====

A memory-backed filesystem mounter for Mac OS X

ramfs automates the segmentation of an area of physical memory, allowing it to
be mounted as a (volatile) filesystem, much like a DMG image.  Please note,
however, that any data stored within this filesystem will not survive a reboot
or even being unmounted.

The intended use is for high-speed scratch-disks or temporary working areas for
high-memory, flash-equipped Macs where reducing write-cycles may be beneficial.

`ramfs` works best with GNU utilities (available via [homebrew](http://brew.sh),
[macports](http://www.macports.org), or
[Gentoo Prefix](https://www.gentoo.org/proj/en/gentoo-alt/prefix/bootstrap.xml))
but care has been taken to ensure that `ramfs` also operates with the standard
Mac OS BSD utilities.  The one exception to this is the `numfmt` command which
is used to parse numbers with SI or IEC suffixes into raw values and back
again.  This could be reimplemented in pure shell-script at some point, but for
now this utility is required.  It will be installed as part of GNU coreutils
(along with many other special-use but very cool tools) from any of the above
package repositories.  Alternatively, a 64-bit binary from a Gentoo Prefix
installation is included in this repo.

