---
title: 翻转
description: 翻转图层。 在应用crop=和rotate=和extend=之前水平、垂直或同时翻转图层。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 2%

---

# 翻转{#flip}

翻转图层。 在应用crop=和rotate=和extend=之前水平、垂直或同时翻转图层。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>水平翻转图层（从左到右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>垂直翻转图层（上下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">负载</span> </p> </td> 
  <td class="stentry"> <p>水平和垂直翻转。 </p> </td> 
 </tr> 
</table>

也可以将其应用于文本图层。

选择`layer=comp`时，某些命令（包括`extend=`）隐式应用于图层0而非复合图层。 在这种情况下，自动分配到层0的所有命令在应用于`layer=comp`的命令之前应用。 因此，当`layer=comp`时，`extend=`在`flip=`之前应用。

>[!NOTE]
>
>翻转的图层基于图层锚点定位。 当锚点不在图层中心时，不同的`flip=`值会导致不同的图层位置。

## 属性 {#section-294da2af7be746b5adfc35e29ee68217}

图层命令。 应用于当前图层或复合图像（如果`layer=comp`）。 被效果层忽略。

## 默认 {#section-502044f81a89492198d5f12a738459ea}

无。

## 另请参阅 {#section-47f6484deccd420983df15ec163b4a83}

[旋转=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ， [锚点=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
