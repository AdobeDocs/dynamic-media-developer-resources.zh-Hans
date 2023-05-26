---
title: 大小
description: 贴花大小。 指定贴花材料的大小。
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

贴花大小。 指定贴花材料的大小。

` size= *`宽度，高度`*[ *`，粗细`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 宽度、高度 </span> </p> </td> 
  <td class="stentry"> <p>以场景坐标单位表示的贴花对象的大小（通常为英寸）（真实、真实）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 粗细 </span> </p> </td> 
  <td class="stentry"> <p>贴花对象的粗细，以场景坐标单位表示（通常为英寸）（实数）。 </p> </td> 
 </tr> 
</table>

如果宽度或高度都不为0，则图像将缩放到完全指定的尺寸，并且图像的纵横比不会保留。 将任一值设置为0会保留图像的纵横比。

如果 *`thickness`* 指定，如果晕影对象定义了相应的光矢量，则会渲染投影。 设置 *`thickness`* 设置为0可禁用投影渲染。

## 属性 {#section-818e01e91fed4015951189c818ef28d8}

材质属性。 仅供标记使用；被所有其他材料忽略。 `res=` 如果宽度或高度大于0，则会被忽略。 值不得为负。

## 默认 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 如果贴花材料基于目录条目；否则 `size=0,0,0`. 贴花大小的计算方式为 `res=` 如果 *`wid`* 和 *`hei`* 未指定或设置为0。 以下情况下不呈现投影 *`thickness`* 未指定或设置为0。

## 示例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

用于贴花的MSS根据分辨率调整大小，顺时针旋转20°，厚度为2.5英寸，用于适当的投影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另请参阅 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[场景坐标](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)， [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)， [attribute：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
