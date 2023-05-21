---
description: 影像目錄中的使用者資料。 傳回URL路徑中所指定影像目錄專案的使用者資料。
solution: Experience Manager
title: 使用者資料
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b1d85ea6-0e12-49a8-b1dc-4c64a672770b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 8%

---

# 使用者資料{#userdata}

影像目錄中的使用者資料。 傳回URL路徑中所指定影像目錄專案的使用者資料。

`req=userdata[,text|{xml[, *`编码`*]}|json]`

<table id="simpletable_F9D94C83865F4216BCF7987C32FACC46"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 编码</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
</table>

以下專案的內容： `catalog::UserData` 會傳回。 指定&#39;text&#39;格式時，所有實體 `??` 在 `catalog::UserData`取代為直線終止元，且單線終止元(CR/LF)會附加至末端。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。 要求&#39;xml&#39;或&#39;json&#39;格式時，會套用適當的格式設定。

請求字串中的其他命令會被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

>[!NOTE]
>
>使用者資料屬性索引鍵名稱中不允許冒號字元。

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
