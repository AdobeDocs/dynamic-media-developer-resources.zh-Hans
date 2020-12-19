---
description: 戴尔大小。 指定倾斜材料的大小。
seo-description: 戴尔大小。 指定倾斜材料的大小。
seo-title: 大小
solution: Experience Manager
title: 大小
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 3%

---


# 大小{#size}

戴尔大小。 指定倾斜材料的大小。

` size= *`宽度，高度`*[ *`，粗细`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 宽度、高度  </span> </p> </td> 
  <td class="stentry"> <p>以场景坐标单位（通常为英寸）（实数、实数）表示的十字体对象的大小。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 厚度  </span> </p> </td> 
  <td class="stentry"> <p>以场景坐标单位（通常为英寸）（实数）表示的贴体对象的粗细。 </p> </td> 
 </tr> 
</table>

如果宽度和高度均不为0，则图像将缩放到精确指定的尺寸，并且不保留图像的长宽比。 将任一值设置为0可保留图像的长宽比。

如果指定&#x200B;*`thickness`*，则暗角对象定义适当的光矢量时，将呈现投影。 将&#x200B;*`thickness`*&#x200B;设置为0可禁用投影渲染。

## 属性 {#section-818e01e91fed4015951189c818ef28d8}

材料属性。 只供贴士使用；被所有其他材料忽略。 `res=` 如果宽度或高度大于0，则忽略此值。值不得为负。

## 默认 {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` 贴牌材料是基于目录条目的；否 `size=0,0,0`则。如果未指定&#x200B;*`wid`*&#x200B;和&#x200B;*`hei`*&#x200B;或将&lt;a2/>设置为0，则从`res=`计算decal大小。 如果未指定&#x200B;*`thickness`*&#x200B;或将其设置为0，则不渲染投影。

## 示例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

贴牌的MSS，根据分辨率调整大小，顺时针旋转20°，厚度为2.5英寸，以实现适当的投影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另请参阅 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[场景坐标](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)，属 [性：:Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
