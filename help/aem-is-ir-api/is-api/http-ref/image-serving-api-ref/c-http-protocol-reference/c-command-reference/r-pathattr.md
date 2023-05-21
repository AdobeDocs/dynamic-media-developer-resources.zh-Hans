---
description: 路徑文字屬性。
solution: Experience Manager
title: pathAttr
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---

# pathAttr{#pathattr}

路徑文字屬性。

` pathAttr= *`方向`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 標準 </span> | <span class="codeph"> 反轉 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文字起始位置（實數0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>路徑上的文字結束位置（實數0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定 `norm` 繪製從第一個路徑頂點附近開始的文字，並 `reverse` 以相反方向繪製文字，從最後一個頂點附近開始。

*`startPos`* 和 *`endPos`* 允許調整繪製文字的路徑位置。 0.0對應於路徑中的第一個頂點，1.0對應於最後一個頂點；中間值表示沿著路徑在第一個和最後一個頂點之間的距離。

## 屬性 {#section-80f266da4e2549d89f022a3f9ff4584d}

圖層屬性。 如果圖層不包含，則忽略 `textPs=` 和 `textPath=` 命令。

*`startPos`* 必須大於或等於0且小於1.0。 *`endPos`* 必須大於 *`startPos`* 和小於或等於1.0 （當套用至開放路徑時）或小於或等於( *`startPos`* + 1.0)。

## 默认 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另请参阅 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
