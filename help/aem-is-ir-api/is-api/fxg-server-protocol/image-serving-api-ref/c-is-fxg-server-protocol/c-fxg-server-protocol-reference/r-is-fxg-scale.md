---
description: 缩放图像。 相对于全分辨率图像按因子缩放图像。
seo-description: 缩放图像。 相对于全分辨率图像按因子缩放图像。
seo-title: scale
solution: Experience Manager
title: 缩放
uuid: db5bab94-e5c1-41fe-ab1b-5c62b6a798d0
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 7%

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

如果未指定，则使用图像时不进行缩放。

## 示例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
