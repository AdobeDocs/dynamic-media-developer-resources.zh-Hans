---
title: wid
description: 回复图像宽度。 指定渲染图像的缩放比例，以使回复图像不高于指定值，同时保持图像的宽高比。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 1%

---

# wid{#wid}

回复图像宽度。 指定渲染图像的缩放比例，以使回复图像不高于指定值，同时保持图像的宽高比。

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">值</span> </p> </td> 
  <td class="stentry"> <p>图像宽度，以像素为单位（int大于0）。 </p></td> 
 </tr> 
</table>

如果同时指定了`wid=`和`hei=`，并且`wid`/`hei`与图像的长宽比不同，则不会填充图像。

`wid=`和`hei=`共同定义服务器返回的映像的大小。 如果`scl=`在URL中的`wid=`或`hei=`之后，它将取消这些命令并`scl=`定义服务器返回的图像的大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`之后，则它们取消`scl=`和`wid=`/`hei=`定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-2d067c6d371748e19cb157684700a49d}

可能出现在请求中的任何位置。 使用`wid=`、`hei=`或`scl=`调整图像大小不会更改响应图像中嵌入的打印分辨率值。 如果命令序列中的`scl=`出现在`wid=`或`hei=`之后，则忽略。

## 默认 {#section-c7c6efa03d864592a3398b6f1de5a0b0}

如果未指定`wid=`、`hei=`或`scl=`，则回复图像将进行缩放以适应`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小与晕影的视图图像相同。

## 另请参阅 {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ，[attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)，[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，[scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29)，[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
