---
description: 翻转层。 在应用crop=后和rotate=和extend=前，水平、垂直或两者翻转图层。
seo-description: 翻转层。 在应用crop=后和rotate=和extend=前，水平、垂直或两者翻转图层。
seo-title: 翻转
solution: Experience Manager
title: 翻转
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# flip{#flip}

翻转层。 在应用crop=后和rotate=和extend=前，水平、垂直或两者翻转图层。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>水平翻转图层（从左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>垂直（向上向下）翻转图层。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>水平和垂直翻转。 </p> </td> 
 </tr> 
</table>

也可应用于文本图层。

选择`layer=comp`时，某些命令（包括`extend=`）会隐式应用到层0而不是复合层。 在这种情况下，自动分配给第0层的所有命令将在应用于`layer=comp`的命令之前应用。 因此，当`layer=comp`时，在`flip=`之前应用`extend=`。

>[!NOTE]
>
>翻转的图层基于图层锚点进行定位；当锚点不位于图层中心时，不同的flip=值将导致不同的图层位置。

## 属性 {#section-294da2af7be746b5adfc35e29ee68217}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
