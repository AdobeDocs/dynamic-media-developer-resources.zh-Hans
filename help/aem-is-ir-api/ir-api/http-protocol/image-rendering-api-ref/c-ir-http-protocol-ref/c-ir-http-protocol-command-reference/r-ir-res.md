---
title: res
description: 材質解析度。 指定可重複紋理或貼花影像的解析度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f207355d-5819-47fc-bda5-27a411449569
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 2%

---

# res{#res}

材質解析度。 指定可重複紋理或貼花影像的解析度。

` res= *`val`*`

<table id="simpletable_2004B804D46E43C090E59BBFF8144598"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>解析度；材質解析度單位（通常每英吋畫素） （實數）。 </p> </td> 
 </tr> 
</table>

如果有貼花材料， `size=` 如果兩者皆有，則為優先 `size=` 和 `res=` 已指定。

## 屬性 {#section-6a458ddc202f46e0b668c9f040a65cef}

材質屬性。 被純色材料忽略。 只有在使用材質時，才能透過封櫃和視窗覆蓋材料。

## 默认 {#section-ee4088a994014df59105fc1dbb2aa042}

`catalog::Resolution`，如果材質是以目錄專案為基礎，否則 `attribute::Resolution`，若為 `res= is` 未指定或設定為小於或等於0的值。

## 另请参阅 {#section-c00f6fb7b3e74719ac361de9a9ce4e52}

[材質解析度](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-material-resolution.md#concept-f60103c64e324e2cae78bd76dfb4de8b)， [size=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)， [catalog：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7)， [attribute：：Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
