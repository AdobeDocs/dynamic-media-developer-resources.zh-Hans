---
description: 图层位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic，SDK/API
role: Developer,Business Practitioner
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---

# pos{#pos}

图层位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>从此层原点到0原点的像素偏移(int，int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从此层原点到0层原点的标准化偏移（实、实）。 </p></td> 
 </tr> 
</table>

对于图像、文本和纯色层，`pos=`指定层锚点相对于层0锚点的位置。 `posN=` 坐标值相对于实际的0层直接大小进行标准化。

对于效果层，`pos=`会相对于父层移动效果层。

正值将层向右/下移动，向左/上移动负值。 `posN=0.5,0.5` 将图层向下和向右移动0宽度和高度的一半。

## 属性 {#section-51a60cdc52d040538fef378ace7c2e7d}

层属性。 如果为`layer=0`或`layer=comp`，则忽略。

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果图层是图像、文本或纯色图层，则会将图层锚点放置在与图层0锚点相同的位置。 将效果层直接放置在其父层上或下。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

请参阅[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
