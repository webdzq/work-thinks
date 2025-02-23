# 常用的adb命令
- 做学习机开发，必须会用adb命令，日常安装应用，下载日志，截图，本地镜像、代码调试等都用的到。用好了adb，工作效率非常高。

##  代码行统计 cloc.sh

 - `cloc /Users/xxx-dong/gitlab/xxx-print/src`
## 安装adb 

- 安装工具包 `brew cask install android-platform-tools`

- 检查设备是否和电脑连通 `adb devices` 
  
```bash
(base) xxx-dong@xxx-dongdeMacBook-Pro ~ % adb devices


70x05x3030500020xxxx0** **device

```

## 安装投屏控制软件scrcpy


- 安装工具包 `brew install scrcpy`

- 启动scrcpy在控制台输入`scrcpy`,这样就可以把平板镜像到电脑屏幕上。尤其方便电视会议群共享和showcase环节中使用，截图也很方便，提升会议效率。
  
```bash

(base) xxx-dong@xxx-dongdeMacBook-Pro ~ % scrcpy

```


## 重写设备分辨率

- `adb shell wm size 1200x2000` 和 `adb shell wm density 280`

- 恢复命令：`adb shell wm size reset`


## 监控内存和cpu情况

- 应用查看 `adb shell top -m 10 -s 9 | grep 代码的应用包名`

- 查看top10应用`adb shell top -m 10 -s 9`



## Adb 其他命令
- 安装应用`adb install -t apk路径`和`adb install -d -r -t   强制安装`

- 设备root：`adb root`

- 查看指定关键词的日志：`adb logcat -s WebView`和 `adb logcat | grep -i webview`

- `adb logcat | grep big_web_fcp`

- 把日志输出到指定目录`adb logcat  > 1.txt`

- 导出日志：`adb pull /sdcard/zlog/ Desktop/日志`

- 导出截图（有用）：`adb pull /sdcard/Pictures/Screenshots/Screenshot_20241120-142538.png /Users/xx-dong/github`

- 截屏

```bash
adb shell

screencap -p /sdcard/test.png

// 拉取到电脑中

exit

adb pull /sdcard/test.png  /Users/xx-dong/Downloads

```
