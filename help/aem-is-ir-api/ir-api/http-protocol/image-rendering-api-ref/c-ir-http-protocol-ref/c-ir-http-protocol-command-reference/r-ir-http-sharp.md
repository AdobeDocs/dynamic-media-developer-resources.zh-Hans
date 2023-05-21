---
title: 銳利化
description: 銳利化紋理。 指定呈現此材質時要套用的銳利化。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7921ceba-e249-4aab-823e-c54705c4a7c3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 5%

---

# 銳利化{#sharp}

銳利化紋理。 指定呈現此材質時要套用的銳利化。

`sharp=0|1|2|3`

<table id="simpletable_04B4EAA7CE7D4ED48A61A50CD001388F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>不銳利化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>一般銳利化（延遲）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>0替代銳利化（早期）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>更銳利化（早和晚）。 </p> </td> 
 </tr> 
</table>

`sharp=1` 在材質演算後套用銳利化； `sharp=2` 在紋理的初始縮放之後，但在轉換為場景之前套用銳利化； `sharp=3` 在變形前後都套用銳利化。

銳利化演演算法、銳利化量及其他USM （非銳利化遮色片）引數是由暈映提供的預設材質範本控制，或使用 `rs=`.

## 屬性 {#section-498ec9fcb8eb415fb99532d36c11d4c7}

材質屬性。 被純色材料忽略。

## 默认 {#section-febfa16e65864987b4d328e2ff1df64d}

`catalog::Sharp`，如果材質是以目錄專案為基礎，否則 `attribute::Sharp`.

## 另请参阅 {#section-0d5e2c94342c4ee586374ad9c917eeb9}

[catalog：：Sharp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0) ， [銳利化=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharpen.md#reference-13034d22d176483cb99ccafc2a4f6a6e)， [rs=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rs.md#reference-d20cefaaa6cd4f449d1591c87959b4cf)
