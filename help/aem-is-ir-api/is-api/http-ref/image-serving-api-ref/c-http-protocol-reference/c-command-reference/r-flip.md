---
description: 翻转图层。 在应用crop=后和rotate=和extend=前，水平、垂直或两者翻转图层。
solution: Experience Manager
title: 翻转
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 3%

---


# flip{#flip}

翻转图层。 在应用crop=后和rotate=和extend=前，水平、垂直或两者翻转图层。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>水平翻转图层（从左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>垂直翻转图层（向上向下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud  </span> </p> </td> 
  <td class="stentry"> <p>水平和垂直翻转。 </p> </td> 
 </tr> 
</table>

也可应用于文本图层。

选择`layer=comp`时，某些命令（包括`extend=`）隐式应用于图层0而不是复合图层。 在这种情况下，自动分配给层0的所有命令将在应用于`layer=comp`的命令之前应用。 因此，当`layer=comp`时，`extend=`在`flip=`之前应用。

>[!NOTE]
>
>翻转的图层基于图层锚点定位；当锚点不位于图层中心时，不同的flip=值将导致不同的图层位置。

## 属性 {#section-294da2af7be746b5adfc35e29ee68217}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果图层忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
