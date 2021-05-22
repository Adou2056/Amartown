中文 | [English](README_English.md)
# 阿玛丁QQ群组
* 一群：`722870741`
* 二群：`865530844`

![Image text](https://raw.githubusercontent.com/Adou2056/Amartown/A-Watch/c47c5f5f-d57c-49bd-a7ad-6e3d27f81c90.jpg)

# 阿玛丁智能手表是什么？
阿玛丁智能手表（A-Watch）<br>
是国内一款出名的电子移动设备<br>
其运存和内存都存在描述偏差<br>
有软件安装限制<br>
搭载Android 4.4.4(kitkat)的FWatchOS(fwOS)<br>
由于FWOS存在反Root机制且未开源放包<br>
所以阿玛丁手表很难进行Root<br>
目前无法找到稳定且有效的Root手段
## 常见阿玛丁配置
| Device | A-WATCH(16G) |
| ----------------: | :---------------------------------------------- |
| SoC | sp9820e_1h10_v5m_8x |
| CPU | sp9820e 32 MODE (armeabi-v7a) |
| GPU | ARM Mali-T820  |
| Memory | 1 GB RAM  |
| Shipped Android version | 4.4.4  |
| Storage | 6-7GB  |
| Battery | 1700 mAh |
| Camera | 0.3 MP (640 × 480) 3.75 mm |
# 为什么要买阿玛丁？
总之当时就是非常非常后悔（雾）

>充电接口类型
>>①普通Mirco USB接口<br>
    ②底座磁吸<br>
    ③多触点并排磁吸<br>

# 如何安装第三方应用软件
你需要:<br>
  * 一台计算机
  * 一枚A-Watch（为Mirco USB接口或多触点磁吸）
  * 一条适用的数据线（需要可以传输数据）<br>
所需必要文件可在项目view code找到
### Note:
底座磁吸需要焊接，动手能力强的可以尝试，但是不建议折腾，早日脱坑吧（笑）
## A-Watch:
### Step 1.进入原生设置
在AI语音助手中说`打开设置`<br>
或者在拨号盘输入`*#991#*`<br>
### Step 2.打开usb调试
关于手机-版本号<br>
连续点击7次 返回上一级设置<br>
在开发者选项中打开usb调试<br>
### Step 3.插线连接电脑
## 计算机:
### Step 1.下载<br>
`安卓adb驱动`和`adb工具包`<br>
### Step 2.配置adb
将`adb.exe` `AdbWinUsbApi.dl` `AdbWinApi.dl` `fastboot.exe`放入<br>
`系统盘:\user(用户)\$登录用户`根目录里
* Linux使用apt-get install android-tools-adb指令配置adb
* Mac使用homebrew配置adb，不赘述
### Step 3.cmd/终端输入adb相关指令
* 查看设备状态<br>
``
adb device
``<br>
* 安装应用<br>
``
adb install [.apk文件所在路径]
``<br>
例如<br>
`adb install D:\TIM2.5.2.apk`<br>
* 覆盖安装应用<br>
``
adb install -r [.apk文件所在路径]
``<br>
* 删除应用<br>
``
adb uninstall [软件包名]
``<br>
例如<br>
`adb uninstall com.tencent.mobileqq`
### Note:
1.apk文件需要兼容32位处理器，支持安卓4.4.4<br>
2.apk所在路径需要没有特殊字符、空格<br>
3.低版本adb工具的甚至要求不能有中文字眼<br>

## 自由安装器——蚂蚁市场使用方法
### Step 1.覆盖安装蚂蚁市场
``
adb install -r [Path]
``
### Step 2.安装应用
1.将apk文件移动到/sdcard/jx/market中<br>
2.进入蚂蚁市场滑到最右侧的文件管理<br>
3.点击安装

# 进阶
* 修改dpi（解决登录、协议点不到的问题）<br>
``
adb shell
``<br>
``
wm density [number]
``<br>
[number]为72-150之间的数字（推荐85）<br>
* 修改分辨率<br>
``
...
``<br>
``
wm size
``<br>
* 强制恢复出厂设置
> 快速连续点击电源键
## Fin
2021.3.9
