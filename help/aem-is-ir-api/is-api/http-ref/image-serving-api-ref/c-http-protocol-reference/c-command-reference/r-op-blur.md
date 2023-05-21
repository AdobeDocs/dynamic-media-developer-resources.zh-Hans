---
description: 模糊影像。 將模糊濾鏡套用至影像資料。
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

模糊影像。 將模糊濾鏡套用至影像資料。

`op_blur= *`半徑`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半徑</span> </p> </td> 
  <td class="stentry"> <p>模糊濾鏡半徑，以畫素為單位（實數0..100）。 </p></td> 
 </tr> 
</table>

*`radius`* 是以相對於複合影像的畫素為單位。 也用於羽化圖層效果。

## 屬性 {#section-92573fe2c07746a7bab93a81fc3d208d}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`.

## 默认 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`，不會產生模糊效果。

## 示例 {#section-1ebacde68388492eb108ae0fcd7424db}

模糊影像的背景。 參照的單獨遮色片影像 `catalog::MaskPath`. 請注意 `layer=0`必須明確指定，否則 `op_blur` 會套用至整個複合影像。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
