---
description: 缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。
seo-description: 缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。
seo-title: scl
solution: Experience Manager
title: scl
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 04839c44-01b6-4fa2-9eda-bbb0f2822db4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---


# scl{#scl}

缩放视图。 相对于全分辨率暗角，按指定的缩放因子缩放渲染的图像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>反比例因子（实数、1.0或更大）。 </p></td> 
 </tr> 
</table>

如果`scl=`位于URL中的`wid=`或`hei=`之后，它将取消这些命令，而`scl=`定义服务器返回的图像大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`之后出现，则它们将取消`scl=`和`wid=`/ `hei=`定义服务器返回的图像大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-170458cbd6984bd59a3434431258b20f}

可能在请求中的任何位置发生。 如果在命令序列中的`scl=`之后出现`wid=`或`hei=`，则忽略。

调整图像大小时使用`scl=`不会更改嵌入在响应图像中的打印分辨率值。

## 默认 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果既未指定`wid=`、`hei=`也未指定`scl=`，则将缩放回复图像以适合由`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小与暗角的视图图像相同。

## 另请参阅 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [resMode=,](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)属性： [:MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)，属性：: [DefaultPixPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
