mhi-linux-kernel-patches
========================

mhi-linux-kernel-patches is a repository holding out-of-tree kernel patches to support Telit PCIe EP modems for specific kernel versions.

The patches need to be applied on top of the official kernel source code releases available at https://github.com/torvalds/linux

Modem support status
--------------------
Following the status of Telit modems support against the kernel version with patches applied:
|  |v5.12|v5.13|v5.14|>= v5.15|
|--|--|--|--|--|
|<b>FN980 hw v1 |amss: QRTR, RMNET|amss: QRTR, RMNET|amss: QRTR, RMNET|amss: QRTR, RMNET|amss: QRTR, RMNET|amss: QRTR, RMNET|
|<b>FN980 hw v2  |amss: QRTR, RMNET, DIAG, NMEA, AT, AT<br>sbl: DIAG, SAHARA|amss: QRTR, RMNET, DIAG, NMEA, AT, AT<br>sbl: DIAG, SAHARA|amss: QRTR, RMNET, DIAG, NMEA, AT, AT<br>sbl: DIAG, SAHARA|amss: QRTR, RMNET, DIAG, NMEA, AT, AT<br>sbl: DIAG, SAHARA|
|<b>FN990  | n/a |n/a|n/a|amss: MBIM, DIAG, NMEA, AT, AT<br>sbl: DIAG, SAHARA|


Applying the patches
--------------------

To apply the patches:

* Clone the repository

`git clone https://github.com/telit/mhi-linux-kernel-patches.git`

* Checkout the tag related to the kernel version in use:

`git checkout <tag>`

e.g.

`git checkout v5.12`

Branches are in the form `mhi_vx.y` with x.y the actual version.
Tags are in the form `vx.y` for first set of patches or `vx.y-tz` for bugfixing.

* Move to the kernel source code release root and apply the patches:

`git am <directory where patches are stored>/00*`

Rebuild the kernel.
