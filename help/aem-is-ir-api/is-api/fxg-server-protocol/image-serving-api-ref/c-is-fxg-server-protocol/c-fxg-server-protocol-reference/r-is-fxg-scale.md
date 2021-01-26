---
description: 缩放图像。 相对于全分辨率图像按因子缩放图像。
seo-description: 缩放图像。 相对于全分辨率图像按因子缩放图像。
seo-title: scale
solution: Experience Manager
title: 规模
topic: Dynamic Media Image Serving - Image Rendering API
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 9%

---


# scale{#scale}

缩放图像。 相对于全分辨率图像按因子缩放图像。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>缩放因子（实数，&gt;0）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-e9e53959b35844579f0f1d7721b71f8e}

如果未指定，则不使用缩放来使用图像。

## 示例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
