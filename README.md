Ubantu Boot Tool
================




How To Download
---------------

 Choose your Local Directory
```bash
  $ cd /home/$user$/Workspace
```
Open terminal on this Directory

Type Those command for Download it
```bash
  $ git clone https://github.com/Kukun7610/ubantu-tool-bootimg.git
```

How to Unpack bootimg
---------------------

Copy the boot.img file into ubantu-tool-bootimg folder

Open terminal on same folder

Run script


```bash
  $ ./boot-tool boot.img boot
```
on there 

boot.img is origenal bootimg file

boot folder is after extraction of boot.img file

Example

 
```bash        
$ ./boot-tool boot.img boot
Unpack & decompress boot.img to boot
  kernel         : /home/$USER$/workspace/ubantu-tool-bootimg/boot/zImage
  ramdisk        : /home/$USER$/workspace/ubantu-tool-bootimg/boot/ramdisk.gz
  page_size      : 2048
  base_addr      : 0x00000000
  kernel size    : 4146912
  kernel_addr    : 0x00008000
  ramdisk_size   : 89
  ramdisk_addr   : 0x01000000
  second_size    : 0
  second_addr    : 0x00f00000
  dtb_size       : 419840
  dtb_img        : /home/$USER$/workspace/ubantu-tool-bootimg/boot/dt.img
  tags_addr      : 0x00000100
  cmdline        : console=ttyHSL0,115200,n8 androidboot.console=ttyHSL0 androidboot.hardware=qcom user_debug=31 msm_rtb.filter=0x37 utags.blkdev=/dev/block/platform/msm_sdcc.1/by-name/utags vmalloc=400M
```


How to Repack bootimg
---------------------

After Modify boot folder

Open terminal on same folder

run script



```bash
  $ ./boot-tool boot newboot.img
```
on there 

boot.img is origenal bootimg file

boot folder is after extraction of boot.img file

Example



```bash
 $ ./boot-tool boot newboot.img
mkbootimg from boot/img_info.
  kernel         : /home/$USER$/workspace/ubantu-tool-bootimg/boot/zImage
  ramdisk        : /home/$USER$/workspace/ubantu-tool-bootimg/boot/new_ramdisk.gz
  page_size      : 2048
  base_addr      : 0x00000000
  kernel size    : 4146912
  kernel_addr    : 0x00008000
  ramdisk_size   : 89
  ramdisk_addr   : 0x01000000
  dtb_size       : 419840
  dtb_img        : dt.img
  tags_addr      : 0x00000100
  cmdline        : console=ttyHSL0,115200,n8 androidboot.console=ttyHSL0 androidboot.hardware=qcom user_debug=31 msm_rtb.filter=0x37 utags.blkdev=/dev/block/platform/msm_sdcc.1/by-name/utags vmalloc=400M
Kernel size: 4146912, new ramdisk size: 87, newboot.img: 4571136.
newboot.img has been created.
```
