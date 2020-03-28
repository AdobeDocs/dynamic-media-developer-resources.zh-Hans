---
description: Jpeg大小（以千字节为单位）。 指定JPEG响应的最大大小（以千字节为单位）。
seo-description: Jpeg大小（以千字节为单位）。 指定JPEG响应的最大大小（以千字节为单位）。
seo-title: jpegSize
solution: Experience Manager
title: jpegSize
topic: Scene7 Image Serving - Image Rendering API
uuid: 832163ca-0554-481d-b87f-bf322f415274
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# jpegSize{#jpegsize}

Jpeg大小（以千字节为单位）。 指定JPEG响应的最大大小（以千字节为单位）。

`jpegSize= *`大小`*`

<table id="simpletable_EC2A8D8B65854B45B9CB184DA1069355"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 大小</span></span> </p> </td> 
  <td class="stentry"> <p>大小（以千字节为单位）。 </p></td> 
 </tr> 
</table>

如果设置为正值，且具有指定JPEG质量的JPEG响应未超过此值，则该图像将作为响应返回。 否则，JPEG质量会降低，直到它生成的图像符合指定大小，或直到它确定它不适合。 在后一种情况下，请求失败并出现错误。

值0表示响应不受大小限制。

不允许使用负值。

## 属性 {#section-19e544e77d35478b98fe8666f27d6968}

请求属性。 无论当前图层设置如何，均可应用。 如果输出图像格式不是JPEG，则忽略该值。

## 默认 {#section-198b798ed187453197e0969c641d6fb5}

0

## 示例 {#section-46bf806fd3ef4875b7726df32b6f834d}

确保大小不会太大，无法交付到内存有限的设备：

`http://server/myRoodId/myImageId?qlt=60&wid=300&jpegSize=10`

## 另请参阅 {#section-98d472b39d6547969fce6dd86748c153}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a) ，属 [性：:JpegQuality](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-jpegquality.md#reference-4a879e7c46024c8a898a9fd226f9eb09)
