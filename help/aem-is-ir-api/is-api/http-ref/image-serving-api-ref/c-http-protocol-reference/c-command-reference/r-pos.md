---
title: pos
description: 图层位置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 2%

---

# pos{#pos}

图层位置。

pos= *`coord`*

posN= *`coordN`*

<table id="simpletable_754F76EE00BF4129B07502647FF172B7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">坐标</span> </p> </td> 
  <td class="stentry"> <p>从该图层原点到图层0原点的像素偏移(int， int)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> coordN</span> </p></td> 
  <td class="stentry"> <p>从此图层原点到图层0原点的归一化偏移（实际、实际）。 </p></td> 
 </tr> 
</table>

如果有图像、文本和纯色图层，则`pos=`指定图层锚点相对于图层0锚点的位置。 `posN=`坐标值是相对于实际图层0矩形大小进行规范化的。

如果有效果层，则`pos=`将效果层相对于父层移动。

正值将图层向右/下移动，而负值向左/上移动。 在`posN=0.5,0.5`中，它将图层0宽度和高度上下移动一半。

## 属性 {#section-51a60cdc52d040538fef378ace7c2e7d}

层属性。 如果`layer=0`或`layer=comp`则忽略。

## 默认 {#section-70a6bc71ded5494e843194dfb6bf5a6c}

`posN=0,0`。 如果是图像、文本或纯色图层，则此坐标会将图层锚点放置在与图层0锚点相同的位置。 将效果层直接置于其父层上方或下方。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

查看[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
