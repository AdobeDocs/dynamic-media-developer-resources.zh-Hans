---
description: 图像目录中的用户数据。 返回在url路径中指定的图像目录条目的用户数据。
solution: Experience Manager
title: userdata
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 7%

---


# userdata{#userdata}

图像目录中的用户数据。 返回在url路径中指定的图像目录条目的用户数据。

`req=userdata[,text|{xml[, *`编码`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 编码</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

将返回`catalog::UserData`的内容。 当指定“text”格式时，`catalog::UserData`中`??`的所有实例都由行终结器替换，并在末尾附加单行终结器(CR/LF)。 如果URL路径未解析为有效的目录条目，则响应仅由单行终结器组成。 在请求“xml”或“json”格式时，会应用适当的格式。

请求字符串中的其他命令将被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

>[!NOTE]
>
>userdata属性键名中不允许使用冒号字符。

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
