# xiaoXinPro-i5-PM981

**这里只是小新PRO13硬盘为PM981的折中方案，为了更好的使用黑果，强烈建议更换其他型号硬盘。**


使用方法一：克隆法（一定成功）
---
1. 安装mac系统到U盘/移动硬盘/其他型号的硬盘
2. 克隆安装好的MAC分区到PM981硬盘
3. 使用此处的`clover`建立引导，引导PM981里的MAC系统

使用方法二：正常安装
---
**我测试了两次安装，两次升级都成功了，缺少更多测试，不保证一定成功，不成功请选择克隆法**
1. 下载合适安装镜像写入U盘。
2. 使用磁盘精灵打开U盘`EFI`分区，
3. 删除分区内的`clover`文件夹，
4. 拷贝`安装clover`文件夹到U盘EFI分区原来的`clover`位置，并更名为`clover`
5. 按照[小兵博客](https://blog.daliansky.net/Lenovo-Xiaoxin-PRO-13-2019-and-macOS-Catalina-Installation-Tutorial.html)正常安装（安装过程不需要选择config_install文件）
6. 安装完成如果无法启动，请参照第四条将引导文件替换为`正常使用clover`，第一次引导过程需要选择`install_config`,进入系统重建缓存后下次开机不需要选择。

关于系统升级
---
* PM981升级系统很有可能升级失败，务必在win下备份系统。
* 我的电脑可以正常升级，但是缺少更多测试，无法保证所有的小新都能升级。
* 如果使用`正常使用clover`升级失败请尝试使用`安装clover`。


关于PM981补丁
---
补丁分为安装补丁，和正常使用补丁，我已经放入对应文件夹,用此处的clover不需要修改

* 正常使用补丁位于`正常使用clover/ACPI/SSDT-nvme.aml`和`正常使用clover/kexts/other/HackrNVMeFamily.kext`

* 安装补丁位于`安装clover/kexts/NVMeFix.kext`

如果是其他型号计算机可以尝试添加上面所述的补丁到你的clover,不保证可以使用。

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
* 无法完全睡眠，PM981硬盘正常盒盖不关wifi和蓝牙耗电大概`6%~7%/h`,关闭wifi和蓝牙`3%~4%`
* 打开QQ+Chrome看小时大概使用8小时左右

现存问题：
---
* 开启store视屏自动播放功能/使用腾讯视屏会导致显卡变频失效

# 请详细阅读小兵大佬提供的[安装教程](https://blog.daliansky.net/Lenovo-Xiaoxin-PRO-13-2019-and-macOS-Catalina-Installation-Tutorial.html)，按照教程操作，不要错漏任何一步。

# 本人只是搬运工，感谢小兵大佬和宪武大佬以及众多群友的无私奉献，感谢群友`HellO`提供的PM981补丁，有什么疑难问题请到黑果群提问，此处不做解答。
