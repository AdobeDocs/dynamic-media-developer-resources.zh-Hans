---
description: 縮放目標資料。 沒有或多個縮放目標屬性，這些屬性可以與縮放檢視器使用者端結合使用。
solution: Experience Manager
title: 目标
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 2%

---

# 目标{#targets}

縮放目標資料。 沒有或多個縮放目標屬性，這些屬性可以與縮放檢視器使用者端結合使用。

伺服器傳回此欄位的內容以回應 `req=targets`，取代&#39; `??`&#39;記錄終止元Token。

每個縮放目標最多可以有四個屬性相關聯：

` Target. *`數字`*.frame= *`框架`*`

` Target. *`數字`*.rect= *`left，top，width，height`*`

` Target. *`數字`*.label= *`標籤`*`

` Target. *`數字`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 數字 </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標編號(int)；縮放目標必須從1開始依序連續編號。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 框架 </span> </span> </p> </td> 
  <td class="stentry"> <p>選擇性影格/頁碼，用於鎖定迴轉或摺頁集的特定影格/頁面；如果未針對迴轉與摺頁檢視器用途指定，則預設為0；縮放檢視器會略過。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 左，上 </span> </span> </p> </td> 
  <td class="stentry"> <p>從影像左上角到縮放目標矩形(int， int)左上角的畫素位移；必須是0或更大。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 寬度，高度 </span> </span> </p> </td> 
  <td class="stentry"> <p>縮放目標矩形(int， int)的畫素大小；必須大於0。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 標籤 </span> </span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用作縮放目標連結的文字標籤。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>文字資料值；可用來將目標特定資訊傳遞至使用者端，例如SKU值或快速連結URL。 </p> </td> 
 </tr> 
</table>

Target. *`num`*&#x200B;每個縮放目標都需要.rect，而且必須在影像中完全指定一個矩形。 所有其他屬性都是選用的。

*`label`* 和 *`userData`* 參與文字字串本地化。 請參閱 [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) 在 *HTTP通訊協定參考* 以取得詳細資訊。

對於涉及迴轉和小冊子檢視器使用者端的應用程式，必須在定義影像集的相同目錄記錄中定義縮放目標。 檢視器會忽略影像整合員的目錄記錄中的任何縮放目標定義。

Dynamic Media檢視器會使用已透過下列指令調整之完整解析度影像座標中的縮放目標： `catalog::Modifier`.

## 屬性 {#section-b3f8eba4985f4b00bb935d592fe770f9}

[屬性資料](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) 值。

## 默认 {#section-feab29f6575e482391086a57f547543c}

无。

## 另请参阅 {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog：：Imageset](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ， [catalog：：Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)， [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md)， [文字字串本地化](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
