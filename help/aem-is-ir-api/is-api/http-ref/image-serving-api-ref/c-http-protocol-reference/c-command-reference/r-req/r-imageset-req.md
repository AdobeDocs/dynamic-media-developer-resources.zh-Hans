---
description: 图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。
solution: Experience Manager
title: 图像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# 图像集{#imageset}

图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。

`req=imageset[,text|javascript|{xml[, *`编码`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname">编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

`catalog::ImageSet`的内容无需进一步修改即返回（字符串本地化除外，如果适用），后跟单行终止符(CR/LF)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终止符组成。

请求字符串中的其他命令将被忽略。 可使用基于`catalog::NonImgExpiration`的TTL来缓存HTTP响应。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选。 默认值为`s7jsonResponse`。
