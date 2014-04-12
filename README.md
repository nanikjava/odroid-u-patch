odroid-u-patch
==============

Files inside this repository is used for ODROID-U3.

**) flash_all -- script to flash Android image to sdcard. Following are the explanation on how to use it
 

1. First create a new directory to host all the necessary files for the sdcard and also copy over the flash_all script to the same directory. For example sake let's named the directory /home/androidu3/sdcard

2. Copy over the ramdisk.img from the the out/target/product/odroidu directory to /home/androidu3/sdcard

3. Copy over bl1.bin, bl2.bin, tzsw.bin and u-boot.bin from /device/hardkernel/proprietary/uboot to /home/androidu3/sdcard

4. Copy over zImage file from the out/target/product/odroidu/obj/KERNEL_OBJ/arch/arm/boot/ directory to /home/androidu3/sdcard

After all files copied execute the flash_all.sh script

	sudo flash_all <sdcard>  <android_out_directory>

You can find what is your sdcard by using - sudo fdisk -l, in my case it's /dev/sdf. You must specify your Android /out directory in the second parameter in my case mine is inside /media/ODROID/out/target/product/odroidu

For example in my case this is my full command

	sudo flash_all /dev/sdf  /media/ODROID/out/target/product/odroidu

Once you are done flashing just put the sdcard into your ODROID-U3 and off you go to the Android world !
