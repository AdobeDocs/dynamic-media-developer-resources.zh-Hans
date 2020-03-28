---
description: 路径文本属性。
seo-description: 路径文本属性。
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Scene7 Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# pathAttr{#pathattr}

路径文本属性。

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 方向 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 范 </span> 数|反 <span class="codeph"> 向 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>路径上的文本开始位置（实数0.0...1.0）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>路径上的文本结束位置（实数0.0...&lt;2.0）。 </p> </td> 
 </tr> 
</table>

指定 `norm` 从第一个路径顶点附近开始绘制文本， `reverse` 并从最后一个顶点附近开始沿相反方向绘制文本。

*`startPos`* 并 *`endPos`* 允许调整将绘制文本的路径位置。 0.0对应于路径中第一个顶点，1.0对应于最后一个顶点；中间值表示沿着第一顶点和最后一个顶点之间的路径的距离。

## 属性 {#section-80f266da4e2549d89f022a3f9ff4584d}

图层属性。 如果图层不包括和命令，则 `textPs=` 忽略 `textPath=` 该参数。

*`startPos`* 必须大于或等于0且小于1.0。当应 *`endPos`* 用到开放路径时， *`startPos`* 必须大于或等于1.0，或者当应用到闭合路径时，必须小于或等于( *`startPos`* + 1.0)。

## 默认 {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## 另请参阅 {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
