---
description: 缓存控制。 允许有选择地禁用客户端缓存（浏览器、代理服务器、网络缓存系统）和内部 [!DNL Platform Server] 缓存中的缓存。
solution: Experience Manager
title: 缓存
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# 缓存{#cache}

缓存控制。 允许选择性地禁用内部[!DNL Platform Server]缓存中的客户端缓存（浏览器、代理服务器、网络缓存系统）和缓存。

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">开启|关闭</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">开启|关闭</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">开启|关闭</span> </p></td> 
 </tr> 
</table>

如果只指定一个&#x200B;*`cacheControl`*&#x200B;值，则它同时应用于客户端和服务器缓存。

请求属性。 在请求未返回回复图像时忽略。 当图像目录禁用客户端缓存时（如果`catalog::Expiration`具有负值），将忽略&#x200B;*`clientControl`*。

默认为`cache=on,on`。
