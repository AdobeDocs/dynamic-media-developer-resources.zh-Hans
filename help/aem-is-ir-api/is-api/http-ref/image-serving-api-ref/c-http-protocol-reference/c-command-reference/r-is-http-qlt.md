---
description: JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据量），并间接改变生成图像的视觉质量。
seo-description: JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据量），并间接改变生成图像的视觉质量。
seo-title: qlt
solution: Experience Manager
title: qlt
uuid: 9f69845d-3b25-41a7-b6c0-83cf1d2bc450
feature: Dynamic Media Classic，SDK/API
role: 开发人员，商业从业者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 5%

---


# qlt{#qlt}

JPEG质量。 指定JPEG编码属性以控制压缩级别。 这进而会改变文件大小（回复数据量），并间接改变生成图像的视觉质量。

` qlt= *``*[, *`色度`*]`

<table id="simpletable_FB8090D4BEBF42FD83A64A7AAB6D7F92"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 质量 </span> </p> </td> 
  <td class="stentry"> <p>JPEG编码质量(1...100 int)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 色度  </span> </p> </td> 
  <td class="stentry"> <p>JPEG色度缩减采样(0=normal， 1=disable);可选，默认值为0。 </p> </td> 
 </tr> 
</table>

*`quality`*&#x200B;值越高，文件大小和质量越高，值越低，文件大小越小，图像质量越低。 如果值大于 90，所产生的图像往往与未解压缩图像几乎没有区别。

设置&#x200B;*`chroma`*&#x200B;标志以禁用典型JPEG编码器采用的RGB色度缩减采样。 当边缘由色相而不是亮度的变化来定义时，这可能会增加图像中边缘的感知锐度。 设置此标志可能会使文件大小略有增加。 如果文本看起来略微模糊，则尝试使用此设置。

## 属性 {#section-925a44cbdc9042db8d4eb149cd073d21}

请求属性。 无论当前图层设置如何，均适用。 如果输出图像文件格式不支持JPEG编码，则忽略。 有关输出图像格式支持`qlt=`的信息，请参阅`fmt=`的说明。

*`chroma`* 如果输出像素类型为CMYK或灰色，则忽略此值。

## 默认 {#section-0d8aa45d84df49e6b846596bbaf7f740}

`attribute::JpegQuality`

## 示例 {#section-d7d33871d401433aa51d028823eae7a9}

通过低带宽连接降低传输质量：

`http://server/myRoodId/myImageId?qlt=60&wid=300`

提高高带宽连接的质量：

`http://server/myRootId/myImageId?qlt=95,1&wid=300`

## 另请参阅 {#section-0074a060bb314ddfa7f4ed23be976507}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) , [属性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
