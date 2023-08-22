---
title: 缓存
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部缓存 [!DNL Platform Server] 缓存。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# 缓存{#cache}

缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部缓存 [!DNL Platform Server] 缓存。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 开启|关闭|验证|更新</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 开|关</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 开|关</span> </p></td> 
 </tr> 
</table>

如果只有一个 `*`cacheControl`*` 指定值后，该值会同时应用于客户端和服务器缓存。

此 `validate` 关键字允许在图像文件更改后更新缓存条目，而无需等待缓存条目自动过期。 此命令不会影响客户端缓存。

此 `update` 关键字可用于强制更新服务器端缓存条目。 在更改了缓存验证机制不直接跟踪的资源后（例如，修改字体文件而不更改其文件名或关联的字体ID时），此功能非常有用。

如果在嵌套请求中指定， `cache=on` 启用嵌套请求生成的图像的服务器端持久缓存。 只有当同一嵌套请求应使用完全相同的参数重复调用时，才应当注意为嵌套请求启用缓存。

## 属性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

请求属性。 无论当前图层设置如何，均适用。 在请求未返回回复图像时忽略。 *`clientControl`*在图像目录禁用客户端缓存时忽略(如果 `catalog::Expiration` 具有负值)。

客户端缓存控制( `on` 和 `off` 仅适用于)也可用于静态内容请求 [!DNL /is/content/].

## 默认 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 对于HTTP请求， `cache=off` 对于嵌套/嵌入请求， `cache=on` 用于静态内容请求。

## 另请参阅 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog：：过期时间](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ， [需要=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
