---
description: 缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
seo-description: 缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
seo-title: 目标
solution: Experience Manager
title: 目标
topic: Scene7 Image Serving - Image Rendering API
uuid: e20dcd2c-913a-4153-97c7-dfb190763e39
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 目标{#targets}

缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。

`req=targets[,text|{xml[, *`encodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

返回的 `catalog::Targets` 内容。 当请求“text”格式时，所有in实例都由行终止符 `??` 替 `catalog::Targets` 换，并在结尾处附加一个单行终止符( `CR/LF`)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终结器组成。 当请求“xml”或“json”格式时，会应用相应的格式。

请求字符串中的其他命令将被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用参数的扩展语法指定JS回调处理函数的 `req=` 名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。 仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
