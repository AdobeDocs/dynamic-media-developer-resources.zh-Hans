---
description: 图像目录中的用户数据。 返回在url路径中指定的图像目录条目的用户数据。
solution: Experience Manager
title: 用户数据
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---

# 用户数据{#userdata}

图像目录中的用户数据。 返回在url路径中指定的图像目录条目的用户数据。

`req=userdata[,text|{xml[, *`编码`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">编码</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

返回`catalog::UserData`的内容。 当指定“text”格式时，`??`中`catalog::UserData`的所有实例都替换为行终止符，并且末尾附加一个单行终止符(CR/LF)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终止符组成。 在请求“xml”或“json”格式时应用相应的格式。

请求字符串中的其他命令将被忽略。

可使用基于`catalog::Expiration`的TTL来缓存HTTP响应。

>[!NOTE]
>
>userdata属性键名称中不允许使用冒号字符。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选。 默认值为`s7jsonResponse`。
