---
description: 请求验证。
solution: Experience Manager
title: 确认
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 88424371-45a0-43bb-af49-2e8568b7b44c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

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

解析请求字符串时，如同指定了`req=img`，但不替换变量和评估引用对象（图像、ICC配置文件、字体等）。 如果解析失败，则返回标准错误响应，否则返回以下属性：

`request.isValid=1`

无法缓存HTTP响应。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法来指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。只允许使用a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
