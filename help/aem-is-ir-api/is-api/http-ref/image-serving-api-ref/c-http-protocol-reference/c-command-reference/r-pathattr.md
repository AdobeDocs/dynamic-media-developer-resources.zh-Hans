---
description: 路径上文本属性。
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

路径上文本属性。

` pathAttr= *`方向`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 范数 </span> | <span class="codeph"> 反向 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>路径上的文本起始位置（实数0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>路径上的文本结束位置（实数0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定 `norm` 绘制从第一个路径顶点附近开始的文本，并 `reverse` 以反向绘制文本，从最后一个顶点附近开始。

*`startPos`* 和 *`endPos`* 允许调整文本在路径上的绘制位置。 0.0对应于路径中的第一个顶点，1.0对应于最后一个顶点；中间值表示沿着路径在第一个和最后一个顶点之间的距离。

## 属性 {#section-80f266da4e2549d89f022a3f9ff4584d}

层属性。 如果图层不包含，则忽略 `textPs=` 和 `textPath=` 命令。

*`startPos`* 必须大于或等于0且小于1.0。 *`endPos`* 必须大于 *`startPos`* 和小于或等于1.0（当应用于开放路径时），或者小于或等于( *`startPos`* + 1.0)。

## 默认 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另请参阅 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ， [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
