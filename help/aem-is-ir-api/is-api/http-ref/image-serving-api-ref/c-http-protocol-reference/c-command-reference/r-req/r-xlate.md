---
description: 可用的地區設定特定版本。 傳回請求路徑中所指定之目錄ID的可用地區設定特定版本清單。
solution: Experience Manager
title: xlate
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bf5b3cb7-9792-4eca-a1aa-55aa4089b4d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 14%

---

# xlate{#xlate}

可用的地區設定特定版本。 傳回請求路徑中所指定之目錄ID的可用地區設定特定版本清單。

`req=xlate[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8970A3A5A64F4DC2B184E251993390C5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>唯一請求識別碼。 </p></td> 
 </tr> 
</table>

另請參閱 [物件ID轉譯](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414).

例如：

`xlate.translatedIds=image,image_fr,image_de`

HTTP 响应是可缓存的，且 TTL 基于 `catalog::Expiration`.

支援JSONP回應格式的請求可讓您使用擴充語法來指定JS回呼處理常式的名稱。 `req=` 引數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP回應中呈現的JS處理常式名稱。 僅允許a-z、A-Z和0-9字元。 可选. 默认值为 `s7jsonResponse`.
