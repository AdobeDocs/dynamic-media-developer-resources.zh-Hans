---
description: 缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。
seo-description: 缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。
seo-title: 缓存
solution: Experience Manager
title: 缓存
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# 缓存{#cache}

缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on |关闭 |验证 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>on |关闭 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>on |关闭 </p></td> 
 </tr> 
</table>

如果只指定了一个&#x200B;*`cacheControl`*&#x200B;值，则它将同时应用于客户端和服务器缓存。

“ `validate`”关键字允许在纹理或晕影文件发生更改后更新服务器缓存条目，而无需等待缓存条目自动过期。 客户端缓存不受此命令的影响。

如果在嵌套请求中指定，`cache=on`将启用由嵌套请求生成的图像的永久服务器端缓存。 仅当期望使用完全相同的参数重复调用同一嵌套请求时，才应当注意启用嵌套请求的缓存。

## 属性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能在请求中的任何位置发生。 当请求不返回回复图像时忽略。 *`clientControl`* 当材料目录禁用客户端缓存(如果 `attribute::Expiration` 有负值)时忽略。*`serverControl`* 如果禁用了服务器缓存()，则 `PlatformServer::cache.enable`忽略。

## 默认 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` （针对HTTP请求）， `cache=off` 针对嵌套/嵌入式请求。

## 另请参阅 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
