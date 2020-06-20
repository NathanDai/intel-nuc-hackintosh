intel-nuc7-hackintosh
===

Intel NUC7 微型电脑 黑苹果安装和日常使用EFI


<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**目录**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [说明](#说明)
- [使用方法](#%E4%BD%BF%E7%94%A8%E6%96%B9%E6%B3%95)
- [其他说明](#%E5%85%B6%E4%BB%96%E8%AF%B4%E6%98%8E)
- [Change log](#change-log)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

### 说明

此合集适用于Intel NUC7 微型电脑，其他系列的NUC 微型电脑也差不多适用(ps. NUC6,7,8)

SSDT hotpatch来自[RehabMan](https://github.com/RehabMan/OS-X-Clover-Laptop-Config) 

文件列表：

1. EFI (可直接用于安装、升级和日常使用)

### 使用方法

**1**. EFI

安装时（不保证能顺利安装）：

#### 1.下载 macOS

* (1)使用黑苹果虚拟机或者白苹果下载 macOS 安装器，例如 [macOS Mojave](https://support.apple.com/zh-cn/HT201475) 或 [macOS High Sierra](https://support.apple.com/zh-cn/HT201475)。

* (2)macOS 安装器打开后，请退出而不要继续安装。

* (3)在“应用程序”文件夹中找到单个“Install”文件形式的安装器，例如“Install macOS Mojave”。

#### 2.在“终端”中使用“createinstallmedia”命令

* (1)下载安装器后，请连接用于可引导安装器的 USB 闪存驱动器或其他宗卷。确保该驱动器至少有 12 GB 可用储存空间，并且[格式化为 Mac OS 扩展格式](https://support.apple.com/zh-cn/HT208496)。

* (2)打开“应用程序”文件夹内“实用工具”文件夹中的“终端”。

* (3)在“终端”中键入或粘贴以下命令之一。这些命令假设安装器仍位于您的“应用程序”文件夹中，并且 MyVolume 是 USB 闪存驱动器或您正在使用的其他宗卷的名称。如果不是这个名称，请相应地替换为 ``MyVolume``。

[Mojave](https://support.apple.com/zh-cn/HT201475)：*
```sh 
sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
```
制作好后，使用 `clover configurator` 挂载MacOS所在硬盘的EFI分区，把EFI拷贝进去，重启按F10选择U盘启动。
按照推荐指导，不断点下一步，直到安装完成。

**2**. 声卡、耳机

声卡驱动对于NUC7i7做了配置，i5需要自己折腾一下(生命不息，折腾不止)，耳机的适用和麦克风没有问题，HDMI的声音没有问题，但是机器自带的麦克风无法驱动。

### 其他说明

### Change log

2018-12-08

- 更新 最新驱动，适配了nuc7i7bnh
