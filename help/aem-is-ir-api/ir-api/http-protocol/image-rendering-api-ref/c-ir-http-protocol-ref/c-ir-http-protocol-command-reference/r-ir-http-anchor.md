---
description: 图像锚点（热点）。 指定可重复纹理或倾斜材料的纹理锚点（热点）。
solution: Experience Manager
title: 锚记
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: ea2c5dce-6eb1-4f05-80bd-7336deb08b9e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 2%

---

# 锚记{#anchor}

图像锚点（热点）。 指定可重复纹理或倾斜材料的纹理锚点（热点）。

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>、 <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源图像左上角的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>与源图像中心的标准化偏移（实、实）。 </p></td> 
 </tr> 
</table>

可重复的纹理被应用于晕影对象，以便纹理锚点(`anchor=`)位于对象的纹理原点。

倾斜图像被应用于晕影对象，以便倾斜锚点位于对象的倾斜原点。 可使用`pos=`命令进一步调整倾斜位置。

`anchorN=0,0` 将图像锚点放置在源图像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位于左上角， `anchorN=0.5,0.5` 并且位于源图像的右下角。

## 属性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料属性**。如果`align=2`，或者材料不是可重复的质地、墙纸或倾斜图，则忽略。

## 默认 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`，则为“材料基于目录条目”。否则，请为可重复的纹理和壁纸选择`anchor=0,0`（图像的左上角），为十字体选择`anchorN=0,0`（图像的中心）。

## 另请参阅 {#section-b18bf0b035644ca5aedebbc64373718e}

[目录：：锚点](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
