---
title: 群組
description: 圖磚灌漿顏色和粗細。 模擬陶瓷與天然石塊的灌漿。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---

# 群組 {#grout}

圖磚灌漿顏色和粗細。 模擬陶瓷與天然石塊的灌漿。

格勞特= *`color`*[，*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 顏色 </span> </span> </p> </td>
  <td class="stentry"> <p>群組顏色(灰色或RGB)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>灌漿厚度；場景座標單位（通常為英吋） （實數）。 </p> </td>
 </tr> 
</table>

為了最大程度地控制灌漿外觀，請套用下列要求：

* 圖磚必須是方形或矩形；目前不支援其他形狀。
* 影像隻能包含單一圖磚。
* 影像中的預設群組（如果有的話）在所有四個邊緣上必須有相同的厚度。
* 必須在材料目錄中指定預設群組的厚度( `catalog::GroutWidth`)。

## 屬性 {#section-de78b678245b4ffda48097c345949e77}

材質屬性。 `*`顏色`*` 必須是RGB色彩值。 `*`寬度`*` 必須為大於或等於0的實數值。

如果重複= 4、5、7、8、9、14或更高，或為可重複紋理以外的材料指定時，則忽略。

## 默认 {#section-bfab3621f70b4489a21994ab11b20cc6}

若 `grout=` 未指定，未修改影像中的群組。 若 `grout= *`顏色`*` 已指定， `*`寬度`*` 預設為 `catalog::GroutWidth`.

## 另请参阅 {#section-8d472906a44943f5a8557e98f2fbc71f}

[色彩值](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
