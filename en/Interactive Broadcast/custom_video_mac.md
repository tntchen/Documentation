
---
title: Customize the Video Source and Renderer
description: 
platform: macOS
updatedAt: Fri Nov 02 2018 04:10:20 GMT+0000 (UTC)
---
# Customize the Video Source and Renderer
## Scenario Description

The Agora SDK provides access to the default camera configuration. To extend the functionality, Agora provides access to customize the video source.

- To add new functions in the SDK for the camera’s video source, such as image enhancement or using the preprocessing library.
- If an app contains a video module, the video source can be customized for code reuse.
- To use non-camera video sources, such as recorded screen data.
- Flexible video capturing device resource allocation to avoid conflicts with other services.

## Integrate the Agora SDK

See [Integrate SDK](../../en/Interactive%20Broadcast/mac_video.md) .

## Customize the Video Source

Step 1. Implement the `AgoraVideoSourceProtocol` to create the customized video source class:

- Specify the buffer type in `bufferType`.

  ```c++
  - (AgoraVideoBufferType)bufferType;
  ```

- Save the AgoraVideoFrameConsumer object in `shouldInitialize`.

  ```c++
  - (BOOL)shouldInitialize;
  ```

- Send the video frame after `shouldStart`.

  ```c++
  - (void)shouldStart;
  ```

- Send the data to the media engine through `AgoraVideoFrameConsumer`.

- Stop sending the frame in `shouldStop`.

  ```c++
  - (void)shouldStop;
  ```

- Remove the frame in `shouldDispose`.

  ```c++
  - (void)shouldDispose;
  ```

Step 2. Create the customized video source object.

Step 3. Pass the external video source to the media engine by Set the Video Source \(`setVideoSource`\).

```c++
- (void)setVideoSource:(id<AgoraVideoSourceProtocol>_Nullable)videoSource;
```

Step 4. The media engine implements the methods in `AgoraVideoSourceProtocol`.

## Customize the Video Sink

Step 1. Call `bufferType` and `pixelFormat` to set the buffer type and pixel format of the video frame.

Step 2. Implement `shouldInitialize`, `shouldStart`, `shouldStop`, and `shouldDispose` to manage the customized video sink.

Step 3. Implement the buffer type and pixel format as specified in Step 1 of `AgoraVideoFrameConsumer`.

Step 4. Create the customized video sink object.

Step 5. Call the `setLocalVideoRenderer` and `setRemoteVideoRenderer` methods to set the local and remote renderers.

Step 6. The media engine will call functions in `AgoraVideoSinkProtocol` according to its internal state.
