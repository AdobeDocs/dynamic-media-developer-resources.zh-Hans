---
title: 地图
description: 图像映射数据。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3330f49a-934e-492a-804c-ace4d147c65a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 地图{#map}

图像映射数据。

`req=map[,text|{xml[, *`编码`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_10F2152FDF33411491FBBAFD173CA5ED"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

在查询未指定其他命令的简单目录条目时返回`catalog::Map`而不进行修改（不缩放到`catalog::maxPix`）。

如果在请求中指定了任何其他命令，则会返回复合图像映射。 复合图像映射是通过缩放、裁切、旋转和分层请求中包含的所有`catalog::Map`和/或`map=`命令派生的，就像图像数据将包含`req=img`一样。

指定`text`或省略第二个参数，以便您可以返回响应MIME类型为`text/plain`的`HTML <AREA>`元素字符串形式的图像映射数据。

指定`xml`，以便可以将响应格式化为XML而不是HTML。 可以选择指定文本编码。 默认值为`UTF-8`。

如果指定的目录对象找不到映射数据和/或在裁剪图像后没有保留`<AREA>`元素，则返回空字符串（或空`<AREA>`元素）。

可使用基于`catalog::Expiration`的TTL来缓存HTTP响应。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选。 默认值为`s7jsonResponse`。

查看[图像映射](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-image-maps.md#reference-ff7d1bac2a064104b0c508a81316fdab)。
