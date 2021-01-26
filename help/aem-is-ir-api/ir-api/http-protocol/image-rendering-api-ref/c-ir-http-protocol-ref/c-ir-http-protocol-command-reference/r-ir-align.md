---
description: 纹理渲染对齐。 指定将使用由选定暗角对象定义的来源点。
seo-description: 纹理渲染对齐。 指定将使用由选定暗角对象定义的来源点。
seo-title: 对齐
solution: Experience Manager
title: 对齐
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 4%

---


# align{#align}

纹理渲染对齐。 指定将使用由选定暗角对象定义的来源点。

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>默认（中间匹配）来源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>连续匹配来源。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>随机对齐。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3.6 </p></td> 
  <td class="stentry"> <p>用户定义的来源。 </p></td> 
 </tr> 
</table>

呈示器将纹理应用于对象，以使纹理锚点(`anchor=`)与指定的来源点一致。

每个对象最多可定义6个来源点(0、1、3、4、5、6)。 如果指定了`align`值，但相应的来源点未由晕影对象定义，则使用默认（中间匹配）来源点。

`align=2` 指定随机纹理对齐，在这种情况下， `anchor=` 会有效忽略纹理对齐。

主要用于室内装饰材料，可能用于服装织物，以管理相邻物体之间的纹理对齐。

## 属性 {#section-350fadc87dcf4812a8a02d1c3d6697a0}

材料属性。 如果选择了墙、机柜、装置或窗口覆盖框对象，或者材料不是可重复的纹理，则忽略此问题。

## 默认 {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`，如果材料基于目录条目，则为0（中间匹配）。

## 另请参阅 {#section-945d1ce275df487d9d564d4043156c79}

[catalog::Alignment](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
