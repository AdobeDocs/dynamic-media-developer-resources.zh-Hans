---
description: 缩放目标图像目录中的数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
seo-description: 缩放目标图像目录中的数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
seo-title: 目标
solution: Experience Manager
title: 目标
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 7%

---


# 目标{#targets}

缩放目标图像目录中的数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

将返回`catalog::Targets`的内容。 当请求“text”格式时，`catalog::Targets`中`??`的所有实例都由行终结器替换，并在末尾附加单行终结器(`CR/LF`)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终结器组成。 在请求“xml”或“json”格式时，会应用适当的格式。

请求字符串中的其他命令将被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
