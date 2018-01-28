# Cedrus support for Allwinner / sunXi platform

Here is the driver Cedrus for video decoding on sunXi platform

## Adding the Mali to your Device Tree

If that isn't already the case, you'll need to edit your Device Tree file to
add a node following the [Device Tree binding](https://github.com/mripard/cedrus/blob/master/driver/sunxi-cedrus.txt)

## Apply patches to your Kernel

In order to build the kernel module, 
you need to apply patches according to your Kernel Version.
Find Kernel patches under `patches/*` folder and
apply them to your kernel.

## Building the kernel module

In order to build the kernel module,
you need `CONFIG_V4L2_MEM2MEM_DEV` enabled in your kernel configuration.

Then you can compile the module using the following commands:

```
git clone https://github.com/mripard/cedrus.git
cd cedrus/driver
export CROSS_COMPILE=$TOOLCHAIN_PREFIX
export KDIR=$KERNEL_BUILD_DIR
make ARCH=arm 
```
