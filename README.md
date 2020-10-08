# Bubba B3 kernel

Gentoo-sources kernel used by [bubbagen](https://github.com/gordonb3/bubbagen) on the Excito B3

## Description

<img src="https://raw.githubusercontent.com/gordonb3/cache/master/Bubba/Excito-B3.jpg" alt="Excito B3" width="250px" align="right"/>
This project contains supported builds of the

[bubbagen](https://github.com/gordonb3/bubbagen) kernel.

The project files include scripts to prepare and build the [preboot kernel](https://github.com/gordonb3/bubba-b3-kernel/releases/tag/4.9.49-pre) that is required to be able to boot the zImage kernels created by the (mostly) automated kernel build script in the `src` folder.

## Installation

The advised route for installing this kernel is to emerge the `bubba-b3-kernel-bin` package from the bubba overlay. Should you wish to install a non-released kernel version you built yourself and/or deploy the preboot kernel on a different gentoo release for the Excito B3 simply unpack the release tarball to the root file system ('/'). Note that this manual method does not verify if you have the boot partition mounted in '/boot'.



## Feedback Welcome!

If you have any problems, questions or comments regarding this project, feel free to contact me! (gordon@bosvangennip.nl)

