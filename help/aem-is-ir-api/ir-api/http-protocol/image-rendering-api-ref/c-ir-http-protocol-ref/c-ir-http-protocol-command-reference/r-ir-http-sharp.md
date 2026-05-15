---
title: 锐化
description: 锐化纹理。 指定渲染此材质时要应用的锐化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
TQID: 'https://experienceleague.adobe.com/AWUw6E0xSWAsMfijewBvnSC8JdM5l9-qtFNLZsweFRY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 5%

---

# 锐化{#sharp}

锐化纹理。 指定渲染此材质时要应用的锐化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>不锐化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>普通锐化（延迟）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0备用锐化（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更锐化（早和晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1`在呈现材质后应用锐化；`sharp=2`在纹理的初始缩放之后但在将其转换为场景之前应用锐化；`sharp=3`在转换之前和之后应用锐化。

锐化算法、锐化量和其他USM（钝化蒙版）参数由晕影提供的默认材质模板或通过`rs=`进行控制。

## 属性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材质属性。 已被纯色材料忽略。

## 默认 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`，如果材料基于目录条目，否则`attribute::Sharp`。

## 另请参阅 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[目录：：锐化](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0)，[锐化=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e)，[rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
