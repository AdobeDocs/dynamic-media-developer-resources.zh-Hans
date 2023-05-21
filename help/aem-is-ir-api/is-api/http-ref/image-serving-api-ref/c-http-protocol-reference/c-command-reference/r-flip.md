---
description: 反向圖層。 在套用crop=和rotate=和extend=之前，水準、垂直或兩者同時反向圖層。
solution: Experience Manager
title: 翻轉
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# 翻轉{#flip}

反向圖層。 在套用crop=和rotate=和extend=之前，水準、垂直或兩者同時反向圖層。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>水準翻轉圖層（左右翻轉）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>垂直翻轉圖層（由上到下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>水平與垂直翻轉。 </p> </td> 
 </tr> 
</table>

也可以套用至文字圖層。

某些命令，包括 `extend=`，在下列情況下，隱含套用至圖層0而非複合圖層： `layer=comp` 「 」已選取。 在這種情況下，所有自動指派給圖層0的指令都會在套用至的指令之前套用 `layer=comp`. 因此，當 `layer=comp`， `extend=` 之前套用 `flip=`.

>[!NOTE]
>
>翻轉的圖層是根據圖層錨點來定位；當錨點不位於圖層中心時，不同的翻轉值會導致不同的圖層位置。

## 屬性 {#section-294da2af7be746b5adfc35e29ee68217}

圖層指令。 套用至目前圖層或複合影像，如果 `layer=comp`. 被效果圖層忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ， [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
