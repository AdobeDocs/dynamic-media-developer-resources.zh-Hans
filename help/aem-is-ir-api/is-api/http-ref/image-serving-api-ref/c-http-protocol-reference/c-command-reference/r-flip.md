---
description: 反向图层。 在应用crop=和rotate=和extend=之前水平、垂直或同时翻转图层。
solution: Experience Manager
title: 翻转
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# 翻转{#flip}

反向图层。 在应用crop=和rotate=和extend=之前水平、垂直或同时翻转图层。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>水平翻转图层（左右翻转）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>垂直翻转图层（上下翻转）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>水平和垂直翻转。 </p> </td> 
 </tr> 
</table>

也可以应用于文本图层。

一些命令，包括 `extend=`时，隐式应用于图层0而不是复合图层 `layer=comp` 已选中。 在此类情况下，自动分配到层0的所有命令都会在应用于的命令之前应用 `layer=comp`. 因此，当 `layer=comp`， `extend=` 之前应用 `flip=`.

>[!NOTE]
>
>翻转的图层基于图层锚点定位；当锚点不位于图层中心时，不同的翻转值将导致不同的图层位置。

## 属性 {#section-294da2af7be746b5adfc35e29ee68217}

“图层”命令。 应用于当前图层或复合图像，如果 `layer=comp`. 被效果层忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[旋转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ， [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
