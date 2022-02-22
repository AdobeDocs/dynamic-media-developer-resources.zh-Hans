---
title: qlt
description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 49af2620-081f-4bcc-8245-5aa6bab89a05
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 7%

---

# qlt{#qlt}

Jpeg质量。 指定JPEG编码属性以控制压缩级别。

` qlt= *`质量`*[. *`色度`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下采样(0=normal， 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

指定JPEG编码属性以控制压缩级别。 这反过来会改变文件大小（回复数据的量），并间接地改变生成图像的视觉质量。

较高 *`quality`* 值会增加文件大小和质量，值越小，文件大小越小，图像质量越低。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置 *`chroma`* 标记，以禁用典型JPEG编码器使用的色度下采样。 当边缘由色相而不是亮度的变化来定义时，该设置可能会增加图像中边缘的感知锐度。 设置此标志可能会稍微增加文件大小。 如果文本看起来略微模糊，请尝试使用此设置。

## 属性 {#section-897b61c786dd4230a2c5807f2f40e722}

可能会在请求中的任意位置发生。

如果输出图像格式不支持JPEG压缩，则忽略。 请参阅 `fmt=` 以获取支持JPEG压缩的输出图像格式列表。

## 默认 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 另请参阅 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [属性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
