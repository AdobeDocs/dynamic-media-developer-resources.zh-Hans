---
title: 锚记
description: 图像锚点（热点）。 指定可重复纹理或倾斜材料的纹理锚点（热点）。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 3%

---

# 锚记{#anchor}

图像锚点（热点）。 指定可重复纹理或倾斜材料的纹理锚点（热点）。

`anchor= *`x`*, *`y`*`

`anchorN= *`xn`*, *`玄`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>, <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源图像左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>, <span class="varname"> 玄</span> </p></td> 
  <td class="stentry"> <p>与源图像中心的标准化偏移（实、实）。 </p></td> 
 </tr> 
</table>

可重复的纹理被应用于晕影对象，以便纹理锚点( `anchor=`)位于对象的纹理原点。

倾斜图像被应用于晕影对象，以便倾斜锚点位于对象的倾斜原点。 该倾斜位置可进一步使用 `pos=` 命令。

`anchorN=0,0` 将图像锚点放置在源图像的中心。 `anchorN=-0.5,-0.5` 或 `anchor=0,0` 位于左上角， `anchorN=0.5,0.5` 位于源图像的右下角。

## 属性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料属性**. 如果 `align=2`，或者如果材料不是可重复的质地、墙纸或贴图。

## 默认 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`，则为“材料基于目录条目”。 否则， `anchor=0,0` （图像的左上角）可重复的纹理和壁纸，以及 `anchorN=0,0` （图像的中心）。

## 另请参阅 {#section-b18bf0b035644ca5aedebbc64373718e}

[目录：：锚点](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) , [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
