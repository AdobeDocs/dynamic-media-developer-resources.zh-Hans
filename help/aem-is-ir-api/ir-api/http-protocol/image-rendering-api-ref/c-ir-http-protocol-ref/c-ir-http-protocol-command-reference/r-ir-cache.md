---
title: 缓存
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部 [!DNL Platform Server] 缓存中的缓存。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# 缓存 {#cache}

缓存控制。 允许您有选择地禁用内部[!DNL Platform Server]缓存中的客户端缓存（浏览器、代理服务器、网络缓存系统）和缓存。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>日期 | 关 | 验证 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>日期 | 关 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>日期 | 关 </p></td> 
 </tr> 
</table>

如果只指定一个&#x200B;*`cacheControl`*&#x200B;值，则它同时应用于客户端和服务器缓存。

“`validate`”关键字允许在纹理或晕影文件更改后更新服务器缓存项，而无需等待缓存项自动过期。 此命令不会影响客户端缓存。

如果在嵌套请求中指定，`cache=on`将启用嵌套请求生成的映像的服务器端持久缓存。 请注意，仅当使用相同的参数重复调用相同的嵌套请求时，才为嵌套请求启用缓存。

## 属性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能出现在请求中的任何位置。 在请求未返回回复图像时忽略。 材料目录禁用客户端缓存时（如果&#x200B;*`clientControl`*&#x200B;具有负值），将忽略属性`attribute::Expiration`。 如果服务器缓存被禁用( *`serverControl`*)，则忽略属性`PlatformServer::cache.enable`。

## 默认 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

对于HTTP请求`cache=on,on`，对于嵌套/嵌入请求`cache=off`。

## 另请参阅 {#section-2f5853751dab49579e97418fa766bdf9}

[目录：：过期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)，[请求=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
