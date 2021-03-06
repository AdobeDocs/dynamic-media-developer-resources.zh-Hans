---
description: 翻转图层。 在应用crop=和rotate=和extend=之前，水平、垂直或两者翻转图层。
solution: Experience Manager
title: 翻转
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 翻转{#flip}

翻转图层。 在应用crop=和rotate=和extend=之前，水平、垂直或两者翻转图层。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>水平翻转图层（从左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>垂直翻转图层（向上向下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>水平和垂直翻转。 </p> </td> 
 </tr> 
</table>

也可以应用于文本层。

一些命令，包括 `extend=`，在 `layer=comp` 中。 在这些情况下，自动分配给层0的所有命令都会应用于 `layer=comp`. 因此，当 `layer=comp`, `extend=` 在 `flip=`.

>[!NOTE]
>
>翻转层基于层锚定；当锚点不在层的中心时，不同flip=值将导致不同的层位置。

## 属性 {#section-294da2af7be746b5adfc35e29ee68217}

层命令。 应用于当前图层或复合图像(如果 `layer=comp`. 被效果层忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[旋转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
