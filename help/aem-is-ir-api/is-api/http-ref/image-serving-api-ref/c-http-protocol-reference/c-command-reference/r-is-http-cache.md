---
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。
solution: Experience Manager
title: 缓存
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# 缓存{#cache}

缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 开|关|验证|更新</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 打开|关闭</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 打开|关闭</span> </p></td> 
 </tr> 
</table>

如果只指定了一个`*`cacheControl`*`值，则它将同时应用于客户端和服务器缓存。

`validate`关键字允许在图像文件发生更改后更新缓存条目，而无需等待缓存条目自动过期。 客户端缓存不受此命令的影响。

`update`关键字可用于强制更新服务器端缓存条目。 当资源已被更改，而缓存验证机制不会直接跟踪这些资源后，这非常有用，例如，当修改字体文件而不更改其文件名或关联的字体ID时。

如果在嵌套请求中指定，则`cache=on`会对由嵌套请求生成的图像启用永久性服务器端缓存。 仅当希望使用完全相同的参数重复调用同一嵌套请求时，才应当注意启用嵌套请求的缓存。

## 属性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

请求属性。 无论当前的层设置如何，都适用。 在请求未返回回复图像时忽略。 *`clientControl`*在图像目录禁用客户端缓存时（如果`catalog::Expiration`具有负值），将忽略该事件。

客户端缓存控件（仅`on`和`off`）也适用于位于[!DNL /is/content/]的静态内容请求。

## 默认 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 对于HTTP请求、嵌 `cache=off` 套/嵌入请求、静 `cache=on` 态内容请求。

## 另请参阅 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[目录：：过期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ，请 [求=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
