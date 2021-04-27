mhi-linux-kernel-patches
========================

mhi-linux-kernel-patches is a repository holding out-of-tree kernel patches to support Telit PCIe EP modems for specific kernel versions.

The patches need to be applied on top of the official kernel source code releases.

Patches are available since kernel v5.12

Applying the patches
--------------------

To apply the patches:

* Clone the repository

`git clone https://github.com/telit/mhi-linux-kernel-patches.git`

* Checkout the tag related to the kernel version in use:

`git checkout <tag>`

e.g.

`git checkout v5.12`

* Move to the kernel source code release root and apply the patches:

`git am <directory where patches are stored>/00*`

Rebuild the kernel.
