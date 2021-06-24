---
description: 缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 8%

---

# 目标{#targets}

缩放图像目录中的目标数据。 返回在URL路径中指定的图像目录条目的缩放目标数据。

`req=targets[,text|{xml[, *``*]}|{json[&id= *`encodeingreqId`*]}]`

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

返回`catalog::Targets`的内容。 当请求“text”格式时，`catalog::Targets`中`??`的所有实例都由行终止符替换，并在末尾附加单行终止符(`CR/LF`)。 如果URL路径未解析为有效的目录条目，则响应只包含单个行终结器。 请求“xml”或“json”格式时，会应用适当的格式。

请求字符串中的其他命令将被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法来指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。只允许使用a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
