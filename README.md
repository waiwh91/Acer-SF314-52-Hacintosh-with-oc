# Acer-SF314-52-Hacintosh-with-oc

针对2018年Acer 蜂鸟 Swift 3 笔记本电脑的oc驱动

支持macOS 10.15，在10.14可以使用，但是intel Wi-Fi无法驱动，itlwm仅在10.15上运行

本引导程序在tonymacx论坛上的[efi](https://github.com/FallenChromium/Acer-Swift3-2018-hackintosh/blob/master/README.md)上进行了修改(主要原因是懒得搞voodooi2c的ssdt了白嫖真香)

##硬件：
CPU: I5-8250U
显卡：UHD620
网卡：INTEL 7265
触摸板：i2c触摸板
硬盘：intel 600p


##能够正常工作的：

1.uhd620核显。 通过oc注入ID实现

2.声卡ALC255，oc注入ID

*3.intel网卡，使用itlwm驱动，进入macOS之后打开heliport即可进行网络配置

4.i2c触摸板：支持几乎所有的原生手势，滑动很流畅，但是有的时候会误判。。。

*5.键盘调节的音量与亮度：Fn+上下左右 调节亮度通过DSDT补丁实现

*6.intel 600p硬盘：修复了掉盘卡顿的问题：通过hackrnvme+ssdt实现

7.摄像头

8.睡眠，变频均正常

##不能够正常工作的
1.左侧最后一个USB口子：接上去连电都不能充

2.SD卡读卡器：用不了

3.指纹：据原作者说，能检测到但是用不了，，

4.HDMI未测试，原EFI亦未测试

打*表示是我后期优化的XD



#This OpenCore EFI is for the 2018 Acer Swift 3 laptop 

this efi is based on [efi](https://github.com/FallenChromium/Acer-Swift3-2018-hackintosh/blob/master/README.md)

but i have make it more perfect XD

##Hardware：
CPU: I5-8250U
GPU：UHD620
NetCard：INTEL 7265
Touchpad：i2c Touchpad
NVME：intel 600p

##Working：

1.uhd620

2.SoundCard ALC255

*3.The build-in Intel WIFI -   USE [itlwm](https://github.com/OpenIntelWireless/itlwm)

  you can use the Heliport app in the folder to connect to wifi

4.i2c touchpad：smooth

*5.FN + [up/down/left/right] to control the volume and brightness : work with DSDT.aml

*6.intel 600p NVME: USE Hackrnvme + SSDT to solve the problem (actually the hackrnvme is for 10.12, however it makes the 600p more stable

  with the original IONvmeFamily, it's very likely to cause a kernel panic.
  
##Not working:

1. the second USB port in the left : Not even charging

2.fingerprint: detected but not working

3.SD Card Reader


##Not Tested

1.HDMI


what marked with * is my work XD 


