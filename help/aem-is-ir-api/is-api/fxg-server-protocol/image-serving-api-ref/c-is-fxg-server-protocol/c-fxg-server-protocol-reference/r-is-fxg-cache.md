---
description: 缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。
seo-description: 缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。
seo-title: 高速缓存
solution: Experience Manager
title: 高速缓存
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# 缓存{#cache}

缓存控件。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部平台服务器缓存中的缓存。

`&cache= *`cacheControl`*`

`&cache= *`ClientControlserver `*, *`Control`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 打开|关闭</span> </p></td> 
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

如果只指定一个&#x200B;*`cacheControl`*&#x200B;值，则它将同时应用于客户端和服务器缓存。

请求属性。 当请求不返回回复图像时忽略。 *`clientControl`* 当图像目录禁用客户端缓存时(如果 `catalog::Expiration` 有负值)，将忽略。

默认为`cache=on,on`。
