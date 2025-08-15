---
title: 大小
description: 贴花大小。 指定贴花材料的大小。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 2%

---

# 大小{#size}

贴花大小。 指定贴花材料的大小。

` size= *`宽度，高度`*[ *`，粗细`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">宽度，高度</span> </p> </td> 
  <td class="stentry"> <p>以场景坐标单位表示的贴花对象的大小（通常为英寸）（真实、真实）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">粗细</span> </p> </td> 
  <td class="stentry"> <p>以场景坐标单位表示的贴花对象的粗细（通常为英寸）（实际）。 </p> </td> 
 </tr> 
</table>

如果宽度或高度都不为0，则图像将缩放到完全指定的尺寸，并且不保留图像的纵横比。 将任一值设置为0将保留图像的纵横比。

如果指定了&#x200B;*`thickness`*，则在晕影对象定义适当的光矢量时，将渲染投影。 将&#x200B;*`thickness`*&#x200B;设置为0可禁用投影渲染。

## 属性 {#section-818e01e91fed4015951189c818ef28d8}

材质属性。 仅供标记使用；被所有其他材料忽略。 如果宽度或高度大于0，则忽略`res=`。 值不得为负。

## 默认 {#section-f91f516c6af54f0eb4d8c964b923cae0}

如果贴花材料基于目录条目，则为`catalog::Size`；否则为`size=0,0,0`。 如果未指定`res=`和&#x200B;*`wid`*&#x200B;或将其设置为0，则从&#x200B;*`hei`*&#x200B;计算贴花大小。 如果未指定&#x200B;*`thickness`*&#x200B;或将其设置为0，则不呈现投影。

## 示例 {#section-04fdc2b60b9e4071b672bf6a913738ad}

一种贴花的MSS，其根据分辨率调整大小，顺时针旋转20°，厚度为2.5英寸，用于适当的投影效果：

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## 另请参阅 {#section-1b116ecd60214732a1757ee1f0cf21c2}

[场景坐标](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1)，[res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)，[属性：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
