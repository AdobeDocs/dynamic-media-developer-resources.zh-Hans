---
description: 图像目录中的图像集数据。 返回在URL路径中指定的图像目录条目的图像集数据。
solution: Experience Manager
title: 图像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
TQID: 'https://experienceleague.adobe.com/1PbZjs--lk7GcyXU1F-AJ-vWcgwVX9JFivvbnTGrWKQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
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

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选. 默认值为`s7jsonResponse`。
