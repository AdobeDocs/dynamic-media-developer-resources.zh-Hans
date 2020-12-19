---
description: 图层位置。
seo-description: 图层位置。
seo-title: pos
solution: Experience Manager
title: pos
topic: Scene7 Image Serving - Image Rendering API
uuid: e9872ce9-5c47-49c5-9c87-4fa8441c4770
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---


# pos{#pos}

图层位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 坐标</span> </p> </td> 
  <td class="stentry"> <p>从此图层的来源到图层0来源的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从此层的来源到层0来源的标准化偏移(real、real)。 </p></td> 
 </tr> 
</table>

对于图像、文本和纯色图层，`pos=`指定图层锚点相对于图层0锚点的位置。 `posN=` 坐标值相对于实际图层0矩形大小进行标准化。

如果是效果层，`pos=`会相对于父层移动效果层。

正值将图层向右／向下移动，向左／向上移动负值。 `posN=0.5,0.5` 向下和向右移动图层0宽度和高度的一半。

## 属性 {#section-51a60cdc52d040538fef378ace7c2e7d}

图层属性。 如果`layer=0`或`layer=comp`，则忽略。

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果图层是图像、文本或纯色图层，则这会将图层锚点放在与图层0锚点相同的位置。 将效果图层直接置于其父图层之上或之下。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[来源=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
