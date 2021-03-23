---
description: 媒体集信息。
seo-description: 媒体集信息。
seo-title: 设置
solution: Experience Manager
title: 设置
uuid: ebd78249-45ea-47cd-8845-786070f92f21
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 11%

---


# 设置{#set}

媒体集信息。

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 编码</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>唯一请求标识符 </p></td> 
 </tr> 
</table>

返回有关图像、视频、色板以及与目录：::ImageSet关联的各种元数据的信息，这些元数据用于在URL路径中指定的图像目录条目。 该响应是由所提供的集合类型确定的分层结构。 在请求“xml”或“json”格式时，会应用适当的格式。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.

>[!NOTE]
>
>req=set请求中不允许使用冒号字符。

支持JSON响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理程序的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
