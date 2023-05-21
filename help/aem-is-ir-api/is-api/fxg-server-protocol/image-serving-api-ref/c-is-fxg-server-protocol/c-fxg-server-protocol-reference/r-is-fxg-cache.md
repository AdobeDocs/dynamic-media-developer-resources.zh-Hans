---
description: 快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。
solution: Experience Manager
title: 快取
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# 快取{#cache}

快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 開啟|關閉</span> </p></td> 
 </tr> 
</table>

若只有一個 *`cacheControl`* 指定值，則會同時套用至使用者端和伺服器快取。

要求屬性。 當請求未傳回回覆影像時忽略。 *`clientControl`* 被影像目錄停用時忽略(如果 `catalog::Expiration` 具有負值)。

預設為 `cache=on,on`.
