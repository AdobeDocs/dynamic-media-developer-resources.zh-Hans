---
title: scl
description: 缩放视图。 相对于全分辨率晕影，按指定的缩放因子缩放渲染的图像。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e36db25c-af45-4256-b982-b7b06b87f5f9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 1%

---

# scl{#scl}

缩放视图。 相对于全分辨率晕影，按指定的缩放因子缩放渲染的图像。

`scl= *`invFactor`*`

<table id="simpletable_EFE352FA8EF14197B6934783A2883451"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> invFactor</span> </span> </p></td> 
  <td class="stentry"> <p>反比例因子（实数，1.0或更高）。 </p></td> 
 </tr> 
</table>

如果`scl=`在URL中的`wid=`或`hei=`之后，它将取消这些命令并`scl=`定义服务器返回的图像的大小。

但是，如果`wid=`或`hei=`在URL中的`scl=`之后，则它们取消`scl=`和`wid=`/`hei=`定义服务器返回的图像的大小。

>[!NOTE]
>
>如果计算的或默认的回复图像大小大于`attribute::MaxPix`，则返回错误。

## 属性 {#section-170458cbd6984bd59a3434431258b20f}

可能出现在请求中的任何位置。 如果在命令序列中的`scl=`之后发生`wid=`或`hei=`，则忽略该参数。

使用`scl=`调整图像大小不会更改响应图像中嵌入的打印分辨率值。

## 默认 {#section-d47ab3fb5a7d486a9fc207904b3e70dd}

如果未指定`wid=`、`hei=`或`scl=`，则回复图像将进行缩放以适应`attribute::DefaultPix`定义的大小。 如果`attribute::DefaultPix`为空，则回复图像的大小与晕影的视图图像相同。

## 另请参阅 {#section-cc5002a1d49340bbb5c7a5864c297621}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ，[hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)，[resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)，[attribute：：MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)，[attribute：：DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f)
