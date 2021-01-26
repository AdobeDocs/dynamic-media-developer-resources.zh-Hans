---
description: 图像锚点（热点）。 指定可重复的纹理或贴花材料的纹理锚点（热点）。
seo-description: 图像锚点（热点）。 指定可重复的纹理或贴花材料的纹理锚点（热点）。
seo-title: 锚记
solution: Experience Manager
title: 锚记
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 1e695882-f97a-4208-b595-2851b91bdbfe
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 3%

---


# 锚记{#anchor}

图像锚点（热点）。 指定可重复的纹理或贴花材料的纹理锚点（热点）。

`anchor= *``*, *`xy`*`

`anchorN= *``*, *`xnyn`*`

<table id="simpletable_1D8E91D8424A424787C4D20C9B040115"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> x</span>,  <span class="varname"> y</span> </p></td> 
  <td class="stentry"> <p>源图像左上角的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> xn</span>,  <span class="varname"> yn</span> </p></td> 
  <td class="stentry"> <p>从源图像中心标准化的偏移(real、real)。 </p></td> 
 </tr> 
</table>

可重复的纹理被应用到暗角对象，以便纹理锚点(`anchor=`)位于对象的纹理来源点。

倾斜图像被应用到暗角对象，以便倾斜锚点位于对象的倾斜来源点。 可以使用`pos=`命令进一步调整倾斜位置。

`anchorN=0,0` 将图像锚点放在源图像的中心。`anchorN=-0.5,-0.5` 或 `anchor=0,0` 者位于左上角， `anchorN=0.5,0.5` 并且位于源图像的右下角。

## 属性 {#section-91f929d35cd745ab9e1eeecf45fcedae}

**材料属性**。如果`align=2`，或者材料不是可重复的纹理、墙纸或贴胶，则忽略。

## 默认 {#section-b06d728c2f664c29bacf810eefcbde69}

`catalog::Anchor`, if the material is based on a catalog entry.否则，`anchor=0,0`（图像的左上角）用于可重复的纹理和壁纸，`anchorN=0,0`（图像的中心）用于装饰。

## 另请参阅 {#section-b18bf0b035644ca5aedebbc64373718e}

[catalog::Anchor](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab) ,  [align=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7)
