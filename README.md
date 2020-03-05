# xiaoXinPro-i5-PM981

# 小白又不爱看教程请直接换硬盘，小白又喜欢自由发挥请直接换硬盘，小白还是直接换硬盘吧！！！

**这里只是小新PRO13硬盘为PM981的折中方案，为了更好的使用黑果，强烈建议更换其他型号硬盘。**

**i7 cpu或者i7 id的i5 cpu请自行修改dvmt,不修改无法驱动显卡，修改文件在qq群：946132482（提问请描述清楚你的问题，包括但不限于cpu型号，是否修改dvmt，硬盘型号，操作过程，到了哪一步，遇到什么情况，想要做什么）**

使用方法一：克隆法（一定成功）
---
1. 安装mac系统到U盘/移动硬盘/其他型号的硬盘
2. 克隆安装好的MAC分区到PM981硬盘
3. 使用此处的`clover`建立引导，引导PM981里的MAC系统

使用方法二：正常安装
---
1. 下载合适安装镜像写入U盘。
2. 使用磁盘精灵打开U盘`EFI`分区，
3. 删除分区内的`clover`文件夹，
4. 拷贝`安装clover`文件夹到U盘EFI分区原来的`clover`位置，并更名为`clover`
5. 按照[小兵博客](https://blog.daliansky.net/Lenovo-Xiaoxin-PRO-13-2019-and-macOS-Catalina-Installation-Tutorial.html)正常安装（安装过程不需要选择config_install文件）
6. 安装完成如果无法启动，请参照第四条将引导文件替换为`正常使用clover`，第一次引导需要选择`install_config`,进入系统重建缓存。（如果重建缓存后无法启动，请使用config_i7引导）



关于系统升级
---
**PM981升级系统可能失败，务必备份系统**
1. 使用`正常使用clover/OC`进入系统，在系统设置里升级系统
2. 使用`安装clover`引导安装升级文件（带data或者pn后缀，如果无法成功，请多试几次或者自己找办法解决）
3. 使用`正常使用clover`引导进入系统更新缓存。



关于PM981补丁
---
补丁分为安装补丁，和正常使用补丁，我已经放入对应文件夹,用此处的clover不需要修改

* 正常使用补丁位于`正常使用clover/ACPI/SSDT-nvme.aml`和`正常使用clover/kexts/other/HackrNVMeFamily.kext`

* 安装补丁位于`安装clover/kexts/NVMeFix.kext`

如果是其他型号计算机可以尝试添加上面所述的补丁到你的clover,不保证可以使用。

关于睡眠
---
小新pro13不支持MAC的S3睡眠模式，S3睡眠会卡在睡眠的过程中，并且无法唤醒，所以禁用了S3睡眠。
这里的clover&OC都使用的是宪武大佬提供的AOAC睡眠补丁，仿S3睡眠，开盖无法唤醒，唤醒需要按电源键/电源键+Fn+q,**这不是bug**

注意事项
---
* 注意：第一次启动可能不成功，长按电源键重启多试几次（只有更改clover后才会出现此情况，正常使用不会）
* 这不是安装教程，只是PM981硬盘安装黑苹果的折中办法，详细安装教程请移步[小兵博客](https://blog.daliansky.net/Lenovo-Xiaoxin-PRO-13-2019-and-macOS-Catalina-Installation-Tutorial.html)
* PM981升级MAC系统有很大概率失败，想升级系统请在win下完整备份MAC系统后再尝试。

硬件型号
---

|硬件|型号|
| --- | --- |
|CPU|10210U|
|核显|uhd620|
|网卡|已经更换BCM94360CS2|
|声卡|alc257|
|显示器|华星|
|硬盘|PM981A|

功能情况
---
* CPU变频正常
* 核显驱动正常
* 触摸板驱动正常，支持手势
* 声卡内置MIC无法驱动，其余正常
* FN+F1-F9快捷键正常
* 打开QQ+Chrome看小时大概使用8小时左右
* AOAC睡眠，睡眠期间2%每小时，唤醒需要按电源键
* clover已经移植睡眠补丁，OC & clover均支持AOAC睡眠

现存问题：
---
* 内置声卡无mic
* 启动速度慢：偶尔启动时间接近50s,原因未知
  
可能出现状况和解决办法
---
<details><summary>使用BCM94360CS2网卡死机</summary>
	
**表现**
电脑负载高时突然屏幕卡住，电脑没有任何响应
**可能解决办法**
参考DW1820A屏蔽转接卡正面的两个针脚：[参考链接](http://bbs.pcbeta.com/viewthread-1846508-1-1.html)
  
</details>

# 请详细阅读小兵大佬提供的[安装教程](https://blog.daliansky.net/Lenovo-Xiaoxin-PRO-13-2019-and-macOS-Catalina-Installation-Tutorial.html)，按照教程操作，不要错漏任何一步，请按教程操作完有问题再提问。

# 本人只是搬运工，感谢小兵大佬和宪武大佬以及众多群友的无私奉献，感谢群友`HellO`提供的PM981补丁，有什么疑难问题请到黑果群提问，此处不做解答。
