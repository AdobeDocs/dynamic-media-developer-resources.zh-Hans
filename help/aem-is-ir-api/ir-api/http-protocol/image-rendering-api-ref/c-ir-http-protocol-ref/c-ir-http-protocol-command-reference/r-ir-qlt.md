---
description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。
seo-description: Jpeg质量。 指定JPEG编码属性以控制压缩级别。
seo-title: qlt
solution: Experience Manager
title: qlt
topic: Scene7 Image Serving - Image Rendering API
uuid: 46f5b0da-7fe7-4daf-947b-bb5f5f5f5e6d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# qlt{#qlt}

Jpeg质量。 指定JPEG编码属性以控制压缩级别。

` qlt= *`质`*[. *`量色度`*]`

<table id="simpletable_A245B6A3D2374A6A89DE63A5621CFEC0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度缩减采样(0=normal, 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据量），并间接改变生成图像的视觉质量。

Higher *`quality`* values increase file size and quality, lower values decrease file sizes and reduce perceived image quality. 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置标 *`chroma`* 志以禁用典型JPEG编码器采用的色度缩减采样。 当边缘由色相而不是亮度的变化来定义时，这可能会增加图像中边缘的感知锐度。 设置此标志可能会导致文件大小略有增加。 如果文本看起来略微模糊，则尝试使用此设置。

## 属性 {#section-897b61c786dd4230a2c5807f2f40e722}

可能在请求中的任何位置发生。

如果输出图像格式不支持JPEG压缩，则忽略该参数。 有关支持JPEG压 `fmt=` 缩的输出图像格式列表，请参阅的说明。

## 默认 {#section-1c1257df843c475bbac6aadaffcb6347}

`attribute::JpegQuality`

## 另请参阅 {#section-61871fbded3a42f68cf3bdcaed35eae1}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c)，属 [性：:JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50)
