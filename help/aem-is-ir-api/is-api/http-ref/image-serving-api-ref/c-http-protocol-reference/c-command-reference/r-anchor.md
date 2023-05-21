---
description: 影像錨點。 定義影像、純色或文字邊界方框矩形的錨點，然後套用轉換(crop=、scale=、rotate=、flip=)。 也用作rotate=的旋轉中心。
solution: Experience Manager
title: 锚记
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---

# 锚记{#anchor}

影像錨點。 定義影像、純色或文字邊界方框矩形的錨點，然後套用轉換(crop=、scale=、rotate=、flip=)。 也用作rotate=的旋轉中心。

`anchor= *`座標`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 座標</span> </span> </p> </td> 
  <td class="stentry"> <p>從來源影像左上角的畫素位移(int， int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>從來源影像中心的標準化位移（實數、實數） </p></td> 
 </tr> 
</table>

錨點會與影像一起變形，成為圖層原點(除非 `origin=` 也會指定，在這種情況下 `anchor=` 僅用作旋轉中心 `rotate=`)。

`anchorN=0,0` 將影像錨點放置在來源影像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 位於左上角，且 `anchorN=0.5,0.5` 位於來源影像的右下角。

## 屬性 {#section-f08942bc6aae46a8b5d341faaff80640}

來源影像屬性。 套用至目前的圖層，或套用至圖層0，如果 `layer=comp`.

## 默认 {#section-35d369fab1254f1a9b91684a6e169ad1}

若 `anchor=` 未指定，使用catalog：：Anchor。 若 `catalog::Anchor` 未定義，則會使用影像矩形的中心(與指定 `anchorN=0,0`)。

文字圖層涉及 `textPs=` 和涉及下列專案的圖層 `clipPath=` 可能有不同的預設錨點。

## 示例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

請參閱中的「範例C」 [範本](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 另请参阅 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog：：錨點](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ， [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)， [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)， [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)， [文字圖層](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
