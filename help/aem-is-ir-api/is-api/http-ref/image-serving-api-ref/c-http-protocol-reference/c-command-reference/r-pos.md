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

---


# pos{#pos}

图层位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>从此图层的来源到图层0来源的像素偏移(int, int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从此图层的来源到图层0来源的标准化偏移(real、real)。 </p></td> 
 </tr> 
</table>

对于图像、文本和纯色图层，指 `pos=` 定图层锚点相对于图层0锚点的位置。 `posN=` 坐标值相对于实际的0层矩形大小进行标准化。

如果是效果图层，则 `pos=` 会相对于父图层移动效果图层。

正值将图层向右／底部移动，向左／顶部移动负值。 `posN=0.5,0.5` 将图层向下和向右移动0宽度和高度的一半。

## 属性 {#section-51a60cdc52d040538fef378ace7c2e7d}

图层属性。 如果或， `layer=0` 则忽略 `layer=comp`。

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果图层是图像、文本或纯色图层，则这会将图层锚点放在与图层0锚点相同的位置。 将效果图层直接放置在其父图层上方或下方。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

请参阅模板中的 [示例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[来源=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
