# EasyProtector  [ ![Download](https://api.bintray.com/packages/lamster2018/maven/easy-protector-release/images/download.svg) ](https://bintray.com/lamster2018/maven/easy-protector-release/_latestVersion)

EasyProtector，a simple way to check root/virtual app/emulator/xposed framework/tracer/debugger.

很多朋友是通过[郭霖老师的公众号推送](https://mp.weixin.qq.com/s/XvqUc3drJhdJ9hOuCcfdkg) 或者[陈宇明老师的公众号推送](https://mp.weixin.qq.com/s/7I_vGV77TWqhQR9Myc5FQg)了解到这个库的。

既然来都来了，欢迎大家star/fork,哪怕提个issue都好，我希望这是一个好用的库（省去application的初始化操作，避免更多的权限要求，尽可能的懒加载）

Ps:已经失业，最近在找工作，有空会陆续修复issue，谢谢各位的建议和意见！！

# Document

- [中国人猛戳这里](https://www.jianshu.com/p/c37b1bdb4757)
- English （not yet）



# Download



You can download a jar from GitHub's [releases page](https://github.com/lamster2018/EasyProtector/releases).



Or use Gradle:

```
repositories {
  jcenter()
  maven()
  google()
}

dependencies {
  implementation 'com.lahm.library:easy-protector-release:latest.release'
}
```



Or maven

```
<dependency>
  <groupId>com.lahm.library</groupId>
  <artifactId>easy-protector-release</artifactId>
  <version>1.0.5</version>
  <type>pom</type>
</dependency>
```



# How do I use it？

EasyProtectorLib.checkIsRoot();

EasyProtectorLib.checkIsDebug();

EasyProtectorLib.checkIsPortUsing();

EasyProtectorLib.checkIsXposedExist();

EasyProtectorLib.checkIsBeingTracedByJava();

EasyProtectorLib.checkIsUsingMultiVirtualApp();

EasyProtectorLib.checkIsRunningInEmulator();

......

More function see

SecurityCheckUtil.class

EmulatorCheckUtil.class

VirtualApkCheckUtil.class

AccessibilityServicesCheckUtil.class


# Proguard

no need



# Compatibility

- Minimum Android SDK: requires a minimum API level of 16.
- CPU: support x86 & arm



# Test

| Phone      | SDK         | ROM             |
| ---------- | ----------- | --------------- |
| RedMi 3s   | Android 6.0 | google eng      |
| Huawei P9  | Android 7.0 | EMUI 5.1 root   |
| Mix 2      | Android 8.0 | MIUI 9 stable   |
| OnePlus 5T | Android 8.1 | H2OS 5.1 stable |



# License
Apache 2.0. See the [LICENSE](https://github.com/lamster2018/EasyProtector/blob/master/LICENSE) file for details.


# About Emulator Detecting

|   机器/测试方案   | 检测结果 |
| :---------------: | -------- |
|   AS自带模拟器 9.0   |      模拟器     |
| Genymotion2.12.1  |     模拟器       |
|  逍遥模拟器6.0.0  |       模拟器      |
|     Appetize      |      模拟器     |
|  夜神模拟器6.2.5.3010  |     模拟器     |
| 腾讯手游助手2.0.6.8 |      模拟器      |
|  雷电模拟器3.41   |     模拟器       |
|  木木模拟器2.0.25   |     模拟器       |
|      一加5T       |       真机     |
|      华为P9       |      真机     |

自2018/6/13集成并上线自己的项目里，至10/24已经收集了11w+疑似模拟器的检测数据，
如果各位需要在业务里做非常细致的模拟器鉴别，可以在自行增加判断条件。

各位老铁提有关xx模拟器检测不出的issue的时候，请尽量附上emulatorInfo信息哈，我的demo里专门给你们打印了，这样方便调试。

![demo capture](https://upload-images.jianshu.io/upload_images/2554175-4fe7325ab886bd7f.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
