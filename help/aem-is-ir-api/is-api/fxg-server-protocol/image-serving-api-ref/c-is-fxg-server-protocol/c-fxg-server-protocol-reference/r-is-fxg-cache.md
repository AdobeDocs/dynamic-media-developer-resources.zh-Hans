---
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。
seo-description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。
seo-title: 高速缓存
solution: Experience Manager
title: 高速缓存
topic: Scene7 Image Serving - Image Rendering API
uuid: 10332f0d-4ed3-4981-8034-46dffa5d68b0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部Platform Server缓存中的缓存。

`&cache= *`cacheControl`*`

`&cache= *`clientControlserverControl`*, *``*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 缓 <span class="varname"> 存控制</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
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

如果只指定 *`cacheControl`* 了一个值，则该值同时应用于客户端和服务器缓存。

请求属性。 当请求不返回回复图像时忽略。 *`clientControl`* 当图像目录禁用客户端缓存时(如果 `catalog::Expiration` 有负值)，将忽略。

默认为 `cache=on,on`。
