---
description: 列印解析度。 覆寫內嵌在回應影像中的列印解析度值。
solution: Experience Manager
title: printRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 81c4c3b8-946d-401b-a279-ba3f426ea5a4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 2%

---

# printRes{#printres}

列印解析度。 覆寫內嵌在回應影像中的列印解析度值。

`printRes= *`val`*`

<table id="simpletable_85C271760AE5466C96115027E6511559"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>列印解析度(dpi)。 </p></td> 
 </tr> 
</table>

列印解析度通常由下列定義 `catalog::PrintResolution` 若是目錄專案，則為來源影像中內嵌的列印解析度值。 如果是範本或圖層複合影像，回應檔案中內嵌的預設列印解析度是圖層編號最低的圖層影像的列印解析度。

設定列印解析度不會變更回覆影像的畫素大小。

## 屬性 {#section-03c7910ebe234804a319e5d0d8ef3a74}

要求屬性。 無論目前的圖層設定為何，均適用。

## 默认 {#section-d7d89fd235cc418fb381014612530f00}

`catalog::PrintResolution` 或內嵌在來源影像中的列印解析度。

## 另请参阅 {#section-4c479b6d6ccd41fc9ce8b239a28e726d}

[catalog：：PrintResolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-printresolution-cat.md#reference-4ebb2e136995470b84b7c5e10cb8e5f5)
