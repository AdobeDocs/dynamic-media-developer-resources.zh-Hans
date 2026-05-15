---
title: hei
description: 回复图像高度。 指定渲染图像的缩放比例，以使回复图像的高度不大于指定值，同时保持图像的宽高比。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
TQID: 'https://experienceleague.adobe.com/-sH3rlYycsZ36DheRgEpMUm6xSuUnY7s-3awUgdfloA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 1%

---

# hei{#hei}

回复图像高度。 指定渲染图像的缩放比例，以使回复图像的高度不大于指定值，同时保持图像的宽高比。

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span> </span> </p></td> 
  <td class="stentry"> <p>回复图像高度，以像素为单位（大于0的整数）。 </p></td> 
 </tr> 
</table>

如果同时指定了`wid=`和`hei=`，且宽度/高度与图像的纵横比不同，则不会填充图像。

`wid=`和`hei=`共同定义服务器返回的映像的大小。 如果`scl=`在URL中的`wid=`或`hei=`之后，它将取消这些命令并`scl=`定义服务器返回的图像的大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`之后，则它们取消`scl=`和`wid=`/`hei=`定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能出现在请求中的任何位置。 使用`wid=`、`hei=`或`scl=`调整图像大小不会更改响应图像中嵌入的打印分辨率值。 如果命令序列中的`scl=`出现在`wid=`和/或`hei=`之后，则忽略此项。

## 默认 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果未指定`wid=`、`hei=`或`scl=`，则回复图像将进行缩放以适应`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小与晕影的视图图像相同。

## 另请参阅 {#section-7ba51379f1e2421c92d3592d20a37734}

[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ，[attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)，[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec)，[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)，[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
