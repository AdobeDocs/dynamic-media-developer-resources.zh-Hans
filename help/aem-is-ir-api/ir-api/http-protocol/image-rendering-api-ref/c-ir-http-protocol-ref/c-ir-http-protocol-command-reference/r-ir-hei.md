---
title: hei
description: 回复图像高度。 指定渲染图像的缩放比例，以使回复图像的高度不大于指定的值，同时保持图像的宽高比。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

回复图像高度。 指定渲染图像的缩放比例，以使回复图像的高度不大于指定的值，同时保持图像的宽高比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>回复图像高度，以像素为单位（大于0的整数）。 </p></td> 
 </tr> 
</table>

如果两者都有，则图像不会填充 `wid=` 和 `hei=` 指定且宽度/高度与图像的纵横比不同。

`wid=` 和 `hei=` 共同定义服务器返回的图像的大小。 如果 `scl=` 之后 `wid=` 或 `hei=` 在URL中，它会取消这些命令并 `scl=` 定义服务器返回的图像的大小。

但是，如果 `wid=` 或 `hei=` 之后 `scl=` 在URL中，他们会取消 `scl=` 和 `wid=`/ `hei=` 定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于 `attribute::MaxPix`.

## 属性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能出现在请求中的任意位置。 调整图像大小 `wid=`， `hei=`，或 `scl=` 不会更改响应图像中嵌入的打印分辨率值。 忽略条件 `scl=` 发生于 `wid=` 和/或 `hei=` 在命令序列中。

## 默认 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果 `wid=`， `hei=`，或 `scl=` 未指定，回复图像将进行缩放以适合由定义的大小 `attribute::DefaultPix`. 如果 `attribute::DefaultPix` 为空，则回复图像的大小与晕影的视图图像相同。

## 另请参阅 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ， [attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)， [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)， [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)， [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
