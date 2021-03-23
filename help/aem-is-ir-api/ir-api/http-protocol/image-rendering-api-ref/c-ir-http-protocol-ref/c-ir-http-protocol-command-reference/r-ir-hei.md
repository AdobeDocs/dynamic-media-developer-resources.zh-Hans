---
description: 回复图像高度。 指定渲染后的图像的缩放，以便返回图像的高度不大于指定值，同时保持图像的长宽比。
seo-description: 回复图像高度。 指定渲染后的图像的缩放，以便返回图像的高度不大于指定值，同时保持图像的长宽比。
seo-title: hei
solution: Experience Manager
title: 平
uuid: 616d3306-ccbd-4400-8a94-1ff6f47b802e
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 2%

---


# hei{#hei}

回复图像高度。 指定渲染后的图像的缩放，以便返回图像的高度不大于指定值，同时保持图像的长宽比。

`hei= *`瓦尔`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 瓦尔</span> </span> </p></td> 
  <td class="stentry"> <p>返回图像高度（以像素为单位，整数大于0）。 </p></td> 
 </tr> 
</table>

如果同时指定了`wid=`和`hei=`并且宽度/高度不同于图像的长宽比，则不填充图像。

`wid=` 并 `hei=` 共同定义服务器返回的图像大小。如果`scl=`位于URL中的`wid=`或`hei=`之后，它将取消这些命令，而`scl=`定义服务器返回的图像大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`后面，则它们会取消`scl=`，而`wid=`/ `hei=`定义服务器返回的图像大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-6cbc6acd37c847beab84c896ac25280c}

可能发生在请求中的任何位置。 调整具有`wid=`、`hei=`或`scl=`的图像大小不会更改嵌入在响应图像中的打印分辨率值。 如果`scl=`在命令序列中的`wid=`和/或`hei=`之后出现，则忽略。

## 默认 {#section-61043f6c1f5d450883ff9e5eafd95955}

如果未指定`wid=`、`hei=`和`scl=`，则会缩放回复图像以适合由`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小与晕影的视图图像相同。

## 另请参阅 {#section-7ba51379f1e2421c92d3592d20a37734}

[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), scl [=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),   [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
