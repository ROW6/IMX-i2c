# iMX-i2c
IMX Support for I2C slave functionality

All based off of [this patch](https://lore.kernel.org/patchwork/patch/639459/), released by Dmitriy Baranov and Maxim Syrchin

The patch above was not updated for Linux Toradex BSP Release 3.0.4 with kernel version 4.14-2.3

A new patch was created for the aformentioned BSP, named  4.14-2.3-imx-slave-support.patch

# Applying the patch

1. Download the patch

2. Open a command line window

3. Create a new working directory

    `mkdir ~/bin`
    
    `cd ~/bin`
    
4. Clone the Toradex BSP into directory

    `git clone -b toradex_4.14-2.3.x-imx git://git.toradex.com/linux_toradex.git`
    
5. Move into linux-toradex 

    `cd linux-toradex`
    
6. Set to correct general configurations

    `export ARCH=arm`
    
7. Configure for correct machine

    `make apalis_imx6_defconfig`
    
8. Update specific configurations

    `make menuconfig`

9. Apply patch

    `sudo patch -p1 < ~/Downloads/4.14-2.3-imx-slave-support.patch`

# References

[Original Patch](https://lore.kernel.org/patchwork/patch/639459/)

[Patching Kernel in OpenEmbedded](https://www.toradex.com/de/blog/patching-kernel-in-openembedded)

[OpenEmbedded (core)](https://developer.toradex.com/knowledge-base/board-support-package/openembedded-(core))

[Build U-Boot and Linux Kernel from Source Code](https://developer.toradex.com/knowledge-base/build-u-boot-and-linux-kernel-from-source-code#Source_Code)

[Toradex Easy Installer](https://developer.toradex.com/software/toradex-easy-installer)

[iMX Recovery Mode](https://developer.toradex.com/knowledge-base/imx-recovery-mode)

[Linux Software](https://developer.toradex.com/software/linux/linux-software)
