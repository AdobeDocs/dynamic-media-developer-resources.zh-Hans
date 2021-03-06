---
description: JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的量），并间接地改变生成图像的视觉质量。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic，SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 6%

---

# qlt{#qlt}

JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的量），并间接地改变生成图像的视觉质量。

` qlt= *``*[, *`质量色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度下采样(0=normal， 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;值越高，文件大小和质量就越高，值越低，文件大小就越小，图像质量就越低。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置&#x200B;*`chroma`*&#x200B;标记以禁用典型JPEG编码器采用的RGB色度下采样。 当边缘由色相而不是亮度的变化来定义时，这可能会增加图像中边缘的感知锐度。 设置此标志可能会稍微增加文件大小。 如果文本看起来略微模糊，请尝试使用此设置。

## 属性 {#section-925a44cbdc9042db8d4eb149cd073d21}

请求属性。 无论当前的层设置如何，都适用。 如果输出图像文件格式不支持JPEG编码，则忽略。 有关哪些输出图像格式支持`qlt=`的信息，请参阅`fmt=`的说明。

*`chroma`* 如果输出像素类型为CMYK或灰色，则忽略此参数。

## 默认 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 示例 {#section-d7d33871d401433aa51d028823eae7a9}

通过低带宽连接降低传输质量：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高带宽连接的质量：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另请参阅 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，属 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
