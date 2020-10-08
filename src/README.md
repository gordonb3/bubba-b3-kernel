# zImage kernel for the Excito B3

## Description
These scripts are for building the zImage kernel for the Excito B3. 

## Prerequisite
There are no kernel sources included in this project and these must therefore be installed separately and marked active through `eselect`.

## Building the kernel
* Run `build-zImage-b3` to create a tar.xz deployment archive of the kernel and accompanying libraries in the system's source directory `/usr/src` (`/usr/armv5tel-softfloat-linux-gnueabi/usr/src` if you run this on a crossdev machine)

## Additional notes
* The resulting kernel does NOT include a Device Tree Blob (DTB) nor the required patch to temporarily disable the L2 cache (per [this note](https://lists.debian.org/debian-boot/2012/08/msg00804.html)). These are added by the kexec preboot kernel when it loads the final kernel, thus allowing the exact same kernel to be used in various configurations, e.g. different front led colour during boot, different init system, etc.


## Feedback Welcome!

If you have any problems, questions or comments regarding this project, feel free to contact me! (gordon@bosvangennip.nl)

