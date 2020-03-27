---
description: 回复图像高度。 指定对渲染后的图像进行缩放，使回复图像的高度不大于指定值，同时保持图像的长宽比。
seo-description: 回复图像高度。 指定对渲染后的图像进行缩放，使回复图像的高度不大于指定值，同时保持图像的长宽比。
seo-title: hei
solution: Experience Manager
title: hei
topic: Scene7 Image Serving - Image Rendering API
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# hei{#hei}

回复图像高度。 指定对渲染后的图像进行缩放，使回复图像的高度不大于指定值，同时保持图像的长宽比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>返回图像高度（以像素为单位）（大于0的整数）。 </p></td> 
 </tr> 
</table>

如果同时指定和指定 `wid=` ，并且 `hei=` 宽度／高度不同于图像的长宽比，则不填充图像。

`wid=` 并 `hei=` 共同定义服务器返回的图像大小。 如 `scl=` 果URL后 `wid=` 面或 `hei=` URL中出现，则会取消这些命令，并 `scl=` 定义服务器返回的图像大小。

但是，如 `wid=` 果URL中 `hei=` 或之后 `scl=` 出现，它们将取消并 `scl=` / `wid=``hei=` 定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于，则返回错误 `attribute::MaxPix`。

## 属性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能发生在请求内的任何位置。 调整图像大小 `wid=`时， `hei=`或 `scl=` 不更改嵌入在响应图像中的打印分辨率值。 如果在命 `scl=` 令序列中 `wid=` 和／或 `hei=` 之后发生，则忽略。

## 默认 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果既 `wid=`未指定 `hei=`、也未指 `scl=` 定，则缩放回复图像以适合由定义的大小 `attribute::DefaultPix`。 如 `attribute::DefaultPix` 果为空，则回复图像的大小与暗角的视图图像相同。

## 另请参阅 {#section-7ba51379f1e2421c92d3592d20a37734}

[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ，属 [性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), wid= [, scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
