# Preboot kernel for the Excito B3

## Description
These scripts are for preparing and building the kexec preboot kernel for the Excito B3. 

## Prerequisite
The scripts are hardcoded for kernel version `4.9.49-r1` sources which must be installed separately and is provided by the bubba overlay.

## Building the kexec preboot kernel
* Run `make-kexec-initramfs-b3` to create the RAM file system
* Run `configure-kexec-kernel-b3` to write out the required configuration. This also creates the alternate device tree source files for controlling the front led
* Run `build-kexec-uImage-b3 -u` to create a USB install mode kernel or run the script without parameters to create a normal runtime uImage kernel

## Additional notes
* Depending on whether you are building a USB install mode kernel or one to run from the internal harddisk, the build script will attach a device tree blob that lights the front led on the B3 either green (install mode) or purple (normal run mode). This default colour scheme can be overridden by using the `-d` parameter to the build script.
* While the install mode kernel bares a different name (`install.itb`) it is in fact a uImage. The difference between the two kernels is in the script RAM filesystem that determines which logical drive is mounted to look for the final kernel to boot. Thus by renaming the uImage to `install.itb` you can run the B3 from a disk that is not supported by the uboot. The downside is that you must press the button on the back at startup, so it won't come up automatically after a power failure.
* If a file named `boot.ini` is present in the root of the dedicated boot partition, the preboot kernel will parse this file for alternative parameters to pass to the final kernel. Reference the sample file in this folder for details.

## Feedback Welcome!

If you have any problems, questions or comments regarding this project, feel free to contact me! (gordon@bosvangennip.nl)

