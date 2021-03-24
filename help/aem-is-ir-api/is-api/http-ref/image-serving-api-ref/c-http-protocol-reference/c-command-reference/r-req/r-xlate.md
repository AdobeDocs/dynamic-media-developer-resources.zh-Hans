---
description: 可用的区域设置特定版本。 返回列表在请求路径中指定的目录ID的可用区域设置特定版本。
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---


# xlate{#xlate}

可用的区域设置特定版本。 返回列表在请求路径中指定的目录ID的可用区域设置特定版本。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一请求标识符。 </p></td> 
 </tr> 
</table>

请参阅[对象ID转换](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414)。

例如：

`xlate.translatedIds=image,image_fr,image_de`

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支持JSONP响应格式的请求允许您使用`req=`参数的扩展语法指定JS回调处理函数的名称：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP响应中存在的JS处理函数的名称。仅允许a-z、A-Z和0-9个字符。 可选。默认值为 `s7jsonResponse`.
