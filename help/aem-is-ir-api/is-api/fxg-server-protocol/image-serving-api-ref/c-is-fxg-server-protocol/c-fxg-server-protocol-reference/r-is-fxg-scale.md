---
description: 缩放图像。 相对于全分辨率图像按因子缩放图像。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 8%

---

# 比例{#scale}

缩放图像。 相对于全分辨率图像按因子缩放图像。

`scale= *`因子`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因子</span></span> </p> </td> 
  <td class="stentry"> <p>比例因子（实数，&gt;0）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-e9e53959b35844579f0f1d7721b71f8e}

如果未指定，则使用图像时不进行缩放。

## 示例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
