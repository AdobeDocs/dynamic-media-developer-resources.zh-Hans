---
title: 大小
description: 貼花大小。 指定貼花材質的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 2%

---

# 大小{#size}

貼花大小。 指定貼花材質的大小。

` size= *`寬度，高度`*[ *`，粗細`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 寬度，高度 </span> </p> </td> 
  <td class="stentry"> <p>以場景座標單位表示的貼花物件大小（通常為英吋） （真實、真實）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 粗細 </span> </p> </td> 
  <td class="stentry"> <p>貼花物件的粗細，以場景座標單位表示（通常為英吋） （實數）。 </p> </td> 
 </tr> 
</table>

如果寬度或高度皆為0，則影像會縮放至完全指定的尺寸，且不會保留影像的外觀比例。 將任一值設定為0，可保留影像的外觀比例。

若 *`thickness`* 指定，如果暈映物件定義了適當的光線向量，則會演算陰影。 設定 *`thickness`* 設為0可停用投影演算。

## 屬性 {#section-818e01e91fed4015951189c818ef28d8}

材質屬性。 僅供貼花使用；被其他所有材料忽略。 `res=` 如果寬度或高度大於0，則會被忽略。 值不得為負數。

## 默认 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 如果貼花材質是以目錄專案為基礎；否則 `size=0,0,0`. 貼花大小的計算依據 `res=` 如果 *`wid`* 和 *`hei`* 未指定或設為0。 如果符合下列條件，則不會轉譯投影 *`thickness`* 未指定或設為0。

## 示例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

貼花的MSS，根據解析度調整大小，順時針旋轉20度，厚度為2.5英吋，以獲得適當的投影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另请参阅 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[場景座標](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)， [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)， [attribute：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
