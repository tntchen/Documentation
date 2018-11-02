
---
title: 错误代码和警告代码
description: 
platform: All Platforms
updatedAt: Thu Nov 01 2018 08:53:36 GMT+0000 (UTC)
---
# 错误代码和警告代码
# 错误代码和警告代码

<table>
<colgroup>
<col/>
<col/>
<col/>
</colgroup>
<tbody>
<tr><td><strong>错误代码</strong></td>
<td><strong>值</strong></td>
<td><strong>描述</strong></td>
</tr>
<tr><td>SUCCESS</td>
<td>0</td>
<td>没有错误</td>
</tr>
<tr><td>LOGOUT_E_OTHER</td>
<td>100</td>
<td>未知原因导致退出登录，通常是由于网络问题引起的</td>
</tr>
<tr><td>LOGOUT_E_USER</td>
<td>101</td>
<td>用户登出</td>
</tr>
<tr><td>LOGOUT_E_NET</td>
<td>102</td>
<td>网络问题</td>
</tr>
<tr><td>LOGOUT_E_KICKED</td>
<td>103</td>
<td>该账户已在别处登录</td>
</tr>
<tr><td>LOGOUT_E_PACKET</td>
<td>104</td>
<td>已被弃用</td>
</tr>
<tr><td>LOGOUT_E_TOKENEXPIRED</td>
<td>105</td>
<td>SignalingToken 过期</td>
</tr>
<tr><td>LOGOUT_E_OLDVERSION</td>
<td>106</td>
<td>已被弃用</td>
</tr>
<tr><td>LOGOUT_E_TOKENWRONG</td>
<td>107</td>
<td>已被弃用</td>
</tr>
<tr><td>LOGOUT_E_ALREADY_LOGOUT</td>
<td>108</td>
<td>在处于登出状态时再次调用了 logout()</td>
</tr>
<tr><td>LOGIN_E_OTHER</td>
<td>200</td>
<td>原因未知</td>
</tr>
<tr><td>LOGIN_E_NET</td>
<td>201</td>
<td>网络问题</td>
</tr>
<tr><td>LOGIN_E_FAILED</td>
<td>202</td>
<td>被服务器拒绝</td>
</tr>
<tr><td>LOGIN_E_CANCEL</td>
<td>203</td>
<td>用户已取消登录</td>
</tr>
<tr><td>LOGIN_E_TOKENEXPIRED</td>
<td>204</td>
<td>SignalingToken 过期，登录被拒</td>
</tr>
<tr><td>LOGIN_E_OLDVERSION</td>
<td>205</td>
<td>已被弃用</td>
</tr>
<tr><td>LOGIN_E_TOKENWRONG</td>
<td>206</td>
<td>SignalingToken 无效</td>
</tr>
<tr><td>LOGIN_E_TOKEN_KICKED</td>
<td>207</td>
<td>用户已使用更新后的 SignalingToken 在别处登录了系统</td>
</tr>
<tr><td>LOGIN_E_ALREADY_LOGIN</td>
<td>208</td>
<td>用户已登录，再次发起登录会触发该错误。可以忽视该错误</td>
</tr>
<tr><td>LOGIN_E_INVALID_USER</td>
<td>209</td>
<td>用户名不合法</td>
</tr>
<tr><td>JOINCHANNEL_E_OTHER</td>
<td>300</td>
<td>加入频道失败未知错误</td>
</tr>
<tr><td>SENDMESSAGE_E_OTHER</td>
<td>400</td>
<td>发送消息失败未知错误</td>
</tr>
<tr><td>SENDMESSAGE_E_TIMEOUT</td>
<td>401</td>
<td>发送消息超时</td>
</tr>
<tr><td>QUERYUSERNUM_E_OTHER</td>
<td>500</td>
<td>查询频道用户号码失败</td>
</tr>
<tr><td>QUERYUSERNUM_E_TIMEOUT</td>
<td>501</td>
<td>查询频道用户号码超时</td>
</tr>
<tr><td>QUERYUSERNUM_E_BYUSER</td>
<td>501</td>
<td>已被弃用</td>
</tr>
<tr><td>LEAVECHANNEL_E_OTHER</td>
<td>600</td>
<td>未知原因导致退出频道</td>
</tr>
<tr><td>LEAVECHANNEL_E_KICKED</td>
<td>601</td>
<td>被管理员踢出频道</td>
</tr>
<tr><td>LEAVECHANNEL_E_BYUSER</td>
<td>602</td>
<td>用户不在频道内</td>
</tr>
<tr><td>LEAVECHANNEL_E_LOGOUT</td>
<td>603</td>
<td>登出时被踢出频道</td>
</tr>
<tr><td>LEAVECHANNEL_E_DISCONN</td>
<td>604</td>
<td>网络问题导致退出频道</td>
</tr>
<tr><td>INVITE_E_OTHER</td>
<td>700</td>
<td>呼叫失败</td>
</tr>
<tr><td>INVITE_E_REINVITE</td>
<td>701</td>
<td>重复呼叫</td>
</tr>
<tr><td>INVITE_E_NET</td>
<td>702</td>
<td>网络问题</td>
</tr>
<tr><td>INVITE_E_PEEROFFLINE</td>
<td>703</td>
<td>对方处于离线状态</td>
</tr>
<tr><td>INVITE_E_TIMEOUT</td>
<td>704</td>
<td>呼叫超时</td>
</tr>
<tr><td>INVITE_E_CANTRECV</td>
<td>705</td>
<td>已被弃用</td>
</tr>
<tr><td>GENERAL_E</td>
<td>1000</td>
<td>一般错误</td>
</tr>
<tr><td>GENERAL_E_FAILED</td>
<td>1001</td>
<td>一般错误 - 失败</td>
</tr>
<tr><td>GENERAL_E_UNKNOWN</td>
<td>1002</td>
<td>一般错误 - 未知</td>
</tr>
<tr><td>GENERAL_E_NOT_LOGIN</td>
<td>1003</td>
<td>一般错误 - 操作前没有登录</td>
</tr>
<tr><td>GENERAL_E_WRONG_PARAM</td>
<td>1004</td>
<td>一般错误 - 参数调用失败</td>
</tr>
</tbody>
</table>



