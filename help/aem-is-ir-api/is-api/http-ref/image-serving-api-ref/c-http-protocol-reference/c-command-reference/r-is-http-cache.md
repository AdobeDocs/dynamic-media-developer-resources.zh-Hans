---
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。
seo-description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。
seo-title: 高速缓存
solution: Experience Manager
title: 高速缓存
topic: Scene7 Image Serving - Image Rendering API
uuid: 08f4e4d0-0f7d-48fe-956c-284af97c902e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。

`cache= *`cacheControl`*`

`cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 缓 <span class="varname"> 存控制</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> clientControl <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 服务器 <span class="varname"> 控制</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

如果只指定 ` *`一个cacheControl值`*` ，则它同时应用于客户端和服务器缓存。

该关 `validate` 键字允许在图像文件发生更改后更新缓存条目，而不必等待缓存条目自动过期。 客户端缓存不受此命令的影响。

该关 `update` 键字可用于强制更新服务器端缓存条目。 在资源发生更改后（这些资源不会直接由缓存验证机制跟踪），这非常有用，例如在修改字体文件时，不更改其文件名或关联的字体ID。

如果在嵌套请求中指定， `cache=on` 则启用嵌套请求生成的图像的永久服务器端缓存。 仅当需要使用完全相同的参数重复调用同一嵌套请求时，才应谨慎启用嵌套请求的缓存。

## 属性 {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

请求属性。 无论当前图层设置如何，均可应用。 当请求不返回回复图像时忽略。 *`clientControl`*在图像目录禁用客户端缓存时忽略(如果 `catalog::Expiration` 有负值)。

客户端缓存控件( `on` 且仅 `off` 限)也可用于的静态内容请求 [!DNL /is/content/]。

## 默认 {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` 对于HTTP请求， `cache=off` 对于嵌套／嵌入式请求， `cache=on` 对于静态内容请求。

## 另请参阅 {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
