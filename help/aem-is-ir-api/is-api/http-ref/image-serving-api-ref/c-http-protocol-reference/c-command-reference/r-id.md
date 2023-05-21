---
description: 影像/中繼資料版本。 處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和企業Proxy伺服器快取）中的伺服器可能會儲存影像伺服回應，這些回應可能會過期一段時間。
solution: Experience Manager
title: id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 4%

---

# id{#id}

影像/中繼資料版本。 處理經常變更的內容時，快取網路（例如Akamai、瀏覽器快取和企業Proxy伺服器快取）中的伺服器可能會儲存影像伺服回應，這些回應可能會過期一段時間。

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>版本字串。 </p> </td> 
 </tr> 
</table>

「影像伺服」包含版本設定機制，有助於減少應用程式使用過時快取專案的機率。 此機制涉及使用 `req=props` 取得影像資料和中繼資料（例如影像地圖或縮放目標資料）的版本識別碼字串。 然後，版本識別碼字串會新增至可快取的「影像伺服」請求，使用 `id=` 命令。

當來源影像或中繼資料變更時，對應的版本ID值也會變更。 將最新的版本ID值加入 `id=` 命令可確保不再存取舊的快取專案。

下表列出用於每個的版本識別碼字串 `req=` 型別：

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> req=props中的版本識別碼</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 地图 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 遮色片 </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 目标 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> 使用者資料 </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` 上面未列出的型別會有簡短TTL ( `attribute::NonImgExpiration`)或其回應完全不可快取；包含 `id=` 進行此類要求。

## 屬性 {#section-62e973d0d5884abebbb0679f9278ae2c}

要求屬性。 可选. 伺服器一律忽略。

## 默认 {#section-96136720c82842c89505347ec39e6024}

无。

## 示例 {#section-a5fb871e0ec8485c91c4fca78895d17f}

請參閱「 」的說明 [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) 例如使用方式。

## 另请参阅 {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ， [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)， [catalog：：到期](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a)， [attribute：：NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
