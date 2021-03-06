
---
title: 产品
description: 
platform: 产品
updatedAt: Fri Nov 02 2018 04:03:46 GMT+0000 (UTC)
---
# 产品
本页包含 Agora 产品的相关问题。

### 请问你们提供的解决方案包含什么内容？

我们提供的是 PAAS 层的解决方案。简单来说，我们提供一个SDK，里面含有一整套 API，你可以将此 SDK 集成到任何 app 或者网页上，实现音视频通话和直播。我们的 SDK 支持 iOS，Android，Windows，macOS，Linux 和 Web。

### 一般情况下，从集成声网 SDK 开始到产品上线需要多长时间？

跑通 Demo，大致只需要 30 分钟。如果是要集成到 App 里面验证功能，做 POC，一般 1 周左右。

如果要达到上线状态，大致需要 1-4 个月，视具体集成工程复杂度而定。如果需要额外的定制化功能，需要和我们的商务联系，经过技术评估后，才能给出时间预期。

### 声网  SDK 与哪些平台和版本兼容？

声网提供全平台 SDK，包括 iOS，Android，Windows，macOS，Linux，Web，微信小程序等。具体支持版本如下：
* Android：4.1+
* iOS：8.0+
* Windows：XP SP3+
* macOS：10.0+
* 微信小程序：支持
* Web：Chrome 58+；Firefox 56+；Safari 11+；Opera 45+；QQ 10+

### 我能通过使用声网 Agora 的实时云服务在我的程序中实现哪些通讯功能？

* App 之间的音视频通话；
* App 和网页 Web 之间的音视频通话；
* 网页 Web 之间的音视频通话；
* App 与手机落地电话通信（通过第三方合作）

### 声网 Agora 提供点播服务吗？

不提供。声网目前只提供音视频通信和全互动直播和连麦服务。

声网提供人脸识别、美颜和滤镜贴纸服务吗？提供的。可以通过 400 632 6626 或 sales@agora.io 联系我们。

### 声网 Agora 提供鉴黄服务吗？

提供的。可以通过 400 632 6626 或 sales@agora.io 联系我们。

### 声网 Agora 支持自动重连么？

是的，支持。

### 声网 Agora 的通话与音频处理有什么特点？

我们在通话和音频处理上有很多的独特算法，希望用户通话时能真的有”声临其境”的体验。这些特点主要包括主动混音、自动增益控制、话音检测、舒适背景噪声和抗啸叫等。

想亲耳试听，了解我们在声音上的独特优势，可参考 https://www.agora.io/cn/audiocall/ 。

### 声网 Agora 使用什么架构？是点对点（P2P）还是基于服务器的？

声网 Agora 的解决方案当前是基于服务器的，在全球有近 100 个数据中心，它们在公共云上建立了一个新的层次，从而确保了服务质量。

此外，声网 Agora 的算法还能保证通话之间的最佳路由。我们可以根据客户的要求加入 P2P，提供服务器和 P2P 混合方案来满足您的要求。

## 视频

### 视频传输流程

