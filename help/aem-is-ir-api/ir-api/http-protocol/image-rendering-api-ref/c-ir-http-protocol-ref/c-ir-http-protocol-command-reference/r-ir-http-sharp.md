---
description: 锐化纹理。 指定渲染此素材时要应用的锐化。
seo-description: 锐化纹理。 指定渲染此素材时要应用的锐化。
seo-title: 锐
solution: Experience Manager
title: 锐
uuid: 8265eebf-9cec-4ad3-8b22-0f46f33a89f1
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 5%

---


# sharp{#sharp}

锐化纹理。 指定渲染此素材时要应用的锐化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>无需锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>正常锐化（延迟）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0个备用锐化（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更锐化（早、晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1` 在渲染材料后应用锐化； `sharp=2` 在纹理初始缩放后应用锐化，但在将其转换为场景之前应用； `sharp=3` 在变换前后应用锐化。

锐化算法和锐化量以及其他USM（USM锐化）参数由晕影提供的默认材料模板或`rs=`控制。

## 属性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材料属性。 被纯色材料忽略。

## 默认 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`, if the material is based on a catalog entry， oftherse  `attribute::Sharp`

## 另请参阅 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog::Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ,  [sharpen=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e),  [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
