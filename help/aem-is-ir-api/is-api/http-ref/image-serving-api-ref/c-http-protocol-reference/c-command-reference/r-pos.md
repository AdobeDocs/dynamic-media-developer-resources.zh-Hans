---
title: pos
description: 图层位置。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2e9a1f3-7216-4ab0-9c37-57f083119cef
TQID: 'https://experienceleague.adobe.com/9UMGN0TeM4mZ0IZI--dEA3KBYKOVhJxCJMZuPevlq8o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
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

`posN=0,0`. 如果是图像、文本或纯色图层，则此坐标会将图层锚点放置在与图层0锚点相同的位置。 将效果层直接置于其父层上方或下方。

## 示例 {#section-a89a02c22f6b4260bfcf7c842cd6069d}

查看[模板](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)中的示例A。

## 另请参阅 {#section-812d95575ba542808e8387d0a8650606}

[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)
