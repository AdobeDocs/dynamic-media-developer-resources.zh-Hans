---
description: 图像映射数据。
solution: Experience Manager
title: 地图
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 8%

---


# 地图{#map}

图像映射数据。

`req=map[,text|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

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

在查询没有指定其他命令的简单目录条目时（不会缩放到`catalog::maxPix`），返回`catalog::Map`，但不进行修改。

如果在请求中指定了任何其他命令，则返回一个复合图像映射，该映射通过缩放、裁剪、旋转和分层请求中包含的所有`catalog::Map`和/或`map=`命令而导出，就像图像数据与`req=img`一样。

指定`text`或省略第二个参数以返回响应MIME类型为`text/plain`的`HTML <AREA>`元素字符串形式的图像映射数据。

指定`xml`以将响应格式化为XML而非HTML。 可以选择指定文本编码。 默认值为 `UTF-8`.

如果没有为指定的目录对象找到映射数据，和/或裁剪图像后没有保留任何`<AREA>`元素，则返回空字符串（或空`<AREA>`元素）。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.

请参阅[图像映射](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
