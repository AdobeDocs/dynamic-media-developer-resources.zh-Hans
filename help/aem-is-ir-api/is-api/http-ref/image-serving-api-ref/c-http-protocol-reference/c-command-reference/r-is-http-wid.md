---
description: 檢視寬度。 指定請求中不存在fit=時回應影像（檢視影像）的寬度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ba22c79b-da59-4993-aa1c-2c990a0c4be5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# wid{#wid}

檢視寬度。 指定請求中不存在fit=時回應影像（檢視影像）的寬度。

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>影像寬度，以畫素為單位（整數大於0）。 </p> </td> 
 </tr> 
</table>

若兩者皆有 `hei=` 和 `scl=` 指定，複合影像可根據 `align=` 屬性。 時間 `fit=` 存在， `wid=` 指定精確、最小或最大回應影像寬度；請參閱 `fit=` 以取得詳細資訊。

若 `scl=` 未指定，則會縮放複合影像以符合大小。 若兩者皆有 `wid=` 和 `hei=` 已指定，且 `scl=` 未指定，則會縮放影像以完全符合wid/hei矩形，儘可能留下最小的背景區域顯示。 在此情況下，影像會根據 `align=` 屬性。

>[!NOTE]
>
>如果計算的或預設的回覆影像大小大於 `attribute::MaxPix`.

## 默认 {#section-976d4c8554a34c899f85d172f6ac6f58}

如果兩者都不 `wid=`， `hei=`，也不 `scl=` 指定，回覆影像會具有複合影像的大小，或 `attribute::DefaultPix`，以較小者為準。

## 屬性 {#section-c93b7ce1b0d2475f80b06264b45d1285}

檢視屬性。 無論目前的圖層設定為何，均適用。

## 示例 {#section-82bc98b7c15a451bbe9b915d414c0470}

請求影像以符合200x200矩形；如果影像不是正方形，則右上方對齊影像。 任何背景區域皆已填滿 `attribute::BkgColor`.

` http:// *`伺服器`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

相同的影像，以200畫素的固定寬度傳送，但具有可變高度以維持影像的外觀比例。 在這種情況下，傳回的影像永遠不會有任何背景填滿區域。 請注意，在此情況下， align=完全無效。

` http:// *`伺服器`*/myRootId/myImageId?wid=200`

## 另请参阅 {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [attribute：：DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)， [attribute：：MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
