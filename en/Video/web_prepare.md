
---
title: Integrate SDK
description: 
platform: Web
updatedAt: Thu Nov 01 2018 08:46:19 GMT+0000 (UTC)
---
# Integrate SDK
# Integrate SDK

This page contains information on how to prepare the development environment before enabling a video call with the Agora Web SDK.

## <a name = "pre"></a>Prerequisites

1. Install a browser supported by Agora Web SDK as shown in the following table:
  <table>
  <tr>
    <th>Platform</th>
    <th>Chrome 58+</th>
    <th>Firefox 56+</th>
    <th>Safari 11+</th>
    <th>Opera 45+</th>
    <th>QQ Browser Latest</th>
    <th>360 Security  Browser</th>
    <th>Wechat Built-in Browser</th>
  </tr>
   <tr>
    <td>Android 4.1+</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
		<td><b>N/A</b></td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
  </tr>
  <tr>
    <td>iOS 11+</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
    <td><font color="green">✔</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
  </tr>
  <tr>
    <td>macOS 10+</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="red">✘</td>
    <td><font color="red">✘</td>
  </tr>
  <tr>
    <td>Windows 7+</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
		<td><b>N/A</b></td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="green">✔</td>
    <td><font color="red">✘</td>
  </tr>
</table>

> Agora Web SDK 2.5 also supports Chrome 49 on Windows XP.

2. Connect to the specified ports and whitelist domains as described in [Firewall Requirements](../../en/Agora%20Platform/firewall.md).
3. Understand the limitations in [Known Issues](../../en/Video/release_web_video.md) and [FAQ](https://docs.agora.io/en/2.4.1/faq/faq/web).

## Creating an Agora Account and Getting an App ID

1. Create a developer account at [www.agora.io](https://dashboard.agora.io/signin/) to login to **Dashboard**.

2. Click **Add New Project** on the **Projects** page of the Dashboard.

   <img alt="../_images/appid_1.jpg" src="https://web-cdn.agora.io/docs-files/en/appid_1.jpg" style="width: 1142.0px; height: 360.0px;"/>

1. Fill in the **Project Name** and click **Submit**.

2. Find the **App ID** under the created project. You will need it to enable a video call.

   <img alt="../_images/appid_2.jpg" src="https://web-cdn.agora.io/docs-files/en/appid_2.jpg" style="width: 1138.0px; height: 344.0px;"/>



## Importing the Agora Web SDK to Your Project

Choose one of the following two methods to obtain the Agora Web SDK:

### Method 1: Getting the SDK through the CDN

Add `<script src="http://cdn.agora.io/sdk/web/AgoraRTCSDK-2.4-latest.js”></script>` to the line above `</body>` in your project.

<img alt="../_images/web_sdk_cdn.png" src="https://web-cdn.agora.io/docs-files/en/web_sdk_cdn.png" style="width: 859.2px; height: 78.0px;"/>

### Method 2: Getting the SDK from the official Agora website

1. [Download](https://docs.agora.io/en/Agora%20Platform/downloads) the latest Agora Web SDK.

   <img alt="../_images/web_sdk_download.png" src="https://web-cdn.agora.io/docs-files/en/web_sdk_download.png" style="width: 393.3px; height: 92.15px;"/>

2. Copy the `AgoraRTCSDK-2.4.js` file to your project.

3. Reference the `AgoraRTCSDK-2.4.js` file in your project.

   <img alt="../_images/web_sdk_reference.jpeg" src="https://web-cdn.agora.io/docs-files/en/web_sdk_reference.jpeg" style="width: 851.2px; height: 120.0px;"/>

> The screenshots are for reference only, please use the latest version of the SDK.

## Preparing the Web Server

1. Install a web server, such as Apache, Nginx, or Node.js.
2. Import the downloaded Agora Web SDK to your web server.
3. Set up your web server properly so that you can access the sample app page or your own app page on the supported browsers, see [Prerequisites](#pre) .

The Web environment is now set to use the Agora SDK.