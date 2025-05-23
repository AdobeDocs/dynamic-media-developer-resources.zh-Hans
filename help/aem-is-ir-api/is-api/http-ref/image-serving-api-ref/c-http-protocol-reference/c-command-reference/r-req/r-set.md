---
description: 媒体集信息。
solution: Experience Manager
title: 设置
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---

# 设置{#set}

媒体集信息。

req=set[，xml[， *`encoding`*]|&lbrace;json[&amp;id=*`reqId`*]]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">编码</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符 </p></td> 
 </tr> 
</table>

返回有关图像、视频、样本以及与URL路径中指定的图像目录条目的catalog：：ImageSet关联的各种元数据的信息。 该响应是由所提供的集合类型确定的层次结构。 在请求“xml”或“json”格式时应用相应的格式。

可使用基于`catalog::NonImgExpiration`的TTL来缓存HTTP响应。

>[!NOTE]
>
>req=set请求中不允许使用冒号字符。

支持JSON响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理程序的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>`是JSONP响应中存在的JS处理程序的名称。 只允许使用a-z、A-Z和0-9字符。 可选。 默认值为`s7jsonResponse`。
