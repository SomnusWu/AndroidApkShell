
# 导出已经安装的apk:


> 查看已经安装的apk
adb shell pm list package

> 点击打开需要导出的应用，让其处于第一窗口，执行以下命令可以输入当前窗口的Activity
adb -s 192.168.20.103:5555 shell dumpsys window w |findstr \/ |findstr name=
输出结果：  mSurface=Surface(name=com.yx.ystpdjhandroid/com.yx.ystpdjhandroid.MainActivity)

> 根据要导出的app包名，查看APP安装路径
adb shell pm path com.xx
输出结果：package:/system/app/AutoControl/AutoControl.apk

> 导出apk

adb pull app安装路径 保存路径
eg: adb pull /system/app/AutoControl/AutoControl.apk C:\Users\Somnus\Desktop\apk安装脚本






