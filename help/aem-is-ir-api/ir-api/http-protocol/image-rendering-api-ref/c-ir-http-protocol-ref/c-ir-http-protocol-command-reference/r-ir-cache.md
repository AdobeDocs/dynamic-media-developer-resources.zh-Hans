---
title: 快取
description: 快取控制。 允許選擇性地停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# 快取 {#cache}

快取控制。 可讓您選擇性停用使用者端快取（瀏覽器、Proxy伺服器、網路快取系統）和內部快取 [!DNL Platform Server] 快取。

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>於 |關閉 |驗證 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>於 |關閉 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>於 |關閉 </p></td> 
 </tr> 
</table>

若只有一個 *`cacheControl`* 指定值，則會同時套用至使用者端和伺服器快取。

「 `validate`「關鍵字」允許在紋理或暈映檔案變更後更新伺服器快取專案，而不必等待快取專案自動過期。 使用者端快取不受這個命令影響。

若在巢狀要求中指定， `cache=on` 啟用巢狀要求所產生影像的伺服器端持續快取。 請注意，只有當使用相同的引數重複呼叫相同的巢狀要求時，才為巢狀要求啟用快取。

## 屬性 {#section-0dcbd62e1122400e8c347f408f2d937e}

可能發生在請求中的任何位置。 當請求未傳回回覆影像時忽略。 屬性 *`clientControl`* 材料目錄停用使用者端快取時忽略(如果 `attribute::Expiration` 具有負值)。 屬性 *`serverControl`* 會忽略伺服器快取是否停用( `PlatformServer::cache.enable`)。

## 默认 {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` 若為HTTP要求， `cache=off` 適用於巢狀/內嵌請求。

## 另请参阅 {#section-2f5853751dab49579e97418fa766bdf9}

[catalog：：到期](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)， [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
