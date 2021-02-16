# Acer-SF314-52-Hacintosh-with-oc Support 11.0 Big Sur

针对2018年Acer 蜂鸟 Swift 3 笔记本电脑的oc驱动

##无痛升级11.0 beta 6 基本上完全支持11.0，使用体验还行


支持macOS 10.15，在10.14可以使用，但是10.14下intel Wi-Fi无法驱动，itlwm仅在10.15及以上运行


本引导程序在tonymacx论坛上的[efi](https://github.com/FallenChromium/Acer-Swift3-2018-hackintosh/blob/master/README.md)上进行了修改(主要原因是懒得搞voodooi2c的ssdt了白嫖真香)

## 没有更换任何硬件

## 硬件：

CPU: I5-8250U

显卡：UHD620

网卡：INTEL 7265

触摸板：i2c触摸板

硬盘：intel 600p


## 能够正常工作的：

1.uhd620核显。 通过oc注入ID实现

2.声卡ALC255，oc注入ID

*3.intel网卡，使用airportitlwm驱动，原生网络配置，支持定位，接力

4.i2c触摸板：支持几乎所有的原生手势，滑动很流畅，但是有的时候会误判。。。

*5.键盘调节的音量与亮度：Fn+上下左右 调节亮度通过DSDT补丁实现

*6.intel 600p硬盘：修复了掉盘卡顿的问题：通过hackrnvme+ssdt实现

*7.通过null ethernet+ssdt修复因为没有有线网卡导致的App Store问题

8.摄像头

9.睡眠，变频均正常

10.蓝牙 使用zxystd的intel bluetooth驱动，并且可以正常开关蓝牙

## 不能够正常工作的

1.左侧最后一个USB口子：接上去连电都不能充

2.SD卡读卡器：用不了

3.指纹：据原作者说，能检测到但是用不了，，

4.HDMI未测试，原EFI亦未测试

打*表示是我后期优化的XD



# This OpenCore EFI is for the 2018 Acer Swift 3 laptop 

this efi is based on [efi](https://github.com/FallenChromium/Acer-Swift3-2018-hackintosh/blob/master/README.md)

but i have make it more perfect XD

## No Hardware Replaced , all orignal

## Hardware：
CPU: I5-8250U

GPU：UHD620

NetCard：INTEL 7265

Touchpad：i2c Touchpad

NVME：intel 600p


## Working：

1.uhd620

2.SoundCard ALC255

*3.The build-in Intel WIFI -   USE [itlwm](https://github.com/OpenIntelWireless/itlwm)

  support the original airport, handoff and locating

4.i2c touchpad：smooth

*5.FN + [up/down/left/right] to control the volume and brightness : work with DSDT.aml

*6.intel 600p NVME: USE Hackrnvme + SSDT to solve the problem (actually the hackrnvme is for 10.12, however it makes the 600p more stable

  with the original IONvmeFamily, it's very likely to cause a kernel panic.
  
*7.Fix App Store with Null Ethernet + ssdt

*8.Bluetooth : With the latest intel bluetooth firmmware by zxystd , the switch can work too.
  
## Not working:

1. the second USB port in the left : Not even charging

2.fingerprint: detected but not working

3.SD Card Reader


## Not Tested

1.HDMI


what marked with * is my work XD 


