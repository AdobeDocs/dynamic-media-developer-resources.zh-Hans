---
description: 请求验证。
seo-description: 请求验证。
seo-title: 确认
solution: Experience Manager
title: 确认
topic: Scene7 Image Serving - Image Rendering API
uuid: 5322c484-2cf5-4022-9863-73fc525beb56
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 确认{#validate}

请求验证。

`req=validate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_F214CDA7580A46C0B5CF14CF13AA9B0A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

像指定的那样分析请 `req=img` 求字符串，但不替换变量并评估引用的对象(图像、ICC用户档案、字体等)。 如果解析失败，则返回标准错误响应，否则返回以下属性：

`request.isValid=1`

HTTP响应不可缓存。

支持JSONP响应格式的请求允许您使用参数的扩展语法指定JS回调处理函数的 `req=` 名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。 仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
