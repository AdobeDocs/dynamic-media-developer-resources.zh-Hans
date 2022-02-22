---
title: 锐
description: 锐化纹理。 指定渲染此材料时要应用的锐化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 6%

---

# 锐{#sharp}

锐化纹理。 指定渲染此材料时要应用的锐化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>无锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>正常锐化（延迟）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0次备用锐化（提前）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更锐化（早、晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1` 在渲染材料后应用锐化； `sharp=2` 在初始缩放纹理后，但在将其转换为场景之前应用锐化； `sharp=3` 在转换前后均应用锐化。

锐化算法和锐化量以及其他USM（USM锐化）参数由晕影提供或通过 `rs=`.

## 属性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材料属性。 被纯色材料忽略。

## 默认 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`，否则 `attribute::Sharp`.

## 另请参阅 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[目录：:Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) , [锐化=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e), [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
