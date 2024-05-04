---
manufacturer:
-一般
---

###Android 6+

经常检查以下设置：

-在旧设备上：<溴>
_手机设置>电池和省电>电池使用>忽略优化>打开_忽略应用程序的电池优化。

-在新设备上：<溴>
_设置>应用程序>您的应用程序>电池>优化电池使用>全部（从上到下）>您的应用程序_（切换到禁用）。

###Android 8+

检查如果**手机设置>应用程序和通知>您的应用程序>背景限制**或**背景限制**没有为应用程序启用。

如果一切失败，你可以完全关闭瞌睡模式。

##关闭Android6.0及更早版本的doze

在**设置>开发人员选项**（如果你不知道如何启用开发人员选项，Google应该提供帮助。）

### Turn off doze on Android 7+

Requires expert skills

`dumpsys deviceidle disable`

### If all fails

Look for any vendor-specific battery saver on your device and ideally uninstall if possible, disable if possible.


If not, you are left with the option to root your device or uninstall it though **adb** (requires some expert skills though):

`adb shell`

`pm uninstall --user 0 com.useless.piece.of.trash`


Look through the vendor-specific phone settings and search for anything related to battery optimization or background processing.
If you find it try to disable it.


Try the generic approach below as some vendors tend to hook more functionality into this than AOSP


**Phone settings > Battery & power saving > Battery usage > Ignore optimizations > Turn on** to ignore battery optimization for your app.
