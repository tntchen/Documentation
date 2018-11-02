
---
title: Web SDK 相关
description: 
platform: Web SDK 相关
updatedAt: Thu Nov 01 2018 08:10:06 GMT+0000 (UTC)
---
# Web SDK 相关
# Web SDK 相关

### H264 模式下，在 macOS 上用 Firefox 浏览器加入通话，打开小流时，获取的分辨率与大流一致？

H264模式下，在 macOS 设备上使用 Firefox 打开小流时，获取的分辨率与大流相同；如果是 VP8 模式，则没有此问题。我们会持续关注并更新在该问题上的进展。

### 在 macOS 上用最新的 Firefox 浏览器（v59.01 版本）加入通话，只能看到本地视频，看不到对方视频？

macOS 上, 使用 v59.01 版本的 Firefox 浏览器加入通话或直播时，会出现只能看到本地视频，看不到对方视频的问题。这个问题目前在 Web SDK 2.1 Hotfix 版本上已解决。

### 两台电脑和一台手机互通时，手机出现屏幕卡住的情况，按 home 键也无法退出?

当 Safari 浏览器、 Chrome 浏览器和移动端加入通话时，有可能会在移动端出现页面冻结或卡住的情况。这是由 Chrome 浏览器发出的 H.264 视频编码导致的。这个问题在使用 Safari 台式电脑与 Safari iOS 互通时不会出现。更多信息，详见：

http://bugs.webkit.org/show_bug.cgi?id=176439
http://bugs.webkit.org/show_bug.cgi?id=178357

### 在安卓设备上使用 Chrome 浏览器，无法与 Native 及 Safari 浏览器互通?

由于 Safari 浏览器通过使用 H.264 视频编码来运行，因此所有 Safari 浏览器上的通话都需要支持该编码。然而当前安卓设备上的 Chrome 浏览器 61 之后的版本有个 bug ，会阻止设备给其他通话方发送 H.264 编码，因此远端的通话方在屏幕上看不到直播的视频，而只能看到一个黑色窗口。

安卓设备上的 Chrome 浏览器可以解码来自其他通话方发来的 H.264 编码。

该问题会在 Chrome 浏览器后续版本中解决，我们会持续关注该问题的进展。更多信息详见：
https://bugs.chromium.org/p/chromium/issues/detail?id=761336

另外，安卓设备的 Chrome 浏览器上也可能会出现通话者只听到声音，但看不到图像的情况。安卓 Chrome 浏览器会在 57 版本中支持解码 H.264。目前安卓手机中只有高通（Kitkat 及以后版本）和三星猎户座（Lollipop 及以后版本）的芯片支持解码 H.264。更多信息详见：
https://groups.google.com/forum/#!msg/discuss-webrtc/xXjeKbW_JYI/LIXzVrKWCwAJ

### 网页端视频过程中，接了个QQ电话，再回来网页视频时，就发送不出音频了?

在 Web 端使用浏览器通话过程中，如果有第三方 app 占用音频设备（如系统接听 QQ 电话等），再切换回 Web 端通话时，将无法发送音频信号。建议您退出后重新连接。

### Mac 和 Windows 上均使用 Chrome 浏览器通话，如果 Windows 端切换 Wi-Fi, Mac 端画面卡住？

当在 Mac 端和 Windows 端均使用 Chrome 浏览器通话时，若果在 Windows 端切换连接的 Wi-Fi，Mac 端的画面会卡住，需刷新界面后才能恢复画面，但是 Windows 端就不受影响。该问题预计两周后修复。

### 通话或直播过程中在 iOS 11 的 Safari 浏览器端开启双流后本地窗口黑屏，另一端也接收不到 iOS 端的画面？

iOS 端 Safari 浏览器目前支持双流有限制，双流功能在此浏览器下的支持受到 Safari 浏览器本身的限制，造成设置不生效或异常现象。我们会持续关注该问题的进展。

### Web SDK join channel 参数数据类型因版本变化有差异，导致加入 channel 失败，报 websocket error，同时会产生类似 ddos 的攻击，短时间巨量的ws的连接？

Web SDK 1.12 及之后的版本中，Join() 增加了Channelkey的属性，https://docs.agora.io/cn/2.0/product/Video/API%20Reference/web_API_video?platform=Web 。

Web SDK 1.12 之前的版本中 Join() 中无此属性，https://docs.agora.io/cn/1.8/user_guide/API/webrtc_api.html 。代码集成时，需要注意此处改动。

### h264_interop 模式下，Firefox 浏览器作为发送端时，接收端切换小流失败？

