---
description: 请求验证。
seo-description: 请求验证。
seo-title: 确认
solution: Experience Manager
title: 确认
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 5%

---


# 确认{#validate}

请求验证。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span> </span> </p> </td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

解析请求字符串，就像指定了`req=img`一样，但不替换变量和评估引用的对象(图像、ICC用户档案、字体等)。 如果解析失败，则返回标准错误响应，否则返回以下属性：

`request.isValid=1`

HTTP响应不可缓存。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
