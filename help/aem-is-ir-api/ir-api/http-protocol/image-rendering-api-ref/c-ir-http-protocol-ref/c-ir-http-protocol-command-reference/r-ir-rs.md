---
title: rs
description: 進階演算設定。 指定呈現目前選取範圍時要套用的進階演算設定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 419baeb7-e06e-4753-a487-a1f407845f6d
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# rs{#rs}

進階演算設定。 指定呈現目前選取範圍時要套用的進階演算設定。

`rs= *`val`*`

<table id="simpletable_4B028996E5824FC18B9749D1A6A3C2E3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>演算設定字串。 </p></td> 
 </tr> 
</table>

用於微調演算器外觀。 若要建立演算設定字串，請使用暈映製作工具的演算功能(Dynamic Media影像製作套件的一部分)。

## 屬性 {#section-9a2b2228789046658cb80eddf343af75}

材質屬性。

## 默认 {#section-f4751476c3134f16ac6283d6f0c46e47}

`catalog::RenderSettings`.

## 示例 {#section-47e4811882574441a4d517e42a35f352}

在「影像製作」中做了一些實驗之後，我們判斷不銳利化遮色片(USM)為指定的應用程式和材質提供了正確的銳利化量。 設定USM的轉譯器設定字串會複製到 `rs=` 要與此材料一起使用的命令：

`…&rs=U2V20W50X2&…`

## 另请参阅 {#section-930116e735024a008c994547ba36ee40}

[catalog：：RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711)
