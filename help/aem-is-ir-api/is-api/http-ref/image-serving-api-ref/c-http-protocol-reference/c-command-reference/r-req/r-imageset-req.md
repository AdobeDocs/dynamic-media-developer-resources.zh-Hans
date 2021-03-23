---
description: 图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。
seo-description: 图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。
seo-title: 图像集
solution: Experience Manager
title: 图像集
uuid: 8854e903-a85f-403a-ae3d-b7281a236262
feature: Dynamic Media Classic，SDK/API，图像集
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 7%

---


# imageset{#imageset}

图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。

`req=imageset[,text|javascript|{xml[, *``*]}|{json[&id= *`encodingreqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

返回`catalog::ImageSet`的内容时无需进一步修改(字符串本地化除外，如果适用)，后跟单行终结器(CR/LF)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终结器组成。

请求字符串中的其他命令将被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
