---
description: 影像目錄中的影像集資料。 針對URL路徑中指定的影像目錄專案，傳回影像集資料。
solution: Experience Manager
title: 影像集
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---

# 影像集{#imageset}

影像目錄中的影像集資料。 針對URL路徑中指定的影像目錄專案，傳回影像集資料。

`req=imageset[,text|javascript|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 编码</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

的內容 `catalog::ImageSet` 會直接傳回，而不會進一步修改（字串本地化除外，如果適用），後面接著單行終止元(CR/LF)。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。

請求字串中的其他命令會被忽略。 HTTP 响应是可缓存的，且 TTL 基于 `catalog::NonImgExpiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
