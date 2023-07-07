# Hackintosh_i3-6100_H110N_HD530_EFI

| 名称 | 型号版本 |
|  ----  | ----  |
| 主板 | 梅捷 SY-H110N 全固版 |
| CPU	| Intel i3 6100 |
| 核显	| Intel HD Graphics 530|
| 独显	| 无|
| 网卡	| 瑞昱Realtek RTL8105E |
| 引导	| OpenCore 0.7.0 |
| 机型	| Macmini8,1 |
| 显示器| 1080P@60Hz VGA接口 |
| 平台ID | 0x193B0005|
| 音频 | 瑞昱Realtek ALC662 |
| 系统 | **macOS Catalina10.15.7(19H2026)** |

这个项目基于**[Hackintosh_i5-6500_B250M_HD530_EFI](https://github.com/wonpn/Hackintosh_i5-6500_B250M_HD530_EFI)**修改变成[**Maxzby/Hackintosh_i3-6100_B150M_HD530_EFI** ](https://github.com/Maxzby/Hackintosh_i3-6100_B150M_HD530_EFI)基于以上再次修改成**Hackintosh_i3-6100_H110N_HD530_EFI******



# 更新内容

添加瑞昱（Realtek）网卡驱动，（**RealtekRTL8105E**）**找不到原项目链接**

添加英特尔（intel）蓝牙驱动，（**IntelBluetoothFirmware**）[Github链接](https://github.com/OpenIntelWireless/IntelBluetoothFirmware)

更新OpenCore版本为 0.7.0 

# 核显驱动（以下为原作者编写内容）

显示器为4k显示器，主板Gigabyte B250M-D3H支持4k@60分辨率的DP口显示输出。

B250系主板一般配7代 intel cpu，如 i5-7500，核显型号为 HD 630。GitHub上有很多现成的EFI可以直接使用。我这里6500核显为 HD 530，直接使用EFI，黑屏，无法启动。

仿冒ID：12345678 可以启动，也可以支持到4K，但是显存显示为31MB，特别卡，无法使用。

正确的设置方法为：

 - 机型设置为：Macmini8,1。如果为iMac 17/18 均会出现紫屏现象。
 - 仿冒ID：0x193B0005

以上设置已经配置在 EFI 文件中，同型号HD 530 直接使用即可，不需要另外设置。

### **视频显示输出接口选择**（以下为我修改的版本）

这个项目**基于**[Hackintosh_i5-6500_B250M_HD530_EFI](https://github.com/wonpn/Hackintosh_i5-6500_B250M_HD530_EFI)**修改**变成[Maxzby/Hackintosh_i3-6100_B150M_HD530_EFI ](https://github.com/Maxzby/Hackintosh_i3-6100_B150M_HD530_EFI)基于以上再次修改成**Hackintosh_i3-6100_H110N_HD530_EFI**

**实测主板VGA接口可以完美驱动1080P@60Hz，显存1536MB**

**但DVI接口也在登录界面闪屏后黑屏**

# 音频

该主板使用的是瑞昱Realtek ALC662，仿冒id=5

成功驱动

# 支持情况

 ✅ 1080P@60 显示

 ✅ 核显显存 1536MB

 ✅ Audio 正常

 ✅ 有线网卡 正常

 ❔ 睡眠唤醒 （短期睡眠正常可以唤醒，长期睡眠睡死）

## 存在的问题

 ❌ VedioProc 显示不支持硬件解码，剪辑软件很卡。（Chrome 播放 4K 视频、本地 4K 视频播放正常）

 ❌ Chrome 播放4K高码率视频回卡屏，系统假死。关闭 chrome 的“硬件加速”选项可以解决该问题。

 ❌ DVI接口无法使用，在登录界面黑屏
"# Hackintosh_i3-6100_H110N_HD530_EFI" 
