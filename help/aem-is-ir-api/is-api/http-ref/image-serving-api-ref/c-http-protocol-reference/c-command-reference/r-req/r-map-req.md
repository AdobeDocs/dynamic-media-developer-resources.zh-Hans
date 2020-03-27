---
description: 图像映射数据。
seo-description: 图像映射数据。
seo-title: 地图
solution: Experience Manager
title: 地图
topic: Scene7 Image Serving - Image Rendering API
uuid: 57cb0fcf-5a07-4109-bfd4-ef9aaf794b27
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 地图{#map}

图像映射数据。

`req=map[,text|{xml[, *`encodingreqId`*]}|{json[&id= *``*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8| UTF-16| UTF-16LE| UTF-16BE| ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

在查 `catalog::Map` 询没有指定其他命令的简单目录条目时（不会缩放到），返回时不进行修 `catalog::maxPix`改。

如果在请求中指定了任何其他命令，则返回合成图像映射，该映射通过缩放、裁剪、旋转和层叠请求中包含的所有和／或命令来派生，就像图像数据一样 `catalog::Map``map=``req=img`。

指 `text` 定或忽略第二个参数，以响应MIME类型的元素字符串形式返 `HTML <AREA>` 回图像映射数据 `text/plain`。

指 `xml` 定将响应格式设置为XML而非HTML。 可以选择指定文本编码。 默认值为 `UTF-8`.

如果未找到指定目录对象的映 `<AREA>` 射数据，和／或裁剪图像后没有任何元素仍保留，则返回空字符串( `<AREA>` 或空元素)。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用参数的扩展语法指定JS回调处理函数的 `req=` 名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。 仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

See [Image Maps](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab).
