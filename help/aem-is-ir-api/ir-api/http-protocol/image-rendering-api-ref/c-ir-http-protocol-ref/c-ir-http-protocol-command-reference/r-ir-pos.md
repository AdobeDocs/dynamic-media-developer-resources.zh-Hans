---
title: pos
description: 贴花位置。 定义从贴花图像的anchor=点到目标晕影对象定义的贴花原点的偏移量（以英寸为单位）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 531f1465-2bec-46b6-a41e-54d993cbf410
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 3%

---

# pos{#pos}

贴花位置。 定义从贴花图像的anchor=点到目标晕影对象定义的贴花原点的偏移量（以英寸为单位）。

`pos=x,y`

<table id="simpletable_DB3B64EFB67A47AD843812324ABFAE45"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>，<span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>以场景坐标单位表示的相对位置调整（通常为英寸）（真实、真实）。 </p></td> 
 </tr> 
</table>

## 属性 {#section-50371cfa4e244bc49d2295a918749258}

材质属性。 被标记以外的材料忽略。

## 默认 {#section-1b66efab054c45ca8d67d6a9865020f4}

`pos=0,0`。 将贴花的锚点与晕影对象的贴花原点对齐。

## 另请参阅 {#section-7cd8139481334ed79704d628b5bbd236}

[场景坐标](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)，[锚点=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
