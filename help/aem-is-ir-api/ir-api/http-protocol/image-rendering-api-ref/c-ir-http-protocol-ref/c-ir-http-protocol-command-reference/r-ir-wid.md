---
description: 回复图像宽度。 指定渲染后图像的缩放比例，使回复图像不高于指定值，同时保持图像的长宽比。
seo-description: 回复图像宽度。 指定渲染后图像的缩放比例，使回复图像不高于指定值，同时保持图像的长宽比。
seo-title: wid
solution: Experience Manager
title: wid
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# wid{#wid}

回复图像宽度。 指定渲染后图像的缩放比例，使回复图像不高于指定值，同时保持图像的长宽比。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>图像宽度（以像素为单位，int大于0）。 </p></td> 
 </tr> 
</table>

如果同时指定了`wid=`和`hei=`并且`wid`/ `hei`与图像的长宽比不同，则不填充图像。

`wid=` 并 `hei=` 共同定义服务器返回的图像大小。如果`scl=`位于URL中的`wid=`或`hei=`之后，它将取消这些命令，而`scl=`定义服务器返回的图像大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`之后出现，则它们将取消`scl=`和`wid=`/ `hei=`定义服务器返回的图像大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-2d067c6d371748e19cb157684700a49d}

可能在请求中的任何位置发生。 调整图像大小时，使用`wid=`、`hei=`或`scl=`不会更改嵌入在响应图像中的打印分辨率值。 如果`scl=`出现在命令序列中的`wid=`或`hei=`之后，则忽略。

## 默认 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

如果既未指定`wid=`、`hei=`和`scl=`，则将缩放回复图像以适合由`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小将与暗角的视图图像相同。

## 另请参阅 {#section-450dfc12b1d440e2a3172a69d91db51f}

[属性：:DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [属性：:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), scl [=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [Mode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