小流切换与浏览器类型、分辨率、编解码类型相关。各浏览器会根据自己浏览器的内部算法进行调整，因此在进行小流切换时，某些分辨率下会出现小流切换与预计不一致的现象。

### 直播场景中，在 AgoraRTC.createClient({mode: ‘interop’}) 模式下，Web 单主播如果不设置转码推流，就没有视频？

在 AgoraRTC.createClient({mode: ‘interop’}) 模式下，如果使用单 Web 主播进行推流，需要将 Web 单主播的码流进行转码后再进行推流，否则会出现没有视频的现象。

若要对 Web 单主播直接进行推流，请使用 AgoraRTC.createClient({mode: ‘h264_interop’}) 模式。

影响：Agora 转码需要收取转码费用。

### 直播过程中，Safari 浏览器播放第三方音乐后直播音频异常？

经测试分析，使用第三方应用播放音频之后，再切回音视频通话，会导致 Safari 的音视频通话受影响。目前考虑，可能是由于 Safari 近期的更新引起的，我们会持续关注并跟进该问题的最新进展。更多信息，请见：
https://bugs.webkit.org/show_bug.cgi?id=179964

### 在 Web 端使用 Firefox 浏览器设置 video profile 进入频道不生效？

在 Web 端使用 Firefox 浏览器时，我们发现部分机器设置的 video profile 会不生效，这个问题目前分析是由于电脑和浏览器的兼容问题导致的。目前统计到的设备和现象包括：

* Macbook Pro(13-inch, 2016, Two Thunderbolt 3 ports) 打开 Firefox，打开 Web Premium，选择任意一个 video profile 加入频道。进入后 Mac Forefox 发送的都是 720p，之前设置的 video profile 不生效；
* Windows 10 (MI)，打开 Firefox，打开 Web Premium，选择任意一个 video profile 加入频道。进入后 Windows Firefox 发送的 video profile 与设定的不一致；

我们会持续关注此问题的最新进展。并持续更新异常设备列表。如果您在使用中遇到此类问题，请将问题反馈给 Agora 客户服务。

### iOS 端无法使用 getAudioLevel 方法获取音量？

经测试分析，iOS Safari 端无法使用 getAudioLevel 方法来获取音量，这是由浏览器本身的限制所造成的，我们会持续关注此问题的最新进展。

### Web SDK 支持 iFrame 吗？为何我使用 Chrome 时在 iFrame 里 Stream 无法 init 成功？

Web SDK 是支持 iFrame 的。根据 Chrome 策略，iFrame 需加上额外的权限。例如：`<iframe src="..." allow="microphone; camera"></iframe>`。

### 使用华为 P10(VTR-AL00) 进入频道出现黑屏无画面？

因为华为 P10(VTR-AL00) 不支持 Web RTC。

### 黑屏

当 Agora Native SDK 和 Web 用户加入同一直播频道时，PC 或移动端用户可以看见本地和远端视频，但网页端用户看到的远端视频为黑屏。

PC 或移动端用户 (即使用 Agora Native SDK 的用户) 在直播场景下必须调用 API `enableWebSdkInteroperability` 打开互通功能。

### 报错

一般来说, 您可以根据 Agora Web SDK 查看所有错误消息以及其对应的描述。该描述正在不断完善中。

以下列出了常见问题的解决方案：

#### 设备限制

当 SDK 返回 Media access: OverconstrainedgetUserMedia failed Object { type=”error”, msg=”Overconstrained”/”CONSTRAINT_NOT_SATISFIED”时:

该问题通常是由于用户的设备限制引起的。请执行以下自检操作：

调用 API `setVideoProfile` 调整视频分辨率，例如, 摄像头无法获取 720P 或 1080P 数据。

升级浏览器。详见  [设置开发环境](../../cn/Quickstart%20Guide/web_prepare.md) 。

#### 没有摄像头

当 SDK 返回 Uncaught TypeError: Cannot read property ‘0’ of null 时：

该问题可能是由于没有摄像头导致的。在调用 `createStream` 时请将参数 video 设为 false。

#### 缺少库

当 SDK 返回 Uncaught ReferenceError: is not defined 时：x'w'w'w

请根据 webrtc_deploy 引用所需的延伸库。

#### 浏览器相关

当 SDK 返回 getUserMedia() no longer works on insecure origins. To use this feature, you should consider switching your application to a secure origin, such as HTTPS时：请根据 [设置开发环境](../../cn/Quickstart%20Guide/web_prepare.md) 使用 https 部署网页，而非 http。


