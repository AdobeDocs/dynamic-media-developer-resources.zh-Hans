---
description: 興趣地區。 指定複合影像中的矩形興趣區域(ROI)，以畫素表示。
solution: Experience Manager
title: rgn
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4fa597ba-f949-47f2-bb0f-5c078b5c7524
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# rgn{#rgn}

興趣地區。 指定複合影像中的矩形興趣區域(ROI)，以畫素表示。

rgn= *`coord`*， *`size`*

<table id="simpletable_3A430F9078B04C2E90F4D1A130AFA20C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 座標</span> </p> </td> 
  <td class="stentry"> <p>從複合影像左上角到ROI (int， int)左上角的畫素位移。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 大小</span> </p></td> 
  <td class="stentry"> <p>ROI的大小，以畫素為單位(int、int)。 </p></td> 
 </tr> 
</table>

>[!NOTE]
>
>`rgn=` 只定義ROI而不裁切影像。 時間 `wid=` 和/或 `hei=` 也會套用大於大小的內容，最終回覆影像中可能會顯示複合影像的其他資料。

## 屬性 {#section-53edb35f4e364d7ca13fd0886e8b0c86}

檢視屬性。 無論目前的圖層設定為何，均適用。

任何延伸至複合影像外部的ROI區域，都會填入 `bgc=`.

`rgn=` 在最終縮放和彎管頭之前套用 `scl=`， `wid=`， `hei=`， `fit=`， `rect=`，或 `align=`.

## 默认 {#section-6a3df8f670084def900ffef9dab7e94a}

整個複合影像( `rgn=0,0,width,height`)。

## 另请参阅 {#section-07883760f25c4d17aedbee36b7883891}

[crop=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-crop.md#reference-6fd0f6399966446ab4425ce050572eab) ， [延伸=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)， [wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)， [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)， [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)， [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)， [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989)， [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3)
