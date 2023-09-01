---
title: 地图
description: 图像映射数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 9%

---

# 地图{#map}

图像映射数据。

`req=map[,text|{xml[, *`编码`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

返回 `catalog::Map` 在查询未指定其他命令的简单目录条目时未进行修改(不缩放到 `catalog::maxPix`)。

如果在请求中指定了任何其他命令，则会返回复合图像映射。 合成图像映射通过缩放、裁剪、旋转和分层全部导出 `catalog::Map` 和/或 `map=` 请求中包含的命令，就像图像数据将使用的 `req=img`.

指定 `text` 或省略第二个参数，以便您可以返回格式为 `HTML <AREA>` 具有响应MIME类型的元素字符串 `text/plain`.

指定 `xml` 因此，您可以将响应格式设置为XML而不是HTML。 可以选择指定文本编码。 默认值为 `UTF-8`.

返回空字符串（或为空） `<AREA>` 元素)，如果没有找到指定目录对象的映射数据，和/或如果没有 `<AREA>` 裁切图像后元素仍会保留。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用扩展语法指定JS回调处理程序的名称 `req=` 参数：

`req=...,json [&handler = reqHandler ]`

此 `<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选. 默认值为 `s7jsonResponse`.

请参阅 [图像映射](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
