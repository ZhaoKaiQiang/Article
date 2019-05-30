# 统计事件测试

### 在 Android Studio 调试日志中查看事件

您可以启用详细日志记录功能以监控 SDK 的事件记录，从而帮助验证是否正确记录了事件，包括自动和手动记录的事件。

您可以通过一系列 adb 命令启用详细日志记录功能：

```text
adb shell setprop log.tag.FA VERBOSE
adb shell setprop log.tag.FA-SVC VERBOSE
```

然后使用以下命令开启 logcat，此命令可在 Android Studio logcat 中显示您的事件，帮助您立即验证所发送的事件。

```text
adb logcat -v time -s FA FA-SVC
```

也可以在命令行中设置过滤条件

```text
adb logcat -v time -s FA | grep Logging    设置只显示 FA 标签的包含 Logging 的内容
```

### 参考资料

1. [https://firebase.google.com/docs/analytics/android/events](https://firebase.google.com/docs/analytics/android/events)