![](https://web-cdn.agora.io/docs-files/1540446528600)

Windows采集一般遵循下面的流程：

![](https://web-cdn.agora.io/docs-files/1540446560600)

## 直播

### Agora 全互动直播和 CDN 有什么区别？

CDN 是传统的单项直播，延迟高，无互动；

Agora 的全互动直播带有主播与主播间，主播与观众间可随时进行实时互动， 具有超低延时保障，真实重现现场。

### Agora 支持海外直播吗？

Agora 已在全球部署数据中心，支持海外直播。

### Agora 直播技术架构有何独特之处？

Agora 底层使用 UDP 传输而非传统的高延迟的 TCP，可以保证低延迟和实时性互动。

### Agora 直播如何支持大并发？

Agora 在全球部署了近百个数据中心，几千台服务器保证亿级并发，同时有国内外顶级的 CDN 厂商作为合作伙伴保证旁路直播的高并发。

### Agora 支持纯音频直播吗？

支持。

### 客户端连麦与服务器端连麦有什么区别？

本质上来说连麦都是通过客户端进行的。区别在于做连麦后的视频合成分发可以有两种方式：

<table>
  <tr>
    <th>方式</th>
    <th>缺点</th>
    <th>优点</th>
  </tr>
  <tr>
    <td>用户在客户端自己合成</td>
    <td>需耗费更大的带宽，对设备要求比较高</td>
    <td>对布局、连麦策略规划的更加精确</td>
  </tr>
  <tr>
    <td>用户在 Agora 服务器端合成</td>
    <td>对布局，连麦策略等支持较差</td>
    <td>保证较小的延时，对设备、带宽要求较小</td>
  </tr>
</table>

### 直播中如何踢人？

目前 App 可以支持服务端踢人功能。具体用法可参考 [Dashboard RESTful API](../../cn/API%20Reference/dashboard_restful_live.md) 。

### 为什么两个主播进入同一个频道却看不见对方？

进行以下检查：

确认两个主播是否使用相同的 App ID，如果厂商注册多个 App ID，容易弄混；
确认两个主播是否进入相同的频道(频道名相同)；
确认两个主播的网络是否正常连接。

### PC 上直播的清晰度分辨率有哪些推荐范围？

PC 上目前最高支持 1080P，但根据场景和接收端的处理能力, 需使用不同的分辨率。

手机上推荐分辨率为 360 * 640，如果观众端接受过高的码率或分辨率，目前版本会造成功耗上升，CPU 处理瓶颈导致卡顿等问题。

后续观众端硬件能力提升后，Agora 可以考虑为 PC 端定制双码率的下发，例如 PAD 和高端手机上显示 720P，低端手机显示 360P。

### 什么是单流观众/主播和双流观众/主播，如何使用？

在直播场景里，Agora 有两种用户角色: 主播和观众，两种角色均有单流和双流 (大流和小流，由分辨率，帧率和码率而定) 模式。

<table>
  <tr>
    <td>单流观众和双流主播</td>
    <td>单流直播仅 发送一路流，而双流直播发送两路流（大流和小流）；</td>
  </tr>
  <tr>
    <td>单流观众和双流观众</td>
    <td>单流观众和双流观众都仅能接收每位主播的一路流，区别是单流观众默认接受大流，双流观众默认接收小流，但均可通过调用 <code>setRemoteVideoStreamType(Android/Windows)</code> 或 <code>setRemoteVideoStream(iOS/macOS)</code> 设置和进行切换。</td>
  </tr>
</table>

不要将单双流模式的用户角色进行混用：

<table>
  <tr>
    <th>角色和模式</th>
    <th>单流主播</th>
    <th>双流主播</th>
  </tr>
  <tr>
    <td>单流观众</td>
    <td>支持</td>
    <td>不支持</td>
  </tr>
  <tr>
    <td>双流观众</td>
    <td>不支持</td>
    <td>支持</td>
  </tr>
</table>

### 双流观众可以同时拿到同一位主播的两路流吗？

不可以，双流观众指的是当主播发送双流时，用户可以从主播发送的两条流里选择接收其中 1 条：

* 观众只能接收每位主播的 1 路流；
* 观众拿到某位主播的这一路流，是由观众 SDK 调用 `setRemoteVideoStreamType` 接口设置而定的；
* 单流观众和双流观众的区别: 单流观众默认收到的是主播的大流；双流观众默认收到的是主播的小流。默认指的是: 观众没有调用 `setRemoteVideoStreamType` 接口之前。

### 主播和观众的单流或双流可以混用吗？

不可以，仅支持：

* 单流主播 + 单流观众
* 双流主播 + 双流观众

### 观众连麦有没有限制？如果没有，万一 App 遭到攻击怎么办？

Agora 提供了一套连麦鉴权方案，确保即便 App 安全系统遭受攻击，也不会出现观众任意扰乱直播的情况。有需求的客户，请联系 sales@agora.io 。

### 推流失败后，是否有重推机制?

有，推流失败后，每 2 秒重试一次。

### 为什么推流录制的最后出现 30 秒的卡顿?

为了防止主播断线或临时退出加入等情况造成 rtmp 断流，录制服务默认会预留 30s 用于缓冲静态数据，在主播退出 30s 后才完全退出推流录制。

### 为什么设置分辨率为 640 x 360，实际为 640 x 352？

由于 Android 机型较多，受部分编码器限制，只支持视频宽度是 16 的倍数，所以我们统一将分辨率设置为 16 的倍数 例如宽度为 360 时，实际上宽度为 352。

### 使用 CDN 测试地址时，为什么会有跨域问题？

测试地址使用的域名主要应用在测试环境，由于 CDN 上没有配置 cross.xml，因此会有跨域问题出现。

### 使用旁路直播时，建议使用什么 H5/Flash 播放器？

建议使用 video.js 或者 jwplayer， 测试时可以使用 Agora.io 提供的测试页面：
http://broadcastapp.agora.io/test.html.

### 如何调整旁路直播的布局？

请参考各平台 API 文档中 `setLiveTranscoding` 接口的描述。

### 可以指定旁路直播的分辨率和码率吗？

可以，但因为指定分辨率/码率需要推流时重新解码编码，所以可能需要额外的开销：

* 场景 1: 对于两位主播以上的场景，因为合流本身也需要重新编码解码，所以没有额外开销；
* 场景 2: 对于单人主播，指定分辨率/码率有额外开销。

### 旁路直播的观众和用 Agora 直播 SDK 的观众有什么区别？

Agora 直播里有三种用户：

* 主播
* 高级观众
* 普通观众

### 前两者需要用 Agora SDK，第三种只需要有网页浏览器。与普通观众相比，高级观众有以下不同：
* 观看延迟更小
* 抗丢包能力更强
* 可以切换为主播进行连麦

### 可以推到厂商自己的 CDN 吗？

技术上可行，但需要和 BD 联系，确认需求。

### 纯音频的直播也可以旁路直播吗？

支持。

### 旁路直播有流量限制吗？

旁路直播的 URL 分为测试和正式两种：
* 测试: 申请后立即开通、可能不稳定、有效期一周、不计费、并发限制 5 路。
* 正式: 申请后 4 个工作日开通、稳定、有效期随合同、计费、无并发路数限制。

### 为什么旁路直播和旁路直播的录制内容里只听得到声音，却看不到视频?

检查一下 API `setLiveTranscoding` 是否已正确调用。

### 是否支持主播多路视频同时直播显示？

是的，实现方法如下：

* APP 负责采集屏幕和主播摄像，把屏幕和主播摄像混合成一路输入 Agora SDK(此处不再建议使用 SDK 自带的截屏输出流，合图再输入的方式实现，会有额外的效率损失，关于 PC 端屏幕采集的原理 Agora 会提供技术支持)
* 主播在 PC 端进行直播的同时，在手机 APP 端主播以嘉宾的身份登录，把手机视频以嘉宾连线方式进入小窗口。
* PC 端应用程序用嘉宾连线的方式，把主播的一路视频连入直播室。

### Agora 支持给直播视频打水印吗？

支持。Agora 从 v2.2.0 开始支持在本地直播或转码直播过程中，将本地的一张 png 图片添加到正在直播的视频上。具体用法详见各平台 API 文档中下列 API 的用法描述：

* 本地直播推流：`addVideoWatermark`
* 直播转码推流：`setLiveTranscoding`

### Agora 支持直播视频敏感内容的自动检测吗？

是的，Agora 支持以下两种方式：

* 直接对视频敏感内容进行鉴定；
* 将视频敏感内容截图发给厂商进行鉴定；

### 观众在直播间的时长数据，可以拿到吗？

推荐通过信令层自行统计，后续 Agora 将提供非实时对账接口。

### 是否有推流失败错误码？

使用旁路直播推流状态回调 `onStreamPublished(string url, int error)`，该回调用于通知主播是否推流成功。

参数url主播推流的 HTTP/HTTPS 地址，error错误代码，详细定义见 Error codeERR_TIMEOUT(10)：推流超时未成功。ERR_ALREADY_IN_USE(19)：推流地址已经在推流 ERR_ENCRYPTED_STREAM_NOT_ALLOWED_PUBLISHED(130)：推流已加密不能推流。

### 是否可以推多路CDN 地址？

频道内多次推流/推多路流的说明： 

多个主播同时推同一个地址： 不可以
多个主播同时推不同的地址： 可以
一个主播同时推多个不同的址址： 可以

### 推纯音频，旁路推流为什么要加一个16X16的，bitrate为1的小图片？ 

这是由旁路端的播放器决定的，正常的播放器 VLC、 ffmpeg 都是需要等到有视频才会播放。 为了解决这个问题所以才加个图片的。 至于16X16，bitrate=1， 是为了不会产品视频流量，不会产生视频费用。

## 录制

### 录制文件命名方式

录制文件保存目录命名规则：“ChannelID+目录生成时间”（UTC时间）
录制文件命名规则：”用户UID+文件生成年月日时分秒毫秒“（UTC时间）

## 信令

### Login 过程关键点

* 用户登录到信令服务器，登录后即在线
* 不用 token 也能登录信令系统，token 用  `_no_need_token`
* 已经 `login`，再次 `login` 会被忽略
* 调用 login 之后，无需等到login成功，即可调用其他方法。这些操作等到 login 成功后发送。如果 `login` 失败，这些操作会失败
* `login` 之后，如果没有网络问题或者主动 logout，会一直在 `login` 状态。没有超时自动 `logout` 的机制
* 一个用户只能同时登录一台设备，后登录的设备会踢掉之前登录的设备，被踢设备能收到回调（暂时不支持多终端在线）
* 用 java  信令调用的 `login` 返回的 uid 是负数可以转换一下 `getUid()`& `0XFFFFFFFFL`

### Logout 过程关键点

* 调用 `logout` 之后，无需收到 `logout` 成功回调，可再次调用 `login` 以及其他操作
* 断网重连：用户配置重连时间和重连次数，满足任一条件，即会 `logout`
* 两分钟之内掉线会重连，实际测试是 64-65 秒就 `logout`
* app 在后台/锁屏 状态，默认是被系统挂起的，信令会掉线，客户自己做保活也没用

### Token关键点

通常用户需要自己的账号系统，用来完成注册、登录密码验证、更换密码、密码找回、头像之类的功能。因此用户通常会有自己的账号服务器，里面存有 Agora 的 SignKey。

* 向Agora信令服务器登录时，并不验证 Agora 账号是否存在，用户可以使用多种方式的Agora账号，比如 UID、GUID、昵称、邮箱之类的，只要是文本就可以，小于64个字符。
* 登录成功后，就可以用账号来访问呼叫、Channel、消息等功能。

## Web SDK

### 浏览器兼容性相关：

* Google Chrome 浏览器，Chrome 58 及以上版本（仅支持 HTTPS）
* Firefox 浏览器，Firefox 56 及以上版本（仅支持 HTTPS）
* Opera 浏览器，Opera 45 及以上版本（仅支持 HTTPS）
* Safari 浏览器，Safari 11 及以上版本（仅支持 HTTPS）
* 电脑版 QQ 浏览器，最新版本（仅支持 HTTPS）
* 2.4及之后的版本SDK  XP系统支持且仅支持 chrome 49（使用 chrome 49时 建议客户去掉检测浏览器兼容性的接口   `checkSystemRequirements` ，不然会报不支持） 
* 在浏览器上调试的时候请不要模拟手机调试，这种方式目前暂不支持

### 在安卓设备上使用 Chrome 浏览器，无法与 Native 及 Safari 浏览器互通?

由于 Safari 浏览器通过使用 H.264 视频编码来运行，因此所有 Safari 浏览器上的通话都需要支持该编码。然而当前安卓设备上的 Chrome 浏览器 61 之后的版本有个 bug ，会阻止设备给其他通话方发送 H.264 编码， 因此远端的通话方在屏幕上看不到直播的视频，而只能看到一个黑色窗口。 安卓设备上的 Chrome 浏览器可以解码来自其他通话方发来的 H.264 编码。

该问题会在 Chrome 浏览器后续版本中解决，我们会持续关注该问题的进展。更多信息详见：https://bugs.chromium.org/p/chromium/issues/detail?id=761336

另外，安卓设备的 Chrome 浏览器上也可能会出现通话者只听到声音，但看不到图像的情况。安卓 Chrome 浏览器会在 57 版本中支持解码 H.264。目前安卓手机中只有高通（Kitkat 及以后版本）和三星猎户座（Lollipop 及以后版本）的芯片支持解码 H.264。更多信息详见：https://groups.google.com/forum/#!msg/discuss-webrtc/xXjeKbW_JYI/LIXzVrKWCwAJ

### 浏览器版本更新相关：

即将发布的 chrome 70 版本中，2.4 之前的 SDK 中 `getAudioLevel` 接口调用会失效，因为 chrome 对这一块的策略做了变更（调用接口前 7 秒内必须要点击一下屏幕），2.4 SDK 可以正常调用 `getAudioLevel`。

### Web SDK 简单实现逻辑是什么？

createClient → Client.init()  →  Client.join() → Client.createStream() → Stream.setVideoProfile() → Stream.init() → Stream.play() → Client.publish() →  Client.subscribe()→ leave
![](https://web-cdn.agora.io/docs-files/1540533706082)

### 何时会触发 Stream-Removed 事件？
`stream-removed` 回调触发逻辑：A 端 publish 之后调用 unpublish ，B 端触发 `stream-removed`；或者 B 端 10 秒内没有收到 A 端（这个时候A应该是异常断开的状态）的音视频流也会触发 `stream-removed`。

## Native SDK

### API执行时序

#### leaveChannel 方法实现过程介绍

客户 APP 向 SDK 发送 `leaveChannel` 请求，SDK 会向 SD-RTN 发送 `quit`，如果引擎顺利退出频道则向 APP 返回`onleaveChannel`。

什么情况可能导致用户APP收不到onleaveChannel()回调？

* 用户关闭应用程序；
* 用户退出房间时应用程序突然 hang；
* 用户手机突然断网。

` leaveChannel` 具体过程请参见下图

![](https://web-cdn.agora.io/docs-files/1540448888144)

 #### destroy 方法实现过程介绍

该方法为同步方法，因此不要在主线程中调用或者在回调中直接调用，不然会导致应用阻塞。

`destroy` 方法要销毁引擎彻底释放底层资源，根据经验通常需要 1-3 s 的时间（根据不同设备具体时间不同），因此建议用户在APP 层增加逻辑，防止用户销毁引擎的过程中再调用引擎进行通话等操作，提高应用的健壮性的同时降低系统崩溃隐患。


### 日志框架

#### 日志级别

建议上线前项目调试阶段输出全量日志（DEBUG 级别日志），便于问题排查。

建议上线后只打印 INFO，ERROR，WARNING 级别的日志，不输出 CRITICAL，DEBUG 级别的日志，这样的好处是：

* 上线后CRITICAL问题相对较少
* 减少日志文件大小
* 降低日志线程对CPU的消耗
* 降低内存占用率

具体设置方法：调用 `setLogFilter` 设置 SDK 输出日志的过滤器，不同过滤器可以使用不同的组合，日志级别顺序依次为 OFF、CRITICAL、ERROR、WARNING、INFO 和 DEBUG

设置过滤器等级：

LOG_FILTER_OFF(0)：不输出任何日志
LOG_FILTER_DEBUG(0x80f)：输出所有的 API 日志
LOG_FILTER_INFO(0x0f)：输出 CRITICAL、ERROR、WARNING、INFO 级别的日志
LOG_FILTER_WARNING(0x0e)：仅输出 CRITICAL、ERROR、WARNING 级别的日志
LOG_FILTER_ERROR(0x0c)：仅输出 CRITICAL、ERROR 级别的日志
LOG_FILTER_CRITICAL(0x08)：仅输出 CRITICAL 级别的日志

最佳实践是默认配置：即只设置`setLogfile`：setInt（ “rtc.log_filter”, filter&LOG_FILTER_MASK ）只打印INFO+ERROR+WARNING日志，不输出 DEBUG

