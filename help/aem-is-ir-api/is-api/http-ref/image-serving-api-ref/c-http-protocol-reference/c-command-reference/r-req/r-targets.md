---
description: 从图像目录缩放目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 8%

---

# 目标{#targets}

从图像目录缩放目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。

`req=targets[,text|{xml[, *`编码`*]}|{json[&id= *`reqId`*]}]`

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

的内容 `catalog::Targets` 会返回。 请求&#39;text&#39;格式时，的所有实例 `??` 在 `catalog::Targets` 替换为行终结符和单行终结符( `CR/LF`)将附加到末尾。 如果URL路径未解析为有效的目录条目，则响应仅由单行终止符组成。 在请求“xml”或“json”格式时，将应用相应的格式。

请求字符串中的其他命令将被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用扩展语法指定JS回调处理程序的名称 `req=` 参数：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。 仅允许a-z、A-Z和0-9字符。 可选. 默认值为 `s7jsonResponse`.
