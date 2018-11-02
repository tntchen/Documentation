
---
title: 离开频道
description: 
platform: Windows
updatedAt: Thu Nov 01 2018 08:20:32 GMT+0000 (UTC)
---
# 离开频道
# 离开频道
通话或直播结束时，调用 <code>leaveChannel</code> 方法离开频道。

不论当前是否还在通话中，调用该方法会把会话相关的所有资源释放掉。真正退出频道后，SDK 会触发 <code>onleaveChannel</code> 回调。

> 如果在调用 <code>leaveChannel</code> 方法后立即使用 <code>release</code>，则退出频道会被打断，SDK 也不会触发 <code>onleaveChannel</code> 回调。

```
int nRet = m_lpAgoraEngine->leaveChannel();
```