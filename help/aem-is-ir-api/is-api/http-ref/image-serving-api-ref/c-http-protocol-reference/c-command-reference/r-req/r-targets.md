---
description: 從影像目錄縮放目標資料。 針對URL路徑中指定的影像目錄專案，傳回縮放目標資料。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 8%

---

# 目标{#targets}

從影像目錄縮放目標資料。 針對URL路徑中指定的影像目錄專案，傳回縮放目標資料。

`req=targets[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

以下專案的內容： `catalog::Targets` 會傳回。 要求&#39;text&#39;格式時，所有例項 `??` 在 `catalog::Targets` 取代為直線終止元和單一直線終止元( `CR/LF`)會附加至結尾。 如果URL路徑無法解析為有效的目錄專案，回應只會包含單行終止元。 要求&#39;xml&#39;或&#39;json&#39;格式時，會套用適當的格式設定。

請求字串中的其他命令會被忽略。

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
