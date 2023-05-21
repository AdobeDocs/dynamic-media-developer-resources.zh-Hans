---
description: 縮放影像。 相對於完整解析度影像，以係數縮放影像。
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 89701a15-a0b6-460d-b0c1-5e25f3305380
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 9%

---

# scale{#scale}

縮放影像。 相對於完整解析度影像，以係數縮放影像。

`scale= *`因數`*`

<table id="simpletable_AC0974B79E064BA99C1F76461BDE808A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 因數</span></span> </p> </td> 
  <td class="stentry"> <p>縮放因數（實數， &gt;0）。 </p></td> 
 </tr> 
</table>

## 默认 {#section-e9e53959b35844579f0f1d7721b71f8e}

如果未指定，則會使用影像而不縮放比例。

## 示例 {#section-d5526953d6434c58bb2388bd936c13b5}

[!DNL http://server/is/agm/myRootId/myImageId?scale=.5]
