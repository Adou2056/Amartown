# Amartown QQ Groups
* Group 1：`722870741`
* Group 2：`865530844`
# What's Amartown Watch(A-Watch)？
Amartown Smart Watch(A-Watch)<br>
is known electronic mobile equipment in China<br>
has a description bias in both ROM and RAM<br>
has software installation restrictions<br>
its FWatchOS(fwOS) is based on Android 4.4.4(kitkat)<br>
FWOS has an anti-root mechanism and does not open source the packages<br>
So the watches are very difficult to get rooted<br>
A stable and effective Root method is currently not available<br>
## Common Amartown Config
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
# Why Amartown？
Anyway, it was very, very regretful（雾）

>Charging interface types
>>①Mirco USB<br>
    ②Chassis magnetic suction<br>
    ③Multiple contacts side by side magnetic suction<br>

# How to install apps normally
You need:<br>
  * A computer
  * An A-Watch(Mirco USB or Multiple contacts side by side magnetic suction)
  * A suitable charging line (need to be able to transmit data) <br>
The necessary files can be found in Code
### Note:
The chassis magnetic suction charging device needs welding. If you have strong hands-on ability, you can try it, but I don't hope you to do so...Please get out of the pit as soon as possible (wwwwww)
## A-Watch:
### Step 1.Go to Native Settings
Say to the AI voice assistant `打开设置`(da'kai'she'zhi)<br>
Or input on the dial`*#991#*`<br>
### Step 2.Open USB Debug
About phone-Build number<br>
Click 7 times,then return to the previous level <br>
Turn on USB Debug in the Developer option <br>
### Step 3.Plug the line into the computer
## Computer:
### Step 1.Download<br>
`Android ADB Drive `and`adb-tools`<br>
### Step 2.Configurate ADB
Copy`adb.exe` `AdbWinUsbApi.dl` `AdbWinApi.dl` `fastboot.exe`into<br>
`System Disk:\user\$Login user `
* Linux uses `apt-get install android-tools-adb` to configurate adb
* Mac use Homebrew to configurate adb
### Step 3.cmd/Terminal input 
* View device status<br>
``
adb device
``<br>
* Install the app<br>
``
adb install [Path of .apk file]
``<br>
Like<br>
`adb install D:\TIM2.5.2.apk`<br>
* Reinstall the app<br>
``
adb install -r [Path of .apk file]
``<br>
* Uninstall the app<br>
``
adb uninstall [Package Name]
``<br>
Like<br>
`adb uninstall com.tencent.mobileqq`
### Note:
1. APK files need to be compatible with 32-bit processor and support Android 4.4.4<br>
2. The apk path must have no special characters and Spaces<br>
3. The lower version of ADB tool even requires that there be no Chinese words.
## Freedom installer - how to use 蚂蚁市场
### Step 1.Reinstall 蚂蚁市场
``
adb install -r [Path]
``
### Step 2.Install apps
1.Move apk files into /sdcard/jx/market<br>
2.蚂蚁市场-文件管理(Slide to the far right)<br>
3.Pause to install

# Advanced
* Fix dpi(Solve the problem of login and protocol not being clicked)<br>
``
adb shell
``<br>
``
wm density [number]
``<br>
[number] equals to number between 72 and 150(85 is the best for me)<br>
* Fix resolution<br>
``
...
``<br>
``
wm size
``<br>
* Force to restore factory Settings
> Click the power button rapidly in succession
## Fin
2021.3.9
