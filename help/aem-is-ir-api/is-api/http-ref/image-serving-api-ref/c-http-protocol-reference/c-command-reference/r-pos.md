---
description: 图层位置。
solution: Experience Manager
title: pos
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 3%

---


# pos{#pos}

图层位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coord</span> </p> </td> 
  <td class="stentry"> <p>从此图层的来源到图层0来源的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>将此图层来源到图层0来源的偏移标准化（实数、实数）。 </p></td> 
 </tr> 
</table>

对于图像、文本和纯色图层，`pos=`指定图层锚点相对于图层0锚点的位置。 `posN=` 坐标值相对于实际图层0矩形大小进行标准化。

如果是效果图层，`pos=`会相对于父图层移动效果图层。

正值将图层向右/向下移动，向左/向上移动负值。 `posN=0.5,0.5` 将图层向下和向右移动0宽度和高度的一半。

## 属性 {#section-51a60cdc52d040538fef378ace7c2e7d}

图层属性。 如果`layer=0`或`layer=comp`，则忽略。

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`. 如果图层是图像、文本或纯色图层，则会将图层锚点放在与图层0锚点相同的位置。 将效果图层直接置于其父图层之上或之下。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

请参阅[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[来源=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
