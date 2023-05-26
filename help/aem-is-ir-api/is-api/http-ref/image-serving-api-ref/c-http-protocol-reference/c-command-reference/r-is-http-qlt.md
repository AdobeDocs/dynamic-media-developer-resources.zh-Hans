---
description: JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。
solution: Experience Manager
title: qlt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2a611a8-f331-4e01-a262-34340ce67b21
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 6%

---

# qlt{#qlt}

JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据的数量），并间接改变生成图像的视觉质量。

` qlt= *`品质`*[, *`色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>编码质量JPEG(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度 </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度缩减像素采样（0=正常，1=禁用）；可选，默认值为0。 </p> </td> 
 </tr> 
</table>

更高 *`quality`* 值会增加文件大小和质量，值越小，文件大小越小，感知到的图像质量也越低。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置 *`chroma`* 用于禁用典型JPEG编码器采用的RGB色度缩减采样的标志。 当边缘由色相变化而不是亮度变化定义时，这可以提高图像中边缘的感知锐度。 设置此标志可能会导致文件大小略有增加。 如果文本看起来稍微模糊，请尝试使用此设置。

## 属性 {#section-925a44cbdc9042db8d4eb149cd073d21}

请求属性。 无论当前图层设置如何，均适用。 如果输出图像文件格式不支持JPEG编码，则忽略。 请参阅 `fmt=` 有关哪些输出图像格式支持的信息 `qlt=`.

*`chroma`* 如果输出像素类型为CMYK或灰度，则会被忽略。

## 默认 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 示例 {#section-d7d33871d401433aa51d028823eae7a9}

降低通过低带宽连接进行更快传输的质量：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高带宽连接的质量：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另请参阅 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ， [attribute：：JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
